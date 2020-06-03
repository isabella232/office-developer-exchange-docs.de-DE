---
title: Erstellen einer Terminserie mithilfe von EWS in Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 88ed6e87-25f7-4a54-83fa-d757a0ff2528
description: Erfahren Sie, wie Sie wiederkehrende Besprechungen mithilfe der verwaltete EWS-API oder EWS in Exchange erstellen.
ms.openlocfilehash: 1d04bd48c56a1a0e94eb1368166f776b3dfeb23a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456871"
---
# <a name="create-a-recurring-series-by-using-ews-in-exchange"></a><span data-ttu-id="44e5a-103">Erstellen einer Terminserie mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="44e5a-103">Create a recurring series by using EWS in Exchange</span></span>

<span data-ttu-id="44e5a-104">Erfahren Sie, wie Sie wiederkehrende Besprechungen mithilfe der verwaltete EWS-API oder EWS in Exchange erstellen.</span><span class="sxs-lookup"><span data-stu-id="44e5a-104">Learn how to create recurring meetings by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="44e5a-105">Das Erstellen einer Terminserie oder Besprechung ist nicht ganz so viel anders als das Erstellen [eines Termins oder einer Besprechung einer einzelnen Instanz](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md).</span><span class="sxs-lookup"><span data-stu-id="44e5a-105">Creating a recurring appointment or meeting isn't all that much different than creating [a single instance appointment or meeting](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md).</span></span> <span data-ttu-id="44e5a-106">Sie müssen nur einigen weiteren Serien bezogenen Eigenschaftenwerte zuweisen.</span><span class="sxs-lookup"><span data-stu-id="44e5a-106">You just need to assign values to a few additional recurrence-related properties.</span></span> <span data-ttu-id="44e5a-107">Diese werden für das [Serien](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.recurrence%28v=exchg.80%29.aspx) Objekt eines [Datei "ExchangeService. Termin](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) Objekts (wenn Sie das verwaltete EWS-API verwenden) oder das untergeordnete [Serien](https://msdn.microsoft.com/library/5f164e5b-47b6-4242-b6b9-8d650090a831%28Office.15%29.aspx) Element eines [CalendarItem](https://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) -Elements (wenn Sie EWS verwenden) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="44e5a-107">These are set on an [ExchangeService.Appointment](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) object's [Recurrence](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.recurrence%28v=exchg.80%29.aspx) object (if you're using the EWS Managed API), or the [Recurrence](https://msdn.microsoft.com/library/5f164e5b-47b6-4242-b6b9-8d650090a831%28Office.15%29.aspx) child element of a [CalendarItem](https://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) element (if you're using EWS).</span></span> <span data-ttu-id="44e5a-108">Eine Sache, die Sie beim Erstellen einer wiederkehrenden statt einer Besprechung mit einer einzelnen Instanz berücksichtigen müssen, ist, dass das von Ihnen erstellte Kalenderelement der wiederkehrende Master für eine Datenreihe ist.</span><span class="sxs-lookup"><span data-stu-id="44e5a-108">One thing to consider when you create a recurring, rather than a single-instance meeting, is that the calendar item you create is the recurring master for a series.</span></span> <span data-ttu-id="44e5a-109">Eine Reihe von Eigenschaften wird nur für einen wiederkehrenden Master festgelegt. Diese Eigenschaften können Ihnen dabei helfen, einzelne Instanzen in einer Datenreihe zu finden, zu ändern oder zu löschen.</span><span class="sxs-lookup"><span data-stu-id="44e5a-109">A number of properties are set only on a recurring master; these properties can help you find, modify, or delete individual instances in a series.</span></span> <span data-ttu-id="44e5a-110">Aus diesem Grund kann es hilfreich sein, die ID des wiederkehrenden Masters nachzuverfolgen, wenn Sie eine wiederkehrende Reihe erstellen.</span><span class="sxs-lookup"><span data-stu-id="44e5a-110">For this reason, it might be useful to keep track of the ID of the recurring master when you create a recurring series.</span></span> 
  
<span data-ttu-id="44e5a-111">**Tabelle 1. Eigenschaften, die für wiederkehrende Master Kalenderelemente festgelegt wurden**</span><span class="sxs-lookup"><span data-stu-id="44e5a-111">**Table 1. Properties set on recurring master calendar items**</span></span>

