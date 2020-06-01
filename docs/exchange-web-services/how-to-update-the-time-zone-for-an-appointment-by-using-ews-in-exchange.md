---
title: Aktualisieren der Zeitzone für einen Termin mithilfe von EWS in Exchange
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: dc2240c1-5500-4d5c-97d5-09d63ffd30d5
description: Erfahren Sie, wie Sie die Zeitzone für einen vorhandenen Termin oder eine Besprechung mithilfe der verwaltete EWS-API oder EWS in Exchange aktualisieren.
ms.openlocfilehash: 064f99997b7c3d1197cb8d1ee6a24f8fb874f706
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455842"
---
# <a name="update-the-time-zone-for-an-appointment-by-using-ews-in-exchange"></a><span data-ttu-id="0dd92-103">Aktualisieren der Zeitzone für einen Termin mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="0dd92-103">Update the time zone for an appointment by using EWS in Exchange</span></span>

<span data-ttu-id="0dd92-104">Erfahren Sie, wie Sie die Zeitzone für einen vorhandenen Termin oder eine Besprechung mithilfe der verwaltete EWS-API oder EWS in Exchange aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="0dd92-104">Learn how to update the time zone for an existing appointment or meeting by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="0dd92-105">Wenn ein Termin oder eine Besprechung in einem Exchange-Kalender erstellt wird, wird die Zeitzone, die zum Angeben der Start-und Endzeit verwendet wird, als Erstellungs Zeitzone für den Termin gespeichert.</span><span class="sxs-lookup"><span data-stu-id="0dd92-105">When an appointment or meeting is created on an Exchange calendar, the time zone used to specify the start and end times is saved as the creation time zone for the appointment.</span></span> <span data-ttu-id="0dd92-106">Sie können diese Zeitzone mithilfe der verwaltete EWS-API oder EWS ändern.</span><span class="sxs-lookup"><span data-stu-id="0dd92-106">You can change that time zone by using the EWS Managed API or EWS.</span></span> <span data-ttu-id="0dd92-107">Das Ändern der Zeitzone eines Termins hat jedoch andere Auswirkungen auf die Anfangs-und Endzeit des Termins.</span><span class="sxs-lookup"><span data-stu-id="0dd92-107">However, changing the time zone on an appointment has other effects on the start and end time of the appointment.</span></span>
  
<span data-ttu-id="0dd92-108">Zeitwerte werden auf dem Exchange-Server in Coordinate Universal Time (UTC) gespeichert.</span><span class="sxs-lookup"><span data-stu-id="0dd92-108">Time values are stored on the Exchange server in Coordinate Universal Time (UTC).</span></span> <span data-ttu-id="0dd92-109">Wenn also ein Termin für den Start um 1:00 Uhr (13:00) in der Eastern Time-Zone (UTC-05:00) festgelegt ist, wird dieser Wert auf dem Server als 6:00 pm (18:00) gespeichert, vorausgesetzt, die Zeitzone befindet sich in der Standardzeit Phase.</span><span class="sxs-lookup"><span data-stu-id="0dd92-109">So if an appointment is set to start at 1:00 PM (13:00) in the Eastern time zone (UTC-05:00), that value is stored as 6:00 PM (18:00) on the server, assuming that the time zone is in its standard time phase.</span></span> <span data-ttu-id="0dd92-110">Wenn dieser Termin in anderen Zeitzonen angezeigt wird, wird die entsprechende Anzahl von Stunden vom UTC-Wert hinzugefügt oder subtrahiert, um die Zeitzonenspezifische Zeit zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="0dd92-110">When that appointment is viewed in other time zones, the appropriate number of hours is added or subtracted from the UTC value to determine the time zone-specific time.</span></span> <span data-ttu-id="0dd92-111">Wenn beispielsweise ein Termin um 1:00 Uhr Eastern (6:00 Uhr UTC) beginnt und von einem Client in der Pacific Time Zone (UTC-08:00) angezeigt wird, lautet die Zeitzonenspezifische Startzeit für diesen Client 10:00 am (18:00-08:00).</span><span class="sxs-lookup"><span data-stu-id="0dd92-111">For example, if an appointment has a start time at 1:00 PM Eastern (6:00 PM UTC), and is viewed from a client in the Pacific time zone (UTC-08:00), the time-zone specific start time for that client would be 10:00 AM (18:00 - 08:00).</span></span>
  
