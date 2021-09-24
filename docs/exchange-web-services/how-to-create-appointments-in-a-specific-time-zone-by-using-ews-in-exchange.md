---
title: Erstellen von Terminen in einer bestimmten Zeitzone mithilfe von EWS in Exchange
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: e68aaa27-250e-4170-b099-077a979c127c
description: Erfahren Sie, wie Sie Termine in bestimmten Zeitzonen mithilfe der verwalteten EWS-API oder EWS in Exchange erstellen.
ms.openlocfilehash: 589c72982fdda568170468c376b8a6d9f598aa36
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521144"
---
# <a name="create-appointments-in-a-specific-time-zone-by-using-ews-in-exchange"></a>Erstellen von Terminen in einer bestimmten Zeitzone mithilfe von EWS in Exchange

Erfahren Sie, wie Sie Termine in bestimmten Zeitzonen mithilfe der verwalteten EWS-API oder EWS in Exchange erstellen.
  
Wenn ein Termin oder eine Besprechung in einem Exchange Kalender erstellt wird, wird die Zeitzone, die zum Angeben der Anfangs- und Endzeiten verwendet wird, als Erstellungszeitzone für den Termin gespeichert. Diese Zeitzone wird auch verwendet, um [Datums- und Uhrzeitwerte](time-zones-and-ews-in-exchange.md)zu interpretieren, für die keine explizite Zeitzone angegeben ist. Daher ist es wichtig, die Optionen zum Angeben der Zeitzone zu verstehen.
  
## <a name="creating-appointments-in-different-time-zones-by-using-the-ews-managed-api"></a>Erstellen von Terminen in verschiedenen Zeitzonen mithilfe der verwalteten EWS-API

Beim Erstellen von Terminen oder Besprechungen mithilfe der verwalteten EWS-API stehen Ihnen drei Optionen zum Angeben der Zeitzone zur Verfügung:
  
- Wenn Sie die Zeitzone des Computers verwenden möchten, auf dem Ihre verwaltete EWS-API ausgeführt wird, geben Sie beim Erstellen des [ExchangeService-Objekts](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) keine Zeitzone an. 
    
- Um eine bestimmte Zeitzone für alle Datums-/Uhrzeiteigenschaften zu verwenden, einschließlich eigenschaften beim Erstellen eines neuen Termins oder einer Besprechung, geben Sie eine Zeitzone im Konstruktor für das **ExchangeService** -Objekt an. 
    
- Um eine andere Zeitzone als die in der [ExchangeService.TimeZone-Eigenschaft](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.timezone%28v=exchg.80%29.aspx) angegebene zu verwenden, verwenden Sie die Eigenschaften [Appointment.StartTimeZone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.starttimezone%28v=exchg.80%29.aspx) und [Appointment.EndTimeZone.](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.endtimezone%28v=exchg.80%29.aspx) 
    
    > [!NOTE]
    > Die **EndTimeZone-Eigenschaft** ist nur verfügbar, wenn die [ExchangeService.RequestedServerVersion-Eigenschaft](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.requestedserverversion%28v=exchg.80%29.aspx) auf **Exchange2010** oder höher festgelegt ist. Wenn es nicht verfügbar ist, gilt das Festlegen von **StartTimeZone** sowohl für die Start- als auch die Endzeit des Termins. 
  
Im folgenden Beispiel wird die verwaltete EWS-API verwendet, um drei Termine zu erstellen. Jeder Termin beginnt in zwei Tagen um 13:00 Uhr in einer nicht angegebenen Zeitzone und endet eine Stunde später. Der erste Termin wird in der Zeitzone des Clientcomputers mithilfe des standardmäßigen EWS Managed API-Verhaltens erstellt. Die zweite wird in der zentralen Zeitzone mithilfe der Eigenschaften **Appointment.StartTimeZone** und **Appointment.EndTimeZone** erstellt. Die dritte wird in der Zeitzone "Mountain" mithilfe der **ExchangeService.TimeZone-Eigenschaft** erstellt. 
  
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

Wenn dieses Beispiel auf einem Clientcomputer ausgeführt wird, der in der Eastern-Zeitzone konfiguriert ist, und die drei erstellten Termine von einem Client angezeigt werden, der in der Eastern-Zeitzone konfiguriert ist, werden sie jeweils um 13:00 Uhr, 14:00 Uhr und 15:00 Uhr angezeigt.
  
