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
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756885"
---
# <a name="find-autodiscover-endpoints-by-using-scp-lookup-in-exchange"></a><span data-ttu-id="7fd68-103">Suchen Sie nach AutoErmittlung-Endpunkten mithilfe von SCP-Suche in Exchange</span><span class="sxs-lookup"><span data-stu-id="7fd68-103">Find Autodiscover endpoints by using SCP lookup in Exchange</span></span>

<span data-ttu-id="7fd68-104">Erfahren Sie, wie Sie AutoErmittlungs-SCP-Objekte in Active Directory-Domänendienste (AD DS) suchen und verwenden, um AutoErmittlungsendpunkt-URLs für die Verwendung mit dem Exchange-AutoErmittlungsdienst zu suchen.</span><span class="sxs-lookup"><span data-stu-id="7fd68-104">Find out how to locate Autodiscover SCP objects in Active Directory Domain Services (AD DS) and use them to find Autodiscover endpoint URLs to use with the Exchange Autodiscover service.</span></span>
  
<span data-ttu-id="7fd68-p101">AutoErmittlung vereinfacht das Abrufen von Informationen, die Sie zum Herstellen von Verbindungen mit Postfächern auf Exchange-Servern benötigen. Um AutoErmittlung verwenden zu können, benötigen Sie jedoch ein Verfahren zum Suchen nach AutoErmittlungsservern, die für den Benutzer geeignet sind, dessen Einstellungen Sie abrufen. SCP-Objekte (Service Connection Point, Dienstverbindungspunkt) in AD DS bieten der Domäne beigetretenen Clients eine einfache Möglichkeit zum Suchen nach AutoErmittlungsservern.</span><span class="sxs-lookup"><span data-stu-id="7fd68-p101">Autodiscover makes it easy to retrieve information that you need to connect to mailboxes on Exchange servers. However, in order to use Autodiscover, you need a way to find Autodiscover servers that are appropriate for the user you're retrieving settings for. Service connection point (SCP) objects in AD DS provide an easy way for domain-joined clients to look up Autodiscover servers.</span></span> 
  
## <a name="get-set-up-to-find-autodiscover-endpoints"></a><span data-ttu-id="7fd68-108">Einrichten der Suche nach AutoErmittlungsendpunkten</span><span class="sxs-lookup"><span data-stu-id="7fd68-108">Get set up to find Autodiscover endpoints</span></span>
<span data-ttu-id="7fd68-109"><a name="bk_PreReqs"> </a></span><span class="sxs-lookup"><span data-stu-id="7fd68-109"></span></span>

<span data-ttu-id="7fd68-110">Um AutoErmittlungs-SCP-Objekte in AD DS zu finden, benötigen Sie Zugriff auf Folgendes:</span><span class="sxs-lookup"><span data-stu-id="7fd68-110">To locate Autodiscover SCP objects in AD DS, you need to have access to the following:</span></span>
  
- <span data-ttu-id="7fd68-111">Einen Server mit einer Version von Exchange lokal ab Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="7fd68-111">A server that is running a version of Exchange on-premises starting with Exchange 2007 SP1.</span></span>
    
- <span data-ttu-id="7fd68-112">Einen Clientcomputer, der der Domäne beigetreten ist, in der der Exchange-Server installiert ist.</span><span class="sxs-lookup"><span data-stu-id="7fd68-112">A client computer that is joined to the domain that the Exchange server is installed in.</span></span>
    
- <span data-ttu-id="7fd68-113">Ein Benutzerkonto mit einem Postfach auf dem Exchange-Server.</span><span class="sxs-lookup"><span data-stu-id="7fd68-113">A user account that has a mailbox on the Exchange server.</span></span> 
    
<span data-ttu-id="7fd68-p102">Außerdem sollten Sie sich vor Beginn mit einigen grundlegenden Konzepten vertraut machen. Nachfolgend werden einige hilfreiche Ressourcen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="7fd68-p102">Also, before you begin, you'll want to be familiar some basic concepts. The following are some resources that you'll find helpful.</span></span>
  
<span data-ttu-id="7fd68-116">**Tabelle 1. Verwandte Artikel zum Suchen nach AutoErmittlungsendpunkten von SCP-Objekten**</span><span class="sxs-lookup"><span data-stu-id="7fd68-116">**Table 1. Related articles for finding Autodiscover endpoints from SCP objects**</span></span>