<span data-ttu-id="0dd92-112">Wenn Sie die Zeitzone des Termins aktualisieren, ohne die Anfangs-und Endzeit zu aktualisieren, aktualisiert der Server die auf dem Server gespeicherten UTC-Werte, um die Start-und Endzeit als Zeitzonenspezifische Zeiten beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="0dd92-112">When you update the time zone of the appointment without updating the start and end time, the server updates the UTC values stored on the server to keep the start and end time as the same time zone-specific times.</span></span> <span data-ttu-id="0dd92-113">Nehmen Sie beispielsweise den 1:00 PM Eastern-Termin in Frage.</span><span class="sxs-lookup"><span data-stu-id="0dd92-113">For example, consider the 1:00 PM Eastern appointment.</span></span> <span data-ttu-id="0dd92-114">Die Uhrzeit wird auf dem Server als 18:00 UTC gespeichert.</span><span class="sxs-lookup"><span data-stu-id="0dd92-114">The time is stored as 18:00 UTC on the server.</span></span> <span data-ttu-id="0dd92-115">Wenn die Zeitzone des Termins in die Zeitzone Pacific Time geändert wird, verschiebt der Server die Startzeit auf 1:00 Uhr Pacific (21:00 UTC).</span><span class="sxs-lookup"><span data-stu-id="0dd92-115">If the time zone of the appointment is changed to the Pacific time zone, the server shifts the start time to 1:00 PM Pacific (21:00 UTC).</span></span>
  
<span data-ttu-id="0dd92-116">Sie können dieses Verhalten ändern, indem Sie die Anfangs-und Endzeiten explizit festlegen.</span><span class="sxs-lookup"><span data-stu-id="0dd92-116">You can change this behavior by explicitly setting the start and end times.</span></span>
  
## <a name="updating-the-time-zone-on-an-existing-appointment-by-using-the-ews-managed-api"></a><span data-ttu-id="0dd92-117">Aktualisieren der Zeitzone eines vorhandenen Termins mithilfe der verwaltete EWS-API</span><span class="sxs-lookup"><span data-stu-id="0dd92-117">Updating the time zone on an existing appointment by using the EWS Managed API</span></span>

<span data-ttu-id="0dd92-118">Im folgenden Beispiel wird der verwaltete EWS-API verwendet, um die Zeitzone eines vorhandenen Termins in die zentrale Zeitzone zu aktualisieren, indem die Eigenschaften **Termin. StartTimeZone** und **Termin. EndTimeZone** aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="0dd92-118">In the following example, the EWS Managed API is used to update the time zone on an existing appointment to the Central time zone by updating the **Appointment.StartTimeZone** and **Appointment.EndTimeZone** properties.</span></span> <span data-ttu-id="0dd92-119">Wenn der Parameter _shiftAppointnment_ auf **true**festgelegt ist, wird der Code nicht explizit die Start-und Endzeit für den Termin festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0dd92-119">If the  _shiftAppointnment_ parameter is set to **true**, the code does not explicitly set the start and end times on the appointment.</span></span> <span data-ttu-id="0dd92-120">In diesem Fall verschiebt der Server die Start-und Endzeiten, um Sie in der neuen Zeitzone gleichzeitig zu den relativen Zeitpunkten zu halten.</span><span class="sxs-lookup"><span data-stu-id="0dd92-120">In this case, the server will shift the start and end times to keep them at the same time zone-relative times in the new time zone.</span></span> <span data-ttu-id="0dd92-121">Bei Festlegung auf " **false**" wandelt der Code die Anfangs-und Endzeiten explizit um, damit der Termin in der UTC gleichzeitig bleibt.</span><span class="sxs-lookup"><span data-stu-id="0dd92-121">If set to **false**, the code converts the start and end times explicitly to keep the appointment at the same time in UTC.</span></span> 

<span data-ttu-id="0dd92-122">In diesem Beispiel wird davon ausgegangen, dass das **ExchangeService**-Objekt mit gültigen Werten in den [Credentials](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx)- und [Url](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx)-Eigenschaften initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="0dd92-122">This example assumes that the **ExchangeService** object has been initialized with valid values in the [Credentials](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) and [Url](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) properties.</span></span> 
  
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

