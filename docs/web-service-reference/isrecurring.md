---
title: IsRecurring
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IsRecurring
api_type:
- schema
ms.assetid: f4df6997-8d5b-4893-a4a5-fc7047e0a9c3
description: Das IsRecurring-Element gibt an, ob ein Kalenderelement, eine Besprechungsanfrage oder eine Aufgabe Teil einer Terminserie ist. Dieses Element ist schreibgeschützt.
ms.openlocfilehash: ea910b78e962906285a73c869e394147c324372c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59532726"
---
# <a name="isrecurring"></a>IsRecurring

Das **IsRecurring-Element** gibt an, ob ein Kalenderelement, eine Besprechungsanfrage oder eine Aufgabe Teil einer Terminserie ist. Dieses Element ist schreibgeschützt. 
  
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
  
## <a name="remarks"></a>HinwBemerkungeneise

Die folgende Tabelle zeigt, wie die **IsRecurring-Eigenschaft** für verschiedene Kalenderelementtypen für Organisatoren und Teilnehmer sowie für Besprechungsanfragen und -aktualisierungen festgelegt wird. 
  
|**CalendarItem-Typ**|**Organizer  <br/> (IsRecurring)**|**Attendee  <br/> (IsRecurring)**|**Besprechungsanfrage/-update  <br/> (IsRecurring)**|
|:-----|:-----|:-----|:-----|
|Einzelnes Vorkommen  <br/> |**FALSE** <br/> |**FALSE** <br/> |**FALSE** <br/> |
|Serienmaster  <br/> |**FALSE** <br/> |**STIMMT** <br/> |**STIMMT** <br/> |
|Wiederkehrende Ausnahme  <br/> |**STIMMT** <br/> |**STIMMT** <br/> |**STIMMT** <br/> |
   
Der Wert der **IsRecurring-Eigenschaft,** der für wiederkehrende Masterkalenderelemente für den Organisator festgelegt wird, ist falsch. dieser Wert sollte auf **TRUE** festgelegt werden. 
  
> [!NOTE]
> Der GetUserAvailability-Vorgang weist auch ein [IsRecurring-Element (CalendarEventDetails)](isrecurring-calendareventdetails.md) auf. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[TaskType.IsRecurring](https://msdn.microsoft.com/library/ExchangeWebServices.TaskType.IsRecurring.aspx)
  
[CalendarEventDetails.IsRecurring](https://msdn.microsoft.com/library/ExchangeWebServices.CalendarEventDetails.IsRecurring.aspx)
  
[CalendarItemType.IsRecurring](https://msdn.microsoft.com/library/ExchangeWebServices.CalendarItemType.IsRecurring.aspx)
  
[MeetingRequestMessageType.IsRecurring](https://msdn.microsoft.com/library/ExchangeWebServices.MeetingRequestMessageType.IsRecurring.aspx)
  
[CalendarItemType.IsRecurringSpecified](https://msdn.microsoft.com/library/ExchangeWebServices.CalendarItemType.IsRecurringSpecified.aspx)
  
[MeetingRequestMessageType.IsRecurringSpecified](https://msdn.microsoft.com/library/ExchangeWebServices.MeetingRequestMessageType.IsRecurringSpecified.aspx)
  
[TaskType.IsRecurringSpecified](https://msdn.microsoft.com/library/ExchangeWebServices.TaskType.IsRecurringSpecified.aspx)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

