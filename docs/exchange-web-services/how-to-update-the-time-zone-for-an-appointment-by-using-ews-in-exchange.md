---
title: Aktualisieren Sie die Zeitzone für einen Termin im Exchange mithilfe der Exchange-Webdienste
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: dc2240c1-5500-4d5c-97d5-09d63ffd30d5
description: Hier erfahren Sie, wie die Zeitzone für einen Termin oder eine Besprechung zu aktualisieren, und verwenden die EWS Managed API oder EWS in Exchange.
ms.openlocfilehash: 535eb9f546d9a4353408579f3a24750f32237699
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757010"
---
# <a name="update-the-time-zone-for-an-appointment-by-using-ews-in-exchange"></a><span data-ttu-id="65b2d-103">Aktualisieren Sie die Zeitzone für einen Termin im Exchange mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="65b2d-103">Update the time zone for an appointment by using EWS in Exchange</span></span>

<span data-ttu-id="65b2d-104">Hier erfahren Sie, wie die Zeitzone für einen Termin oder eine Besprechung zu aktualisieren, und verwenden die EWS Managed API oder EWS in Exchange.</span><span class="sxs-lookup"><span data-stu-id="65b2d-104">Learn how to update the time zone for an existing appointment or meeting by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="65b2d-105">Beim Erstellen eines Termins oder einer Besprechung auf einem Exchange-Kalender wird die Zeitzone verwendet, um die Anfangs- und Endzeiten angeben als Zeitzone für den Termin Erstellung gespeichert.</span><span class="sxs-lookup"><span data-stu-id="65b2d-105">When an appointment or meeting is created on an Exchange calendar, the time zone used to specify the start and end times is saved as the creation time zone for the appointment.</span></span> <span data-ttu-id="65b2d-106">Sie können diese Zeitzone mithilfe der EWS Managed API oder EWS ändern.</span><span class="sxs-lookup"><span data-stu-id="65b2d-106">You can change that time zone by using the EWS Managed API or EWS.</span></span> <span data-ttu-id="65b2d-107">Ändern der Zeitzone für einen Termin hat jedoch anderer Effekte auf dem Zeitpunkt der Start- und Endzeit des Termins.</span><span class="sxs-lookup"><span data-stu-id="65b2d-107">However, changing the time zone on an appointment has other effects on the start and end time of the appointment.</span></span>
  
<span data-ttu-id="65b2d-108">Zeitwerte werden auf dem Exchange-Server als koordinieren Weltzeit (UTC) gespeichert.</span><span class="sxs-lookup"><span data-stu-id="65b2d-108">Time values are stored on the Exchange server in Coordinate Universal Time (UTC).</span></span> <span data-ttu-id="65b2d-109">In diesem Fall 1:00 Uhr (13:00) Eastern Standard Time-Zone starten ein Termins festgelegt ist (UTC-05:00), dass der Wert als 6:00 Uhr (18:00) gespeichert wird, auf dem Server, vorausgesetzt, dass die Zeitzone in der Phase der Standardzeit ist.</span><span class="sxs-lookup"><span data-stu-id="65b2d-109">So if an appointment is set to start at 1:00 PM (13:00) in the Eastern time zone (UTC-05:00), that value is stored as 6:00 PM (18:00) on the server, assuming that the time zone is in its standard time phase.</span></span> <span data-ttu-id="65b2d-110">Wenn eines Termins in anderen Zeitzonen angezeigt wird, wird die entsprechende Anzahl von Stunden hinzugefügt oder entfernt der UTC-Wert, der die Zeitzone-spezifischen Zeit zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="65b2d-110">When that appointment is viewed in other time zones, the appropriate number of hours is added or subtracted from the UTC value to determine the time zone-specific time.</span></span> <span data-ttu-id="65b2d-111">Angenommen, ein Termin eine Startzeit 1:00 Uhr weist Eastern (18:00 Uhr UTC), und von einem Client in der Pacific Standard Time-Zone angezeigt wird (UTC-08:00), das Zeitzone spezifische Startzeit für der Client 10:00 Uhr (18:00-08:00) wäre.</span><span class="sxs-lookup"><span data-stu-id="65b2d-111">For example, if an appointment has a start time at 1:00 PM Eastern (6:00 PM UTC), and is viewed from a client in the Pacific time zone (UTC-08:00), the time-zone specific start time for that client would be 10:00 AM (18:00 - 08:00).</span></span>
  
