---
title: Reminder
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bfaf84eb-271a-4728-84fc-a20205a100bd
description: Das Reminder-Element gibt den Typ der Erinnerungen an, die zurückgegeben werden sollen.
ms.openlocfilehash: 4ac20143bbfb29fb8f962515f2faba224b2f973f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465527"
---
# <a name="remindertype"></a>Reminder

Das **Reminder** -Element gibt den Typ der Erinnerungen an, die zurückgegeben werden sollen. 
  
```XML
<ReminderType> All | Current | Old </ReminderType>
```

 **Zeichenfolge**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[GetReminders](getreminders.md)
  
## <a name="text-value"></a>Textwert

Der Textwert des **Reminder** -Elements ist der Typ der Erinnerungen, die zurückgegeben werden sollen, entweder **all**, **Current**oder **Old**. **All** ist der empfohlene Wert für dieses Element. Weitere Informationen zur Beziehung zwischen dem **Reminder** -Element und den Elementen [BeginTime](begintime.md) und [EndTime](endtime-remindermessagedatatype.md) finden Sie unter [getmahnte-Vorgang](getreminders-operation.md).
  
## <a name="remarks"></a>Bemerkungen

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetReminders](getreminders.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

