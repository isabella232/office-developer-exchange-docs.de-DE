---
title: FilterHtmlContent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- FilterHtmlContent
api_type:
- schema
ms.assetid: 2f9358a0-de1d-4544-9aa0-d9f6519f3b5f
description: Das FilterHtmlContent-Element gibt an, ob potenziell unsicherer HTML-Inhalt aus einem Element oder einer Anlage gefiltert wird.
ms.openlocfilehash: 9400c86465db994251a00164517590268e7e4ad1
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510085"
---
# <a name="filterhtmlcontent"></a>FilterHtmlContent

Das **FilterHtmlContent-Element** gibt an, ob potenziell unsicherer HTML-Inhalt aus einem Element oder einer Anlage gefiltert wird. 
  
```xml
<FilterHtmlContent>true or false</FilterHtmlContent>
```

 **boolean**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[AttachmentShape](attachmentshape.md) <br/> | Identifiziert zusätzliche Eigenschaften, die in einer Antwort auf eine [GetAttachment-Anforderung](getattachment.md) zurückgegeben werden sollen.  <br/><br/>  Für dieses Element wird folgender XPath-Ausdruck verwendet:  <br/> <br/>  `/GetAttachment/AttachmentShape` <br/> |
|[ItemShape](itemshape.md) <br/> | Identifiziert die Elementeigenschaften und -inhalte, die in eine GetItem-, FindItem- oder SyncFolderItems-Antwort eingeschlossen werden sollen.  <br/> <br/> Folgende XPath-Ausdrücke werden für dieses Element verwendet: <br/> <br/>  `/GetItem/ItemShape`<br/> <br/>  `/FindItem/ItemShape`<br/> <br/>  `/SyncFolderItems/ItemShape` <br/> |
   
## <a name="text-value"></a>Textwert

Dieses Element kann entweder **"true"** oder **"false" sein.** Der Standardwert ist **false**. Dies ist ein boolescher Datentyp.
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element ist optional.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Exchange Server mit installierter Clientzugriffsserverrolle ausgeführt wird.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

