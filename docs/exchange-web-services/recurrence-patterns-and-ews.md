---
title: Serienmuster und EWS
manager: luken
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: fd9ef706-1e01-49fa-af6f-2f6d3e173c16
description: Informationen Sie zu Serienmuster und sich wiederholenden Reihe im Exchange ein.
ms.openlocfilehash: ac10e9b9a347abb5907b77f0e0e7315e4e86d97a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757128"
---
# <a name="recurrence-patterns-and-ews"></a>Serienmuster und EWS

Informationen Sie zu Serienmuster und sich wiederholenden Reihe im Exchange ein.
  
Eine Terminserie ist ein Termin oder eine Besprechung, die nach einem definierten Muster wiederholt. Eine Terminserie kann entweder eine bestimmte Anzahl von Vorkommen oder kann auf unbestimmte Zeit wiederholen. Darüber hinaus kann sich wiederholenden Reihe Ausnahmen verfügen, die folgen nicht das Muster der restlichen vorkommen, und kann vorkommen, die aus dem Muster gelöscht wurden aufweisen. Die EWS Managed API und EWS können sich wiederholenden Reihe und deren zugeordneten Kalenderelemente entwickelt.
  
## <a name="recurring-calendar-items"></a>Wiederkehrende Kalenderelemente

Alle Elemente im Kalender werden in der folgenden vier Kategorien unterteilt:
  
- Nicht wiederkehrende Kalenderelemente
    
- Wiederkehrende Master-Shapes
    
- Vorkommen in einer Reihe
    
- Geänderte Vorkommen in einer Reihe, bezeichnet als Ausnahmen
    
In diesem Artikel werden die drei Typen von Kalenderelementen betrachten wir, die Teil einer Serie sind.
  
Es ist hilfreich, zu verstehen, wie sich wiederholenden Reihe implementiert werden, auf dem Exchange-Server. Anstatt für jedes Vorkommen einer separaten separate Element in einer Terminserie zu erstellen, erstellt der Server nur ein Element im Kalender als wiederkehrenden Master bezeichnet. Das Format eines sich wiederholenden Master ist ein Termin nicht wiederkehrende durch die hinzugefügte Muster Serieninformationen sehr ähnlich. Der Server generiert dann basierende auf das Serienmuster als Antwort auf Clientanforderungen für Informationen zum Kalendertermin, unter Verwendung der sogenannten Erweiterung vorkommen. Diese generierten Vorkommen werden auf dem Server nicht dauerhaft gespeichert. Dies ist wichtig zu verstehen, da die Möglichkeit, die Sie für Kalenderelemente suchen bestimmt, welche Informationen Sie erhalten und gibt an, ob die Erweiterung erfolgt.
  
## <a name="recurrence-patterns"></a>Serienmuster

Die Hauptinformationen in einer Terminserie, die Erweiterung ermöglicht ist das Serienmuster. Das Serienmuster gefunden wird, auf dem sich wiederholenden Master und beschreibt einen Satz von Kriterien für die Berechnung basierend auf Datum und Uhrzeit des wiederkehrenden Master vorkommen.
  
**In Tabelle 1. Serienmuster verfügbar**

