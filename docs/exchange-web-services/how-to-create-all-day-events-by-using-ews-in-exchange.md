---
title: Erstellen Sie mithilfe der Exchange-Webdienste im Exchange ganztägige Ereignisse
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 0fcb484b-4ffc-41a5-aeed-8c797766b70c
description: Erfahren Sie, wie ganztägige Ereignisse zu erstellen, indem Sie die EWS Managed API oder EWS in Exchange.
ms.openlocfilehash: 0547fdf0ca92ba0648caeb5de6940d90d2a8ff46
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756873"
---
# <a name="create-all-day-events-by-using-ews-in-exchange"></a><span data-ttu-id="d8b86-103">Erstellen Sie mithilfe der Exchange-Webdienste im Exchange ganztägige Ereignisse</span><span class="sxs-lookup"><span data-stu-id="d8b86-103">Create all-day events by using EWS in Exchange</span></span>

<span data-ttu-id="d8b86-104">Erfahren Sie, wie ganztägige Ereignisse zu erstellen, indem Sie die EWS Managed API oder EWS in Exchange.</span><span class="sxs-lookup"><span data-stu-id="d8b86-104">Learn how to create all-day events by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="d8b86-105">Ganztägige Ereignisse bieten die Möglichkeit, etwas darstellen, die für einen ganzen Tag oder mehrere Tage geschieht – beispielsweise einen Feiertag oder Urlaubstage.</span><span class="sxs-lookup"><span data-stu-id="d8b86-105">All-day events provide a way to represent something that happens for an entire day or multiple days—for example, a holiday, or vacation days.</span></span> <span data-ttu-id="d8b86-106">Ganztägige Ereignisse mit dem EWS Managed API oder EWS erstellen, ist ein Kinderspiel.</span><span class="sxs-lookup"><span data-stu-id="d8b86-106">Creating all-day events with the EWS Managed API or EWS is a snap.</span></span> <span data-ttu-id="d8b86-107">[Erstellen von Terminen](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md), vergleichbar mit ein paar geringfügige Änderungen ist.</span><span class="sxs-lookup"><span data-stu-id="d8b86-107">It's just like [creating appointments](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md), but with a few small changes.</span></span>
  
## <a name="setting-start-and-end-times"></a><span data-ttu-id="d8b86-108">Festlegen der Start- und Endzeiten</span><span class="sxs-lookup"><span data-stu-id="d8b86-108">Setting start and end times</span></span>

<span data-ttu-id="d8b86-109">Per Definition ganztägige Ereignisse Mitternacht für einen bestimmten Tag, und die End 24 Stunden (oder ein Vielfaches von 24 Stunden) weiter unten.</span><span class="sxs-lookup"><span data-stu-id="d8b86-109">By definition, all-day events start at midnight on a specific day, and end 24 hours (or a multiple of 24 hours) later.</span></span> <span data-ttu-id="d8b86-110">Jedoch die EWS Managed API und EWS können Sie angeben, wie oft als Mitternacht beim ganztägige Ereignisse erstellen.</span><span class="sxs-lookup"><span data-stu-id="d8b86-110">However, the EWS Managed API and EWS allow you to specify times other than midnight when creating all day events.</span></span> <span data-ttu-id="d8b86-111">Dies kann zu unbeabsichtigten Verhalten führen, wenn Sie nicht wissen, wie diese Zeiten auf dem Server übersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="d8b86-111">This can lead to unintended behavior if you're not aware of how these times get translated on the server.</span></span>
  
<span data-ttu-id="d8b86-112">Wenn eine Anforderung empfangen wird, erstellen Sie ein neues ganztägiges Ereignis mit Mitternacht (in der [Zeitzone des Anforderung oder Termin](time-zones-and-ews-in-exchange.md)) Anfangs- und/oder Endzeit, erhalten diese Zeiten Mitternacht in der entsprechenden Zeitzone nach den folgenden Regeln angepasst:</span><span class="sxs-lookup"><span data-stu-id="d8b86-112">When a request is received to create a new all-day event with non-midnight (in the [time zone of the request or appointment](time-zones-and-ews-in-exchange.md)) start and/or end times, those times get adjusted to midnight in the appropriate time zone according to the following rules:</span></span>
  
- <span data-ttu-id="d8b86-113">Nicht-Mitternacht Anfangszeiten werden die Mitternacht vor der angegebenen Zeit angepasst.</span><span class="sxs-lookup"><span data-stu-id="d8b86-113">Non-midnight start times are adjusted to the midnight prior to the time specified.</span></span> <span data-ttu-id="d8b86-114">Beispielsweise ruft 1:00 PM 6. Juni auf 00:00 Uhr am 6. Juni korrigiert.</span><span class="sxs-lookup"><span data-stu-id="d8b86-114">For example, 1:00 PM on June 6 gets adjusted to 12:00 AM on June 6.</span></span>
    
