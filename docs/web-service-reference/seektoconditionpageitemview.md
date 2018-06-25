---
title: SeekToConditionPageItemView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b3b86720-d086-47c3-94af-921fdd719edf
description: Das SeekToConditionPageItemView-Element identifiziert die Bedingung, die zur Identifizierung der am Ende von einer Suche, der Startindex für eine Suche, die maximale Einträge zurückgegeben und die Suche erfahren Sie, wie eine Suche FindItem oder FindConversation verwendet wird.
ms.openlocfilehash: e95246079f8c6e7acffac1dabb278895265767d9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831328"
---
# <a name="seektoconditionpageitemview"></a>SeekToConditionPageItemView

Das **SeekToConditionPageItemView** -Element identifiziert die Bedingung, die das Ende einer Suche, der Startindex für eine Suche, die maximale Einträge zurückgegeben und die Richtung der Suche für einen **FindItem** oder **FindConversation identifiziert **suchen. 
  
```XML
<SeekToConditionPageItemView BasePoint="" MaxEntriesReturned="">
   <Condition/>
</SeekToConditionPageItemView>
```

 **SeekToConditionPageViewType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|Basispunkt  <br/> |Der Textwert des **Basispunkt** -Attributs ist der Basiskalender aus, in dem die Suche beginnen soll. Der **Anfang** ein Textwerts gibt an, dass die Suche am Anfang des Resultsets gestartet wird. **Ende** ein Textwerts gibt an, dass die Suche am Ende des Resultsets gestartet wird.  <br/> |
|"MaxEntriesReturned"  <br/> |Der Textwert des Attributs **"MaxEntriesReturned"** ist die maximale Anzahl der Elemente, die in einem Resultset zurückgegeben werden kann.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

[Bedingung (RestrictionType)](condition-restrictiontype.md)
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[FindConversation](findconversation.md) | [FindItem](finditem.md)
  
## <a name="remarks"></a>Hinweise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Kann leer sein  <br/> |false  <br/> |
   

