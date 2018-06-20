---
title: GetAttachment
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
ms.assetid: 9443cf96-b451-4530-b868-490dff798673
description: Das GetAttachment-Element ist das Stammelement im eine Anforderung an eine Anlage aus dem Exchange-Speicher abzurufen.
ms.openlocfilehash: fb639c86a0654e8f9e9601310f7c2f5b0fc7d729
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758582"
---
# <a name="getattachment"></a>GetAttachment

Das **GetAttachment** -Element ist das Stammelement im eine Anforderung an eine Anlage aus dem Exchange-Speicher abzurufen. 
  
```xml
<GetAttachment>
   <AttachmentShape/>
   <AttachmentIds/>
</GetAttachment>
```

 **GetAttachmentType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[AttachmentShape](attachmentshape.md) <br/> |Zusätzliche erweiterte Elementeigenschaften in einer Antwort auf eine Anforderung [GetAttachment](getattachment.md) zurückzugebenden identifiziert. Dieses Element ist optional.  <br/> |
|[AttachmentIds](attachmentids.md) <br/> |Ein Array mit den IDs der Anlage enthält.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>Hinweise

Das [AttachmentShape](attachmentshape.md) -Element ist nicht erforderlich, um die in der Antwort zurückgegebenen Eigenschaften zu identifizieren. Die [-Vorgangs GetAttachment](getattachment-operation.md) gibt den Namen, ContentType, ContentId, ContentLocation und die Content-Eigenschaften für Dateianlagen zurück. Für Anlagen sind die zurückgegebenen Eigenschaften den Namen, ContentType, ContentId, ContentLocation und alle die angefügte Eigenschaften des Elements. Dies ist gleichbedeutend mit mithilfe des AllProperties-Basis-Shapes in einer [GetItem](getitem.md) -Anforderung. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetAttachment-Vorgang](getattachment-operation.md)
  
[GetAttachmentResponse](getattachmentresponse.md)

