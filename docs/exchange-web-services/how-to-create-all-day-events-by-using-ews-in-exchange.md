---
title: Erstellen von ganztägigen Ereignissen mithilfe von EWS in Exchange
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 0fcb484b-4ffc-41a5-aeed-8c797766b70c
description: Informationen zum Erstellen von ganztägigen Ereignissen mithilfe der verwaltete EWS-API oder EWS in Exchange.
ms.openlocfilehash: 6be638c17cc0e0c86fa6b4217169aa7259dfd4aa
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456864"
---
# <a name="create-all-day-events-by-using-ews-in-exchange"></a><span data-ttu-id="6f1aa-103">Erstellen von ganztägigen Ereignissen mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="6f1aa-103">Create all-day events by using EWS in Exchange</span></span>

<span data-ttu-id="6f1aa-104">Informationen zum Erstellen von ganztägigen Ereignissen mithilfe der verwaltete EWS-API oder EWS in Exchange.</span><span class="sxs-lookup"><span data-stu-id="6f1aa-104">Learn how to create all-day events by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="6f1aa-105">Ganztägige Ereignisse bieten eine Möglichkeit, etwas darzustellen, das für einen ganzen Tag oder mehrere Tage stattfindet (beispielsweise einen Feiertag oder Urlaubstage).</span><span class="sxs-lookup"><span data-stu-id="6f1aa-105">All-day events provide a way to represent something that happens for an entire day or multiple days—for example, a holiday, or vacation days.</span></span> <span data-ttu-id="6f1aa-106">Das Erstellen von ganztägigen Ereignissen mit dem verwaltete EWS-API oder EWS ist ein Kinderspiel.</span><span class="sxs-lookup"><span data-stu-id="6f1aa-106">Creating all-day events with the EWS Managed API or EWS is a snap.</span></span> <span data-ttu-id="6f1aa-107">Es ist genau wie das [Erstellen von Terminen](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md), aber mit ein paar kleinen Änderungen.</span><span class="sxs-lookup"><span data-stu-id="6f1aa-107">It's just like [creating appointments](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md), but with a few small changes.</span></span>
  
## <a name="setting-start-and-end-times"></a><span data-ttu-id="6f1aa-108">Festlegen der Anfangs-und Endzeiten</span><span class="sxs-lookup"><span data-stu-id="6f1aa-108">Setting start and end times</span></span>

<span data-ttu-id="6f1aa-109">Per Definition beginnen ganztägige Ereignisse an einem bestimmten Tag um Mitternacht und enden später 24 Stunden (oder ein Vielfaches von 24 Stunden).</span><span class="sxs-lookup"><span data-stu-id="6f1aa-109">By definition, all-day events start at midnight on a specific day, and end 24 hours (or a multiple of 24 hours) later.</span></span> <span data-ttu-id="6f1aa-110">Mit dem verwaltete EWS-API und EWS können Sie jedoch beim Erstellen aller Day-Ereignisse andere Zeiten als Mitternacht angeben.</span><span class="sxs-lookup"><span data-stu-id="6f1aa-110">However, the EWS Managed API and EWS allow you to specify times other than midnight when creating all day events.</span></span> <span data-ttu-id="6f1aa-111">Dies kann zu unerwünschtem Verhalten führen, wenn Sie nicht wissen, wie diese Zeiten auf dem Server übersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="6f1aa-111">This can lead to unintended behavior if you're not aware of how these times get translated on the server.</span></span>
  
<span data-ttu-id="6f1aa-112">Wenn eine Anforderung empfangen wird, um ein Neues ganztägiges Ereignis zu erstellen, das nicht Mitternacht (in der Zeitzone der [Anforderung oder des Termins](time-zones-and-ews-in-exchange.md)) beginnt und/oder endet, werden diese Zeiten entsprechend den folgenden Regeln auf Mitternacht in der entsprechenden Zeitzone angepasst:</span><span class="sxs-lookup"><span data-stu-id="6f1aa-112">When a request is received to create a new all-day event with non-midnight (in the [time zone of the request or appointment](time-zones-and-ews-in-exchange.md)) start and/or end times, those times get adjusted to midnight in the appropriate time zone according to the following rules:</span></span>
  
