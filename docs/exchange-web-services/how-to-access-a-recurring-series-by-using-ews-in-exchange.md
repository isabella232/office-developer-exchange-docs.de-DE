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
# <a name="access-a-recurring-series-by-using-ews-in-exchange"></a><span data-ttu-id="e368b-103">Zugreifen auf eine Terminserie mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="e368b-103">Access a recurring series by using EWS in Exchange</span></span>

<span data-ttu-id="e368b-104">Informationen zum Zugreifen auf Kalenderelemente in einer Terminserie mithilfe der verwaltete EWS-API oder EWS in Exchange.</span><span class="sxs-lookup"><span data-stu-id="e368b-104">Learn how to access calendar items in a recurring series by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="e368b-105">Eine wiederkehrende Reihe von Terminen oder Besprechungen besteht aus einem wiederkehrenden Master, einer Reihe von Vorkommen in einer Reihe, die nach einem festgelegten Muster wiederholt werden, und optional aus Mengen von vorkommen, die geändert wurden und gelöscht wurden.</span><span class="sxs-lookup"><span data-stu-id="e368b-105">A recurring series of appointments or meetings is made up of a recurring master, a number of occurrences in a series that repeat according to a set pattern, and, optionally, sets of occurrences that were changed and that were deleted.</span></span> <span data-ttu-id="e368b-106">Sie können die verwaltete EWS-API oder EWS verwenden, um auf Kalenderelemente in einer wiederkehrenden Reihe zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="e368b-106">You can use the EWS Managed API or EWS to access calendar items in a recurring series.</span></span> <span data-ttu-id="e368b-107">Auf diese Weise können Sie Folgendes tun:</span><span class="sxs-lookup"><span data-stu-id="e368b-107">This enables you to:</span></span>
  
- <span data-ttu-id="e368b-108">Überprüfen Sie, ob ein Kalenderelement, das einer Element-ID zugeordnet ist, ein wiederkehrendes Master-Objekt, ein Vorkommen in einer Datenreihe oder eine Ausnahme für eine Datenreihe ist.</span><span class="sxs-lookup"><span data-stu-id="e368b-108">Check to see if a calendar item associated with an item ID is a recurring master, an occurrence in a series, or an exception to a series.</span></span>
    
- <span data-ttu-id="e368b-109">Durchsuchen Sie Ihren Kalenderordner nach Serienterminen.</span><span class="sxs-lookup"><span data-stu-id="e368b-109">Search your calendar folder for recurrence appointments.</span></span>
    
- <span data-ttu-id="e368b-110">Abrufen verwandter Serien Kalenderelemente</span><span class="sxs-lookup"><span data-stu-id="e368b-110">Get related recurrence calendar items</span></span>
    
- <span data-ttu-id="e368b-111">Durchlaufen von Vorkommnissen in einer Datenreihe, Vorkommen von Ausnahmen oder Vorkommen von Löschungen.</span><span class="sxs-lookup"><span data-stu-id="e368b-111">Iterate through occurrences in a series, occurrence exceptions, or occurrence deletions.</span></span>
    
## <a name="get-a-collection-of-recurring-calendar-items-by-using-the-ews-managed-api"></a><span data-ttu-id="e368b-112">Abrufen einer Auflistung von wiederkehrenden Kalenderelementen mithilfe der verwaltete EWS-API</span><span class="sxs-lookup"><span data-stu-id="e368b-112">Get a collection of recurring calendar items by using the EWS Managed API</span></span>

