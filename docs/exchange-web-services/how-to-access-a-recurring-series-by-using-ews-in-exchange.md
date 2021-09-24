---
title: Zugreifen auf eine Serienserie mithilfe von EWS in Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 196a5671-2836-4696-b734-d5ecfdbf8962
description: Erfahren Sie, wie Sie mithilfe der verwalteten EWS-API oder EWS in Exchange auf Kalenderelemente in einer Terminserie zugreifen.
ms.openlocfilehash: 280affe532beb282bdd5cdb0c02a3dfaa62751e5
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513241"
---
# <a name="access-a-recurring-series-by-using-ews-in-exchange"></a>Zugreifen auf eine Serienserie mithilfe von EWS in Exchange

Erfahren Sie, wie Sie mithilfe der verwalteten EWS-API oder EWS in Exchange auf Kalenderelemente in einer Terminserie zugreifen.
  
Eine Terminserie oder Besprechungsserie besteht aus einem wiederkehrenden Master, einer Reihe von Vorkommen in einer Serie, die sich gemäß einem festgelegten Muster wiederholen, und optional aus Sätzen von Vorkommen, die geändert und gelöscht wurden. Sie können die verwaltete EWS-API oder EWS verwenden, um auf Kalenderelemente in einer Terminserie zuzugreifen. Auf diese Weise können Sie:
  
- Überprüfen Sie, ob ein kalenderelement, das einer Element-ID zugeordnet ist, ein wiederkehrendes Master-Shape, ein Vorkommen in einer Datenreihe oder eine Ausnahme zu einer Datenreihe ist.
    
- Durchsuchen Sie ihren Kalenderordner nach Serienterminen.
    
- Abrufen verwandter Serienkalenderelemente
    
- Durchlaufen von Vorkommen in einer Datenreihe, Vorkommens ausnahmen oder Löschvorgänge.
    
## <a name="get-a-collection-of-recurring-calendar-items-by-using-the-ews-managed-api"></a>Abrufen einer Sammlung wiederkehrender Kalenderelemente mithilfe der verwalteten EWS-API

Wenn Sie eine Sammlung von Terminen abrufen möchten, können Sie mit der [ExchangeService.FindAppointments-Methode](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx) alle Termine zwischen einem bestimmten Anfangs- und Enddatum abrufen und dann alle Kalenderelemente mit dem Termintyp **"Occurrence"** oder **"Exception"** einer Auflistung hinzufügen, wie im folgenden Beispiel gezeigt. 
  
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

Beachten Sie, dass wiederkehrende Masterkalenderelemente in einem Aufruf von **FindAppointments** nicht zurückgegeben werden. Wenn Sie wiederkehrende Master abrufen möchten oder einen allgemeineren Ansatz zum Abrufen von Kalenderelementen wünschen, müssen Sie [ExchangeService.FindItems](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)verwenden. Anschließend können Sie einen Suchfilter verwenden, um nur Elemente abzurufen, deren Startdatum größer oder gleich einem ausgewählten Datum ist, und eine Elementansicht, um die Anzahl der zurückzugebenden Elemente einzuschränken. Beachten Sie, dass ein serienweiser Master mit einem Startdatum vor dem Startdatum in Der Suche nicht gefunden wird, auch wenn Vorkommen in diesem Bereich auftreten.
  
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

## <a name="get-related-recurrence-calendar-items-by-using-the-ews-managed-api"></a>Abrufen verwandter Serienkalenderelemente mithilfe der verwalteten EWS-API

Manchmal haben Sie ein Teil des Puzzles, aber um es zu lösen, benötigen Sie die restlichen Teile. Wenn Sie über die Element-ID für ein Serienkalenderelement verfügen, können Sie die anderen benötigten Teile abrufen, indem Sie eine von mehreren verwalteten EWS-API-Eigenschaften oder -Methoden verwenden.
  
**Tabelle 1. Verwaltete EWS-API-Eigenschaft oder -Methode zum Abrufen verwandter Serienkalenderelemente**

