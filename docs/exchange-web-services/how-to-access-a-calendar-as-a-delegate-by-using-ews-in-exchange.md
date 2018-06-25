---
title: Zugriff auf einen Kalender als Stellvertretung mithilfe der EWS in Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: d7db4a1e-9ed6-41da-8529-a73ca285cdf2
description: Hier erfahren Sie, wie Sie einen Kalender als Stellvertreter zugreifen, indem Sie die EWS Managed API oder EWS in Exchange.
ms.openlocfilehash: 24327c28f58e728807fc5581b480d3c01d3b7208
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756858"
---
#  <a name="access-a-calendar-as-a-delegate-by-using-ews-in-exchange"></a><span data-ttu-id="6b9c9-103">Zugriff auf einen Kalender als Stellvertretung mithilfe der EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="6b9c9-103">Access a calendar as a delegate by using EWS in Exchange</span></span>

<span data-ttu-id="6b9c9-104">Hier erfahren Sie, wie Sie einen Kalender als Stellvertreter zugreifen, indem Sie die EWS Managed API oder EWS in Exchange.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-104">Learn how to access a calendar as a delegate by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="6b9c9-105">Sie können die EWS Managed API verwenden oder EWS so erteilen Sie einen Benutzer delegieren des Zugriffs auf Kalenderordner des Postfachbesitzers.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-105">You can use the EWS Managed API or EWS to give a user delegate access to a mailbox owner's Calendar folder.</span></span> <span data-ttu-id="6b9c9-106">Delegaten kann dann Erstellen von Besprechungsanfragen im Auftrag des Postfachbesitzers, Erstellen von Terminen, Antworten auf Besprechungsanfragen, und abrufen, aktualisieren und Löschen von Besprechungen von der Postfachbesitzer Kalenderordner abhängig von ihren Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-106">The delegate can then create meeting requests on behalf of the mailbox owner, create appointments, respond to meeting requests, and retrieve, update, and delete meetings from the mailbox owner's Calendar folder, depending on their permissions.</span></span>
  
