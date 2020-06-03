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
description: Das ItemShape-Element identifiziert eine Reihe von Eigenschaften, die in einer GetItem-Operation, einer FindItem-Operation oder einer SyncFolderItems-Vorgangs Antwort zurückgegeben werden sollen.
ms.openlocfilehash: ffb666ee331b55a4f04cad076c705e4bec980e03
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458124"
---
# <a name="itemshape"></a>ItemShape

Das **ItemShape** -Element identifiziert eine Reihe von Eigenschaften, die in einer [GetItem-Operation](getitem-operation.md), einer [FindItem-Operation](finditem-operation.md)oder einer SyncFolderItems- [Vorgangs](syncfolderitems-operation.md) Antwort zurückgegeben werden sollen. 
  
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
|[BaseShape](baseshape.md) <br/> |Gibt die grundlegende Konfiguration von Eigenschaften an, die in einer Element-oder Ordner Antwort zurückgegeben werden sollen.  <br/> |
|[IncludeMimeContent](includemimecontent.md) <br/> |Gibt an, ob der Multipurpose Internet Mail Extensions (MIME) Inhalt eines Elements in der Antwort zurückgegeben wird.  <br/> |
|[BodyType](bodytype.md) <br/> |Gibt an, wie der Textkörper in der Antwort formatiert wird.  <br/> |
|[ConvertHtmlCodePageToUTF8](converthtmlcodepagetoutf8.md) <br/> |Gibt an, ob der Element-HTML-Text in UTF8 konvertiert wird.  <br/> |
|[FilterHtmlContent](filterhtmlcontent.md) <br/> |Gibt an, ob die HTML-Inhaltsfilterung aktiviert ist.  <br/> |
|[AdditionalProperties](additionalproperties.md) <br/> |Identifiziert zusätzliche Eigenschaften, die in einer Antwort zurückgegeben werden sollen.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GetItem](getitem.md) <br/> |Definiert eine Anforderung zum Abrufen von Elementen aus einem Postfach im Exchange-Informationsspeicher.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/GetItem` <br/> |
|[FindItem](finditem.md) <br/> |Definiert eine Anforderung zum Suchen aller Elemente, die in einem Ordner enthalten sind.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/FindItem` <br/> |
|[SyncFolderItems](syncfolderitems.md) <br/> |Definiert eine Anforderung zum Synchronisieren von Elementen in einem Exchange-Informationsspeicher Ordner.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/SyncFolderItems` <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetItem-Vorgang](getitem-operation.md)
  
[FindItem-Vorgang](finditem-operation.md)
  
[SyncFolderItems-Vorgang](syncfolderitems-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

