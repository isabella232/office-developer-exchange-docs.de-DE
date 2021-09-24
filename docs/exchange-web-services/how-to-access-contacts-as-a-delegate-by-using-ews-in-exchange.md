---
title: Zugriff auf Kontakte als Delegat mithilfe der EWS in Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 3cd34c14-18b0-4fe2-a4c2-d884318c88fc
description: Erfahren Sie, wie Sie mithilfe der verwalteten EWS-API oder EWS in Exchange auf Kontakte als Stellvertretung zugreifen.
ms.openlocfilehash: a1ebef7f447f0b04bb3f73a8c418f291399486e3
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59512191"
---
# <a name="access-contacts-as-a-delegate-by-using-ews-in-exchange"></a>Zugriff auf Kontakte als Delegat mithilfe der EWS in Exchange

Erfahren Sie, wie Sie mithilfe der verwalteten EWS-API oder EWS in Exchange auf Kontakte als Stellvertretung zugreifen.
  
Sie können die verwaltete EWS-API oder EWS verwenden, um einem Benutzer Zugriff auf den Kontaktordner eines Postfachbesitzers zu gewähren. Der Stellvertreter kann dann Kontakte im Namen des Postfachbesitzers erstellen und Kontakte aus dem Kontaktordner des Postfachbesitzers abrufen, aktualisieren und löschen, je nach berechtigungen.
  
