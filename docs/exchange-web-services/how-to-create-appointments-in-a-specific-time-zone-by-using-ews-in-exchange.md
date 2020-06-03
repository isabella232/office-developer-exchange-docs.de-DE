---
title: Erstellen von Terminen in einer bestimmten Zeitzone mithilfe von EWS in Exchange
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e68aaa27-250e-4170-b099-077a979c127c
description: Informationen zum Erstellen von Terminen in bestimmten Zeitzonen mithilfe der verwaltete EWS-API oder EWS in Exchange.
ms.openlocfilehash: 9b1160a9d62ab092d1b60265eba1ad953be0032b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456857"
---
# <a name="create-appointments-in-a-specific-time-zone-by-using-ews-in-exchange"></a>Erstellen von Terminen in einer bestimmten Zeitzone mithilfe von EWS in Exchange

Informationen zum Erstellen von Terminen in bestimmten Zeitzonen mithilfe der verwaltete EWS-API oder EWS in Exchange.
  
Wenn ein Termin oder eine Besprechung in einem Exchange-Kalender erstellt wird, wird die Zeitzone, die zum Angeben der Start-und Endzeit verwendet wird, als Erstellungs Zeitzone für den Termin gespeichert. Diese Zeitzone wird auch verwendet, um [Datums-und Uhrzeitwerte zu interpretieren, für die keine explizite Zeitzone angegeben](time-zones-and-ews-in-exchange.md)ist, daher ist es wichtig, die Optionen zum Angeben der Zeitzone zu verstehen.
  
## <a name="creating-appointments-in-different-time-zones-by-using-the-ews-managed-api"></a>Erstellen von Terminen in unterschiedlichen Zeitzonen mithilfe der verwaltete EWS-API

Beim Erstellen von Terminen oder Besprechungen mit dem verwaltete EWS-API haben Sie drei Optionen zum Angeben der Zeitzone:
  