<span data-ttu-id="0dd92-123">Wenn das Beispiel zum Aktualisieren eines Termins verwendet wird, der um 1:00 Uhr Ost beginnt und um 2:00 Uhr Eastern endet, wobei der _shiftAppointment_ -Parameter auf true festgelegt ist und die [Datei "ExchangeService. TimeZone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.timezone%28v=exchg.80%29.aspx) -Eigenschaft auf die Eastern Time-Zone festgelegt ist, sieht die Ausgabe wie folgt aus.</span><span class="sxs-lookup"><span data-stu-id="0dd92-123">When the example is used to update an appointment that starts at 1:00 PM Eastern and ends at 2:00 PM Eastern, with the  _shiftAppointment_ parameter set to true, and the [ExchangeService.TimeZone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.timezone%28v=exchg.80%29.aspx) property set to the Eastern time zone, the output looks like the following.</span></span> 
  
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

<span data-ttu-id="0dd92-124">Wenn das Beispiel verwendet wird, um den gleichen Termin mit dem _shiftAppointment_ -Parameter auf "false" zu aktualisieren, und wenn die **TimeZone** -Eigenschaft erneut auf die Eastern Time-Zone festgelegt wurde, sieht die Ausgabe etwas anders aus.</span><span class="sxs-lookup"><span data-stu-id="0dd92-124">When the example is used to update the same appointment with the  _shiftAppointment_ parameter set to false, and with the **TimeZone** property again set to the Eastern time zone, the output looks a little different.</span></span> 
  
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

<span data-ttu-id="0dd92-125">Beachten Sie, dass sich die Anfangs-und Endzeiten nicht geändert haben.</span><span class="sxs-lookup"><span data-stu-id="0dd92-125">Notice that the start and end times did not change.</span></span> <span data-ttu-id="0dd92-126">Dies liegt daran, dass die Zeiten in der östlichen Zeitzone interpretiert werden (da die **TimeZone** -Eigenschaft auf die Eastern Time-Zone festgelegt ist), und die Zeitwerte wurden aktualisiert, um zu verhindern, dass der Termin verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="0dd92-126">This is because the times are being interpreted in the Eastern time zone (because the **TimeZone** property is set to the Eastern time zone), and the time values were updated to prevent the appointment from shifting.</span></span> 
  
## <a name="updating-the-time-zone-on-an-existing-appointment-by-using-ews"></a><span data-ttu-id="0dd92-127">Aktualisieren der Zeitzone eines vorhandenen Termins mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="0dd92-127">Updating the time zone on an existing appointment by using EWS</span></span>

<span data-ttu-id="0dd92-128">Im folgenden Beispiel für die EWS- [UpdateItem-Vorgangs](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) Anforderung wird die Zeitzone eines Termins aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="0dd92-128">The following example EWS [UpdateItem operation](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) request updates the time zone on an appointment.</span></span> <span data-ttu-id="0dd92-129">In diesem Beispiel werden nur die [StartTimeZone](https://msdn.microsoft.com/library/d38c4dc1-4ecb-42a1-8d57-a451b16a2de2%28Office.15%29.aspx) -und [EndTimeZone](https://msdn.microsoft.com/library/6c53c337-be60-4d22-9e9e-a0c140c5e913%28Office.15%29.aspx) -Elemente aktualisiert, sodass der Server die Start-und Endzeit des Termins verschiebt, um ihn zur gleichen Zeitzone-relativen Zeit in der neuen Zeitzone zu halten.</span><span class="sxs-lookup"><span data-stu-id="0dd92-129">This example only updates the [StartTimeZone](https://msdn.microsoft.com/library/d38c4dc1-4ecb-42a1-8d57-a451b16a2de2%28Office.15%29.aspx) and [EndTimeZone](https://msdn.microsoft.com/library/6c53c337-be60-4d22-9e9e-a0c140c5e913%28Office.15%29.aspx) elements, so the server will shift the start and end times of the appointment to keep it at the same time-zone-relative time in the new time zone.</span></span> <span data-ttu-id="0dd92-130">Der Wert des **ItemID** -Elements wird zur Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="0dd92-130">The value of the **ItemId** element is shortened for readability.</span></span> 
  
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

<span data-ttu-id="0dd92-131">Im folgenden Beispiel wird die Zeitzone des Termins aktualisiert und auch die Start-und Endzeit durch explizites Festlegen der **Start** -und **End** -Elemente aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="0dd92-131">The following example request updates the time zone of the appointment, and also updates the start and end times by explicitly setting the **Start** and **End** elements.</span></span> <span data-ttu-id="0dd92-132">Der Wert des **ItemID** -Elements wird zur Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="0dd92-132">The value of the **ItemId** element is shortened for readability.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="0dd92-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0dd92-133">See also</span></span>

- [<span data-ttu-id="0dd92-134">Zeitzonen und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="0dd92-134">Time zones and EWS in Exchange</span></span>](time-zones-and-ews-in-exchange.md)   
- [<span data-ttu-id="0dd92-135">Erstellen von Terminen in einer bestimmten Zeitzone mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="0dd92-135">Create appointments in a specific time zone by using EWS in Exchange</span></span>](how-to-create-appointments-in-a-specific-time-zone-by-using-ews-in-exchange.md)   
- [<span data-ttu-id="0dd92-136">Aktualisieren von Terminen und Besprechungen mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="0dd92-136">Update appointments and meetings by using EWS in Exchange</span></span>](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)
    

