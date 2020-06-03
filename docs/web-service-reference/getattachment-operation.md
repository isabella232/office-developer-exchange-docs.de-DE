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
description: Der GetAttachment-Vorgang wird verwendet, um vorhandene Anlagen für Elemente im Exchange-Informationsspeicher abzurufen.
ms.openlocfilehash: ac7eafd61c62b077a8d20e5fd8d004924bf06cf1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461289"
---
# <a name="getattachment-operation"></a>GetAttachment-Vorgang

Der GetAttachment-Vorgang wird verwendet, um vorhandene Anlagen für Elemente im Exchange-Informationsspeicher abzurufen.
  
## <a name="getattachment-request-example"></a>GetAttachment-Anforderungs Beispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel der GetAttachment-Anforderung zeigt, wie eine Anlage abgerufen wird.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
xmlns:xsd="http://www.w3.org/2001/XMLSchema"
xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetAttachment xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <AttachmentShape/>
      <AttachmentIds>
        <t:AttachmentId Id="AAAtAEFkbWluaX..."/>
      </AttachmentIds>
    </GetAttachment>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Comments

Mit dem [AttachmentShape](attachmentshape.md) -Element können Sie angeben, welche Anlageninformationen zurückgegeben werden sollen. Ein leeres [AttachmentShape](attachmentshape.md) -Element ist gültig und rendert Ihre Anlagen ohne MIME-Inhalt für Element Anlagen, mit Textkörpertyp und ohne zusätzliche Eigenschaften. 
  
Die [AttachmentIds](attachmentids.md) -Auflistung ermöglicht es Ihnen, einen oder mehrere Anlagen Bezeichner anzugeben, die zurückgegeben werden sollen. Beachten Sie, dass diese vom Typ RequestAttachmentIdType sind, sodass bei allen AttachmentIds, die Sie von **CreateAttachment** erhalten, die Attribute **RootItemId** und **RootItemChangeKey** entfernt werden müssen, bevor Sie an **GetAttachment**übergeben werden.
  
> [!NOTE]
> Die Anlagen-ID und der Änderungsschlüssel wurden verkürzt, um die Lesbarkeit zu erhalten. 
  
### <a name="request-elements"></a>Anfordern von Elementen

In der Anforderung werden folgende Elemente verwendet:
  
- [GetAttachment](getattachment.md)
    
- [AttachmentShape](attachmentshape.md)
    
- [AttachmentIds](attachmentids.md)
    
- [Attachment-Nr (GetAttachment und DeleteAttachment-)](attachmentid-getattachment-and-deleteattachment.md)
    
## <a name="getattachment-response-example"></a>GetAttachment-Antwortbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine GetAttachment-Anforderung. In diesem Beispiel wird eine Dateianlage zurückgegeben.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="662" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <GetAttachmentResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                           xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a>Comments

Die Antwortnachrichten für GetAttachment enthalten immer die vollständige Anlage; Dies bedeutet, dass alle Eigenschaften immer eingeschlossen werden. Für Dateianlagen sind diese Eigenschaften [Name (AttachmentType)](name-attachmenttype.md), [ContentType](contenttype.md), [Inhalts](contentid.md)- [ContentLocation](contentlocation.md)und [Inhalt](content.md). Für Element Anlagen sind diese Eigenschaften [Name (AttachmentType)](name-attachmenttype.md), [ContentType](contenttype.md), [Inhalts](contentid.md)- [ContentLocation](contentlocation.md) und alle Eigenschaften des Elements, als ob die **allproperties** -Form in einem GetItem-Aufruf verwendet wurde. Das [AttachmentShape](attachmentshape.md) -Element, falls vorhanden, ermöglicht einer Consumer-Anwendung, zusätzliche erweiterte Eigenschaften für Element Anlagen anzufordern. 
  
### <a name="successful-response-elements"></a>Erfolgreiche Antwortelemente

In der Antwort werden folgende Elemente verwendet:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [GetAttachmentResponse](getattachmentresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [GetAttachmentResponseMessage](getattachmentresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Anlagen](attachments-ex15websvcsotherref.md)
    
- [FileAttachment](fileattachment.md)
    
- [Attachment-Nr (GetAttachment und DeleteAttachment-)](attachmentid-getattachment-and-deleteattachment.md)
    
- [Name (AttachmentType)](name-attachmenttype.md)
    
- [Content](content.md)
    
## <a name="see-also"></a>Siehe auch



[CreateAttachment-Vorgang](createattachment-operation.md)
  
[DeleteAttachment-Vorgang](deleteattachment-operation.md)