- <span data-ttu-id="6f1aa-113">Startzeiten außerhalb der Mitternachtszeit werden vor der angegebenen Uhrzeit auf Mitternacht angepasst.</span><span class="sxs-lookup"><span data-stu-id="6f1aa-113">Non-midnight start times are adjusted to the midnight prior to the time specified.</span></span> <span data-ttu-id="6f1aa-114">Beispielsweise wird 1:00 Uhr am 6. Juni auf 12:00 Uhr am 6. Juni angepasst.</span><span class="sxs-lookup"><span data-stu-id="6f1aa-114">For example, 1:00 PM on June 6 gets adjusted to 12:00 AM on June 6.</span></span>
    
- <span data-ttu-id="6f1aa-115">Endzeiten von nicht-Mitternacht werden nach der angegebenen Uhrzeit auf Mitternacht angepasst.</span><span class="sxs-lookup"><span data-stu-id="6f1aa-115">Non-midnight end times are adjusted to the midnight after the time specified.</span></span> <span data-ttu-id="6f1aa-116">Beispielsweise wird 1:00 Uhr am 6. Juni auf 12:00 Uhr am 7. Juni angepasst.</span><span class="sxs-lookup"><span data-stu-id="6f1aa-116">For example, 1:00 PM on June 6 gets adjusted to 12:00 AM on June 7.</span></span>
    
<span data-ttu-id="6f1aa-117">Das ganztägige Ereignis, das Sie erstellen, ist also immer die Start-und Endzeit, die Sie angeben, aber möglicherweise zusätzliche Zeit im Kalender des Benutzers aufgrund der Verschiebung bis Mitternacht beansprucht.</span><span class="sxs-lookup"><span data-stu-id="6f1aa-117">So the all-day event that you create is always inclusive of the start and end time that you specify, but might claim additional time on the user's calendar due to the shift to midnight.</span></span> <span data-ttu-id="6f1aa-118">Da der Server die Start-und Endzeit auf Mitternacht anpassen wird, wird empfohlen, dass Sie die Start-und Endzeit um Mitternacht angeben, um unbeabsichtigte Änderungen an den Zeiten zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="6f1aa-118">Because the server will adjust the start and end time to midnight, we recommend that you specify your start and end time at midnight to avoid any unintended changes to the times.</span></span>
  
<span data-ttu-id="6f1aa-119">Bei der Erstellung von ganztägigen Ereignissen ist es auch wichtig, Zeitzonen zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="6f1aa-119">It's also important to consider time zones when creating all-day events.</span></span> <span data-ttu-id="6f1aa-120">Da der Exchange-Server eine Mitternachts Start-und-Endzeit in der Zeitzone der Anforderung oder des Termins erzwingt, kann das Anzeigen dieses ganztägigen Ereignisses in einem für eine andere Zeitzone konfigurierten Client unerwartete Ergebnisse liefern.</span><span class="sxs-lookup"><span data-stu-id="6f1aa-120">Because the Exchange server enforces a midnight start and end time in the time zone of the request or appointment, viewing that all-day event in a client configured for a different time zone can yield unexpected results.</span></span> <span data-ttu-id="6f1aa-121">Je nach Client kann es als ganztägiges Ereignis mit zusätzlichen Tagen angezeigt werden, die Sie nicht einschließen wollten, oder es wird möglicherweise nicht als ganztägiges Ereignis insgesamt angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6f1aa-121">Depending on the client, it might appear as an all-day event with extra days that you did not intend to include, or it might not appear as an all-day event altogether.</span></span> <span data-ttu-id="6f1aa-122">Aus diesem Grund wird empfohlen, die bevorzugte Zeitzone des Benutzers zu verwenden, wenn immer möglich, wenn Sie ganztägige Ereignisse erstellen.</span><span class="sxs-lookup"><span data-stu-id="6f1aa-122">Because of this, we recommend that you use the user's preferred time zone whenever possible when you create all-day events.</span></span>
  
## <a name="create-an-all-day-event-by-using-the-ews-managed-api"></a><span data-ttu-id="6f1aa-123">Erstellen Sie ein ganztägiges Ereignis mithilfe der verwaltete EWS-API</span><span class="sxs-lookup"><span data-stu-id="6f1aa-123">Create an all-day event by using the EWS Managed API</span></span>

