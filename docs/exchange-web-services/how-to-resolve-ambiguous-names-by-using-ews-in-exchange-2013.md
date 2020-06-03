---
title: Auflösen von mehrdeutigen Namen mithilfe der EWS Exchange 2013
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1ba21c54-ecd2-4a1e-80d4-0f4171dea84f
description: In diesem Artikel erfahren Sie, wie Sie mit dem verwaltete EWS-API oder EWS eindeutige Namen auflösen können, indem Sie mögliche Übereinstimmungen aus Active Directory-Domänendienste (AD DS) oder aus einem Kontaktordner im Postfach des Benutzers erhalten.
ms.openlocfilehash: 5e30e268f54e6ca257e188592e49d168e64332ff
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527747"
---
# <a name="resolve-ambiguous-names-by-using-ews-in-exchange-2013"></a>Auflösen von mehrdeutigen Namen mithilfe der EWS Exchange 2013

In diesem Artikel erfahren Sie, wie Sie mit dem verwaltete EWS-API oder EWS eindeutige Namen auflösen können, indem Sie mögliche Übereinstimmungen aus Active Directory-Domänendienste (AD DS) oder aus einem Kontaktordner im Postfach des Benutzers erhalten.
  
Ein Benutzer in Ihrer Organisation erhält eine handschriftliche Liste mit Namen und Adressen für Mitarbeiter, die an einer Schulungssitzung teilgenommen haben. Sie möchten eine e-Mail mit einigen zusätzlichen Informationen an Personen in der Liste senden, aber Sie können nicht alle e-Mail-Adressen lesen. Wenn Sie dieses Problem für Ihre Benutzer in Ihrer Anwendung lösen möchten, kann EWS helfen. Sie können die [Datei "ExchangeService. ResolveName](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) verwaltete EWS-API-Methode oder den [ResolveNames](https://msdn.microsoft.com/library/c85207e1-1315-443b-94ec-2b58f405076b%28Office.15%29.aspx) -EWS-Vorgang verwenden, um eine Liste möglicher Übereinstimmungen für eine Textauswahl zurückzugeben, beispielsweise einen Teil eines Nachnamens. Bei den zurückgegebenen Elementen kann es sich um öffentliche Benutzerpostfächer, Verteilergruppen und Kontakte handeln. 
  
Beachten Sie, dass Exchange e-Mail-Adressen mit vorfixierten Routing Typen wie SMTP oder SIP in einem mehrwertigen Array speichert. Die **ResolveName** -Methode und der **ResolveNames** -Vorgang führen eine partielle Übereinstimmung mit jedem Wert dieses Arrays aus, wenn Sie den Routingtyp am Anfang des nicht aufgelösten namens wie "SIP: user1" hinzufügen. Wenn Sie keinen Routingtyp angeben, wird die Methode oder der Vorgang standardmäßig auf SMTP festgelegt, mit einer primären SMTP-Adress Eigenschaft abgeglichen und nicht mit dem mehrwertigen Array durchsucht. Wenn Sie beispielsweise nach user1 suchen und das SIP-Präfix nicht einschließen, erhalten Sie SIP:user1@contoso.com nicht als Ergebnis, selbst wenn es sich um ein gültiges Postfach handelt. 
  
Sie können nur einen eindeutigen Namen in einer einzelnen Anforderung angeben. Wenn Sie eine Liste mit uneindeutigen Namen auflösen müssen, müssen Sie die Liste durchlaufen und die Methode oder den Vorgang für jeden Eintrag aufrufen. Kandidaten aus dem Ordner Kontakte eines Benutzers verfügen über einen Element-ID-Wert ungleich NULL, der dann in einem [Contact. Bind](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.contact.bind%28v=exchg.80%29.aspx) -Methodenaufruf oder einer [GetItem](https://msdn.microsoft.com/library/769df8eb-9c72-48b5-a49f-82c6b86bc5fc%28Office.15%29.aspx) -Vorgangsanforderung zum Abrufen zusätzlicher Informationen verwendet werden kann. Wenn es sich bei dem Kandidaten um eine Verteilergruppe handelt, können Sie die verwaltete EWS-API-Methode von [expandgroup (Itemid)](https://msdn.microsoft.com/library/office/ee356407%28v=exchg.80%29.aspx) oder den EWS-Vorgang [ExpandDL](https://msdn.microsoft.com/library/affe84a5-ad98-4aba-83f4-8732938b763d%28Office.15%29.aspx) verwenden, um die Liste der Elemente abzurufen. Wenn der Parameter _returnContactDetails_ oder das **ReturnFullContactData** -EWS-Attribut auf true festgelegt ist, enthalten Active Directory Einträge, die über eine **ResolveName** -Methode oder einen **ResolveNames** -Vorgang zurückgegeben werden, zusätzliche Eigenschaften, die den Kontakt beschreiben. Der _returnContactDetails_ -Parameter oder das **ReturnFullContactData** -Attribut wirkt sich nicht auf die Daten aus, die für Kontakte und Kontaktgruppen zurückgegeben werden. 
  
## <a name="resolve-ambiguous-names-by-using-ews-managed-api"></a>Auflösen von nicht eindeutigen Namen mithilfe von verwaltete EWS-API
<a name="bk_EWSMA"> </a>

Sie können die [ResolveName](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) -Methode verwenden, um Kandidaten zu finden, die mit dem nicht eindeutigen Namen übereinstimmen, den Sie übergeben. Sie können Überladungen der **ResolveName** -Methode verwenden, um auf fünf verschiedene Arten nach Kandidaten zu suchen. 
  
**Tabelle 1. Überladene ResolveName-Methoden**

|**Methode**|**Funktionsweise**|
|:-----|:-----|
|[ResolveName (Zeichenfolge)](https://msdn.microsoft.com/library/dd635548%28v=exchg.80%29.aspx) <br/> |Findet Kontakte im Kontakteordner des Benutzers und in der globalen Adressliste (GAL) – in dieser Reihenfolge. Die Zeichenfolgenvariable ist der eindeutige Name, den Sie auflösen möchten.  <br/> |
|[ResolveName (String, ResolveNameSearchLocation, Boolean)](https://msdn.microsoft.com/library/dd634595%28v=exchg.80%29.aspx) <br/> |Sucht nach Kontakten im Standardordner "Kontakte" und/oder in der globalen Adressliste (GAL). Der Zeichenfolgenwert ist der nicht eindeutiger Name, der Such Speicherort gibt den Kontakteordner und/oder die GAL an, und der boolesche Wert gibt an, ob die vollständigen Kontaktinformationen zurückgegeben werden sollen.  <br/> |
|[ResolveName (String, ResolveNameSearchLocation, Boolean, PropertySet)](https://msdn.microsoft.com/library/hh532803%28v=exchg.80%29.aspx) <br/> |Sucht nach Kontakten im standardmäßigen Kontakteordner und/oder der globalen Adressliste (GAL). Mit dieser Methode können Sie die zurückgegebenen Eigenschaften festlegen.  <br/> |
|[ResolveName (String, IEnumerable \<FolderId\> , ResolveNameSearchLocation, Boolean)](https://msdn.microsoft.com/library/dd636014%28v=exchg.80%29.aspx) <br/> |Sucht nach Kontakten in angegebenen Kontaktordnern und/oder der globalen Adressliste (GAL). Sie können diese Methode verwenden, um eine Sammlung von Ordnern an die Suche zu übergeben. Auf diese Weise können Sie in anderen Kontaktordnern als dem Standardordner Kontakte suchen.  <br/> |
|[ResolveName (String, IEnumerable \<FolderId\> , ResolveNameSearchLocation, Boolean, PropertySet)](https://msdn.microsoft.com/library/hh532581%28v=exchg.80%29.aspx) <br/> |Sucht Kontakte in der globalen Adressliste (GAL) und/oder in bestimmten Kontaktordnern. Mit dieser Methode können Sie die zurückgegebenen Eigenschaften festlegen.  <br/> |
   
Lassen Sie uns mit einem einfachen Beispiel beginnen. Das folgende Beispiel zeigt, wie Sie die Textzeichenfolge "Dan" auflösen und den Namen und die e-Mail-Adresse jedes gefundenen Kandidaten ausgeben. In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und dass der Benutzer mit einem Exchange-Server authentifiziert wurde. 
  
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

Die Antwort gibt maximal 100 Kandidaten zurück, allerdings gibt es möglicherweise mehr als 100 potenzielle Kandidaten. Überprüfen Sie den Wert von [IncludesAllResolutions](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.nameresolutioncollection.includesallresolutions%28v=exchg.80%29.aspx) im [NameResolutionCollection](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.nameresolutioncollection%28v=exchg.80%29.aspx) -Objekt, um festzustellen, ob nur die ersten 100 Kandidaten einer größeren Anzahl von Kandidaten zurückgegeben wurden. Wenn der Wert true ist, gibt es keine weiteren möglichen Kandidaten; Wenn der Wert auf false festgelegt ist, hat die Methode nur den ersten 100 einer größeren Anzahl potenzieller Kandidaten zurückgegeben. 
  
Wenn Sie in einer großen Organisation arbeiten, ist es wahrscheinlich, dass ein Name wie "Dan" die maximale Anzahl von 100 Kandidaten zurückgibt. Wenn Sie die Anzahl der zurückgegebenen Kandidaten reduzieren möchten, beschränken Sie die Suchfunktion. Im nächsten Beispiel wird die [ResolveNameSearchLocation](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.resolvenamesearchlocation%28v=exchg.80%29.aspx) -Aufzählung verwendet, um anzugeben, wo gesucht werden soll, um den nicht eindeutigen Namen aufzulösen. 
  
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

Wenn Sie Ihre Kontakte in einem anderen Ordner als dem bekannten Ordner Kontakte speichern, verwenden Sie eine der überladenen Methoden, um anzugeben, wo nach Kandidaten gesucht werden soll. Im folgenden Beispiel wird eine Ordnerliste für die **ResolveName** -Methode basierend auf der Ordner-ID erstellt. Die **Ordner** -Nr wurde zur Lesbarkeit gekürzt. 
  
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

Wenn Sie Filter anwenden und keine Kandidaten zurückgegeben werden, enthält die [NameResolutionCollection](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.nameresolutioncollection%28v=exchg.80%29.aspx) NULL Einträge. Sie können dies überprüfen, indem Sie die [count](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.nameresolutioncollection.count%28v=exchg.80%29.aspx) -Eigenschaft der Auflistung betrachten. 
  
## <a name="resolve-ambiguous-names-by-using-ews"></a>Auflösen von nicht eindeutigen Namen mithilfe von EWS
<a name="bk_EWSMA"> </a>

Sie können den [ResolveNames](https://msdn.microsoft.com/library/c85207e1-1315-443b-94ec-2b58f405076b%28Office.15%29.aspx) -EWS-Vorgang verwenden, um mögliche Kandidaten für einen nicht eindeutigen Namen zu identifizieren. Das [UnresolvedEntry](https://msdn.microsoft.com/library/5ac6116a-3b24-40f8-a877-dbe9a6935919%28Office.15%29.aspx) -Element enthält den eindeutigen Namen, den Sie auflösen möchten. Im folgenden Beispiel wird gezeigt, wie der Name Sadie aufgelöst wird. Dies ist auch die XML-Anforderung, die der verwaltete EWS-API verwendet, wenn Sie [die ResolveName-Methode verwenden](#bk_EWSMA), mit dem Unterschied, dass für gültige Ausgabe Beispiele ein anderer Name verwendet wird.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <ResolveNames xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                  ReturnFullContactData="true">
      <UnresolvedEntry>Sadie</UnresolvedEntry>
    </ResolveNames>
  </soap:Body>
</soap:Envelope>
```

Die Antwort gibt maximal 100 Kandidaten zurück, obwohl es möglicherweise mehr als 100 potenzielle Kandidaten gibt, um festzustellen, ob nur die ersten 100 Kandidaten einer größeren Anzahl von Kandidaten zurückgegeben wurden, überprüfen Sie den Wert des [IncludesLastItemInRange](https://msdn.microsoft.com/library/e7d6c7d3-548e-48b0-a313-bfef81e4832a%28Office.15%29.aspx) -Attributs des [resolutionset](https://msdn.microsoft.com/library/43d5b876-0e87-4414-9b1d-bff1c1ec825c%28Office.15%29.aspx) -Elements. Wenn der Wert true ist, gibt es keine weiteren möglichen Kandidaten; Wenn der Wert auf false festgelegt ist, hat der Vorgang nur den ersten 100 einer größeren Anzahl potenzieller Kandidaten zurückgegeben. 
  
Das folgende Beispiel zeigt die XML-Antwort, wenn ein Kandidat gefunden wird. Denken Sie daran, dass das [resolutionset](https://msdn.microsoft.com/library/43d5b876-0e87-4414-9b1d-bff1c1ec825c%28Office.15%29.aspx) bis zu 100 Kandidaten enthalten kann, wobei jedes durch das [Auflösungs](https://msdn.microsoft.com/library/573bed4b-d7b1-4baf-b16f-0795cdebf1a7%28Office.15%29.aspx) Element und dessen untergeordnete Elemente dargestellt wird. 
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <ResolveNamesResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

Sie werden nicht immer mit Kandidaten für Ihren eindeutigen Namen kommen. Im folgenden Beispiel wird die XML-Antwort als Fehler angezeigt, wenn keine Kandidaten gefunden werden.
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <ResolveNamesResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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


- [Personen und Kontakte in EWS in Exchange](people-and-contacts-in-ews-in-exchange.md)
    
- [Erweitern von Verteilergruppen mithilfe von EWS in Exchange 2013](how-to-expand-distribution-groups-by-using-ews-in-exchange-2013.md)
    