|<span data-ttu-id="44e5a-112">**Verwaltete EWS-API Klasse oder Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="44e5a-112">**EWS Managed API class or property**</span></span>|<span data-ttu-id="44e5a-113">**EWS-XML-Element**</span><span class="sxs-lookup"><span data-stu-id="44e5a-113">**EWS XML element**</span></span>|<span data-ttu-id="44e5a-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="44e5a-114">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="44e5a-115">Serien Klasse</span><span class="sxs-lookup"><span data-stu-id="44e5a-115">Recurrence class</span></span>](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.recurrence%28v=exchg.80%29.aspx) <br/> <span data-ttu-id="44e5a-116">Die **Serien** Klasse ist die Basisklasse für eine abgeleitete Muster Klasse, entweder [IntervalPattern](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.recurrence.intervalpattern%28v=exchg.80%29.aspx), [RelativeYearlyPattern](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.recurrence.relativeyearlypattern%28v=exchg.80%29.aspx)oder [YearlyPattern](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.recurrence.yearlypattern%28v=exchg.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="44e5a-116">The **Recurrence** class is the base class for a derived pattern class, either [IntervalPattern](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.recurrence.intervalpattern%28v=exchg.80%29.aspx), [RelativeYearlyPattern](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.recurrence.relativeyearlypattern%28v=exchg.80%29.aspx), or [YearlyPattern](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.recurrence.yearlypattern%28v=exchg.80%29.aspx).</span></span>  <br/> |[<span data-ttu-id="44e5a-117">Serie (serietype)</span><span class="sxs-lookup"><span data-stu-id="44e5a-117">Recurrence (RecurrenceType)</span></span>](https://msdn.microsoft.com/library/3d1c2c1c-4103-47ce-ad3c-ad16ec6e9b12%28Office.15%29.aspx) <br/> |<span data-ttu-id="44e5a-118">Enthält Serien bezogene Informationen, einschließlich des Serienmusters (täglich, wöchentlich, monatlich usw.), Start-und Enddatum, Anzahl der Vorkommen usw.</span><span class="sxs-lookup"><span data-stu-id="44e5a-118">Contains recurrence-related information, including the recurrence pattern (daily, weekly, monthly, and so on), start and end date, number of occurrences, and so on.</span></span>  <br/> |
|[<span data-ttu-id="44e5a-119">FirstOccurrence-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="44e5a-119">FirstOccurrence property</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.firstoccurrence%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="44e5a-120">FirstOccurrence</span><span class="sxs-lookup"><span data-stu-id="44e5a-120">FirstOccurrence</span></span>](https://msdn.microsoft.com/library/d6748860-ce0d-4d2e-b7e4-9ed834f1e45a%28Office.15%29.aspx) <br/> |<span data-ttu-id="44e5a-121">Enthält die Anfangs-und Endzeiten sowie die Element-ID für die erste Besprechung in einer Datenreihe.</span><span class="sxs-lookup"><span data-stu-id="44e5a-121">Contains the start and end times and the item ID for the first meeting in a series.</span></span>  <br/> |
|[<span data-ttu-id="44e5a-122">LastOccurrence-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="44e5a-122">LastOccurrence property</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.lastoccurrence%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="44e5a-123">LastOccurrence</span><span class="sxs-lookup"><span data-stu-id="44e5a-123">LastOccurrence</span></span>](https://msdn.microsoft.com/library/c9ef0fcb-4265-4e60-9986-fff0f211d00b%28Office.15%29.aspx) <br/> |<span data-ttu-id="44e5a-124">Enthält die Anfangs-und Endzeiten sowie die Element-ID für die letzte Besprechung in einer Datenreihe.</span><span class="sxs-lookup"><span data-stu-id="44e5a-124">Contains the start and end times and the item ID for the last meeting in a series.</span></span>  <br/> |
|[<span data-ttu-id="44e5a-125">ModifiedOccurrences-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="44e5a-125">ModifiedOccurrences property</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.modifiedoccurrences%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="44e5a-126">ModifiedOccurrences</span><span class="sxs-lookup"><span data-stu-id="44e5a-126">ModifiedOccurrences</span></span>](https://msdn.microsoft.com/library/552932fc-b3b4-486e-8d73-32c0bb10bd68%28Office.15%29.aspx) <br/> |<span data-ttu-id="44e5a-127">Enthält die Gruppe aller Besprechungen in der Datenreihe, die aus dem ursprünglichen Serienmuster geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="44e5a-127">Contains the set of all meetings in the series that have been modified from the original recurrence pattern.</span></span>  <br/> |
|[<span data-ttu-id="44e5a-128">DeletedOccurrences-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="44e5a-128">DeletedOccurrences property</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.deletedoccurrences%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="44e5a-129">DeletedOccurrences</span><span class="sxs-lookup"><span data-stu-id="44e5a-129">DeletedOccurrences</span></span>](https://msdn.microsoft.com/library/736fb305-9528-4be8-ad37-65d7556edbf2%28Office.15%29.aspx) <br/> |<span data-ttu-id="44e5a-130">Enthält die Gruppe aller Besprechungen in der Datenreihe, die aus dem ursprünglichen Serienmuster gelöscht wurden.</span><span class="sxs-lookup"><span data-stu-id="44e5a-130">Contains the set of all meetings in the series that have been deleted from the original recurrence pattern.</span></span>  <br/> |
   
<span data-ttu-id="44e5a-131">Da es sich bei Besprechungen im Wesentlichen um Termine handelt, die Teilnehmer umfassen, zeigen die Codebeispiele in diesem Artikel, wie wiederkehrende Besprechungen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="44e5a-131">Because meetings are essentially appointments that include attendees, the code examples in this article show how to create recurring meetings.</span></span> <span data-ttu-id="44e5a-132">Wenn Sie eine Terminserie erstellen möchten, können Sie die Beispiele ändern, indem Sie Code im Zusammenhang mit den Teilnehmern entfernen.</span><span class="sxs-lookup"><span data-stu-id="44e5a-132">If you want to create a recurring appointment, you can modify the examples by removing code related to attendees.</span></span>
  
## <a name="create-a-recurring-meeting-by-using-the-ews-managed-api"></a><span data-ttu-id="44e5a-133">Erstellen einer Besprechungsserie mithilfe der verwaltete EWS-API</span><span class="sxs-lookup"><span data-stu-id="44e5a-133">Create a recurring meeting by using the EWS Managed API</span></span>
<span data-ttu-id="44e5a-134"><a name="bk_CreateMtgEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="44e5a-134"><a name="bk_CreateMtgEWSMA"> </a></span></span>

<span data-ttu-id="44e5a-135">Das folgende Codebeispiel zeigt, wie Sie eine Besprechungsserie erstellen.</span><span class="sxs-lookup"><span data-stu-id="44e5a-135">The following code example shows how to create a recurring meeting.</span></span> <span data-ttu-id="44e5a-136">Weisen Sie zunächst den Eigenschaften eines [Termin Objekts](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) , das zum Erstellen einer Besprechung verwendet wird, Werte zu, und verwenden Sie dann die [Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) -Methode, um die wiederkehrende Reihe in Ihrem Kalenderordner zu speichern und Besprechungsanfragen an die Teilnehmer zu senden.</span><span class="sxs-lookup"><span data-stu-id="44e5a-136">First, assign values to the properties of an [Appointment object](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) used to create a meeting, then use the [Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) method to save the recurring series to your calendar folder, and send meeting requests to your attendees.</span></span> <span data-ttu-id="44e5a-137">Verwenden Sie schließlich die [Termin. Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) -Methode, um die Werte zu betrachten, die für den wiederkehrenden Master für die wiederkehrende Reihe festgelegt wurden, die Sie soeben erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="44e5a-137">Finally, use the [Appointment.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) method to look at the values set on the recurring master for the recurring series you just created.</span></span> 
  
<span data-ttu-id="44e5a-138">In diesem Beispiel wird davon ausgegangen, das Sie sich an einem Exchange-Server angemeldet haben und das [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt **service** erhalten haben.</span><span class="sxs-lookup"><span data-stu-id="44e5a-138">This example assumes that you have authenticated to an Exchange server and have acquired an [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object named **service**.</span></span> <span data-ttu-id="44e5a-139">Die Methode in diesem Beispiel gibt die [Element-ID](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) des wiederkehrenden Masters der wiederkehrenden Reihe zurück.</span><span class="sxs-lookup"><span data-stu-id="44e5a-139">The method in this example returns the [item ID](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) of the recurring series' recurring master.</span></span> 
  
```cs
public static ItemId CreateARecurringMeeting(ExchangeService service)
{        Appointment recurrMeeting = new Appointment(service);
        // Set the properties you need to create a meeting.
        recurrMeeting.Subject = "Weekly Update Meeting";
        recurrMeeting.Body = "Come hear about how the project is coming along!";
        recurrMeeting.Start = DateTime.Now.AddDays(1);
        recurrMeeting.End = recurrMeeting.Start.AddHours(1);
        recurrMeeting.Location = "Contoso Main Gallery";
        recurrMeeting.RequiredAttendees.Add("Mack@contoso.com");
        recurrMeeting.RequiredAttendees.Add("Sadie@contoso.com");
        recurrMeeting.RequiredAttendees.Add("Magdalena@contoso.com"); recurrMeeting.ReminderMinutesBeforeStart = 30;
             
        DayOfTheWeek[] dow = new DayOfTheWeek[] { (DayOfTheWeek)recurrMeeting.Start.DayOfWeek };
        // The following are the recurrence-specific properties for the meeting.
        recurrMeeting.Recurrence = new Recurrence.WeeklyPattern(recurrMeeting.Start.Date, 1, dow);
        recurrMeeting.Recurrence.StartDate = recurrMeeting.Start.Date;
        recurrMeeting.Recurrence.NumberOfOccurrences = 10;
        // This method results in in a CreateItem call to EWS.
        recurrMeeting.Save(SendInvitationsMode.SendToAllAndSaveCopy);
        // Retrieve the meeting subject and the properties that are set on a recurring master when a recurring series is created.
        recurrMeeting = Appointment.Bind(service, recurrMeeting.Id, new PropertySet(AppointmentSchema.Subject,
                                                                                    AppointmentSchema.AppointmentType, 
                                                                                    AppointmentSchema.Recurrence, 
                                                                                    AppointmentSchema.FirstOccurrence,
                                                                                    AppointmentSchema.LastOccurrence,
                                                                                    AppointmentSchema.ModifiedOccurrences,
                                                                                    AppointmentSchema.DeletedOccurrences));
        // Print out the recurring master properties.
        Console.WriteLine("\nAppointment created: " + recurrMeeting.Subject);
        Console.WriteLine("Appointment Type: {0}\n", recurrMeeting.AppointmentType);
        Console.WriteLine("These property values are always null unless the item is a recurring master:\n");
        Console.WriteLine("\tRecurrence pattern: {0}", recurrMeeting.Recurrence.ToString());
        Console.WriteLine("\tRecurring series start Date: {0}", recurrMeeting.Recurrence.StartDate.ToString());
        Console.WriteLine("\tRecurring series end Date: {0}", 
                        recurrMeeting.Recurrence.EndDate == null ? "Null" : recurrMeeting.Recurrence.EndDate.ToString());
        Console.WriteLine("\tHas end: {0}", recurrMeeting.Recurrence.HasEnd.ToString());
        Console.WriteLine("\tNumber of occurrances: {0}", recurrMeeting.Recurrence.NumberOfOccurrences);
        Console.WriteLine("\tLast 24 characters of the first occurrence's item ID:\t {0}", 
                        recurrMeeting.FirstOccurrence.ItemId.ToString().Substring(144));
        Console.WriteLine("\tLast 24 characters of the last occurrence's item ID:\t {0}", 
                        recurrMeeting.LastOccurrence.ItemId.ToString().Substring(144)); 
        Console.WriteLine("\tModified Occurrences: {0}", 
                        (recurrMeeting.ModifiedOccurrences == null ? "Null" : recurrMeeting.ModifiedOccurrences.Count.ToString()));
        Console.WriteLine("\tDeleted Occurrences: {0}", 
                        recurrMeeting.DeletedOccurrences == null ? "Null" : recurrMeeting.ModifiedOccurrences.Count.ToString());
        // Return the ID of the recurring master.
        return recurrMeeting.Id;
}

```

## <a name="create-a-recurring-meeting-by-using-ews"></a><span data-ttu-id="44e5a-140">Erstellen einer Besprechungsserie mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="44e5a-140">Create a recurring meeting by using EWS</span></span>
<span data-ttu-id="44e5a-141"><a name="bk_CreateMtgEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="44e5a-141"><a name="bk_CreateMtgEWS"> </a></span></span>

<span data-ttu-id="44e5a-142">Der Anforderungs-und Antwort-XML-Code in den folgenden Beispielen entspricht den aufrufen, die zum [Erstellen einer Besprechungsserie mithilfe der verwaltete EWS-API](#bk_CreateMtgEWSMA)ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="44e5a-142">The request and response XML in the following examples correspond to calls made to [create a recurring meeting by using the EWS Managed API](#bk_CreateMtgEWSMA).</span></span> <span data-ttu-id="44e5a-143">Beachten Sie, dass die Anforderung im Wesentlichen identisch mit dem Festlegen von Serien spezifischen Werten für das [Serien](https://msdn.microsoft.com/library/5f164e5b-47b6-4242-b6b9-8d650090a831%28Office.15%29.aspx) Element ist, die Sie zum Erstellen eines Termins mit einer einzelnen Instanz verwenden würden.</span><span class="sxs-lookup"><span data-stu-id="44e5a-143">Note that other than setting recurrence-specific values on the [Recurrence](https://msdn.microsoft.com/library/5f164e5b-47b6-4242-b6b9-8d650090a831%28Office.15%29.aspx) element, the request is essentially the same as one you would use to create a single-instance appointment.</span></span> <span data-ttu-id="44e5a-144">Das folgende Beispiel zeigt den Anforderungs-XML-Code beim Erstellen einer Besprechung mithilfe des [CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx)-Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="44e5a-144">The following example shows the request XML when you use the [CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) operation to create a meeting.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Name="(UTC-08:00) Pacific Time (US &amp;amp; Canada)" Id="Pacific Standard Time">
        <t:Periods>
          <t:Period Bias="P0DT8H0M0.0S" Name="Standard" Id="Std" />
          <t:Period Bias="P0DT7H0M0.0S" Name="Daylight" Id="Dlt/1" />
          <t:Period Bias="P0DT7H0M0.0S" Name="Daylight" Id="Dlt/2007" />
        </t:Periods>
        <t:TransitionsGroups>
          <t:TransitionsGroup Id="0">
            <t:RecurringDayTransition>
              <t:To Kind="Period">Dlt/1</t:To>
              <t:TimeOffset>P0DT2H0M0.0S</t:TimeOffset>
              <t:Month>4</t:Month>
              <t:DayOfWeek>Sunday</t:DayOfWeek>
              <t:Occurrence>1</t:Occurrence>
            </t:RecurringDayTransition>
            <t:RecurringDayTransition>
              <t:To Kind="Period">Std</t:To>
              <t:TimeOffset>P0DT2H0M0.0S</t:TimeOffset>
              <t:Month>10</t:Month>
              <t:DayOfWeek>Sunday</t:DayOfWeek>
              <t:Occurrence>-1</t:Occurrence>
            </t:RecurringDayTransition>
          </t:TransitionsGroup>
          <t:TransitionsGroup Id="1">
            <t:RecurringDayTransition>
              <t:To Kind="Period">Dlt/2007</t:To>
              <t:TimeOffset>P0DT2H0M0.0S</t:TimeOffset>
              <t:Month>3</t:Month>
              <t:DayOfWeek>Sunday</t:DayOfWeek>
              <t:Occurrence>2</t:Occurrence>
            </t:RecurringDayTransition>
            <t:RecurringDayTransition>
              <t:To Kind="Period">Std</t:To>
              <t:TimeOffset>P0DT2H0M0.0S</t:TimeOffset>
              <t:Month>11</t:Month>
              <t:DayOfWeek>Sunday</t:DayOfWeek>
              <t:Occurrence>1</t:Occurrence>
            </t:RecurringDayTransition>
          </t:TransitionsGroup>
        </t:TransitionsGroups>
        <t:Transitions>
          <t:Transition>
            <t:To Kind="Group">0</t:To>
          </t:Transition>
          <t:AbsoluteDateTransition>
            <t:To Kind="Group">1</t:To>
            <t:DateTime>2007-01-01T08:00:00.000Z</t:DateTime>
          </t:AbsoluteDateTransition>
        </t:Transitions>
      </t:TimeZoneDefinition>
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:CreateItem SendMeetingInvitations="SendToAllAndSaveCopy">
      <m:Items>
        <t:CalendarItem>
          <t:Subject>Weekly Update Meeting</t:Subject>
          <t:Body BodyType="HTML">Come hear about how the Organized Observational Paradigm SkyNet project is coming along!</t:Body>
          <t:ReminderMinutesBeforeStart>30</t:ReminderMinutesBeforeStart>
          <t:Start>2014-03-08T13:21:32.868-08:00</t:Start>
          <t:End>2014-03-08T14:21:32.868-08:00</t:End>
          <t:Location>Contoso Main Gallery</t:Location>
          <t:RequiredAttendees>
            <t:Attendee>
              <t:Mailbox>
                <t:EmailAddress>Mack@contoso.com</t:EmailAddress>
              </t:Mailbox>
            </t:Attendee>
            <t:Attendee>
              <t:Mailbox>
                <t:EmailAddress>Sadie@contoso.com</t:EmailAddress>
              </t:Mailbox>
            </t:Attendee>
            <t:Attendee>
              <t:Mailbox>
                <t:EmailAddress>Magdalena@contoso.com</t:EmailAddress>
              </t:Mailbox>
            </t:Attendee>
          </t:RequiredAttendees>
          <t:Recurrence>
            <t:WeeklyRecurrence>
              <t:Interval>1</t:Interval>
              <t:DaysOfWeek>Saturday</t:DaysOfWeek>
            </t:WeeklyRecurrence>
            <t:NumberedRecurrence>
              <t:StartDate>2014-03-08-08:00</t:StartDate>
              <t:NumberOfOccurrences>10</t:NumberOfOccurrences>
            </t:NumberedRecurrence>
          </t:Recurrence>
        </t:CalendarItem>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>

```

 <span data-ttu-id="44e5a-145">Das folgende Beispiel zeigt den Antwort-XML-Code, der vom **CreateItem**-Vorgang zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="44e5a-145">The following example shows the response XML that is returned by the **CreateItem** operation.</span></span> 
  
<span data-ttu-id="44e5a-146">Die Attribute **ItemID** und **ChangeKey** werden zur Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="44e5a-146">The **ItemId** and **ChangeKey** attributes are shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="893" MinorBuildNumber="10" 
                         Version="V2_10" xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:CreateItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:CreateItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:CalendarItem>
              <t:ItemId Id="AAMkAD" ChangeKey="DwAAAB" />
            </t:CalendarItem>
          </m:Items>
        </m:CreateItemResponseMessage>
      </m:ResponseMessages>
    </m:CreateItemResponse>
  </s:Body>
</s:Envelope>

```

<span data-ttu-id="44e5a-147">Das folgende Beispiel zeigt den Anforderungs-XML-Code, der generiert wird, wenn Sie den [GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) -Vorgang und das **ItemID** -Objekt für die von Ihnen erstellte Datenreihe verwenden und Anforderungseigenschaften nur für einen wiederkehrenden Master festlegen, um zu bestätigen, dass die vom Server zurückgegebene **ItemID** beim Erstellen einer wiederkehrenden Reihe für eine wiederkehrende Masterseite gilt</span><span class="sxs-lookup"><span data-stu-id="44e5a-147">The following example shows the request XML that is generated when you use the [GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) operation and the **ItemId** for the series you created, and request properties only set on a recurring master to confirm that the **ItemId** returned by the server when creating a recurring series is for a recurring master.</span></span> 
  
<span data-ttu-id="44e5a-148">Die Attribute **ItemID** und **ChangeKey** werden zur Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="44e5a-148">The **ItemId** and **ChangeKey** attributes are shortened for readability.</span></span> 
  
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
    <m:GetItem>
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
          <t:FieldURI FieldURI="calendar:CalendarItemType" />
          <t:FieldURI FieldURI="calendar:Recurrence" />
          <t:FieldURI FieldURI="calendar:FirstOccurrence" />
          <t:FieldURI FieldURI="calendar:LastOccurrence" />
          <t:FieldURI FieldURI="calendar:ModifiedOccurrences" />
          <t:FieldURI FieldURI="calendar:DeletedOccurrences" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:ItemIds>
        <t:ItemId Id="AAMkAD" ChangeKey="DwAAAB" />
      </m:ItemIds>
    </m:GetItem>
  </soap:Body>
</soap:Envelope>

```

 <span data-ttu-id="44e5a-149">Das folgende Beispiel zeigt den Antwort-XML-Code, der vom **GetItem**-Vorgang zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="44e5a-149">The following example shows the response XML that is returned by the **GetItem** operation.</span></span> 
  
<span data-ttu-id="44e5a-150">Die Attribute **ItemID** und **ChangeKey** werden zur Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="44e5a-150">The **ItemId** and **ChangeKey** attributes are shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="893" MinorBuildNumber="10" 
                         Version="V2_10" xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:CalendarItem>
              <t:ItemId Id="AAMkAD" ChangeKey="DwAAAB" />
              <t:Subject>Weekly Update Meeting</t:Subject>
              <t:CalendarItemType>RecurringMaster</t:CalendarItemType>
              <t:Recurrence>
                <t:WeeklyRecurrence>
                  <t:Interval>1</t:Interval>
                  <t:DaysOfWeek>Saturday</t:DaysOfWeek>
                </t:WeeklyRecurrence>
                <t:NumberedRecurrence>
                  <t:StartDate>2014-03-08-08:00</t:StartDate>
                  <t:NumberOfOccurrences>10</t:NumberOfOccurrences>
                </t:NumberedRecurrence>
              </t:Recurrence>
              <t:FirstOccurrence>
                <t:ItemId Id="AAMkAD" ChangeKey="DwAAABY" />
                <t:Start>2014-03-08T21:21:00Z</t:Start>
                <t:End>2014-03-08T22:21:00Z</t:End>
                <t:OriginalStart>2014-03-08T21:21:00Z</t:OriginalStart>
              </t:FirstOccurrence>
              <t:LastOccurrence>
                <t:ItemId Id="AAMkAD" ChangeKey="DwAAABY" />
                <t:Start>2014-05-10T20:21:00Z</t:Start>
                <t:End>2014-05-10T21:21:00Z</t:End>
                <t:OriginalStart>2014-05-10T20:21:00Z</t:OriginalStart>
              </t:LastOccurrence>
            </t:CalendarItem>
          </m:Items>
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </m:GetItemResponse>
  </s:Body>
</s:Envelope>

```

## <a name="see-also"></a><span data-ttu-id="44e5a-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="44e5a-151">See also</span></span>


- [<span data-ttu-id="44e5a-152">Kalender und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="44e5a-152">Calendars and EWS in Exchange</span></span>](calendars-and-ews-in-exchange.md)
    
- [<span data-ttu-id="44e5a-153">Erstellen von Terminen und Besprechungen mithilfe von EWS in Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="44e5a-153">Create appointments and meetings by using EWS in Exchange 2013</span></span>](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [<span data-ttu-id="44e5a-154">Serienmuster und EWS</span><span class="sxs-lookup"><span data-stu-id="44e5a-154">Recurrence patterns and EWS</span></span>](recurrence-patterns-and-ews.md)
    
- [<span data-ttu-id="44e5a-155">Zugreifen auf eine Terminserie mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="44e5a-155">Access a recurring series by using EWS in Exchange</span></span>](how-to-access-a-recurring-series-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="44e5a-156">Löschen von Terminen in einer Terminserie mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="44e5a-156">Delete appointments in a recurring series by using EWS in Exchange</span></span>](how-to-delete-appointments-in-a-recurring-series-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="44e5a-157">Aktualisieren einer Terminserie mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="44e5a-157">Update a recurring series by using EWS</span></span>](how-to-update-a-recurring-series-by-using-ews.md)
    
- [<span data-ttu-id="44e5a-158">Aktualisieren einer Terminserie mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="44e5a-158">Update a recurring series by using EWS in Exchange</span></span>](how-to-update-a-recurring-series-by-using-ews-in-exchange.md)
    

