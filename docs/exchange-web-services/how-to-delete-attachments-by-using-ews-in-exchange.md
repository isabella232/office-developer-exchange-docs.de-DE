---
title: Löschen von Anlagen mithilfe der EWS in Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 71871ac7-ee1a-4f93-9e81-77f312d432f4
description: Erfahren Sie, wie Anlagen aus Elementen löschen, indem Sie die EWS Managed API oder EWS in Exchange.
ms.openlocfilehash: 458331f81493283efc20d24c7e2bebe0e74bbdbd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756888"
---
# <a name="delete-attachments-by-using-ews-in-exchange"></a>Löschen von Anlagen mithilfe der EWS in Exchange

Erfahren Sie, wie Anlagen aus Elementen löschen, indem Sie die EWS Managed API oder EWS in Exchange.
  
Wenn es zum Löschen der Datei und Anlagen aus Elementen geht mithilfe der EWS Managed API, stehen Ihnen eine Reihe von Optionen. Sie können Löschen aller Anlagen aus der Nachricht, löschen, indem Sie einen Dateinamen ein, oder löschen, indem Sie Position in der Auflistung. Für jede dieser Optionen gibt es eine [AttachmentCollection](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.attachmentcollection%28v=exchg.80%29.aspx) -Methode. 
  
Im Gegensatz dazu entspricht unabhängig davon, ob Sie alle Anlagen aus einem Element oder nur ein einziges, löschen möchten, dem mit Exchange-Webdienste, die Reihenfolge der Vorgänge. Im Gegensatz zu EWS Managed API enthält EWS getrennte Vorgänge zu löschenden keinen basierend auf den Namen oder die Position im Array Anlagen.
  
**In Tabelle 1. EWS Managed API-Methoden und EWS-Vorgänge zum Löschen von Anlagen**

