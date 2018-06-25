---
title: Lösen Sie mehrdeutige Namen auf, mithilfe von EWS in Exchange 2013
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1ba21c54-ecd2-4a1e-80d4-0f4171dea84f
description: Erfahren Sie, wie die EWS Managed API oder EWS verwenden, um mehrdeutige Namen aufzulösen, indem Sie die erste möglicher Übereinstimmungen aus Active Directory-Domänendienste (AD DS) oder eines Kontaktordners im Postfach des Benutzers.
ms.openlocfilehash: 05a88043083a27d2e6d445cd71e5f3919c5a775d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756989"
---
# <a name="resolve-ambiguous-names-by-using-ews-in-exchange-2013"></a>Lösen Sie mehrdeutige Namen auf, mithilfe von EWS in Exchange 2013

Erfahren Sie, wie die EWS Managed API oder EWS verwenden, um mehrdeutige Namen aufzulösen, indem Sie die erste möglicher Übereinstimmungen aus Active Directory-Domänendienste (AD DS) oder eines Kontaktordners im Postfach des Benutzers.
  
Ein Benutzer in Ihrer Organisation erhält eine handgeschriebenen Liste der Namen und Adressen für Mitarbeiter, die eine Schulung teilnahmen. Sie eine e-Mail mit einige zusätzliche Informationen an Personen in der Liste senden möchten, aber sie alle e-Mail-Adresse können nicht gelesen werden. Wenn Sie für Ihre Benutzer in Ihrer Anwendung dieses Problem zu beheben möchten, können EWS helfen. Sie können die [ExchangeService.ResolveName](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) EWS Managed API-Methode oder die [ResolveNames](http://msdn.microsoft.com/library/c85207e1-1315-443b-94ec-2b58f405076b%28Office.15%29.aspx) EWS-Vorgang verwenden, um eine Liste der möglichen Übereinstimmungen für eine Auswahl von Text, z. B. Teil eines Nachnamens zurückzugeben. Die zurückgegebenen Elemente möglicherweise öffentliche Benutzerpostfächer, Verteilergruppen und Kontakte. 
  
Beachten Sie, dass Exchange e-Mail-Adressen mit vorangestellter routing Typen, wie die SMTP- oder Sip, in einem mehrwertigen Array speichert. Die **ResolveName** -Methode und der **ResolveNames** Vorgang ausführen eine teilweise Übereinstimmung mit jeder Wert eines Arrays beim Hinzufügen der Routingtyp am Anfang der aufgelöste Name, beispielsweise "Sip: User1". Wenn Sie eine Routingtyp nicht angeben, wird die Methode oder der Vorgang standardmäßig auf smtp, ihm eine primäre SMTP-Adresseneigenschaft zuordnen und nicht durchsucht das mehrwertige Array. Beispielsweise wenn Sie nach ' User1 suchen ' und nicht das Präfix "Sip" einschließen, erhalten Sie keine sip:User1@Contoso.com vorkommen, selbst wenn, die ein gültiges Postfach wird. 
  
Sie können nur eine mehrdeutigen Name in einer einzelnen Anforderung angeben. Wenn Sie eine Liste von mehrdeutige Namen aufgelöst haben, müssen Sie die Liste durchlaufen, und rufen Sie die Methode oder der Vorgang für jeden Eintrag. Kandidaten aus eines Benutzers Kontakteordner müssen einen Wert ungleich Null-Element-ID, die dann in einem Aufruf der [Contact.Bind](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.contact.bind%28v=exchg.80%29.aspx) -Methode oder [GetItem](http://msdn.microsoft.com/library/769df8eb-9c72-48b5-a49f-82c6b86bc5fc%28Office.15%29.aspx) Operation Anforderung verwendet werden kann, um zusätzliche Informationen abzurufen. Wenn der Kandidaten eine Verteilergruppe ist, können Sie die [ExpandGroup(ItemId)](http://msdn.microsoft.com/en-us/library/office/ee356407%28v=exchg.80%29.aspx) EWS Managed API-Methode oder [der ExpandDL](http://msdn.microsoft.com/library/affe84a5-ad98-4aba-83f4-8732938b763d%28Office.15%29.aspx) EWS-Vorgangs zum Abrufen der Liste der Elemente verwenden. Wenn der Parameter _ReturnContactDetails_ oder das **ReturnFullContactData** EWS-Attribut auf "true" Active Directory-Einträge, die über eine **ResolveName** -Methode zurückgegeben, festgelegt ist oder **ResolveNames** Vorgang zusätzliche Eigenschaften enthält Beschreiben des Kontakts. Der Parameter _ReturnContactDetails_ oder das **ReturnFullContactData** -Attribut nicht Einfluss auf die Daten, die für Kontakte zurückgegeben wird und Kontaktgruppen. 
  
## <a name="resolve-ambiguous-names-by-using-ews-managed-api"></a>Lösen Sie mehrdeutige Namen auf, mithilfe von EWS Managed API
<a name="bk_EWSMA"> </a>

Die [ResolveName](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) -Methode können Sie die um Kandidaten zu finden, die den mehrdeutigen Name entsprechen, den Sie weitergeben. Überladungen der **ResolveName** -Methode können Sie die Kandidaten in fünf verschiedenen Arten gesucht. 
  
**In Tabelle 1. Überladene ResolveName-Methoden**

|**Methode**|**Funktionsweise**|
|:-----|:-----|
|[ResolveName(String)](http://msdn.microsoft.com/en-us/library/dd635548%28v=exchg.80%29.aspx) <br/> |Sucht Kontakte im Kontakteordner der Benutzer und der globalen Adressliste (GAL) – in dieser Reihenfolge. String-Variable ist die mehrdeutiger Name, den Sie zu beheben versuchen.  <br/> |
|[ResolveName (Zeichenfolge, ResolveNameSearchLocation, Boolesch)](http://msdn.microsoft.com/en-us/library/dd634595%28v=exchg.80%29.aspx) <br/> |Sucht nach Kontakten in den Standardordner Kontakte und/oder der globalen Adressliste (GAL). String-Wert ist der mehrdeutiger Name, der Speicherort der gibt den Ordner Kontakte und/oder der globalen Adressliste und der boolesche Wert gibt an, ob die vollständigen Kontaktinformationen zurückgegeben.  <br/> |
|[ResolveName (Zeichenfolge, ResolveNameSearchLocation, Boolean, PropertySet)](http://msdn.microsoft.com/en-us/library/hh532803%28v=exchg.80%29.aspx) <br/> |Sucht nach Kontakten in den Standardordner Kontakte und/oder der globalen Adressliste (GAL). Mit dieser Methode können Sie die Eigenschaften festlegen, die zurückgegeben werden.  <br/> |
|[ResolveName (String, IEnumerable\<FolderId\>, ResolveNameSearchLocation, Boolean)](http://msdn.microsoft.com/en-us/library/dd636014%28v=exchg.80%29.aspx) <br/> |Sucht nach Kontakten in angegebenen Kontaktordner und/oder der globalen Adressliste (GAL). Mit dieser Methode können Sie um eine Auflistung von Ordner für die Suche zu übergeben. So können Sie Kontaktordner als den Standardordner Kontakte durchsucht.  <br/> |
|[ResolveName (String, IEnumerable\<FolderId\>, ResolveNameSearchLocation, Boolean, PropertySet)](http://msdn.microsoft.com/en-us/library/hh532581%28v=exchg.80%29.aspx) <br/> |Sucht nach Kontakten in der globalen Adressliste (GAL) und/oder in bestimmten Ordnern Kontakt. Mit dieser Methode können Sie die Eigenschaften festlegen, die zurückgegeben werden.  <br/> |
   
Wir beginnen mit ein einfaches Beispiel. Im folgenden Beispiel wird veranschaulicht, wie die Zeichenfolge "Dan" auflösen und Ausgabe der Name und e-Mail-Adresse des einzelnen Candidate gefunden. In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und der Benutzer bei einem Exchange-Server authentifiziert wurde. 
  
```cs
// Resolve the ambiguous name "dan".
   NameResolutionCollection resolvedNames = service.ResolveName("dan");
   // Output the list of candidates.
   foreach (NameResolution nameRes in resolvedNames)
   {
      Console.WriteLine("Contact name: " + nameRes.Mailbox.Name);
      Console.WriteLine("Contact e-mail address: " + nameRes.Mailbox.Address);
      Console.WriteLine("Mailbox type: " + nameRes.Mailbox.MailboxType);
   }

```

Die Antwort gibt maximal 100 Kandidaten, obwohl möglicherweise mehr als 100 potenzielle Kandidaten zurück. Um zu bestimmen, ob nur die ersten 100 Kandidaten für eine größere Anzahl von Kandidaten zurückgegeben wurden, überprüfen Sie den Wert des [IncludesAllResolutions](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.nameresolutioncollection.includesallresolutions%28v=exchg.80%29.aspx) im [NameResolutionCollection](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.nameresolutioncollection%28v=exchg.80%29.aspx) -Objekt. Wenn der Wert true ist, sind keine weiteren mögliche Kandidaten; Wenn der Wert false ist, zurückgegeben, die-Methode nur die ersten 100 für eine größere Anzahl von potenziellen Kandidaten. 
  
Wenn Sie in einer großen Organisation arbeiten, ist es wahrscheinlich, dass ein Namen wie "Dan" die maximale Anzahl von 100 Kandidaten zurückgegeben wird. Um die Anzahl der zurückgegebenen Kandidaten zu reduzieren, einschränken Sie, in dem Sie suchen. Das nächste Beispiel verwendet die [ResolveNameSearchLocation](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.resolvenamesearchlocation%28v=exchg.80%29.aspx) -Aufzählung, um anzugeben, wo Sie suchen, um den mehrdeutige Namen aufzulösen. 
  
```cs
// Resolve the ambiguous name "dan".
// Only use the Contacts folder.
   NameResolutionCollection resolvedNames = service.ResolveName("dan", ResolveNameSearchLocation.ContactsOnly, false);
   // Output the list of candidates.   
   foreach (NameResolution nameRes in resolvedNames)
   {
      Console.WriteLine("Contact name: " + nameRes.Mailbox.Name);
      Console.WriteLine("Contact e-mail address: " + nameRes.Mailbox.Address);
      Console.WriteLine("Mailbox type: " + nameRes.Mailbox.MailboxType);
   }

```

Wenn Sie Ihre Kontakte in einem anderen Ordner als den bekannten Kontakteordner speichern, verwenden Sie eine der überladenen Methoden um wo Kandidaten gesucht werden soll. Das folgende Beispiel erstellt eine Ordnerliste für die **ResolveName** -Methode basierend auf den Ordner-ID. Die **FolderId** wurde zur besseren Lesbarkeit gekürzt. 
  
```cs
// Create a list to store folders to search.
List<FolderId> folders = new List<FolderId>();
// Add a folder to the list based on the FolderId.
folders.Add(new FolderId("AABR8mboAAA="));
// Resolve the ambiguous name "dan".
// Only use the folders specified.
NameResolutionCollection resolvedNames = service.ResolveName("dan", folders, ResolveNameSearchLocation.ContactsOnly, false);
   foreach (NameResolution nameRes in resolvedNames)
   {
      Console.WriteLine("Contact name: " + nameRes.Mailbox.Name);
      Console.WriteLine("Contact e-mail address: " + nameRes.Mailbox.Address);
      Console.WriteLine("Mailbox type: " + nameRes.Mailbox.MailboxType);
   }

```

Wenn Sie Filter anwenden und keine Kandidaten zurückgegeben werden, wird die [NameResolutionCollection](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.nameresolutioncollection%28v=exchg.80%29.aspx) NULL Einträge enthalten. Sie können dies überprüfen, indem Sie die [Count](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.nameresolutioncollection.count%28v=exchg.80%29.aspx) -Eigenschaft der Auflistung ansehen. 
  
## <a name="resolve-ambiguous-names-by-using-ews"></a>Lösen Sie mehrdeutige Namen auf, mithilfe der Exchange-Webdienste
<a name="bk_EWSMA"> </a>

[ResolveNames](http://msdn.microsoft.com/library/c85207e1-1315-443b-94ec-2b58f405076b%28Office.15%29.aspx) EWS-Vorgangs können Sie um mögliche Kandidaten für ein mehrdeutiger Name zu identifizieren. Das [UnresolvedEntry](http://msdn.microsoft.com/library/5ac6116a-3b24-40f8-a877-dbe9a6935919%28Office.15%29.aspx) -Element enthält den mehrdeutigen Name, den Sie zu beheben möchten. Im folgenden Beispiel wird gezeigt, wie den Namen Sadie aufzulösen. Dies ist auch die XML-Anfrage, die die EWS Managed API verwendet, wenn Sie die [Verwendung der ResolveName-Methode](#bk_EWSMA), außer dass sie einen anderen Namen für Beispiele gültiger verwendet.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <ResolveNames xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
                  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
                  ReturnFullContactData="true">
      <UnresolvedEntry>Sadie</UnresolvedEntry>
    </ResolveNames>
  </soap:Body>
</soap:Envelope>
```

Die Antwort zurückgegeben maximal 100 Kandidaten, obwohl möglicherweise mehr als 100 potenzielle Kandidaten zu bestimmen, ob nur die ersten 100 Kandidaten für eine größere Anzahl von Kandidaten zurückgegeben wurden, überprüfen Sie den Wert der [IncludesLastItemInRange](http://msdn.microsoft.com/library/e7d6c7d3-548e-48b0-a313-bfef81e4832a%28Office.15%29.aspx) -Attribut des [ResolutionSet](http://msdn.microsoft.com/library/43d5b876-0e87-4414-9b1d-bff1c1ec825c%28Office.15%29.aspx) -Elements. Wenn der Wert true ist, sind keine weiteren mögliche Kandidaten; Wenn der Wert false ist, zurückgegeben, der Vorgang nur die ersten 100 für eine größere Anzahl von potenziellen Kandidaten. 
  
Das folgende Beispiel zeigt die XML-Antwort, wenn eine in Frage kommende gefunden wird. Beachten Sie, dass die [ResolutionSet](http://msdn.microsoft.com/library/43d5b876-0e87-4414-9b1d-bff1c1ec825c%28Office.15%29.aspx) bis zu 100 Kandidaten, jeweils, die durch die [Lösung](http://msdn.microsoft.com/library/573bed4b-d7b1-4baf-b16f-0795cdebf1a7%28Office.15%29.aspx) -Element und dessen untergeordnete Elemente enthalten kann. 
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <ResolveNamesResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:ResolveNamesResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:ResolutionSet TotalItemsInView="1" IncludesLastItemInRange="true">
            <t:Resolution>
              <t:Mailbox>
                <t:Name>Sadie Daniels</t:Name>
                <t:EmailAddress>Sadie@Contoso.com</t:EmailAddress>
                <t:RoutingType>SMTP</t:RoutingType>
                <t:MailboxType>Mailbox</t:MailboxType>
              </t:Mailbox>
              <t:Contact>
                <t:DisplayName>Sadie Daniels</t:DisplayName>
                <t:EmailAddresses>
                  <t:Entry Key="EmailAddress1">SMTP:Sadie@Contoso.com</t:Entry>
                </t:EmailAddresses>
                <t:ContactSource>ActiveDirectory</t:ContactSource>
              </t:Contact>
            </t:Resolution>
          </m:ResolutionSet>
        </m:ResolveNamesResponseMessage>
      </m:ResponseMessages>
    </ResolveNamesResponse>
  </soap:Body>
</soap:Envelope>
```

Sie nun nicht immer mit Kandidaten für Ihre mehrdeutiger Name. Das folgende Beispiel zeigt die XML-Antwort als Fehler, wenn keine Kandidaten gefunden werden.
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <ResolveNamesResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:ResolveNamesResponseMessage ResponseClass="Error">
          <m:MessageText>No results were found.</m:MessageText>
          <m:ResponseCode>ErrorNameResolutionNoResults</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:ResolveNamesResponseMessage>
      </m:ResponseMessages>
    </ResolveNamesResponse>
  </soap:Body>
</soap:Envelope>

```

## <a name="see-also"></a>Siehe auch


- [Benutzer und Kontakte in EWS in Exchange](people-and-contacts-in-ews-in-exchange.md)
    
- [Erweitern von Verteilergruppen durch Verwenden von EWS in Exchange 2013](how-to-expand-distribution-groups-by-using-ews-in-exchange-2013.md)
    

