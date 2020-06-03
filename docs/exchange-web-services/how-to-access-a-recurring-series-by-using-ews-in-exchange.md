---
title: Zugreifen auf eine Terminserie mithilfe von EWS in Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 196a5671-2836-4696-b734-d5ecfdbf8962
description: Informationen zum Zugreifen auf Kalenderelemente in einer Terminserie mithilfe der verwaltete EWS-API oder EWS in Exchange.
ms.openlocfilehash: dca41472b3b2f775f420b6654d7e43ef456b0583
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456892"
---
# <a name="access-a-recurring-series-by-using-ews-in-exchange"></a>Zugreifen auf eine Terminserie mithilfe von EWS in Exchange

Informationen zum Zugreifen auf Kalenderelemente in einer Terminserie mithilfe der verwaltete EWS-API oder EWS in Exchange.
  
Eine wiederkehrende Reihe von Terminen oder Besprechungen besteht aus einem wiederkehrenden Master, einer Reihe von Vorkommen in einer Reihe, die nach einem festgelegten Muster wiederholt werden, und optional aus Mengen von vorkommen, die geändert wurden und gelöscht wurden. Sie können die verwaltete EWS-API oder EWS verwenden, um auf Kalenderelemente in einer wiederkehrenden Reihe zuzugreifen. Auf diese Weise können Sie Folgendes tun:
  
- Überprüfen Sie, ob ein Kalenderelement, das einer Element-ID zugeordnet ist, ein wiederkehrendes Master-Objekt, ein Vorkommen in einer Datenreihe oder eine Ausnahme für eine Datenreihe ist.
    
- Durchsuchen Sie Ihren Kalenderordner nach Serienterminen.
    
- Abrufen verwandter Serien Kalenderelemente
    
- Durchlaufen von Vorkommnissen in einer Datenreihe, Vorkommen von Ausnahmen oder Vorkommen von Löschungen.
    
## <a name="get-a-collection-of-recurring-calendar-items-by-using-the-ews-managed-api"></a>Abrufen einer Auflistung von wiederkehrenden Kalenderelementen mithilfe der verwaltete EWS-API

