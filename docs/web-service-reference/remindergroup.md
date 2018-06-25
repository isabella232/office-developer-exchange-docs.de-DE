---
title: ReminderGroup
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3e23c2a1-05d8-4fec-897c-f684a5b97e4c
description: Das ReminderGroup-Element gibt an, ob die Erinnerung für ein Kalenderelement oder einer Aufgabe ist.
ms.openlocfilehash: d9d31cdab482d04149428021ad44cc742108053a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831060"
---
# <a name="remindergroup"></a>ReminderGroup

Das **ReminderGroup** -Element gibt an, ob die Erinnerung für ein Kalenderelement oder einer Aufgabe ist. 
  
```XML
<ReminderGroup> Calendar | Task </ReminderGroup>
```

 **ReminderGroupType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[Reminder](reminder.md)
  
## <a name="text-value"></a>Textwert

Der Textwert des **ReminderGroup** -Elements ist die Gruppentyp der Erinnerung. Der Textwert der **Kalender** gibt an, dass die Erinnerung für ein Kalenderelement ist. Der Textwert der **Aufgabe** gibt an, dass die Erinnerung für ein Aufgabenelement ist. 
  
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



[Reminder](reminder.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