|**Aufgabe**|**EWS Managed API-Methode**|**EWS-Vorgang**|
|:-----|:-----|:-----|
|Löschen Sie alle Anlagen aus einem Element.  <br/> |[Item.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx), gefolgt von [AttachmentCollection.Clear](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.attachmentcollection.clear%28v=exchg.80%29.aspx), gefolgt von [EmailMessage.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx) <br/> |[GetItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) gefolgt von [DeleteAttachment](http://msdn.microsoft.com/library/43d0c1cb-92ca-4399-9b3a-acb2b5c22624%28Office.15%29.aspx) <br/> |
|Löschen einer Anlage aus einem Element nach Namen.  <br/> |[Item.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx), gefolgt von [AttachmentCollection.Remove](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.attachmentcollection.remove%28v=exchg.80%29.aspx), gefolgt von [EmailMessage.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx) <br/> |[GetItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) gefolgt von [DeleteAttachment](http://msdn.microsoft.com/library/43d0c1cb-92ca-4399-9b3a-acb2b5c22624%28Office.15%29.aspx) <br/> |
|Löschen einer Anlage aus einem Element nach Position in der Auflistung.  <br/> |[Item.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx), gefolgt von [AttachmentCollection.RemoveAt](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.attachmentcollection.removeat%28v=exchg.80%29.aspx), gefolgt von [EmailMessage.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx) <br/> |[GetItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) gefolgt von [DeleteAttachment](http://msdn.microsoft.com/library/43d0c1cb-92ca-4399-9b3a-acb2b5c22624%28Office.15%29.aspx) <br/> |
   
## <a name="delete-all-attachments-from-an-email-by-using-the-ews-managed-api"></a>Löschen Sie alle Anlagen aus einer e-Mail mithilfe der EWS Managed API
<a name="bk_deleteattachewsma"> </a>

Im folgenden Codebeispiel wird veranschaulicht, wie alle Anlagen aus einer e-Mail durch Löschen:
  
1. Mithilfe der Methode [EmailMessage.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) Binden an eine vorhandene e-Mail-Nachricht und Abrufen der Auflistung von [Anlagen](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.attachments%28v=exchg.80%29.aspx).
    
2. Verwenden die [AttachmentCollection.Clear](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.attachmentcollection.clear%28v=exchg.80%29.aspx) -Methode zum Löschen aller Anlagen aus der e-Mail. 
    
3. Verwenden die [EmailMessage.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx) -Methode, um die Änderungen zu speichern. 
    
In diesem Beispiel wird davon ausgegangen, dass **Service** ist ein gültiges [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objekt, **ItemId** ist die [ItemId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemid%28v=exchg.80%29.aspx) der Nachricht aus der Anlagen gelöscht werden, und der Benutzer an einen Exchange-Server authentifiziert wurde. 
  
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

## <a name="delete-an-attachment-by-name-from-an-email-by-using-the-ews-managed-api"></a>Löschen einer Anlage nach Namen aus einer e-Mail mithilfe der EWS Managed API
<a name="bk_deleteattachewsma"> </a>

Das folgende Beispiel zeigt für Code Löschen einer Anlage wie namentlich durch:
  
1. Mithilfe der Methode [EmailMessage.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) Binden an eine vorhandene e-Mail-Nachricht und Abrufen der Auflistung von [Anlagen](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.attachments%28v=exchg.80%29.aspx).
    
2. Verwenden die [AttachmentCollection.Remove](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.attachmentcollection.remove%28v=exchg.80%29.aspx) -Methode zum Löschen einer Anlage, die mit dem Namen FileAttachment.txt. 
    
3. Verwenden die [EmailMessage.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx) -Methode, um die Änderungen zu speichern. 
    
In diesem Beispiel wird davon ausgegangen, dass **Service** ist ein gültiges [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objekt, **ItemId** ist die [ItemId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemid%28v=exchg.80%29.aspx) der Nachricht aus der Anlage gelöscht werden soll, und der Benutzer an einen Exchange-Server authentifiziert wurde. 
  
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

## <a name="delete-attachments-by-position-by-using-the-ews-managed-api"></a>Löschen von Anlagen mit einem Position mithilfe der EWS Managed API
<a name="bk_deleteattachewsma"> </a>

Im folgenden Codebeispiel wird veranschaulicht, wie eine Anlage nach Position durch Löschen:
  
1. Mithilfe der Methode [EmailMessage.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) Binden an eine vorhandene e-Mail-Nachricht und Abrufen der Auflistung von [Anlagen](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.attachments%28v=exchg.80%29.aspx) und die [EmailMessage.HasAttachments](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.hasattachments%28v=exchg.80%29.aspx) -Eigenschaft. 
    
2. Verwenden die [AttachmentCollection.Remove](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.attachmentcollection.remove%28v=exchg.80%29.aspx) -Methode die erste Anlage in der Auflistung zu löschen. 
    
3. Verwenden die [EmailMessage.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx) -Methode, um die Änderungen zu speichern. 
    
In diesem Beispiel wird davon ausgegangen, dass **Service** ist ein gültiges [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objekt, **ItemId** ist die [ItemId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemid%28v=exchg.80%29.aspx) der Nachricht aus der Anlage gelöscht werden soll, und der Benutzer an einen Exchange-Server authentifiziert wurde. 
  
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

## <a name="delete-attachments-from-an-item-by-using-ews"></a>Löschen von Anlagen aus einem Element mithilfe der Exchange-Webdienste
<a name="bk_deleteattachewsma"> </a>

Zum Löschen von Anlagen mithilfe der Exchange-Webdienste, müssen Sie zuerst die Nachricht und die Anlage-Auflistung zum Bestimmen der [AttachmentId (GetAttachment und DeleteAttachment)](http://msdn.microsoft.com/library/4bea1cb5-0a0f-4e14-9b09-f91af8cf9899%28Office.15%29.aspx) der Anlage zu löschenden abrufen. Nachdem Sie einen oder mehrere **AttachmentId** Werte zu löschenden haben, rufen Sie den Vorgang [DeleteAttachment](http://msdn.microsoft.com/library/4d48e595-b98c-48e7-bbeb-cacf91d12a78%28Office.15%29.aspx) , um die angegebenen Anlagen aus der Nachricht zu entfernen. 
  
Im folgenden Codebeispiel wird veranschaulicht, wie der [GetItem](http://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx)-Vorgang zum Abrufen einer E-Mail und der Anlagenauflistung in der Nachricht verwendet wird. Dies ist auch der erste XML-Anforderung, die die EWS Managed API sendet, wenn Sie die EWS Managed API zum [Löschen aller Anlagen aus einer e-Mail](#bk_deleteattachewsma)verwenden. Die Werte einiger Attribute wurden zur besseren Lesbarkeit gekürzt.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

Der Server antwortet auf die **GetItem**-Anforderung mit einer [GetItemResponse](http://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx)-Nachricht, die einen [ResponseCode](http://msdn.microsoft.com/en-us/library/aa580757%28v=exchg.150%29.aspx)-Wert **NoError** umfasst, der angibt, dass die E-Mail erfolgreich abgerufen wurde, sowie [AttachmentId](http://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx)-Werte der vorhandenen Anlagen. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="939"
                         MinorBuildNumber="12"
                         Version="V2_11"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

Nach dem bestimmen Sie, welche Anlage zu löschen, rufen Sie den Vorgang [DeleteAttachment](http://msdn.microsoft.com/library/4d48e595-b98c-48e7-bbeb-cacf91d12a78%28Office.15%29.aspx) und gehören zu den Werten **AttachmentId** Anlagen löschen. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

Der Server antwortet auf die Anforderung **DeleteAttachment** mit einer [DeleteAttachmentResponse](http://msdn.microsoft.com/library/24099a88-4ab6-4bf3-8ed5-efec8e07b9b9%28Office.15%29.aspx) -Nachricht, die [ResponseCode](http://msdn.microsoft.com/en-us/library/aa580757%28v=exchg.150%29.aspx) Wert **NoError** für jede [DeleteAttachmentResponseMessage](http://msdn.microsoft.com/library/1edb085f-1674-48e5-8ec3-42351adeac7d%28Office.15%29.aspx)enthält, die jede Anlage wurde gelöscht. Die Werte einiger Attribute wurden zur besseren Lesbarkeit gekürzt.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="939"
                         MinorBuildNumber="12"
                         Version="V2_11"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:DeleteAttachmentResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                                xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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


- [Attachments and EWS in Exchange](attachments-and-ews-in-exchange.md)
    
- [Hinzufügen von Anlagen im Exchange mithilfe der Exchange-Webdienste](how-to-add-attachments-by-using-ews-in-exchange.md)
    
- [Abrufen von Anlagen im Exchange mithilfe der Exchange-Webdienste](how-to-get-attachments-by-using-ews-in-exchange.md)
    

