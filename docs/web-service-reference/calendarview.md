---
title: CalendarView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CalendarView
api_type:
- schema
ms.assetid: a4a953b8-0710-416c-95ef-59e51eba9982
description: Das CalendarView-Element definiert eine FindItem-Operation als zurückgeben von Kalenderelementen in einer Gruppe, wie Sie in einem Kalender angezeigt werden.
ms.openlocfilehash: e547a4b2db5c09ebefd9a072da6cc4733818002e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462262"
---
# <a name="calendarview"></a>CalendarView

Das **CalendarView** -Element definiert eine [FindItem-Operation](finditem-operation.md) als zurückgeben von Kalenderelementen in einer Gruppe, wie Sie in einem Kalender angezeigt werden. 
  
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
|**MaxEntriesReturned** <br/> |Beschreibt die maximale Anzahl von Ergebnissen, die in der FindItem-Antwort zurückgegeben werden.  <br/> |
|**StartDate** <br/> |Gibt den Anfang einer Zeitspanne an, die für Kalenderelemente abgefragt wird. Alle Kalenderelemente mit einer Endzeit, die vor dem Start **Datum** liegt, werden nicht zurückgegeben. Der Wert von **StartDate** kann in koordinierte Weltzeit (UTC) Format angegeben werden, wie in 2006-01-02T12:00:00Z oder in einem Format, in dem der lokale Zeit-und Zeitzonenoffset angegeben ist, wie in 2006-01-02T04:00:00-08:00.  <br/><br/>Dieses Attribut ist erforderlich.  <br/> |
|**EndDate** <br/> |Gibt das Ende einer Zeitspanne an, die für Kalenderelemente abgefragt wird. Alle Kalenderelemente mit einer Startzeit, die sich auf oder nach **EndDate** befinden, werden nicht zurückgegeben. Der Wert von **EndDate** kann im UTC-Format angegeben werden, wie in 2006-02-02T12:00:00Z oder in einem Format, in dem der lokale Zeit-und Zeitzonenoffset angegeben ist, wie in 2006-02-02T04:00:00-08:00.  <br/><br/>**EndDate** muss größer als oder gleich **StartDate**sein; Andernfalls wird ein Fehler zurückgegeben. Dieses Attribut ist erforderlich.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FindItem](finditem.md) <br/> |Definiert eine Anforderung zum Suchen von Elementen in einem Postfach.<br/><br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/FindItem` <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn das **CalendarView** -Element in einer FindItem-Anforderung angegeben ist, gibt der Webdienst eine Liste einzelner Kalenderelemente und Vorkommen von wiederkehrenden Kalenderelementen innerhalb des durch **StartDate** und **EndDate**angegebenen Bereichs zurück.
  
Wenn das **CalendarView** -Element in einer FindItem-Anforderung nicht angegeben ist, gibt der Webdienst eine Liste einzelner Kalenderelemente und wiederkehrende Master Kalenderelemente zurück. Kalender Vorkommen eines wiederkehrenden Kalenderelements werden nicht erweitert. 
  
CalendarView-Abfragen sollten nur die folgenden Eigenschaften verwenden, da Sie schnellere Kalenderabfragen unterstützen.
  
### <a name="recurrence-blob-properties"></a>Serien-BLOB-Eigenschaften
  
- MapiStartTime
    
- MapiEndTime
    
- SubjectPrefixInternal
    
- NormalizedSubjectInternal
    
- MapiSubject
    
- Standort
    
- AppointmentColor
    
- MapiIsAllDayEvent
    
- MapiHasAttachment
    
- FreeBusyStatus
    
- ReminderIsSetInternal
    
- ReminderMinutesBeforeStartInternal
    
- AppointmentState
    
- AllAttachmentsHidden
    
- ChangeHighlight
    
### <a name="calculated-from-the-primary-recurrence-blob-or-master"></a>Berechnet aus dem primären Serien-BLOB oder-Stamm
  
- ItemId
    
- IsRecurring
    
- Isexception
    
- AppointmentRecurring
    
- MapiStartTime
    
- MapiPRStartDate
    
- MapiEndTime
    
- MapiPREndDate
    
- CalendarItemType
    
- GlobalObjectId
    
- TimeZoneDefinitionStart
    
- TimeZoneDefinitionEnd
    
### <a name="master-calendar-item-properties"></a>Eigenschaften des Master Kalenderelements
  
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
    
- Isexception
    
- IsRecurring
    
- MapiSensitivity
    
- ContainerClass
    
- MapiPRStartDate
    
- MapiPREndDate
    
- Kategorien
    
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt eine FindItem-Anforderung. Bei einer erfolgreichen Anforderung wird eine Antwort zurückgegeben, die Kalenderelemente enthält, die in 2006-05-18T00:00:00-08:00 oder nach gestartet und vor 2006-05-19T00:00:00-08:00-beendet wurden.
  
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
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [FindItem-Vorgang](finditem-operation.md)
- [Suchen von Elementen](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

