---
title: GetAttachment-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- GetAttachment
api_type:
- schema
ms.assetid: 24d10a15-b942-415e-9024-a6375708f326
description: Der GetAttachment-Vorgang wird verwendet, um vorhandene Anlagen für Elemente im Exchange Speicher abzurufen.
ms.openlocfilehash: 44a9e1988deb513039f7700e11c645c366641519
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59509937"
---
# <a name="getattachment-operation"></a>GetAttachment-Vorgang

Der GetAttachment-Vorgang wird verwendet, um vorhandene Anlagen für Elemente im Exchange Speicher abzurufen.
  
## <a name="getattachment-request-example"></a>GetAttachment-Anforderungsbeispiel

### <a name="description"></a>Beschreibung

Im folgenden Beispiel der GetAttachment-Anforderung wird gezeigt, wie eine Anlage abgerufen wird.
  
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

Mit dem [AttachmentShape-Element](attachmentshape.md) können Sie angeben, welche Anlageninformationen zurückgegeben werden sollen. Ein leeres [AttachmentShape-Element](attachmentshape.md) ist gültig und rendert Ihre Anlagen ohne MIME-Inhalt für Elementanlagen, mit einem Textkörpertyp und ohne zusätzliche Eigenschaften. 
  
Mit [der AttachmentIds-Auflistung](attachmentids.md) können Sie einen oder mehrere Anlagenbezeichner angeben, die zurückgegeben werden sollen. Beachten Sie, dass diese vom Typ RequestAttachmentIdType sind, sodass alle AttachmentIds, die Sie von **CreateAttachment** erhalten, die **Attribute RootItemId** und **RootItemChangeKey** entfernen müssen, bevor sie an **GetAttachment** übergeben werden.
  
> [!NOTE]
> Der Anlagenbezeichner und der Änderungsschlüssel wurden gekürzt, um die Lesbarkeit zu gewährleisten. 
  
### <a name="request-elements"></a>Anfordern von Elementen

In der Anforderung werden folgende Elemente verwendet:
  
- [GetAttachment](getattachment.md)
    
- [AttachmentShape](attachmentshape.md)
    
- [AttachmentIds](attachmentids.md)
    
- [AttachmentId (GetAttachment und DeleteAttachment)](attachmentid-getattachment-and-deleteattachment.md)
    
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

Die Antwortnachrichten für GetAttachment enthalten immer die vollständige Anlage. d. h., alle Eigenschaften werden immer eingeschlossen. Bei Dateianlagen sind diese Eigenschaften [Name (AttachmentType),](name-attachmenttype.md) [ContentType](contenttype.md), [ContentId](contentid.md), [ContentLocation](contentlocation.md)und [Content](content.md). Bei Elementanlagen sind diese Eigenschaften [Name (AttachmentType),](name-attachmenttype.md) [ContentType](contenttype.md), [ContentId](contentid.md), [ContentLocation](contentlocation.md) und alle Eigenschaften des Elements, als ob das **AllProperties-Shape** in einem GetItem-Aufruf verwendet worden wäre. Wenn das [AttachmentShape-Element](attachmentshape.md) vorhanden ist, kann eine Consumeranwendung zusätzliche erweiterte Eigenschaften für Elementanlagen anfordern. 
  
### <a name="successful-response-elements"></a>Erfolgreiche Antwortelemente

In der Antwort werden folgende Elemente verwendet:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [GetAttachmentResponse](getattachmentresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [GetAttachmentResponseMessage](getattachmentresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Anhänge](attachments-ex15websvcsotherref.md)
    
- [FileAttachment](fileattachment.md)
    
- [AttachmentId (GetAttachment und DeleteAttachment)](attachmentid-getattachment-and-deleteattachment.md)
    
- [Name (AttachmentType)](name-attachmenttype.md)
    
- [Inhalt](content.md)
    
## <a name="see-also"></a>Siehe auch



[CreateAttachment-Vorgang](createattachment-operation.md)
  
[DeleteAttachment-Vorgang](deleteattachment-operation.md)

