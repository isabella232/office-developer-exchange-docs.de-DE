---
title: ReminderGroup
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 3e23c2a1-05d8-4fec-897c-f684a5b97e4c
description: Das ReminderGroup-Element gibt an, ob es sich bei der Erinnerung um ein Kalenderelement oder eine Aufgabe handelt.
ms.openlocfilehash: 7ec19505e9237680aee1b3a31332db7fdc4c0dd4
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59512471"
---
# <a name="remindergroup"></a>ReminderGroup

Das **ReminderGroup-Element** gibt an, ob es sich bei der Erinnerung um ein Kalenderelement oder eine Aufgabe handelt. 
  
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

Der Textwert des **ReminderGroup-Elements** ist der Gruppentyp der Erinnerung. Der Textwert des **Kalenders** gibt an, dass die Erinnerung für ein Kalenderelement ist. Der Textwert von **Vorgang** gibt an, dass die Erinnerung für ein Aufgabenelement gilt. 
  
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



[Reminder](reminder.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

