---
title: ReminderType
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bfaf84eb-271a-4728-84fc-a20205a100bd
description: Das ReminderType-Element gibt den Typ des zurückzugebenden Erinnerungen.
ms.openlocfilehash: 11739d2068a1009b2840b2169e86b113151cbfa9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831077"
---
# <a name="remindertype"></a>ReminderType

Das **ReminderType** -Element gibt den Typ des zurückzugebenden Erinnerungen. 
  
```XML
<ReminderType> All | Current | Old </ReminderType>
```

 **string**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[GetReminders](getreminders.md)
  
## <a name="text-value"></a>Textwert

Der Textwert des **ReminderType** -Elements ist der Typ der Erinnerungen um **Alle**, **aktuelle**oder **alte**zurückzugeben. **Alle** ist der empfohlene Wert für dieses Element. Weitere Informationen zur Beziehung zwischen dem **ReminderType** -Element und die Elemente [BeginTime](begintime.md) und [EndTime](endtime-remindermessagedatatype.md) finden Sie unter [GetReminders-Vorgang](getreminders-operation.md).
  
## <a name="remarks"></a>Hinweise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetReminders](getreminders.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

