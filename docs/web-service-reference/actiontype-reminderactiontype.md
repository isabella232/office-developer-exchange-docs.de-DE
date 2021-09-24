---
title: ActionType (ReminderActionType)
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 0ffcdcf4-8ea3-483c-bb7f-0cd84126120c
description: Das ActionType-Element gibt die Aktion an, die für die Erinnerung ausgeführt werden soll.
ms.openlocfilehash: d78725c75ad13a71d69d7749f0a71cd99d606929
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522257"
---
# <a name="actiontype-reminderactiontype"></a>ActionType (ReminderActionType)

Das **ActionType-Element** gibt die Aktion an, die für die Erinnerung ausgeführt werden soll. 
  
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

Der Textwert des **ActionType-Elements** gibt die Aktion an, die für die Erinnerung ausgeführt werden soll. Der Textwert **Schließen** gibt an, dass die Erinnerung geschlossen werden soll. Der Textwert von **"Snooze"** gibt an, dass die Erinnerung bis zu dem durch das [NewReminderTime-Element](newremindertime.md) angegebenen Zeitpunkt verzögert werden soll. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [ReminderItemAction](reminderitemaction.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

