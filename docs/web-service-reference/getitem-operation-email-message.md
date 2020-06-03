---
title: GetItem-Vorgang (e-Mail-Nachricht)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
api_name:
- GetItem
api_type:
- schema
ms.assetid: e8492e3b-1c8d-4b14-8070-9530f8306edd
description: Der GetItem-Vorgang ermöglicht dem Benutzer den Zugriff auf Informationen über e-Mail-Nachrichten.
localization_priority: Priority
ms.openlocfilehash: f8be01cad3d4c4534f66593cbe8bcee477726972
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459994"
---
# <a name="getitem-operation-email-message"></a>GetItem-Vorgang (e-Mail-Nachricht)

Der GetItem-Vorgang ermöglicht dem Benutzer den Zugriff auf Informationen über e-Mail-Nachrichten.
  
## <a name="using-the-getitem-operation-for-messages"></a>Verwenden des GetItem-Vorgangs für Nachrichten

Die GetItem-Anforderung muss über die folgenden Informationen verfügen:
  
- Das [ItemID](itemid.md) -Element zum Identifizieren der zurückzugebenden Elementinformationen. 
    
- Das [ItemShape](itemshape.md) -Element, um die zurückzugebenden Elementeigenschaften zu identifizieren. 
    
## <a name="getitem-request-example"></a>GetItem-Anforderungs Beispiel

### <a name="description"></a>Beschreibung

Im folgenden Beispiel einer GetItem-Anforderung wird gezeigt, wie auf Informationen zu e-Mail-Nachrichten zugegriffen werden kann.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope
  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
  xmlns:xsd="http://www.w3.org/2001/XMLSchema"
  xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetItem
      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <ItemShape>
        <t:BaseShape>Default</t:BaseShape>
        <t:IncludeMimeContent>true</t:IncludeMimeContent>
      </ItemShape>
      <ItemIds>
        <t:ItemId Id="AAAlAF" ChangeKey="CQAAAB" />
      </ItemIds>
    </GetItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a>Anfordern von Elementen

In der Anforderung werden folgende Elemente verwendet:
  
- [GetItem](getitem.md)
    
- [ItemShape](itemshape.md)
    
- [BaseShape](baseshape.md)
    
- [IncludeMimeContent](includemimecontent.md)
    
- [ItemIds](itemids.md)
    
- [ItemId](itemid.md)
    
## <a name="successful-getitem-e-mail-message-response-example"></a>Erfolgreiches GetItem (e-Mail-Nachricht)-Antwortbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die GetItem-Anforderung.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                     xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                     xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:GetItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Message>
              <t:MimeContent CharacterSet="UTF-8">UmVjZWl</t:MimeContent>
              <t:ItemId Id="AAAlAFVz" ChangeKey="CQAAAB" />
              <t:Subject />
              <t:Sensitivity>Normal</t:Sensitivity>
              <t:Body BodyType="HTML">
                <html dir="ltr">
                  <head>
                    <meta http-equiv="Content-Type" content="text/html; charset=utf-8">
                      <meta content="MSHTML 6.00.3790.2759" name="GENERATOR">
                        <style title="owaParaStyle">P { MARGIN-TOP: 0px; MARGIN-BOTTOM: 0px } </style>
                      </head>
                  <body ocsi="x">
                    <div dir="ltr">
                      <font face="Tahoma" color="#000000" size="2"></font>&amp;nbsp;
                    </div>
                  </body>
                </html>
              </t:Body>
              <t:Size>881</t:Size>
              <t:DateTimeSent>2006-10-28T01:37:06Z</t:DateTimeSent>
              <t:DateTimeCreated>2006-10-28T01:37:06Z</t:DateTimeCreated>
              <t:ResponseObjects>
                <t:ReplyToItem />
                <t:ReplyAllToItem />
                <t:ForwardItem />
              </t:ResponseObjects>
              <t:HasAttachments>false</t:HasAttachments>
              <t:ToRecipients>
                <t:Mailbox>
                  <t:Name>User1</t:Name>
                  <t:EmailAddress>User1@example.com</t:EmailAddress>
                  <t:RoutingType>SMTP</t:RoutingType>
                </t:Mailbox>
              </t:ToRecipients>
              <t:IsReadReceiptRequested>false</t:IsReadReceiptRequested>
              <t:IsDeliveryReceiptRequested>false</t:IsDeliveryReceiptRequested>
              <t:From>
                <t:Mailbox>
                  <t:Name>User2</t:Name>
                  <t:EmailAddress>User2@example.com</t:EmailAddress>
                  <t:RoutingType>SMTP</t:RoutingType>
                </t:Mailbox>
              </t:From>
              <t:IsRead>false</t:IsRead>
            </t:Message>
          </m:Items>
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </GetItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Comments

Die MIME-Inhalte, Ordner und Element-IDs wurden verkürzt, um die Lesbarkeit zu erhalten.
  
### <a name="successful-response-elements"></a>Erfolgreiche Antwortelemente

In der Antwort werden folgende Elemente verwendet:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [GetItemResponse](getitemresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [GetItemResponseMessage](getitemresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Elemente](items.md)
    
- [Message](message-ex15websvcsotherref.md)
    
- [MimeContent](mimecontent.md)
    
- [ItemId](itemid.md)
    
- [Betreff](subject.md)
    
- [Sensitivity](sensitivity.md)
    
- [Body](body.md)
    
- [Größe](size.md)
    
- [DateTimeSent](datetimesent.md)
    
- [DateTimeCreated](datetimecreated.md)
    
- [ResponseObjects](responseobjects.md)
    
- [ReplyToItem](replytoitem.md)
    
- [ReplyAllToItem](replyalltoitem.md)
    
- [ForwardItem](forwarditem.md)
    
- [HasAttachments](hasattachments.md)
    
- [ToRecipients](torecipients.md)
    
- [Postfach](mailbox.md)
    
- [Name (EmailAddressType)](name-emailaddresstype.md)
    
- [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md)
    
- [Routingtype (e-mailemailtype)](routingtype-emailaddresstype.md)
    
- [IsReadReceiptRequested](isreadreceiptrequested.md)
    
- [IsDeliveryReceiptRequested](isdeliveryreceiptrequested.md)
    
- [From](from.md)
    
- [IsRead](isread.md)
    
## <a name="getitem-e-mail-message-error-response-example"></a>Fehlerantwort-Beispiel für GetItem (e-Mail-Nachricht)

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine Fehlerantwort auf eine GetItem-Anforderung. Der Fehler wurde durch einen Versuch verursacht, eine ungültige zusätzliche Eigenschaft abzurufen.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                     xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                     xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:GetItemResponseMessage ResponseClass="Error">
          <m:MessageText>Property is not valid for this object type.</m:MessageText>
          <m:ResponseCode>ErrorInvalidPropertyRequest</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:MessageXml>
            <t:FieldURI FieldURI="meeting:AssociatedCalendarItemId" />
          </m:MessageXml>
          <m:Items />
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </GetItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a>Fehlerantwortelemente

Folgende Elemente werden in der Fehlerantwort verwendet:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [GetItemResponse](getitemresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [GetItemResponseMessage](getitemresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
- [Messagexml verwendet](messagexml.md)
    
- [FieldURI](fielduri.md)
    
## <a name="see-also"></a>Siehe auch



[GetItem-Vorgang](getitem-operation.md)

