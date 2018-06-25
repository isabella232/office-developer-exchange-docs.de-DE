---
title: FilterHtmlContent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FilterHtmlContent
api_type:
- schema
ms.assetid: 2f9358a0-de1d-4544-9aa0-d9f6519f3b5f
description: Das FilterHtmlContent-Element gibt an, ob potenziell unsichere HTML-Inhalte aus eines Elements oder einer Anlage gefiltert wird.
ms.openlocfilehash: db181eff9586061d728a5e4ef55a78f4955b5713
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758427"
---
# <a name="filterhtmlcontent"></a>FilterHtmlContent

Das **FilterHtmlContent** -Element gibt an, ob potenziell unsichere HTML-Inhalte aus eines Elements oder einer Anlage gefiltert wird. 
  
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
|[AttachmentShape](attachmentshape.md) <br/> | Bezeichnet die zusätzliche Eigenschaften in einer Antwort auf eine Anforderung [GetAttachment](getattachment.md) zurückgegeben werden sollen.  <br/><br/>  Es folgt der XPath-Ausdruck, der dieses Element: <br/> <br/>  `/GetAttachment/AttachmentShape` <br/> |
|[ItemShape](itemshape.md) <br/> | Identifiziert die Elementeigenschaften und den Inhalt in einer Antwort GetItem, FindItem oder SyncFolderItems aufzunehmen.  <br/> <br/> Folgende XPath-Ausdrücke werden für dieses Element verwendet: <br/> <br/>  `/GetItem/ItemShape`<br/> <br/>  `/FindItem/ItemShape`<br/> <br/>  `/SyncFolderItems/ItemShape` <br/> |
   
## <a name="text-value"></a>Textwert

Dieses Element kann **true** oder **false**sein. Der Standardwert ist **false**. Dies ist ein Boolean-Datentyp.
  
## <a name="remarks"></a>Hinweise

Dieses Element ist optional.
  
Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, der Exchange-Server, mit die Clientzugriffs-Serverrolle installiert ausgeführt wird.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

