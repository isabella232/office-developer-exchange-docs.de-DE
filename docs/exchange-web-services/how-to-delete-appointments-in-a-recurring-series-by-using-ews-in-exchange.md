---
title: Löschen von Terminen in einer Terminserie mithilfe von EWS in Exchange
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a9d5244a-bc4a-4e9c-9c6c-ff361e04cbf8
description: In diesem Artikel erfahren Sie, wie Sie Termine in einer Terminserie mithilfe der verwaltete EWS-API oder EWS in Exchange löschen.
ms.openlocfilehash: 5646a30d218ed4d795044aefe5efea1399d19a79
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528125"
---
# <a name="delete-appointments-in-a-recurring-series-by-using-ews-in-exchange"></a><span data-ttu-id="7a087-103">Löschen von Terminen in einer Terminserie mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="7a087-103">Delete appointments in a recurring series by using EWS in Exchange</span></span>

<span data-ttu-id="7a087-104">In diesem Artikel erfahren Sie, wie Sie Termine in einer Terminserie mithilfe der verwaltete EWS-API oder EWS in Exchange löschen.</span><span class="sxs-lookup"><span data-stu-id="7a087-104">Learn how to delete appointments in a recurring series by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="7a087-105">Sie können die verwaltete EWS-API oder EWS verwenden, um eine Reihe von Terminen oder Besprechungen oder nur eine Instanz in der Datenreihe zu löschen.</span><span class="sxs-lookup"><span data-stu-id="7a087-105">You can use the EWS Managed API or EWS to delete a series of appointments or meetings, or just one instance in the series.</span></span> <span data-ttu-id="7a087-106">Der Vorgang, den Sie zum Löschen einer ganzen Datenreihe verwenden, ist im Wesentlichen identisch mit dem Vorgang, den Sie zum Löschen eines einzelnen Exemplars verwenden.</span><span class="sxs-lookup"><span data-stu-id="7a087-106">The process you use to delete an entire series is essentially the same as the process you use to delete just a single occurrence.</span></span> <span data-ttu-id="7a087-107">Sie verwenden dieselben verwaltete EWS-API Methoden oder EWS-Vorgänge, die Sie zum [Löschen eines Termins oder einer Besprechung einer einzelnen Instanz](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)verwenden.</span><span class="sxs-lookup"><span data-stu-id="7a087-107">You use the same EWS Managed API methods or EWS operations that you use to [delete a single instance appointment or meeting](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md).</span></span> <span data-ttu-id="7a087-108">Der Unterschied besteht in der Element-ID, die in der Methode oder dem Vorgang enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="7a087-108">The difference is in the item ID that is included in the method or operation.</span></span> <span data-ttu-id="7a087-109">Zunächst sehen wir uns an, wie beide Szenarien identisch sind.</span><span class="sxs-lookup"><span data-stu-id="7a087-109">Let's start by looking at how both scenarios are the same.</span></span> 
  
<span data-ttu-id="7a087-110">Wenn Sie eine wiederkehrende Datenreihe oder ein einzelnes Vorkommen in einer Terminserie löschen möchten, müssen Sie das zu löschende vorkommen oder die zu löschende Datenreihe suchen und dann die entsprechende Methode oder den entsprechenden Vorgang aufrufen, um Sie zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="7a087-110">In order to delete a recurring series or a single occurrence in a recurring series, you need to find the occurrence or series that you want to delete, and then call the appropriate method or operation to remove it.</span></span> <span data-ttu-id="7a087-111">Sie können zwar einfach jede Art von Termin löschen, es wird jedoch empfohlen, dass Sie alle Teilnehmer oder Organisatoren auf dem neuesten Stand halten und Besprechungen kündigen, die der Benutzer organisiert hat, und Besprechungen ablehnen, die der Benutzer nicht organisiert hat.</span><span class="sxs-lookup"><span data-stu-id="7a087-111">While you can simply delete any type of appointment, we recommend that you keep any attendees or the organizer up to date and cancel meetings that the user has organized and decline meetings that the user did not organize.</span></span>
  
