---
title: NewReminderTime
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ff1b6b1c-3557-41d4-8aa6-9528fdb3a21a
description: Das NewReminderTime-Element gibt eine neue Zeit für eine Erinnerung.
ms.openlocfilehash: 9f3f509942c673c916cc646cd9519240aef6ea06
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830531"
---
# <a name="newremindertime"></a>NewReminderTime

Das **NewReminderTime** -Element gibt eine neue Zeit für eine Erinnerung. 
  
```XML
<NewReminderTime/>
```

 **string**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[ReminderItemAction](reminderitemaction.md)
  
## <a name="text-value"></a>Textwert

Der Textwert der **NewReminderTime** -Element ist ein neues Zeitintervall für die Erinnerung. Das **NewReminderTime** -Element wird verwendet, wenn das [ActionType](actiontype-reminderactiontype.md) -Element, um die Erinnerung verzögert **erneut erinnern**, festgelegt ist. Der Wert der **NewReminderTime** muss größer als der durch die [GetReminders Vorgang](getreminders-operation.md)zurückgegebenen [ReminderTime](remindertime.md) sein.
  
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



[ReminderItemAction](reminderitemaction.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

