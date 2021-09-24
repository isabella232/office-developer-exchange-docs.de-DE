---
title: Zugreifen auf E-Mails als Stellvertretung mithilfe der EWS in Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: a8123604-c7c0-405d-a0ed-7a9b4a431bfd
description: Erfahren Sie, wie Sie mithilfe der verwalteten EWS-API oder EWS in Exchange auf E-Mails als Stellvertretung zugreifen.
ms.openlocfilehash: aa921bc36004b3a26caa514390e52249021b304f
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521214"
---
# <a name="access-email-as-a-delegate-by-using-ews-in-exchange"></a>Zugreifen auf E-Mails als Stellvertretung mithilfe der EWS in Exchange

Erfahren Sie, wie Sie mithilfe der verwalteten EWS-API oder EWS in Exchange auf E-Mails als Stellvertretung zugreifen.
  
Sie können die verwaltete EWS-API oder EWS verwenden, um einem Benutzer delegaten Zugriff auf den Posteingangsordner eines Postfachbesitzers zu gewähren. Der Stellvertreter kann dann Besprechungsanfragen im Namen des Postfachbesitzers erstellen, nach E-Mails suchen und E-Mails aus dem Posteingangsordner des Postfachbesitzers abrufen, aktualisieren und löschen, je nach ihren Berechtigungen.
  
Als Stellvertretung verwenden Sie die gleichen Methoden und Vorgänge, um auf den Posteingangsordner eines Postfachbesitzers zuzugreifen, den Sie für den Zugriff auf einen Posteingangsordner ohne Stellvertretungszugriff verwenden. Der Hauptunterschied besteht darin, dass Sie [expliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_explicit) verwenden müssen, um ein E-Mail-Element zu suchen oder zu erstellen. Nachdem Sie die Element-ID identifiziert haben, können Sie [impliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_implicit) verwenden, um das Element abzurufen, zu aktualisieren oder zu löschen. 
  
**Tabelle 1. Verwaltete EWS-API-Methoden und EWS-Vorgänge für den Zugriff auf E-Mails als Stellvertretung**

