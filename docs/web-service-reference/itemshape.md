---
title: ItemShape
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ItemShape
api_type:
- schema
ms.assetid: c5604161-bbc0-40bc-ad75-ff7e837d745f
description: Das ItemShape-Element identifiziert eine Reihe von Eigenschaften in einem GetItem Operation, FindItem Vorgang oder SyncFolderItems Vorgangsantwort zurückgegeben werden sollen.
ms.openlocfilehash: 95174a85a8fa05cb2612e1289d46c8db32b6e052
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830191"
---
# <a name="itemshape"></a>ItemShape

Das **ItemShape** -Element identifiziert eine Reihe von Eigenschaften in einer Antwort [GetItem Operation](getitem-operation.md), [FindItem Vorgang](finditem-operation.md)oder [SyncFolderItems Vorgang](syncfolderitems-operation.md) zurückgegeben werden sollen. 
  
```XML
<ItemShape>
   <BaseShape/>
   <IncludeMimeContent/>
   <BodyType/>
   <FilterHtmlContent/>
   <ConvertHtmlCodePageToUTF8/>
   <AdditionalProperties/>
</ItemShape>
```

 **ItemResponseShapeType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[BaseShape](baseshape.md) <br/> |Identifiziert die grundlegende Konfiguration von Eigenschaften in einer Antwort Elements oder Ordners zurückgegeben werden sollen.  <br/> |
|[IncludeMimeContent](includemimecontent.md) <br/> |Gibt an, ob der Inhalt Multipurpose Internet Mail Extensions (MIME) eines Elements in der Antwort zurückgegeben wird.  <br/> |
|[BodyType](bodytype.md) <br/> |Gibt an, wie der Textkörper in der Antwort formatiert ist.  <br/> |
|[ConvertHtmlCodePageToUTF8](converthtmlcodepagetoutf8.md) <br/> |Gibt an, ob das Element HTML-Textkörper in UTF8 konvertiert wird.  <br/> |
|[FilterHtmlContent](filterhtmlcontent.md) <br/> |Gibt an, ob HTML-Content-Filterung aktiviert ist.  <br/> |
|[AdditionalProperties](additionalproperties.md) <br/> |Bezeichnet die zusätzliche Eigenschaften, die in eine Antwort zurückgegeben.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GetItem](getitem.md) <br/> |Definiert eine Anforderung zum Abrufen von Elementen aus einem Postfach im Exchange-Speicher.  <br/> Es folgt der XPath-Ausdruck, der dieses Element:  <br/>  `/GetItem` <br/> |
|[FindItem](finditem.md) <br/> |Definiert eine Anforderung an allen Elementen gesucht, die in einem Ordner enthalten sind.  <br/> Es folgt der XPath-Ausdruck, der dieses Element:  <br/>  `/FindItem` <br/> |
|[SyncFolderItems](syncfolderitems.md) <br/> |Definiert eine Anforderung zum Synchronisieren von Elementen in einem Ordner von Exchange-Speicher.  <br/> Es folgt der XPath-Ausdruck, der dieses Element:  <br/>  `/SyncFolderItems` <br/> |
   
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



[GetItem Operation](getitem-operation.md)
  
[FindItem-Vorgang](finditem-operation.md)
  
[SyncFolderItems-Vorgang](syncfolderitems-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

