---
title: DeleteAttachment-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- DeleteAttachment
api_type:
- schema
ms.assetid: 4d48e595-b98c-48e7-bbeb-cacf91d12a78
description: Der DeleteAttachment-Vorgang wird verwendet, um Datei- und Elementanlagen aus einem vorhandenen Element im Exchange Speicher zu löschen.
ms.openlocfilehash: bd08776e1f4e75204819ef5463e297e3770a34a4
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59546686"
---
# <a name="deleteattachment-operation"></a>DeleteAttachment-Vorgang

Der DeleteAttachment-Vorgang wird verwendet, um Datei- und Elementanlagen aus einem vorhandenen Element im Exchange Speicher zu löschen.
  
## <a name="remarks"></a>HinwBemerkungeneise

Mit diesem Vorgang können Sie eine oder mehrere Anlagen nach ID löschen.
  
## <a name="deleteattachment-request-example"></a>DeleteAttachment-Anforderungsbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel einer DeleteAttachment-Anforderung zeigt, wie eine Elementanlage gelöscht wird.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <DeleteAttachment xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <AttachmentIds>
        <t:AttachmentId Id="AAAtAEFkbWluaX"/>
      </AttachmentIds>
    </DeleteAttachment>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Comments

Der Anlagenbezeichner wurde gekürzt, um die Lesbarkeit zu gewährleisten.
  
### <a name="request-elements"></a>Anfordern von Elementen

In der Anforderung werden folgende Elemente verwendet:
  
- [DeleteAttachment](deleteattachment.md)
    
- [AttachmentIds](attachmentids.md)
    
- [AttachmentId](attachmentid.md)
    
## <a name="deleteattachment-response-example"></a>DeleteAttachment-Antwortbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine DeleteAttachment-Anforderung.
  
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
    <DeleteAttachmentResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                              xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                              xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:DeleteAttachmentResponseMessage xsi:type="m:DeleteAttachmentResponseMessageType" ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootItemId RootItemId="AAAtAEFkbWluaXN..." RootItemChangeKey="CQAAABYAA..."/>
        </m:DeleteAttachmentResponseMessage>
      </m:ResponseMessages>
    </DeleteAttachmentResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Comments

Der CreateAttachment-Vorgang gibt ein Element vom Typ AttachmentIdType zurück, das eine **RootItemId** und **einen RootItemChangeKey** enthält. Diese Attribute sind für Bezeichner innerhalb einer DeleteAttachment-Anforderung nicht zulässig. DeleteAttachment verwendet Elemente vom Typ RequestAttachmentIdType, die diese Attribute nicht enthalten.
  
Die DeleteAttachment-Antwort enthält die ID des übergeordneten Elements. Wenn Anlagen aus einem Element entfernt werden, wird der Änderungsschlüssel des Elements geändert. Der neue Elementänderungsschlüssel kann aus der DeleteAttachment-Antwort abgerufen werden.
  
> [!NOTE]
> Der [RootItemId-Bezeichner](rootitemid.md) und der ChangeKey wurden gekürzt, um die Lesbarkeit zu gewährleisten. 
  
### <a name="successful-response-elements"></a>Erfolgreiche Antwortelemente

In der Antwort werden folgende Elemente verwendet:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [DeleteAttachmentResponse](deleteattachmentresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [DeleteAttachmentResponseMessage](deleteattachmentresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [RootItemId](rootitemid.md)
    
## <a name="see-also"></a>Siehe auch

- [CreateAttachment-Vorgang](createattachment-operation.md) 
- [GetAttachment-Vorgang](getattachment-operation.md)

