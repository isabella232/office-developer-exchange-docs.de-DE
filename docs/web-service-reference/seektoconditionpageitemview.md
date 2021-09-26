---
title: SeekToConditionPageItemView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: b3b86720-d086-47c3-94af-921fdd719edf
description: Das SeekToConditionPageItemView-Element identifiziert die Bedingung, die verwendet wird, um das Ende einer Suche, den Startindex einer Suche, die maximal zurückzugebenden Einträge und die Suchanweisungen für eine FindItem- oder FindConversation-Suche zu identifizieren.
ms.openlocfilehash: 6f4797a6b90456a50922db1c829757711816273e
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59546105"
---
# <a name="seektoconditionpageitemview"></a>SeekToConditionPageItemView

Das **SeekToConditionPageItemView-Element** identifiziert die Bedingung, die verwendet wird, um das Ende einer Suche, den Startindex einer Suche, die maximal zurückzugebenden Einträge und die Suchanweisungen für eine **FindItem-** oder **FindConversation-Suche** zu identifizieren. 
  
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
|Basispunkt  <br/> |Der Textwert des **BasePoint-Attributs** ist der Basispunkt, von dem aus die Suche gestartet wird. Der Textwert  Anfang gibt an, dass die Suche am Anfang des Resultsets beginnt. Der Textwert  Ende gibt an, dass die Suche am Ende des Resultsets beginnt.  <br/> |
|MaxEntriesReturned  <br/> |Der Textwert des **MaxEntriesReturned-Attributs** ist die maximale Anzahl von Elementen, die in einem Resultset zurückgegeben werden können.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

[Bedingung (RestrictionType)](condition-restrictiontype.md)
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[FindConversation](findconversation.md)  |  [FindItem](finditem.md)
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Kann leer sein  <br/> |false  <br/> |
   

