---
title: Suchen Sie nach AutoErmittlung-Endpunkten mithilfe von SCP-Suche in Exchange
manager: kelbow
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: b24228a8-5127-4bac-aef0-9c9e8843c9ff
description: Erfahren Sie, wie Sie AutoErmittlungs-SCP-Objekte in Active Directory-Domänendienste (AD DS) suchen und verwenden, um AutoErmittlungsendpunkt-URLs für die Verwendung mit dem Exchange-AutoErmittlungsdienst zu suchen.
ms.openlocfilehash: 59fd316d0aa0feea81b60c279040da018c51b47d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19756885"
---
# <a name="find-autodiscover-endpoints-by-using-scp-lookup-in-exchange"></a>Suchen Sie nach AutoErmittlung-Endpunkten mithilfe von SCP-Suche in Exchange

Erfahren Sie, wie Sie AutoErmittlungs-SCP-Objekte in Active Directory-Domänendienste (AD DS) suchen und verwenden, um AutoErmittlungsendpunkt-URLs für die Verwendung mit dem Exchange-AutoErmittlungsdienst zu suchen.
  
AutoErmittlung vereinfacht das Abrufen von Informationen, die Sie zum Herstellen von Verbindungen mit Postfächern auf Exchange-Servern benötigen. Um AutoErmittlung verwenden zu können, benötigen Sie jedoch ein Verfahren zum Suchen nach AutoErmittlungsservern, die für den Benutzer geeignet sind, dessen Einstellungen Sie abrufen. SCP-Objekte (Service Connection Point, Dienstverbindungspunkt) in AD DS bieten der Domäne beigetretenen Clients eine einfache Möglichkeit zum Suchen nach AutoErmittlungsservern. 
  
## <a name="get-set-up-to-find-autodiscover-endpoints"></a>Einrichten der Suche nach AutoErmittlungsendpunkten
<a name="bk_PreReqs"> </a>

Um AutoErmittlungs-SCP-Objekte in AD DS zu finden, benötigen Sie Zugriff auf Folgendes:
  
- Einen Server mit einer Version von Exchange lokal ab Exchange 2007 SP1.
    
- Einen Clientcomputer, der der Domäne beigetreten ist, in der der Exchange-Server installiert ist.
    
- Ein Benutzerkonto mit einem Postfach auf dem Exchange-Server. 
    
Außerdem sollten Sie sich vor Beginn mit einigen grundlegenden Konzepten vertraut machen. Nachfolgend werden einige hilfreiche Ressourcen aufgeführt.
  
**Tabelle 1. Verwandte Artikel zum Suchen nach AutoErmittlungsendpunkten von SCP-Objekten**