|**Aktion**|**Verwenden Sie diese verwaltete EWS-API-Methode...**|**Verwenden Sie diesen EWS-Vorgang...**|
|:-----|:-----|:-----|
|Erstellen und Senden einer E-Mail als Stellvertretung  <br/> |[EmailMessage.Save](https://msdn.microsoft.com/library/dd635209%28v=exchg.80%29.aspx) where the [FolderId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Drafts folder  <br/> [EmailMessage.SendAndSaveCopy,](https://msdn.microsoft.com/library/dd634248%28v=exchg.80%29.aspx) wobei der [Parameter FolderId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) [expliziten Zugriff auf](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) den Ordner "Gesendete Elemente" des Postfachbesitzers bietet  <br/> |[CreateItem,](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) wobei das [Mailbox-Element](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) die [EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) des Postfachbesitzers angibt  <br/> [SendItem,](https://msdn.microsoft.com/library/a966da19-b05a-4504-ac98-91acc1667b9a%28Office.15%29.aspx) wobei das [Mailbox-Element](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) die [EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) des Postfachbesitzers angibt  <br/> |
|Erstellen mehrerer E-Mail-Nachrichten als Stellvertretung  <br/> |[ExchangeService.CreateItems,](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) wobei der **Parameter FolderId** [expliziten Zugriff auf](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) den Posteingangsordner des Postfachbesitzers bietet  <br/> |[CreateItem,](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) wobei das [Mailbox-Element](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) die [EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) des Postfachbesitzers angibt  <br/> |
|Suchen nach oder Suchen einer E-Mail als Stellvertretung  <br/> |[ExchangeService.FindItems,](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) wobei der **Parameter FolderId** [expliziten Zugriff auf](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) den Posteingangsordner des Postfachbesitzers bietet  <br/> |[FindItem,](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) wobei das [Mailbox-Element](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) die [EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) des Postfachbesitzers angibt  <br/> |
|Abrufen einer E-Mail als Stellvertretung  <br/> |[EmailMessage.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) <br/> |[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |
|Aktualisieren einer E-Mail als Stellvertretung  <br/> |[EmailMessage.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) gefolgt von [EmailMessage.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx) <br/> |[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) gefolgt von [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |
|Löschen einer E-Mail als Stellvertretung  <br/> |[EmailMessage.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) gefolgt von [EmailMessage.Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.delete%28v=exchg.80%29.aspx) <br/> |[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) gefolgt von [DeleteItem](../web-service-reference/deleteitem-operation.md) <br/> |
   
Beachten Sie beim Arbeiten mit E-Mails als Stellvertretung Folgendes:
  
- Wenn ein Stellvertreter nur mit Besprechungsanfragen und -antworten arbeiten muss, benötigt die Stellvertretung keinen Zugriff auf den Ordner "Posteingang". Weitere Informationen finden Sie unter [den erforderlichen Aufgaben für den Zugriff auf Kalender als Stellvertretung.](how-to-access-a-calendar-as-a-delegate-by-using-ews-in-exchange.md#bk_prereq)
    
- Wenn ein Empfänger eine Nachricht empfängt, die im Auftrag eines Postfachbesitzers gesendet wurde, wird der Absender als *"Stellvertreter*  im Auftrag des  *Postfachbesitzers"*  angezeigt. 
    
> [!NOTE]
> In den Codebeispielen in diesem Artikel ist primary@contoso.com der Postfachbesitzer. 
  
## <a name="prerequisite-tasks"></a>Erforderliche Aufgaben
<a name="bk_prereq"> </a>

Bevor ein Benutzer als Stellvertreter auf den Posteingangsordner des Postfachbesitzers zugreifen kann, muss der Benutzer [als Stellvertretung mit Berechtigungen](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md) für den Posteingangsordner des Postfachbesitzers hinzugefügt werden. 
  
## <a name="create-and-send-an-email-as-a-delegate-by-using-the-ews-managed-api"></a>Erstellen und Senden einer E-Mail als Stellvertretung mithilfe der verwalteten EWS-API
<a name="bk_createewsma"> </a>

Mit der verwalteten EWS-API können Sie das Dienstobjekt für den Stellvertreterbenutzer verwenden, um E-Mails im Namen des Postfachbesitzers zu erstellen und zu senden. In diesem Beispiel wird gezeigt, wie Sie die [Save-Methode](https://msdn.microsoft.com/library/dd635209%28v=exchg.80%29.aspx) verwenden, um die Nachricht im Ordner "Entwürfe" des Postfachbesitzers zu speichern, und dann die [SendAndSaveCopy-Methode,](https://msdn.microsoft.com/library/dd634248%28v=exchg.80%29.aspx) um die E-Mail zu senden und die Nachricht im Ordner "Gesendete Elemente" des Postfachbesitzers zu speichern. 
  
In diesem Beispiel wird davon ausgegangen, dass **der Dienst** ein gültiges [ExchangeService-Objekt](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) für die Stellvertretung ist und dass der Stellvertretung die [entsprechenden Berechtigungen für den Ordner Posteingang, Entwürfe und gesendete Elemente des Postfachbesitzers](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md)erteilt wurden.
  
```cs
public static void DelegateAccessCreateEmail(ExchangeService service)
{
    // Create an email message and provide it with connection 
    // configuration information by using an ExchangeService 
    // object named service.
    EmailMessage message = new EmailMessage(service);
    // Set properties on the email message.
    message.Subject = "Company Soccer Team";
    message.Body = "Are you interested in joining?";
    message.ToRecipients.Add("sadie@contoso.com");
    // Save the email to the mailbox owner's Drafts folder.
    // This method call results in a CreateItem call to EWS.
    // The FolderId parameter contains the context for the 
    // mailbox owner's Inbox folder. Any additional actions 
    // taken on this message will be performed in the mailbox 
    // owner's mailbox. 
    message.Save(new FolderId(WellKnownFolderName.Drafts, new Mailbox("primary@contoso.com")));
    // Send the email and save the message in the mailbox owner's 
    // Sent Items folder.
    // This method call results in a SendItem call to EWS.
    message.SendAndSaveCopy(new FolderId(WellKnownFolderName.SentItems, new Mailbox("primary@contoso.com")));
    Console.WriteLine("An email with the subject '" + message.Subject + "' has been sent to '" 
    + message.ToRecipients[0] + "' and saved in the Sent Items folder of the mailbox owner.");
}
```

## <a name="create-and-send-an-email-as-a-delegate-by-using-ews"></a>Erstellen und Senden einer E-Mail als Stellvertretung mithilfe von EWS
<a name="bk_createews"> </a>

Mit EWS können Sie das Dienstobjekt für den Stellvertreterbenutzer verwenden, um E-Mails im Namen des Postfachbesitzers zu erstellen und zu senden. In diesem Beispiel wird gezeigt, wie sie den [CreateItem-Vorgang](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) verwenden, um eine E-Mail zu erstellen, und den [SendItem-Vorgang,](https://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) um die Zeit zu senden und im Ordner "Gesendete Elemente" des Postfachbesitzers zu speichern. 
  
Dies ist auch die erste XML-Anforderung, die die verwaltete EWS-API sendet, wenn Sie die **Save-Methode** zum [Erstellen und Senden einer E-Mail](#bk_createewsma)verwenden.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version=" Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:CreateItem MessageDisposition="SaveOnly">
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="drafts">
          <t:Mailbox>
            <t:EmailAddress>primary@contoso.com</t:EmailAddress>
          </t:Mailbox>
        </t:DistinguishedFolderId>
      </m:SavedItemFolderId>
      <m:Items>
        <t:Message>
          <t:Subject>Company Soccer Team</t:Subject>
          <t:Body BodyType="HTML">Are you interested in joining?</t:Body>
          <t:ToRecipients>
            <t:Mailbox>
              <t:EmailAddress>sadie@contoso.com</t:EmailAddress>
            </t:Mailbox>
          </t:ToRecipients>
        </t:Message>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

Der Server antwortet auf die **CreateItem-Anforderung** mit einer [CreateItemResponse-Nachricht,](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) die den [ResponseCode-Elementwert](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **"NoError"** enthält, der angibt, dass die E-Mail erstellt und erfolgreich gespeichert wurde. Die Antwort enthält auch die Element-ID der neu erstellten E-Mail.
  
Der **ItemId-Wert** wurde zur besseren Lesbarkeit gekürzt. 
  
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
    <m:CreateItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:CreateItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Message>
              <t:ItemId Id="iNRaAAA="
                        ChangeKey="CQAAABYAAADOilbYa8KaT7ZgMoTz2P+hAAABiQPU" />
            </t:Message>
          </m:Items>
        </m:CreateItemResponseMessage>
      </m:ResponseMessages>
    </m:CreateItemResponse>
  </s:Body>
</s:Envelope>
```

Verwenden Sie als Nächstes den **SendItem-Vorgang,** um die Nachricht im Auftrag des Postfachbesitzers zu senden und im Ordner "Gesendete Elemente" des Postfachbesitzers zu speichern. 
  
Der **ItemId-Wert** wurde zur besseren Lesbarkeit gekürzt. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version=" Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:SendItem SaveItemToFolder="true">
      <m:ItemIds>
        <t:ItemId Id="iNRaAAA="
                  ChangeKey="CQAAABYAAADOilbYa8KaT7ZgMoTz2P+hAAABiQPU" />
      </m:ItemIds>
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="sentitems">
          <t:Mailbox>
            <t:EmailAddress>primary@contoso.com</t:EmailAddress>
          </t:Mailbox>
        </t:DistinguishedFolderId>
      </m:SavedItemFolderId>
    </m:SendItem>
  </soap:Body>
</soap:Envelope>
```

Der Server antwortet auf die **SendItem-Anforderung** mit einer [SendItemResponse-Nachricht,](https://msdn.microsoft.com/library/26ac41c7-57d9-473e-ab7a-bae93e1d2aba%28Office.15%29.aspx) die den [ResponseCode-Elementwert](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **"NoError"** enthält, der angibt, dass die E-Mail erfolgreich gesendet und im Ordner "Gesendete Elemente" des Postfachbesitzers gespeichert wurde.
  
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
    <m:SendItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:SendItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:SendItemResponseMessage>
      </m:ResponseMessages>
    </m:SendItemResponse>
  </s:Body>
</s:Envelope>
```

## <a name="search-for-an-email-as-a-delegate-by-using-the-ews-managed-api"></a>Suchen nach einer E-Mail als Stellvertretung mithilfe der verwalteten EWS-API
<a name="bk_searchewsma"> </a>

Um nach einer E-Mail zu suchen, müssen Sie eine der [ExchangeService.FindItems-Methoden](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) verwenden, die einen [FolderId-Parameter](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) enthalten, damit Sie den Posteingangsordner des Postfachbesitzers angeben können. 
  
```cs
static void DelegateAccessSearchEmailWithFilter(ExchangeService service)
{
    // Limit the result set to 10 items.
    ItemView view = new ItemView(10);
    // Define the search filter.
    SearchFilter.ContainsSubstring filter = new SearchFilter.ContainsSubstring(ItemSchema.Subject, 
        "soccer", ContainmentMode.Substring, ComparisonMode.IgnoreCase);
    view.PropertySet = new PropertySet(ItemSchema.Subject,
                                       ItemSchema.DateTimeReceived,
                                       EmailMessageSchema.IsRead);
    // Item searches do not support deep traversal.
    view.Traversal = ItemTraversal.Shallow;
    // Sorting.
    view.OrderBy.Add(ItemSchema.DateTimeReceived, SortDirection.Descending);
    try
    {
        // Call FindItems to find matching Inbox items. 
        // The parameters of FindItems must denote the mailbox owner,
        // mailbox, and Inbox folder.
        // This call results in a FindItem call to EWS.
        FindItemsResults<Item> results = service.FindItems(new 
            FolderId(WellKnownFolderName.Inbox, "primary@contoso.com"), 
            filter, view);
        foreach (Item item in results.Items)
        {
            Console.WriteLine("Subject: {0}", item.Subject);
            Console.WriteLine("Id: {0}", item.Id.ToString());
            if (item is EmailMessage)
            {
                EmailMessage message = item as EmailMessage;
                Console.WriteLine("Read: {0}", message.IsRead.ToString());
            }
        }
    }
    catch (Exception ex)
    {
        Console.WriteLine("Exception while enumerating results: {0}", ex.Message);
    }
}
```

Nachdem der **FindItems-Aufruf** eine Antwort mit einer ID zurückgegeben hat, können Sie diese E-Mail mithilfe der ID und des [impliziten Zugriffs](delegate-access-and-ews-in-exchange.md#bk_implicit) abrufen, aktualisieren oder löschen – und Sie müssen nicht die SMTP-Adresse des Postfachbesitzers angeben. 
  
## <a name="search-for-an-email-as-a-delegate-by-using-ews"></a>Suchen nach einer E-Mail als Stellvertretung mithilfe von EWS
<a name="bk_searchews"> </a>

Mit EWS können Sie das Dienstobjekt für den Stellvertretungsbenutzer verwenden, um nach E-Mails zu suchen, die eine Reihe von Suchkriterien erfüllen. In diesem Beispiel wird gezeigt, wie der [FindItem-Vorgang](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) verwendet wird, um Nachrichten im Posteingangsordner des Besitzers zu suchen, die das Wort "sport" im Betreff enthalten. 
  
Dies ist auch die XML-Anforderung, die die verwaltete EWS-API sendet, wenn Sie [nach einer E-Mail suchen.](#bk_searchewsma)
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version=" Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:FindItem Traversal="Shallow">
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
          <t:FieldURI FieldURI="item:DateTimeReceived" />
          <t:FieldURI FieldURI="message:IsRead" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:IndexedPageItemView MaxEntriesReturned="10"
                             Offset="0"
                             BasePoint="Beginning" />
      <m:Restriction>
        <t:Contains ContainmentMode="Substring"
                    ContainmentComparison="IgnoreCase">
          <t:FieldURI FieldURI="item:Subject" />
          <t:Constant Value="soccer" />
        </t:Contains>
      </m:Restriction>
      <m:SortOrder>
        <t:FieldOrder Order="Descending">
          <t:FieldURI FieldURI="item:DateTimeReceived" />
        </t:FieldOrder>
      </m:SortOrder>
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox">
          <t:Mailbox>
            <t:EmailAddress>primary@contoso.com</t:EmailAddress>
          </t:Mailbox>
        </t:DistinguishedFolderId>
      </m:ParentFolderIds>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

Der Server antwortet auf die **FindItem-Anforderung** mit einer [FindItemResponse-Nachricht,](https://msdn.microsoft.com/library/c8b316df-d4ab-49b8-96d4-8e9a016730ef%28Office.15%29.aspx) die den [ResponseCode-Elementwert](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **"NoError"** enthält, der angibt, dass die Suche erfolgreich abgeschlossen wurde. Die Antwort enthält ein [Message-Element](https://msdn.microsoft.com/library/2400b33c-43b2-4fc2-b6fb-275a99e0e810%28Office.15%29.aspx) für alle E-Mails, die die Suchkriterien erfüllt haben. In diesem Fall wird nur eine E-Mail gefunden. 
  
Der Wert des [ItemId-Elements](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) wurde zur besseren Lesbarkeit gekürzt. 
  
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
    <m:FindItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="1"
                        TotalItemsInView="1"
                        IncludesLastItemInRange="true">
            <t:Items>
              <t:Message>
                <t:ItemId Id="iNwoAAA="
                          ChangeKey="CQAAABYAAADOilbYa8KaT7ZgMoTz2P+hAAABiQuu" />
                <t:Subject>Soccer team</t:Subject>
                <t:DateTimeReceived>2014-03-10T06:16:55Z</t:DateTimeReceived>
                <t:IsRead>false</t:IsRead>
              </t:Message>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>
```

Nachdem Sie nun über die **ItemId** für die E-Mail verfügen, die Ihre Kriterien erfüllt, können Sie diese E-Mail mithilfe der **ItemId** und des [impliziten Zugriffs](delegate-access-and-ews-in-exchange.md#bk_implicit) abrufen, aktualisieren oder löschen – und Sie müssen nicht die SMTP-Adresse des Postfachbesitzers angeben. 
  
## <a name="get-update-or-delete-email-items-as-a-delegate-by-using-the-ews-managed-api"></a>Abrufen, Aktualisieren oder Löschen von E-Mail-Elementen als Delegat mithilfe der verwalteten EWS-API
<a name="bk_geteswma"> </a>

Sie können die verwaltete EWS-API verwenden, um eine E-Mail auf die gleiche Weise abzurufen, zu aktualisieren oder zu löschen, wie Sie diese Aktionen ausführen, wenn Sie keinen Stellvertretungszugriff verwenden. Der einzige Unterschied besteht darin, dass das **ExchangeService-Objekt** für den Delegatbenutzer vorgesehen ist. Die im **Bind-Methodenaufruf** enthaltene Element-ID identifiziert das Element im Postfachspeicher eindeutig im Posteingangsordner des Postfachbesitzers. 
  
**Tabelle 2. EWS Managed API-Methoden, die mit E-Mails als Delegat arbeiten**

|**Aufgabe**|**EWS Managed API-Methode**|**Codebeispiel**|
|:-----|:-----|:-----|
|Abrufen einer E-Mail  <br/> |[Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) <br/> |[Abrufen eines Elements mithilfe der verwalteten EWS-API](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getewsma) <br/> |
|Aktualisieren einer E-Mail  <br/> |[Binden](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) gefolgt von [Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx) <br/> |[Aktualisieren eines Elements mithilfe der verwalteten EWS-API](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_updateewsma) <br/> |
|Löschen einer E-Mail  <br/> |[Binden](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) gefolgt von ["Löschen"](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.delete%28v=exchg.80%29.aspx) <br/> |[Löschen eines Elements mithilfe der verwalteten EWS-API](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteewsma) <br/> |
   
## <a name="get-update-or-delete-email-items-as-a-delegate-by-using-ews"></a>Abrufen, Aktualisieren oder Löschen von E-Mail-Elementen als Delegat mithilfe von EWS
<a name="bk_getews"> </a>

Sie können die verwaltete EWS-API verwenden, um eine E-Mail auf die gleiche Weise abzurufen, zu aktualisieren oder zu löschen, wie Sie diese Aktionen ausführen, wenn Sie keinen Stellvertretungszugriff verwenden. Der einzige Unterschied besteht darin, dass das Dienstobjekt für den Delegatenbenutzer gilt. Die in der **GetItem-Anforderung** enthaltene Element-ID identifiziert das Element im Postfachspeicher eindeutig im Posteingangsordner des Postfachbesitzers. 
  
**Tabelle 3. EWS-Vorgänge zum Arbeiten mit E-Mails als Stellvertretung**

|**Aufgabe**|**EWS-Vorgang**|**Codebeispiel**|
|:-----|:-----|:-----|
|Abrufen einer E-Mail  <br/> |[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |[Abrufen eines Elements mithilfe von EWS](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getews) <br/> |
|Aktualisieren einer E-Mail  <br/> |[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) gefolgt von [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |[Aktualisieren eines Elements mithilfe von EWS](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_updateews) <br/> |
|Löschen einer E-Mail  <br/> |[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) gefolgt von [DeleteItem](../web-service-reference/deleteitem-operation.md) <br/> |[Löschen eines Elements mithilfe von EWS](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteews) <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Stellvertretungszugriff und EWS in Exchange](delegate-access-and-ews-in-exchange.md)    
- [Hinzufügen und Entfernen von Delegaten mithilfe der EWS in Exchange](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md)    
- [Festlegen von Ordnerberechtigungen für einen anderen Benutzer mithilfe der EWS in Exchange](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md)    
- [Kalender und EWS in Exchange](calendars-and-ews-in-exchange.md)
    