<span data-ttu-id="7a087-112">Wie unterscheiden sich die Szenarien?</span><span class="sxs-lookup"><span data-stu-id="7a087-112">So how are the scenarios different?</span></span> <span data-ttu-id="7a087-113">Es geht um das [Termin](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) Objekt, mit dem die Methode (für das verwaltete EWS-API) oder die in der Vorgangsanforderung enthaltene Element-ID (für EWS) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="7a087-113">It's all about the [Appointment](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) object used to invoke the method (for the EWS Managed API) or the item ID included in the operation request (for EWS).</span></span> <span data-ttu-id="7a087-114">Zum Löschen einer ganzen Datenreihe benötigen Sie das **Termin** Objekt oder die Element-ID für den wiederkehrenden Master.</span><span class="sxs-lookup"><span data-stu-id="7a087-114">To delete an entire series, you need the **Appointment** object or item ID for the recurring master.</span></span> <span data-ttu-id="7a087-115">Zum Löschen eines einzelnen Exemplars benötigen Sie das **Termin** Objekt oder die Element-ID für das vorkommen.</span><span class="sxs-lookup"><span data-stu-id="7a087-115">To delete a single occurrence, you need the **Appointment** object or item ID for the occurrence.</span></span> 
  
## <a name="delete-a-recurring-appointment-by-using-the-ews-managed-api"></a><span data-ttu-id="7a087-116">Löschen einer Terminserie mithilfe der verwaltete EWS-API</span><span class="sxs-lookup"><span data-stu-id="7a087-116">Delete a recurring appointment by using the EWS Managed API</span></span>