<span data-ttu-id="6b9c9-107">Als Stellvertretung verwenden Sie die gleichen Methoden und Vorgänge auf Kalenderordner des Postfachbesitzers zugreifen, mit denen Sie Ihre eigenen Kalenderordner zugreifen.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-107">As a delegate, you use the same methods and operations to access a mailbox owner's Calendar folder that you use to access your own Calendar folder.</span></span> <span data-ttu-id="6b9c9-108">Der Hauptunterschied ist, dass Sie mithilfe von [expliziten Access](delegate-access-and-ews-in-exchange.md#bk_explicit) suchen oder erstellen Sie ein Kalenderelement oder Kalenderunterordner, und klicken Sie dann, nachdem Sie die Element-ID oder Ordner-ID identifiziert haben, können [impliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_implicit) erhalten möchten, aktualisieren und Löschen des Elements.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-108">The main difference is that you have to use [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicit) to find or create a calendar item or calendar subfolder, and then after you identify the item ID or folder ID, you can use [implicit access](delegate-access-and-ews-in-exchange.md#bk_implicit) to get, update, or delete the item.</span></span> 
  
<span data-ttu-id="6b9c9-109">**In Tabelle 1. EWS Managed API-Methoden und EWS-Vorgänge für den Zugriff auf einen Kalender als Stellvertreter**</span><span class="sxs-lookup"><span data-stu-id="6b9c9-109">**Table 1. EWS Managed API methods and EWS operations for accessing a calendar as a delegate**</span></span>

|<span data-ttu-id="6b9c9-110">**Aktion**</span><span class="sxs-lookup"><span data-stu-id="6b9c9-110">**If you want to…**</span></span>|<span data-ttu-id="6b9c9-111">**Verwenden Sie diese Methode EWS Managed API...**</span><span class="sxs-lookup"><span data-stu-id="6b9c9-111">**Use this EWS Managed API method…**</span></span>|<span data-ttu-id="6b9c9-112">**Verwenden Sie diese Operation EWS...**</span><span class="sxs-lookup"><span data-stu-id="6b9c9-112">**Use this EWS operation…**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6b9c9-113">Erstellen einer Besprechung oder eines Termins als Stellvertreter</span><span class="sxs-lookup"><span data-stu-id="6b9c9-113">Create a meeting or appointment as a delegate</span></span>  <br/> |<span data-ttu-id="6b9c9-114">[Appointment.Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) , in dem der Parameter [FolderId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) [expliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) auf den Postfachbesitzer Kalenderordner enthält</span><span class="sxs-lookup"><span data-stu-id="6b9c9-114">[Appointment.Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) where the [FolderId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Calendar folder</span></span>  <br/> |<span data-ttu-id="6b9c9-115">[CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) , in dem das [Postfach](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) -Element gibt an, die [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) des Postfachbesitzers</span><span class="sxs-lookup"><span data-stu-id="6b9c9-115">[CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) where the [Mailbox](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element specifies the [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) of the mailbox owner</span></span>  <br/> |
|<span data-ttu-id="6b9c9-116">Erstellen Sie mehrerer Besprechungen oder Termine als Stellvertreter</span><span class="sxs-lookup"><span data-stu-id="6b9c9-116">Create multiple meetings or appointments as a delegate</span></span>  <br/> |<span data-ttu-id="6b9c9-117">[ExchangeService.CreateItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) , in dem der Parameter **FolderId** [expliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) auf den Postfachbesitzer Kalenderordner enthält</span><span class="sxs-lookup"><span data-stu-id="6b9c9-117">[ExchangeService.CreateItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) where the **FolderId** parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Calendar folder</span></span>  <br/> |<span data-ttu-id="6b9c9-118">[CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) , in dem das [Postfach](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) -Element gibt an, die [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) des Postfachbesitzers</span><span class="sxs-lookup"><span data-stu-id="6b9c9-118">[CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) where the [Mailbox](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element specifies the [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) of the mailbox owner</span></span>  <br/> |
|<span data-ttu-id="6b9c9-119">Suchen Sie nach oder suchen Sie nach eines Termins oder einer Besprechung als Stellvertreter</span><span class="sxs-lookup"><span data-stu-id="6b9c9-119">Search for or find an appointment or meeting as a delegate</span></span>  <br/> |<span data-ttu-id="6b9c9-120">[ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) , in dem der Parameter **FolderId** [expliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) auf den Postfachbesitzer Kalenderordner enthält</span><span class="sxs-lookup"><span data-stu-id="6b9c9-120">[ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) where the **FolderId** parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Calendar folder</span></span>  <br/> |<span data-ttu-id="6b9c9-121">[FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) , in dem das [Postfach](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) -Element gibt an, die [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) des Postfachbesitzers</span><span class="sxs-lookup"><span data-stu-id="6b9c9-121">[FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) where the [Mailbox](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element specifies the [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) of the mailbox owner</span></span>  <br/> |
|<span data-ttu-id="6b9c9-122">Abrufen eines Termins oder einer Besprechung als Stellvertreter</span><span class="sxs-lookup"><span data-stu-id="6b9c9-122">Get an appointment or meeting as a delegate</span></span>  <br/> |[<span data-ttu-id="6b9c9-123">Appointment.Bind</span><span class="sxs-lookup"><span data-stu-id="6b9c9-123">Appointment.Bind</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="6b9c9-124">GetItem</span><span class="sxs-lookup"><span data-stu-id="6b9c9-124">GetItem</span></span>](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="6b9c9-125">Aktualisieren eines Termins oder einer Besprechung als Stellvertreter</span><span class="sxs-lookup"><span data-stu-id="6b9c9-125">Update an appointment or meeting as a delegate</span></span>  <br/> |<span data-ttu-id="6b9c9-126">[Appointment.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) gefolgt von [Appointment.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6b9c9-126">[Appointment.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) followed by [Appointment.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx)</span></span> <br/> |<span data-ttu-id="6b9c9-127">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) gefolgt von [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6b9c9-127">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span></span> <br/> |
|<span data-ttu-id="6b9c9-128">Löschen eines Termins oder einer Besprechung als Stellvertreter</span><span class="sxs-lookup"><span data-stu-id="6b9c9-128">Delete an appointment or meeting as a delegate</span></span>  <br/> |<span data-ttu-id="6b9c9-129">[Appointment.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) gefolgt von [Appointment.Delete](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6b9c9-129">[Appointment.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) followed by [Appointment.Delete](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx)</span></span> <br/> |<span data-ttu-id="6b9c9-130">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) gefolgt von [DeleteItem](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6b9c9-130">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [DeleteItem](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx)</span></span> <br/> |
   
> [!NOTE]
> <span data-ttu-id="6b9c9-131">In den Codebeispielen in diesem Artikel ist primary@contoso.com der Postfachbesitzer.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-131">In the code examples in this article, primary@contoso.com is the mailbox owner.</span></span> 
  
## <a name="prerequisite-tasks"></a><span data-ttu-id="6b9c9-132">Erforderliche Aufgaben</span><span class="sxs-lookup"><span data-stu-id="6b9c9-132">Prerequisite tasks</span></span>
<span data-ttu-id="6b9c9-133"><a name="bk_prereq"> </a></span><span class="sxs-lookup"><span data-stu-id="6b9c9-133"></span></span>

<span data-ttu-id="6b9c9-134">Bevor ein Benutzer eine Postfachbesitzer Kalenderordner als Stellvertreter zugreifen kann, muss der Benutzer des Postfachbesitzers Kalenderordner [als Stellvertreter mit Berechtigungen hinzugefügt](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md) .</span><span class="sxs-lookup"><span data-stu-id="6b9c9-134">Before a user can access a mailbox owner's Calendar folder as a delegate, the user must be [added as a delegate with permissions](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md) to the mailbox owner's Calendar folder.</span></span> 
  
<span data-ttu-id="6b9c9-135">Eine Stellvertretung muss mit einem Postfach verbunden, ihr Konto so aktualisieren Sie den Kalender des Postfachbesitzers haben.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-135">A delegate must have a mailbox attached to their account to update the calendar of a mailbox owner.</span></span>
  
<span data-ttu-id="6b9c9-136">Wenn eine Stellvertretung Besprechungsanfragen und-Antworten entwickelt muss nur, können fügen Sie die Stellvertretung in den Ordner Kalender, und Verwenden der Standardwert [MeetingRequestsDeliveryScope.DelegatesAndSendInformationToMe](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.meetingrequestsdeliveryscope%28v=exchg.80%29.aspx) EWS Managed API-Enumeration oder die [ DeliverMeetingRequests](http://msdn.microsoft.com/library/04b999af-0b27-4e6d-a8b1-400955a1afaa%28Office.15%29.aspx) EWS-Elementwert des **DelegatesAndSendInformationToMe** für die Anfragen an die Stellvertreter und informative Nachrichten an den Postfachbesitzer.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-136">If a delegate needs to work with meeting requests and responses only, you can add the delegate to the Calendar folder, and use the default [MeetingRequestsDeliveryScope.DelegatesAndSendInformationToMe](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.meetingrequestsdeliveryscope%28v=exchg.80%29.aspx) EWS Managed API enumeration value or the [DeliverMeetingRequests](http://msdn.microsoft.com/library/04b999af-0b27-4e6d-a8b1-400955a1afaa%28Office.15%29.aspx) EWS element value of **DelegatesAndSendInformationToMe** to send the requests to the delegate and informational messages to the mailbox owner.</span></span> <span data-ttu-id="6b9c9-137">Die Stellvertretung muss an den Postfachbesitzer Posteingangsordner Zugriff gewährt werden dann nicht.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-137">The delegate then does not need to be given access to the mailbox owner's Inbox folder.</span></span> 
  
## <a name="create-a-meeting-or-appointment-as-a-delegate-by-using-the-ews-managed-api"></a><span data-ttu-id="6b9c9-138">Erstellen einer Besprechung oder eines Termins als Stellvertretung mithilfe der EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="6b9c9-138">Create a meeting or appointment as a delegate by using the EWS Managed API</span></span>
<span data-ttu-id="6b9c9-139"><a name="bk_createewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="6b9c9-139"></span></span>

<span data-ttu-id="6b9c9-140">Die EWS Managed API können Sie das Objekt für den Benutzer Delegaten verwenden, um Elemente im Kalender für den Besitzer des Postfachs zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-140">The EWS Managed API enables you to use the service object for the delegate user to create calendar items for the mailbox owner.</span></span> <span data-ttu-id="6b9c9-141">In diesem Beispiel wird veranschaulicht, wie mit der [Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) -Methode erstellen Sie eine Besprechung und Besprechungsanfragen an die Teilnehmer senden.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-141">This example shows how to use the [Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) method to create a meeting and send meeting requests to the attendees.</span></span> 
  
<span data-ttu-id="6b9c9-142">In diesem Beispiel wird davon ausgegangen, die **Service** ist ein gültiges [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objekt für den Delegaten und, die die Stellvertretung hat die entsprechenden Berechtigungen für den Postfachbesitzer Kalenderordner gewährt wurde.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-142">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object for the delegate and that the delegate has been granted the appropriate permissions for the mailbox owner's Calendar folder.</span></span> 
  
```cs
private static void DelegateAccessCreateMeeting(ExchangeService service)
{
    Appointment meeting = new Appointment(service);
    // Set the properties on the meeting object to create the meeting.
    meeting.Subject = "Team building exercise";
    meeting.Body = "Let's learn to really work as a team and then have lunch!";
    meeting.Start = DateTime.Now.AddDays(2);
    meeting.End = meeting.Start.AddHours(4);
    meeting.Location = "Conference Room 12";
    meeting.RequiredAttendees.Add("sadie@contoso.com");
    meeting.ReminderMinutesBeforeStart = 60;
    // Save the meeting to the Calendar folder for 
    // the mailbox owner and send the meeting request.
    // This method call results in a CreateItem call to EWS.
    meeting.Save(new FolderId(WellKnownFolderName.Calendar, 
        "primary@contoso.com"), 
        SendInvitationsMode.SendToAllAndSaveCopy);
    // Verify that the meeting was created.
    Item item = Item.Bind(service, meeting.Id, new PropertySet(ItemSchema.Subject));
    Console.WriteLine("\nMeeting created: " + item.Subject + "\n");
}
```

<span data-ttu-id="6b9c9-143">Beachten Sie, dass beim Speichern des Elements Methodenaufruf [Speichern](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) des Postfachbesitzers Kalenderordner bestimmen muss.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-143">Note that when you save the item, the [Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) method call must identify the mailbox owner's Calendar folder.</span></span> <span data-ttu-id="6b9c9-144">Wenn der Postfachbesitzer Kalenderordner nicht angegeben ist, ruft die Besprechungsanfrage der Stellvertretung Kalender und nicht des Postfachbesitzers Kalenderordner gespeichert.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-144">If the mailbox owner's Calendar folder is not specified, the meeting request gets saved to the delegate's calendar and not the mailbox owner's Calendar folder.</span></span> <span data-ttu-id="6b9c9-145">Sie können im Methodenaufruf **Speichern** auf zwei Arten der Postfachbesitzer Kalenderordner einschließen.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-145">You can include the mailbox owner's Calendar folder in the **Save** method call in two ways.</span></span> <span data-ttu-id="6b9c9-146">Es wird empfohlen, dass Sie eine neue Instanz des Objekts [FolderId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) instanziieren, mithilfe der [WellKnownFolderName](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) und die SMTP-Adresse des Postfachbesitzers.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-146">We recommend that you instantiate a new instance of the [FolderId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) object by using the [WellKnownFolderName](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) and the SMTP address of the mailbox owner.</span></span> 
  
```cs
meeting.Save(new FolderId(WellKnownFolderName.Calendar,
    "primary@contoso.com"), SendInvitationsMode.SendToAllAndSaveCopy);
```

<span data-ttu-id="6b9c9-147">Sie können jedoch auch [gebunden werden](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) in den Ordner Kalender zuerst, und verwenden Sie die ID des Ordners in den Methodenaufruf **zu speichern** .</span><span class="sxs-lookup"><span data-stu-id="6b9c9-147">However, you can also [Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) to the Calendar folder first, and then use the ID of the folder in the **Save** method call.</span></span> <span data-ttu-id="6b9c9-148">Beachten Sie jedoch, dass dieser einen zusätzlichen EWS-Aufruf erstellt.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-148">Be aware, however, that this creates an extra EWS call.</span></span> 
  
```cs
    // Identify the mailbox owner's SMTP address
    // and bind to their Calendar folder.
    Mailbox primary = new Mailbox("primary@contoso.com"); 
    Folder primaryCalendar = Folder.Bind(service, 
        new FolderId(WellKnownFolderName.Calendar, primary)); 
…
    // Save the meeting to the Calendar folder for the mailbox owner and send the meeting request.
    meeting.Save(primaryCalendar.Id, 
        SendInvitationsMode.SendToAllAndSaveCopy);
```

## <a name="create-a-meeting-or-appointment-as-a-delegate-by-using-ews"></a><span data-ttu-id="6b9c9-149">Erstellen einer Besprechung oder eines Termins als Stellvertretung mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="6b9c9-149">Create a meeting or appointment as a delegate by using EWS</span></span>
<span data-ttu-id="6b9c9-150"><a name="bk_createews"> </a></span><span class="sxs-lookup"><span data-stu-id="6b9c9-150"></span></span>

<span data-ttu-id="6b9c9-151">Exchange-Webdienste können Sie das Objekt für den Benutzer Delegaten verwenden, um Elemente im Kalender für den Besitzer des Postfachs zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-151">EWS enables you to use the service object for the delegate user to create calendar items for the mailbox owner.</span></span> <span data-ttu-id="6b9c9-152">In diesem Beispiel wird gezeigt, wie mithilfe den [CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) -Vorgang erstellen Sie eine Besprechung und Besprechungsanfragen an die Teilnehmer senden.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-152">This example shows how to use the [CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) operation to create a meeting and send meeting requests to the attendees.</span></span> 
  
<span data-ttu-id="6b9c9-153">Dies ist auch die XML-Anfrage, die die EWS Managed API sendet, wenn Sie die **Speichern** -Methode zum [Erstellen einer Besprechung oder eines Termins als Stellvertreter](#bk_createewsma)verwenden.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-153">This is also the XML request that the EWS Managed API sends when you use the **Save** method to [create a meeting or appointment as a delegate](#bk_createewsma).</span></span>
  
<span data-ttu-id="6b9c9-154">SOAP-Header wurde aus dem folgenden Beispiel aus Platzgründen entfernt.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-154">The SOAP header has been removed from the following example for brevity.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
         xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
         xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
…
  <soap:Body>
    <m:CreateItem SendMeetingInvitations="SendToAllAndSaveCopy">
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="calendar">
          <t:Mailbox>
            <t:EmailAddress>primary@contoso.com</t:EmailAddress>
          </t:Mailbox>
        </t:DistinguishedFolderId>
      </m:SavedItemFolderId>
      <m:Items>
        <t:CalendarItem>
          <t:Subject>Team building exercise</t:Subject>
          <t:Body BodyType="HTML">Let's learn to really work as a 
              team and then have lunch!</t:Body>
          <t:ReminderMinutesBeforeStart>60</t:ReminderMinutesBeforeStart>
          <t:Start>2014-03-09T23:26:33.756-05:00</t:Start>
          <t:End>2014-03-10T03:26:33.756-05:00</t:End>
          <t:Location>Conference Room 12</t:Location>
          <t:RequiredAttendees>
            <t:Attendee>
              <t:Mailbox>
                <t:EmailAddress>sadie@contoso.com</t:EmailAddress>
              </t:Mailbox>
            </t:Attendee>
          </t:RequiredAttendees>
        </t:CalendarItem>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="6b9c9-155">Der Server antwortet auf die **CreateItem** -Anforderung mit einer [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) -Nachricht, die enthält den Elementwert [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **noError zurück**, der angibt, dass die Besprechung erfolgreich erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-155">The server responds to the **CreateItem** request with a [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the meeting was created successfully.</span></span> <span data-ttu-id="6b9c9-156">Die Antwort enthält auch die Element-ID der neu erstellten Besprechung.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-156">The response also contains the item ID of the newly created meeting.</span></span>
  
## <a name="search-for-a-meeting-or-appointment-as-a-delegate-by-using-the-ews-managed-api"></a><span data-ttu-id="6b9c9-157">Suchen Sie nach einer Besprechung oder eines Termins als Stellvertretung mithilfe der EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="6b9c9-157">Search for a meeting or appointment as a delegate by using the EWS Managed API</span></span>
<span data-ttu-id="6b9c9-158"><a name="bk_searchewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="6b9c9-158"></span></span>

<span data-ttu-id="6b9c9-159">Um für eine Besprechung zu suchen, müssen Sie eine der Methoden, die einen [FolderId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) -Parameter enthält [ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) verwenden, damit Sie den Postfachbesitzer Kalenderordner angeben können.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-159">To search for a meeting, you must use one of the [ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) methods that includes a [FolderId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) parameter, so that you can specify the mailbox owner's Calendar folder.</span></span> 
  
```cs
static void DelegateAccessSearchWithFilter
    (ExchangeService service, SearchFilter filter)
{
    // Limit the result set to 10 items.
    ItemView view = new ItemView(10);
    view.PropertySet = new PropertySet(ItemSchema.Subject,
                                       ItemSchema.DateTimeReceived,
                                       EmailMessageSchema.IsRead);
    // Item searches do not support deep traversal.
    view.Traversal = ItemTraversal.Shallow;
    // Define the sort order.
    view.OrderBy.Add(ItemSchema.DateTimeReceived, SortDirection.Descending);
    try
    {
        // Call FindItems to find matching calendar items. 
        // The FindItems parameters must denote the mailbox owner,
        // mailbox, and Calendar folder.
        // This method call results in a FindItem call to EWS.
        FindItemsResults<Item> results = service.FindItems(
        new FolderId(WellKnownFolderName.Calendar, 
            "primary@contoso.com"), 
            filter, 
            view);
        foreach (Item item in results.Items)
        {
            Console.WriteLine("Subject: {0}", item.Subject);
            Console.WriteLine("Id: {0}", item.Id.ToString());
        }
    }
    catch (Exception ex)
    {
        Console.WriteLine("Exception while 
            enumerating results: {0}", ex.Message);
    }
}
```

<span data-ttu-id="6b9c9-160">Nachdem der Anruf **FindItems** eine Antwort mit einer ID zurückgegeben wurde, können erhalten möchten, aktualisiert oder gelöscht werden diese Besprechung mit der ID und [impliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_implicit) – und Sie müssen nicht die SMTP-Adresse des Postfachbesitzers angeben.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-160">After the **FindItems** call returns a response with an ID, you can get, update or delete that meeting by using the ID and [implicit access](delegate-access-and-ews-in-exchange.md#bk_implicit) — and you do not need to specify the mailbox owner's SMTP address.</span></span> 
  
## <a name="search-for-a-meeting-or-appointment-as-a-delegate-by-using-ews"></a><span data-ttu-id="6b9c9-161">Suchen Sie nach einer Besprechung oder eines Termins als Stellvertretung mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="6b9c9-161">Search for a meeting or appointment as a delegate by using EWS</span></span>
<span data-ttu-id="6b9c9-162"><a name="bk_searchews"> </a></span><span class="sxs-lookup"><span data-stu-id="6b9c9-162"></span></span>

<span data-ttu-id="6b9c9-163">EWS können Sie das Objekt für den Benutzer Delegaten verwenden, für die Suche nach Terminen und Besprechungen, die eine Reihe von Suchkriterien erfüllen.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-163">EWS enables you to use the service object for the delegate user to search for appointments and meetings that meet a set of search criteria.</span></span> <span data-ttu-id="6b9c9-164">In diesem Beispiel wird veranschaulicht, wie mit den Vorgang [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) finden Besprechungen in der Postfachbesitzer Kalenderordner, die das Wort "building" im Betreff enthalten.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-164">This example shows how to use the [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) operation to find meetings in the mailbox owner's Calendar folder that contain the word "building" in the subject.</span></span> 
  
<span data-ttu-id="6b9c9-165">Dies ist auch die XML-Anfrage, die die EWS Managed API sendet, wenn Sie die **FindItem** -Methode für die [Suche nach einer Besprechung oder eines Termins als Stellvertreter](#bk_searchewsma)verwenden.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-165">This is also the XML request that the EWS Managed API sends when you use the **FindItem** method to [search for a meeting or appointment as a delegate](#bk_searchewsma).</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:FindItem Traversal="Shallow">
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
          <t:FieldURI FieldURI="item:DateTimeReceived" />
          <t:FieldURI FieldURI="message:IsRead" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:IndexedPageItemView MaxEntriesReturned="10"
                             Offset="0"
                             BasePoint="Beginning" />
      <m:Restriction>
        <t:Contains ContainmentMode="Substring"
                    ContainmentComparison="IgnoreCase">
          <t:FieldURI FieldURI="item:Subject" />
          <t:Constant Value="building" />
        </t:Contains>
      </m:Restriction>
      <m:SortOrder>
        <t:FieldOrder Order="Descending">
          <t:FieldURI FieldURI="item:DateTimeReceived" />
        </t:FieldOrder>
      </m:SortOrder>
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="calendar">
          <t:Mailbox>
            <t:EmailAddress>primary@contoso.com</t:EmailAddress>
          </t:Mailbox>
        </t:DistinguishedFolderId>
      </m:ParentFolderIds>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="6b9c9-166">Der Server antwortet auf die Anforderung **FindItem** mit einer [FindItemResponse](http://msdn.microsoft.com/library/c8b316df-d4ab-49b8-96d4-8e9a016730ef%28Office.15%29.aspx) -Nachricht, die enthält den Wert [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) Element **noError zurück**, das anzeigt, dass die Suche erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-166">The server responds to the **FindItem** request with a [FindItemResponse](http://msdn.microsoft.com/library/c8b316df-d4ab-49b8-96d4-8e9a016730ef%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the search completed successfully.</span></span> <span data-ttu-id="6b9c9-167">Die Antwort enthält eine [CalendarItem](http://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) für Termine oder Besprechungen, die die Suchkriterien erfüllen.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-167">The response contains a [CalendarItem](http://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) for any appointments or meetings that met the search criteria.</span></span> <span data-ttu-id="6b9c9-168">In diesem Fall wird nur eine Besprechung gefunden.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-168">In this case, only one meeting is found.</span></span> 
  
<span data-ttu-id="6b9c9-169">Der Wert des Elements [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) wurde zur besseren Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-169">The value of the [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) element has been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="893"
                         MinorBuildNumber="10"
                         Version="V2_10"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body>
    <m:FindItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="1"
                        TotalItemsInView="1"
                        IncludesLastItemInRange="true">
            <t:Items>
              <t:CalendarItem>
                <t:ItemId Id="IJpUAAA="
                          ChangeKey="DwAAABYAAADOilbYa8KaT7ZgMoTz2P+hAAAAIKhS" />
                <t:Subject>Team building exercise</t:Subject>
                <t:DateTimeReceived>2014-03-04T21:27:22Z</t:DateTimeReceived>
              </t:CalendarItem>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="6b9c9-170">Nun, da Sie die **ItemId** für die Besprechung verfügen, die die Kriterien erfüllt, können Sie abrufen, aktualisieren oder löschen Sie diese Besprechung mithilfe des **ItemId** und [impliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_implicit) – und Sie müssen nicht die SMTP-Adresse des Postfachbesitzers angeben.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-170">Now that you have the **ItemId** for the meeting that meets your criteria, you can get, update, or delete that meeting by using the **ItemId** and [implicit access](delegate-access-and-ews-in-exchange.md#bk_implicit) — and you do not need to specify the mailbox owner's SMTP address.</span></span> 
  
## <a name="get-update-or-delete-calendar-items-as-a-delegate-by-using-the-ews-managed-api"></a><span data-ttu-id="6b9c9-171">Erhalten möchten, aktualisieren oder Löschen von Kalenderelementen (engl.) als Stellvertretung mithilfe der EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="6b9c9-171">Get, update, or delete calendar items as a delegate by using the EWS Managed API</span></span>
<span data-ttu-id="6b9c9-172"><a name="bk_geteswma"> </a></span><span class="sxs-lookup"><span data-stu-id="6b9c9-172"></span></span>

<span data-ttu-id="6b9c9-173">Die EWS Managed API können Sie abrufen, aktualisieren oder Löschen einer Besprechung oder eines Termins in die gleiche Weise, die Sie diese Aktionen ausführen, wenn Sie Stellvertretungszugriff nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-173">You can use the EWS Managed API to get, update, or delete a meeting or appointment in the same way that you perform these actions when you're not using delegate access.</span></span> <span data-ttu-id="6b9c9-174">Der einzige Unterschied ist, dass das Objekt für den Benutzer Delegat ist.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-174">The only difference is that the service object is for the delegate user.</span></span> <span data-ttu-id="6b9c9-175">Die Element-ID im Methodenaufruf **binden** enthalten sind, eindeutig identifiziert das Element im Postfachspeicher im Kalenderordner des Postfachbesitzers.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-175">The item ID included in the **Bind** method call uniquely identifies the item in the mailbox store, in the mailbox owner's Calendar folder.</span></span> 
  
<span data-ttu-id="6b9c9-176">**In Tabelle 2. EWS Managed API-Methoden zum Arbeiten mit Termine und Besprechungen als Stellvertreter**</span><span class="sxs-lookup"><span data-stu-id="6b9c9-176">**Table 2. EWS Managed API methods for working with appointments and meetings as a delegate**</span></span>

|<span data-ttu-id="6b9c9-177">**Aufgabe**</span><span class="sxs-lookup"><span data-stu-id="6b9c9-177">**Task**</span></span>|<span data-ttu-id="6b9c9-178">**EWS Managed API-Methode**</span><span class="sxs-lookup"><span data-stu-id="6b9c9-178">**EWS Managed API method**</span></span>|<span data-ttu-id="6b9c9-179">**Codebeispiel**</span><span class="sxs-lookup"><span data-stu-id="6b9c9-179">**Code example**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6b9c9-180">Abrufen eines Termins oder einer Besprechung</span><span class="sxs-lookup"><span data-stu-id="6b9c9-180">Get an appointment or meeting</span></span>  <br/> |[<span data-ttu-id="6b9c9-181">Bind</span><span class="sxs-lookup"><span data-stu-id="6b9c9-181">Bind</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="6b9c9-182">Abrufen eines Elements mithilfe der EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="6b9c9-182">Get an item by using the EWS Managed API</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getewsma) <br/> |
|<span data-ttu-id="6b9c9-183">Aktualisieren eines Termins oder einer Besprechung</span><span class="sxs-lookup"><span data-stu-id="6b9c9-183">Update an appointment or meeting</span></span>  <br/> |<span data-ttu-id="6b9c9-184">[Binden von](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) gefolgt von [Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6b9c9-184">[Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) followed by [Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx)</span></span> <br/> |[<span data-ttu-id="6b9c9-185">Aktualisieren einer Besprechung mithilfe der EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="6b9c9-185">Update a meeting by using the EWS Managed API</span></span>](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md#bk_UpdateMtgEWSMA) <br/> |
|<span data-ttu-id="6b9c9-186">Löschen eines Termins oder einer Besprechung</span><span class="sxs-lookup"><span data-stu-id="6b9c9-186">Delete an appointment or meeting</span></span>  <br/> |<span data-ttu-id="6b9c9-187">[Binden von](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) gefolgt von [Löschen](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6b9c9-187">[Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) followed by [Delete](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx)</span></span> <br/> |[<span data-ttu-id="6b9c9-188">Löschen einer Besprechung mithilfe der EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="6b9c9-188">Delete a meeting by using the EWS Managed API</span></span>](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md#bk_DeleteMtgEWSMA) <br/> |
   
## <a name="get-update-or-delete-calendar-items-as-a-delegate-by-using-ews"></a><span data-ttu-id="6b9c9-189">Erhalten möchten, aktualisieren oder Löschen von Kalenderelementen (engl.) als Stellvertretung mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="6b9c9-189">Get, update, or delete calendar items as a delegate by using EWS</span></span>
<span data-ttu-id="6b9c9-190"><a name="bk_getews"> </a></span><span class="sxs-lookup"><span data-stu-id="6b9c9-190"></span></span>

<span data-ttu-id="6b9c9-191">Exchange-Webdienste können Sie abrufen, aktualisieren oder Löschen einer Besprechung oder eines Termins in die gleiche Weise, die Sie diese Aktionen ausführen, wenn Sie Stellvertretungszugriff nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-191">You can use EWS to get, update, or delete a meeting or appointment in the same way that you perform these actions when you're not using delegate access.</span></span> <span data-ttu-id="6b9c9-192">Der einzige Unterschied ist, dass das Objekt für den Benutzer Delegat ist.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-192">The only difference is that the service object is for the delegate user.</span></span> <span data-ttu-id="6b9c9-193">Die Element-ID eindeutig enthalten in den Aufruf [GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) -Methode identifiziert das Element im Postfachspeicher im Kalenderordner des Postfachbesitzers.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-193">The item ID included in the [GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) method call uniquely identifies the item in the mailbox store, in the mailbox owner's Calendar folder.</span></span> 
  
<span data-ttu-id="6b9c9-194">**Tabelle 3. EWS-Vorgänge für die Arbeit mit Termine und Besprechungen als Stellvertreter**</span><span class="sxs-lookup"><span data-stu-id="6b9c9-194">**Table 3. EWS operations for working with appointments and meetings as a delegate**</span></span>

|<span data-ttu-id="6b9c9-195">**Aufgabe**</span><span class="sxs-lookup"><span data-stu-id="6b9c9-195">**Task**</span></span>|<span data-ttu-id="6b9c9-196">**EWS-Vorgang**</span><span class="sxs-lookup"><span data-stu-id="6b9c9-196">**EWS operation**</span></span>|<span data-ttu-id="6b9c9-197">**Codebeispiel**</span><span class="sxs-lookup"><span data-stu-id="6b9c9-197">**Code example**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6b9c9-198">Abrufen eines Termins oder einer Besprechung</span><span class="sxs-lookup"><span data-stu-id="6b9c9-198">Get an appointment or meeting</span></span>  <br/> |[<span data-ttu-id="6b9c9-199">GetItem</span><span class="sxs-lookup"><span data-stu-id="6b9c9-199">GetItem</span></span>](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |[<span data-ttu-id="6b9c9-200">Abrufen eines Elements mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="6b9c9-200">Get an item by using EWS</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getews) <br/> |
|<span data-ttu-id="6b9c9-201">Aktualisieren eines Termins oder einer Besprechung</span><span class="sxs-lookup"><span data-stu-id="6b9c9-201">Update an appointment or meeting</span></span>  <br/> |<span data-ttu-id="6b9c9-202">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) gefolgt von [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6b9c9-202">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span></span> <br/> |[<span data-ttu-id="6b9c9-203">Aktualisieren einer Besprechung mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="6b9c9-203">Update a meeting by using EWS</span></span>](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md#bk_UpdateMtgEWS) <br/> |
|<span data-ttu-id="6b9c9-204">Löschen eines Termins oder einer Besprechung</span><span class="sxs-lookup"><span data-stu-id="6b9c9-204">Delete an appointment or meeting</span></span>  <br/> |<span data-ttu-id="6b9c9-205">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) gefolgt von [DeleteItem](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6b9c9-205">[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [DeleteItem](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx)</span></span> <br/> |[](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md#bk_DeleteMtgEWSMA) <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6b9c9-206">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6b9c9-206">See also</span></span>

- [<span data-ttu-id="6b9c9-207">Stellvertretungszugriff und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="6b9c9-207">Delegate access and EWS in Exchange</span></span>](delegate-access-and-ews-in-exchange.md)   
- [<span data-ttu-id="6b9c9-208">Hinzufügen und Entfernen von Stellvertretungen mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="6b9c9-208">Add and remove delegates by using EWS in Exchange</span></span>](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md)
- [<span data-ttu-id="6b9c9-209">Legen Sie Berechtigungen für einen anderen Benutzer mithilfe der EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="6b9c9-209">Set folder permissions for another user by using EWS in Exchange</span></span>](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md) 
- [<span data-ttu-id="6b9c9-210">Kalender und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="6b9c9-210">Calendars and EWS in Exchange</span></span>](calendars-and-ews-in-exchange.md)
    