<span data-ttu-id="6f1aa-124">Im folgenden Beispiel wird gezeigt, wie Sie mithilfe der verwaltete EWS-API ein ganztägiges Ereignis erstellen, beginnend mit dem durch den Parameter _StartDate_ angegebenen Datum und einer dauerhaften Anzahl von Tagen, die durch den _numDays_ -Parameter angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="6f1aa-124">The following example shows how to use the EWS Managed API to create an all-day event, starting on the date specified by the  _startDate_ parameter and lasting for the number of days specified by the  _numDays_ parameter.</span></span> <span data-ttu-id="6f1aa-125">Beachten Sie, dass der Termin in der Zeitzone erstellt wird, die durch die [Datei "ExchangeService. TimeZone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.timezone%28v=exchg.80%29.aspx) -Eigenschaft angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6f1aa-125">Note that the appointment will be created in the time zone specified by the [ExchangeService.TimeZone](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.timezone%28v=exchg.80%29.aspx) property.</span></span> <span data-ttu-id="6f1aa-126">In diesem Beispiel wird davon ausgegangen, dass das [Datei "ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objekt, das im Parameter _Service_ übergeben wurde, mit gültigen Werten für die Eigenschaften [Credentials](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) und [URL](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="6f1aa-126">This example assumes that the [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object passed in the  _service_ parameter has been initialized with valid values for the [Credentials](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) and [Url](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) properties.</span></span> 
  
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

## <a name="create-an-all-day-event-by-using-ews"></a><span data-ttu-id="6f1aa-127">Erstellen eines ganztägigen Ereignisses mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="6f1aa-127">Create an all-day event by using EWS</span></span>

<span data-ttu-id="6f1aa-128">Das folgende Beispiel zeigt eine EWS- [CreateItem-Vorgangs](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) Anforderung zum Erstellen eines ganztägigen Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="6f1aa-128">The following example shows an EWS [CreateItem operation](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) request to create an all-day event.</span></span> <span data-ttu-id="6f1aa-129">Der Termin wird in der östlichen Zeitzone erstellt, wie vom [timezonecontext](https://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) -Element angegeben.</span><span class="sxs-lookup"><span data-stu-id="6f1aa-129">The appointment is created in the Eastern time zone, as indicated by the [TimeZoneContext](https://msdn.microsoft.com/library/573c462b-aa1d-4ba0-8852-e3f48b26873b%28Office.15%29.aspx) element.</span></span> <span data-ttu-id="6f1aa-130">Beachten Sie, dass der Zeitbereich der Werte für [Start](https://msdn.microsoft.com/library/7cfe9979-c893-4f9b-b3a1-8f9e17515a4b%28Office.15%29.aspx) das Start [-und](https://msdn.microsoft.com/library/72329821-32ff-495d-b6e5-fdc011003c2e%28Office.15%29.aspx) Endelement sowohl "04:00Z" ist, das in der östlichen Zeitzone während der Sommerzeit in Mitternacht konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="6f1aa-130">Notice that the time portion of the values of the [Start](https://msdn.microsoft.com/library/7cfe9979-c893-4f9b-b3a1-8f9e17515a4b%28Office.15%29.aspx) and [End](https://msdn.microsoft.com/library/72329821-32ff-495d-b6e5-fdc011003c2e%28Office.15%29.aspx) elements are both 04:00Z, which converts to midnight in the Eastern time zone during daylight saving time.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

## <a name="see-also"></a><span data-ttu-id="6f1aa-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6f1aa-131">See also</span></span>


- [<span data-ttu-id="6f1aa-132">Kalender und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="6f1aa-132">Calendars and EWS in Exchange</span></span>](calendars-and-ews-in-exchange.md)
    
- [<span data-ttu-id="6f1aa-133">Erstellen von Terminen und Besprechungen mithilfe von EWS in Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="6f1aa-133">Create appointments and meetings by using EWS in Exchange 2013</span></span>](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [<span data-ttu-id="6f1aa-134">Zeitzonen und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="6f1aa-134">Time zones and EWS in Exchange</span></span>](time-zones-and-ews-in-exchange.md)
    

