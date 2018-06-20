---
title: Erstellen von Terminen in einer bestimmten Zeitzone mithilfe der EWS in Exchange
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e68aaa27-250e-4170-b099-077a979c127c
description: Erfahren Sie, wie Termine in bestimmten Zeitzonen zu erstellen, indem Sie die EWS Managed API oder EWS in Exchange.
ms.openlocfilehash: 1725498847f89a417b62a06fb8a3109af5c4deb0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19756883"
---
# <a name="create-appointments-in-a-specific-time-zone-by-using-ews-in-exchange"></a>Erstellen von Terminen in einer bestimmten Zeitzone mithilfe der EWS in Exchange

Erfahren Sie, wie Termine in bestimmten Zeitzonen zu erstellen, indem Sie die EWS Managed API oder EWS in Exchange.
  
Beim Erstellen eines Termins oder einer Besprechung auf einem Exchange-Kalender wird die Zeitzone verwendet, um die Anfangs- und Endzeiten angeben als Zeitzone für den Termin Erstellung gespeichert. Diese Zeitzone wird auch [interpretiert werden Datum und Uhrzeit Werte, die nicht über eine explizite Angabe einer Zeitzone verfügen](time-zones-and-ews-in-exchange.md), verwendet, daher es wichtig ist zu verstehen, die Optionen zum Angeben der Zeitzone.
  
## <a name="creating-appointments-in-different-time-zones-by-using-the-ews-managed-api"></a>Erstellen von Terminen in unterschiedlichen Zeitzonen mithilfe der EWS Managed API

Wenn Termine oder die EWS Managed API Besprechungen erstellen, müssen Sie drei Optionen zur Angabe der Time-Zone:
  
