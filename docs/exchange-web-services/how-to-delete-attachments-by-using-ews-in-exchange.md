---
title: Löschen von Anlagen mithilfe von EWS in Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 71871ac7-ee1a-4f93-9e81-77f312d432f4
description: Erfahren Sie, wie Sie Anlagen aus Elementen mithilfe der verwalteten EWS-API oder EWS in Exchange löschen.
ms.openlocfilehash: bc9b8bbf5833cfdb44f9ca4e8387681473fad3c3
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521151"
---
# <a name="delete-attachments-by-using-ews-in-exchange"></a>Löschen von Anlagen mithilfe von EWS in Exchange

Erfahren Sie, wie Sie Anlagen aus Elementen mithilfe der verwalteten EWS-API oder EWS in Exchange löschen.
  
Sie haben eine Reihe von Optionen, wenn es darum geht, Datei- und Elementanlagen aus Elementen mithilfe der verwalteten EWS-API zu löschen. Sie können alle Anlagen aus der Nachricht löschen, mit einem Dateinamen löschen oder nach Position in der Auflistung löschen. Für jede dieser Optionen gibt es eine [AttachmentCollection-Methode.](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.attachmentcollection%28v=exchg.80%29.aspx) 
  
Im Gegensatz dazu ist bei EWS unabhängig davon, ob Sie alle Anlagen aus einem Element oder nur aus einem Element löschen, die Reihenfolge der Vorgänge identisch. Im Gegensatz zur verwalteten EWS-API enthält EWS keine separaten Vorgänge, die basierend auf dem Namen oder der Position im Anlagenarray gelöscht werden sollen.
  
**Tabelle 1. Verwaltete EWS-API-Methoden und EWS-Vorgänge zum Löschen von Anlagen**

