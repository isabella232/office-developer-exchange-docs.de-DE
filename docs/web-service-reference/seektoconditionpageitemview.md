---
title: SeekToConditionPageItemView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b3b86720-d086-47c3-94af-921fdd719edf
description: Das SeekToConditionPageItemView-Element gibt die Bedingung an, die zum Identifizieren des Endes einer Suche, des startIndex einer Suche, der maximal zurückzugebenden Einträge und der Suchanweisungen für eine FindItem-oder FindConversation-Suche verwendet wird.
ms.openlocfilehash: dbb073263740ccdf75367f85f672b7d5ec78f7a0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466836"
---
# <a name="seektoconditionpageitemview"></a>SeekToConditionPageItemView

Das **SeekToConditionPageItemView** -Element gibt die Bedingung an, die zum Identifizieren des Endes einer Suche, des startIndex einer Suche, der maximal zurückzugebenden Einträge und der Suchanweisungen für eine **FindItem** -oder **FindConversation** -Suche verwendet wird. 
  
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
|Basepoint  <br/> |Der Textwert des **Basepoint** -Attributs ist der Basispunkt, von dem aus die Suche gestartet wird. Der Textwert **Anfang** gibt an, dass die Suche am Anfang der Ergebnismenge beginnt. Ein Textwert von **End** gibt an, dass die Suche am Ende der Ergebnismenge beginnt.  <br/> |
|MaxEntriesReturned  <br/> |Der Textwert des **MaxEntriesReturned** -Attributs ist die maximale Anzahl von Elementen, die in einer Ergebnismenge zurückgegeben werden können.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

[Condition (restrictiontype)](condition-restrictiontype.md)
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[FindConversation](findconversation.md)  |  [FindItem](finditem.md)
  
## <a name="remarks"></a>Bemerkungen

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Kann leer sein  <br/> |false  <br/> |
   

