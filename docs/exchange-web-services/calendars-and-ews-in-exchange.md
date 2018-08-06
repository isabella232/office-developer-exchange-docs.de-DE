---
title: Kalender und EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: b87b0180-f5b5-44e4-b6ac-4f23e476b03b
description: Weitere Informationen zu Kalendern, Kalenderordnern und -elementen, Terminen und Besprechungen in Exchange.
ms.openlocfilehash: bb9702118ff1db66862a5788c2d8f58dd55c4d09
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756818"
---
# <a name="calendars-and-ews-in-exchange"></a><span data-ttu-id="7e2e9-103">Kalender und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="7e2e9-103">Calendars and EWS in Exchange</span></span>

<span data-ttu-id="7e2e9-104">Weitere Informationen zu Kalendern, Kalenderordnern und -elementen, Terminen und Besprechungen in Exchange.</span><span class="sxs-lookup"><span data-stu-id="7e2e9-104">Learn about calendars, calendar folders and items, appointments, and meetings in Exchange.</span></span>
  
<span data-ttu-id="7e2e9-105">Sie sind wahrscheinlich mit den vielen Kalenderfunktionen in E-Mail-Clients wie Outlook vertraut, mit denen Sie Termine pflegen, Besprechungen planen, die Verfügbarkeit anderer Personen prüfen, Teilnehmer einladen und Besprechungen ändern oder absagen können.</span><span class="sxs-lookup"><span data-stu-id="7e2e9-105">You're probably familiar with many of the calendar features in email clients like Outlook, which enable you to track appointments, schedule meetings, check people's availability, invite attendees, and change or cancel meetings.</span></span>
  
<span data-ttu-id="7e2e9-p101">Kalenderbezogene Funktionen in Exchange unterscheiden sich etwas von den Optionen in einem Client wie Outlook. Statt Informationen anzuzeigen, können Sie mit EWS in Exchange beispielsweise Informationen erstellen, speichern, senden oder ändern. Um EWS zum Arbeiten mit Kalendern zu verwenden, müssen Sie vertraut sein mit Konzepten wie beispielsweise der Informationsspeicherung, Zeiten, Serien und Nachrichtenflüssen. Genauer gesagt, müssen Sie mit Folgendem vertraut sein:</span><span class="sxs-lookup"><span data-stu-id="7e2e9-p101">Calendar-related features in Exchange are a little different than what you see in a client like Outlook. Instead of displaying information, EWS in Exchange enables you to do things like create, store, send, or change information. To use EWS to work with calendars, you'll need to be familiar with concepts such as information storage, time, recurrence, and message flow. More specifically, you'll need to be familiar with the following:</span></span>
  
- <span data-ttu-id="7e2e9-110">Kalenderordner, Kalenderelemente und Kalenderansichten</span><span class="sxs-lookup"><span data-stu-id="7e2e9-110">Calendar folders, calendar items, and calendar views</span></span>
    
- <span data-ttu-id="7e2e9-111">Besprechungsanfragen, Antworten, Planung, Teilnehmern, Ressourcen, Räumen und Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="7e2e9-111">Meeting requests, responses, scheduling, attendees, resources, rooms, and availability</span></span>
    
- <span data-ttu-id="7e2e9-112">Zeiträumen, Zeitzonen und Start- und Endzeiten von Besprechungen und Terminen</span><span class="sxs-lookup"><span data-stu-id="7e2e9-112">Time durations, time zones, and start and end times of meetings and appointments</span></span>
    
- <span data-ttu-id="7e2e9-113">Terminserien, Serienmustern, Ausnahmen und einzelnen Instanzen von Terminen und Besprechungen</span><span class="sxs-lookup"><span data-stu-id="7e2e9-113">Recurring series, recurrence patterns, exceptions, and single instance appointments and meetings</span></span>
    
<span data-ttu-id="7e2e9-p102">Glücklicherweise bieten EWS und die verwaltete EWS-API zahlreiche Vorgänge und Methoden, mit denen Sie eine Vielzahl von kalenderbezogenen Aufgaben ausführen können. Sie können beispielsweise die verwaltete EWS-API verwenden, um mit nur wenigen Codezeilen eine Besprechung zu erstellen und Einladungen an die Teilnehmer versenden, wie im folgenden Beispiel veranschaulicht wird.</span><span class="sxs-lookup"><span data-stu-id="7e2e9-p102">Fortunately, EWS and the EWS Managed API provide a rich set of operations and methods that enable you to perform a wide range of calendar-related tasks. For example, using the EWS Managed API, you can create a meeting and send invitations to attendees with just a few lines of code, as shown in the following example.</span></span>
  
