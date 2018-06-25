---
title: Zugriff auf eine Terminserie mithilfe von EWS in Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 196a5671-2836-4696-b734-d5ecfdbf8962
description: Erfahren Sie, wie Elemente in einer Terminserie im Kalender zugreifen, indem Sie verwenden die EWS Managed API oder EWS in Exchange.
ms.openlocfilehash: 9f78ef5b51766a69d23fce3f36c55fbb9422fb16
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756842"
---
# <a name="access-a-recurring-series-by-using-ews-in-exchange"></a>Zugriff auf eine Terminserie mithilfe von EWS in Exchange

Erfahren Sie, wie Elemente in einer Terminserie im Kalender zugreifen, indem Sie verwenden die EWS Managed API oder EWS in Exchange.
  
Eine Terminserie Termine oder Besprechungen besteht eines sich wiederholenden Master, eine Anzahl von Vorkommen in einer Reihe, die gemäß einem festen Muster wiederholen und optional Sätze von vorkommen, wurden geändert und gelöscht wurden. Der EWS Managed API oder EWS können Sie Elemente in einer Terminserie im Kalender zuzugreifen. So können Sie:
  
- Überprüfen Sie, um herauszufinden, ob ein Kalenderelement eine Element-ID zugeordnet, ein wiederkehrendes Master-Shape, das Auftreten eines Serientermins in der Datenreihe oder eine Ausnahme zu einer Reihe ist.
    
- Suchen Sie den Kalenderordner für Termine Serie.
    
- Abrufen von verwandten Serie Kalenderelementen (engl.)
    
- Durchlaufen Sie Vorkommen in einer Reihe, Vorkommen Ausnahmen oder Löschvorgänge vorkommen.
    
## <a name="get-a-collection-of-recurring-calendar-items-by-using-the-ews-managed-api"></a>Rufen Sie eine Auflistung von wiederkehrende Kalenderelemente mithilfe der EWS Managed API

Wenn Sie eine Auflistung von Terminen abrufen möchten, können Sie mit der [ExchangeService.FindAppointments](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx) -Methode können alle Termine zwischen einem bestimmten Start- und Enddatum abrufen, und fügen Sie alle Elemente im Kalender mit einem Typ Termin **vorkommen **oder **Ausnahme** in einer Auflistung, wie im folgenden Beispiel dargestellt. 
  
