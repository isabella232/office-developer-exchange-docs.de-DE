---
title: ItemShape
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ItemShape
api_type:
- schema
ms.assetid: c5604161-bbc0-40bc-ad75-ff7e837d745f
description: Das ItemShape-Element identifiziert einen Satz von Eigenschaften, die in einer GetItem-Operation, einem FindItem-Vorgang oder einer SyncFolderItems-Vorgangsantwort zurückgegeben werden sollen.
ms.openlocfilehash: d6cc1efc85a8a22e12f2a3616fe949b72b3bba33
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59519394"
---
# <a name="itemshape"></a>ItemShape

Das **ItemShape-Element** identifiziert einen Satz von Eigenschaften, die in einer [GetItem-Operation,](getitem-operation.md)einem [FindItem-Vorgang](finditem-operation.md)oder einer [SyncFolderItems-Vorgangsantwort](syncfolderitems-operation.md) zurückgegeben werden sollen. 
  
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
|[BaseShape](baseshape.md) <br/> |Identifiziert die grundlegende Konfiguration von Eigenschaften, die in einer Element- oder Ordnerantwort zurückgegeben werden sollen.  <br/> |
|[IncludeMimeContent](includemimecontent.md) <br/> |Gibt an, ob der MIME-Inhalt (Multipurpose Internet Mail Extensions) eines Elements in der Antwort zurückgegeben wird.  <br/> |
|[BodyType](bodytype.md) <br/> |Gibt an, wie der Textkörper in der Antwort formatiert wird.  <br/> |
|[ConvertHtmlCodePageToUTF8](converthtmlcodepagetoutf8.md) <br/> |Gibt an, ob der HTML-Textkörper des Elements in UTF8 konvertiert wird.  <br/> |
|[FilterHtmlContent](filterhtmlcontent.md) <br/> |Gibt an, ob die HTML-Inhaltsfilterung aktiviert ist.  <br/> |
|[AdditionalProperties](additionalproperties.md) <br/> |Identifiziert zusätzliche Eigenschaften, die in einer Antwort zurückgegeben werden sollen.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GetItem](getitem.md) <br/> |Definiert eine Anforderung zum Abrufen von Elementen aus einem Postfach im Exchange Speicher.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/GetItem` <br/> |
|[FindItem](finditem.md) <br/> |Definiert eine Anforderung zum Suchen aller Elemente, die in einem Ordner enthalten sind.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/FindItem` <br/> |
|[SyncFolderItems](syncfolderitems.md) <br/> |Definiert eine Anforderung zum Synchronisieren von Elementen in einem Exchange Speicherordner.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/SyncFolderItems` <br/> |
   
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



[GetItem-Vorgang](getitem-operation.md)
  
[FindItem-Vorgang](finditem-operation.md)
  
[SyncFolderItems-Vorgang](syncfolderitems-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

