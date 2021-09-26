---
title: Serienmuster und EWS
manager: luken
ms.date: 03/9/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: fd9ef706-1e01-49fa-af6f-2f6d3e173c16
description: Erfahren Sie mehr über Serienmuster und Serienserien in Exchange.
ms.openlocfilehash: fcd6cf847efedd3bc48a26ad7866a0221de59371
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59541588"
---
# <a name="recurrence-patterns-and-ews"></a>Serienmuster und EWS

Erfahren Sie mehr über Serienmuster und Serienserien in Exchange.
  
Eine Terminserie ist ein Termin oder eine Besprechung, die gemäß einem definierten Muster wiederholt wird. Eine Terminserie kann entweder eine bestimmte Anzahl von Vorkommen aufweisen oder beliebig oft wiederholt werden. Darüber hinaus kann eine Terminserie Ausnahmen aufweisen, die nicht dem Muster der restlichen Vorkommen folgen, und vorkommen können, die aus dem Muster gelöscht wurden. Sie können die verwaltete EWS-API und EWS verwenden, um mit Terminserien und den zugehörigen Kalenderelementen zu arbeiten.
  
## <a name="recurring-calendar-items"></a>Wiederkehrende Kalenderelemente

Alle Kalenderelemente werden in eine der folgenden vier Kategorien unterteilt:
  
- Nicht wiederkehrende Kalenderelemente
    
- Serienmaster
    
- Vorkommen in einer Datenreihe
    
- Geänderte Vorkommen in einer Datenreihe, die als Ausnahmen bezeichnet werden
    
In diesem Artikel werden die drei Arten von Kalenderelementen behandelt, die Teil einer Terminserie sind.
  
Es ist hilfreich zu verstehen, wie Serienserien auf dem Exchange-Server implementiert werden. Anstatt für jedes Vorkommen in einer Terminserie ein eigenes Element zu erstellen, erstellt der Server nur ein tatsächliches Element im Kalender, das als Serienmaster bezeichnet wird. Das Format eines Serienmasters ist mit dem Hinzufügen von Serienmusterinformationen einem Nichtserientermin sehr ähnlich. Der Server generiert dann Vorkommen basierend auf dem Serienmuster als Reaktion auf Clientanforderungen für Termininformationen mithilfe eines Prozesses namens Erweiterung. Diese generierten Vorkommen werden nicht dauerhaft auf dem Server gespeichert. Dies ist wichtig zu verstehen, da die Art und Weise, wie Sie nach Kalenderelementen suchen, bestimmt, welche Informationen Sie erhalten und ob eine Erweiterung erfolgt.
  
## <a name="recurrence-patterns"></a>Serienmuster

Der Schlüssel zu einer Serienserie, die eine Erweiterung ermöglicht, ist das Serienmuster. Das Serienmuster befindet sich im Serienmaster und beschreibt eine Reihe von Kriterien für die Berechnung von Vorkommen basierend auf dem Datum und der Uhrzeit des Serienmasters.
  
**Tabelle 1. Verfügbare Serienmuster**

