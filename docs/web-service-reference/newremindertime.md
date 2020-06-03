---
title: Neuerinnerung
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ff1b6b1c-3557-41d4-8aa6-9528fdb3a21a
description: Das Element Reminder gibt eine neue Zeit für eine Erinnerung an.
ms.openlocfilehash: a10f7e481b474501f33dba4c09060766568952b0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465954"
---
# <a name="newremindertime"></a>Neuerinnerung

Das Element **Reminder** gibt eine neue Zeit für eine Erinnerung an. 
  
```XML
<NewReminderTime/>
```

 **Zeichenfolge**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[ReminderItemAction](reminderitemaction.md)
  
## <a name="text-value"></a>Textwert

Der Textwert des Elements **Reminder** ist eine neue Zeit für die Erinnerung. Das Element **Reminder** wird verwendet, wenn das [Action](actiontype-reminderactiontype.md) Type-Element auf **Snooze**festgelegt ist, um die Erinnerung zu verzögern. Der Wert der **Reminder** -Uhrzeit muss größer sein als die von der [geterinnerungs-Operation](getreminders-operation.md)zurückgegebene [Erinnerungszeit](remindertime.md) .
  
## <a name="remarks"></a>Bemerkungen

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



[ReminderItemAction](reminderitemaction.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