Wenn Sie eine Auflistung von Terminen abrufen möchten, können Sie die [Datei "ExchangeService. FindAppointments](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx) -Methode verwenden, um alle Termine zwischen einem bestimmten Start-und Enddatum abzurufen, und anschließend alle Kalenderelemente mit einem Termintyp eines **Vorkommens** oder einer **Ausnahme** zu einer Auflistung hinzufügen, wie im folgenden Beispiel dargestellt. 
  
In diesem Beispiel wird davon ausgegangen, das Sie sich an einem Exchange-Server angemeldet haben und das [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt **service** erhalten haben. 
  
```cs
public static Collection<Appointment> FindRecurringCalendarItems(ExchangeService service, 
                                                                    DateTime startSearchDate, 
                                                                    DateTime endSearchDate)
{
    // Instantiate a collection to hold occurrences and exception calendar items.
    Collection<Appointment> foundAppointments = new Collection<Appointment>();
    // Create a calendar view to search the calendar folder and specify the properties to return.
    CalendarView calView = new CalendarView(startSearchDate, endSearchDate);
    calView.PropertySet = new PropertySet(BasePropertySet.IdOnly, 
                                            AppointmentSchema.Subject, 
                                            AppointmentSchema.Start, 
                                            AppointmentSchema.IsRecurring, 
                                            AppointmentSchema.AppointmentType);
    // Retrieve a collection of calendar items.
    FindItemsResults<Appointment> findResults = service.FindAppointments(WellKnownFolderName.Calendar, calView);
    // Add all calendar items in your view that are occurrences or exceptions to your collection.
    foreach (Appointment appt in findResults.Items)
    {
        if (appt.AppointmentType == AppointmentType.Occurrence || appt.AppointmentType == AppointmentType.Exception)
        {
            foundAppointments.Add(appt);
        }
        else
        {
            Console.WriteLine("Discarding calendar item of type {0}.", appt.AppointmentType);
        }
    }
    return foundAppointments;
}

```

Beachten Sie, dass wiederkehrende Master Kalenderelemente in einem Aufruf von **FindAppointments**nicht zurückgegeben werden. Wenn Sie wiederkehrende Master abrufen möchten oder einen allgemeineren Ansatz zum Abrufen von Kalenderelementen wünschen, müssen Sie [Datei "ExchangeService. FindItems](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)verwenden. Anschließend können Sie einen Suchfilter verwenden, um nur Elemente abzurufen, deren Startdatum größer oder gleich dem ausgewählten Datum ist, sowie eine Elementansicht, um die Anzahl der zurückzugebenden Elemente zu begrenzen. Beachten Sie, dass ein wiederkehrendes Master-Objekt mit einem Anfangstermin vor dem Startdatum in Ihrer Suche nicht gefunden wird, auch wenn in diesem Bereich vorkommen auftreten.
  
In diesem Beispiel wird davon ausgegangen, das Sie sich an einem Exchange-Server angemeldet haben und das [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt **service** erhalten haben. 
  
```cs
public static Collection<Appointment> FindCalendarItemsByAppointmentType(ExchangeService service, 
                                                                         AppointmentType myAppointmentType, 
                                                                         DateTime startSearchDate)
{
    Collection<Appointment> foundAppointments = new Collection<Appointment>();
    // Create a search filter based on the start search date.
    SearchFilter.SearchFilterCollection searchFilter = new SearchFilter.SearchFilterCollection();
    searchFilter.Add(new SearchFilter.IsGreaterThanOrEqualTo(AppointmentSchema.Start, startSearchDate));
    // Create an item view to specify which properties to return.
    ItemView view = new ItemView(20);
    view.PropertySet = new PropertySet(BasePropertySet.IdOnly, 
                                       AppointmentSchema.Subject, 
                                       AppointmentSchema.Start, 
                                       AppointmentSchema.AppointmentType,
                                       AppointmentSchema.IsRecurring);
    // Get the appointment items from the server with the properties we specified.
    FindItemsResults<Item> findResults = service.FindItems(WellKnownFolderName.Calendar, searchFilter, view);
    // Add each of the appointments of the type you want to the collection.
    foreach (Item item in findResults.Items)
    {
        Appointment appt = item as Appointment;
        if (appt.AppointmentType == myAppointmentType)
        {
            foundAppointments.Add(appt);
        }
    }
    return foundAppointments;
}

```

## <a name="get-related-recurrence-calendar-items-by-using-the-ews-managed-api"></a>Abrufen verwandter Serien Kalenderelemente mithilfe der verwaltete EWS-API

Manchmal haben Sie ein Puzzleteil, aber um es zu lösen, benötigen Sie die restlichen Teile. Wenn Sie die Element-ID für ein Serien Kalenderelement haben, können Sie die anderen benötigten Teile mithilfe einer von mehreren verwaltete EWS-API Eigenschaften oder Methoden abrufen.
  
**Tabelle 1. Verwaltete EWS-API Eigenschaft oder Methode, mit der Verwandte Serien Kalenderelemente abgerufen werden können**

|**Wenn Sie über die Element-ID für...**|**Sie können abrufen...**|**Mithilfe der...**|
|:-----|:-----|:-----|
|Das wiederkehrende Hauptkalender Element  <br/> | Das erste Vorkommen einer Datenreihe  <br/>  Das letzte Vorkommen einer Datenreihe  <br/>  Die Ausnahmen für eine Datenreihe  <br/>  Die gelöschten Termine in einer Reihe  <br/>  Jedes Vorkommen (aufgrund seines Indexes)  <br/> |[Termin. FirstOccurrence](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.firstoccurrence%28v=exchg.80%29.aspx) -Eigenschaft  <br/> [Termin. LastOccurrence](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.lastoccurrence%28v=exchg.80%29.aspx) -Eigenschaft  <br/> [Termin. ModifiedOccurrences](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.modifiedoccurrences%28v=exchg.80%29.aspx) -Eigenschaft  <br/> [Termin. DeletedOccurrences](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.deletedoccurrences%28v=exchg.80%29.aspx) -Eigenschaft  <br/> [Termin. BindToOccurrence](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.appointment.bindtooccurrence%28v=exchg.80%29.aspx) -Methode  <br/> |
|Ein einzelnes Vorkommen in einer Datenreihe  <br/> |Der wiederkehrende Master  <br/> |[Termin. BindToRecurringMaster](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.appointment.bindtorecurringmaster%28v=exchg.80%29.aspx) -Methode  <br/> |
|Beliebiges Kalenderelement (ein [Termin](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) Objekt)  <br/> |Der Aufzählungswert des [Termin Typs](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.appointmenttype%28v=exchg.80%29.aspx)  <br/> |[Termin. termintype](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.appointment.appointmenttype%28v=exchg.80%29.aspx) -Eigenschaft  <br/> |
   
Im folgenden Codebeispiel wird gezeigt, wie ein wiederkehrendes Master-Element, das erste oder letzte Vorkommen einer Datenreihe oder ein vorkommen, das seinen Index erhält, abgerufen wird.
  
In diesem Beispiel wird davon ausgegangen, das Sie sich an einem Exchange-Server angemeldet haben und das [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt **service** erhalten haben. 
  
```cs
public static void GetRelatedRecurrenceCalendarItems(ExchangeService service, ItemId itemId)
{
    Appointment calendarItem = Appointment.Bind(service, itemId, new PropertySet(AppointmentSchema.AppointmentType));
    Appointment recurrMaster = new Appointment(service);
    PropertySet props = new PropertySet(AppointmentSchema.AppointmentType,
                                        AppointmentSchema.Subject,
                                        AppointmentSchema.FirstOccurrence,
                                        AppointmentSchema.LastOccurrence,
                                        AppointmentSchema.ModifiedOccurrences,
                                        AppointmentSchema.DeletedOccurrences);
    // If the item ID is not for a recurring master, retrieve the recurring master for the series.
    switch (calendarItem.AppointmentType)
    {
        // Calendar item is a recurring master so use Appointment.Bind
        case AppointmentType.RecurringMaster:
            recurrMaster = Appointment.Bind(service, itemId, props);
            break;
        // The calendar item is a single instance meeting, so there are no instances to modify or delete.
        case AppointmentType.Single:
            Console.WriteLine("Item id must reference a calendar item that is part of a recurring series.");
            return;
        // The calendar item is an occurrence in the series, so use BindToRecurringMaster.
        case AppointmentType.Occurrence:
            recurrMaster = Appointment.BindToRecurringMaster(service, itemId, props);
            break;
        // The calendar item is an exception to the series, so use BindToRecurringMaster.                
        case AppointmentType.Exception:
            recurrMaster = Appointment.BindToRecurringMaster(service, itemId, props);
            break;
    }
    // View the first occurrence, last occurrence, and number of modified and deleted occurrences associated with the recurring master.
    Console.WriteLine("Information for the {0} recurring series:", recurrMaster.Subject);
    Console.WriteLine("The start time for the first appointment with id \t{0} was on \t{1}.", 
                        recurrMaster.FirstOccurrence.ItemId.ToString().Substring(144), 
                        recurrMaster.FirstOccurrence.Start.ToString());
    Console.WriteLine("The start time for the last appointment with id \t{0} will be on \t{1}.", 
                        recurrMaster.LastOccurrence.ItemId.ToString().Substring(144), 
                        recurrMaster.LastOccurrence.Start.ToString());
    Console.WriteLine("There are {0} modified occurrences and {1} deleted occurrences.", 
                        recurrMaster.ModifiedOccurrences == null ? "no" : recurrMaster.ModifiedOccurrences.Count.ToString(), 
                        recurrMaster.DeletedOccurrences == null ? "no" : recurrMaster.DeletedOccurrences.Count.ToString());
    // Bind to the first occurrence of a series by using its index.
    Appointment firstOccurrence = Appointment.BindToOccurrence(service, 
                                                                recurrMaster.Id, 
                                                                1, // Index of first item is 1, not 0.
                                                                new PropertySet(AppointmentSchema.AppointmentType,
                                                                                AppointmentSchema.Start));
    Console.WriteLine("Compare the start times for a recurring master's first occurrence " + 
                        "and the occurrence found at index 1 using the BindToOccurrence method:");
    Console.WriteLine("The appointment at index 1 has a start time of\t\t\t\t {0}\n" +
                        "Which matches that of the first occurrence on the recurring master: \t {1}",
                        firstOccurrence.Start.ToString(),
                        recurrMaster.FirstOccurrence.Start.ToString());
}

```

## <a name="access-calendar-items-in-a-recurring-series-by-using-ews"></a>Zugreifen auf Kalenderelemente in einer Terminserie mithilfe von EWS

Der Zugriff auf Kalenderelemente in einer Terminserie ähnelt dem Zugriff auf einzelne Instanzen von Kalenderelementen. Sie verwenden eine [GetItem](https://msdn.microsoft.com/library/769df8eb-9c72-48b5-a49f-82c6b86bc5fc%28Office.15%29.aspx) -Vorgangsanforderung, die die gewünschten Eigenschaften angibt, mit dem [OccurrenceItemId](https://msdn.microsoft.com/library/4a15bbc3-5b93-4193-b9ec-da32f0a9a552%28Office.15%29.aspx) der benötigten Termin Instanz. Das [OccurrenceItemId](https://msdn.microsoft.com/library/4a15bbc3-5b93-4193-b9ec-da32f0a9a552%28Office.15%29.aspx) -Element enthält die **ItemID** des wiederkehrenden Masters des Ereignisses sowie den Indexwert in der Datenreihe. 
  
Der folgende XML-Code zeigt die [GetItem](https://msdn.microsoft.com/library/769df8eb-9c72-48b5-a49f-82c6b86bc5fc%28Office.15%29.aspx) -Anforderung, die zum Zurückgeben eines Vorkommens in einer durch den Index angegebenen Datenreihe verwendet wird. Beachten Sie, dass die **ItemID** des wiederkehrenden Masters zur Lesbarkeit gekürzt wurde. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010" />
  </soap:Header>
  <soap:Body>
    <m:GetItem>
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="calendar:CalendarItemType" />
          <t:FieldURI FieldURI="calendar:Start" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:ItemIds>
        <t:OccurrenceItemId RecurringMasterId="AAMkA" InstanceIndex="1" />
      </m:ItemIds>
    </m:GetItem>
  </soap:Body>
</soap:Envelope>
```

Der Server antwortet auf die **GetItem** -Anforderung mit einer [GetItemResponse](https://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx) -Nachricht, die den [Response Code](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx) -Wert **noError**enthält, der angibt, dass die e-Mail erfolgreich erstellt wurde, und das [ItemID](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) der neu erstellten Nachricht. 
  
## <a name="see-also"></a>Siehe auch


- [Kalender und EWS in Exchange](calendars-and-ews-in-exchange.md)
- [Abrufen von Terminen und Besprechungen mithilfe von EWS in Exchange](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md)
    

