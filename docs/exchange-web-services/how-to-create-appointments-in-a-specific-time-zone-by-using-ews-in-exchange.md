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
# <a name="create-appointments-in-a-specific-time-zone-by-using-ews-in-exchange"></a><span data-ttu-id="81fd7-103">Erstellen von Terminen in einer bestimmten Zeitzone mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="81fd7-103">Create appointments in a specific time zone by using EWS in Exchange</span></span>

<span data-ttu-id="81fd7-104">Informationen zum Erstellen von Terminen in bestimmten Zeitzonen mithilfe der verwaltete EWS-API oder EWS in Exchange.</span><span class="sxs-lookup"><span data-stu-id="81fd7-104">Learn how to create appointments in specific time zones by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="81fd7-105">Wenn ein Termin oder eine Besprechung in einem Exchange-Kalender erstellt wird, wird die Zeitzone, die zum Angeben der Start-und Endzeit verwendet wird, als Erstellungs Zeitzone für den Termin gespeichert.</span><span class="sxs-lookup"><span data-stu-id="81fd7-105">When an appointment or meeting is created on an Exchange calendar, the time zone used to specify the start and end times is saved as the creation time zone for the appointment.</span></span> <span data-ttu-id="81fd7-106">Diese Zeitzone wird auch verwendet, um [Datums-und Uhrzeitwerte zu interpretieren, für die keine explizite Zeitzone angegeben](time-zones-and-ews-in-exchange.md)ist, daher ist es wichtig, die Optionen zum Angeben der Zeitzone zu verstehen.</span><span class="sxs-lookup"><span data-stu-id="81fd7-106">That time zone is also used to [interpret date and time values that do not have an explicit time zone specified](time-zones-and-ews-in-exchange.md), so it is important to understand your options to specify the time zone.</span></span>
  
## <a name="creating-appointments-in-different-time-zones-by-using-the-ews-managed-api"></a><span data-ttu-id="81fd7-107">Erstellen von Terminen in unterschiedlichen Zeitzonen mithilfe der verwaltete EWS-API</span><span class="sxs-lookup"><span data-stu-id="81fd7-107">Creating appointments in different time zones by using the EWS Managed API</span></span>

<span data-ttu-id="81fd7-108">Beim Erstellen von Terminen oder Besprechungen mit dem verwaltete EWS-API haben Sie drei Optionen zum Angeben der Zeitzone:</span><span class="sxs-lookup"><span data-stu-id="81fd7-108">When creating appointments or meetings using the EWS Managed API, you have three options for specifying the time zone:</span></span>
  