<span data-ttu-id="65b2d-112">Wenn Sie die Zeitzone des Termins aktualisieren, ohne die Start- und Endzeit Zeit aktualisieren, aktualisiert der Server die UTC-Werte gespeichert werden, auf dem Server, um die Start- und Endzeit Zeit als die gleichen Zeitzone-spezifischen Zeiten beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="65b2d-112">When you update the time zone of the appointment without updating the start and end time, the server updates the UTC values stored on the server to keep the start and end time as the same time zone-specific times.</span></span> <span data-ttu-id="65b2d-113">Angenommen Sie, den 1:00 Uhr Eastern Termin.</span><span class="sxs-lookup"><span data-stu-id="65b2d-113">For example, consider the 1:00 PM Eastern appointment.</span></span> <span data-ttu-id="65b2d-114">Die Zeit wird als 18:00 Uhr UTC auf dem Server gespeichert.</span><span class="sxs-lookup"><span data-stu-id="65b2d-114">The time is stored as 18:00 UTC on the server.</span></span> <span data-ttu-id="65b2d-115">Wenn die Zeitzone des Termins in der Pacific Standard Time-Zone geändert wird, verschiebt der Server die Startzeit für 1:00 Uhr Pacific (21:00 Uhr UTC).</span><span class="sxs-lookup"><span data-stu-id="65b2d-115">If the time zone of the appointment is changed to the Pacific time zone, the server shifts the start time to 1:00 PM Pacific (21:00 UTC).</span></span>
  
<span data-ttu-id="65b2d-116">Sie können dieses Verhalten ändern, indem Sie explizit festlegen der Start- und Endzeiten.</span><span class="sxs-lookup"><span data-stu-id="65b2d-116">You can change this behavior by explicitly setting the start and end times.</span></span>
  
## <a name="updating-the-time-zone-on-an-existing-appointment-by-using-the-ews-managed-api"></a><span data-ttu-id="65b2d-117">Aktualisieren die Zeitzone auf einen vorhandenen Termin mithilfe der EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="65b2d-117">Updating the time zone on an existing appointment by using the EWS Managed API</span></span>

<span data-ttu-id="65b2d-118">Im folgenden Beispiel wird die EWS Managed API verwendet, so aktualisieren Sie die Zeitzone auf einen vorhandenen Termin in der zentralen Zeitzone durch Aktualisieren der **Appointment.StartTimeZone** und **Appointment.EndTimeZone** -Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="65b2d-118">In the following example, the EWS Managed API is used to update the time zone on an existing appointment to the Central time zone by updating the **Appointment.StartTimeZone** and **Appointment.EndTimeZone** properties.</span></span> <span data-ttu-id="65b2d-119">Wenn der Parameter _ShiftAppointnment_ auf **true**festgelegt ist, festgelegt der Code nicht explizit die Anfangs- und Endzeiten für den Termin.</span><span class="sxs-lookup"><span data-stu-id="65b2d-119">If the  _shiftAppointnment_ parameter is set to **true**, the code does not explicitly set the start and end times on the appointment.</span></span> <span data-ttu-id="65b2d-120">In diesem Fall werden der Server die Anfangs- und Endzeiten zum aufbewahren zur gleichen Zeit relativ zur Zeitzone in die neue Zeitzone verschoben.</span><span class="sxs-lookup"><span data-stu-id="65b2d-120">In this case, the server will shift the start and end times to keep them at the same time zone-relative times in the new time zone.</span></span> <span data-ttu-id="65b2d-121">Wenn Festlegung auf **"false"**, mit dem Code die Anfangs- und Endzeiten explizit um behalten den Termin zur selben Zeit in UTC konvertiert.</span><span class="sxs-lookup"><span data-stu-id="65b2d-121">If set to **false**, the code converts the start and end times explicitly to keep the appointment at the same time in UTC.</span></span> 

<span data-ttu-id="65b2d-122">In diesem Beispiel wird davon ausgegangen, dass das **ExchangeService**-Objekt mit gültigen Werten in den [Credentials](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx)- und [Url](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx)-Eigenschaften initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="65b2d-122">This example assumes that the **ExchangeService** object has been initialized with valid values in the [Credentials](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) and [Url](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) properties.</span></span> 
  