Als Stellvertretung verwenden Sie die gleichen Methoden und Vorgänge, um auf den Kontaktordner eines Postfachbesitzers zuzugreifen, den Sie für den Zugriff auf Ihren eigenen Kontakteordner verwenden. Der Hauptunterschied besteht darin, dass Sie [expliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_explicit) verwenden müssen, um ein Kontaktelement zu suchen oder zu erstellen. Nachdem Sie die Element-ID identifiziert haben, können Sie impliziten [Zugriff](delegate-access-and-ews-in-exchange.md#bk_implicit) verwenden, um das Element abzurufen, zu aktualisieren oder zu löschen. 
  
**Tabelle 1. EWS Managed API-Methoden und EWS-Vorgänge für den Zugriff auf einen Kontakt als Delegat**

|**Aktion**|**Verwenden Sie diese verwaltete EWS-API-Methode...**|**Verwenden Sie diesen EWS-Vorgang...**|
|:-----|:-----|:-----|
|Erstellen eines Kontakts als Stellvertretung  <br/> |[Item.Save](https://msdn.microsoft.com/library/dd635209%28v=exchg.80%29.aspx) where the [FolderId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Contacts folder  <br/> |[CreateItem,](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) wobei das [Mailbox-Element](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) die [EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) des Postfachbesitzers angibt  <br/> |
|Erstellen mehrerer Kontakte als Stellvertretung  <br/> |[ExchangeService.CreateItems,](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) wobei der **Parameter FolderId** [expliziten Zugriff auf](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) den Kontaktordner des Postfachbesitzers bietet  <br/> |[CreateItem,](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) wobei das [Mailbox-Element](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) die [EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) des Postfachbesitzers angibt  <br/> |
|Auflösen eines Kontakts als Stellvertretung  <br/> |[ExchangeService.ResolveName,](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) wobei der [Parameter FolderId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) [expliziten Zugriff auf](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) den Kontakteordner des Postfachbesitzers bietet  <br/> |[ResolveNames,](https://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) wobei das [Mailbox-Element](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) die [EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) des Postfachbesitzers angibt  <br/> |
|Suchen nach oder Suchen eines Kontakts als Stellvertretung  <br/> |[ExchangeService.FindItems,](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) wobei der **Parameter FolderId** [expliziten Zugriff auf](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) den Kontaktordner des Postfachbesitzers bietet  <br/> |[FindItem,](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) wobei das [Mailbox-Element](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) die [EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) des Postfachbesitzers angibt  <br/> |
|Abrufen eines Kontakts als Stellvertretung  <br/> |[Contact.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contact.bind%28v=exchg.80%29.aspx) <br/> |[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |
|Aktualisieren eines Kontakts als Stellvertretung  <br/> |[Contact.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contact.bind%28v=exchg.80%29.aspx) gefolgt von [Contact.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.update%28v=exchg.80%29.aspx) <br/> |[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) gefolgt von [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |
|Löschen eines Kontakts als Stellvertretung  <br/> |[Contact.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contact.bind%28v=exchg.80%29.aspx) gefolgt von [Contact.Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.delete%28v=exchg.80%29.aspx) <br/> |[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) gefolgt von [DeleteItem](../web-service-reference/deleteitem-operation.md) <br/> |
   
> [!NOTE]
> In den Codebeispielen in diesem Artikel ist primary@contoso.com der Postfachbesitzer. 

<a name="bk_prereq"> </a>

## <a name="prerequisite-tasks"></a>Erforderliche Aufgaben

Bevor ein Benutzer als Stellvertretung auf den Kontaktordner des Postfachbesitzers zugreifen kann, muss er [als Stellvertreter mit Berechtigungen](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md) für den Kontaktordner des Postfachbesitzers hinzugefügt werden. 

<a name="bk_createewsma"> </a>

## <a name="create-a-contact-as-a-delegate-by-using-the-ews-managed-api"></a>Erstellen eines Kontakts als Delegat mithilfe der verwalteten EWS-API

Mit der verwalteten EWS-API können Sie das Dienstobjekt für den Stellvertreterbenutzer verwenden, um Kontakte für den Postfachbesitzer zu erstellen. In diesem Beispiel wird gezeigt, wie Sie die [Save-Methode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) verwenden, um eine Besprechung zu erstellen und Besprechungsanfragen an die Teilnehmer zu senden. 
  
In diesem Beispiel wird davon ausgegangen, dass es sich bei dem **Dienst** um ein gültiges [ExchangeService-Objekt](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) für den Delegaten handelt und der Stellvertretung die entsprechenden Berechtigungen für den Kontaktordner des Postfachbesitzers erteilt wurden. 
  
```cs
 public static void DelegateAccessCreateContact(ExchangeService service)
{
    // Create the contact.
    Contact contact = new Contact(service);
    // Specify the name and how the contact should be filed.
    contact.GivenName = "Brian";
    contact.MiddleName = "David";
    contact.Surname = "Johnson";
    contact.FileAsMapping = FileAsMapping.SurnameCommaGivenName;
    // Specify the company name.
    contact.CompanyName = "Contoso";
    // Specify the business, home, and car phone numbers.
    contact.PhoneNumbers[PhoneNumberKey.BusinessPhone] = "425-555-0110";
    contact.PhoneNumbers[PhoneNumberKey.HomePhone] = "425-555-0120";
    contact.PhoneNumbers[PhoneNumberKey.CarPhone] = "425-555-0130";
    // Specify two email addresses.
    contact.EmailAddresses[EmailAddressKey.EmailAddress1] = 
        new EmailAddress("brian_1@contoso.com");
    contact.EmailAddresses[EmailAddressKey.EmailAddress2] = 
        new EmailAddress("brian_2@contoso.com");
    // Save the contact in the mailbox owner's Contacts folder.
    // This method call results in a CreateItem call to EWS. 
    // The contact identifier contains the context for the mailbox owner's 
    // Contact folder. Any additional actions take on this contact will 
    // be performed in the mailbox owner's mailbox. 
    contact.Save(new FolderId(WellKnownFolderName.Contacts, 
        "primary@contoso.com"));
    // Verify that the contact was created.
    // This method call results in a GetItem call to EWS
    // to load the display name property on the contact. 
    contact.Load(new PropertySet (ContactSchema.DisplayName));
    Console.WriteLine("\nContact created: " + contact.DisplayName + "\n");
}
```

Beachten Sie, dass beim Speichern des Elements der Aufruf der [Save-Methode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) den Kontaktordner des Postfachbesitzers identifizieren muss. Wenn der Kontaktordner des Postfachbesitzers nicht angegeben ist, wird die Besprechungsanfrage im Kontaktordner des Stellvertreters und nicht im Kontaktordner des Postfachbesitzers gespeichert. Sie können den Kontaktordner des Postfachbesitzers auf zwei Arten in den **Save-Methodenaufruf** einschließen. Es wird empfohlen, eine neue Instanz des [FolderId-Objekts](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) mithilfe von [WellKnownFolderName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) und der SMTP-Adresse des Postfachbesitzers zu instanziieren. 
  
```cs
contact.Save(new FolderId(WellKnownFolderName.Contacts, "primary@contoso.com"));
```

Sie können jedoch auch zuerst eine [Bindung](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) an den Ordner "Kontakte" erstellen und dann die ID des Ordners im Aufruf der **Save-Methode** verwenden. Beachten Sie jedoch, dass dadurch ein zusätzlicher EWS-Aufruf erstellt wird. 
  
```cs
    // Identify the mailbox owner's SMTP address 
    // and bind to their Contacts folder.
    Mailbox primary = new Mailbox("primary@contoso.com"); 
    Folder primaryContacts = Folder.Bind(service, new FolderId(WellKnownFolderName.Contacts, primary)); 
…
    // Save the contact to the mailbox owner's Contacts folder.
    meeting.Save(primaryContacts.Id);
```

<a name="bk_createews"> </a>

## <a name="create-a-contact-as-a-delegate-by-using-ews"></a>Erstellen eines Kontakts als Delegat mithilfe von EWS

Mit EWS können Sie das Dienstobjekt für den Stellvertreterbenutzer verwenden, um Kontaktelemente für den Postfachbesitzer zu erstellen. In diesem Beispiel wird gezeigt, wie Der [CreateItem-Vorgang](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) zum Erstellen eines Kontakts verwendet wird. 
  
Dies ist auch die XML-Anforderung, die die verwaltete EWS-API sendet, wenn Sie die **Save** -Methode verwenden, um einen Kontakt zu [erstellen.](#bk_createewsma)
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:CreateItem MessageDisposition="SaveOnly">
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="contacts">
          <t:Mailbox>
            <t:EmailAddress>primary@contoso.com</t:EmailAddress>
          </t:Mailbox>
        </t:DistinguishedFolderId>
      </m:SavedItemFolderId>
      <m:Items>
        <t:Contact>
          <t:FileAsMapping>LastCommaFirst</t:FileAsMapping>
          <t:GivenName>Brian</t:GivenName>
          <t:MiddleName>David</t:MiddleName>
          <t:CompanyName>Contoso</t:CompanyName>
          <t:EmailAddresses>
            <t:Entry Key="EmailAddress1">brian_1@contoso.com</t:Entry>
            <t:Entry Key="EmailAddress2">brian_2@contoso.com</t:Entry>
          </t:EmailAddresses>
          <t:PhoneNumbers>
            <t:Entry Key="BusinessPhone">425-555-0110</t:Entry>
            <t:Entry Key="HomePhone">425-555-0120</t:Entry>
            <t:Entry Key="CarPhone">425-555-0130</t:Entry>
          </t:PhoneNumbers>
          <t:Surname>Johnson</t:Surname>
        </t:Contact>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

Der Server antwortet auf die **CreateItem-Anforderung** mit einer [CreateItemResponse-Nachricht,](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) die den [ResponseCode-Elementwert](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **NoError** enthält, der angibt, dass der Kontakt erfolgreich erstellt wurde. Die Antwort enthält auch die Element-ID des neu erstellten Kontakts.

<a name="bk_resolveewsma"> </a>

## <a name="resolve-a-contact-as-a-delegate-by-using-the-ews-managed-api"></a>Auflösen eines Kontakts als Delegat mithilfe der verwalteten EWS-API

Um einen Kontakt basierend auf einem möglicherweise nicht eindeutigen Namen oder Ausdruck zu finden, müssen Sie eine der [ExchangeService.ResolveName-Methoden](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) verwenden, die einen [FolderId-Parameter](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) enthalten, damit Sie den Kontaktordner des Postfachbesitzers angeben können. 
  
```cs
private static void DelegateAccessResolveContacts(ExchangeService service)
{
    // Create a list to store folders to search.
    List<FolderId> folders = new List<FolderId>();
   
    // Add the mailbox owner's folder to the list.
    folders.Add(new FolderId(WellKnownFolderName.Contacts, 
        "primary@contoso.com"));
    
    // Resolve the ambiguous name "Johnson".
    // This method call results in a ResolveNames call to EWS.
    NameResolutionCollection resolvedNames = service.ResolveName(
        "johnson", folders, ResolveNameSearchLocation.ContactsOnly, true);
    // Output the list of candidate email addresses and contact names.
    foreach (NameResolution nameRes in resolvedNames)
    {
        Console.WriteLine("Contact e-mail address: " + nameRes.Mailbox.Address);
        Console.WriteLine("Contact ID: " + nameRes.Mailbox.Id);
    }
}
```

Nachdem der **ResolveNames-Methodenaufruf** eine Antwort mit einer ID zurückgegeben hat, können Sie den Kontakt mithilfe der ID und des [impliziten Zugriffs](delegate-access-and-ews-in-exchange.md#bk_implicit) [abrufen, aktualisieren oder löschen,](#bk_getewsma) &mdash; und Sie müssen die SMTP-Adresse des Postfachbesitzers nicht angeben. 

<a name="bk_resolveews"> </a>

## <a name="resolve-a-contact-as-a-delegate-by-using-ews"></a>Auflösen eines Kontakts als Stellvertretung mithilfe von EWS

Mit EWS können Sie das Dienstobjekt für den Stellvertreterbenutzer verwenden, um Teilnamen im Kontaktordner des Postfachbesitzers aufzulösen. In diesem Beispiel wird gezeigt, wie sie den [ResolveNames-Vorgang](https://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) verwenden, um Besprechungen im Kontaktordner des Postfachbesitzers zu suchen, die das Wort "csv" enthalten. 
  
Dies ist auch die XML-Anforderung, die die verwaltete EWS-API sendet, wenn Sie die **ResolveName** -Methode zum [Auflösen eines Kontakts](#bk_resolveewsma)verwenden.
  
```xml
 <?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:ResolveNames ReturnFullContactData="true"
                    SearchScope="Contacts">
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="contacts">
          <t:Mailbox>
            <t:EmailAddress>primary@contoso.com</t:EmailAddress>
          </t:Mailbox>
        </t:DistinguishedFolderId>
      </m:ParentFolderIds>
      <m:UnresolvedEntry>johnson</m:UnresolvedEntry>
    </m:ResolveNames>
  </soap:Body>
</soap:Envelope>
```

Der Server antwortet auf die **ResolveNames-Anforderung** mit einer [ResolveNamesResponse-Nachricht,](https://msdn.microsoft.com/library/5e7be1e2-44ea-403f-9135-2388d030078c%28Office.15%29.aspx) die den [ResponseCode-Elementwert](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **"NoError"** enthält, der angibt, dass der Vorgang erfolgreich abgeschlossen wurde und nur ein Ergebnis gefunden hat, oder **ErrorNameResolutionMultipleResults,** wenn mehrere Ergebnisse gefunden wurden . Dies wird im dritten Codebeispiel basierend auf dem Kontakt ["Kontakt als Stellvertreter erstellen" mithilfe der verwalteten EWS-API](#bk_createewsma)gezeigt. Die Antwort enthält auch die [ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) jedes Ergebnisses. 
  
Der Wert des **ItemId-Elements** wurde zur besseren Lesbarkeit gekürzt. 
  
```XML
 <?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="893"
                         MinorBuildNumber="17"
                         Version="V2_10"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body>
    <m:ResolveNamesResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                            xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:ResolveNamesResponseMessage ResponseClass="Warning">
          <m:MessageText>Multiple results were found.</m:MessageText>
          <m:ResponseCode>ErrorNameResolutionMultipleResults</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:ResolutionSet TotalItemsInView="2"
                           IncludesLastItemInRange="true">
            <t:Resolution>
              <t:Mailbox>
                <t:Name>brian_1@contoso.com</t:Name>
                <t:EmailAddress>brian_1@contoso.com</t:EmailAddress>
                <t:RoutingType>SMTP</t:RoutingType>
                <t:MailboxType>Contact</t:MailboxType>
                <t:ItemId Id="iMihAAA="
                          ChangeKey="EQAAABYAAADOilbYa8KaT7ZgMoTz2P+hAAABiPQo" />
              </t:Mailbox>
            </t:Resolution>
            <t:Resolution>
              <t:Mailbox>
                <t:Name>brian_2@contoso.com</t:Name>
                <t:EmailAddress>brian_2@contoso.com</t:EmailAddress>
                <t:RoutingType>SMTP</t:RoutingType>
                <t:MailboxType>Contact</t:MailboxType>
                <t:ItemId Id="iMihAAA="
                          ChangeKey="EQAAABYAAADOilbYa8KaT7ZgMoTz2P+hAAABiPQo" />
              </t:Mailbox>
            </t:Resolution>
          </m:ResolutionSet>
        </m:ResolveNamesResponseMessage>
      </m:ResponseMessages>
    </m:ResolveNamesResponse>
  </s:Body>
</s:Envelope>
```

Nachdem Sie nun über die **ItemId** für die Kontakte verfügen, die dem mehrdeutigen Namen entsprechen, können Sie [Kontaktelemente mithilfe von EWS mithilfe der](#bk_getews) **ItemId** und des [impliziten Zugriffs](delegate-access-and-ews-in-exchange.md#bk_implicit)als Stellvertretung abrufen, aktualisieren oder &mdash; löschen, und Sie müssen nicht die SMTP-Adresse des Postfachbesitzers angeben. 

<a name="bk_getewsma"> </a>

## <a name="get-update-or-delete-contact-items-as-a-delegate-by-using-the-ews-managed-api"></a>Abrufen, Aktualisieren oder Löschen von Kontaktelementen als Delegat mithilfe der verwalteten EWS-API

Sie können die verwaltete EWS-API verwenden, um einen Kontakt auf die gleiche Weise abzurufen, zu aktualisieren oder zu löschen, wie Sie diese Aktionen ausführen, wenn Sie keinen Delegatenzugriff verwenden. Der einzige Unterschied besteht darin, dass das Dienstobjekt für den Delegatenbenutzer gilt. Die im **Bind-Methodenaufruf** enthaltene Element-ID identifiziert das Element im Postfachspeicher eindeutig im Kontaktordner des Postfachbesitzers. 
  
**Tabelle 2. Verwaltete EWS-API-Methoden, die mit einem Kontakt als Delegat arbeiten**

|**Aufgabe**|**EWS Managed API-Methode**|**Codebeispiel**|
|:-----|:-----|:-----|
|Abrufen eines Kontakts  <br/> |[Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) <br/> |[Abrufen eines Elements mithilfe der verwalteten EWS-API](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getewsma) <br/> |
|Einen Kontakt aktualisieren  <br/> |[Binden](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) gefolgt von [Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx) <br/> |[Aktualisieren eines Elements mithilfe der verwalteten EWS-API](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_updateewsma) <br/> |
|Löschen eines Kontakts  <br/> |[Binden](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) gefolgt von ["Löschen"](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx) <br/> |[Löschen eines Elements mithilfe der verwalteten EWS-API](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteewsma) <br/> |

<a name="bk_getews"> </a>

## <a name="get-update-or-delete-contact-items-as-a-delegate-by-using-ews"></a>Abrufen, Aktualisieren oder Löschen von Kontaktelementen als Stellvertretung mithilfe von EWS

Sie können EWS verwenden, um einen Besprechungs- oder Terminkontakt auf die gleiche Weise abzurufen, zu aktualisieren oder zu löschen, wie Sie diese Aktionen ausführen, wenn Sie keinen Stellvertretungszugriff verwenden. Der einzige Unterschied besteht darin, dass das Dienstobjekt für den Delegatenbenutzer gilt. Die in der [GetItem-Anforderung](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) enthaltene Element-ID identifiziert das Element im Postfachspeicher eindeutig im Kontaktordner des Postfachbesitzers. 
  
**Tabelle 3. EWS-Vorgänge für die Arbeit mit einem Kontakt als Delegat**

|**Aufgabe**|**EWS-Vorgang**|**Beispiel**|
|:-----|:-----|:-----|
|Abrufen eines Kontakts  <br/> |[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |[Abrufen eines Elements mithilfe von EWS](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getews) <br/> |
|Einen Kontakt aktualisieren  <br/> |[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) gefolgt von [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |[Aktualisieren eines Elements mithilfe von EWS](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_updateews) <br/> |
|Löschen eines Kontakts  <br/> |[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) gefolgt von [DeleteItem](../web-service-reference/deleteitem-operation.md) <br/> |[Löschen eines Elements mithilfe von EWS](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteews) <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Stellvertretungszugriff und EWS in Exchange](delegate-access-and-ews-in-exchange.md)
- [Hinzufügen und Entfernen von Delegaten mithilfe der EWS in Exchange](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md)
- [Festlegen von Ordnerberechtigungen für einen anderen Benutzer mithilfe der EWS in Exchange](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md)
- [Personen und Kontakte in EWS in Exchange](people-and-contacts-in-ews-in-exchange.md)
- [Auflösen von mehrdeutigen Namen mithilfe der EWS Exchange 2013](how-to-resolve-ambiguous-names-by-using-ews-in-exchange-2013.md)
    

