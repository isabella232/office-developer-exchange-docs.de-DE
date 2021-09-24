---
title: Erinnerung
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 54dd748a-23a5-4ea2-88f2-b74c68a3c48f
description: Das Reminder-Element gibt eine Erinnerung für eine Aufgabe oder ein Kalenderelement an.
ms.openlocfilehash: 97b4a1dfb2739ff9ea335bca1e61e264715ced30
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59512492"
---
# <a name="reminder"></a>Erinnerung

Das **Reminder-Element** gibt eine Erinnerung für eine Aufgabe oder ein Kalenderelement an. 
  
```XML
<Reminder>
   <Subject></Subject>
   <Location></Location>
   <ReminderTime></ReminderTime>
   <StartDate></StartDate>
   <EndDate></EndDate>
   <ItemId></ItemId>
   <RecurringMasterItemId></RecurringMasterItemId>
   <ReminderGroup></ReminderGroup>
   <UID></UID>
</Reminder>

```

 **ReminderType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

[Betreff](subject.md)  |  [Speicherort](location.md)  |  [ReminderTime](remindertime.md)  |  [StartDate](startdate.md)  |  [EndDate (ReminderType)](enddate-remindertype.md)  |  [ItemId](itemid.md)  |  [RecurringMasterItemId (ItemIdType)](recurringmasteritemid-itemidtype.md)  |  [ReminderGroup](remindergroup.md)  |  [UID](uid.md)
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[Reminders](reminders.md)
  
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



[Reminders](reminders.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

