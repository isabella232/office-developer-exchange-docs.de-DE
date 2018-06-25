---
title: Access-Kontakte als Stellvertretung mithilfe der EWS in Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3cd34c14-18b0-4fe2-a4c2-d884318c88fc
description: Hier erfahren Sie, wie Sie Kontakte als Stellvertreter zugreifen, indem Sie die EWS Managed API oder EWS in Exchange.
ms.openlocfilehash: a7f695dcbe0693809817de84284294dff872aa9c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756855"
---
# <a name="access-contacts-as-a-delegate-by-using-ews-in-exchange"></a>Access-Kontakte als Stellvertretung mithilfe der EWS in Exchange

Hier erfahren Sie, wie Sie Kontakte als Stellvertreter zugreifen, indem Sie die EWS Managed API oder EWS in Exchange.
  
Der EWS Managed API oder EWS können Sie um einem Benutzer den Zugriff auf eine Postfachbesitzer Kontakteordner zu gewähren. Die Stellvertretung kann Klicken Sie dann Kontakte im Auftrag des Postfachbesitzers erstellen und abrufen, aktualisieren und Löschen von Kontakten aus dem Ordner Kontakte des Postfachbesitzers abhängig von ihren Berechtigungen.
  
Als Stellvertretung verwenden Sie die gleichen Methoden und Vorgänge auf des Postfachbesitzers Kontakteordner zugreifen, mit denen Sie Ihre eigenen Ordner Kontakte zugreifen. Der Hauptunterschied ist, dass Sie mithilfe von [expliziten Access](delegate-access-and-ews-in-exchange.md#bk_explicit) suchen oder erstellen ein Kontaktelement, und klicken Sie dann, nachdem Sie die Element-ID identifiziert haben, können [impliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_implicit) erhalten möchten, aktualisieren und Löschen des Elements. 
  
**In Tabelle 1. EWS Managed API-Methoden und EWS-Vorgänge für den Zugriff auf einen Kontakt als Stellvertreter**

|**Aktion**|**Verwenden Sie diese Methode EWS Managed API...**|**Verwenden Sie diese Operation EWS...**|
|:-----|:-----|:-----|
|Erstellen Sie einen Kontakt als Stellvertreter  <br/> |[Item.Save](http://msdn.microsoft.com/en-us/library/dd635209%28v=exchg.80%29.aspx) , in dem der Parameter [FolderId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) [expliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) auf den Postfachbesitzer Kontakteordner bietet  <br/> |[CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) , in dem das [Postfach](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) -Element gibt an, die [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) des Postfachbesitzers  <br/> |
|Erstellen Sie mehrere Kontakte als Stellvertreter  <br/> |[ExchangeService.CreateItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) , in dem der Parameter **FolderId** [expliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) auf den Postfachbesitzer Kontakteordner bietet  <br/> |[CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) , in dem das [Postfach](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) -Element gibt an, die [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) des Postfachbesitzers  <br/> |
|Beheben Sie einen Kontakt als Stellvertreter  <br/> |[ExchangeService.ResolveName](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) , in dem der Parameter [FolderId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) [expliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) auf den Postfachbesitzer Kontakteordner bietet  <br/> |[ResolveNames](http://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) , in dem das [Postfach](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) -Element gibt an, die [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) des Postfachbesitzers  <br/> |
|Suchen Sie nach oder Suchen nach einem Kontakt als Stellvertreter  <br/> |[ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) , in dem der Parameter **FolderId** [expliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) auf den Postfachbesitzer Kontakteordner bietet  <br/> |[FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) , in dem das [Postfach](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) -Element gibt an, die [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) des Postfachbesitzers  <br/> |
|Abrufen eines Kontakts als Stellvertreter  <br/> |[Contact.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.contact.bind%28v=exchg.80%29.aspx) <br/> |[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |
|Aktualisieren eines Kontakts als Stellvertreter  <br/> |[Contact.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.contact.bind%28v=exchg.80%29.aspx) gefolgt von [Contact.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.update%28v=exchg.80%29.aspx) <br/> |[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) gefolgt von [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |
|Löschen eines Kontakts als Stellvertreter  <br/> |[Contact.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.contact.bind%28v=exchg.80%29.aspx) gefolgt von [Contact.Delete](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.delete%28v=exchg.80%29.aspx) <br/> |[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) gefolgt von [DeleteItem](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) <br/> |
   
> [!NOTE]
> In den Codebeispielen in diesem Artikel ist primary@contoso.com der Postfachbesitzer. 

<a name="bk_prereq"> </a>

## <a name="prerequisite-tasks"></a>Erforderliche Aufgaben

Bevor ein Benutzer des Postfachbesitzers Kontakteordner als Stellvertreter zugreifen kann, muss der Benutzer des Postfachbesitzers Kontakteordner [als Stellvertreter mit Berechtigungen hinzugefügt](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md) . 

<a name="bk_createewsma"> </a>

## <a name="create-a-contact-as-a-delegate-by-using-the-ews-managed-api"></a>Erstellen eines Kontakts eine Stellvertretung mithilfe der EWS Managed API

Die EWS Managed API können Sie das Objekt für den Benutzer Delegaten verwenden, um Kontakte für den Besitzer des Postfachs zu erstellen. In diesem Beispiel wird veranschaulicht, wie mit der [Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) -Methode erstellen Sie eine Besprechung und Besprechungsanfragen an die Teilnehmer senden. 
  
In diesem Beispiel wird davon ausgegangen, die **Service** ist ein gültiges [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objekt für den Delegaten und, die der Stellvertreter die entsprechenden Berechtigungen für den Postfachbesitzer Kontakteordner gewährt wurde. 
  
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

Beachten Sie, dass beim Speichern des Elements Methodenaufruf [Speichern](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) des Postfachbesitzers Kontakteordner bestimmen muss. Wenn der Postfachbesitzer Kontakteordner nicht angegeben ist, ruft die Besprechungsanfrage Kontakteordner der Stellvertretung und nicht des Postfachbesitzers Kontakteordner gespeichert. Sie können den Postfachbesitzer Kontaktordners im Methodenaufruf **Speichern** in zwei-Wege-einschließen. Es wird empfohlen, dass Sie eine neue Instanz des Objekts [FolderId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) instanziieren, mithilfe der [WellKnownFolderName](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) und die SMTP-Adresse des Postfachbesitzers. 
  
```cs
contact.Save(new FolderId(WellKnownFolderName.Contacts, "primary@contoso.com"));
```

Sie können jedoch auch [gebunden werden](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) in den Ordner Kontakte zuerst, und verwenden Sie die ID des Ordners in den Methodenaufruf **zu speichern** . Beachten Sie jedoch, dass dieser einen zusätzlichen EWS-Aufruf erstellt. 
  
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

## <a name="create-a-contact-as-a-delegate-by-using-ews"></a>Erstellen eines Kontakts eine Stellvertretung mithilfe der Exchange-Webdienste

Exchange-Webdienste können Sie das Objekt für den Benutzer Delegaten verwenden Sie zum Erstellen von Kontaktelementen (engl.) für den Besitzer des Postfachs. Dieses Beispiel zeigt, wie Sie den [CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) -Vorgang verwenden, um einen Kontakt zu erstellen. 
  
Dies ist auch die XML-Anfrage, die die EWS Managed API sendet, wenn Sie die **Speichern** -Methode erstellen Sie [einen Kontakt](#bk_createewsma)verwenden.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

Der Server antwortet auf die **CreateItem** -Anforderung mit einer [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) -Nachricht, die enthält den Elementwert [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **noError zurück**, der angibt, dass der Kontakt erfolgreich erstellt wurde. Die Antwort enthält auch die Element-ID des neu erstellten Kontakts.

<a name="bk_resolveewsma"> </a>

## <a name="resolve-a-contact-as-a-delegate-by-using-the-ews-managed-api"></a>Beheben Sie einen Kontakt als Stellvertretung mithilfe der EWS Managed API

Um einen Kontakt basierend auf möglicherweise mehrdeutige Namen oder einen Ausdruck ermittelt wird, müssen Sie eine der Methoden [ExchangeService.ResolveName](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) , die einen [FolderId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) -Parameter verwenden, damit Sie den Postfachbesitzer Kontakteordner angeben können. 
  
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

Nachdem eine Antwort mit einer ID **ResolveNames** Methodenaufruf zurückgegeben wird, können Sie [abrufen, aktualisieren oder löschen Sie den Kontakt](#bk_getewsma) mit der ID und [impliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_implicit)&mdash;und müssen nicht die SMTP-Adresse des Postfachbesitzers angeben. 

<a name="bk_resolveews"> </a>

## <a name="resolve-a-contact-as-a-delegate-by-using-ews"></a>Beheben Sie einen Kontakt als Stellvertreter mithilfe der Exchange-Webdienste

EWS können Sie das Objekt für den Benutzer Delegaten verwenden, um im Ordner "Kontakte" des Postfachbesitzers partiellen Namen aufzulösen. In diesem Beispiel wird veranschaulicht, wie mit den Vorgang [ResolveNames](http://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) finden Besprechungen in der Postfachbesitzer Kontakteordner, die das Wort "Johnson" enthalten. 
  
Dies ist auch die XML-Anfrage, die die EWS Managed API sendet, wenn Sie die **ResolveName** -Methode zum [Auflösen eines Kontakts](#bk_resolveewsma)verwenden.
  
```xml
 <?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

Der Server antwortet auf die Anforderung **ResolveNames** mit einer [ResolveNamesResponse](http://msdn.microsoft.com/library/5e7be1e2-44ea-403f-9135-2388d030078c%28Office.15%29.aspx) -Nachricht, die enthält den Wert [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) Element **noError zurück**, das anzeigt, dass den Vorgang erfolgreich abgeschlossen wurde und nur eine gefunden Ergebnis oder **ErrorNameResolutionMultipleResults** mehrere Ergebnisse gefunden – das ist, was im dritten Codebeispiel wird basierend auf den Kontakt, [Erstellen Sie einen Kontakt als Stellvertretung mithilfe der EWS Managed API](#bk_createewsma)angezeigt werden. Die Antwort enthält auch die [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) jedes Ergebnisses. 
  
Der Wert des Elements **ItemId** wurde zur besseren Lesbarkeit gekürzt. 
  
```XML
 <?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="893"
                         MinorBuildNumber="17"
                         Version="V2_10"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body>
    <m:ResolveNamesResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                            xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

Nun, da Sie die **ItemId** für die Kontakte verfügen, mehrdeutigen Name entsprechen, können Sie [abrufen, aktualisieren oder Löschen von Kontaktelementen als Stellvertretung mithilfe der Exchange-Webdienste](#bk_getews) mithilfe der **ItemId** und [impliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_implicit)&mdash;und müssen nicht angeben SMTP-Adresse des Postfachbesitzers. 

<a name="bk_getewsma"> </a>

## <a name="get-update-or-delete-contact-items-as-a-delegate-by-using-the-ews-managed-api"></a>Abrufen, aktualisieren oder Löschen von Kontaktelementen als Stellvertretung mithilfe der EWS Managed API

Die EWS Managed API können Sie abrufen, aktualisieren oder Löschen eines Kontakts auf die gleiche Weise, die Sie diese Aktionen ausführen, wenn Sie Stellvertretungszugriff nicht verwenden. Der einzige Unterschied ist, dass das Objekt für den Benutzer Delegat ist. Die Element-ID im Methodenaufruf **binden** enthalten sind, eindeutig identifiziert das Element im Postfachspeicher im Ordner "Kontakte" des Postfachbesitzers. 
  
**In Tabelle 2. Arbeiten mit einem Kontakt eine Stellvertretung EWS Managed API-Methoden**

|**Aufgabe**|**EWS Managed API-Methode**|**Codebeispiel**|
|:-----|:-----|:-----|
|Abrufen eines Kontakts  <br/> |[Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) <br/> |[Abrufen eines Elements mithilfe der EWS Managed API](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getewsma) <br/> |
|Aktualisieren eines Kontakts  <br/> |[Binden von](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) gefolgt von [Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx) <br/> |[Aktualisieren eines Elements mithilfe der EWS Managed API](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_updateewsma) <br/> |
|Löschen eines Kontakts  <br/> |[Binden von](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) gefolgt von [Löschen](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx) <br/> |[Löschen eines Elements mithilfe der EWS Managed API](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteewsma) <br/> |

<a name="bk_getews"> </a>

## <a name="get-update-or-delete-contact-items-as-a-delegate-by-using-ews"></a>Erhalten möchten, aktualisieren oder Löschen von Kontaktelementen als Stellvertreter mithilfe der Exchange-Webdienste

Exchange-Webdienste können Sie abrufen, aktualisieren oder Löschen eines Besprechung oder eines Termins Kontakts auf die gleiche Weise, dass Sie diese Aktionen ausführen, wenn Sie Stellvertretungszugriff nicht verwenden. Der einzige Unterschied ist, dass das Objekt für den Benutzer Delegat ist. Die Element-ID, enthalten in der [GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) -Anforderung eindeutig identifiziert das Element im Postfachspeicher im Ordner "Kontakte" des Postfachbesitzers. 
  
**Tabelle 3. EWS-Vorgänge für die Arbeit mit einem Kontakt als Stellvertreter**

|**Aufgabe**|**EWS-Vorgang**|**Beispiel**|
|:-----|:-----|:-----|
|Abrufen eines Kontakts  <br/> |[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |[Abrufen eines Elements mithilfe der Exchange-Webdienste](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getews) <br/> |
|Aktualisieren eines Kontakts  <br/> |[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) gefolgt von [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |[Aktualisieren eines Elements mithilfe der Exchange-Webdienste](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_updateews) <br/> |
|Löschen eines Kontakts  <br/> |[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) gefolgt von [DeleteItem](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) <br/> |[Löschen eines Elements mithilfe der Exchange-Webdienste](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteews) <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Stellvertretungszugriff und EWS in Exchange](delegate-access-and-ews-in-exchange.md)
- [Hinzufügen und Entfernen von Stellvertretungen mithilfe von EWS in Exchange](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md)
- [Legen Sie Berechtigungen für einen anderen Benutzer mithilfe der EWS in Exchange](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md)
- [Benutzer und Kontakte in EWS in Exchange](people-and-contacts-in-ews-in-exchange.md)
- [Lösen Sie mehrdeutige Namen auf, mithilfe von EWS in Exchange 2013](how-to-resolve-ambiguous-names-by-using-ews-in-exchange-2013.md)
    