- Verwenden die Zeitzone des Computers, auf dem die EWS Managed API ausgeführt wird, wenn Sie keinen an eine Zeitzone beim Erstellen des [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objekts. 
    
- Um eine bestimmte Zeitzone für alle Datum/Uhrzeit-Eigenschaften zu verwenden, geben einschließlich Eigenschaften beim Erstellen eines neuen Termins oder eine Besprechung, Sie eine Zeitzone in der Konstruktor für das **ExchangeService** -Objekt. 
    
- Um eine andere Zeitzone als der in der [ExchangeService.TimeZone](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.timezone%28v=exchg.80%29.aspx) -Eigenschaft angegebene verwenden möchten, verwenden Sie die Eigenschaften [Appointment.StartTimeZone](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.starttimezone%28v=exchg.80%29.aspx) und [Appointment.EndTimeZone](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.endtimezone%28v=exchg.80%29.aspx) . 
    
    > [!NOTE]
    > **EndTimeZone** -Eigenschaft ist nur verfügbar, wenn die Eigenschaft [ExchangeService.RequestedServerVersion](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.requestedserverversion%28v=exchg.80%29.aspx) auf **Exchange2010** oder höher festgelegt ist. Wenn es nicht verfügbar ist, betrifft festlegen **StartTimeZone** sowohl der Anfangs- und Endzeiten des Termins. 
  
Im folgenden Beispiel wird die EWS Managed API verwendet, um drei Termine zu erstellen. Jeder Termin ist in zwei Tagen, 1:00 Uhr in einem nicht angegebenen Zeitzone und End eine Stunde später starten festgelegt. Der erste Termin wird in der Zeitzone des Clientcomputers mithilfe von Standardverhalten EWS Managed API erstellt. Die zweite wird in der zentralen Zeitzone mithilfe der Eigenschaften **Appointment.StartTimeZone** und **Appointment.EndTimeZone** erstellt. Die dritte wird mithilfe der **ExchangeService.TimeZone** -Eigenschaft in der Mountain Standard Time-Zone erstellt. 
  
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

Wenn auf einem Clientcomputer in der Eastern Time-Zone konfiguriert wird in diesem Beispiel wird ausgeführt, und die drei Termine erstellt werden von einem Client in der Eastern Time-Zone konfiguriert sie 1:00 Uhr, angezeigt werden angezeigt: 00 Uhr und 3:00 Uhr fest.
  
## <a name="creating-appointments-in-different-time-zones-by-using-ews"></a>Erstellen von Terminen in unterschiedlichen Zeitzonen mithilfe der Exchange-Webdienste

Wenn Termine oder Besprechungen mithilfe von EWS erstellen, müssen Sie drei Optionen zur Angabe der Time-Zone:
  
- Keinen Sie koordinierte Weltzeit (UTC) für die Verwendung eines [TimeZoneContext](http://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) -Elements, [MeetingTimeZone](http://msdn.microsoft.com/library/413b47d9-8126-462c-9a4f-4e771a5e8889%28Office.15%29.aspx) -Element (nur Exchange 2007), oder [StartTimeZone](http://msdn.microsoft.com/library/d38c4dc1-4ecb-42a1-8d57-a451b16a2de2%28Office.15%29.aspx) und [EndTimeZone](http://msdn.microsoft.com/library/6c53c337-be60-4d22-9e9e-a0c140c5e913%28Office.15%29.aspx) -Elemente (Exchange 2010 und höher) in der [ CreateItem Operation](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) Anforderung. 
    
- Um eine bestimmte Zeitzone für alle Datum/Uhrzeit-Eigenschaften zu verwenden, geben einschließlich Eigenschaften beim Erstellen eines neuen Termins oder eine Besprechung, Sie eine Zeitzone im [TimeZoneContext](http://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) -Element in der Anforderung [CreateItem Operation](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) . 
    
- Fügen Sie für die Verwendung eine andere Zeitzone als der im [TimeZoneContext](http://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) -Element angegebene [TimeZoneContext](http://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) -Element, [MeetingTimeZone](http://msdn.microsoft.com/library/413b47d9-8126-462c-9a4f-4e771a5e8889%28Office.15%29.aspx) -Element (nur Exchange 2007) oder [StartTimeZone](http://msdn.microsoft.com/library/d38c4dc1-4ecb-42a1-8d57-a451b16a2de2%28Office.15%29.aspx) und [EndTimeZone](http://msdn.microsoft.com/library/6c53c337-be60-4d22-9e9e-a0c140c5e913%28Office.15%29.aspx) Elemente ( Exchange 2010 und höher) in der Anforderung [CreateItem Operation](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) . 
    
Das folgende Beispiel [CreateItem Operation](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) Anforderung wird ein Termin mit UTC erstellt. Beachten Sie, dass das **TimeZoneContext** -Element, das **StartTimeZone** -Element und das **EndTimeZone** -Element nicht vorhanden sind. Die Werte für **Start** und **End** -Element werden in UTC ausgedrückt. 
  
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

Das folgende Beispiel [CreateItem Operation](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) Anforderung mithilfe der **StartTimeZone** und **EndTimeZone** -Elemente an der zentralen Zeitzone für den Termin. Beachten Sie, dass das **TimeZoneContext** -Element nicht vorhanden ist. Falls es vorhanden sind, würde die Werte der Elemente **StartTimeZone** und **EndTimeZone** seinen Wert überschreiben. In diesem Fall werden **Start** und **End** -Elementwerte in UTC ausgedrückt. 
  
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

Das folgende Beispiel [CreateItem Operation](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) Anforderung wird das **TimeZoneContext** -Element der Mountain Standard Time-Zone. Beachten Sie, dass die **StartTimeZone** und **EndTimeZone** -Elemente nicht vorhanden sind. In diesem Fall werden **Start** und **End** -Elementwerte in UTC ausgedrückt. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

Wenn die drei Termine erstellt haben, nach dem vorherigen Beispiel EWS Anforderungen angezeigt werden, von einem Client in der Eastern Time-Zone konfiguriert sie 1:00 Uhr, angezeigt werden: 00 Uhr und 3:00 Uhr fest.
  
## 

Nachdem Sie wissen, wie Termine in bestimmten Zeitzonen erstellen sollten Sie zu einer anderen [Zeitzonen auf vorhandene Termine zu aktualisieren](how-to-update-the-time-zone-for-an-appointment-by-using-ews-in-exchange.md) . 
  
## <a name="see-also"></a>Siehe auch


- [Zeitzonen und EWS in Exchange](time-zones-and-ews-in-exchange.md)
    
- [Aktualisieren Sie die Zeitzone für einen Termin im Exchange mithilfe der Exchange-Webdienste](how-to-update-the-time-zone-for-an-appointment-by-using-ews-in-exchange.md)
    
- [Erstellen von Terminen und Besprechungen mithilfe von EWS in Exchange 2013](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    