- Wenn Sie die Zeitzone des Computers verwenden möchten, auf dem ihr verwaltete EWS-API ausgeführt wird, geben Sie beim Erstellen des [Datei "ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objekts keine Zeitzone an. 
    
- Wenn Sie eine bestimmte Zeitzone für alle Date/Time-Eigenschaften, einschließlich der Eigenschaften beim Erstellen eines neuen Termins oder einer Besprechung, verwenden möchten, geben Sie im Konstruktor für das **Datei "ExchangeService** -Objekt eine Zeitzone an. 
    
- Um eine andere Zeitzone als die in der [Datei "ExchangeService. TimeZone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.timezone%28v=exchg.80%29.aspx) -Eigenschaft angegebene Zeitzone zu verwenden, verwenden Sie die Eigenschaften [Termin. StartTimeZone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.starttimezone%28v=exchg.80%29.aspx) und [Termin. EndTimeZone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.endtimezone%28v=exchg.80%29.aspx) . 
    
    > [!NOTE]
    > Die **EndTimeZone** -Eigenschaft ist nur verfügbar, wenn die [Datei "ExchangeService. RequestedServerVersion](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.requestedserverversion%28v=exchg.80%29.aspx) -Eigenschaft auf **Exchange2010** oder höher festgelegt ist. Wenn er nicht verfügbar ist, gilt das Festlegen der **StartTimeZone** für die Start-und Endzeit des Termins. 
  
Im folgenden Beispiel wird der verwaltete EWS-API verwendet, um drei Termine zu erstellen. Jeder Termin wird so festgelegt, dass er bei 1:00 Uhr zwei Tage ab jetzt in einer nicht angegebenen Zeitzone beginnt und eine Stunde später endet. Der erste Termin wird in der Zeitzone des Clientcomputers mithilfe des Standard verwaltete EWS-API Verhaltens erstellt. Die zweite wird mithilfe der Eigenschaften **Termin. StartTimeZone** und **Termin. EndTimeZone** in der zentralen Zeitzone erstellt. Der dritte wird in der Mountain-Zeitzone mithilfe der **Datei "ExchangeService. TimeZone** -Eigenschaft erstellt. 
  
```cs
using Microsoft.Exchange.WebServices.Data;
using System.Security;
static void CreateAppointments(string userEmail, SecureString userPass)
{
    // *****************************************************
    // Create an appointment using the client computer's time zone.
    // *****************************************************
    // Do not specify a time zone when creating the ExchangeService.
    ExchangeService clientTZService = new ExchangeService(ExchangeVersion.Exchange2010);
    clientTZService.Credentials = new NetworkCredential(userEmail, userPass);
    clientTZService.AutodiscoverUrl(userEmail, redirectionCallback);
    // Create the appointment.
    Appointment clientTZAppt = new Appointment(clientTZService);
    clientTZAppt.Subject = "Appointment created using client time zone";
    clientTZAppt.Body = new MessageBody(string.Format("Time zone: {0}", clientTZService.TimeZone.DisplayName));
    // Set the start time to 1:00 PM two days from today.
    DateTime startTime = new DateTime(DateTime.Now.Year, DateTime.Now.Month, DateTime.Now.Day + 2);
    startTime = startTime.AddHours(13);
    clientTZAppt.Start = startTime;
    // Set the end time to 2:00 PM on that same day.
    DateTime endTime = startTime.AddHours(1);
    clientTZAppt.End = endTime;
    // Save the appointment to the default calendar.
    try
    {
        // This method results in a call to EWS.
        clientTZAppt.Save(SendInvitationsMode.SendToNone);
    }
    catch (Exception ex)
    {
        Console.WriteLine("Error saving appointment: {0}", ex.Message);
    }
    // *****************************************************
    // Create an appointment in the Central time zone by
    // using the StartTimeZone property.
    // *****************************************************
    // Retrieve the Central time zone.
    TimeZoneInfo centralTZ = TimeZoneInfo.FindSystemTimeZoneById("Central Standard Time");
    // Create the appointment.
    Appointment centralTZAppt = new Appointment(clientTZService);
    centralTZAppt.Subject = "Appointment created using Central time zone";
    centralTZAppt.Body = new MessageBody(string.Format("Time zone: {0}", centralTZ.DisplayName));
    // Set the time zone on the appointment.
    centralTZAppt.StartTimeZone = centralTZ;
    centralTZAppt.EndTimeZone = centralTZ;
    // Set the start time to 1:00 PM two days from today.
    centralTZAppt.Start = startTime;
    // Set the end time to 2:00 PM on that same day.
    centralTZAppt.End = endTime;
    // Save the appointment to the default calendar.
    try
    {
        // This method results in a call to EWS.
        centralTZAppt.Save(SendInvitationsMode.SendToNone);
    }
    catch (Exception ex)
    {
        Console.WriteLine("Error saving appointment: {0}", ex.Message);
    }
    // *****************************************************
    // Create an appointment in the Mountain time zone by
    // using the ExchangeService.TimeZone property.
    // *****************************************************
    // Specify the Mountain time zone when creating the ExchangeService.
    TimeZoneInfo mountainTZ = TimeZoneInfo.FindSystemTimeZoneById("Mountain Standard Time");
    ExchangeService mountainTZService = new ExchangeService(ExchangeVersion.Exchange2010, mountainTZ);
    mountainTZService.Credentials = new NetworkCredential(userEmail, userPass);
    mountainTZService.AutodiscoverUrl(userEmail, redirectionCallback);
    // Create the appointment.
    Appointment mountainTZAppt = new Appointment(mountainTZService);
    mountainTZAppt.Subject = "Appointment created using Mountain time zone";
    mountainTZAppt.Body = new MessageBody(string.Format("Time zone: {0}", mountainTZService.TimeZone.DisplayName));
    // Set the start time to 1:00 PM two days from today.
    mountainTZAppt.Start = startTime;
    // Set the end time to 2:00 PM on that same day.
    mountainTZAppt.End = endTime;
    // Save the appointment to the default calendar.
    try
    {
        // This method results in a call to EWS.
        mountainTZAppt.Save(SendInvitationsMode.SendToNone);
    }
    catch (Exception ex)
    {
        Console.WriteLine("Error saving appointment: {0}", ex.Message);
    }
}
```

Wenn dieses Beispiel auf einem Clientcomputer ausgeführt wird, der in der Eastern Time-Zone konfiguriert wurde, und die drei von ihm erstellten Termine von einem in der Eastern Time-Zone konfigurierten Client angezeigt werden, werden diese auf 1:00 Uhr, 2:00 Uhr und 3:00 pm angezeigt.
  
## <a name="creating-appointments-in-different-time-zones-by-using-ews"></a>Erstellen von Terminen in unterschiedlichen Zeitzonen mithilfe von EWS

Beim Erstellen von Terminen oder Besprechungen mithilfe von EWS stehen Ihnen drei Optionen zum Angeben der Zeitzone zur Ver:
  
- Um koordinierte Weltzeit (Coordinated Universal Time, UTC) zu verwenden, fügen Sie kein [timezonecontext](https://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) -Element, [MeetingTimeZone](https://msdn.microsoft.com/library/413b47d9-8126-462c-9a4f-4e771a5e8889%28Office.15%29.aspx) -Element (nur Exchange 2007) oder [StartTimeZone](https://msdn.microsoft.com/library/d38c4dc1-4ecb-42a1-8d57-a451b16a2de2%28Office.15%29.aspx) -und [EndTimeZone](https://msdn.microsoft.com/library/6c53c337-be60-4d22-9e9e-a0c140c5e913%28Office.15%29.aspx) -Elemente (Exchange 2010 und höher) in die [CreateItem-Vorgangs](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) Anforderung ein. 
    
- Wenn Sie eine bestimmte Zeitzone für alle Date/Time-Eigenschaften, einschließlich der Eigenschaften beim Erstellen eines neuen Termins oder einer Besprechung, verwenden möchten, geben Sie im [timezonecontext](https://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) -Element in der [CreateItem-Vorgangs](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) Anforderung eine Zeitzone an. 
    
- Um eine andere Zeitzone als die im [timezonecontext](https://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) -Element angegebene Zeitzone zu verwenden, schließen Sie ein [timezonecontext](https://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) -Element, ein [MeetingTimeZone](https://msdn.microsoft.com/library/413b47d9-8126-462c-9a4f-4e771a5e8889%28Office.15%29.aspx) -Element (nur Exchange 2007) oder [StartTimeZone](https://msdn.microsoft.com/library/d38c4dc1-4ecb-42a1-8d57-a451b16a2de2%28Office.15%29.aspx) -und [EndTimeZone](https://msdn.microsoft.com/library/6c53c337-be60-4d22-9e9e-a0c140c5e913%28Office.15%29.aspx) -Elemente (Exchange 2010 und höher) in die [CreateItem-Vorgangs](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) Anforderung ein. 
    
Im folgenden Beispiel wird mit der [CreateItem-Vorgangs](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) Anforderung ein Termin mithilfe von UTC erstellt. Beachten Sie, dass das **timezonecontext** -Element, das **StartTimeZone** -Element und das **EndTimeZone** -Element fehlen. Die Werte **Start** und **End** -Element werden in UTC ausgedrückt. 
  
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
    <m:CreateItem SendMeetingInvitations="SendToNone">
      <m:Items>
        <t:CalendarItem>
          <t:Subject>Appointment created using UTC</t:Subject>
          <t:Body BodyType="HTML">Time zone: UTC</t:Body>
          <t:Start>2014-06-07T17:00:00.000Z</t:Start>
          <t:End>2014-06-07T18:00:00.000Z</t:End>
        </t:CalendarItem>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

Im folgenden Beispiel für die [CreateItem-Vorgangs](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) Anforderung werden die Elemente **StartTimeZone** und **EndTimeZone** verwendet, um die zentrale Zeitzone für den Termin anzugeben. Beachten Sie, dass das **timezonecontext** -Element nicht vorhanden ist. Wenn er jedoch vorhanden war, überschreiben die Werte der Elemente **StartTimeZone** und **EndTimeZone** seinen Wert. Wieder werden die **Start** - **und** Endelement Werte in UTC ausgedrückt. 
  
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
    <m:CreateItem SendMeetingInvitations="SendToNone">
      <m:Items>
        <t:CalendarItem>
          <t:Subject>Appointment created using Central time zone</t:Subject>
          <t:Body BodyType="HTML">Time zone: (UTC-06:00) Central Time (US &amp;amp; Canada)</t:Body>
          <t:Start>2014-06-07T18:00:00.000Z</t:Start>
          <t:End>2014-06-07T19:00:00.000Z</t:End>
          <t:StartTimeZone Id="Central Standard Time" />
          <t:EndTimeZone Id="Central Standard Time" />
        </t:CalendarItem>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

Im folgenden Beispiel für [CreateItem-Vorgangs](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) Anforderung wird das **timezonecontext** -Element auf die Mountain-Zeitzone festgelegt. Beachten Sie, dass die **StartTimeZone** -und **EndTimeZone** -Elemente nicht vorhanden sind. Wieder werden die **Start** - **und** Endelement Werte in UTC ausgedrückt. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Mountain Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:CreateItem SendMeetingInvitations="SendToNone">
      <m:Items>
        <t:CalendarItem>
          <t:Subject>Appointment created using Mountain time zone</t:Subject>
          <t:Body BodyType="HTML">Time zone: (UTC-07:00) Mountain Time (US &amp;amp; Canada)</t:Body>
          <t:Start>2014-06-07T19:00:00.000Z</t:Start>
          <t:End>2014-06-07T20:00:00.000Z</t:End>
        </t:CalendarItem>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

Wenn die drei von den vorherigen EWS-Beispiel Anforderungen erstellten Termine von einem in der Eastern Time-Zone konfigurierten Client angezeigt werden, werden Sie um 1:00 Uhr, 2:00 Uhr und 3:00 Uhr angezeigt.
  
## 

Da Sie nun wissen, wie Termine in bestimmten Zeitzonen erstellt werden, sollten Sie [die Zeitzonen für vorhandene Termine](how-to-update-the-time-zone-for-an-appointment-by-using-ews-in-exchange.md) auf eine andere aktualisieren. 
  
## <a name="see-also"></a>Siehe auch


- [Zeitzonen und EWS in Exchange](time-zones-and-ews-in-exchange.md)
    
- [Aktualisieren der Zeitzone für einen Termin mithilfe von EWS in Exchange](how-to-update-the-time-zone-for-an-appointment-by-using-ews-in-exchange.md)
    
- [Erstellen von Terminen und Besprechungen mithilfe von EWS in Exchange 2013](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    

