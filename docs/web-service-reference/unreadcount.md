---
title: UnreadCount
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UnreadCount
api_type:
- schema
ms.assetid: 53b22647-1453-4707-9ea0-6a8369748d56
description: Das UnreadCount-Element enthält die Anzahl der ungelesenen Elemente in einem Ordner.
ms.openlocfilehash: fbe887f8f6d83fbcf48ed9593b3d19322a7f48be
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839326"
---
# <a name="unreadcount"></a>UnreadCount

Das **UnreadCount** -Element enthält die Anzahl der ungelesenen Elemente in einem Ordner. 
  
```XML
<UnreadCount/>
```

 **xs: int**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Unterhaltung (ConversationType)](conversation-conversationtype.md) <br/> |Stellt eine einfache Unterhaltung dar.  <br/> |
|[Folder](folder.md) <br/> |Stellt einen Ordner in einem Postfach an.  <br/> |
|[ModifiedEvent](modifiedevent.md) <br/> |Stellt ein Ereignis, bei denen eines Elements oder Ordners geändert wird.  <br/> |
|["SearchFolder"](searchfolder.md) <br/> |Stellt einen Suchordner in einem Postfach an.  <br/> |
|[TasksFolder](tasksfolder.md) <br/> |Stellt einen Ordner in einem Postfach an.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert stellt einen ganzzahligen Wert dar. Diese Eigenschaft ist schreibgeschützt.
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

