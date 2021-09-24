---
title: Auflösen von mehrdeutigen Namen mithilfe der EWS Exchange 2013
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 1ba21c54-ecd2-4a1e-80d4-0f4171dea84f
description: Erfahren Sie, wie Sie die verwaltete EWS-API oder EWS verwenden, um mehrdeutige Namen aufzulösen, indem Sie mögliche Übereinstimmungen aus Active Directory Domain Services (AD DS) oder einem Kontaktordner im Postfach Ihres Benutzers abrufen.
ms.openlocfilehash: 5946dad32639b454b3961eaa172b6069ce118b58
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521123"
---
# <a name="resolve-ambiguous-names-by-using-ews-in-exchange-2013"></a>Auflösen von mehrdeutigen Namen mithilfe der EWS Exchange 2013

Erfahren Sie, wie Sie die verwaltete EWS-API oder EWS verwenden, um mehrdeutige Namen aufzulösen, indem Sie mögliche Übereinstimmungen aus Active Directory Domain Services (AD DS) oder einem Kontaktordner im Postfach Ihres Benutzers abrufen.
  
Einem Benutzer in Ihrer Organisation wird eine handschriftliche Liste mit Namen und Adressen für Mitarbeiter, die an einer Schulungssitzung teilgenommen haben, übergeben. Sie möchten eine E-Mail mit einigen zusätzlichen Informationen an Personen in der Liste senden, aber sie können nicht die E-Mail-Adresse aller Benutzer lesen. Wenn Sie dieses Problem für Ihre Benutzer in Ihrer Anwendung lösen möchten, kann EWS hilfreich sein. Sie können die [ExchangeService.ResolveName](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) EWS Managed API-Methode oder den [ResolveNames](https://msdn.microsoft.com/library/c85207e1-1315-443b-94ec-2b58f405076b%28Office.15%29.aspx) EWS-Vorgang verwenden, um eine Liste potenzieller Übereinstimmungen für eine Textauswahl zurückzugeben, z. B. einen Teil eines Nachnamens. Die zurückgegebenen Elemente können öffentliche Benutzerpostfächer, Verteilergruppen und Kontakte sein. 
  
Beachten Sie, dass Exchange E-Mail-Adressen mit Routingtypen mit Präfix, z. B. SMTP oder SIP, in einem mehrwertigen Array speichert. Die **ResolveName-Methode** und der **ResolveNames-Vorgang** führen eine partielle Übereinstimmung mit jedem Wert dieses Arrays aus, wenn Sie den Routingtyp am Anfang des nicht aufgelösten Namens hinzufügen, z. B. "sip:User1". Wenn Sie keinen Routingtyp angeben, verwendet die Methode oder der Vorgang standardmäßig smtp, gleicht sie mit einer primären SMTP-Adresseigenschaft ab und durchsucht nicht das mehrwertige Array. Wenn Sie beispielsweise nach "User1" suchen und das SIP-Präfix nicht einschließen, erhalten Sie daher keine sip:User1@Contoso.com, auch wenn es sich um ein gültiges Postfach handelt. 
  
Sie können nur einen mehrdeutigen Namen in einer einzigen Anforderung angeben. Wenn Sie eine Liste von mehrdeutigen Namen haben, die aufgelöst werden müssen, müssen Sie die Liste durchlaufen und die Methode oder den Vorgang für jeden Eintrag aufrufen. Kandidaten aus dem Kontaktordner eines Benutzers weisen einen Wert der Element-ID ungleich Null auf, der dann in einem [Contact.Bind-Methodenaufruf](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.contact.bind%28v=exchg.80%29.aspx) oder einer [GetItem-Vorgangsanforderung](https://msdn.microsoft.com/library/769df8eb-9c72-48b5-a49f-82c6b86bc5fc%28Office.15%29.aspx) verwendet werden kann, um zusätzliche Informationen abzurufen. Wenn der Kandidat eine Verteilergruppe ist, können Sie die verwaltete EWS-API-Methode [ExpandGroup(ItemId)](https://msdn.microsoft.com/library/office/ee356407%28v=exchg.80%29.aspx) oder den [ExpandDL](https://msdn.microsoft.com/library/affe84a5-ad98-4aba-83f4-8732938b763d%28Office.15%29.aspx) EWS-Vorgang verwenden, um die Liste der Mitglieder abzurufen. Wenn der  _parameter returnContactDetails_ oder das **ReturnFullContactData** EWS-Attribut auf "true" festgelegt ist, enthalten Active Directory-Einträge, die über eine **ResolveName-Methode** oder **einen ResolveNames-Vorgang** zurückgegeben werden, zusätzliche Eigenschaften, die den Kontakt beschreiben. Der parameter  _returnContactDetails_ oder das **ReturnFullContactData-Attribut** wirkt sich nicht auf die Daten aus, die für Kontakte und Kontaktgruppen zurückgegeben werden. 
  
## <a name="resolve-ambiguous-names-by-using-ews-managed-api"></a>Auflösen von mehrdeutigen Namen mithilfe der verwalteten EWS-API
<a name="bk_EWSMA"> </a>

Sie können die [ResolveName-Methode](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) verwenden, um Kandidaten zu suchen, die dem von Ihnen übergebenen mehrdeutigen Namen entsprechen. Sie können Überladungen der **ResolveName-Methode** verwenden, um auf fünf verschiedene Arten nach Kandidaten zu suchen. 
  
**Tabelle 1. Überladene ResolveName-Methoden**

|**Methode**|**Funktionsweise**|
|:-----|:-----|
|[ResolveName(String)](https://msdn.microsoft.com/library/dd635548%28v=exchg.80%29.aspx) <br/> |Sucht Kontakte im Ordner "Kontakte" des Benutzers und in der globalen Adressliste (GAL) in dieser Reihenfolge. Die Zeichenfolgenvariable ist der mehrdeutige Name, den Sie auflösen möchten.  <br/> |
|[ResolveName(String, ResolveNameSearchLocation, Boolean)](https://msdn.microsoft.com/library/dd634595%28v=exchg.80%29.aspx) <br/> |Sucht Kontakte im Standardordner "Kontakte" und/oder in der globalen Adressliste (GAL). Der Zeichenfolgenwert ist der mehrdeutige Name, der Suchspeicherort gibt den Ordner "Kontakte" und/oder die GAL an, und der boolesche Wert gibt an, ob die vollständigen Kontaktinformationen zurückgegeben werden sollen.  <br/> |
|[ResolveName(String, ResolveNameSearchLocation, Boolean, PropertySet)](https://msdn.microsoft.com/library/hh532803%28v=exchg.80%29.aspx) <br/> |Sucht Kontakte im Standardordner "Kontakte" und/oder "Globale Adressliste" (GAL). Mit dieser Methode können Sie die zurückgegebenen Eigenschaften festlegen.  <br/> |
|[ResolveName(String, IEnumerable \<FolderId\> , ResolveNameSearchLocation, Boolean)](https://msdn.microsoft.com/library/dd636014%28v=exchg.80%29.aspx) <br/> |Sucht Kontakte in angegebenen Kontaktordnern und/oder der globalen Adressliste (GAL). Sie können diese Methode verwenden, um eine Sammlung von Zu durchsuchenden Ordnern zu übergeben. Auf diese Weise können Sie andere Kontaktordner als den Standardordner "Kontakte" suchen.  <br/> |
|[ResolveName(String, IEnumerable \<FolderId\> , ResolveNameSearchLocation, Boolean, PropertySet)](https://msdn.microsoft.com/library/hh532581%28v=exchg.80%29.aspx) <br/> |Sucht Kontakte in der globalen Adressliste (GAL) und/oder in bestimmten Kontaktordnern. Mit dieser Methode können Sie die zurückgegebenen Eigenschaften festlegen.  <br/> |
   
Beginnen wir mit einem einfachen Beispiel. Das folgende Beispiel zeigt, wie Sie die Textzeichenfolge "dan" auflösen und den Namen und die E-Mail-Adresse jedes gefundenen Kandidaten ausgeben. In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und der Benutzer bei einem Exchange-Server authentifiziert wurde. 
  
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

Die Antwort gibt maximal 100 Kandidaten zurück, obwohl es möglicherweise mehr als 100 potenzielle Kandidaten gibt. Um festzustellen, ob nur die ersten 100 Kandidaten einer größeren Anzahl von Kandidaten zurückgegeben wurden, überprüfen Sie den Wert von [IncludesAllResolutions](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.nameresolutioncollection.includesallresolutions%28v=exchg.80%29.aspx) im [NameResolutionCollection-Objekt.](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.nameresolutioncollection%28v=exchg.80%29.aspx) Wenn der Wert "true" ist, gibt es keine weiteren möglichen Kandidaten. wenn der Wert "false" ist, gibt die Methode nur die ersten 100 einer größeren Anzahl potenzieller Kandidaten zurück. 
  
Wenn Sie in einer großen Organisation arbeiten, gibt ein Name wie "dan" wahrscheinlich die maximale Anzahl von 100 Kandidaten zurück. Um die Anzahl der zurückgegebenen Kandidaten zu reduzieren, beschränken Sie den Suchbereich. Im nächsten Beispiel wird die [ResolveNameSearchLocation](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.resolvenamesearchlocation%28v=exchg.80%29.aspx) -Aufzählung verwendet, um anzugeben, wo der mehrdeutige Name aufgelöst werden soll. 
  
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

Wenn Sie Ihre Kontakte in einem anderen Ordner als dem bekannten Kontaktordner speichern, verwenden Sie eine der überladenen Methoden, um anzugeben, wo nach Kandidaten gesucht werden soll. Im folgenden Beispiel wird eine Ordnerliste für die **ResolveName** -Methode basierend auf der Ordner-ID erstellt. Die **FolderId** wurde zur besseren Lesbarkeit gekürzt. 
  
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

Wenn Sie Filter anwenden und keine Kandidaten zurückgegeben werden, enthält [nameResolutionCollection](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.nameresolutioncollection%28v=exchg.80%29.aspx) null Einträge. Sie können dies überprüfen, indem Sie sich die [Count-Eigenschaft](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.nameresolutioncollection.count%28v=exchg.80%29.aspx) der Auflistung ansehen. 
  
## <a name="resolve-ambiguous-names-by-using-ews"></a>Auflösen von mehrdeutigen Namen mithilfe von EWS
<a name="bk_EWSMA"> </a>

Sie können den [ResolveNames](https://msdn.microsoft.com/library/c85207e1-1315-443b-94ec-2b58f405076b%28Office.15%29.aspx) EWS-Vorgang verwenden, um mögliche Kandidaten für einen mehrdeutigen Namen zu identifizieren. Das [UnresolvedEntry-Element](https://msdn.microsoft.com/library/5ac6116a-3b24-40f8-a877-dbe9a6935919%28Office.15%29.aspx) enthält den mehrdeutigen Namen, den Sie auflösen möchten. Das folgende Beispiel zeigt, wie der Name Sadie aufgelöst wird. Dies ist auch die XML-Anforderung, die die verwaltete EWS-API verwendet, wenn Sie [die ResolveName-Methode verwenden,](#bk_EWSMA)mit der Ausnahme, dass sie einen anderen Namen für gültige Ausgabebeispiele verwendet.
  
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

Die Antwort gibt maximal 100 Kandidaten zurück, obwohl es möglicherweise mehr als 100 potenzielle Kandidaten gibt, um festzustellen, ob nur die ersten 100 Kandidaten einer größeren Anzahl von Kandidaten zurückgegeben wurden, überprüfen Sie den Wert des [IncludesLastItemInRange-Attributs](https://msdn.microsoft.com/library/e7d6c7d3-548e-48b0-a313-bfef81e4832a%28Office.15%29.aspx) des [ResolutionSet-Elements.](https://msdn.microsoft.com/library/43d5b876-0e87-4414-9b1d-bff1c1ec825c%28Office.15%29.aspx) Wenn der Wert "true" ist, gibt es keine weiteren möglichen Kandidaten. wenn der Wert "false" ist, gibt der Vorgang nur die ersten 100 einer größeren Anzahl potenzieller Kandidaten zurück. 
  
Das folgende Beispiel zeigt die XML-Antwort, wenn ein Kandidat gefunden wird. Beachten Sie, dass das [ResolutionSet](https://msdn.microsoft.com/library/43d5b876-0e87-4414-9b1d-bff1c1ec825c%28Office.15%29.aspx) bis zu 100 Kandidaten enthalten kann, die jeweils durch das [Resolution-Element](https://msdn.microsoft.com/library/573bed4b-d7b1-4baf-b16f-0795cdebf1a7%28Office.15%29.aspx) und seine untergeordneten Elemente dargestellt werden. 
  
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

Sie werden nicht immer Kandidaten für Ihren mehrdeutigen Namen finden. Das folgende Beispiel zeigt die XML-Antwort als Fehler, wenn keine Kandidaten gefunden werden.
  
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
    

