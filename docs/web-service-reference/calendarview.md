---
title: CalendarView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- CalendarView
api_type:
- schema
ms.assetid: a4a953b8-0710-416c-95ef-59e51eba9982
description: Das CalendarView-Element definiert einen FindItem-Vorgang als Zurückgeben von Kalenderelementen in einer Gruppe, wie sie in einem Kalender angezeigt werden.
ms.openlocfilehash: 5e0180bb5e8a6d9fcbe42380abbe32820117ae29
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59518827"
---
# <a name="calendarview"></a>CalendarView

Das **CalendarView-Element** definiert einen [FindItem-Vorgang](finditem-operation.md) als Zurückgeben von Kalenderelementen in einer Gruppe, wie sie in einem Kalender angezeigt werden. 
  
[FindItem](finditem.md)
  
[CalendarView](calendarview.md)
  
```XML
<CalendarView MaxEntriesReturned="" StartDate="" EndDate="" />
```

**CalendarView**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**MaxEntriesReturned** <br/> |Beschreibt die maximale Anzahl von Ergebnissen, die in der FindItem-Antwort zurückgegeben werden sollen.  <br/> |
|**StartDate** <br/> |Gibt den Anfang einer Zeitspanne an, die für Kalenderelemente abgefragt wird. Alle Kalenderelemente, deren Endzeit vor **StartDate** liegt, werden nicht zurückgegeben. Der Wert von **StartDate** kann wie in 2006-01-02T12:00:00:00Z (coordinated Universal Time, UTC)-Format oder in einem Format angegeben werden, in dem der Offset für Ortszeit und Zeitzone angegeben ist, wie in 2006-01-02T04:00:00-08:00.  <br/><br/>Dieses Attribut ist erforderlich.  <br/> |
|**EndDate** <br/> |Gibt das Ende einer Zeitspanne an, die für Kalenderelemente abgefragt wird. Alle Kalenderelemente mit einer Startzeit, die auf oder nach **EndDate** liegt, werden nicht zurückgegeben. Der Wert von **EndDate** kann im UTC-Format angegeben werden, wie in 2006-02-02T12:00:00Z, oder in einem Format, in dem der Ortszeit- und Zeitzonenoffset angegeben ist, wie in 2006-02-02T04:00:00-08:00.  <br/><br/>**EndDate** muss größer oder gleich **StartDate** sein; andernfalls wird ein Fehler zurückgegeben. Dieses Attribut ist erforderlich.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FindItem](finditem.md) <br/> |Definiert eine Anforderung zum Suchen von Elementen in einem Postfach.<br/><br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/FindItem` <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Wenn das **CalendarView** -Element in einer FindItem -Anforderung angegeben ist, gibt der Webdienst eine Liste der einzelnen Kalenderelemente und Vorkommen von wiederkehrenden Kalenderelementen innerhalb des bereichs durch **StartDate** und **EndDate** angegebenen zurück.
  
Wenn das **CalendarView-Element** nicht in einer FindItem-Anforderung angegeben ist, gibt der Webdienst eine Liste einzelner Kalenderelemente und wiederkehrender Masterkalenderelemente zurück. Kalendervorkommen eines wiederkehrenden Kalenderelements werden nicht erweitert. 
  
CalendarView-Abfragen sollten nur die folgenden Eigenschaften verwenden, da sie schnellere Kalenderabfragen unterstützen.
  
### <a name="recurrence-blob-properties"></a>Eigenschaften von Serienblobs
  
- MapiStartTime
    
- MapiEndTime
    
- SubjectPrefixInternal
    
- NormalizedSubjectInternal
    
- MapiSubject
    
- Ort
    
- AppointmentColor
    
- MapiIsAllDayEvent
    
- MapiHasAttachment
    
- FreeBusyStatus
    
- ReminderIsSetInternal
    
- ReminderMinutesBeforeStartInternal
    
- AppointmentState
    
- AllAttachmentsHidden
    
- ChangeHighlight
    
### <a name="calculated-from-the-primary-recurrence-blob-or-master"></a>Berechnet aus dem primären Serienblob oder Master
  
- ItemId
    
- IsRecurring
    
- IsException
    
- AppointmentRecurring
    
- MapiStartTime
    
- MapiPRStartDate
    
- MapiEndTime
    
- MapiPREndDate
    
- CalendarItemType
    
- GlobalObjectId
    
- TimeZoneDefinitionStart
    
- TimeZoneDefinitionEnd
    
### <a name="master-calendar-item-properties"></a>Eigenschaften von Masterkalenderelementen
  
- EntryId
    
- ChangeKey
    
- ItemClass
    
- SentRepresentingEmailAddress
    
- SentRepresentingDisplayName
    
- SentRepresentingEntryId
    
- AppointmentRecurrenceBlob
    
- TimeZone
    
- TimeZoneBlob
    
- TimeZoneDefinitionRecurring
    
- CleanGlobalObjectId
    
- AppointmentRecurring
    
- IsException
    
- IsRecurring
    
- MapiSensitivity
    
- ContainerClass
    
- MapiPRStartDate
    
- MapiPREndDate
    
- Categories
    
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt eine FindItem-Anforderung. Eine erfolgreiche Anforderung gibt eine Antwort zurück, die Kalenderelemente enthält, die bei 2006-05-18T00:00:00-08:00 oder danach begonnen und vor 2006-05-19T00:00:00-08:00 beendet wurden.
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindItem Traversal="Shallow" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="calendar:Start"/>
          <t:FieldURI FieldURI="calendar:End"/>
          <t:FieldURI FieldURI="item:Subject"/>
        </t:AdditionalProperties>
      </ItemShape>
      <CalendarView MaxEntriesReturned="2" StartDate="2006-05-18T00:00:00-08:00" EndDate="2006-05-19T00:00:00-08:00"/>
      <ParentFolderIds>
        <t:DistinguishedFolderId Id="calendar"/>
      </ParentFolderIds>
    </FindItem>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [FindItem-Vorgang](finditem-operation.md)
- [Suchen von Elementen](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

