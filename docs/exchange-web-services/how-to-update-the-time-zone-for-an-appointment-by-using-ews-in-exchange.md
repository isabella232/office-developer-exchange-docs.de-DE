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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757010"
---
# <a name="update-the-time-zone-for-an-appointment-by-using-ews-in-exchange"></a>Aktualisieren Sie die Zeitzone für einen Termin im Exchange mithilfe der Exchange-Webdienste

Hier erfahren Sie, wie die Zeitzone für einen Termin oder eine Besprechung zu aktualisieren, und verwenden die EWS Managed API oder EWS in Exchange.
  
Beim Erstellen eines Termins oder einer Besprechung auf einem Exchange-Kalender wird die Zeitzone verwendet, um die Anfangs- und Endzeiten angeben als Zeitzone für den Termin Erstellung gespeichert. Sie können diese Zeitzone mithilfe der EWS Managed API oder EWS ändern. Ändern der Zeitzone für einen Termin hat jedoch anderer Effekte auf dem Zeitpunkt der Start- und Endzeit des Termins.
  
Zeitwerte werden auf dem Exchange-Server als koordinieren Weltzeit (UTC) gespeichert. In diesem Fall 1:00 Uhr (13:00) Eastern Standard Time-Zone starten ein Termins festgelegt ist (UTC-05:00), dass der Wert als 6:00 Uhr (18:00) gespeichert wird, auf dem Server, vorausgesetzt, dass die Zeitzone in der Phase der Standardzeit ist. Wenn eines Termins in anderen Zeitzonen angezeigt wird, wird die entsprechende Anzahl von Stunden hinzugefügt oder entfernt der UTC-Wert, der die Zeitzone-spezifischen Zeit zu bestimmen. Angenommen, ein Termin eine Startzeit 1:00 Uhr weist Eastern (18:00 Uhr UTC), und von einem Client in der Pacific Standard Time-Zone angezeigt wird (UTC-08:00), das Zeitzone spezifische Startzeit für der Client 10:00 Uhr (18:00-08:00) wäre.
  
Wenn Sie die Zeitzone des Termins aktualisieren, ohne die Start- und Endzeit Zeit aktualisieren, aktualisiert der Server die UTC-Werte gespeichert werden, auf dem Server, um die Start- und Endzeit Zeit als die gleichen Zeitzone-spezifischen Zeiten beizubehalten. Angenommen Sie, den 1:00 Uhr Eastern Termin. Die Zeit wird als 18:00 Uhr UTC auf dem Server gespeichert. Wenn die Zeitzone des Termins in der Pacific Standard Time-Zone geändert wird, verschiebt der Server die Startzeit für 1:00 Uhr Pacific (21:00 Uhr UTC).
  
Sie können dieses Verhalten ändern, indem Sie explizit festlegen der Start- und Endzeiten.
  
## <a name="updating-the-time-zone-on-an-existing-appointment-by-using-the-ews-managed-api"></a>Aktualisieren die Zeitzone auf einen vorhandenen Termin mithilfe der EWS Managed API

Im folgenden Beispiel wird die EWS Managed API verwendet, so aktualisieren Sie die Zeitzone auf einen vorhandenen Termin in der zentralen Zeitzone durch Aktualisieren der **Appointment.StartTimeZone** und **Appointment.EndTimeZone** -Eigenschaften. Wenn der Parameter _ShiftAppointnment_ auf **true**festgelegt ist, festgelegt der Code nicht explizit die Anfangs- und Endzeiten für den Termin. In diesem Fall werden der Server die Anfangs- und Endzeiten zum aufbewahren zur gleichen Zeit relativ zur Zeitzone in die neue Zeitzone verschoben. Wenn Festlegung auf **"false"**, mit dem Code die Anfangs- und Endzeiten explizit um behalten den Termin zur selben Zeit in UTC konvertiert. 

In diesem Beispiel wird davon ausgegangen, dass das **ExchangeService**-Objekt mit gültigen Werten in den [Credentials](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx)- und [Url](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx)-Eigenschaften initialisiert wurde. 
  
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

Wenn im Beispiel verwendet wird, um einen Termin zu aktualisieren, die 1:00 Uhr beginnt Eastern und 2:00 Uhr endet Eastern, mit dem Parameter _ShiftAppointment_ auf True festgelegt, und die [ExchangeService.TimeZone](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.timezone%28v=exchg.80%29.aspx) -Eigenschaft legen Sie auf der Eastern Time-Zone, die Ausgabe sieht wie folgt. 
  
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

Wenn im Beispiel verwendet wird, derselben Terminserie mit dem _ShiftAppointment_ -Parameter auf False festgelegt und mit der **TimeZone** -Eigenschaft legen Sie erneut auf die Eastern Standard Time-Zone aktualisieren, sieht die Ausgabe ein wenig anders aus. 
  
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

Beachten Sie, dass die Anfangs- und Endzeiten nicht geändert haben. Dies ist, da die Zeiten in der Eastern Zeit interpretiert werden zone (, da die Eigenschaft **"TimeZone"** Eastern Standard Time-Zone festgelegt ist), und die Zeitwerte wurden aktualisiert, um zu verhindern, dass den Termin verschoben. 
  
## <a name="updating-the-time-zone-on-an-existing-appointment-by-using-ews"></a>Aktualisieren die Zeitzone auf einen vorhandenen Termin mithilfe der Exchange-Webdienste

Das folgende Beispiel EWS- [Vorgang UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) Anforderung aktualisiert die Zeitzone für einen Termin. In diesem Beispiel wird aktualisiert nur die Elemente [StartTimeZone](http://msdn.microsoft.com/library/d38c4dc1-4ecb-42a1-8d57-a451b16a2de2%28Office.15%29.aspx) und [EndTimeZone](http://msdn.microsoft.com/library/6c53c337-be60-4d22-9e9e-a0c140c5e913%28Office.15%29.aspx) , sodass der Server die Anfangs- und Endzeiten des Termins aufrechtzuerhalten gleichzeitig Time-Zone-Relative in die neue Zeitzone verschoben werden. Der Wert des Elements **ItemId** wird zur besseren Lesbarkeit gekürzt. 
  
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

Die folgende Beispiel für eine Anforderung aktualisiert die Zeitzone des Termins, und auch die Anfangs- und Endzeiten aktualisiert, indem die **Start** und **End** Elemente explizit festlegen. Der Wert des Elements **ItemId** wird zur besseren Lesbarkeit gekürzt. 
  
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

## <a name="see-also"></a>Siehe auch

- [Zeitzonen und EWS in Exchange](time-zones-and-ews-in-exchange.md)   
- [Erstellen von Terminen in einer bestimmten Zeitzone mithilfe der EWS in Exchange](how-to-create-appointments-in-a-specific-time-zone-by-using-ews-in-exchange.md)   
- [Aktualisieren von Terminen und Besprechungen mithilfe von EWS in Exchange](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)
    