```cs
static void UpdateAppointmentTimeZone(ExchangeService service, ItemId apptId, bool shiftAppointment)
{
    PropertySet includeTimeZones = new PropertySet(AppointmentSchema.Subject,
                                                   AppointmentSchema.Start,
                                                   AppointmentSchema.ReminderDueBy,
                                                   AppointmentSchema.End,
                                                   AppointmentSchema.StartTimeZone,
                                                   AppointmentSchema.EndTimeZone);
    Appointment apptToUpdate;
    // Load the existing appointment.
    // This will result in a call to EWS.
    try
    {
        apptToUpdate = Appointment.Bind(service, apptId, includeTimeZones);
    }
    catch (Exception ex)
    {
        Console.WriteLine("Error retrieving existing appointment: {0}", ex.Message);
        return;
    }
    Console.WriteLine("Before update:");
    // Output the current start, reminder, end, and time zones.
    Console.WriteLine("  Start: {0}", apptToUpdate.Start);
    Console.WriteLine("  Start time zone: {0}", apptToUpdate.StartTimeZone.DisplayName);
    Console.WriteLine("  Reminder: {0}", apptToUpdate.ReminderDueBy);
    Console.WriteLine("  End: {0}", apptToUpdate.End);
    Console.WriteLine("  End time zone: {0}", apptToUpdate.EndTimeZone.DisplayName);
    // Retrieve the Central time zone.
    TimeZoneInfo centralTZ = TimeZoneInfo.FindSystemTimeZoneById("Central Standard Time");
    // Update the time zones on the appointment.
    apptToUpdate.StartTimeZone = centralTZ;
    apptToUpdate.EndTimeZone = centralTZ;
    if (!shiftAppointment)
    {
        // Set the start and end times explicitly so that the appointment
        // will start and end at the same UTC time.
        // Convert the times to then Central time zone. This
        // will keep them at the same time in UTC.
        // For example, 1:00 PM Eastern becomes 12:00 PM Central.
        DateTime newStartTime = TimeZoneInfo.ConvertTime(
            apptToUpdate.Start, centralTZ);
        DateTime newEndTime = TimeZoneInfo.ConvertTime(
            apptToUpdate.End, centralTZ);
        apptToUpdate.Start = newStartTime;
        apptToUpdate.End = newEndTime;
    }
    try
    {
        // Save the changes. This will result in a call to EWS.
        apptToUpdate.Update(ConflictResolutionMode.AlwaysOverwrite, 
            SendInvitationsOrCancellationsMode.SendToNone);
    }
    catch (Exception ex)
    {
        Console.WriteLine("Error updating appointment: {0}", ex.Message);
        return;
    }
    // Now rebind to the appointment to get the new values.
    Appointment apptAfterUpdate;
    
    try
    {
        // This will result in a call to EWS.
        apptAfterUpdate = Appointment.Bind(service, apptId, includeTimeZones);
    }
    catch (Exception ex)
    {
        Console.WriteLine("Error retrieving existing appointment: {0}", ex.Message);
        return;
    }
    Console.WriteLine("After update:");
    // Output the current start, reminder, end, and time zones.
    Console.WriteLine("  Start: {0}", apptAfterUpdate.Start);
    Console.WriteLine("  Start time zone: {0}", apptAfterUpdate.StartTimeZone.DisplayName);
    Console.WriteLine("  Reminder: {0}", apptAfterUpdate.ReminderDueBy);
    Console.WriteLine("  End: {0}", apptAfterUpdate.End);
    Console.WriteLine("  End time zone: {0}", apptAfterUpdate.EndTimeZone.DisplayName);
}
```

<span data-ttu-id="65b2d-123">Wenn im Beispiel verwendet wird, um einen Termin zu aktualisieren, die 1:00 Uhr beginnt Eastern und 2:00 Uhr endet Eastern, mit dem Parameter _ShiftAppointment_ auf True festgelegt, und die [ExchangeService.TimeZone](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice.timezone%28v=exchg.80%29.aspx) -Eigenschaft legen Sie auf der Eastern Time-Zone, die Ausgabe sieht wie folgt.</span><span class="sxs-lookup"><span data-stu-id="65b2d-123">When the example is used to update an appointment that starts at 1:00 PM Eastern and ends at 2:00 PM Eastern, with the  _shiftAppointment_ parameter set to true, and the [ExchangeService.TimeZone](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice.timezone%28v=exchg.80%29.aspx) property set to the Eastern time zone, the output looks like the following.</span></span> 
  
