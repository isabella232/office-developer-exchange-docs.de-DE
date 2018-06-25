---
title: ActionType (ReminderActionType)
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0ffcdcf4-8ea3-483c-bb7f-0cd84126120c
description: ActionType-Element gibt die durchzuführende Aktion auf die Erinnerung an.
ms.openlocfilehash: 361259f733756995fae2c2c2390013a728e475a4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757211"
---
# <a name="actiontype-reminderactiontype"></a>ActionType (ReminderActionType)

**ActionType** -Element gibt die durchzuführende Aktion auf die Erinnerung an. 
  
```XML
<ActionType> Dismiss | Snooze </ActionType>
```

 **ReminderActionType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[ReminderItemAction](reminderitemaction.md)
  
## <a name="text-value"></a>Textwert

Der Textwert der **ActionType** -Element gibt die durchzuführende Aktion auf die Erinnerung an. Der Textwert der **Dismiss** gibt an, dass die Erinnerung geschlossen werden soll. Der Textwert der **erneut erinnern** gibt an, dass die Erinnerung soll, bis die Zeit, die durch das [NewReminderTime](newremindertime.md) -Element angegeben verzögert werden. 
  
## <a name="remarks"></a>Hinweise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [ReminderItemAction](reminderitemaction.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

