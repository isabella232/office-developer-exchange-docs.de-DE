---
title: Elemente
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Items
api_type:
- schema
ms.assetid: 0811a73e-bf1f-4889-9219-73902dd47639
description: Das Items-Element enthält ein Array von Elementen.
ms.openlocfilehash: 489e34ad0e4bcc2520febb3c213db970fa496051
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458131"
---
# <a name="items"></a>Elemente

Das **Items** -Element enthält ein Array von Elementen. 
  
```xml
<Items>
   <Item/>
   <Message/>
   <CalendarItem/>
   <Contact/>
   <DistributionList/>
   <MeetingMessage/>
   <MeetingRequest/>
   <MeetingResponse/>
   <MeetingCancellation/>
   <Task/>
   <PostItem/>
</Items>
```

 **ArrayOfRealItemsType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Element](item.md) <br/> |Stellt ein Element im Exchange-Informationsspeicher dar.  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |Stellt eine Exchange-E-Mail-Nachricht dar.  <br/> |
|[CalendarItem](calendaritem.md) <br/> |Stellt ein Element im Exchange-Kalender dar.  <br/> |
|[Kontaktperson](contact.md) <br/> |Stellt ein Exchange-Kontaktelement dar.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Stellt eine Verteilerliste dar.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Stellt eine Besprechungsnachricht im Exchange-Informationsspeicher dar.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Stellt eine Besprechungsantwort im Exchange-Informationsspeicher dar.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Stellt eine Besprechungsabsage im Exchange-Informationsspeicher dar.  <br/> |
|[Aufgabe](task.md) <br/> |Stellt eine Aufgabe im Exchange-Informationsspeicher dar.  <br/> |
|[PostItem](postitem.md) <br/> |Stellt ein Post-Element im Exchange-Informationsspeicher dar.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[CopyItemResponseMessage](copyitemresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer [CopyItem-Vorgangs](copyitem-operation.md) Anforderung.  <br/> |
|[CreateItemResponseMessage](createitemresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer einzelnen [CreateItem-Vorgangs](createitem-operation.md) Anforderung.  <br/> |
|[GetItemResponseMessage](getitemresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer [GetItem-Vorgangs](getitem-operation.md) Anforderung.  <br/> |
|[GroupedItems](groupeditems.md) <br/> |Stellt eine Auflistung von Elementen dar, die das Ergebnis eines Aufrufs einer gruppierten [FindItem-Operation](finditem-operation.md) sind.  <br/> |
|[MoveItemResponseMessage](moveitemresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer [MoveItem-Vorgangs](moveitem-operation.md) Anforderung.  <br/> |
|[RootFolder (FindItemResponseMessage)](rootfolder-finditemresponsemessage.md) <br/> |Enthält die Ergebnisse einer Suche eines einzelnen Stammordners während eines FindItem- [Vorgangs](finditem-operation.md).  <br/> |
|[UpdateItemResponseMessage](updateitemresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer [UpdateItem-Vorgangs](updateitem-operation.md) Anforderung.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Informationen zur Gruppe von Elementen in einer CreateItem- [Vorgangs](createitem-operation.md) Anforderung finden Sie unter [Items (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md).
  
[Nachrichten](message-ex15websvcsotherref.md) Elemente stellen e-Mail-Nachrichten und alle anderen Elemente dar, die nicht stark vom Exchange-Webdienste Schema typisiert sind. Elemente wie IPM.Sharing- und IPM.InfoPath-Elemente werden als **Message**-Elemente zurückgegeben. Versionen von Exchange, die mit Exchange Server 2010 beginnen, geben das Basis [Element](item.md) Element nicht in den Antworten zurück. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Exchange ausgeführt wird, auf dem die Client Zugriffs-Serverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[EWS-Referenz für Exchange](ews-reference-for-exchange.md)
  
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

