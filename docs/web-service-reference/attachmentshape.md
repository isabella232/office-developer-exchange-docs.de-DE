---
title: AttachmentShape
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AttachmentShape
api_type:
- schema
ms.assetid: 734914b5-3a16-4744-90a5-741fd30c4676
description: Das AttachmentShape-Element identifiziert zusätzliche Eigenschaften in einer Antwort auf eine Anforderung GetAttachment zurückgegeben werden sollen.
ms.openlocfilehash: dc6769faa5fd28ce31b796f86c507aec54abff7a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757397"
---
# <a name="attachmentshape"></a>AttachmentShape

Das **AttachmentShape** -Element identifiziert zusätzliche Eigenschaften in einer Antwort auf eine Anforderung [GetAttachment](getattachment.md) zurückgegeben werden sollen. 
  
- [GetAttachment](getattachment.md)
  
- [AttachmentShape](attachmentshape.md)
  
```xml
<AttachmentShape>
   <IncludeMimeContent/>
   <BodyType/>
   <FilterHtmlContent/>
   <AdditionalProperties/>
</AttachmentShape>
```

 **AttachmentResponseShapeType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[IncludeMimeContent](includemimecontent.md) <br/> |Gibt an, ob der Inhalt Multipurpose Internet Mail Extensions (MIME) eines Elements oder die Anlage in der Antwort zurückgegeben wird. Dieses Element ist optional.  <br/> |
|[BodyType](bodytype.md) <br/> |Gibt an, wie der Textkörper in der Antwort formatiert ist. Dieses Element ist optional.  <br/> |
|[FilterHtmlContent](filterhtmlcontent.md) <br/> |Gibt an, ob potenziell unsichere HTML-Inhalte aus einer Anlage gefiltert wird. Dieses Element ist optional.  <br/> |
|[AdditionalProperties](additionalproperties.md) <br/> |Bezeichnet die zusätzliche Eigenschaften, die in eine Antwort zurückgegeben. Dieses Element ist optional.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GetAttachment](getattachment.md) <br/> |Das Element, das eine Anforderung definiert an eine Anlage aus einem Postfach im Exchange-Speicher abzurufen.  <br/> Es folgt der XPath-Ausdruck, der dieses Element:  <br/>  `/GetAttachment` <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [GetAttachment-Vorgang](getattachment-operation.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