- <span data-ttu-id="d8b86-115">Endzeit nicht Mitternacht werden die Mitternacht nach dem angegebenen Zeitpunkt angepasst.</span><span class="sxs-lookup"><span data-stu-id="d8b86-115">Non-midnight end times are adjusted to the midnight after the time specified.</span></span> <span data-ttu-id="d8b86-116">Beispielsweise ruft 1:00 PM 6. Juni auf 00:00:00 Uhr 7. Juni korrigiert.</span><span class="sxs-lookup"><span data-stu-id="d8b86-116">For example, 1:00 PM on June 6 gets adjusted to 12:00 AM on June 7.</span></span>
    
<span data-ttu-id="d8b86-117">Damit das ganztägige Ereignis, das Sie erstellen immer einschließlich Start- und Endzeit Zeitpunkt steht, die Sie angeben, aber möglicherweise zusätzliche Zeit in Anspruch der Benutzer angezeigt werden sollen, die die UMSCHALTTASTE gedrückt, um Mitternacht.</span><span class="sxs-lookup"><span data-stu-id="d8b86-117">So the all-day event that you create is always inclusive of the start and end time that you specify, but might claim additional time on the user's calendar due to the shift to midnight.</span></span> <span data-ttu-id="d8b86-118">Da der Server die Start- und Endzeit Zeit vor Mitternacht angepasst wird, wird empfohlen, dass Sie Ihre Zeit Start- und Endzeit Mitternacht zur Vermeidung von unbeabsichtigten Änderungen an die Zeiten angeben.</span><span class="sxs-lookup"><span data-stu-id="d8b86-118">Because the server will adjust the start and end time to midnight, we recommend that you specify your start and end time at midnight to avoid any unintended changes to the times.</span></span>
  
<span data-ttu-id="d8b86-119">Es ist außerdem unbedingt Zeitzonen berücksichtigt ganztägige Ereignisse erstellen.</span><span class="sxs-lookup"><span data-stu-id="d8b86-119">It's also important to consider time zones when creating all-day events.</span></span> <span data-ttu-id="d8b86-120">Da der Exchange Server ein Mitternacht erzwingt Start- und Endzeit in der Zeitzone des Anforderung oder einem Termin, kann das anzeigen, ganztägigen Ereignis in einem Client konfiguriert für eine andere Zeitzone unerwarteten Ergebnissen führen.</span><span class="sxs-lookup"><span data-stu-id="d8b86-120">Because the Exchange server enforces a midnight start and end time in the time zone of the request or appointment, viewing that all-day event in a client configured for a different time zone can yield unexpected results.</span></span> <span data-ttu-id="d8b86-121">Je nach den Client kann es so aussehen als ganztägiges Ereignis mit zusätzlichen Tage, die Sie wollten nicht einschließen, oder nicht angezeigt werden als ein ganztägiges Ereignis vollständig.</span><span class="sxs-lookup"><span data-stu-id="d8b86-121">Depending on the client, it might appear as an all-day event with extra days that you did not intend to include, or it might not appear as an all-day event altogether.</span></span> <span data-ttu-id="d8b86-122">Aus diesem Grund wird empfohlen, dass Sie bei der Erstellung von ganztägige Ereignisse des Benutzers bevorzugte Zeitzone nach Möglichkeit verwenden.</span><span class="sxs-lookup"><span data-stu-id="d8b86-122">Because of this, we recommend that you use the user's preferred time zone whenever possible when you create all-day events.</span></span>
  
## <a name="create-an-all-day-event-by-using-the-ews-managed-api"></a><span data-ttu-id="d8b86-123">Erstellen Sie ein ganztägiges Ereignis mithilfe der EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="d8b86-123">Create an all-day event by using the EWS Managed API</span></span>