|**Aufgabe**|**EWS Managed API-Methode**|**EWS-Vorgang**|
|:-----|:-----|:-----|
|Löscht alle Anlagen aus einem Element.  <br/> |[Item.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx), gefolgt von [AttachmentCollection.Clear](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.attachmentcollection.clear%28v=exchg.80%29.aspx), gefolgt von [EmailMessage.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx) <br/> |[GetItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) gefolgt von [DeleteAttachment](https://msdn.microsoft.com/library/43d0c1cb-92ca-4399-9b3a-acb2b5c22624%28Office.15%29.aspx) <br/> |
|Löschen einer Anlage aus einem Element anhand des Namens.  <br/> |[Item.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx), gefolgt von [AttachmentCollection.Remove](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.attachmentcollection.remove%28v=exchg.80%29.aspx), gefolgt von [EmailMessage.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx) <br/> |[GetItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) gefolgt von [DeleteAttachment](https://msdn.microsoft.com/library/43d0c1cb-92ca-4399-9b3a-acb2b5c22624%28Office.15%29.aspx) <br/> |
|Dient zum Löschen einer Anlage aus einem Element nach Position in der Auflistung.  <br/> |[Item.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx), gefolgt von [AttachmentCollection.RemoveAt](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.attachmentcollection.removeat%28v=exchg.80%29.aspx), gefolgt von [EmailMessage.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx) <br/> |[GetItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) gefolgt von [DeleteAttachment](https://msdn.microsoft.com/library/43d0c1cb-92ca-4399-9b3a-acb2b5c22624%28Office.15%29.aspx) <br/> |
   
## <a name="delete-all-attachments-from-an-email-by-using-the-ews-managed-api"></a>Löschen aller Anlagen aus einer E-Mail mithilfe der verwalteten EWS-API
<a name="bk_deleteattachewsma"> </a>

Das folgende Codebeispiel zeigt, wie Alle Anlagen aus einer E-Mail gelöscht werden:
  
1. Verwenden der [EmailMessage.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) -Methode, um eine Bindung an eine vorhandene E-Mail-Nachricht zu erstellen und die Sammlung von [Anlagen](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.attachments%28v=exchg.80%29.aspx)abzurufen.
    
2. Verwenden der [AttachmentCollection.Clear-Methode,](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.attachmentcollection.clear%28v=exchg.80%29.aspx) um alle Anlagen aus der E-Mail zu löschen. 
    
3. Verwenden der [EmailMessage.Update-Methode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx) zum Speichern der Änderungen. 
    
In diesem Beispiel wird davon ausgegangen, dass es sich bei dem **Dienst** um ein gültiges [ExchangeService-Objekt](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) handelt. **ItemId** ist die [ItemId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemid%28v=exchg.80%29.aspx) der Nachricht, aus der Anlagen gelöscht werden, und dass der Benutzer bei einem Exchange Server authentifiziert wurde. 
  
```cs
public static void DeleteAllAttachments(ExchangeService service, ItemId itemId)
{
    // Bind to an existing message by using its item ID and requesting its attachments collection.
    // This method results in a GetItem call to EWS.
    EmailMessage message = EmailMessage.Bind(service, itemId, new PropertySet(ItemSchema.Attachments));
    // Delete all attachments from the message.
    message.Attachments.Clear();
    // Save the updated message.
    // This method results in an DeleteAttachment call to EWS.
    message.Update(ConflictResolutionMode.AlwaysOverwrite);
}
```

## <a name="delete-an-attachment-by-name-from-an-email-by-using-the-ews-managed-api"></a>Löschen einer Anlage anhand des Namens aus einer E-Mail mithilfe der verwalteten EWS-API
<a name="bk_deleteattachewsma"> </a>

Das folgende Codebeispiel zeigt, wie eine Anlage anhand des Namens gelöscht wird:
  
1. Verwenden der [EmailMessage.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) -Methode, um eine Bindung an eine vorhandene E-Mail-Nachricht zu erstellen und die Sammlung von [Anlagen](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.attachments%28v=exchg.80%29.aspx)abzurufen.
    
2. Verwenden der [AttachmentCollection.Remove-Methode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.attachmentcollection.remove%28v=exchg.80%29.aspx) zum Löschen einer Anlage mit dem Namen FileAttachment.txt. 
    
3. Verwenden der [EmailMessage.Update-Methode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx) zum Speichern der Änderungen. 
    
In diesem Beispiel wird davon ausgegangen, dass es sich bei dem **Dienst** um ein gültiges [ExchangeService-Objekt](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) handelt. **ItemId** ist die [ItemId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemid%28v=exchg.80%29.aspx) der Nachricht, aus der die Anlage gelöscht wird, und dass der Benutzer bei einem Exchange Server authentifiziert wurde. 
  
```cs
public static void DeleteNamedAttachments(ExchangeService service, ItemId itemId)
{
    // Bind to an existing message by using its item ID and requesting its attachments collection.
    // This method results in a GetItem call to EWS.
    EmailMessage message = EmailMessage.Bind(service, itemId, new PropertySet(ItemSchema.Attachments));
    // Iterate through the attachments collection and delete the attachment named "FileAttachment.txt," if it exists.
    foreach (Attachment attachment in message.Attachments)
    {
        if (attachment.Name == "FileAttachment.txt")
        {
            message.Attachments.Remove(attachment);
            break;
        }
    }
    // Save the updated message.
    // This method results in an DeleteAttachment call to EWS.
    message.Update(ConflictResolutionMode.AlwaysOverwrite);
}
```

## <a name="delete-attachments-by-position-by-using-the-ews-managed-api"></a>Löschen von Anlagen nach Position mithilfe der verwalteten EWS-API
<a name="bk_deleteattachewsma"> </a>

Das folgende Codebeispiel zeigt, wie eine Anlage nach Position gelöscht wird:
  
1. Verwenden der [EmailMessage.Bind-Methode,](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) um eine Bindung an eine vorhandene E-Mail-Nachricht zu erstellen und die Sammlung von [Anlagen](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.attachments%28v=exchg.80%29.aspx) und die [EmailMessage.HasAttachments-Eigenschaft](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.hasattachments%28v=exchg.80%29.aspx) abzurufen. 
    
2. Verwenden der [AttachmentCollection.Remove](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.attachmentcollection.remove%28v=exchg.80%29.aspx) -Methode, um die erste Anlage in der Auflistung zu löschen. 
    
3. Verwenden der [EmailMessage.Update-Methode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx) zum Speichern der Änderungen. 
    
In diesem Beispiel wird davon ausgegangen, dass es sich bei dem **Dienst** um ein gültiges [ExchangeService-Objekt](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) handelt. **ItemId** ist die [ItemId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemid%28v=exchg.80%29.aspx) der Nachricht, aus der die Anlage gelöscht wird, und dass der Benutzer bei einem Exchange Server authentifiziert wurde. 
  
```cs
public static void DeleteAttachmentByPosition(ExchangeService service, ItemId itemId)
{
    // Bind to an existing message by using its item ID and requesting the HasAttachments property and the attachments collection.
    // This method results in a GetItem call to EWS.
    EmailMessage message = EmailMessage.Bind(service, itemId, new PropertySet(EmailMessageSchema.HasAttachments, ItemSchema.Attachments));
    // Remove attachments using the zero-based index position of the attachment in the attachments collection.
    if (message.HasAttachments)
    {
        message.Attachments.RemoveAt(0);
    }
    // Save the updated message.
    // This method results in an DeleteAttachment call to EWS.
    message.Update(ConflictResolutionMode.AlwaysOverwrite);
}
```

## <a name="delete-attachments-from-an-item-by-using-ews"></a>Löschen von Anlagen aus einem Element mithilfe von EWS
<a name="bk_deleteattachewsma"> </a>

Um Anlagen mithilfe von EWS zu löschen, müssen Sie zuerst die Nachricht und die Anlagensammlung abrufen, um die [AttachmentId (GetAttachment und DeleteAttachment)](https://msdn.microsoft.com/library/4bea1cb5-0a0f-4e14-9b09-f91af8cf9899%28Office.15%29.aspx) der zu löschenden Anlage zu bestimmen. Wenn Sie mindestens einen **AttachmentId-Wert** löschen müssen, rufen Sie den [DeleteAttachment-Vorgang](https://msdn.microsoft.com/library/4d48e595-b98c-48e7-bbeb-cacf91d12a78%28Office.15%29.aspx) auf, um die angegebenen Anlagen aus der Nachricht zu entfernen. 
  
Im folgenden Codebeispiel wird veranschaulicht, wie der [GetItem](https://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx)-Vorgang zum Abrufen einer E-Mail und der Anlagenauflistung in der Nachricht verwendet wird. Dies ist auch die erste XML-Anforderung, die die verwaltete EWS-API sendet, wenn Sie die verwaltete EWS-API verwenden, um [alle Anlagen aus einer E-Mail](#bk_deleteattachewsma)zu löschen. Die Werte einiger Attribute wurden zur besseren Lesbarkeit gekürzt.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Central Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:GetItem>
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Attachments" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:ItemIds>
        <t:ItemId Id="uqE1AAA=" />
      </m:ItemIds>
    </m:GetItem>
  </soap:Body>
</soap:Envelope>
```

Der Server antwortet auf die **GetItem**-Anforderung mit einer [GetItemResponse](https://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx)-Nachricht, die einen [ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx)-Wert **NoError** umfasst, der angibt, dass die E-Mail erfolgreich abgerufen wurde, sowie [AttachmentId](https://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx)-Werte der vorhandenen Anlagen. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="939"
                         MinorBuildNumber="12"
                         Version="V2_11"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Message>
              <t:ItemId Id="uqE1AAA="
                        ChangeKey="CQAAABYAAAAFI5DJmZv+TLtyLOLIF1S5AAAXulcd" />
              <t:Attachments>
                <t:FileAttachment>
                  <t:AttachmentId Id="IpHLObE=" />
                  <t:Name>FileAttachment.txt</t:Name>
                </t:FileAttachment>
                <t:FileAttachment>
                  <t:AttachmentId Id="QuHSSmY=" />
                  <t:Name>SecondAttachment.txt</t:Name>
                </t:FileAttachment>
                <t:FileAttachment>
                  <t:AttachmentId Id="qf2KoPo=" />
                  <t:Name>ThirdAttachment.jpg</t:Name>
                </t:FileAttachment>
                <t:FileAttachment>
                  <t:AttachmentId Id="NFQMnMc=" />
                  <t:Name>FourthAttachment.txt</t:Name>
                </t:FileAttachment>
                <t:ItemAttachment>
                  <t:AttachmentId Id="jJvbLXQ=" />
                  <t:Name>Attached Message Item</t:Name>
                </t:ItemAttachment>
              </t:Attachments>
            </t:Message>
          </m:Items>
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </m:GetItemResponse>
  </s:Body>
</s:Envelope>
```

Nachdem Sie bestimmt haben, welche Anlage gelöscht werden soll, rufen Sie den [DeleteAttachment-Vorgang](https://msdn.microsoft.com/library/4d48e595-b98c-48e7-bbeb-cacf91d12a78%28Office.15%29.aspx) auf, und fügen Sie die **AttachmentId-Werte** der zu löschenden Anlagen ein. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Central Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:DeleteAttachment>
      <m:AttachmentIds>
        <t:AttachmentId Id="IpHLObE=" />
        <t:AttachmentId Id="QuHSSmY=" />
        <t:AttachmentId Id="qf2KoPo=" />
        <t:AttachmentId Id="NFQMnMc=" />
        <t:AttachmentId Id="jJvbLXQ=" />
      </m:AttachmentIds>
    </m:DeleteAttachment>
  </soap:Body>
</soap:Envelope>
```

Der Server antwortet auf die **DeleteAttachment-Anforderung** mit einer [DeleteAttachmentResponse-Nachricht,](https://msdn.microsoft.com/library/24099a88-4ab6-4bf3-8ed5-efec8e07b9b9%28Office.15%29.aspx) die den [ResponseCode-Wert](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx) **NoError** für jede [DeleteAttachmentResponseMessage](https://msdn.microsoft.com/library/1edb085f-1674-48e5-8ec3-42351adeac7d%28Office.15%29.aspx)enthält, was angibt, dass jede Anlage erfolgreich gelöscht wurde. Die Werte einiger Attribute wurden zur besseren Lesbarkeit gekürzt.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="939"
                         MinorBuildNumber="12"
                         Version="V2_11"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:DeleteAttachmentResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                                xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:DeleteAttachmentResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootItemId RootItemId="uqE1AAA=" RootItemChangeKey="AAAXulck" />
        </m:DeleteAttachmentResponseMessage>
        <m:DeleteAttachmentResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootItemId RootItemId="uqE1AAA=" RootItemChangeKey="AAAXulck" />
        </m:DeleteAttachmentResponseMessage>
        <m:DeleteAttachmentResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootItemId RootItemId="uqE1AAA=" RootItemChangeKey="AAAXulck" />
        </m:DeleteAttachmentResponseMessage>
        <m:DeleteAttachmentResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootItemId RootItemId="uqE1AAA=" RootItemChangeKey="AAAXulck" />
        </m:DeleteAttachmentResponseMessage>
        <m:DeleteAttachmentResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootItemId RootItemId="uqE1AAA=" RootItemChangeKey="AAAXulck" />
        </m:DeleteAttachmentResponseMessage>
      </m:ResponseMessages>
    </m:DeleteAttachmentResponse>
  </s:Body>
</s:Envelope>
```

## <a name="see-also"></a>Siehe auch


- [Anlagen und EWS in Exchange](attachments-and-ews-in-exchange.md)
    
- [Hinzufügen von Anlagen mithilfe von EWS in Exchange](how-to-add-attachments-by-using-ews-in-exchange.md)
    
- [Abrufen von Anlagen mithilfe von EWS in Exchange](how-to-get-attachments-by-using-ews-in-exchange.md)
    

