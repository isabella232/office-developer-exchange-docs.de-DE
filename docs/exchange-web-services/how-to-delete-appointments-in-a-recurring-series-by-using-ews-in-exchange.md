---
title: Löschen der Termine in einer Terminserie mithilfe der EWS in Exchange
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a9d5244a-bc4a-4e9c-9c6c-ff361e04cbf8
description: Erfahren Sie, wie Termine in einer Terminserie löschen, indem Sie die EWS Managed API oder EWS in Exchange.
ms.openlocfilehash: 5e4d95058808adf8db159000bdf90c1f92945338
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756902"
---
# <a name="delete-appointments-in-a-recurring-series-by-using-ews-in-exchange"></a><span data-ttu-id="88f62-103">Löschen der Termine in einer Terminserie mithilfe der EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="88f62-103">Delete appointments in a recurring series by using EWS in Exchange</span></span>

<span data-ttu-id="88f62-104">Erfahren Sie, wie Termine in einer Terminserie löschen, indem Sie die EWS Managed API oder EWS in Exchange.</span><span class="sxs-lookup"><span data-stu-id="88f62-104">Learn how to delete appointments in a recurring series by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="88f62-105">Der EWS Managed API oder EWS können Sie eine Reihe von Terminen oder Besprechungen oder nur eine Instanz in der Datenreihe löschen.</span><span class="sxs-lookup"><span data-stu-id="88f62-105">You can use the EWS Managed API or EWS to delete a series of appointments or meetings, or just one instance in the series.</span></span> <span data-ttu-id="88f62-106">Der Prozess, mit denen Sie eine gesamte Datenreihe gelöscht ist im Wesentlichen identisch mit den Prozess, mit denen Sie nur ein einzelnes Element löschen.</span><span class="sxs-lookup"><span data-stu-id="88f62-106">The process you use to delete an entire series is essentially the same as the process you use to delete just a single occurrence.</span></span> <span data-ttu-id="88f62-107">Sie verwenden die gleichen EWS Managed API-Methoden oder EWS-Vorgänge, die Sie, um [eine einzelne Instanz Termin oder eine Besprechung zu löschen verwenden](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="88f62-107">You use the same EWS Managed API methods or EWS operations that you use to [delete a single instance appointment or meeting](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md).</span></span> <span data-ttu-id="88f62-108">Der Unterschied liegt in der Element-ID, die in der Methode oder der Vorgang enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="88f62-108">The difference is in the item ID that is included in the method or operation.</span></span> <span data-ttu-id="88f62-109">Zunächst betrachten, wie beide Szenarien identisch sind.</span><span class="sxs-lookup"><span data-stu-id="88f62-109">Let's start by looking at how both scenarios are the same.</span></span> 
  
<span data-ttu-id="88f62-110">Um eine Terminserie oder ein einzelnes Element in einer Terminserie löschen möchten, müssen Sie hier finden das Vorkommen oder die Serie, die Sie löschen möchten, und rufen Sie dann die entsprechende Methode oder der Vorgang zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="88f62-110">In order to delete a recurring series or a single occurrence in a recurring series, you need to find the occurrence or series that you want to delete, and then call the appropriate method or operation to remove it.</span></span> <span data-ttu-id="88f62-111">Während Sie einfach eine Art von Termin löschen können, wird empfohlen, alle Teilnehmer oder der Organisator auf dem aktuellen Stand halten und Besprechungen, die der Benutzer organisiert hat abzubrechen und Ablehnen von Besprechungen, die der Benutzer nicht organisiert.</span><span class="sxs-lookup"><span data-stu-id="88f62-111">While you can simply delete any type of appointment, we recommend that you keep any attendees or the organizer up to date and cancel meetings that the user has organized and decline meetings that the user did not organize.</span></span>
  
<span data-ttu-id="88f62-112">So unterscheiden sich wie die Szenarien?</span><span class="sxs-lookup"><span data-stu-id="88f62-112">So how are the scenarios different?</span></span> <span data-ttu-id="88f62-113">Es ist alles über [Appointment](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) -Objekts verwendet, um die-Methode (für die EWS Managed API) oder die Element-ID aufzurufen in die Operation Anforderung (EWS) enthalten.</span><span class="sxs-lookup"><span data-stu-id="88f62-113">It's all about the [Appointment](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) object used to invoke the method (for the EWS Managed API) or the item ID included in the operation request (for EWS).</span></span> <span data-ttu-id="88f62-114">Um eine gesamte Datenreihe zu löschen, benötigen Sie die **Appointment** -Objekt oder Element-ID für das wiederkehrende Master-Shape.</span><span class="sxs-lookup"><span data-stu-id="88f62-114">To delete an entire series, you need the **Appointment** object or item ID for the recurring master.</span></span> <span data-ttu-id="88f62-115">Um ein einzelnes Vorkommen löschen möchten, benötigen Sie die **Appointment** -Objekt oder Element-ID für das Vorkommen.</span><span class="sxs-lookup"><span data-stu-id="88f62-115">To delete a single occurrence, you need the **Appointment** object or item ID for the occurrence.</span></span> 
  
## <a name="delete-a-recurring-appointment-by-using-the-ews-managed-api"></a><span data-ttu-id="88f62-116">Löschen einer Terminserie mithilfe der EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="88f62-116">Delete a recurring appointment by using the EWS Managed API</span></span>

<span data-ttu-id="88f62-117">In diesem Beispiel wird davon ausgegangen, das Sie sich an einem Exchange-Server angemeldet haben und das [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt **service** erhalten haben.</span><span class="sxs-lookup"><span data-stu-id="88f62-117">This example assumes that you have authenticated to an Exchange server and have acquired an [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object named **service**.</span></span> <span data-ttu-id="88f62-118">Der Parameter _RecurringItem_ ist ein **Termin** -Objekt für das wiederkehrende Master-Shape oder ein einzelnes Vorkommen.</span><span class="sxs-lookup"><span data-stu-id="88f62-118">The  _recurringItem_ parameter is an **Appointment** object for either the recurring master or a single occurrence.</span></span> <span data-ttu-id="88f62-119">Der Parameter _DeleteEntireSeries_ gibt an, ob die gesamte Datenreihe gelöscht, denen die _RecurringItem_ gehört.</span><span class="sxs-lookup"><span data-stu-id="88f62-119">The  _deleteEntireSeries_ parameter indicates whether to delete the entire series that the  _recurringItem_ is a part of.</span></span> 
  
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

<span data-ttu-id="88f62-120">Um dieses Beispiel zu verwenden, um eine [Bindung an das Auftreten eines Serientermins oder wiederkehrenden Master](how-to-access-a-recurring-series-by-using-ews-in-exchange.md)müssen und resultierenden **Appointment** -Objekts an die-Methode übergeben.</span><span class="sxs-lookup"><span data-stu-id="88f62-120">In order to use this example, you need to [bind to either an occurrence or the recurring master](how-to-access-a-recurring-series-by-using-ews-in-exchange.md), and pass the resulting **Appointment** object to the method.</span></span> <span data-ttu-id="88f62-121">Beachten Sie, dass wenn Sie Termine mithilfe einer [CalendarView](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.calendarview%28v=exchg.80%29.aspx) -Klasse zugreifen, die resultierenden Elemente alle einzelnen Vorkommen werden beibehalten.</span><span class="sxs-lookup"><span data-stu-id="88f62-121">Keep in mind that if you access appointments by using a [CalendarView](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.calendarview%28v=exchg.80%29.aspx) class, the resulting items are all single occurrences.</span></span> <span data-ttu-id="88f62-122">Wenn Sie die [aufrufenArtikel aufrufen](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemview%28v=exchg.80%29.aspx) -Klasse verwenden, sind die resultierenden Elemente dagegen alle wiederkehrenden Master-Shapes.</span><span class="sxs-lookup"><span data-stu-id="88f62-122">Conversely, if you use the [ItemView](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemview%28v=exchg.80%29.aspx) class, the resulting items are all recurring masters.</span></span> 
  
## <a name="delete-a-recurring-appointment-by-using-ews"></a><span data-ttu-id="88f62-123">Löschen einer Terminserie mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="88f62-123">Delete a recurring appointment by using EWS</span></span>

<span data-ttu-id="88f62-124">Löschen einer Terminserie mit dem Exchange-Webdienste ist gleichbedeutend mit dem [Löschen einer Besprechung Einzel-Instanz](how-to-delete-appointments-in-a-recurring-series-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="88f62-124">Deleting a recurring series by using EWS is the same as [deleting a single-instance meeting](how-to-delete-appointments-in-a-recurring-series-by-using-ews-in-exchange.md).</span></span> <span data-ttu-id="88f62-125">Die SOAP-Anforderungen können Sie sogar das gleiche Format in Anspruch nehmen.</span><span class="sxs-lookup"><span data-stu-id="88f62-125">In fact, the SOAP requests take the same format.</span></span> <span data-ttu-id="88f62-126">In diesem Fall ist der Schlüssel die Element-ID in der Anforderung verwendet.</span><span class="sxs-lookup"><span data-stu-id="88f62-126">Again, the key is the item ID used in the request.</span></span> <span data-ttu-id="88f62-127">Wenn das wiederkehrende Master-Shape die Element-ID entspricht, wird die gesamte Datenreihe gelöscht.</span><span class="sxs-lookup"><span data-stu-id="88f62-127">If the item ID corresponds to the recurring master, the entire series will be deleted.</span></span> <span data-ttu-id="88f62-128">Wenn ein einzelnes Vorkommen die Element-ID entspricht, wird nur dieses auftreten gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="88f62-128">If the item ID corresponds to a single occurrence, only that occurrence will be deleted.</span></span>
  
> [!NOTE]
> <span data-ttu-id="88f62-129">In den folgenden Codebeispielen, werden die Attribute **ItemId**, **ChangeKey**und **RecurringMasterId** zur besseren Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="88f62-129">In the code examples that follow, the **ItemId**, **ChangeKey**, and **RecurringMasterId** attributes are shortened for readability.</span></span> 
  
<span data-ttu-id="88f62-130">In diesem Beispiel wird die [CreateItem-Vorgang](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) mit einem [CancelCalendarItem](http://msdn.microsoft.com/library/a2046402-a176-44d5-b4b3-adb696581935%28Office.15%29.aspx) -Element eine Besprechung absagen, bei der der Benutzer der Organisator ist.</span><span class="sxs-lookup"><span data-stu-id="88f62-130">This example uses the [CreateItem operation](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) with a [CancelCalendarItem](http://msdn.microsoft.com/library/a2046402-a176-44d5-b4b3-adb696581935%28Office.15%29.aspx) element to cancel a meeting for which the user is the organizer.</span></span> <span data-ttu-id="88f62-131">Der Wert des [ReferenceItemId](http://msdn.microsoft.com/library/8fd4bb12-a94b-43f5-be3b-f435684e311d%28Office.15%29.aspx) -Elements gibt an, das Element um abzubrechen, und die Element-ID ein wiederkehrendes Master-Shape oder ein einzelnes Vorkommen werden kann.</span><span class="sxs-lookup"><span data-stu-id="88f62-131">The value of the [ReferenceItemId](http://msdn.microsoft.com/library/8fd4bb12-a94b-43f5-be3b-f435684e311d%28Office.15%29.aspx) element indicates the item to cancel, and can be the item ID of a recurring master or a single occurrence.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="88f62-132">In diesem Beispiel wird die **CreateItem-Vorgang** mit einem Element [DeclineItem](http://msdn.microsoft.com/library/2d8d2389-924e-4d03-a324-35d56cf0d6b1%28Office.15%29.aspx) ablehnen eine Besprechung, für die der Benutzer nicht der Organisator ist.</span><span class="sxs-lookup"><span data-stu-id="88f62-132">This example uses the **CreateItem operation** with a [DeclineItem](http://msdn.microsoft.com/library/2d8d2389-924e-4d03-a324-35d56cf0d6b1%28Office.15%29.aspx) element to decline a meeting for which the user is not the organizer.</span></span> <span data-ttu-id="88f62-133">Wie im vorherigen Beispiel wird der Wert des **ReferenceItemId** -Elements gibt das Element an ablehnen möchten, und die Element-ID ein wiederkehrendes Master-Shape oder ein einzelnes Vorkommen werden kann.</span><span class="sxs-lookup"><span data-stu-id="88f62-133">As in the previous example, the value of the **ReferenceItemId** element indicates the item to decline, and can be the item ID of a recurring master or a single occurrence.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="88f62-134">In diesem Beispiel wird mit der [DeleteItem Vorgang](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) ein einzelnes Vorkommen eines Termins ohne Teilnehmer gelöscht.</span><span class="sxs-lookup"><span data-stu-id="88f62-134">This example uses the [DeleteItem operation](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) to delete a single occurrence of an appointment with no attendees.</span></span> <span data-ttu-id="88f62-135">Das Vorkommen löschen wird durch das [OccurrenceItemId](http://msdn.microsoft.com/library/4a15bbc3-5b93-4193-b9ec-da32f0a9a552%28Office.15%29.aspx) -Element angegeben, der aus der Element-ID des wiederkehrenden Master-Shapes und der Index des Vorkommens erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="88f62-135">The occurrence to delete is specified by the [OccurrenceItemId](http://msdn.microsoft.com/library/4a15bbc3-5b93-4193-b9ec-da32f0a9a552%28Office.15%29.aspx) element, which is constructed from the item ID of the recurring master and the index of the occurrence.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="88f62-136">Beachten Sie, dass Sie dasselbe Ergebnis abrufen können, indem das **OccurrenceItemId** -Element durch ein [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) -Element, das die Element-ID das Vorkommen enthält (siehe) ersetzt.</span><span class="sxs-lookup"><span data-stu-id="88f62-136">Note that you can get the same result by replacing the **OccurrenceItemId** element with an [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) element that contains the item ID of the occurrence, as shown.</span></span> 
  
```XML
<m:ItemIds>
  <t:ItemId Id="AAMkADA7..." ChangeKey="DwAAABYA..." />
</m:ItemIds>

```

## <a name="see-also"></a><span data-ttu-id="88f62-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="88f62-137">See also</span></span>


- [<span data-ttu-id="88f62-138">Serienmuster und EWS</span><span class="sxs-lookup"><span data-stu-id="88f62-138">Recurrence patterns and EWS</span></span>](recurrence-patterns-and-ews.md)
    
- [<span data-ttu-id="88f62-139">Zugriff auf eine Terminserie mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="88f62-139">Access a recurring series by using EWS in Exchange</span></span>](how-to-access-a-recurring-series-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="88f62-140">Erstellen einer Terminserie mithilfe der EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="88f62-140">Create a recurring series by using EWS in Exchange</span></span>](how-to-create-a-recurring-series-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="88f62-141">Aktualisieren einer Terminserie mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="88f62-141">Update a recurring series by using EWS</span></span>](how-to-update-a-recurring-series-by-using-ews.md)
    
- [<span data-ttu-id="88f62-142">Aktualisieren einer Terminserie mithilfe der EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="88f62-142">Update a recurring series by using EWS in Exchange</span></span>](how-to-update-a-recurring-series-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="88f62-143">Kalender und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="88f62-143">Calendars and EWS in Exchange</span></span>](calendars-and-ews-in-exchange.md)
    
- [<span data-ttu-id="88f62-144">Erstellen von Terminen und Besprechungen mithilfe von EWS in Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="88f62-144">Create appointments and meetings by using EWS in Exchange 2013</span></span>](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [<span data-ttu-id="88f62-145">Löschen von Terminen und Abbrechen an Besprechungen mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="88f62-145">Delete appointments and cancel meetings by using EWS in Exchange</span></span>](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)
    

