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
description: Das CalendarView-Element definiert einen Vorgang FindItem als Kalenderelemente in einem Satz zurückgeben, wenn sie in einem Kalender angezeigt werden.
ms.openlocfilehash: 79b5ad268a8013092c1122c99bdcd10d876abf2c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757543"
---
# <a name="calendarview"></a>CalendarView

Das **CalendarView** -Element definiert einen [Vorgang FindItem](finditem-operation.md) als Kalenderelemente in einem Satz zurückgeben, wenn sie in einem Kalender angezeigt werden. 
  
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
|**"MaxEntriesReturned"** <br/> |Beschreibt die maximale Anzahl der in der Antwort FindItem zurückzugebender Ergebnisse an.  <br/> |
|**StartDate** <br/> |Identifiziert den Anfang einer bestimmten Zeitspanne für Kalenderelemente abgefragt. Alle Kalenderelemente, die eine Endzeit verfügen, bevor **StartDate** nicht zurückgegeben werden. Der Wert der **StartDate** angegeben werden kann, in koordinierter Weltzeit (UTC) Format, z. B. 2006-01-02T12:00:00Z, oder in einem Format, in dem Ortszeit sowie zur Zeitzone Offset, wie in 2006 angegeben ist-01-02T04:00:00-08:00.  <br/><br/>Dieses Attribut ist erforderlich.  <br/> |
|**EndDate** <br/> |Bezeichnet das Ende einer bestimmten Zeitspanne für Kalenderelemente abgefragt. Alle Elemente im Kalender, die eine Startzeit aufweisen, die am oder nach dem **EndDate** ist werden nicht zurückgegeben. Der Wert der **EndDate** angegeben werden kann, im UTC-Format, wie in 2006-02-02T12:00:00Z, oder in einem Format, in dem Ortszeit sowie zur Zeitzone Offset, wie in 2006 angegeben ist-02-02T04:00:00-08:00.  <br/><br/>**EndDate** muss größer als oder gleich **"StartDate"** sein. Andernfalls wird ein Fehler zurückgegeben. Dieses Attribut ist erforderlich.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FindItem](finditem.md) <br/> |Definiert eine Anforderung zum Suchen von Elementen in einem Postfach an.<br/><br/> Es folgt der XPath-Ausdruck, der dieses Element:  <br/>  `/FindItem` <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn das **CalendarView** -Element in einer Anforderung FindItem angegeben ist, wird eine Liste der einzelnen Kalenderelemente und Vorkommen des wiederkehrende Kalenderelemente innerhalb des Bereichs **StartDate** und **EndDate**angegeben wird von der Webdienst zurückgegeben.
  
Wenn das **CalendarView** -Element in einer Anforderung FindItem nicht angegeben ist, gibt der Webdienst eine Liste der einzelnen Kalenderelemente und wiederkehrende Kalenderelemente Master-Shape zurück. Kalender Vorkommen eines sich wiederholenden Kalenderelements werden nicht erweitert. 
  
CalendarView Abfragen sollten nur vornehmen der folgenden Eigenschaften verwendet werden, da sie schnellere Kalenderabfragen unterstützen.
  
### <a name="recurrence-blob-properties"></a>Serie BLOB-Eigenschaften
  
- MapiStartTime
    
- MapiEndTime
    
- SubjectPrefixInternal
    
- NormalizedSubjectInternal
    
- MapiSubject
    
- Speicherort
    
- AppointmentColor
    
- MapiIsAllDayEvent
    
- MapiHasAttachment
    
- FreeBusyStatus
    
- ReminderIsSetInternal
    
- ReminderMinutesBeforeStartInternal
    
- AppointmentState
    
- AllAttachmentsHidden
    
- ChangeHighlight
    
### <a name="calculated-from-the-primary-recurrence-blob-or-master"></a>Aus dem primären Serienblob oder Master-Shape berechnet
  
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
    
### <a name="master-calendar-item-properties"></a>Elementeigenschaften Master Kalender
  
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
    
- Kategorien
    
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt eine FindItem-Anforderung. Eine erfolgreiche Anforderung gibt eine Antwort mit Kalenderelementen (engl.), die Schritte unter 2006-05-18T00:00:00-08:00 oder nach und beendeten vor dem 2006-05-19T00:00:00-08:00.
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindItem Traversal="Shallow" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [FindItem-Vorgang](finditem-operation.md)
- [Finding Items](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