```MS-DOS
Before update:
  Start: 6/20/2014 1:00:00 PM
  Start time zone: (UTC-05:00) Eastern Time (US &amp; Canada)
  Reminder: 6/20/2014 1:00:00 PM
  End: 6/20/2014 2:00:00 PM
  End time zone: (UTC-05:00) Eastern Time (US &amp; Canada)
After update:
  Start: 6/20/2014 2:00:00 PM
  Start time zone: (UTC-06:00) Central Time (US &amp; Canada)
  Reminder: 6/20/2014 2:00:00 PM
  End: 6/20/2014 3:00:00 PM
  End time zone: (UTC-06:00) Central Time (US &amp; Canada)
```

<span data-ttu-id="65b2d-124">Wenn im Beispiel verwendet wird, derselben Terminserie mit dem _ShiftAppointment_ -Parameter auf False festgelegt und mit der **TimeZone** -Eigenschaft legen Sie erneut auf die Eastern Standard Time-Zone aktualisieren, sieht die Ausgabe ein wenig anders aus.</span><span class="sxs-lookup"><span data-stu-id="65b2d-124">When the example is used to update the same appointment with the  _shiftAppointment_ parameter set to false, and with the **TimeZone** property again set to the Eastern time zone, the output looks a little different.</span></span> 
  
```MS-DOS
Before update:
  Start: 6/20/2014 1:00:00 PM
  Start time zone: (UTC-05:00) Eastern Time (US &amp; Canada)
  Reminder: 6/20/2014 1:00:00 PM
  End: 6/20/2014 2:00:00 PM
  End time zone: (UTC-05:00) Eastern Time (US &amp; Canada)
After update:
  Start: 6/20/2014 1:00:00 PM
  Start time zone: (UTC-06:00) Central Time (US &amp; Canada)
  Reminder: 6/20/2014 1:00:00 PM
  End: 6/20/2014 2:00:00 PM
  End time zone: (UTC-06:00) Central Time (US &amp; Canada)
```

<span data-ttu-id="65b2d-125">Beachten Sie, dass die Anfangs- und Endzeiten nicht geändert haben.</span><span class="sxs-lookup"><span data-stu-id="65b2d-125">Notice that the start and end times did not change.</span></span> <span data-ttu-id="65b2d-126">Dies ist, da die Zeiten in der Eastern Zeit interpretiert werden zone (, da die Eigenschaft **"TimeZone"** Eastern Standard Time-Zone festgelegt ist), und die Zeitwerte wurden aktualisiert, um zu verhindern, dass den Termin verschoben.</span><span class="sxs-lookup"><span data-stu-id="65b2d-126">This is because the times are being interpreted in the Eastern time zone (because the **TimeZone** property is set to the Eastern time zone), and the time values were updated to prevent the appointment from shifting.</span></span> 
  
## <a name="updating-the-time-zone-on-an-existing-appointment-by-using-ews"></a><span data-ttu-id="65b2d-127">Aktualisieren die Zeitzone auf einen vorhandenen Termin mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="65b2d-127">Updating the time zone on an existing appointment by using EWS</span></span>