|**Verwaltete EWS-API-Klasse**|**EWS-Element**|**Beispiele**|
|:-----|:-----|:-----|
|[Recurrence.DailyPattern](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.dailypattern%28v=exchg.80%29.aspx) <br/> |[DailyRecurrence](https://msdn.microsoft.com/library/0aaf265d-b723-49c6-8e9c-9ba60141e9ab%28Office.15%29.aspx) <br/> |Jeden Tag wiederholen.  <br/> Jeden zweiten Tag wiederholen.  <br/> |
|[Recurrence.MonthlyPattern](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.monthlypattern%28v=exchg.80%29.aspx) <br/> |[AbsoluteMonthlyRecurrence](https://msdn.microsoft.com/library/178fa0ae-9dfc-417f-933c-d657d31c2161%28Office.15%29.aspx) <br/> |Jeden Monat am zehnten Tag des Monats wiederholen.  <br/> Wiederholen Sie jeden zweiten Monat am 21. Tag des Monats.  <br/> |
|[Recurrence.RelativeMonthlyPattern](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.relativemonthlypattern%28v=exchg.80%29.aspx) <br/> |[RelativeMonthlyRecurrence](https://msdn.microsoft.com/library/a76595db-7460-44ac-ac2a-53241caa33a7%28Office.15%29.aspx) <br/> |Wiederholen Sie diese Am zweiten Dienstag jeden Monats.  <br/> Wiederholen Sie den Vorgang alle drei Monate am dritten Donnerstag des Monats.  <br/> |
|[Recurrence.RelativeYearlyPattern](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.relativeyearlypattern%28v=exchg.80%29.aspx) <br/> |[RelativeYearlyRecurrence](https://msdn.microsoft.com/library/25b67876-9979-4a30-a637-357ea10a93b8%28Office.15%29.aspx) <br/> |Jedes Jahr am ersten Montag im August wiederholen.  <br/> |
|[Recurrence.WeeklyPattern](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.weeklypattern%28v=exchg.80%29.aspx) <br/> |[WeeklyRecurrence](https://msdn.microsoft.com/library/69c41dd5-597c-45bc-be3f-e2f2b5615aa3%28Office.15%29.aspx) <br/> |Jeden Montag wiederholen.  <br/> Jeden Dienstag und Donnerstag alle zwei Wochen wiederholen.  <br/> |
|[Recurrence.YearlyPattern](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.yearlypattern%28v=exchg.80%29.aspx) <br/> |[AbsoluteYearlyRecurrence](https://msdn.microsoft.com/library/96f53e2c-3893-4f6e-a78a-ac179f45c5db%28Office.15%29.aspx) <br/> |Jedes Jahr am 1. September wiederholen.  <br/> |
   
Die anderen wichtigen Informationen für ein Serienmuster sind das Ende der Serie. Dies kann entweder als festgelegte Anzahl von Vorkommen, als Enddatum oder als Enddatum ausgedrückt werden.
  
**Tabelle 2. Optionen für das Ende einer Terminserie**

|**Verwaltete EWS-API-Methode/-Eigenschaft**|**EWS-Element**|**Beschreibung**|
|:-----|:-----|:-----|
|[Recurrence.NumberOfOccurrences](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.numberofoccurrences%28v=exchg.80%29.aspx) <br/> |[NumberedRecurrence](https://msdn.microsoft.com/library/53746909-ef21-4764-8715-a7769b943cca%28Office.15%29.aspx) <br/> |Der Wert dieser Eigenschaft oder dieses Elements gibt die Anzahl der Vorkommen an.  <br/> |
|[Recurrence.EndDate](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.enddate%28v=exchg.80%29.aspx) <br/> |[EndDateRecurrence](https://msdn.microsoft.com/library/a5ee2504-db84-49ee-870c-cca9269f2e26%28Office.15%29.aspx) <br/> |Das letzte Vorkommen in der Datenreihe fällt auf oder vor das durch diese Eigenschaft oder dieses Element angegebene Datum.  <br/> |
|[Recurrence.HasEnd](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.hasend%28v=exchg.80%29.aspx) <br/> [Recurrence.NeverEnds](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.recurrence.neverends%28v=exchg.80%29.aspx) <br/> |[NoEndRecurrence](https://msdn.microsoft.com/library/ab2ebd9c-388e-45f1-abf9-56e293ef123b%28Office.15%29.aspx) <br/> |Die Datenreihe hat kein Ende.  <br/> |
   
## <a name="expanded-vs-non-expanded-views"></a>Erweiterte ansichten im Vergleich zu nicht erweiterten Ansichten

Mithilfe der **FindAppointments-Methode** in der verwalteten EWS-API (oder dem **FindItem-Vorgang** mit einem **CalendarView-Element** in EWS) wird der Erweiterungsprozess aufgerufen. Dadurch werden Terminserien aus dem Resultset ausgeblendet und stattdessen eine erweiterte Ansicht dieser Terminserie angezeigt. Vorkommen von und Ausnahmen für das wiederkehrende Master-Shape, die in die Parameter der Kalenderansicht fallen, sind im Resultset enthalten. Umgekehrt ruft die Verwendung der **FindItems-Methode** in der verwalteten EWS-API (oder der **FindItem-Vorgang** mit einem **IndexedPageItemView-** oder **FractionalPageItemView-Element** in EWS) den Erweiterungsprozess nicht auf, und Vorkommen und Ausnahmen sind nicht enthalten. Sehen wir uns ein Beispiel an, in dem die beiden Methoden verglichen werden. 
  
**Tabelle 3. Methoden und Vorgänge zum Suchen von Terminen**

|**EWS Managed API-Methode**|**EWS-Vorgang**|**Erweitert Serie?**|**Elemente, die in den Ergebnissen enthalten sind**|
|:-----|:-----|:-----|:-----|
|[ExchangeService.FindAppointments](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx) <br/> |[FindItem-Vorgang](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) mit einem [CalendarView-Element](https://msdn.microsoft.com/library/a4a953b8-0710-416c-95ef-59e51eba9982%28Office.15%29.aspx)  <br/> |Ja  <br/> |Terminserien, einzelne Vorkommen von Terminserien und Ausnahmen von Terminserien  <br/> |
|[ExchangeService.FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) <br/> |[FindItem-Vorgang](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) mit einem [IndexedPageItemView-Element](https://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) oder [fractionalPageItemView-Element](https://msdn.microsoft.com/library/4111afec-35e7-4c6f-b291-9bbba603f633%28Office.15%29.aspx)  <br/> |Nein  <br/> |Terminserien und Terminserien  <br/> |
   
Sadie hat soeben ihren Son für das Team der Geschäftsleitung angemeldet. Das Team trainiert jeden Mittwoch um 08:30 Uhr, beginnend am 2. Juli, mit der letzten Übung am 6. August. Sadie möchte die Praxis nicht vergessen und fügt ihrem Kalender eine Terminserie hinzu, um sie zu erinnern.
  
**Tabelle 4. Sadies Terminserie**

|**Terminfeld**|**Wert**|
|:-----|:-----|
|Betreff  <br/> |Team-Übung "Team trainieren"  <br/> |
|Start  <br/> |2. Juli 2014 08:30 Uhr  <br/> |
|Ende  <br/> |2. Juli 2014 10:00 Uhr  <br/> |
|Wiederholt  <br/> |Jeden Mittwoch  <br/> |
|Letztes Vorkommen  <br/> |6. August 2014 08:30 Uhr  <br/> |
   
Ein kurzer Blick auf einen Kalender zeigt, dass das Team insgesamt sechs Methoden hat. Es gibt jedoch keine sechs unterschiedlichen Terminelemente im Kalender. Stattdessen gibt es nur einen Terminserienmaster, der die Serie darstellt.
  
Sehen wir uns nun die Suche nach Terminen in Sadies Kalender an, die innerhalb des Monats Juli stattfinden. Im folgenden Codebeispiel wird die **FindItems-Methode** in der Exchange Managed API verwendet, um eine nicht erweiterte Ansicht von Sadies Kalender zu erstellen. 
  
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

Dieser Code führt zu der folgenden [FindItem-Vorgangsanforderung](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) mit einem [IndexedPageItemView-Element.](https://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

Die Antwort des Servers enthält nur ein einzelnes Element, den Serienmaster, der durch den [CalendarItemType-Elementwert](https://msdn.microsoft.com/library/1feb0788-adf7-4a7c-830c-005214ad930f%28Office.15%29.aspx) von **RecurringMaster** angegeben wird. Der Wert des [ItemId-Elements](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) wurde zur besseren Lesbarkeit gekürzt. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="939" MinorBuildNumber="16" Version="V2_11" 
        xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

Vergleichen wir nun mit einer erweiterten Ansicht. Im folgenden Codebeispiel wird die **FindAppointments-Methode** in der verwalteten EWS-API verwendet, um eine erweiterte Ansicht des Sadie-Kalenders zu erstellen. 
  
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

Dieser Code führt zu der folgenden [FindItem-Vorgangsanforderung](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) mit einem [CalendarView-Element.](https://msdn.microsoft.com/library/a4a953b8-0710-416c-95ef-59e51eba9982%28Office.15%29.aspx) 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

Dieses Mal enthält die Serverantwort fünf Vorkommen, eines für jeden Mittwoch im Juli. Die [CalendarItemType-Elemente](https://msdn.microsoft.com/library/1feb0788-adf7-4a7c-830c-005214ad930f%28Office.15%29.aspx) für diese Elemente weisen alle den Wert **Occurrence** auf. Beachten Sie, dass der Serienmaster in der Antwort nicht vorhanden ist. Die Werte der [ItemId-Elemente](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) wurden zur besseren Lesbarkeit gekürzt. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="939" MinorBuildNumber="16" Version="V2_11" 
        xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

Wenn Sie über ein wiederkehrendes Master-Shape, ein Vorkommen oder eine Ausnahme verfügen, können Sie immer [die anderen verwandten Elemente abrufen.](how-to-access-a-recurring-series-by-using-ews-in-exchange.md) Bei einem Vorkommen oder einer Ausnahme können Sie den wiederkehrenden Master abrufen und umgekehrt.
  
## <a name="working-with-recurring-calendar-items"></a>Arbeiten mit wiederkehrenden Kalenderelementen

Sie verwenden die gleichen Methoden und Vorgänge für die Arbeit mit Terminserien wie für die Arbeit mit nicht wiederkehrenden Kalenderelementen. Der Unterschied besteht darin, dass die Aktionen, die Sie ausführen, abhängig vom Element, das Sie zum Aufrufen dieser Methoden oder Vorgänge verwenden, auf die gesamte Datenreihe oder nur auf ein einzelnes Vorkommen angewendet werden können. [Aktionen, die für den Serienmaster ausgeführt](how-to-update-a-recurring-series-by-using-ews-in-exchange.md) werden, gelten für alle Vorkommen in der Datenreihe, während Aktionen, die [für ein einzelnes Vorkommen oder eine Ausnahme ausgeführt werden,](how-to-update-a-recurring-series-by-using-ews.md) nur für dieses Vorkommen oder diese Ausnahme gelten. 
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

- [Zugreifen auf eine Serienserie mithilfe von EWS in Exchange](how-to-access-a-recurring-series-by-using-ews-in-exchange.md)
    
- [Erstellen einer Serienserie mithilfe von EWS in Exchange](how-to-create-a-recurring-series-by-using-ews-in-exchange.md)
    
- [Löschen von Terminen in einer Terminserie mithilfe von EWS in Exchange](how-to-delete-appointments-in-a-recurring-series-by-using-ews-in-exchange.md)
    
- [Aktualisieren einer Serienserie mithilfe von EWS](how-to-update-a-recurring-series-by-using-ews.md)
    
- [Aktualisieren einer Serienserie mithilfe von EWS in Exchange](how-to-update-a-recurring-series-by-using-ews-in-exchange.md)
    
## <a name="see-also"></a>Siehe auch


- [Kalender und EWS in Exchange](calendars-and-ews-in-exchange.md)
    
- [Entwickeln von Webdienstclients für Exchange](develop-web-service-clients-for-exchange.md)
    
- [Abrufen von Terminen und Besprechungen mithilfe von EWS in Exchange](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md)
    