```cs
            Appointment meeting = new Appointment(service);
            // Set the properties on the meeting object to create the meeting.
            meeting.Subject = "Team building exercise";
            meeting.Body = "Let's learn to really work as a team and then have lunch!";
            meeting.Start = DateTime.Now.AddDays(2);
            meeting.End = meeting.Start.AddHours(2);
            meeting.Location = "Conference Room 12";
            meeting.RequiredAttendees.Add("Mack.Chaves@contoso.com");
            meeting.RequiredAttendees.Add("Sadie.Daniels@contoso.com");
            meeting.OptionalAttendees.Add("Magdalena.Kemp@contoso.com");
            meeting.ReminderMinutesBeforeStart = 60;
            // Send the meeting request
            meeting.Save(SendInvitationsMode.SendToAllAndSaveCopy);

```

## <a name="calendar-folders-and-calendar-items"></a><span data-ttu-id="7e2e9-116">Kalenderordner und Kalenderelemente</span><span class="sxs-lookup"><span data-stu-id="7e2e9-116">Calendar folders and calendar items</span></span>
<span data-ttu-id="7e2e9-117"><a name="bk_CalendarFolder"> </a></span><span class="sxs-lookup"><span data-stu-id="7e2e9-117"></span></span>

<span data-ttu-id="7e2e9-p103">Kalenderordner enthalten Kalenderelemente. Kalenderordner besitzen eine [Ordnerklasse](http://msdn.microsoft.com/library/0041d135-2869-4612-89a5-d1aa86aa1093%28Office.15%29.aspx) von **IPF.Appointment**, und können nur Elemente enthalten, die durch die verwaltete [ItemClass](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.item.itemclass%28v=exchg.80%29.aspx)-EWS-API-Eigenschaft definiert sind, die mit einem [Appointment-Klasse](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx)-Objekt oder dem EWS-[CalendarItemType](http://msdn.microsoft.com/library/1feb0788-adf7-4a7c-830c-005214ad930f%28Office.15%29.aspx)-Element verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="7e2e9-p103">Calendar folders contain calendar items. Calendar folders have a [folder class](http://msdn.microsoft.com/library/0041d135-2869-4612-89a5-d1aa86aa1093%28Office.15%29.aspx) of **IPF.Appointment**, and can include only the items defined by the [ItemClass](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.item.itemclass%28v=exchg.80%29.aspx) EWS Managed API property, which is associated with an [Appointment Class](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) object, or the EWS [CalendarItemType](http://msdn.microsoft.com/library/1feb0788-adf7-4a7c-830c-005214ad930f%28Office.15%29.aspx) element.</span></span> 
  
<span data-ttu-id="7e2e9-120">Elemente in einem Kalenderordner unterscheiden sich etwas von Elementen in anderen Ordnern eines Postfachs, da Vorkommen in einer Terminserie und Ausnahmen in einer Terminserie keine tatsächlichen Elemente in einem Postfach sind, sondern intern als Anlagen eines Serienmasters gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="7e2e9-120">Items in a Calendar folder are a little different from items in other folders in a mailbox because occurrences in a recurring series and exceptions to a recurring series are not actual items in the mailbox, but rather are stored internally as attachments to a recurring master.</span></span> <span data-ttu-id="7e2e9-121">Um daher alle Termine in einem bestimmten Datumsbereich abzurufen, müssen Sie die Kalenderansicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="7e2e9-121">Therefore, in order to retrieve all appointments in a given date range, you need to use a calendar view.</span></span> <span data-ttu-id="7e2e9-122">Weitere Informationen zum Abrufen von Terminen und Kalenderansichten finden Sie unter [Abrufen von Terminen und Besprechungen mithilfe von EWS in Exchange](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="7e2e9-122">To learn more about retrieving appointments and calendar views, see [How to: Get appointments and meetings by using EWS in Exchange](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md).</span></span>
  
## <a name="meetings-and-appointments"></a><span data-ttu-id="7e2e9-123">Besprechungen und Termine</span><span class="sxs-lookup"><span data-stu-id="7e2e9-123">Meetings and appointments</span></span>
<span data-ttu-id="7e2e9-124"><a name="bk_meetings"> </a></span><span class="sxs-lookup"><span data-stu-id="7e2e9-124"></span></span>

<span data-ttu-id="7e2e9-p105">Der wesentliche Unterschied zwischen Besprechungen und Terminen besteht darin, dass Besprechungen über Teilnehmer verfügen und Termine nicht. Intern verwendet Exchange dasselbe Objekt für Besprechungen und Termine. Zum Arbeiten mit Besprechungen und Terminen verwenden Sie die verwaltete EWS-API-[Appointment-Klasse](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) oder das EWS- [CalendarItem](http://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx)-Element.</span><span class="sxs-lookup"><span data-stu-id="7e2e9-p105">The essential difference between meetings and appointments is that meetings have attendees, and appointments don't. Internally, Exchange uses the same object for both meetings and appointments. You use the EWS Managed API [Appointment class](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) or the EWS [CalendarItem](http://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) element to work with meetings and appointments.</span></span> 
  
<span data-ttu-id="7e2e9-128">Termine und Besprechungen können einzelne Instanzen oder teil einer [Terminserie](recurrence-patterns-and-ews.md) sein, da Termine jedoch keine Teilnehmer, Räume oder Ressourcen umfassen, muss dafür keine Nachricht gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="7e2e9-128">Both appointments and meetings can be single instances or part of a [recurring series](recurrence-patterns-and-ews.md), but because appointments don't include attendees, rooms, or resources, they do not require a message to be sent.</span></span>
  
<span data-ttu-id="7e2e9-p106">Da Besprechungen das Senden und Antworten auf Anfragen und Aktualisierungen umfasst, ist dazu mehr Aufwand nötig, als nur auf Elemente in einem Kalenderordner zuzugreifen. Sie sind auch mit einem Workflow verknüpft. Besprechungen müssen geplant werden, wenn Teilnehmer verfügbar sind und können außerdem die Reservierung eines Besprechungsraums oder von Ressourcen wie einem Projektor oder anderen Dingen umfassen.</span><span class="sxs-lookup"><span data-stu-id="7e2e9-p106">Because meetings include sending and responding to requests and updates, they involve more than just accessing items in a Calendar folder. They also have an associated workflow. Meetings must be scheduled when attendees are available, and can also involve reserving a meeting room, or resources such as a projector or other equipment.</span></span>
  
<span data-ttu-id="7e2e9-132">Zum Besprechungsworkflow gehören in der Regel folgende Schritte:</span><span class="sxs-lookup"><span data-stu-id="7e2e9-132">The meeting workflow typically involves the following steps:</span></span>
  
1. <span data-ttu-id="7e2e9-133">Ein Meeting wird erstellt und mit Informationen wie Start- und Endzeit, Ort und einem Nachrichtentext befüllt.</span><span class="sxs-lookup"><span data-stu-id="7e2e9-133">A meeting is created and populated with information such as start and end time, location, and a message body.</span></span>
    
2. <span data-ttu-id="7e2e9-134">Dann wird eine Liste mit potenziellen Teilnehmern, Ressourcen und dem Raum erstellt.</span><span class="sxs-lookup"><span data-stu-id="7e2e9-134">A list of prospective attendees, resources, and rooms is created.</span></span>
    
3. <span data-ttu-id="7e2e9-135">Anschließend wird der Verfügbarkeitsstatus der Teilnehmer überprüft.</span><span class="sxs-lookup"><span data-stu-id="7e2e9-135">The availability status of attendees is checked.</span></span> 
    
4. <span data-ttu-id="7e2e9-136">Daraufhin wird eine Besprechungsanfrage an die Teilnehmer gesendet.</span><span class="sxs-lookup"><span data-stu-id="7e2e9-136">A meeting request is sent to attendees.</span></span>
    
5. <span data-ttu-id="7e2e9-p107">Teilnehmer antworten auf die Besprechungsanfrage mit der Absicht, an der Besprechung teilzunehmen oder nicht. Teilnehmer können außerdem eine andere Zeit für die Besprechung vorschlagen.</span><span class="sxs-lookup"><span data-stu-id="7e2e9-p107">Attendees reply to the meeting with their intention to attend or not. Attendees may also propose a new time for the meeting.</span></span>
    
6. <span data-ttu-id="7e2e9-139">Besprechungen können abgesagt oder aktualisiert werden, dadurch wird in der Regel ein neues Versenden von E-Mails an die Teilnehmer ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="7e2e9-139">Meetings can be canceled or updated, which typically trigger new messages to be sent to attendees.</span></span>
    
## <a name="calendars-and-time"></a><span data-ttu-id="7e2e9-140">Kalender und die Uhrzeit</span><span class="sxs-lookup"><span data-stu-id="7e2e9-140">Calendars and time</span></span>
<span data-ttu-id="7e2e9-141"><a name="bk_Time"> </a></span><span class="sxs-lookup"><span data-stu-id="7e2e9-141"></span></span>

<span data-ttu-id="7e2e9-p108">Uhrzeitbezogene Funktionen sind integraler Bestandteil von Kalendern. Termine und Besprechungen weisen Start- und Endzeiten auf, Zeiträume und andere zeitbezogene Eigenschaften, wie z. B.die Zeit der Nachrichtenerstellung, Versendung und des Empfangs. Auf Basis der Start- und Endzeit können Termine und Besprechungen aus dem Kalenderordner abgerufen werden. Terminserien weisen Anfangs- und Endzeiten auf. Und Besprechungen treten innerhalb einer angegeben Zeitzone auf, die in der Weltwirtschaft immer wichtiger werden.</span><span class="sxs-lookup"><span data-stu-id="7e2e9-p108">Time-related functionality is integral to calendaring. Appointments and meetings have start and end times, durations, and other time-related properties, such as the time at which a message is created, sent, and received. Existing appointments and meetings can be retrieved from a Calendar folder based on a start and end time. Recurring series have beginnings and ends. And meetings occur within a given time zone, which is increasingly important in a global economy.</span></span>
  
<span data-ttu-id="7e2e9-p109">Uhrzeiten werden auf einem Exchange-Server intern in der koordinierten Weltzeit (Coordinated Universal Time, UTC) gespeichert. Exchange wandelt sie basierend auf den Clienteinstellungen in die Uhrzeit der lokalen Zeitzone um. [DateTime](http://msdn.microsoft.com/library/9c6ecd4c-779c-4fa5-8082-dd2bc0a751f4%28Office.15%29.aspx)-Eigenschaften beziehen sich auf die lokale Zeitzone des Computers.</span><span class="sxs-lookup"><span data-stu-id="7e2e9-p109">Times are stored internally on an Exchange server in Coordinated Universal Time (UTC). Exchange converts them to local time zone based on client settings. [DateTime](http://msdn.microsoft.com/library/9c6ecd4c-779c-4fa5-8082-dd2bc0a751f4%28Office.15%29.aspx) properties are scoped to the computer's local time zone.</span></span> 
  
## <a name="recurring-series"></a><span data-ttu-id="7e2e9-150">Terminserie</span><span class="sxs-lookup"><span data-stu-id="7e2e9-150">Recurring series</span></span>
<span data-ttu-id="7e2e9-151"><a name="bk_recurrence"> </a></span><span class="sxs-lookup"><span data-stu-id="7e2e9-151"></span></span>

<span data-ttu-id="7e2e9-p110">Eine Terminserie von Terminen oder Besprechungen besteht aus einem Serienmaster, einer Gruppe von Serienelementen, und optional aus einer Gruppe von Ausnahmeelementen. Serieninformationen werden im Serienmasterelement gespeichert. Das [RecurringMasterItemId](http://msdn.microsoft.com/library/5800b58c-f3d7-4d8f-acc0-d13e02f4e258%28Office.15%29.aspx)-EWS-Element ist mit Vorkommen und Ausnahmen in einer Serie verknüpft, außerdem können Sie die verwaltete [Appointment.BindToRecurringMaster](http://msdn.microsoft.com/de-DE/library/dd635978%28v=EXCHG.80%29.aspx)-EWS-API-Methode verwenden, um den Serienmaster abzurufen. Mithilfe einer Serieninstanz können Sie nach allen der Serie zugeordneten Elementen und Informationen suchen.</span><span class="sxs-lookup"><span data-stu-id="7e2e9-p110">A recurring series of appointments or meetings is comprised of a recurring master, a set of occurrence items, and optionally, a set of exception items. Recurrence information is stored on the recurring master item. The [RecurringMasterItemId](http://msdn.microsoft.com/library/5800b58c-f3d7-4d8f-acc0-d13e02f4e258%28Office.15%29.aspx) EWS element is associated with occurrences and exceptions in a series, or you can use the [Appointment.BindToRecurringMaster](http://msdn.microsoft.com/de-DE/library/dd635978%28v=EXCHG.80%29.aspx) EWS Managed API method to get the recurring master. Using an instance of a series, you can find all the elements and information associated with the series.</span></span> 
  
<span data-ttu-id="7e2e9-p111">Beachten Sie, dass Serieneigenschaften zu allen Kalenderelementen vorhanden sind, sie werden jedoch nur bei den Serienmasterelementen ausgefüllt. Zusätzlich zu einem Index aller Vorkommen in einer Serie besitzt der Serienmaster einen Verweis zu geänderten und gelöschten Vorkommen und Serienmustern (z. B. täglich, wöchentlich, monatlich oder jährlich).</span><span class="sxs-lookup"><span data-stu-id="7e2e9-p111">Note that recurrence properties exist on all calendar items, but they are populated only on recurring master items. In addition to an index of all occurrences in a series, the recurring master has a reference to modified and deleted occurrences and the recurrence pattern of a series (for example, daily, weekly, monthly, or yearly).</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="7e2e9-158">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="7e2e9-158">In this section</span></span>
<span data-ttu-id="7e2e9-159"><a name="bk_inthissection"> </a></span><span class="sxs-lookup"><span data-stu-id="7e2e9-159"></span></span>

- [<span data-ttu-id="7e2e9-160">Erstellen von Terminen und Besprechungen mithilfe von EWS in Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="7e2e9-160">How to: Create appointments and meetings by using EWS in Exchange 2013</span></span>](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [<span data-ttu-id="7e2e9-161">Erstellen von ganztägigen Ereignissen mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="7e2e9-161">How to: Create all-day events by using EWS in Exchange</span></span>](how-to-create-all-day-events-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="7e2e9-162">Abrufen von Terminen und Besprechungen mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="7e2e9-162">How to: Get appointments and meetings by using EWS in Exchange</span></span>](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="7e2e9-163">Aktualisieren von Terminen und Besprechungen mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="7e2e9-163">How to: Update appointments and meetings by using EWS in Exchange</span></span>](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="7e2e9-164">Löschen von Terminen und Absagen von Besprechungen mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="7e2e9-164">How to: Delete appointments and cancel meetings by using EWS in Exchange</span></span>](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="7e2e9-165">Abrufen von Raumlisten mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="7e2e9-165">How to: Get room lists by using EWS in Exchange</span></span>](how-to-get-room-lists-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="7e2e9-166">Abrufen von Frei/Gebucht-Informationen mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="7e2e9-166">How to: Get free/busy information by using EWS in Exchange</span></span>](how-to-get-free-busy-information-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="7e2e9-167">Vorschlagen einer neuen Besprechungszeit mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="7e2e9-167">How to: Propose a new meeting time by using EWS in Exchange</span></span>](how-to-propose-a-new-meeting-time-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="7e2e9-168">Verarbeiten von Kalenderelementen in Batches in Exchange</span><span class="sxs-lookup"><span data-stu-id="7e2e9-168">How to: Process calendar items in batches in Exchange</span></span>](how-to-process-calendar-items-in-batches-in-exchange.md)
    
- [<span data-ttu-id="7e2e9-169">Serienmuster und EWS</span><span class="sxs-lookup"><span data-stu-id="7e2e9-169">Recurrence patterns and EWS</span></span>](recurrence-patterns-and-ews.md)
    
## <a name="see-also"></a><span data-ttu-id="7e2e9-170">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7e2e9-170">See also</span></span>


- [<span data-ttu-id="7e2e9-171">Entwickeln von Webdienstclients für Exchange</span><span class="sxs-lookup"><span data-stu-id="7e2e9-171">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)
    
- [<span data-ttu-id="7e2e9-172">Erste Schritte mit Webdiensten in Exchange</span><span class="sxs-lookup"><span data-stu-id="7e2e9-172">Start using web services in Exchange</span></span>](start-using-web-services-in-exchange.md)
    
- [<span data-ttu-id="7e2e9-173">Übersicht über den EWS-Cliententwurf für Exchange</span><span class="sxs-lookup"><span data-stu-id="7e2e9-173">EWS client design overview for Exchange</span></span>](ews-client-design-overview-for-exchange.md)
    

