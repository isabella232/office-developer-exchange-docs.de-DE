---
title: GetAttachment-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetAttachment
api_type:
- schema
ms.assetid: 24d10a15-b942-415e-9024-a6375708f326
description: Der Vorgang GetAttachment wird verwendet, um vorhandene Anlagen für Elemente im Exchange-Speicher abzurufen.
ms.openlocfilehash: c260033208bf49c60463c09041d8ffcc52a8f5c2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758585"
---
# <a name="getattachment-operation"></a>GetAttachment-Vorgang

Der Vorgang GetAttachment wird verwendet, um vorhandene Anlagen für Elemente im Exchange-Speicher abzurufen.
  
## <a name="getattachment-request-example"></a>GetAttachment anforderungsbeispiel

### <a name="description"></a>Beschreibung

Im folgenden Beispiel wird der GetAttachment Anforderung veranschaulicht, wie eine Anlage abgerufen.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
xmlns:xsd="http://www.w3.org/2001/XMLSchema"
xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetAttachment xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <AttachmentShape/>
      <AttachmentIds>
        <t:AttachmentId Id="AAAtAEFkbWluaX..."/>
      </AttachmentIds>
    </GetAttachment>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Kommentare

Das [AttachmentShape](attachmentshape.md) -Element können Sie angeben, welche Informationen über die Anlage zurückgegeben werden sollen. Ein leeres Element [AttachmentShape](attachmentshape.md) ist gültig und Ihre Anlagen ohne MIME-Inhaltstyp für das elementanlagen, mit dem Text Texttyp und ohne zusätzlichen Eigenschaften rendert. 
  
Die [AttachmentIds](attachmentids.md) -Auflistung können Sie eine oder mehrere Anlagen Bezeichner zurückzugebenden angeben. Beachten Sie, dass diese vom Typ RequestAttachmentIdType, damit alle AttachmentIds, die Sie aus **CreateAttachment** erhalten die Attribute **RootItemId** und **RootItemChangeKey** verfügen müssen vor der Übergabe an **GetAttachment**entfernt.
  
> [!NOTE]
> Die Anlage-ID und Key ändern wurden gekürzt, um die Lesbarkeit zu erhalten. 
  
### <a name="request-elements"></a>Anfordern von Elementen

In der Anforderung werden folgende Elemente verwendet:
  
- [GetAttachment](getattachment.md)
    
- [AttachmentShape](attachmentshape.md)
    
- [AttachmentIds](attachmentids.md)
    
- [AttachmentId (GetAttachment und DeleteAttachment)](attachmentid-getattachment-and-deleteattachment.md)
    
## <a name="getattachment-response-example"></a>GetAttachment antwortbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine Anforderung GetAttachment. Dieses Beispiel gibt eine Dateianlage.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="662" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <GetAttachmentResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                           xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:GetAttachmentResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Attachments>
            <t:FileAttachment>
              <t:AttachmentId Id="AAAtAEFkbWluaX..."/>
              <t:Name>SomeFile</t:Name>
              <t:Content>AQIDBAU=</t:Content>
            </t:FileAttachment>
          </m:Attachments>
        </m:GetAttachmentResponseMessage>
      </m:ResponseMessages>
    </GetAttachmentResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Kommentare

Die Antwortnachrichten für GetAttachment werden immer die vollständige Anlage enthalten. d. h., werden alle Eigenschaften immer eingeschlossen. Für Dateianlagen sind diese Eigenschaften [Name (AttachmentType)](name-attachmenttype.md), [ContentType](contenttype.md), [ContentId](contentid.md), [ContentLocation](contentlocation.md)und [Content](content.md). Für Anlagen, diese Eigenschaften sind [Name (AttachmentType)](name-attachmenttype.md), [ContentType](contenttype.md), [ContentId](contentid.md), [ContentLocation](contentlocation.md) und alle Eigenschaften des Elements, als ob die Form **AllProperties** verwendet wurden im Gespräch GetItem. Das [AttachmentShape](attachmentshape.md) -Element, kann falls vorhanden, so fordern Sie zusätzliche erweiterte Eigenschaften für das elementanlagen an eine Consumeranwendung ansetzt. 
  
### <a name="successful-response-elements"></a>Elemente einer erfolgreichen Antwort

In der Antwort werden folgende Elemente verwendet:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [GetAttachmentResponse](getattachmentresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [GetAttachmentResponseMessage](getattachmentresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Anlagen](attachments-ex15websvcsotherref.md)
    
- [FileAttachment](fileattachment.md)
    
- [AttachmentId (GetAttachment und DeleteAttachment)](attachmentid-getattachment-and-deleteattachment.md)
    
- [Name ("AttachmentType")](name-attachmenttype.md)
    
- [Inhalt](content.md)
    
## <a name="see-also"></a>Siehe auch



[CreateAttachment-Vorgang](createattachment-operation.md)
  
[DeleteAttachment-Vorgang](deleteattachment-operation.md)

