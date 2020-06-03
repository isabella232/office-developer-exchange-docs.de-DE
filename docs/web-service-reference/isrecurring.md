---
title: IsRecurring
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsRecurring
api_type:
- schema
ms.assetid: f4df6997-8d5b-4893-a4a5-fc7047e0a9c3
description: Das isterminive-Element gibt an, ob ein Kalenderelement, eine Besprechungsanfrage oder eine Aufgabe Teil eines wiederkehrenden Elements ist. Dieses Element ist schreibgeschützt.
ms.openlocfilehash: 72c71c1955b69f1c0df855ce4bd0ed02d4c89122
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526487"
---
# <a name="isrecurring"></a>IsRecurring

Das **isterminive** -Element gibt an, ob ein Kalenderelement, eine Besprechungsanfrage oder eine Aufgabe Teil eines wiederkehrenden Elements ist. Dieses Element ist schreibgeschützt. 
  
```xml
<IsRecurring/>
```

 **Boolescher Wert**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[CalendarItem](calendaritem.md) <br/> |Stellt ein Element im Exchange-Kalender dar.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.  <br/> |
|[Aufgabe](task.md) <br/> |Stellt eine Aufgabe im Exchange-Informationsspeicher dar.  <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert, der einen booleschen Wert darstellt, ist erforderlich.
  
## <a name="remarks"></a>Bemerkungen

In der folgenden Tabelle wird gezeigt, wie die **isterminive** -Eigenschaft für unterschiedliche Kalenderelement Typen für Organisatoren und Teilnehmer sowie für Besprechungsanfragen und Updates festgelegt wird. 
  
|**CalendarItem-Typ**|**Organizer <br/> (reterminal)**|**Teilnehmer <br/> (iswiederkehr)**|**Besprechungsanfrage/-Aktualisierung <br/> (einmaliges Anmelden)**|
|:-----|:-----|:-----|:-----|
|Einzelnes Vorkommen  <br/> |**FALSE** <br/> |**FALSE** <br/> |**FALSE** <br/> |
|Wiederkehrendes Master  <br/> |**FALSE** <br/> |**TRUE** <br/> |**TRUE** <br/> |
|Wiederkehrende Ausnahme  <br/> |**TRUE** <br/> |**TRUE** <br/> |**TRUE** <br/> |
   
Der Wert der **iswiederkehr** -Eigenschaft, der für wiederkehrende Hauptkalender Elemente für den Organisator festgelegt ist, ist falsch; Dieser Wert sollte auf **true**festgelegt werden. 
  
> [!NOTE]
> Der GetUserAvailability-Vorgang verfügt auch über ein [iswiederkehr Endes Element (CalendarEventDetails)](isrecurring-calendareventdetails.md) . 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[TaskType. iswiederkehr Ende](https://msdn.microsoft.com/library/ExchangeWebServices.TaskType.IsRecurring.aspx)
  
[CalendarEventDetails. iswiederkehr Ende](https://msdn.microsoft.com/library/ExchangeWebServices.CalendarEventDetails.IsRecurring.aspx)
  
[CalendarItemType. iswiederkehr Ende](https://msdn.microsoft.com/library/ExchangeWebServices.CalendarItemType.IsRecurring.aspx)
  
[MeetingRequestMessageType. iswiederkehr Ende](https://msdn.microsoft.com/library/ExchangeWebServices.MeetingRequestMessageType.IsRecurring.aspx)
  
[CalendarItemType.IsRecurringSpecified](https://msdn.microsoft.com/library/ExchangeWebServices.CalendarItemType.IsRecurringSpecified.aspx)
  
[MeetingRequestMessageType.IsRecurringSpecified](https://msdn.microsoft.com/library/ExchangeWebServices.MeetingRequestMessageType.IsRecurringSpecified.aspx)
  
[TaskType. IsRecurringSpecified](https://msdn.microsoft.com/library/ExchangeWebServices.TaskType.IsRecurringSpecified.aspx)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

