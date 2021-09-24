---
title: Aktualisieren der Zeitzone für einen Termin mithilfe von EWS in Exchange
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: dc2240c1-5500-4d5c-97d5-09d63ffd30d5
description: Erfahren Sie, wie Sie die Zeitzone für einen vorhandenen Termin oder eine Besprechung mithilfe der verwalteten EWS-API oder EWS in Exchange aktualisieren.
ms.openlocfilehash: 525feb1c7e37914ef4105312e89af8f1a8cf856b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521067"
---
# <a name="update-the-time-zone-for-an-appointment-by-using-ews-in-exchange"></a>Aktualisieren der Zeitzone für einen Termin mithilfe von EWS in Exchange

Erfahren Sie, wie Sie die Zeitzone für einen vorhandenen Termin oder eine Besprechung mithilfe der verwalteten EWS-API oder EWS in Exchange aktualisieren.
  
Wenn ein Termin oder eine Besprechung in einem Exchange Kalender erstellt wird, wird die Zeitzone, die zum Angeben der Anfangs- und Endzeiten verwendet wird, als Erstellungszeitzone für den Termin gespeichert. Sie können diese Zeitzone mithilfe der verwalteten EWS-API oder EWS ändern. Das Ändern der Zeitzone eines Termins hat jedoch andere Auswirkungen auf die Start- und Endzeit des Termins.
  
Zeitwerte werden auf dem Exchange-Server in koordinierter Weltzeit (UTC) gespeichert. Wenn also festgelegt ist, dass ein Termin um 13:00 Uhr (13:00) in der Eastern-Zeitzone (UTC-05:00) beginnt, wird dieser Wert als 18:00 Uhr (18:00) auf dem Server gespeichert, vorausgesetzt, dass sich die Zeitzone in der Standardzeitphase befindet. Wenn dieser Termin in anderen Zeitzonen angezeigt wird, wird die entsprechende Anzahl von Stunden hinzugefügt oder vom UTC-Wert subtrahiert, um die zeitzonenspezifische Uhrzeit zu bestimmen. Wenn ein Termin beispielsweise eine Startzeit um 13:00 Uhr (18:00 Uhr UTC) hat und von einem Client in der Pazifischen Zeitzone (UTC-08:00) angezeigt wird, lautet die zeitzonenspezifische Startzeit für diesen Client 10:00 Uhr (18:00 - 08:00).
  
Wenn Sie die Zeitzone des Termins aktualisieren, ohne die Start- und Endzeit zu aktualisieren, aktualisiert der Server die auf dem Server gespeicherten UTC-Werte, um die Start- und Endzeit als die gleichen zeitzonenspezifischen Uhrzeiten beizubehalten. Nehmen wir beispielsweise den Osttermin um 13:00 Uhr. Die Uhrzeit wird als 18:00 UTC auf dem Server gespeichert. Wenn die Zeitzone des Termins in die Pazifische Zeitzone geändert wird, verschiebt der Server die Startzeit auf 13:00 Uhr Pazifischer Raum (21:00 UTC).
  
Sie können dieses Verhalten ändern, indem Sie die Start- und Endzeiten explizit festlegen.
  
## <a name="updating-the-time-zone-on-an-existing-appointment-by-using-the-ews-managed-api"></a>Aktualisieren der Zeitzone für einen vorhandenen Termin mithilfe der verwalteten EWS-API

Im folgenden Beispiel wird die verwaltete EWS-API verwendet, um die Zeitzone eines vorhandenen Termins auf die zentrale Zeitzone zu aktualisieren, indem die Eigenschaften **Appointment.StartTimeZone** und **Appointment.EndTimeZone** aktualisiert werden. Wenn der  _parameter shiftAppointnment_ auf **"true"** festgelegt ist, legt der Code die Anfangs- und Endzeiten für den Termin nicht explizit fest. In diesem Fall verschiebt der Server die Start- und Endzeiten, um sie in der neuen Zeitzone an den gleichen zeitzonenrelativen Zeiten zu halten. Bei Festlegung auf **"false"** konvertiert der Code die Anfangs- und Endzeiten explizit, um den Termin gleichzeitig in UTC beizubehalten. 

In diesem Beispiel wird davon ausgegangen, dass das **ExchangeService**-Objekt mit gültigen Werten in den [Credentials](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx)- und [Url](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx)-Eigenschaften initialisiert wurde. 
  
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

Wenn das Beispiel verwendet wird, um einen Termin zu aktualisieren, der um 13:00 Uhr Ost beginnt und um 14:00 Uhr Ost endet, wobei der  _parameter shiftAppointment_ auf "true" und die [ExchangeService.TimeZone-Eigenschaft](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.timezone%28v=exchg.80%29.aspx) auf die Eastern-Zeitzone festgelegt ist, sieht die Ausgabe wie folgt aus. 
  
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

Wenn das Beispiel verwendet wird, um den gleichen Termin mit dem  _parameter shiftAppointment_ auf "false" zu aktualisieren, und wenn die **TimeZone-Eigenschaft** erneut auf die Zeitzone "Eastern" festgelegt ist, sieht die Ausgabe etwas anders aus. 
  
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

Beachten Sie, dass sich die Anfangs- und Endzeiten nicht geändert haben. Dies liegt daran, dass die Uhrzeiten in der Eastern-Zeitzone interpretiert werden (da die **TimeZone-Eigenschaft** auf die Eastern-Zeitzone festgelegt ist), und die Zeitwerte aktualisiert wurden, um zu verhindern, dass der Termin verschoben wird. 
  
## <a name="updating-the-time-zone-on-an-existing-appointment-by-using-ews"></a>Aktualisieren der Zeitzone für einen vorhandenen Termin mithilfe von EWS

Im folgenden Beispiel aktualisiert die EWS [UpdateItem-Vorgangsanforderung](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) die Zeitzone eines Termins. This example only updates the [StartTimeZone](https://msdn.microsoft.com/library/d38c4dc1-4ecb-42a1-8d57-a451b16a2de2%28Office.15%29.aspx) and [EndTimeZone](https://msdn.microsoft.com/library/6c53c337-be60-4d22-9e9e-a0c140c5e913%28Office.15%29.aspx) elements, so the server will shift the start and end times of the appointment to keep it at the same time-zone-relative time in the new time zone. Der Wert des **ItemId-Elements** wird zur besseren Lesbarkeit gekürzt. 
  
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

In der folgenden Beispielanforderung wird die Zeitzone des Termins sowie die Start- und Endzeiten aktualisiert, indem die **Elemente "Start"** und **"End"** explizit festgelegt werden. Der Wert des **ItemId-Elements** wird zur besseren Lesbarkeit gekürzt. 
  
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

## <a name="see-also"></a>Siehe auch

- [Zeitzonen und EWS in Exchange](time-zones-and-ews-in-exchange.md)   
- [Erstellen von Terminen in einer bestimmten Zeitzone mithilfe von EWS in Exchange](how-to-create-appointments-in-a-specific-time-zone-by-using-ews-in-exchange.md)   
- [Aktualisieren von Terminen und Besprechungen mithilfe von EWS in Exchange](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)
    

