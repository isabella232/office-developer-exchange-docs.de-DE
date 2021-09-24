---
title: AttachmentShape
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- AttachmentShape
api_type:
- schema
ms.assetid: 734914b5-3a16-4744-90a5-741fd30c4676
description: Das AttachmentShape-Element identifiziert zusätzliche Eigenschaften, die in einer Antwort auf eine GetAttachment-Anforderung zurückgegeben werden sollen.
ms.openlocfilehash: 2c7ceb25f481ec07577117e46e26537e657e18c7
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520038"
---
# <a name="attachmentshape"></a>AttachmentShape

Das **AttachmentShape-Element** identifiziert zusätzliche Eigenschaften, die in einer Antwort auf eine [GetAttachment-Anforderung](getattachment.md) zurückgegeben werden sollen. 
  
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
|[IncludeMimeContent](includemimecontent.md) <br/> |Gibt an, ob der MIME-Inhalt (Multipurpose Internet Mail Extensions) eines Elements oder einer Anlage in der Antwort zurückgegeben wird. Dieses Element ist optional.  <br/> |
|[BodyType](bodytype.md) <br/> |Gibt an, wie der Textkörper in der Antwort formatiert wird. Dieses Element ist optional.  <br/> |
|[FilterHtmlContent](filterhtmlcontent.md) <br/> |Gibt an, ob potenziell unsichere HTML-Inhalte aus einer Anlage gefiltert werden. Dieses Element ist optional.  <br/> |
|[AdditionalProperties](additionalproperties.md) <br/> |Identifiziert zusätzliche Eigenschaften, die in einer Antwort zurückgegeben werden sollen. Dieses Element ist optional.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GetAttachment](getattachment.md) <br/> |Das Element, das eine Anforderung zum Abrufen einer Anlage aus einem Postfach im Exchange Speicher definiert.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/GetAttachment` <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [GetAttachment-Vorgang](getattachment-operation.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

