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
# <a name="update-the-time-zone-for-an-appointment-by-using-ews-in-exchange"></a>Aktualisieren der Zeitzone für einen Termin mithilfe von EWS in Exchange

Erfahren Sie, wie Sie die Zeitzone für einen vorhandenen Termin oder eine Besprechung mithilfe der verwaltete EWS-API oder EWS in Exchange aktualisieren.
  
Wenn ein Termin oder eine Besprechung in einem Exchange-Kalender erstellt wird, wird die Zeitzone, die zum Angeben der Start-und Endzeit verwendet wird, als Erstellungs Zeitzone für den Termin gespeichert. Sie können diese Zeitzone mithilfe der verwaltete EWS-API oder EWS ändern. Das Ändern der Zeitzone eines Termins hat jedoch andere Auswirkungen auf die Anfangs-und Endzeit des Termins.
  
Zeitwerte werden auf dem Exchange-Server in Coordinate Universal Time (UTC) gespeichert. Wenn also ein Termin für den Start um 1:00 Uhr (13:00) in der Eastern Time-Zone (UTC-05:00) festgelegt ist, wird dieser Wert auf dem Server als 6:00 pm (18:00) gespeichert, vorausgesetzt, die Zeitzone befindet sich in der Standardzeit Phase. Wenn dieser Termin in anderen Zeitzonen angezeigt wird, wird die entsprechende Anzahl von Stunden vom UTC-Wert hinzugefügt oder subtrahiert, um die Zeitzonenspezifische Zeit zu bestimmen. Wenn beispielsweise ein Termin um 1:00 Uhr Eastern (6:00 Uhr UTC) beginnt und von einem Client in der Pacific Time Zone (UTC-08:00) angezeigt wird, lautet die Zeitzonenspezifische Startzeit für diesen Client 10:00 am (18:00-08:00).
  
Wenn Sie die Zeitzone des Termins aktualisieren, ohne die Anfangs-und Endzeit zu aktualisieren, aktualisiert der Server die auf dem Server gespeicherten UTC-Werte, um die Start-und Endzeit als Zeitzonenspezifische Zeiten beizubehalten. Nehmen Sie beispielsweise den 1:00 PM Eastern-Termin in Frage. Die Uhrzeit wird auf dem Server als 18:00 UTC gespeichert. Wenn die Zeitzone des Termins in die Zeitzone Pacific Time geändert wird, verschiebt der Server die Startzeit auf 1:00 Uhr Pacific (21:00 UTC).
  
Sie können dieses Verhalten ändern, indem Sie die Anfangs-und Endzeiten explizit festlegen.
  
## <a name="updating-the-time-zone-on-an-existing-appointment-by-using-the-ews-managed-api"></a>Aktualisieren der Zeitzone eines vorhandenen Termins mithilfe der verwaltete EWS-API

Im folgenden Beispiel wird der verwaltete EWS-API verwendet, um die Zeitzone eines vorhandenen Termins in die zentrale Zeitzone zu aktualisieren, indem die Eigenschaften **Termin. StartTimeZone** und **Termin. EndTimeZone** aktualisiert werden. Wenn der Parameter _shiftAppointnment_ auf **true**festgelegt ist, wird der Code nicht explizit die Start-und Endzeit für den Termin festgelegt. In diesem Fall verschiebt der Server die Start-und Endzeiten, um Sie in der neuen Zeitzone gleichzeitig zu den relativen Zeitpunkten zu halten. Bei Festlegung auf " **false**" wandelt der Code die Anfangs-und Endzeiten explizit um, damit der Termin in der UTC gleichzeitig bleibt. 

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

Wenn das Beispiel zum Aktualisieren eines Termins verwendet wird, der um 1:00 Uhr Ost beginnt und um 2:00 Uhr Eastern endet, wobei der _shiftAppointment_ -Parameter auf true festgelegt ist und die [Datei "ExchangeService. TimeZone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.timezone%28v=exchg.80%29.aspx) -Eigenschaft auf die Eastern Time-Zone festgelegt ist, sieht die Ausgabe wie folgt aus. 
  
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

Wenn das Beispiel verwendet wird, um den gleichen Termin mit dem _shiftAppointment_ -Parameter auf "false" zu aktualisieren, und wenn die **TimeZone** -Eigenschaft erneut auf die Eastern Time-Zone festgelegt wurde, sieht die Ausgabe etwas anders aus. 
  
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

Beachten Sie, dass sich die Anfangs-und Endzeiten nicht geändert haben. Dies liegt daran, dass die Zeiten in der östlichen Zeitzone interpretiert werden (da die **TimeZone** -Eigenschaft auf die Eastern Time-Zone festgelegt ist), und die Zeitwerte wurden aktualisiert, um zu verhindern, dass der Termin verschoben wird. 
  
## <a name="updating-the-time-zone-on-an-existing-appointment-by-using-ews"></a>Aktualisieren der Zeitzone eines vorhandenen Termins mithilfe von EWS

Im folgenden Beispiel für die EWS- [UpdateItem-Vorgangs](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) Anforderung wird die Zeitzone eines Termins aktualisiert. In diesem Beispiel werden nur die [StartTimeZone](https://msdn.microsoft.com/library/d38c4dc1-4ecb-42a1-8d57-a451b16a2de2%28Office.15%29.aspx) -und [EndTimeZone](https://msdn.microsoft.com/library/6c53c337-be60-4d22-9e9e-a0c140c5e913%28Office.15%29.aspx) -Elemente aktualisiert, sodass der Server die Start-und Endzeit des Termins verschiebt, um ihn zur gleichen Zeitzone-relativen Zeit in der neuen Zeitzone zu halten. Der Wert des **ItemID** -Elements wird zur Lesbarkeit gekürzt. 
  
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

Im folgenden Beispiel wird die Zeitzone des Termins aktualisiert und auch die Start-und Endzeit durch explizites Festlegen der **Start** -und **End** -Elemente aktualisiert. Der Wert des **ItemID** -Elements wird zur Lesbarkeit gekürzt. 
  
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
    