In diesem Beispiel wird davon ausgegangen, das Sie sich an einem Exchange-Server angemeldet haben und das [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt **service** erhalten haben. 
  
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

Beachten Sie, dass sich wiederholenden master Kalenderelemente in einem Aufruf von **FindAppointments**zurückgegeben werden. Wenn Sie sich wiederholenden Masters abrufen möchten, oder Sie einen allgemeineren Ansatz zum Abrufen von Kalenderelementen (engl. möchten), müssen Sie [ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)verwenden. Sie können einen Suchfilter klicken Sie dann zum Abrufen nur Elemente mit einem Startdatum größer als oder gleich ein Datum, an dem Sie auswählen und ein Elementansicht zur Begrenzung der Anzahl der Elemente zurückzugeben, verwenden. Beachten Sie, dass ein wiederkehrendes Master-Shape mit einer Start früher als das Startdatum bei der Suche nicht gefunden werden, Datum wird selbst wenn in diesem Bereich vorkommen auftreten.
  
In diesem Beispiel wird davon ausgegangen, das Sie sich an einem Exchange-Server angemeldet haben und das [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt **service** erhalten haben. 
  
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

## <a name="get-related-recurrence-calendar-items-by-using-the-ews-managed-api"></a>Rufen Sie verwandte Serie Kalenderelemente ab, indem Sie die EWS Managed API

Manchmal müssen Sie ein Teil der Kette, aber zum Lösen dieses Problems benötigen Sie den Rest der Teile. Wenn Sie die Element-ID für ein Kalenderelement Serie verfügen, können Sie die andere Datenelemente abrufen mithilfe einer mehrere EWS Managed API-Eigenschaften und Methoden des benötigten.
  
**In Tabelle 1. EWS Managed API-Eigenschaft oder Methode zum Abrufen von verwandten Serie Kalenderelementen (engl.)**

|**Wenn Sie die Element-ID für haben...**|**Sie erhalten...**|**Mithilfe der...**|
|:-----|:-----|:-----|
|Das Master-Shape wiederkehrenden Kalenderelement  <br/> | Das erste Auftreten in einer Reihe  <br/>  Das letzte Vorkommen in einer Reihe  <br/>  Die Ausnahmen zu einer Reihe  <br/>  Der gelöschte Termine in einer Serie  <br/>  Jedes Vorkommen (wenn dessen Index)  <br/> |[Appointment.FirstOccurrence](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.firstoccurrence%28v=exchg.80%29.aspx) -Eigenschaft  <br/> [Appointment.LastOccurrence](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.lastoccurrence%28v=exchg.80%29.aspx) -Eigenschaft  <br/> [Appointment.ModifiedOccurrences](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.modifiedoccurrences%28v=exchg.80%29.aspx) -Eigenschaft  <br/> [Appointment.DeletedOccurrences](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.deletedoccurrences%28v=exchg.80%29.aspx) -Eigenschaft  <br/> [Appointment.BindToOccurrence](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.appointment.bindtooccurrence%28v=exchg.80%29.aspx) -Methode  <br/> |
|Ein einzelnes Element in einer Reihe  <br/> |Das wiederkehrende Master-Shape  <br/> |[Appointment.BindToRecurringMaster](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.appointment.bindtorecurringmaster%28v=exchg.80%29.aspx) -Methode  <br/> |
|Jedes beliebige Kalenderelement ( [Appointment](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) -Objekt)  <br/> |Der Wert der [Termin Type](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.appointmenttype%28v=exchg.80%29.aspx) -Aufzählung  <br/> |[Appointment.AppointmentType](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.appointment.appointmenttype%28v=exchg.80%29.aspx) -Eigenschaft  <br/> |
   
Im folgenden Codebeispiel wird veranschaulicht, wie ein wiederkehrendes Master-Shape, das erste oder die letzte Vorkommen in einer Reihe oder ein vorkommen, wenn dessen Index abgerufen.
  
In diesem Beispiel wird davon ausgegangen, das Sie sich an einem Exchange-Server angemeldet haben und das [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt **service** erhalten haben. 
  
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

## <a name="access-calendar-items-in-a-recurring-series-by-using-ews"></a>Zugriff auf Kalenderelemente in einer Terminserie mithilfe der Exchange-Webdienste

Zugreifen auf Elemente in einer Terminserie im Kalender ist sehr ähnlich den Zugriff auf einzelne Instanzen von Kalenderelementen (engl.). Sie verwenden eine [GetItem](http://msdn.microsoft.com/library/769df8eb-9c72-48b5-a49f-82c6b86bc5fc%28Office.15%29.aspx) Operation Anforderung angeben die gewünschten Eigenschaften, mit der [OccurrenceItemId](http://msdn.microsoft.com/library/4a15bbc3-5b93-4193-b9ec-da32f0a9a552%28Office.15%29.aspx) der Termin-Instanz, die Sie benötigen. Die [OccurrenceItemId](http://msdn.microsoft.com/library/4a15bbc3-5b93-4193-b9ec-da32f0a9a552%28Office.15%29.aspx) enthält die **ItemID** das Vorkommen wiederkehrenden Master-Shape als auch dessen Indexwert in der Datenreihe an. 
  
Das folgende XML zeigt die [GetItem](http://msdn.microsoft.com/library/769df8eb-9c72-48b5-a49f-82c6b86bc5fc%28Office.15%29.aspx) -Anforderung verwendet, um das Auftreten eines Serientermins in einer Reihe durch den Index angegebene zurückzugeben. Beachten Sie, dass die **ItemID** des wiederkehrenden Master zur besseren Lesbarkeit wurde verkürzt. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

Der Server antwortet auf die Anforderung **GetItem** mit einer [GetItemResponse](http://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx) -Meldung, die den Wert [ResponseCode](http://msdn.microsoft.com/en-us/library/aa580757%28v=exchg.150%29.aspx) **noError zurück**, der angibt, dass die e-Mail-Nachricht erfolgreich erstellt wurde, und die [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) enthält die neu erstellte Nachricht. 
  
## <a name="see-also"></a>Siehe auch


- [Kalender und EWS in Exchange](calendars-and-ews-in-exchange.md)
- [Abrufen von Terminen und Besprechungen mithilfe von EWS in Exchange](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md)
    