<span data-ttu-id="e368b-113">Wenn Sie eine Auflistung von Terminen abrufen möchten, können Sie die [Datei "ExchangeService. FindAppointments](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx) -Methode verwenden, um alle Termine zwischen einem bestimmten Start-und Enddatum abzurufen, und anschließend alle Kalenderelemente mit einem Termintyp eines **Vorkommens** oder einer **Ausnahme** zu einer Auflistung hinzufügen, wie im folgenden Beispiel dargestellt.</span><span class="sxs-lookup"><span data-stu-id="e368b-113">If you want to retrieve a collection of appointments, you can use the [ExchangeService.FindAppointments](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx) method to retrieve all appointments between a given start and end date, and then add all calendar items with an appointment type of **Occurrence** or **Exception** to a collection, as shown in the following example.</span></span> 
  
<span data-ttu-id="e368b-114">In diesem Beispiel wird davon ausgegangen, das Sie sich an einem Exchange-Server angemeldet haben und das [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt **service** erhalten haben.</span><span class="sxs-lookup"><span data-stu-id="e368b-114">This example assumes that you have authenticated to an Exchange server and have acquired an [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object named **service**.</span></span> 
  
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

<span data-ttu-id="e368b-115">Beachten Sie, dass wiederkehrende Master Kalenderelemente in einem Aufruf von **FindAppointments**nicht zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e368b-115">Note that recurring master calendar items aren't returned in a call to **FindAppointments**.</span></span> <span data-ttu-id="e368b-116">Wenn Sie wiederkehrende Master abrufen möchten oder einen allgemeineren Ansatz zum Abrufen von Kalenderelementen wünschen, müssen Sie [Datei "ExchangeService. FindItems](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)verwenden.</span><span class="sxs-lookup"><span data-stu-id="e368b-116">If you want to retrieve recurring masters, or you want a more general approach to retrieving calendar items, you need to use [ExchangeService.FindItems](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx).</span></span> <span data-ttu-id="e368b-117">Anschließend können Sie einen Suchfilter verwenden, um nur Elemente abzurufen, deren Startdatum größer oder gleich dem ausgewählten Datum ist, sowie eine Elementansicht, um die Anzahl der zurückzugebenden Elemente zu begrenzen.</span><span class="sxs-lookup"><span data-stu-id="e368b-117">You can then use a search filter to retrieve only items with a start date greater than or equal to a date you choose, and an item view to limit the number of items to return.</span></span> <span data-ttu-id="e368b-118">Beachten Sie, dass ein wiederkehrendes Master-Objekt mit einem Anfangstermin vor dem Startdatum in Ihrer Suche nicht gefunden wird, auch wenn in diesem Bereich vorkommen auftreten.</span><span class="sxs-lookup"><span data-stu-id="e368b-118">Note that a recurring master with a start date earlier than the start date in your search will not be found, even if occurrences occur in this range.</span></span>
  
<span data-ttu-id="e368b-119">In diesem Beispiel wird davon ausgegangen, das Sie sich an einem Exchange-Server angemeldet haben und das [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt **service** erhalten haben.</span><span class="sxs-lookup"><span data-stu-id="e368b-119">This example assumes that you have authenticated to an Exchange server and have acquired an [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object named **service**.</span></span> 
  
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

## <a name="get-related-recurrence-calendar-items-by-using-the-ews-managed-api"></a><span data-ttu-id="e368b-120">Abrufen verwandter Serien Kalenderelemente mithilfe der verwaltete EWS-API</span><span class="sxs-lookup"><span data-stu-id="e368b-120">Get related recurrence calendar items by using the EWS Managed API</span></span>

<span data-ttu-id="e368b-121">Manchmal haben Sie ein Puzzleteil, aber um es zu lösen, benötigen Sie die restlichen Teile.</span><span class="sxs-lookup"><span data-stu-id="e368b-121">Sometimes you have one piece of the puzzle, but to solve it you need the rest of the pieces.</span></span> <span data-ttu-id="e368b-122">Wenn Sie die Element-ID für ein Serien Kalenderelement haben, können Sie die anderen benötigten Teile mithilfe einer von mehreren verwaltete EWS-API Eigenschaften oder Methoden abrufen.</span><span class="sxs-lookup"><span data-stu-id="e368b-122">If you have the item ID for a recurrence calendar item, you can get the other pieces you need by using one of several EWS Managed API properties or methods.</span></span>
  
<span data-ttu-id="e368b-123">**Tabelle 1. Verwaltete EWS-API Eigenschaft oder Methode, mit der Verwandte Serien Kalenderelemente abgerufen werden können**</span><span class="sxs-lookup"><span data-stu-id="e368b-123">**Table 1. EWS Managed API property or method to use to get related recurrence calendar items**</span></span>

|<span data-ttu-id="e368b-124">**Wenn Sie über die Element-ID für...**</span><span class="sxs-lookup"><span data-stu-id="e368b-124">**If you have the item ID for…**</span></span>|<span data-ttu-id="e368b-125">**Sie können abrufen...**</span><span class="sxs-lookup"><span data-stu-id="e368b-125">**You can get…**</span></span>|<span data-ttu-id="e368b-126">**Mithilfe der...**</span><span class="sxs-lookup"><span data-stu-id="e368b-126">**By using the…**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e368b-127">Das wiederkehrende Hauptkalender Element</span><span class="sxs-lookup"><span data-stu-id="e368b-127">The recurring master calendar item</span></span>  <br/> | <span data-ttu-id="e368b-128">Das erste Vorkommen einer Datenreihe</span><span class="sxs-lookup"><span data-stu-id="e368b-128">The first occurrence in a series</span></span>  <br/>  <span data-ttu-id="e368b-129">Das letzte Vorkommen einer Datenreihe</span><span class="sxs-lookup"><span data-stu-id="e368b-129">The last occurrence in a series</span></span>  <br/>  <span data-ttu-id="e368b-130">Die Ausnahmen für eine Datenreihe</span><span class="sxs-lookup"><span data-stu-id="e368b-130">The exceptions to a series</span></span>  <br/>  <span data-ttu-id="e368b-131">Die gelöschten Termine in einer Reihe</span><span class="sxs-lookup"><span data-stu-id="e368b-131">The deleted appointments in a series</span></span>  <br/>  <span data-ttu-id="e368b-132">Jedes Vorkommen (aufgrund seines Indexes)</span><span class="sxs-lookup"><span data-stu-id="e368b-132">Any occurrence (given its index)</span></span>  <br/> |<span data-ttu-id="e368b-133">[Termin. FirstOccurrence](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.firstoccurrence%28v=exchg.80%29.aspx) -Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e368b-133">[Appointment.FirstOccurrence](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.firstoccurrence%28v=exchg.80%29.aspx) property</span></span>  <br/> <span data-ttu-id="e368b-134">[Termin. LastOccurrence](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.lastoccurrence%28v=exchg.80%29.aspx) -Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e368b-134">[Appointment.LastOccurrence](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.lastoccurrence%28v=exchg.80%29.aspx) property</span></span>  <br/> <span data-ttu-id="e368b-135">[Termin. ModifiedOccurrences](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.modifiedoccurrences%28v=exchg.80%29.aspx) -Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e368b-135">[Appointment.ModifiedOccurrences](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.modifiedoccurrences%28v=exchg.80%29.aspx) property</span></span>  <br/> <span data-ttu-id="e368b-136">[Termin. DeletedOccurrences](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.deletedoccurrences%28v=exchg.80%29.aspx) -Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e368b-136">[Appointment.DeletedOccurrences](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.deletedoccurrences%28v=exchg.80%29.aspx) property</span></span>  <br/> <span data-ttu-id="e368b-137">[Termin. BindToOccurrence](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.appointment.bindtooccurrence%28v=exchg.80%29.aspx) -Methode</span><span class="sxs-lookup"><span data-stu-id="e368b-137">[Appointment.BindToOccurrence](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.appointment.bindtooccurrence%28v=exchg.80%29.aspx) method</span></span>  <br/> |
|<span data-ttu-id="e368b-138">Ein einzelnes Vorkommen in einer Datenreihe</span><span class="sxs-lookup"><span data-stu-id="e368b-138">A single occurrence in a series</span></span>  <br/> |<span data-ttu-id="e368b-139">Der wiederkehrende Master</span><span class="sxs-lookup"><span data-stu-id="e368b-139">The recurring master</span></span>  <br/> |<span data-ttu-id="e368b-140">[Termin. BindToRecurringMaster](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.appointment.bindtorecurringmaster%28v=exchg.80%29.aspx) -Methode</span><span class="sxs-lookup"><span data-stu-id="e368b-140">[Appointment.BindToRecurringMaster](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.appointment.bindtorecurringmaster%28v=exchg.80%29.aspx) method</span></span>  <br/> |
|<span data-ttu-id="e368b-141">Beliebiges Kalenderelement (ein [Termin](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) Objekt)</span><span class="sxs-lookup"><span data-stu-id="e368b-141">Any calendar item (an [Appointment](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) object)</span></span>  <br/> |<span data-ttu-id="e368b-142">Der Aufzählungswert des [Termin Typs](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.appointmenttype%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e368b-142">The [appointment type](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.appointmenttype%28v=exchg.80%29.aspx) enumeration value</span></span>  <br/> |<span data-ttu-id="e368b-143">[Termin. termintype](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.appointment.appointmenttype%28v=exchg.80%29.aspx) -Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e368b-143">[Appointment.AppointmentType](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.appointment.appointmenttype%28v=exchg.80%29.aspx) property</span></span>  <br/> |
   
<span data-ttu-id="e368b-144">Im folgenden Codebeispiel wird gezeigt, wie ein wiederkehrendes Master-Element, das erste oder letzte Vorkommen einer Datenreihe oder ein vorkommen, das seinen Index erhält, abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="e368b-144">The following code example shows how to get a recurring master, the first or last occurrence in a series, or an occurrence given its index.</span></span>
  
<span data-ttu-id="e368b-145">In diesem Beispiel wird davon ausgegangen, das Sie sich an einem Exchange-Server angemeldet haben und das [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt **service** erhalten haben.</span><span class="sxs-lookup"><span data-stu-id="e368b-145">This example assumes that you have authenticated to an Exchange server and have acquired an [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object named **service**.</span></span> 
  
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

## <a name="access-calendar-items-in-a-recurring-series-by-using-ews"></a><span data-ttu-id="e368b-146">Zugreifen auf Kalenderelemente in einer Terminserie mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="e368b-146">Access calendar items in a recurring series by using EWS</span></span>

<span data-ttu-id="e368b-147">Der Zugriff auf Kalenderelemente in einer Terminserie ähnelt dem Zugriff auf einzelne Instanzen von Kalenderelementen.</span><span class="sxs-lookup"><span data-stu-id="e368b-147">Accessing calendar items in a recurring series is very similar to accessing single instances of calendar items.</span></span> <span data-ttu-id="e368b-148">Sie verwenden eine [GetItem](https://msdn.microsoft.com/library/769df8eb-9c72-48b5-a49f-82c6b86bc5fc%28Office.15%29.aspx) -Vorgangsanforderung, die die gewünschten Eigenschaften angibt, mit dem [OccurrenceItemId](https://msdn.microsoft.com/library/4a15bbc3-5b93-4193-b9ec-da32f0a9a552%28Office.15%29.aspx) der benötigten Termin Instanz.</span><span class="sxs-lookup"><span data-stu-id="e368b-148">You use a [GetItem](https://msdn.microsoft.com/library/769df8eb-9c72-48b5-a49f-82c6b86bc5fc%28Office.15%29.aspx) operation request, specifying the properties you want, with the [OccurrenceItemId](https://msdn.microsoft.com/library/4a15bbc3-5b93-4193-b9ec-da32f0a9a552%28Office.15%29.aspx) of the appointment instance you need.</span></span> <span data-ttu-id="e368b-149">Das [OccurrenceItemId](https://msdn.microsoft.com/library/4a15bbc3-5b93-4193-b9ec-da32f0a9a552%28Office.15%29.aspx) -Element enthält die **ItemID** des wiederkehrenden Masters des Ereignisses sowie den Indexwert in der Datenreihe.</span><span class="sxs-lookup"><span data-stu-id="e368b-149">The [OccurrenceItemId](https://msdn.microsoft.com/library/4a15bbc3-5b93-4193-b9ec-da32f0a9a552%28Office.15%29.aspx) contains the **ItemID** of the occurrence's recurring master, as well as its index value in the series.</span></span> 
  
<span data-ttu-id="e368b-150">Der folgende XML-Code zeigt die [GetItem](https://msdn.microsoft.com/library/769df8eb-9c72-48b5-a49f-82c6b86bc5fc%28Office.15%29.aspx) -Anforderung, die zum Zurückgeben eines Vorkommens in einer durch den Index angegebenen Datenreihe verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e368b-150">The following XML shows the [GetItem](https://msdn.microsoft.com/library/769df8eb-9c72-48b5-a49f-82c6b86bc5fc%28Office.15%29.aspx) request used to return an occurrence in a series specified by its index.</span></span> <span data-ttu-id="e368b-151">Beachten Sie, dass die **ItemID** des wiederkehrenden Masters zur Lesbarkeit gekürzt wurde.</span><span class="sxs-lookup"><span data-stu-id="e368b-151">Note that the **ItemID** of the recurring master has been shortened for readability.</span></span> 
  
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

<span data-ttu-id="e368b-152">Der Server antwortet auf die **GetItem** -Anforderung mit einer [GetItemResponse](https://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx) -Nachricht, die den [Response Code](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx) -Wert **noError**enthält, der angibt, dass die e-Mail erfolgreich erstellt wurde, und das [ItemID](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) der neu erstellten Nachricht.</span><span class="sxs-lookup"><span data-stu-id="e368b-152">The server responds to the **GetItem** request with a [GetItemResponse](https://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, which indicates that the email was created successfully, and the [ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) of the newly created message.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e368b-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e368b-153">See also</span></span>


- [<span data-ttu-id="e368b-154">Kalender und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="e368b-154">Calendars and EWS in Exchange</span></span>](calendars-and-ews-in-exchange.md)
- [<span data-ttu-id="e368b-155">Abrufen von Terminen und Besprechungen mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="e368b-155">Get appointments and meetings by using EWS in Exchange</span></span>](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md)
    