- <span data-ttu-id="81fd7-109">Wenn Sie die Zeitzone des Computers verwenden möchten, auf dem ihr verwaltete EWS-API ausgeführt wird, geben Sie beim Erstellen des [Datei "ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objekts keine Zeitzone an.</span><span class="sxs-lookup"><span data-stu-id="81fd7-109">To use the time zone of the computer where your EWS Managed API is executing, do not specify a time zone when creating the [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object.</span></span> 
    
- <span data-ttu-id="81fd7-110">Wenn Sie eine bestimmte Zeitzone für alle Date/Time-Eigenschaften, einschließlich der Eigenschaften beim Erstellen eines neuen Termins oder einer Besprechung, verwenden möchten, geben Sie im Konstruktor für das **Datei "ExchangeService** -Objekt eine Zeitzone an.</span><span class="sxs-lookup"><span data-stu-id="81fd7-110">To use a specific time zone for all date/time properties, including properties when creating a new appointment or meeting, specify a time zone in the constructor for the **ExchangeService** object.</span></span> 
    
- <span data-ttu-id="81fd7-111">Um eine andere Zeitzone als die in der [Datei "ExchangeService. TimeZone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.timezone%28v=exchg.80%29.aspx) -Eigenschaft angegebene Zeitzone zu verwenden, verwenden Sie die Eigenschaften [Termin. StartTimeZone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.starttimezone%28v=exchg.80%29.aspx) und [Termin. EndTimeZone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.endtimezone%28v=exchg.80%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="81fd7-111">To use a different time zone than the one specified in the [ExchangeService.TimeZone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.timezone%28v=exchg.80%29.aspx) property, use the [Appointment.StartTimeZone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.starttimezone%28v=exchg.80%29.aspx) and [Appointment.EndTimeZone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.endtimezone%28v=exchg.80%29.aspx) properties.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="81fd7-112">Die **EndTimeZone** -Eigenschaft ist nur verfügbar, wenn die [Datei "ExchangeService. RequestedServerVersion](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.requestedserverversion%28v=exchg.80%29.aspx) -Eigenschaft auf **Exchange2010** oder höher festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="81fd7-112">The **EndTimeZone** property is only available when the [ExchangeService.RequestedServerVersion](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.requestedserverversion%28v=exchg.80%29.aspx) property is set to **Exchange2010** or later.</span></span> <span data-ttu-id="81fd7-113">Wenn er nicht verfügbar ist, gilt das Festlegen der **StartTimeZone** für die Start-und Endzeit des Termins.</span><span class="sxs-lookup"><span data-stu-id="81fd7-113">If it is not available, setting the **StartTimeZone** applies to both the start and end times of the appointment.</span></span> 
  
<span data-ttu-id="81fd7-114">Im folgenden Beispiel wird der verwaltete EWS-API verwendet, um drei Termine zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="81fd7-114">In the following example, the EWS Managed API is used to create three appointments.</span></span> <span data-ttu-id="81fd7-115">Jeder Termin wird so festgelegt, dass er bei 1:00 Uhr zwei Tage ab jetzt in einer nicht angegebenen Zeitzone beginnt und eine Stunde später endet.</span><span class="sxs-lookup"><span data-stu-id="81fd7-115">Each appointment is set to start at 1:00 PM two days from now, in an unspecified time zone, and end one hour later.</span></span> <span data-ttu-id="81fd7-116">Der erste Termin wird in der Zeitzone des Clientcomputers mithilfe des Standard verwaltete EWS-API Verhaltens erstellt.</span><span class="sxs-lookup"><span data-stu-id="81fd7-116">The first appointment is created in the client computer's time zone by using default EWS Managed API behavior.</span></span> <span data-ttu-id="81fd7-117">Die zweite wird mithilfe der Eigenschaften **Termin. StartTimeZone** und **Termin. EndTimeZone** in der zentralen Zeitzone erstellt.</span><span class="sxs-lookup"><span data-stu-id="81fd7-117">The second is created in the Central time zone by using the **Appointment.StartTimeZone** and **Appointment.EndTimeZone** properties.</span></span> <span data-ttu-id="81fd7-118">Der dritte wird in der Mountain-Zeitzone mithilfe der **Datei "ExchangeService. TimeZone** -Eigenschaft erstellt.</span><span class="sxs-lookup"><span data-stu-id="81fd7-118">The third is created in the Mountain time zone by using the **ExchangeService.TimeZone** property.</span></span> 
  
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

<span data-ttu-id="81fd7-119">Wenn dieses Beispiel auf einem Clientcomputer ausgeführt wird, der in der Eastern Time-Zone konfiguriert wurde, und die drei von ihm erstellten Termine von einem in der Eastern Time-Zone konfigurierten Client angezeigt werden, werden diese auf 1:00 Uhr, 2:00 Uhr und 3:00 pm angezeigt.</span><span class="sxs-lookup"><span data-stu-id="81fd7-119">When this example is executed on a client computer configured in the Eastern time zone, and the three appointments it creates are viewed from a client configured in the Eastern time zone, they appear at 1:00 PM, 2:00 PM, and 3:00 PM, respectively.</span></span>
  
## <a name="creating-appointments-in-different-time-zones-by-using-ews"></a><span data-ttu-id="81fd7-120">Erstellen von Terminen in unterschiedlichen Zeitzonen mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="81fd7-120">Creating appointments in different time zones by using EWS</span></span>

<span data-ttu-id="81fd7-121">Beim Erstellen von Terminen oder Besprechungen mithilfe von EWS stehen Ihnen drei Optionen zum Angeben der Zeitzone zur Ver:</span><span class="sxs-lookup"><span data-stu-id="81fd7-121">When creating appointments or meetings using EWS, you have three options for specifying the time zone:</span></span>
  
- <span data-ttu-id="81fd7-122">Um koordinierte Weltzeit (Coordinated Universal Time, UTC) zu verwenden, fügen Sie kein [timezonecontext](https://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) -Element, [MeetingTimeZone](https://msdn.microsoft.com/library/413b47d9-8126-462c-9a4f-4e771a5e8889%28Office.15%29.aspx) -Element (nur Exchange 2007) oder [StartTimeZone](https://msdn.microsoft.com/library/d38c4dc1-4ecb-42a1-8d57-a451b16a2de2%28Office.15%29.aspx) -und [EndTimeZone](https://msdn.microsoft.com/library/6c53c337-be60-4d22-9e9e-a0c140c5e913%28Office.15%29.aspx) -Elemente (Exchange 2010 und höher) in die [CreateItem-Vorgangs](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) Anforderung ein.</span><span class="sxs-lookup"><span data-stu-id="81fd7-122">To use Coordinated Universal Time (UTC), do not include a [TimeZoneContext](https://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) element, [MeetingTimeZone](https://msdn.microsoft.com/library/413b47d9-8126-462c-9a4f-4e771a5e8889%28Office.15%29.aspx) element (Exchange 2007 only), or [StartTimeZone](https://msdn.microsoft.com/library/d38c4dc1-4ecb-42a1-8d57-a451b16a2de2%28Office.15%29.aspx) and [EndTimeZone](https://msdn.microsoft.com/library/6c53c337-be60-4d22-9e9e-a0c140c5e913%28Office.15%29.aspx) elements (Exchange 2010 and later) in the [CreateItem operation](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) request.</span></span> 
    
- <span data-ttu-id="81fd7-123">Wenn Sie eine bestimmte Zeitzone für alle Date/Time-Eigenschaften, einschließlich der Eigenschaften beim Erstellen eines neuen Termins oder einer Besprechung, verwenden möchten, geben Sie im [timezonecontext](https://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) -Element in der [CreateItem-Vorgangs](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) Anforderung eine Zeitzone an.</span><span class="sxs-lookup"><span data-stu-id="81fd7-123">To use a specific time zone for all date/time properties, including properties when creating a new appointment or meeting, specify a time zone in the [TimeZoneContext](https://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) element in the [CreateItem operation](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) request.</span></span> 
    
- <span data-ttu-id="81fd7-124">Um eine andere Zeitzone als die im [timezonecontext](https://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) -Element angegebene Zeitzone zu verwenden, schließen Sie ein [timezonecontext](https://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) -Element, ein [MeetingTimeZone](https://msdn.microsoft.com/library/413b47d9-8126-462c-9a4f-4e771a5e8889%28Office.15%29.aspx) -Element (nur Exchange 2007) oder [StartTimeZone](https://msdn.microsoft.com/library/d38c4dc1-4ecb-42a1-8d57-a451b16a2de2%28Office.15%29.aspx) -und [EndTimeZone](https://msdn.microsoft.com/library/6c53c337-be60-4d22-9e9e-a0c140c5e913%28Office.15%29.aspx) -Elemente (Exchange 2010 und höher) in die [CreateItem-Vorgangs](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) Anforderung ein.</span><span class="sxs-lookup"><span data-stu-id="81fd7-124">To use a different time zone than the one specified in the [TimeZoneContext](https://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) element, include a [TimeZoneContext](https://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) element, [MeetingTimeZone](https://msdn.microsoft.com/library/413b47d9-8126-462c-9a4f-4e771a5e8889%28Office.15%29.aspx) element (Exchange 2007 only), or [StartTimeZone](https://msdn.microsoft.com/library/d38c4dc1-4ecb-42a1-8d57-a451b16a2de2%28Office.15%29.aspx) and [EndTimeZone](https://msdn.microsoft.com/library/6c53c337-be60-4d22-9e9e-a0c140c5e913%28Office.15%29.aspx) elements (Exchange 2010 and later) in the [CreateItem operation](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) request.</span></span> 
    
<span data-ttu-id="81fd7-125">Im folgenden Beispiel wird mit der [CreateItem-Vorgangs](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) Anforderung ein Termin mithilfe von UTC erstellt.</span><span class="sxs-lookup"><span data-stu-id="81fd7-125">The following example [CreateItem operation](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) request creates an appointment using UTC.</span></span> <span data-ttu-id="81fd7-126">Beachten Sie, dass das **timezonecontext** -Element, das **StartTimeZone** -Element und das **EndTimeZone** -Element fehlen.</span><span class="sxs-lookup"><span data-stu-id="81fd7-126">Notice that the **TimeZoneContext** element, the **StartTimeZone** element, and the **EndTimeZone** element are absent.</span></span> <span data-ttu-id="81fd7-127">Die Werte **Start** und **End** -Element werden in UTC ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="81fd7-127">The **Start** and **End** element values are expressed in UTC.</span></span> 
  
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

<span data-ttu-id="81fd7-128">Im folgenden Beispiel für die [CreateItem-Vorgangs](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) Anforderung werden die Elemente **StartTimeZone** und **EndTimeZone** verwendet, um die zentrale Zeitzone für den Termin anzugeben.</span><span class="sxs-lookup"><span data-stu-id="81fd7-128">The following example [CreateItem operation](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) request uses the **StartTimeZone** and **EndTimeZone** elements to specify the Central time zone for the appointment.</span></span> <span data-ttu-id="81fd7-129">Beachten Sie, dass das **timezonecontext** -Element nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="81fd7-129">Notice that the **TimeZoneContext** element is absent.</span></span> <span data-ttu-id="81fd7-130">Wenn er jedoch vorhanden war, überschreiben die Werte der Elemente **StartTimeZone** und **EndTimeZone** seinen Wert.</span><span class="sxs-lookup"><span data-stu-id="81fd7-130">However, if it were present, the values of the **StartTimeZone** and **EndTimeZone** elements would override its value.</span></span> <span data-ttu-id="81fd7-131">Wieder werden die **Start** - **und** Endelement Werte in UTC ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="81fd7-131">Again, the **Start** and **End** element values are expressed in UTC.</span></span> 
  
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

<span data-ttu-id="81fd7-132">Im folgenden Beispiel für [CreateItem-Vorgangs](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) Anforderung wird das **timezonecontext** -Element auf die Mountain-Zeitzone festgelegt.</span><span class="sxs-lookup"><span data-stu-id="81fd7-132">The following example [CreateItem operation](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) request sets the **TimeZoneContext** element to the Mountain time zone.</span></span> <span data-ttu-id="81fd7-133">Beachten Sie, dass die **StartTimeZone** -und **EndTimeZone** -Elemente nicht vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="81fd7-133">Notice that the **StartTimeZone** and **EndTimeZone** elements are absent.</span></span> <span data-ttu-id="81fd7-134">Wieder werden die **Start** - **und** Endelement Werte in UTC ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="81fd7-134">Again, the **Start** and **End** element values are expressed in UTC.</span></span> 
  
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

<span data-ttu-id="81fd7-135">Wenn die drei von den vorherigen EWS-Beispiel Anforderungen erstellten Termine von einem in der Eastern Time-Zone konfigurierten Client angezeigt werden, werden Sie um 1:00 Uhr, 2:00 Uhr und 3:00 Uhr angezeigt.</span><span class="sxs-lookup"><span data-stu-id="81fd7-135">When the three appointments created by the previous EWS example requests are viewed from a client configured in the Eastern time zone, they appear at 1:00 PM, 2:00 PM, and 3:00 PM, respectively.</span></span>
  
## 

<span data-ttu-id="81fd7-136">Da Sie nun wissen, wie Termine in bestimmten Zeitzonen erstellt werden, sollten Sie [die Zeitzonen für vorhandene Termine](how-to-update-the-time-zone-for-an-appointment-by-using-ews-in-exchange.md) auf eine andere aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="81fd7-136">Now that you know how to create appointments in specific time zones, you might want to [update the time zones on existing appointments](how-to-update-the-time-zone-for-an-appointment-by-using-ews-in-exchange.md) to a different one.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="81fd7-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="81fd7-137">See also</span></span>


- [<span data-ttu-id="81fd7-138">Zeitzonen und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="81fd7-138">Time zones and EWS in Exchange</span></span>](time-zones-and-ews-in-exchange.md)
    
- [<span data-ttu-id="81fd7-139">Aktualisieren der Zeitzone für einen Termin mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="81fd7-139">Update the time zone for an appointment by using EWS in Exchange</span></span>](how-to-update-the-time-zone-for-an-appointment-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="81fd7-140">Erstellen von Terminen und Besprechungen mithilfe von EWS in Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="81fd7-140">Create appointments and meetings by using EWS in Exchange 2013</span></span>](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    