<span data-ttu-id="d8b86-124">Im folgenden Beispiel wird veranschaulicht, wie die EWS Managed API verwenden, erstellen Sie ein ganztägiges Ereignis, ab dem Datum angegeben wird, indem der Parameter _StartDate_ und, jedoch nur für die Anzahl der Tage, die durch den Parameter _NumDays_ angegeben.</span><span class="sxs-lookup"><span data-stu-id="d8b86-124">The following example shows how to use the EWS Managed API to create an all-day event, starting on the date specified by the  _startDate_ parameter and lasting for the number of days specified by the  _numDays_ parameter.</span></span> <span data-ttu-id="d8b86-125">Beachten Sie, dass der Termin in die Zeitzone, die durch die [ExchangeService.TimeZone](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice.timezone%28v=exchg.80%29.aspx) -Eigenschaft angegebenen erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="d8b86-125">Note that the appointment will be created in the time zone specified by the [ExchangeService.TimeZone](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice.timezone%28v=exchg.80%29.aspx) property.</span></span> <span data-ttu-id="d8b86-126">In diesem Beispiel wird davon ausgegangen, dass das im _Dienst_ -Parameter übergebene [ExchangeService](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objekt durch gültige Werte für die [Anmeldeinformationen](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) und [Url](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) -Eigenschaften initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="d8b86-126">This example assumes that the [ExchangeService](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object passed in the  _service_ parameter has been initialized with valid values for the [Credentials](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) and [Url](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) properties.</span></span> 
  
```cs
static void CreateAllDayAppointment(ExchangeService service, DateTime startDate, int numDays)
{
    // Best practice is to set the start date to midnight
    // on the first day of the all-day event.
    DateTime startDateMidnight = startDate.Date;
    // The end date should be midnight on the first day
    // after the event.
    DateTime endDateMidnight = startDateMidnight.AddDays(numDays);
    Appointment allDayEvent = new Appointment(service);
    // Set IsAllDayEvent to true.
    allDayEvent.IsAllDayEvent = true;
    // Set other properties.
    allDayEvent.Subject = "Vacation";
    allDayEvent.LegacyFreeBusyStatus = LegacyFreeBusyStatus.OOF;
    allDayEvent.Start = startDateMidnight;
    allDayEvent.End = endDateMidnight;
    // Save the appointment.
    try
    {
        allDayEvent.Save(WellKnownFolderName.Calendar, SendInvitationsMode.SendToNone);
        Console.WriteLine("All day event created.");
    }
    catch (Exception ex)
    {
        Console.WriteLine("Error saving all day event: {0}", ex.Message);
    }
}
```

## <a name="create-an-all-day-event-by-using-ews"></a><span data-ttu-id="d8b86-127">Erstellen Sie ein ganztägiges Ereignis mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="d8b86-127">Create an all-day event by using EWS</span></span>

<span data-ttu-id="d8b86-128">Das folgende Beispiel zeigt eine Anforderung EWS [CreateItem Operation](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) ein ganztägiges Ereignis erstellen.</span><span class="sxs-lookup"><span data-stu-id="d8b86-128">The following example shows an EWS [CreateItem operation](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) request to create an all-day event.</span></span> <span data-ttu-id="d8b86-129">Der Termin wird in der Eastern Time-Zone erstellt, wie das [TimeZoneContext](http://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) -Element angegeben.</span><span class="sxs-lookup"><span data-stu-id="d8b86-129">The appointment is created in the Eastern time zone, as indicated by the [TimeZoneContext](http://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) element.</span></span> <span data-ttu-id="d8b86-130">Beachten Sie, dass der Zeitteil der Werte der Elemente [Start](http://msdn.microsoft.com/library/7cfe9979-c893-4f9b-b3a1-8f9e17515a4b%28Office.15%29.aspx) und [End](http://msdn.microsoft.com/library/72329821-32ff-495d-b6e5-fdc011003c2e%28Office.15%29.aspx) sind beide 04:00Z, die in der Eastern Time-Zone während der Sommerzeit Mitternacht konvertiert.</span><span class="sxs-lookup"><span data-stu-id="d8b86-130">Notice that the time portion of the values of the [Start](http://msdn.microsoft.com/library/7cfe9979-c893-4f9b-b3a1-8f9e17515a4b%28Office.15%29.aspx) and [End](http://msdn.microsoft.com/library/72329821-32ff-495d-b6e5-fdc011003c2e%28Office.15%29.aspx) elements are both 04:00Z, which converts to midnight in the Eastern time zone during daylight saving time.</span></span> 
  
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
    <m:CreateItem SendMeetingInvitations="SendToNone">
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="calendar" />
      </m:SavedItemFolderId>
      <m:Items>
        <t:CalendarItem>
          <t:Subject>Vacation</t:Subject>
          <t:Start>2014-06-09T04:00:00.000Z</t:Start>
          <t:End>2014-06-10T04:00:00.000Z</t:End>
          <t:IsAllDayEvent>true</t:IsAllDayEvent>
          <t:LegacyFreeBusyStatus>OOF</t:LegacyFreeBusyStatus>
        </t:CalendarItem>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="d8b86-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d8b86-131">See also</span></span>


- [<span data-ttu-id="d8b86-132">Kalender und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="d8b86-132">Calendars and EWS in Exchange</span></span>](calendars-and-ews-in-exchange.md)
    
- [<span data-ttu-id="d8b86-133">Erstellen von Terminen und Besprechungen mithilfe von EWS in Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="d8b86-133">Create appointments and meetings by using EWS in Exchange 2013</span></span>](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [<span data-ttu-id="d8b86-134">Zeitzonen und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="d8b86-134">Time zones and EWS in Exchange</span></span>](time-zones-and-ews-in-exchange.md)
    

