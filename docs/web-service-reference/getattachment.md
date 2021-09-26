---
title: GetAttachment
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
ms.assetid: 9443cf96-b451-4530-b868-490dff798673
description: Das GetAttachment-Element ist das Stammelement in einer Anforderung zum Abrufen einer Anlage aus dem Exchange Speicher.
ms.openlocfilehash: 057b42e78845f583cf1e52804e0108f335ef951c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59546371"
---
# <a name="getattachment"></a>GetAttachment

Das **GetAttachment-Element** ist das Stammelement in einer Anforderung zum Abrufen einer Anlage aus dem Exchange Speicher. 
  
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
|[AttachmentShape](attachmentshape.md) <br/> |Identifiziert zusätzliche erweiterte Elementeigenschaften, die in einer Antwort auf eine [GetAttachment-Anforderung](getattachment.md) zurückgegeben werden sollen. Dieses Element ist optional.  <br/> |
|[AttachmentIds](attachmentids.md) <br/> |Enthält ein Array von Anlagenbezeichnern.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das [AttachmentShape-Element](attachmentshape.md) ist nicht erforderlich, um die in der Antwort zurückgegebenen Eigenschaften zu identifizieren. Der [GetAttachment-Vorgang](getattachment-operation.md) gibt die Eigenschaften "Name", "ContentType", "ContentId", "ContentLocation" und "Content" für Dateianlagen zurück. Bei Elementanlagen sind die zurückgegebenen Eigenschaften Name, ContentType, ContentId, ContentLocation und alle Eigenschaften des angefügten Elements. Dies entspricht der Verwendung des AllProperties-Basis-Shapes in einer [GetItem-Anforderung.](getitem.md) 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetAttachment-Vorgang](getattachment-operation.md)
  
[GetAttachmentResponse](getattachmentresponse.md)