|**Verwaltete EWS-API-Klasse**|**EWS-Element**|**Beispiele**|
|:-----|:-----|:-----|
|[Recurrence.DailyPattern](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.recurrence.dailypattern%28v=exchg.80%29.aspx) <br/> |[DailyRecurrence](http://msdn.microsoft.com/library/0aaf265d-b723-49c6-8e9c-9ba60141e9ab%28Office.15%29.aspx) <br/> |Wiederholen Sie täglich aus.  <br/> Wiederholen Sie jeden zweiten Tag.  <br/> |
|[Recurrence.MonthlyPattern](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.recurrence.monthlypattern%28v=exchg.80%29.aspx) <br/> |[AbsoluteMonthlyRecurrence](http://msdn.microsoft.com/library/178fa0ae-9dfc-417f-933c-d657d31c2161%28Office.15%29.aspx) <br/> |Wiederholen Sie jeden Monat am zehnten Tag des Monats.  <br/> Wiederholen Sie alle zwei Monate am zwanzig ersten Tag des Monats.  <br/> |
|[Recurrence.RelativeMonthlyPattern](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.recurrence.relativemonthlypattern%28v=exchg.80%29.aspx) <br/> |[RelativeMonthlyRecurrence](http://msdn.microsoft.com/library/a76595db-7460-44ac-ac2a-53241caa33a7%28Office.15%29.aspx) <br/> |Wiederholen Sie die am zweiten Dienstag des Monats.  <br/> Wiederholen Sie die dem dritten Donnerstag des Monats alle drei Monate.  <br/> |
|[Recurrence.RelativeYearlyPattern](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.recurrence.relativeyearlypattern%28v=exchg.80%29.aspx) <br/> |[RelativeYearlyRecurrence](http://msdn.microsoft.com/library/25b67876-9979-4a30-a637-357ea10a93b8%28Office.15%29.aspx) <br/> |Wiederholen Sie am ersten Montag August jedes Jahr.  <br/> |
|[Recurrence.WeeklyPattern](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.recurrence.weeklypattern%28v=exchg.80%29.aspx) <br/> |[WeeklyRecurrence](http://msdn.microsoft.com/library/69c41dd5-597c-45bc-be3f-e2f2b5615aa3%28Office.15%29.aspx) <br/> |Wiederholen Sie jeden Montag.  <br/> Wiederholen Sie jeden Dienstag und Donnerstag alle zwei Wochen.  <br/> |
|[Recurrence.YearlyPattern](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.recurrence.yearlypattern%28v=exchg.80%29.aspx) <br/> |[AbsoluteYearlyRecurrence](http://msdn.microsoft.com/library/96f53e2c-3893-4f6e-a78a-ac179f45c5db%28Office.15%29.aspx) <br/> |Wiederholen Sie am 1. September jedes Jahr.  <br/> |
   
Der andere wichtige Informationen für ein Serienmuster ist, wenn das Serienmuster endet. Dies kann als eine festgelegte Anzahl von vorkommen, als ein Enddatum oder dass kein Ende ausgedrückt werden.
  
**In Tabelle 2. Optionen für das Ende einer Terminserie**

|**EWS Managed API-Methode /-Eigenschaft**|**EWS-Element**|**Beschreibung**|
|:-----|:-----|:-----|
|[Recurrence.NumberOfOccurrences](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.recurrence.numberofoccurrences%28v=exchg.80%29.aspx) <br/> |[NumberedRecurrence](http://msdn.microsoft.com/library/53746909-ef21-4764-8715-a7769b943cca%28Office.15%29.aspx) <br/> |Der Wert dieser Eigenschaft oder eines Elements gibt die Anzahl von vorkommen.  <br/> |
|[Recurrence.EndDate](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.recurrence.enddate%28v=exchg.80%29.aspx) <br/> |[EndDateRecurrence](http://msdn.microsoft.com/library/a5ee2504-db84-49ee-870c-cca9269f2e26%28Office.15%29.aspx) <br/> |Das letzte Vorkommen in der Datenreihe liegt am oder vor dem angegebenen Datum die durch diese Eigenschaft oder eines Elements.  <br/> |
|[Recurrence.HasEnd](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.recurrence.hasend%28v=exchg.80%29.aspx) <br/> [Recurrence.NeverEnds](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.recurrence.neverends%28v=exchg.80%29.aspx) <br/> |[NoEndRecurrence](http://msdn.microsoft.com/library/ab2ebd9c-388e-45f1-abf9-56e293ef123b%28Office.15%29.aspx) <br/> |Die Datenreihe, weist kein Ende.  <br/> |
   
## <a name="expanded-vs-non-expanded-views"></a>Im Vergleich zu Ansichten nicht erweiterten erweitert

Verwendung der **FindAppointments** -Methode in die EWS Managed API (oder mit einem **CalendarView** -Element im EWS-Vorgangs **FindItem** ) Ruft den Erweiterungsprozess. Dies Blendet master Terminserien aus dem Ergebnissatz und stattdessen stellt eine erweiterte Ansicht dieser Serie. Vorkommen und Ausnahmen auf der sich wiederholenden Master, die in die Parameter der Kalenderansicht fallen sind im Resultset enthalten. Dagegen mithilfe der **FindItems** -Methode in die EWS Managed API (oder die Operation **FindItem** mit einem **IndexedPageItemView** oder **FractionalPageItemView** -Element im EWS) wird keine aufgerufen Erweiterung Prozesses und der Vorkommen und Ausnahmen sind nicht enthalten. Sehen wir uns ein Beispiel für die beiden Methoden verglichen. 
  
**Tabelle 3. Methoden und Vorgänge für die Suche nach Terminen**

|**EWS Managed API-Methode**|**EWS-Vorgang**|**Erweitert die Datenreihe?**|**Elemente, die in Suchergebnissen enthalten**|
|:-----|:-----|:-----|:-----|
|[ExchangeService.FindAppointments](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx) <br/> |[FindItem Vorgang](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) mit einem [CalendarView](http://msdn.microsoft.com/library/a4a953b8-0710-416c-95ef-59e51eba9982%28Office.15%29.aspx) -element  <br/> |Ja  <br/> |Nicht wiederkehrende Termine einzelnen Vorkommen von sich wiederholenden Reihe und Ausnahmen von sich wiederholenden Reihe  <br/> |
|[ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) <br/> |[FindItem Vorgang](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) mit einer [IndexedPageItemView](http://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) Element oder [FractionalPageItemView](http://msdn.microsoft.com/library/4111afec-35e7-4c6f-b291-9bbba603f633%28Office.15%29.aspx) -element  <br/> |Nein  <br/> |Nicht wiederkehrende Termine und Terminserien Master-Shape  <br/> |
   
Sadie hat sich ihr Son bei schwimmen Team gerade angemeldet. Das Team weist Practice jeden Mittwoch Morgen um 8:30 Uhr, beginnend mit der letzten Practice wird am 6. August 2. Juli. Nicht möchte, praktischen vergessen, fügt Sadie eine Terminserie auf ihren Kalender aus, um ihn zu erinnern.
  
**In Tabelle 4. Terminserie des Sadie**

|**Termin dar**|**Wert**|
|:-----|:-----|
|Subject  <br/> |Schwimmen Team-Methode  <br/> |
|Beginn  <br/> |2 Juli 2014 8:30 Uhr ausgeführt.  <br/> |
|Ende  <br/> |2 Juli 2014 10:00 Uhr  <br/> |
|Wiederholt  <br/> |Jeden Mittwoch  <br/> |
|Letzte Vorkommen  <br/> |6 August 2014 8:30 Uhr ausgeführt.  <br/> |
   
Ein schnellen Blick auf einen Kalender zeigt, dass das Team insgesamt sechs Methoden hat. Jedoch keine sechs verschiedene Terminelemente vorhanden sind, im Kalender. Stattdessen wird nur ein Master-Shape Terminserie, der Datenreihe darstellt.
  
Jetzt sehen wir uns finden von Terminen Sadie Kalender, die innerhalb des Monats Juli auftreten. Im folgenden Codebeispiel wird verwendet die **FindItems** -Methode in der Exchange-Managed-API zum Erstellen einer nicht erweiterten Ansicht des Sadies Kalenders. 
  
```cs
PropertySet propSet = new PropertySet(AppointmentSchema.Subject,
                                      AppointmentSchema.Location,
                                      AppointmentSchema.Start, 
                                      AppointmentSchema.End,
                                      AppointmentSchema.AppointmentType);
#region FindItems + ItemView method
ItemView itemView = new ItemView(100);
itemView.PropertySet = propSet;
List<SearchFilter> filterList = new List<SearchFilter>();
// Find appointments that start after midnight on July 1, 2014.
SearchFilter.IsGreaterThan startFilter = new SearchFilter.IsGreaterThan(AppointmentSchema.Start,
    new DateTime(2014, 7, 1));
// Find appointments that end before midnight on July 31, 2014
SearchFilter.IsLessThan endFilter = new SearchFilter.IsLessThan(AppointmentSchema.End,
    new DateTime(2014, 7, 31));
filterList.Add(startFilter);
filterList.Add(endFilter);
SearchFilter.SearchFilterCollection calendarFilter = new SearchFilter.SearchFilterCollection(LogicalOperator.And, filterList);
// This results in a call to EWS.
FindItemsResults<Item> results = service.FindItems(WellKnownFolderName.Calendar, calendarFilter, itemView);
foreach(Item appt in results.Items)
{
    Console.WriteLine(appt.Subject);
}
```

Dieser Code führt die folgenden [FindItem Vorgang](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) -Anforderung mit einem [IndexedPageItemView](http://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) -Element. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Pacific Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:FindItem Traversal="Shallow">
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
          <t:FieldURI FieldURI="calendar:Location" />
          <t:FieldURI FieldURI="calendar:Start" />
          <t:FieldURI FieldURI="calendar:End" />
          <t:FieldURI FieldURI="calendar:CalendarItemType" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:IndexedPageItemView MaxEntriesReturned="100" Offset="0" BasePoint="Beginning" />
      <m:Restriction>
        <t:And>
          <t:IsGreaterThan>
            <t:FieldURI FieldURI="calendar:Start" />
            <t:FieldURIOrConstant>
              <t:Constant Value="2014-07-01T07:00:00.000Z" />
            </t:FieldURIOrConstant>
          </t:IsGreaterThan>
          <t:IsLessThan>
            <t:FieldURI FieldURI="calendar:End" />
            <t:FieldURIOrConstant>
              <t:Constant Value="2014-07-31T07:00:00.000Z" />
            </t:FieldURIOrConstant>
          </t:IsLessThan>
        </t:And>
      </m:Restriction>
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="calendar" />
      </m:ParentFolderIds>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

Die Antwort des Servers enthält nur ein einzelnes Element, das sich wiederholenden Master-Shape, von dem Elementwert [CalendarItemType](http://msdn.microsoft.com/library/1feb0788-adf7-4a7c-830c-005214ad930f%28Office.15%29.aspx) des **RecurringMaster**angegeben. Der Wert des Elements [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) wurde zur besseren Lesbarkeit gekürzt. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="939" MinorBuildNumber="16" Version="V2_11" 
        xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="1" TotalItemsInView="1" IncludesLastItemInRange="true">
            <t:Items>
              <t:CalendarItem>
                <t:ItemId Id="AAMkADA5..." ChangeKey="DwAAABYA..." />
                <t:Subject>Swim Team Practice</t:Subject>
                <t:Start>2014-07-02T15:30:00Z</t:Start>
                <t:End>2014-07-02T17:00:00Z</t:End>
                <t:Location>Neighborhood Swimming Pool</t:Location>
                <t:CalendarItemType>RecurringMaster</t:CalendarItemType>
              </t:CalendarItem>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>
```

Jetzt Vergleichen wir mit einer erweiterten Ansicht. Im folgenden Codebeispiel wird die **FindAppointments** -Methode in die EWS Managed API zum Erstellen einer erweiterten Ansicht Sadies Kalenders verwendet. 
  
```cs
PropertySet propSet = new PropertySet(AppointmentSchema.Subject,
                                      AppointmentSchema.Location,
                                      AppointmentSchema.Start, 
                                      AppointmentSchema.End,
                                      AppointmentSchema.AppointmentType);
CalendarView calView = new CalendarView(new DateTime(2014, 7, 1),
    new DateTime(2014, 7, 31));
calView.PropertySet = propSet;
FindItemsResults<Appointment> results = service.FindAppointments(WellKnownFolderName.Calendar, calView);
foreach(Appointment appt in results.Items)
{
    Console.WriteLine(appt.Subject);
}
```

Dieser Code führt die folgenden [FindItem Vorgang](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) -Anforderung mit einem [CalendarView](http://msdn.microsoft.com/library/a4a953b8-0710-416c-95ef-59e51eba9982%28Office.15%29.aspx) -Element. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Pacific Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:FindItem Traversal="Shallow">
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
          <t:FieldURI FieldURI="calendar:Location" />
          <t:FieldURI FieldURI="calendar:Start" />
          <t:FieldURI FieldURI="calendar:End" />
          <t:FieldURI FieldURI="calendar:CalendarItemType" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:CalendarView StartDate="2014-07-01T07:00:00.000Z" EndDate="2014-07-31T07:00:00.000Z" />
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="calendar" />
      </m:ParentFolderIds>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

Diesmal enthält die Antwort vom Server fünf vorkommen, einen für jeden Mittwoch im Juli. Auf diese Elemente, die alle Elemente [CalendarItemType](http://msdn.microsoft.com/library/1feb0788-adf7-4a7c-830c-005214ad930f%28Office.15%29.aspx) aufweisen Wert **Vorkommen**. Beachten Sie, dass das wiederkehrende Master-Shape nicht in der Antwort vorhanden ist. Die Werte der [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) Elemente wurden zur besseren Lesbarkeit gekürzt. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="939" MinorBuildNumber="16" Version="V2_11" 
        xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder TotalItemsInView="5" IncludesLastItemInRange="true">
            <t:Items>
              <t:CalendarItem>
                <t:ItemId Id="AAMkADA6..." ChangeKey="DwAAABYA..." />
                <t:Subject>Swim Team Practice</t:Subject>
                <t:Start>2014-07-02T15:30:00Z</t:Start>
                <t:End>2014-07-02T17:00:00Z</t:End>
                <t:Location>Neighborhood Swimming Pool</t:Location>
                <t:CalendarItemType>Occurrence</t:CalendarItemType>
              </t:CalendarItem>
              <t:CalendarItem>
                <t:ItemId Id="AAMkADA7..." ChangeKey="DwAAABYA..." />
                <t:Subject>Swim Team Practice</t:Subject>
                <t:Start>2014-07-09T15:30:00Z</t:Start>
                <t:End>2014-07-09T17:00:00Z</t:End>
                <t:Location>Neighborhood Swimming Pool</t:Location>
                <t:CalendarItemType>Occurrence</t:CalendarItemType>
              </t:CalendarItem>
              <t:CalendarItem>
                <t:ItemId Id="AAMkADA8..." ChangeKey="DwAAABYA..." />
                <t:Subject>Swim Team Practice</t:Subject>
                <t:Start>2014-07-16T15:30:00Z</t:Start>
                <t:End>2014-07-16T17:00:00Z</t:End>
                <t:Location>Neighborhood Swimming Pool</t:Location>
                <t:CalendarItemType>Occurrence</t:CalendarItemType>
              </t:CalendarItem>
              <t:CalendarItem>
                <t:ItemId Id="AAMkADA9..." ChangeKey="DwAAABYA..." />
                <t:Subject>Swim Team Practice</t:Subject>
                <t:Start>2014-07-23T15:30:00Z</t:Start>
                <t:End>2014-07-23T17:00:00Z</t:End>
                <t:Location>Neighborhood Swimming Pool</t:Location>
                <t:CalendarItemType>Occurrence</t:CalendarItemType>
              </t:CalendarItem>
              <t:CalendarItem>
                <t:ItemId Id="AAMkADAA..." ChangeKey="DwAAABYA..." />
                <t:Subject>Swim Team Practice</t:Subject>
                <t:Start>2014-07-30T15:30:00Z</t:Start>
                <t:End>2014-07-30T17:00:00Z</t:End>
                <t:Location>Neighborhood Swimming Pool</t:Location>
                <t:CalendarItemType>Occurrence</t:CalendarItemType>
              </t:CalendarItem>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>
```

Nachdem Sie ein wiederkehrendes Master-Shape, das Auftreten eines Serientermins oder eine Ausnahme haben, können Sie immer für [die anderen verwandten Elemente abzurufen](how-to-access-a-recurring-series-by-using-ews-in-exchange.md). Sie können erhält ein Vorkommen oder eine Ausnahmebedingung, das sich wiederholenden Master-Shape abrufen und umgekehrt.
  
## <a name="working-with-recurring-calendar-items"></a>Arbeiten mit sich wiederholenden Kalenderelementen (engl.)

Sie verwenden die gleichen Methoden und Vorgänge sich wiederholenden Reihe entwickelt, wie Sie verwenden, um eine nicht wiederkehrende Kalenderelemente entwickelt. Der Unterschied besteht darin, je nach dem Element, das Sie verwenden, um das Aufrufen von Methoden oder Vorgänge, die Aktionen, mit denen Sie auf die gesamte Datenreihe oder nur ein einzelnes Vorkommen anwenden können. [Aktionen, die für die periodische Master](how-to-update-a-recurring-series-by-using-ews-in-exchange.md) gilt für alle Vorkommen in der Datenreihe während [Aktionen, um ein einzelnes Vorkommen oder eine Ausnahme](how-to-update-a-recurring-series-by-using-ews.md) nur diese Vorkommen oder Ausnahme zugewiesen wird. 
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

- [Zugriff auf eine Terminserie mithilfe von EWS in Exchange](how-to-access-a-recurring-series-by-using-ews-in-exchange.md)
    
- [Erstellen einer Terminserie mithilfe der EWS in Exchange](how-to-create-a-recurring-series-by-using-ews-in-exchange.md)
    
- [Löschen der Termine in einer Terminserie mithilfe der EWS in Exchange](how-to-delete-appointments-in-a-recurring-series-by-using-ews-in-exchange.md)
    
- [Aktualisieren einer Terminserie mithilfe der Exchange-Webdienste](how-to-update-a-recurring-series-by-using-ews.md)
    
- [Aktualisieren einer Terminserie mithilfe der EWS in Exchange](how-to-update-a-recurring-series-by-using-ews-in-exchange.md)
    
## <a name="see-also"></a>Siehe auch


- [Kalender und EWS in Exchange](calendars-and-ews-in-exchange.md)
    
- [Entwickeln von Webdienstclients für Exchange](develop-web-service-clients-for-exchange.md)
    
- [Abrufen von Terminen und Besprechungen mithilfe von EWS in Exchange](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md)
    

