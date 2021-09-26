---
title: BaseShape (PreviewItemBaseShapeType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 7b9e2fdd-5678-4178-9297-7f12a3ca9d64
description: Das BaseShape-Element gibt entweder die Standardvorschau mit allen zurückgegebenen Eigenschaften oder eine kompakte Vorschau mit weniger zurückgegebenen Eigenschaften an.
ms.openlocfilehash: b30922a5f8e11200679ffe5aa813d3a0e5f4578e
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59545692"
---
# <a name="baseshape-previewitembaseshapetype"></a>BaseShape (PreviewItemBaseShapeType)

Das **BaseShape-Element** gibt entweder die Standardvorschau mit allen zurückgegebenen Eigenschaften oder eine kompakte Vorschau mit weniger zurückgegebenen Eigenschaften an. 
  
```XML
<BaseShape> Default | Compact</BaseShape>
```

 **PreviewItemBaseShapeType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[PreviewItemResponseShape](previewitemresponseshape.md) <br/> |Enthält die Form der Antwort.  <br/> |
   
## <a name="text-value"></a>Textwert

**BaseShape-Elementtextwerte**

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Standard  <br/> |Gibt an, dass alle Eigenschaften angezeigt werden.  <br/> |
|Compact  <br/> |Gibt an, dass nur ausgewählte Eigenschaften angezeigt werden.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Typschema  <br/> |
|Überprüfungsdatei  <br/> |types.xsd  <br/> |
|Kann leer sein  <br/> ||
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