<span data-ttu-id="65b2d-128">Das folgende Beispiel EWS- [Vorgang UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) Anforderung aktualisiert die Zeitzone für einen Termin.</span><span class="sxs-lookup"><span data-stu-id="65b2d-128">The following example EWS [UpdateItem operation](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) request updates the time zone on an appointment.</span></span> <span data-ttu-id="65b2d-129">In diesem Beispiel wird aktualisiert nur die Elemente [StartTimeZone](http://msdn.microsoft.com/library/d38c4dc1-4ecb-42a1-8d57-a451b16a2de2%28Office.15%29.aspx) und [EndTimeZone](http://msdn.microsoft.com/library/6c53c337-be60-4d22-9e9e-a0c140c5e913%28Office.15%29.aspx) , sodass der Server die Anfangs- und Endzeiten des Termins aufrechtzuerhalten gleichzeitig Time-Zone-Relative in die neue Zeitzone verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="65b2d-129">This example only updates the [StartTimeZone](http://msdn.microsoft.com/library/d38c4dc1-4ecb-42a1-8d57-a451b16a2de2%28Office.15%29.aspx) and [EndTimeZone](http://msdn.microsoft.com/library/6c53c337-be60-4d22-9e9e-a0c140c5e913%28Office.15%29.aspx) elements, so the server will shift the start and end times of the appointment to keep it at the same time-zone-relative time in the new time zone.</span></span> <span data-ttu-id="65b2d-130">Der Wert des Elements **ItemId** wird zur besseren Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="65b2d-130">The value of the **ItemId** element is shortened for readability.</span></span> 
  
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
    <m:UpdateItem ConflictResolution="AlwaysOverwrite" SendMeetingInvitationsOrCancellations="SendToNone">
      <m:ItemChanges>
        <t:ItemChange>
          <t:ItemId Id="AAMkADA5..." ChangeKey="DwAAABYA..." />
          <t:Updates>
            <t:SetItemField>
              <t:FieldURI FieldURI="calendar:StartTimeZone" />
              <t:CalendarItem>
                <t:StartTimeZone Id="Central Standard Time" />
              </t:CalendarItem>
            </t:SetItemField>
            <t:SetItemField>
              <t:FieldURI FieldURI="calendar:EndTimeZone" />
              <t:CalendarItem>
                <t:EndTimeZone Id="Central Standard Time" />
              </t:CalendarItem>
            </t:SetItemField>
          </t:Updates>
        </t:ItemChange>
      </m:ItemChanges>
    </m:UpdateItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="65b2d-131">Die folgende Beispiel für eine Anforderung aktualisiert die Zeitzone des Termins, und auch die Anfangs- und Endzeiten aktualisiert, indem die **Start** und **End** Elemente explizit festlegen.</span><span class="sxs-lookup"><span data-stu-id="65b2d-131">The following example request updates the time zone of the appointment, and also updates the start and end times by explicitly setting the **Start** and **End** elements.</span></span> <span data-ttu-id="65b2d-132">Der Wert des Elements **ItemId** wird zur besseren Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="65b2d-132">The value of the **ItemId** element is shortened for readability.</span></span> 
  
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
    <m:UpdateItem ConflictResolution="AlwaysOverwrite" SendMeetingInvitationsOrCancellations="SendToNone">
      <m:ItemChanges>
        <t:ItemChange>
          <t:ItemId Id="AAMkADA5..." ChangeKey="DwAAABYA..." />
          <t:Updates>
            <t:SetItemField>
              <t:FieldURI FieldURI="calendar:StartTimeZone" />
              <t:CalendarItem>
                <t:StartTimeZone Id="Central Standard Time" />
              </t:CalendarItem>
            </t:SetItemField>
            <t:SetItemField>
              <t:FieldURI FieldURI="calendar:EndTimeZone" />
              <t:CalendarItem>
                <t:EndTimeZone Id="Central Standard Time" />
              </t:CalendarItem>
            </t:SetItemField>
            <t:SetItemField>
              <t:FieldURI FieldURI="calendar:Start" />
              <t:CalendarItem>
                <t:Start>2014-06-20T17:00:00.000Z</t:Start>
              </t:CalendarItem>
            </t:SetItemField>
            <t:SetItemField>
              <t:FieldURI FieldURI="calendar:End" />
              <t:CalendarItem>
                <t:End>2014-06-20T18:00:00.000Z</t:End>
              </t:CalendarItem>
            </t:SetItemField>
          </t:Updates>
        </t:ItemChange>
      </m:ItemChanges>
    </m:UpdateItem>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="65b2d-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="65b2d-133">See also</span></span>

- [<span data-ttu-id="65b2d-134">Zeitzonen und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="65b2d-134">Time zones and EWS in Exchange</span></span>](time-zones-and-ews-in-exchange.md)   
- [<span data-ttu-id="65b2d-135">Erstellen von Terminen in einer bestimmten Zeitzone mithilfe der EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="65b2d-135">Create appointments in a specific time zone by using EWS in Exchange</span></span>](how-to-create-appointments-in-a-specific-time-zone-by-using-ews-in-exchange.md)   
- [<span data-ttu-id="65b2d-136">Aktualisieren von Terminen und Besprechungen mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="65b2d-136">Update appointments and meetings by using EWS in Exchange</span></span>](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)
    