<span data-ttu-id="7a087-117">In diesem Beispiel wird davon ausgegangen, das Sie sich an einem Exchange-Server angemeldet haben und das [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt **service** erhalten haben.</span><span class="sxs-lookup"><span data-stu-id="7a087-117">This example assumes that you have authenticated to an Exchange server and have acquired an [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object named **service**.</span></span> <span data-ttu-id="7a087-118">Der _recurringItem_ -Parameter ist ein **Termin** Objekt für den wiederkehrenden Master oder ein einzelnes vorkommen.</span><span class="sxs-lookup"><span data-stu-id="7a087-118">The  _recurringItem_ parameter is an **Appointment** object for either the recurring master or a single occurrence.</span></span> <span data-ttu-id="7a087-119">Der Parameter _deleteEntireSeries_ gibt an, ob die gesamte Datenreihe gelöscht werden soll, in der das _recurringItem_ -Element enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="7a087-119">The  _deleteEntireSeries_ parameter indicates whether to delete the entire series that the  _recurringItem_ is a part of.</span></span> 
  
```cs
public static bool DeleteRecurringItem(ExchangeService service, Appointment recurringItem, bool deleteEntireSeries)
{
    Appointment appointmentToDelete = null;
    // If the item is a single appointment, fail.
    if (recurringItem.AppointmentType == AppointmentType.Single)
    {
        Console.WriteLine("ERROR: The item to delete is not part of a recurring series.");
        return false;
    }
    // Check the Appointment that was passed. Is it
    // an occurrence or the recurring master?
    if (recurringItem.AppointmentType == AppointmentType.RecurringMaster)
    {
        if (!deleteEntireSeries)
        {
            // The item is the recurring master, so deleting it will delete
            // the entire series. The caller indicated that the entire series
            // should not be deleted, so fail.
            Console.WriteLine("ERROR: The item to delete is the recurring master of the series. Deleting it will delete the entire series.");
            return false;
        }
        else
        {
            appointmentToDelete = recurringItem;
        }
    }
    else
    {
        if (deleteEntireSeries)
        {
            // The item passed is not the recurring master, but the caller
            // wants to delete the entire series. Bind to the recurring
            // master to delete it.
            try
            {
                appointmentToDelete = Appointment.BindToRecurringMaster(service, recurringItem.Id);
            }
            catch (Exception ex)
            {
                Console.WriteLine("ERROR: {0}", ex.Message);
                return false;
            }
        }
        else
        {
            // The item passed is not the recurring master, but the caller
            // only wants to delete the occurrence, so just
            // delete the passed item.
            appointmentToDelete = recurringItem;
        }
    }
    if (appointmentToDelete != null)
    {
        // Remove the item, depending on the scenario. 
        if (appointmentToDelete.IsMeeting)
        {
            CalendarActionResults results;
            // If it's a meeting and the user is the organizer, cancel it.
            // Determine this by testing the AppointmentState bitmask for 
            // the presence of the second bit. This bit indicates that the appointment
            // was received, which means that someone sent it to the user. Therefore,
            // they're not the organizer.
            int isReceived = 2;
            if ((appointmentToDelete.AppointmentState &amp; isReceived) == 0)
            {
                results = appointmentToDelete.CancelMeeting("Cancelling this meeting.");
                return true;
            }
            // If it's a meeting and the user is not the organizer, decline it.
            else
            {
                results = appointmentToDelete.Decline(true);
                return true;
            }
        }
        else
        {
            // The item isn't a meeting, so just delete it.
            appointmentToDelete.Delete(DeleteMode.MoveToDeletedItems);
            return true;
        }
    }
    return false;
}
```

<span data-ttu-id="7a087-120">Um dieses Beispiel verwenden zu können, müssen Sie an [ein vorkommen oder den wiederkehrenden Master binden](how-to-access-a-recurring-series-by-using-ews-in-exchange.md)und das resultierende **Termin** Objekt an die Methode übergeben.</span><span class="sxs-lookup"><span data-stu-id="7a087-120">In order to use this example, you need to [bind to either an occurrence or the recurring master](how-to-access-a-recurring-series-by-using-ews-in-exchange.md), and pass the resulting **Appointment** object to the method.</span></span> <span data-ttu-id="7a087-121">Beachten Sie, dass beim Zugriff auf Termine mithilfe einer [CalendarView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.calendarview%28v=exchg.80%29.aspx) -Klasse die resultierenden Elemente alle einzelnen Vorkommen sind.</span><span class="sxs-lookup"><span data-stu-id="7a087-121">Keep in mind that if you access appointments by using a [CalendarView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.calendarview%28v=exchg.80%29.aspx) class, the resulting items are all single occurrences.</span></span> <span data-ttu-id="7a087-122">Wenn Sie die [ItemView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview%28v=exchg.80%29.aspx) -Klasse verwenden, sind die resultierenden Elemente umgekehrt alle wiederkehrenden Master.</span><span class="sxs-lookup"><span data-stu-id="7a087-122">Conversely, if you use the [ItemView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview%28v=exchg.80%29.aspx) class, the resulting items are all recurring masters.</span></span> 
  
## <a name="delete-a-recurring-appointment-by-using-ews"></a><span data-ttu-id="7a087-123">Löschen einer Terminserie mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="7a087-123">Delete a recurring appointment by using EWS</span></span>

<span data-ttu-id="7a087-124">Das Löschen einer Terminserie mithilfe von EWS entspricht dem [Löschen einer Besprechung mit einer Einzelinstanz](how-to-delete-appointments-in-a-recurring-series-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="7a087-124">Deleting a recurring series by using EWS is the same as [deleting a single-instance meeting](how-to-delete-appointments-in-a-recurring-series-by-using-ews-in-exchange.md).</span></span> <span data-ttu-id="7a087-125">Tatsächlich nehmen die SOAP-Anforderungen dasselbe Format an.</span><span class="sxs-lookup"><span data-stu-id="7a087-125">In fact, the SOAP requests take the same format.</span></span> <span data-ttu-id="7a087-126">Der Schlüssel ist wiederum die Element-ID, die in der Anforderung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7a087-126">Again, the key is the item ID used in the request.</span></span> <span data-ttu-id="7a087-127">Wenn die Element-ID dem wiederkehrenden Master entspricht, wird die gesamte Datenreihe gelöscht.</span><span class="sxs-lookup"><span data-stu-id="7a087-127">If the item ID corresponds to the recurring master, the entire series will be deleted.</span></span> <span data-ttu-id="7a087-128">Wenn die Element-ID einem einzelnen Vorkommen entspricht, wird nur dieses vorkommen gelöscht.</span><span class="sxs-lookup"><span data-stu-id="7a087-128">If the item ID corresponds to a single occurrence, only that occurrence will be deleted.</span></span>
  
> [!NOTE]
> <span data-ttu-id="7a087-129">In den folgenden Codebeispielen werden die Attribute **ItemID**, **ChangeKey**und **RecurringMasterId** zur Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="7a087-129">In the code examples that follow, the **ItemId**, **ChangeKey**, and **RecurringMasterId** attributes are shortened for readability.</span></span> 
  
<span data-ttu-id="7a087-130">In diesem Beispiel wird der [CreateItem-Vorgang](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) mit einem [CancelCalendarItem](https://msdn.microsoft.com/library/a2046402-a176-44d5-b4b3-adb696581935%28Office.15%29.aspx) -Element verwendet, um eine Besprechung abzubrechen, für die der Benutzer der Organisator ist.</span><span class="sxs-lookup"><span data-stu-id="7a087-130">This example uses the [CreateItem operation](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) with a [CancelCalendarItem](https://msdn.microsoft.com/library/a2046402-a176-44d5-b4b3-adb696581935%28Office.15%29.aspx) element to cancel a meeting for which the user is the organizer.</span></span> <span data-ttu-id="7a087-131">Der Wert des [ReferenceItemId](https://msdn.microsoft.com/library/8fd4bb12-a94b-43f5-be3b-f435684e311d%28Office.15%29.aspx) -Elements gibt das Element an, das abgebrochen werden soll, und kann die Element-ID eines wiederkehrenden Masters oder eines einzelnen Exemplars sein.</span><span class="sxs-lookup"><span data-stu-id="7a087-131">The value of the [ReferenceItemId](https://msdn.microsoft.com/library/8fd4bb12-a94b-43f5-be3b-f435684e311d%28Office.15%29.aspx) element indicates the item to cancel, and can be the item ID of a recurring master or a single occurrence.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Eastern Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:CreateItem MessageDisposition="SendAndSaveCopy">
      <m:Items>
        <t:CancelCalendarItem>
          <t:ReferenceItemId Id="AAMkADA5..." ChangeKey="DwAAABYA..." />
          <t:NewBodyContent BodyType="HTML">Cancelling this meeting.</t:NewBodyContent>
        </t:CancelCalendarItem>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="7a087-132">In diesem Beispiel wird der **CreateItem-Vorgang** mit einem [DeclineItem](https://msdn.microsoft.com/library/2d8d2389-924e-4d03-a324-35d56cf0d6b1%28Office.15%29.aspx) -Element verwendet, um eine Besprechung abzulehnen, für die der Benutzer nicht der Organisator ist.</span><span class="sxs-lookup"><span data-stu-id="7a087-132">This example uses the **CreateItem operation** with a [DeclineItem](https://msdn.microsoft.com/library/2d8d2389-924e-4d03-a324-35d56cf0d6b1%28Office.15%29.aspx) element to decline a meeting for which the user is not the organizer.</span></span> <span data-ttu-id="7a087-133">Wie im vorherigen Beispiel gibt der Wert des **ReferenceItemId** -Elements das Element an, das abgelehnt werden soll, und kann die Element-ID eines wiederkehrenden Masters oder eines einzelnen Exemplars sein.</span><span class="sxs-lookup"><span data-stu-id="7a087-133">As in the previous example, the value of the **ReferenceItemId** element indicates the item to decline, and can be the item ID of a recurring master or a single occurrence.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Eastern Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:CreateItem MessageDisposition="SendAndSaveCopy">
      <m:Items>
        <t:DeclineItem>
          <t:ReferenceItemId Id="AAMkADA6..." ChangeKey="DwAAABYA..." />
        </t:DeclineItem>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="7a087-134">In diesem Beispiel wird der [DeleteItem-Vorgang](https://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) verwendet, um ein einzelnes Vorkommen eines Termins ohne Teilnehmer zu löschen.</span><span class="sxs-lookup"><span data-stu-id="7a087-134">This example uses the [DeleteItem operation](https://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) to delete a single occurrence of an appointment with no attendees.</span></span> <span data-ttu-id="7a087-135">Das zu löschende vorkommen wird durch das [OccurrenceItemId](https://msdn.microsoft.com/library/4a15bbc3-5b93-4193-b9ec-da32f0a9a552%28Office.15%29.aspx) -Element angegeben, das aus der Element-ID des wiederkehrenden Master-Objekts und dem Index des Vorkommens erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="7a087-135">The occurrence to delete is specified by the [OccurrenceItemId](https://msdn.microsoft.com/library/4a15bbc3-5b93-4193-b9ec-da32f0a9a552%28Office.15%29.aspx) element, which is constructed from the item ID of the recurring master and the index of the occurrence.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Eastern Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:DeleteItem DeleteType="MoveToDeletedItems" SendMeetingCancellations="SendToAllAndSaveCopy">
      <m:ItemIds>
        <t:OccurrenceItemId RecurringMasterId="AAMkADA8..." InstanceIndex="3" />
      </m:ItemIds>
    </m:DeleteItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="7a087-136">Beachten Sie, dass Sie dasselbe Ergebnis erhalten können, indem Sie das **OccurrenceItemId** -Element durch ein [ItemID](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) -Element ersetzen, das die Element-ID des Vorkommens enthält (siehe Abbildung).</span><span class="sxs-lookup"><span data-stu-id="7a087-136">Note that you can get the same result by replacing the **OccurrenceItemId** element with an [ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) element that contains the item ID of the occurrence, as shown.</span></span> 
  
```XML
<m:ItemIds>
  <t:ItemId Id="AAMkADA7..." ChangeKey="DwAAABYA..." />
</m:ItemIds>

```

## <a name="see-also"></a><span data-ttu-id="7a087-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a087-137">See also</span></span>


- [<span data-ttu-id="7a087-138">Serienmuster und EWS</span><span class="sxs-lookup"><span data-stu-id="7a087-138">Recurrence patterns and EWS</span></span>](recurrence-patterns-and-ews.md)
    
- [<span data-ttu-id="7a087-139">Zugreifen auf eine Terminserie mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="7a087-139">Access a recurring series by using EWS in Exchange</span></span>](how-to-access-a-recurring-series-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="7a087-140">Erstellen einer Terminserie mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="7a087-140">Create a recurring series by using EWS in Exchange</span></span>](how-to-create-a-recurring-series-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="7a087-141">Aktualisieren einer Terminserie mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="7a087-141">Update a recurring series by using EWS</span></span>](how-to-update-a-recurring-series-by-using-ews.md)
    
- [<span data-ttu-id="7a087-142">Aktualisieren einer Terminserie mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="7a087-142">Update a recurring series by using EWS in Exchange</span></span>](how-to-update-a-recurring-series-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="7a087-143">Kalender und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="7a087-143">Calendars and EWS in Exchange</span></span>](calendars-and-ews-in-exchange.md)
    
- [<span data-ttu-id="7a087-144">Erstellen von Terminen und Besprechungen mithilfe von EWS in Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="7a087-144">Create appointments and meetings by using EWS in Exchange 2013</span></span>](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [<span data-ttu-id="7a087-145">Löschen von Terminen und Absagen von Besprechungen mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="7a087-145">Delete appointments and cancel meetings by using EWS in Exchange</span></span>](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)
    