|**Wenn Sie die Element-ID für...**|**Sie können...**|**Mithilfe der...**|
|:-----|:-----|:-----|
|Das Serienmasterkalenderelement  <br/> | Das erste Vorkommen in einer Datenreihe  <br/>  Das letzte Vorkommen in einer Datenreihe  <br/>  Die Ausnahmen zu einer Datenreihe  <br/>  Die gelöschten Termine in einer Reihe  <br/>  Ein beliebiges Vorkommen (mit angabe des Indexes)  <br/> |[Appointment.FirstOccurrence-Eigenschaft](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.firstoccurrence%28v=exchg.80%29.aspx)  <br/> [Appointment.LastOccurrence-Eigenschaft](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.lastoccurrence%28v=exchg.80%29.aspx)  <br/> [Appointment.ModifiedOccurrences-Eigenschaft](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.modifiedoccurrences%28v=exchg.80%29.aspx)  <br/> [Appointment.DeletedOccurrences-Eigenschaft](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.deletedoccurrences%28v=exchg.80%29.aspx)  <br/> [Appointment.BindToOccurrence-Methode](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.appointment.bindtooccurrence%28v=exchg.80%29.aspx)  <br/> |
|Ein einzelnes Vorkommen in einer Datenreihe  <br/> |Der Serienmaster  <br/> |[Appointment.BindToRecurringMaster-Methode](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.appointment.bindtorecurringmaster%28v=exchg.80%29.aspx)  <br/> |
|Ein beliebiges Kalenderelement (ein [Appointment-Objekt)](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx)  <br/> |Der [Enumerationswert des Termintyps](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.appointmenttype%28v=exchg.80%29.aspx)  <br/> |[Appointment.AppointmentType-Eigenschaft](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.appointment.appointmenttype%28v=exchg.80%29.aspx)  <br/> |
   
Das folgende Codebeispiel zeigt, wie sie einen Serienmaster, das erste oder letzte Vorkommen in einer Datenreihe oder ein Vorkommen mit dem Index abrufen.
  
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

Der Zugriff auf Kalenderelemente in einer Terminserie ähnelt dem Zugriff auf einzelne Instanzen von Kalenderelementen. Sie verwenden eine [GetItem-Vorgangsanforderung,](https://msdn.microsoft.com/library/769df8eb-9c72-48b5-a49f-82c6b86bc5fc%28Office.15%29.aspx) die die gewünschten Eigenschaften mit der [OccurrenceItemId](https://msdn.microsoft.com/library/4a15bbc3-5b93-4193-b9ec-da32f0a9a552%28Office.15%29.aspx) der benötigten Termininstanz angibt. Die [OccurrenceItemId](https://msdn.microsoft.com/library/4a15bbc3-5b93-4193-b9ec-da32f0a9a552%28Office.15%29.aspx) enthält die **ItemID** des Serienmasters des Vorkommens sowie den Indexwert in der Datenreihe. 
  
Der folgende XML-Code zeigt die [GetItem-Anforderung,](https://msdn.microsoft.com/library/769df8eb-9c72-48b5-a49f-82c6b86bc5fc%28Office.15%29.aspx) die verwendet wird, um ein Vorkommen in einer durch den Index angegebenen Datenreihe zurückzugeben. Beachten Sie, dass die **ItemID** des Serienmasters zur besseren Lesbarkeit gekürzt wurde. 
  
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

Der Server antwortet auf die **GetItem-Anforderung** mit einer [GetItemResponse-Nachricht,](https://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx) die den [ResponseCode-Wert](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx) **NoError** enthält, der angibt, dass die E-Mail erfolgreich erstellt wurde, und die [ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) der neu erstellten Nachricht. 
  
## <a name="see-also"></a>Siehe auch


- [Kalender und EWS in Exchange](calendars-and-ews-in-exchange.md)
- [Abrufen von Terminen und Besprechungen mithilfe von EWS in Exchange](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md)
    