## <a name="creating-appointments-in-different-time-zones-by-using-ews"></a>Erstellen von Terminen in verschiedenen Zeitzonen mithilfe von EWS

Beim Erstellen von Terminen oder Besprechungen mithilfe von EWS stehen Ihnen drei Optionen zum Angeben der Zeitzone zur Verfügung:
  
- Um koordinierte Weltzeit (COORDINATED Universal Time, UTC) zu verwenden, schließen Sie kein [TimeZoneContext-Element,](https://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) [meetingTimeZone-Element](https://msdn.microsoft.com/library/413b47d9-8126-462c-9a4f-4e771a5e8889%28Office.15%29.aspx) (nur Exchange 2007) oder [StartTimeZone-](https://msdn.microsoft.com/library/d38c4dc1-4ecb-42a1-8d57-a451b16a2de2%28Office.15%29.aspx) und [EndTimeZone-Elemente](https://msdn.microsoft.com/library/6c53c337-be60-4d22-9e9e-a0c140c5e913%28Office.15%29.aspx) (Exchange 2010 und höher) in die [CreateItem-Vorgangsanforderung](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) ein. 
    
- Um eine bestimmte Zeitzone für alle Datums-/Uhrzeiteigenschaften zu verwenden, einschließlich der Eigenschaften beim Erstellen eines neuen Termins oder einer Besprechung, geben Sie eine Zeitzone im [TimeZoneContext-Element](https://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) in der [CreateItem-Vorgangsanforderung](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) an. 
    
- Um eine andere Zeitzone als die im [TimeZoneContext-Element](https://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) angegebene zu verwenden, schließen Sie ein [TimeZoneContext-Element,](https://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) [ein MeetingTimeZone-Element](https://msdn.microsoft.com/library/413b47d9-8126-462c-9a4f-4e771a5e8889%28Office.15%29.aspx) (nur Exchange 2007) oder [StartTimeZone-](https://msdn.microsoft.com/library/d38c4dc1-4ecb-42a1-8d57-a451b16a2de2%28Office.15%29.aspx) und [EndTimeZone-Elemente](https://msdn.microsoft.com/library/6c53c337-be60-4d22-9e9e-a0c140c5e913%28Office.15%29.aspx) (Exchange 2010 und höher) in die [CreateItem-Vorgangsanforderung](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) ein. 
    
Im folgenden Beispiel erstellt [die CreateItem-Vorgangsanforderung](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) einen Termin mit UTC. Beachten Sie, dass das **TimeZoneContext-Element,** das **StartTimeZone-Element** und das **EndTimeZone-Element** nicht vorhanden sind. Die **Start-** und **End-Elementwerte** werden in UTC ausgedrückt. 
  
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

The following example [CreateItem operation](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) request uses the **StartTimeZone** and **EndTimeZone** elements to specify the Central time zone for the appointment. Beachten Sie, dass das **TimeZoneContext-Element** nicht vorhanden ist. Wenn sie jedoch vorhanden wäre, würden die Werte der **Elemente StartTimeZone** und **EndTimeZone** ihren Wert überschreiben. Auch hier werden die **Start-** und **End-Elementwerte** in UTC ausgedrückt. 
  
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

The following example [CreateItem operation](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) request sets the **TimeZoneContext** element to the Mountain time zone. Beachten Sie, dass die **Elemente StartTimeZone** und **EndTimeZone** nicht vorhanden sind. Auch hier werden die **Start-** und **End-Elementwerte** in UTC ausgedrückt. 
  
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

Wenn die drei von den vorherigen EWS-Beispielanforderungen erstellten Termine von einem Client angezeigt werden, der in der Eastern-Zeitzone konfiguriert ist, werden sie jeweils um 13:00 Uhr, 14:00 Uhr und 15:00 Uhr angezeigt.
  
## 

Da Sie nun wissen, wie Termine in bestimmten Zeitzonen erstellt werden, sollten Sie [die Zeitzonen für vorhandene Termine](how-to-update-the-time-zone-for-an-appointment-by-using-ews-in-exchange.md) auf eine andere aktualisieren. 
  
## <a name="see-also"></a>Siehe auch


- [Zeitzonen und EWS in Exchange](time-zones-and-ews-in-exchange.md)
    
- [Aktualisieren der Zeitzone für einen Termin mithilfe von EWS in Exchange](how-to-update-the-time-zone-for-an-appointment-by-using-ews-in-exchange.md)
    
- [Erstellen von Terminen und Besprechungen mithilfe von EWS in Exchange 2013](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    