|<span data-ttu-id="7fd68-117">**Artikel**</span><span class="sxs-lookup"><span data-stu-id="7fd68-117">**Read this article**</span></span>|<span data-ttu-id="7fd68-118">**Thema**</span><span class="sxs-lookup"><span data-stu-id="7fd68-118">**To learn about…**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7fd68-119">AutoErmittlung für Exchange</span><span class="sxs-lookup"><span data-stu-id="7fd68-119">Autodiscover for Exchange</span></span>](autodiscover-for-exchange.md) <br/> |<span data-ttu-id="7fd68-120">Funktionsweise des AutoErmittlungsdiensts</span><span class="sxs-lookup"><span data-stu-id="7fd68-120">How the Autodiscover service works.</span></span>  <br/> |
|[<span data-ttu-id="7fd68-121">Veröffentlichen mit Dienstverbindungspunkten</span><span class="sxs-lookup"><span data-stu-id="7fd68-121">Publishing with Service Connection Points</span></span>](http://msdn.microsoft.com/library/3544aa64-ecb0-48a1-ae49-05247a983842%28Office.15%29.aspx) <br/> |<span data-ttu-id="7fd68-122">Verwendung von SCP-Objekten zum Veröffentlichen von dienstspezifischen Daten</span><span class="sxs-lookup"><span data-stu-id="7fd68-122">How SCP objects are used to publish service-specific data.</span></span>  <br/> |
   
## <a name="locate-autodiscover-scp-objects-in-ad-ds"></a><span data-ttu-id="7fd68-123">Suchen von AutoErmittlungs-SCP-Objekten in AD DS</span><span class="sxs-lookup"><span data-stu-id="7fd68-123">Locate Autodiscover SCP objects in AD DS</span></span>
<span data-ttu-id="7fd68-124"><a name="bk_LocateScpObjects"> </a></span><span class="sxs-lookup"><span data-stu-id="7fd68-124"></span></span>

<span data-ttu-id="7fd68-p103">Der erste Schritte bei der Suche nach in AD DS veröffentlichten AutoErmittlungsendpunkten besteht darin, die AutoErmittlungs-SCP-Objekte zu suchen. Exchange veröffentlicht zwei Arten von SCP-Objekten für AutoErmittlung:</span><span class="sxs-lookup"><span data-stu-id="7fd68-p103">The first step toward finding Autodiscover endpoints published in AD DS is to locate the Autodiscover SCP objects. Exchange publishes two types of SCP objects for Autodiscover:</span></span>
  
- <span data-ttu-id="7fd68-p104">**SCP-Zeiger** - Diese enthalten Informationen, die auf bestimmte LDAP-Server verweisen, die zum Suchen nach AutoErmittlungs-SCP-Objekten für die Domäne des Benutzers verwendet werden sollten. SCP-Zeiger haben die folgende GUID als Stempel: 67661d7F-8FC4-4fa7-BFAC-E1D7794C1F68.</span><span class="sxs-lookup"><span data-stu-id="7fd68-p104">**SCP pointers** — These contain information that points to specific LDAP servers that should be used to locate Autodiscover SCP objects for the user's domain. SCP pointers are stamped with the following GUID: 67661d7F-8FC4-4fa7-BFAC-E1D7794C1F68.</span></span> 
    
- <span data-ttu-id="7fd68-p105">**SCP-URLs** - Diese enthalten URLs für AutoErmittlungsendpunkte. SCP-URLs haben die folgende GUID als Stempel: 77378F46-2C66-4aa9-A6A6-3E7A48B19596.</span><span class="sxs-lookup"><span data-stu-id="7fd68-p105">**SCP URLs** — These contain URLs for Autodiscover endpoints. SCP URLs are stamped with the following GUID: 77378F46-2C66-4aa9-A6A6-3E7A48B19596.</span></span> 
    
### <a name="to-locate-autodiscover-scp-objects"></a><span data-ttu-id="7fd68-131">So suchen Sie nach AutoErmittlungs-SCP-Objekten</span><span class="sxs-lookup"><span data-stu-id="7fd68-131">To locate Autodiscover SCP objects</span></span>

1. <span data-ttu-id="7fd68-p106">In der **configurationNamingContext** -Eigenschaft des DSE-Stammeintrags in AD DS finden Sie den Pfad zum Konfigurationsbenennungskontext für die Domäne. Zum Lesen dieser Eigenschaft können Sie die [DirectoryEntry](http://msdn2.microsoft.com/EN-US/library/z9cddzaa)-Klasse oder jede andere API verwenden, die auf AD DS zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="7fd68-p106">Read the **configurationNamingContext** property of the root DSE entry in AD DS to get the path to the configuration naming context for the domain. You can do this by using the [DirectoryEntry](http://msdn2.microsoft.com/EN-US/library/z9cddzaa) class, or any other API that can acces AD DS.</span></span> 
    
2. <span data-ttu-id="7fd68-134">Suchen Sie im Konfigurationsbenennungskontext nach SCP-Objekten, deren **keywords** -Eigenschaft entweder die GUID des SCP-Zeigers oder die GUID der SCP-URL enthält.</span><span class="sxs-lookup"><span data-stu-id="7fd68-134">Search for SCP objects in the configuration naming context that have either the SCP pointer GUID or the SCP URL GUID in the **keywords** property.</span></span> 
    
3. <span data-ttu-id="7fd68-135">Überprüfen Sie die SCP-Objekten Sie gefunden für ein SCP-Zeiger, der auf die Domäne des Benutzers ausgelegt ist, Überprüfen der **Keywords** -Eigenschaft für einen Eintrag gleich `"Domain=<domain>"`.</span><span class="sxs-lookup"><span data-stu-id="7fd68-135">Check the SCP objects you found for an SCP pointer that is scoped to the user's domain by checking the **keywords** property for an entry equal to `"Domain=<domain>"`.</span></span> <span data-ttu-id="7fd68-136">Angenommen, wenn die e-Mail-Adresse des Benutzers elvin@contoso.com ist, Sie sieht für einen Zeiger SCP mit einem Eintrag in der **Keywords** -Eigenschaft, die gleich ist `"Domain=contoso.com"`.</span><span class="sxs-lookup"><span data-stu-id="7fd68-136">For example, if the user's email address is elvin@contoso.com, you would look for an SCP pointer with an entry in the **keywords** property that is equal to `"Domain=contoso.com"`.</span></span> <span data-ttu-id="7fd68-137">Wenn ein passendes SCP-Zeiger gefunden wird, verwerfen Sie den Satz von SCP-Objekten, und beginnen Sie mit Schritt 1 mit dem Wert der Eigenschaft **ServiceBindingInformation** wie des Servers für den Eintrag Root-DSE herstellen über.</span><span class="sxs-lookup"><span data-stu-id="7fd68-137">If a matching SCP pointer is found, discard the set of SCP objects and start over at step 1 using the value of the **serviceBindingInformation** property as the server to connect to for the Root DSE entry.</span></span> 
    
4. <span data-ttu-id="7fd68-138">Wenn Sie keine SCP-Zeiger finden, die der Domäne des Benutzers zugeordnet sind, überprüfen Sie, ob andere SCP-Zeiger vorhanden sind, die keiner Domäne zugeordnet sind, und speichern Sie den Wert der **serviceBindingInformation** -Eigenschaft als „Ausweichserver" für den Fall, das der aktuelle Server keine Ergebnisse zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="7fd68-138">If you don't find any SCP pointers scoped to the user's domain, check for any SCP pointers that aren't scoped to any domain, and save the value of the **serviceBindingInformation** property as a "fallback" server, in case the current server doesn't give you any results.</span></span> 
    
5. <span data-ttu-id="7fd68-139">Wenn Sie keine der Domäne zugeordneten SCP-Zeiger gefunden haben, können Sie mit dem nächsten Schritt fortfahren: dem Generieren einer priorisierten Liste von AutoErmittlungsendpunkten aus den Abfrageergebnissen.</span><span class="sxs-lookup"><span data-stu-id="7fd68-139">If you didn't find any SCP pointers scoped to the domain, you're ready to move on to the next step: generating a prioritized list of Autodiscover endpoints from your results.</span></span>
    
## <a name="generate-a-prioritized-list-of-autodiscover-endpoints"></a><span data-ttu-id="7fd68-140">Generieren einer priorisierten Liste mit AutoErmittlungsendpunkten</span><span class="sxs-lookup"><span data-stu-id="7fd68-140">Generate a prioritized list of Autodiscover endpoints</span></span>
<span data-ttu-id="7fd68-141"><a name="bk_GenerateList"> </a></span><span class="sxs-lookup"><span data-stu-id="7fd68-141"></span></span>

<span data-ttu-id="7fd68-142">Sie können wie folgt eine priorisierte Liste der URLs von AutoErmittlungsendpunkten anhand der gefundenen SCP-Objekte generieren:</span><span class="sxs-lookup"><span data-stu-id="7fd68-142">You can generate a prioritized list of Autodiscover endpoint URLs, using the set of SCP objects that you located, by doing the following:</span></span>
  
1. <span data-ttu-id="7fd68-143">Ermitteln Sie den Namen des Active Directory-Standorts des Clientcomputers.</span><span class="sxs-lookup"><span data-stu-id="7fd68-143">Get the Active Directory site name of the client computer.</span></span>
    
2. <span data-ttu-id="7fd68-144">Überprüfen Sie die **keywords** -Eigenschaft für jede SCP-URL im Satz der gefundenen SCP-Objekte, und weisen Sie der URL gemäß den folgenden Regeln eine Priorität zu:</span><span class="sxs-lookup"><span data-stu-id="7fd68-144">Check the **keywords** property on each SCP URL in the set of SCP objects you found, and assign a priority to the URL based on the following rules:</span></span> 
    
  - <span data-ttu-id="7fd68-145">**Keywords** -Eigenschaft enthält einen Wert von `"Site=<site name>"`, wobei `<site name>` entspricht, die der Namen des Active Directory-Standort Sie im vorherigen Schritt abgerufen weisen Sie der URL die Priorität 1.</span><span class="sxs-lookup"><span data-stu-id="7fd68-145">If the **keywords** property contains a value of `"Site=<site name>"`, where `<site name>` equals the name of the Active Directory site you retrieved in the previous step, assign the URL a priority of 1.</span></span> 
    
  - <span data-ttu-id="7fd68-146">Wenn die **Keywords** -Eigenschaft nicht Eintrag mit einem Wert enthält, die mit beginnt `"Site="`, weisen Sie der URL eine Priorität von 2.</span><span class="sxs-lookup"><span data-stu-id="7fd68-146">If the **keywords** property does not contain an entry with a value that starts with `"Site="`, assign the URL a priority of 2.</span></span> 
    
  - <span data-ttu-id="7fd68-147">**Keywords** -Eigenschaft enthält einen Wert von `"Site=<site name>`, wobei `<site name>` nicht gleich der Name der Active Directory-Standort, die Sie im vorherigen Schritt abgerufen wird, weisen Sie der URL eine Priorität von 3.</span><span class="sxs-lookup"><span data-stu-id="7fd68-147">If the **keywords** property contains a value of `"Site=<site name>`, where `<site name>` does not equal the name of the Active Directory site you retrieved in the previous step, assign the URL a priority of 3.</span></span> 
    
## <a name="code-example-performing-an-scp-lookup"></a><span data-ttu-id="7fd68-148">Codebeispiel: Durchführen einer SCP-Suche</span><span class="sxs-lookup"><span data-stu-id="7fd68-148">Code example: Performing an SCP lookup</span></span>
<span data-ttu-id="7fd68-149"><a name="bk_CodeExample"> </a></span><span class="sxs-lookup"><span data-stu-id="7fd68-149"></span></span>

<span data-ttu-id="7fd68-150">Im folgenden Codebeispiel wird veranschaulicht, wie Sie nach AutoErmittlungs-SCP-Objekten suchen und eine priorisierte Liste mit AutoErmittlungsendpunkten generieren.</span><span class="sxs-lookup"><span data-stu-id="7fd68-150">In the following code example, you'll see how to locate Autodiscover SCP objects and generate a prioritized list of Autodiscover endpoints.</span></span>
  
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

## <a name="next-steps"></a><span data-ttu-id="7fd68-151">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="7fd68-151">Next steps</span></span>
<span data-ttu-id="7fd68-152"><a name="bk_NextSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="7fd68-152"></span></span>

<span data-ttu-id="7fd68-p108">Im nächsten Schritt des AutoErmittlungsprozesses werden AutoErmittlungsanforderungen an die gefundenen URLs gesendet, beginnend mit URLs der Priorität 1, gefolgt von URLs der Priorität 2 und schließlich URLs der Priorität 3. Weitere Informationen über das Senden von AutoErmittlungsanforderungen und die Verarbeitung von Antworten finden Sie in den folgenden Artikeln:</span><span class="sxs-lookup"><span data-stu-id="7fd68-p108">The next step in the Autodiscover process is to send Autodiscover requests to the URLs that you found, starting with priority 1 URLs, then priority 2 URLs, and finally priority 3 URLs. To learn more about how to send Autodiscover requests and handle responses, read the following articles:</span></span>
  
- [<span data-ttu-id="7fd68-155">Abrufen von benutzereinstellungen aus Exchange mithilfe der AutoErmittlung</span><span class="sxs-lookup"><span data-stu-id="7fd68-155">Get user settings from Exchange by using Autodiscover</span></span>](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)
    
- [<span data-ttu-id="7fd68-156">Behandeln von AutoErmittlungs-Fehlermeldungen</span><span class="sxs-lookup"><span data-stu-id="7fd68-156">Handling Autodiscover error messages</span></span>](handling-autodiscover-error-messages.md)
    
## <a name="see-also"></a><span data-ttu-id="7fd68-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7fd68-157">See also</span></span>

- [<span data-ttu-id="7fd68-158">AutoErmittlung für Exchange</span><span class="sxs-lookup"><span data-stu-id="7fd68-158">Autodiscover for Exchange</span></span>](autodiscover-for-exchange.md)   
- [<span data-ttu-id="7fd68-159">Einrichten Ihrer EWS-Anwendung</span><span class="sxs-lookup"><span data-stu-id="7fd68-159">Setting up your EWS application</span></span>](setting-up-your-ews-application.md)
    