|**Artikel**|**Thema**|
|:-----|:-----|
|[AutoErmittlung für Exchange](autodiscover-for-exchange.md) <br/> |Funktionsweise des AutoErmittlungsdiensts  <br/> |
|[Veröffentlichen mit Dienstverbindungspunkten](http://msdn.microsoft.com/library/3544aa64-ecb0-48a1-ae49-05247a983842%28Office.15%29.aspx) <br/> |Verwendung von SCP-Objekten zum Veröffentlichen von dienstspezifischen Daten  <br/> |
   
## <a name="locate-autodiscover-scp-objects-in-ad-ds"></a>Suchen von AutoErmittlungs-SCP-Objekten in AD DS
<a name="bk_LocateScpObjects"> </a>

Der erste Schritte bei der Suche nach in AD DS veröffentlichten AutoErmittlungsendpunkten besteht darin, die AutoErmittlungs-SCP-Objekte zu suchen. Exchange veröffentlicht zwei Arten von SCP-Objekten für AutoErmittlung:
  
- **SCP-Zeiger** - Diese enthalten Informationen, die auf bestimmte LDAP-Server verweisen, die zum Suchen nach AutoErmittlungs-SCP-Objekten für die Domäne des Benutzers verwendet werden sollten. SCP-Zeiger haben die folgende GUID als Stempel: 67661d7F-8FC4-4fa7-BFAC-E1D7794C1F68. 
    
- **SCP-URLs** - Diese enthalten URLs für AutoErmittlungsendpunkte. SCP-URLs haben die folgende GUID als Stempel: 77378F46-2C66-4aa9-A6A6-3E7A48B19596. 
    
### <a name="to-locate-autodiscover-scp-objects"></a>So suchen Sie nach AutoErmittlungs-SCP-Objekten

1. In der **configurationNamingContext** -Eigenschaft des DSE-Stammeintrags in AD DS finden Sie den Pfad zum Konfigurationsbenennungskontext für die Domäne. Zum Lesen dieser Eigenschaft können Sie die [DirectoryEntry](http://msdn2.microsoft.com/EN-US/library/z9cddzaa)-Klasse oder jede andere API verwenden, die auf AD DS zugreifen kann. 
    
2. Suchen Sie im Konfigurationsbenennungskontext nach SCP-Objekten, deren **keywords** -Eigenschaft entweder die GUID des SCP-Zeigers oder die GUID der SCP-URL enthält. 
    
3. Überprüfen Sie die SCP-Objekten Sie gefunden für ein SCP-Zeiger, der auf die Domäne des Benutzers ausgelegt ist, Überprüfen der **Keywords** -Eigenschaft für einen Eintrag gleich `"Domain=<domain>"`. Angenommen, wenn die e-Mail-Adresse des Benutzers elvin@contoso.com ist, Sie sieht für einen Zeiger SCP mit einem Eintrag in der **Keywords** -Eigenschaft, die gleich ist `"Domain=contoso.com"`. Wenn ein passendes SCP-Zeiger gefunden wird, verwerfen Sie den Satz von SCP-Objekten, und beginnen Sie mit Schritt 1 mit dem Wert der Eigenschaft **ServiceBindingInformation** wie des Servers für den Eintrag Root-DSE herstellen über. 
    
4. Wenn Sie keine SCP-Zeiger finden, die der Domäne des Benutzers zugeordnet sind, überprüfen Sie, ob andere SCP-Zeiger vorhanden sind, die keiner Domäne zugeordnet sind, und speichern Sie den Wert der **serviceBindingInformation** -Eigenschaft als „Ausweichserver" für den Fall, das der aktuelle Server keine Ergebnisse zurückgibt. 
    
5. Wenn Sie keine der Domäne zugeordneten SCP-Zeiger gefunden haben, können Sie mit dem nächsten Schritt fortfahren: dem Generieren einer priorisierten Liste von AutoErmittlungsendpunkten aus den Abfrageergebnissen.
    
## <a name="generate-a-prioritized-list-of-autodiscover-endpoints"></a>Generieren einer priorisierten Liste mit AutoErmittlungsendpunkten
<a name="bk_GenerateList"> </a>

Sie können wie folgt eine priorisierte Liste der URLs von AutoErmittlungsendpunkten anhand der gefundenen SCP-Objekte generieren:
  
1. Ermitteln Sie den Namen des Active Directory-Standorts des Clientcomputers.
    
2. Überprüfen Sie die **keywords** -Eigenschaft für jede SCP-URL im Satz der gefundenen SCP-Objekte, und weisen Sie der URL gemäß den folgenden Regeln eine Priorität zu: 
    
  - **Keywords** -Eigenschaft enthält einen Wert von `"Site=<site name>"`, wobei `<site name>` entspricht, die der Namen des Active Directory-Standort Sie im vorherigen Schritt abgerufen weisen Sie der URL die Priorität 1. 
    
  - Wenn die **Keywords** -Eigenschaft nicht Eintrag mit einem Wert enthält, die mit beginnt `"Site="`, weisen Sie der URL eine Priorität von 2. 
    
  - **Keywords** -Eigenschaft enthält einen Wert von `"Site=<site name>`, wobei `<site name>` nicht gleich der Name der Active Directory-Standort, die Sie im vorherigen Schritt abgerufen wird, weisen Sie der URL eine Priorität von 3. 
    
## <a name="code-example-performing-an-scp-lookup"></a>Codebeispiel: Durchführen einer SCP-Suche
<a name="bk_CodeExample"> </a>

Im folgenden Codebeispiel wird veranschaulicht, wie Sie nach AutoErmittlungs-SCP-Objekten suchen und eine priorisierte Liste mit AutoErmittlungsendpunkten generieren.
  
```cs
using System;
using System.Collections.Generic;
using System.DirectoryServices;
using System.DirectoryServices.ActiveDirectory;
namespace ScpLookup
{
    // This sample is for demonstration purposes only. Before you run this sample, make sure 
    // that the code meets the coding requirements of your organization. 
    class Program
    {
        static void Main(string[] args)
        {
            string domain = args[0];
            Console.WriteLine("Performing SCP lookup for {0}.", domain);
            List<string> scpUrls = GetScpUrls(null, domain);
            Console.WriteLine("\nOrdered List of Autodiscover endpoints:");
            foreach (string url in scpUrls)
            {
                Console.WriteLine("  {0}", url);
            }
            Console.WriteLine("SCP lookup done.");
        }
        // GUID for SCP URL keyword.
        private const string ScpUrlGuidString = @"77378F46-2C66-4aa9-A6A6-3E7A48B19596";
        // GUID for SCP pointer keyword.
        private const string ScpPtrGuidString = @"67661d7F-8FC4-4fa7-BFAC-E1D7794C1F68";
        static List<string> GetScpUrls(string ldapServer, string domain)
        {
            // Create a new list to return.
            List<string> scpUrlList = new List<string>();
            string rootDSEPath = null;
            // If ldapServer is null/empty, use LDAP://RootDSE to
            // connect to Active Directory Domain Services (AD DS). Otherwise, use
            // LDAP://SERVERNAME/RootDSE to connect to a specific server.
            if (string.IsNullOrEmpty(ldapServer))
            {
                rootDSEPath = "LDAP://RootDSE";
            }
            else
            {
                rootDSEPath = ldapServer + "/RootDSE";
            }
            SearchResultCollection scpEntries = null;
            try
            {
                // Get the root directory entry.
                DirectoryEntry rootDSE = new DirectoryEntry(rootDSEPath);
                // Get the configuration path.
                string configPath = rootDSE.Properties["configurationNamingContext"].Value as string;
                // Get the configuration entry.
                DirectoryEntry configEntry = new DirectoryEntry("LDAP://" + configPath);
                // Create a search object for the configuration entry.
                DirectorySearcher configSearch = new DirectorySearcher(configEntry);
                // Set the search filter to find SCP URLs and SCP pointers.
                configSearch.Filter = "(&amp;(objectClass=serviceConnectionPoint)" +
                    "(|(keywords=" + ScpPtrGuidString + ")(keywords=" + ScpUrlGuidString + ")))";
                // Specify which properties you want to retrieve.
                configSearch.PropertiesToLoad.Add("keywords");
                configSearch.PropertiesToLoad.Add("serviceBindingInformation");
                scpEntries = configSearch.FindAll();
            }
            catch (Exception ex)
            {
                Console.WriteLine("SCP lookup failed with: ");
                Console.WriteLine(ex.ToString());
            }
            // If no SCP entries were found, then exit.
            if (scpEntries == null || scpEntries.Count <= 0)
            {
                Console.WriteLine("No SCP records found.");
                return null;
            }
            string fallBackLdapPath = null;
            // Check for SCP pointers.
            foreach (SearchResult scpEntry in scpEntries)
            {
                ResultPropertyValueCollection entryKeywords = scpEntry.Properties["keywords"];
                if (CollectionContainsExactValue(entryKeywords, ScpPtrGuidString))
                {
                    string ptrLdapPath = scpEntry.Properties["serviceBindingInformation"][0] as string;
                    // Determine whether this pointer is scoped to the user's domain.
                    if (CollectionContainsExactValue(entryKeywords, "Domain=" + domain))
                    {
                        Console.WriteLine("Found SCP pointer for " + domain + " in " + scpEntry.Path);
                        // Restart SCP lookup with the server assigned for the domain.
                        Console.WriteLine("Restarting SCP lookup in " + ptrLdapPath);
                        return GetScpUrls(ptrLdapPath, domain);
                    }
                    else
                    {
                        // Save the first SCP pointer that is not scoped to a domain as a fallback
                        // in case you do not get any results from this server.
                        if (entryKeywords.Count == 1 &amp;&amp; string.IsNullOrEmpty(fallBackLdapPath))
                        {
                            fallBackLdapPath = ptrLdapPath;
                            Console.WriteLine("Saved fallback SCP pointer: " + fallBackLdapPath);
                        }
                    }
                }
            }
            string computerSiteName = null;
            try
            {
                // Get the name of the ActiveDirectorySite the computer
                // belongs to (if it belongs to one).
                ActiveDirectorySite site = ActiveDirectorySite.GetComputerSite();
                computerSiteName = site.Name;
                Console.WriteLine("Local computer in site: " + computerSiteName);
            }
            catch (Exception ex)
            {
                Console.WriteLine("Unable to get computer site name.");
                Console.WriteLine(ex.ToString());
            }
            if (!string.IsNullOrEmpty(computerSiteName))
            {
                // Scan the search results for SCP URLs.
                // SCP URLs fit into three tiers:
                //   Priority 1: The URL is scoped to the computer's Active Directory site.
                //   Priority 2: The URL is not scoped to any Active Directory site.
                //   Priority 3: The URL is scoped to a different Active Directory site.
                // Temporary lists to hold priority 2 and 3 URLs.
                List<string> priorityTwoUrls = new List<string>();
                List<string> priorityThreeUrls = new List<string>();
                foreach (SearchResult scpEntry in scpEntries)
                {
                    ResultPropertyValueCollection entryKeywords = scpEntry.Properties["keywords"];
                    // Check for SCP URLs.
                    if (CollectionContainsExactValue(entryKeywords, ScpUrlGuidString))
                    {
                        string scpUrlPath = scpEntry.Properties["adsPath"][0] as string;
                        Console.WriteLine("SCP URL found at {0}", scpUrlPath);
                        string scpUrl = scpEntry.Properties["serviceBindingInformation"][0] as string;
                        scpUrl = scpUrl.ToLower();
                        // Determine whether this entry is scoped to the computer's site.
                        if (CollectionContainsExactValue(entryKeywords, "Site=" + computerSiteName))
                        {
                            // Priority 1.
                            if (!scpUrlList.Contains(scpUrl.ToLower()))
                            {
                                Console.WriteLine("Adding priority 1 SCP URL: {0}", scpUrl.ToLower());
                                scpUrlList.Add(scpUrl);
                            }
                            else
                            {
                                Console.WriteLine("Priority 1 SCP URL already found: {0}", scpUrl);
                            }
                        }
                        else
                        {
                            // Determine whether this is a priority 2 or 3 URL.
                            if (CollectionContainsPrefixValue(entryKeywords, "Site="))
                            {
                                // Priority 3.
                                if (!priorityThreeUrls.Contains(scpUrl))
                                {
                                    Console.WriteLine("Adding priority 3 SCP URL: {0}", scpUrl);
                                    priorityThreeUrls.Add(scpUrl);
                                }
                                else
                                {
                                    Console.WriteLine("Priority 3 SCP URL already found: {0}", scpUrl);
                                }
                            }
                            else
                            {
                                // Priority 2.
                                if (!priorityTwoUrls.Contains(scpUrl))
                                {
                                    Console.WriteLine("Adding priority 2 SCP URL: {0}", scpUrl);
                                    priorityTwoUrls.Add(scpUrl);
                                }
                                else
                                {
                                    Console.WriteLine("Priority 2 SCP URL already found: {0}", scpUrl);
                                }
                            }
                        }
                    }
                }
                // Now add the priority 2 URLs into the main list.
                foreach (string priorityTwoUrl in priorityTwoUrls)
                {
                    // If the URL is already in the list as a priority 1, 
                    // don't add it again.
                    if (!scpUrlList.Contains(priorityTwoUrl))
                    {
                        scpUrlList.Add(priorityTwoUrl);
                    }
                }
                // Now add the priority 3 URLs into the main list.
                foreach (string priorityThreeUrl in priorityThreeUrls)
                {
                    // If the URL is already in the list as a priority 1
                    // or priority 2, don't add it again.
                    if (!scpUrlList.Contains(priorityThreeUrl))
                    {
                        scpUrlList.Add(priorityThreeUrl);
                    }
                }
                // If after all this, you still have no URLs in your list,
                // try the fallback SCP pointer, if you have one.
                if (scpUrlList.Count == 0 &amp;&amp; fallBackLdapPath != null)
                {
                    return GetScpUrls(fallBackLdapPath, domain);
                }
            }
            return scpUrlList;
        }
        private static bool CollectionContainsExactValue(ResultPropertyValueCollection collection, string value)
        {
            foreach (object obj in collection)
            {
                string entry = obj as string;
                if (entry != null)
                {
                    if (string.Compare(value, entry, true) == 0)
                        return true;
                }
            }
            return false;
        }
        private static bool CollectionContainsPrefixValue(ResultPropertyValueCollection collection, string value)
        {
            foreach (object obj in collection)
            {
                string entry = obj as string;
                if (entry != null)
                {
                    if (entry.StartsWith(value))
                        return true;
                }
            }
            return false;
        }
    }
}
```

## <a name="next-steps"></a>Nächste Schritte
<a name="bk_NextSteps"> </a>

Im nächsten Schritt des AutoErmittlungsprozesses werden AutoErmittlungsanforderungen an die gefundenen URLs gesendet, beginnend mit URLs der Priorität 1, gefolgt von URLs der Priorität 2 und schließlich URLs der Priorität 3. Weitere Informationen über das Senden von AutoErmittlungsanforderungen und die Verarbeitung von Antworten finden Sie in den folgenden Artikeln:
  
- [Abrufen von benutzereinstellungen aus Exchange mithilfe der AutoErmittlung](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)
    
- [Behandeln von AutoErmittlungs-Fehlermeldungen](handling-autodiscover-error-messages.md)
    
## <a name="see-also"></a>Siehe auch

- [AutoErmittlung für Exchange](autodiscover-for-exchange.md)   
- [Einrichten Ihrer EWS-Anwendung](setting-up-your-ews-application.md)
    

