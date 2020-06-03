---
title: Zugriff auf einen Kalender als Delegat mithilfe der EWS in Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.assetid: d7db4a1e-9ed6-41da-8529-a73ca285cdf2
description: Erfahren Sie, wie Sie mithilfe der verwaltete EWS-API oder EWS in Exchange auf einen Kalender als Stellvertreter zugreifen.
localization_priority: Priority
ms.openlocfilehash: 20ec294ddc4ccf014f0b2148c786c8c3ef8a6069
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528293"
---
#  <a name="access-a-calendar-as-a-delegate-by-using-ews-in-exchange"></a><span data-ttu-id="ca19c-103">Zugriff auf einen Kalender als Delegat mithilfe der EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="ca19c-103">Access a calendar as a delegate by using EWS in Exchange</span></span>

<span data-ttu-id="ca19c-104">Erfahren Sie, wie Sie mithilfe der verwaltete EWS-API oder EWS in Exchange auf einen Kalender als Stellvertreter zugreifen.</span><span class="sxs-lookup"><span data-stu-id="ca19c-104">Learn how to access a calendar as a delegate by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="ca19c-105">Sie können die verwaltete EWS-API oder EWS verwenden, um einem Benutzer Stellvertretungszugriff auf den Kalenderordner eines Postfachbesitzers zu gewähren.</span><span class="sxs-lookup"><span data-stu-id="ca19c-105">You can use the EWS Managed API or EWS to give a user delegate access to a mailbox owner's Calendar folder.</span></span> <span data-ttu-id="ca19c-106">Der Stellvertreter kann dann Besprechungsanfragen im Auftrag des Postfachbesitzers erstellen, Termine erstellen, Besprechungsanfragen beantworten sowie Besprechungen aus dem Kalenderordner des Postfachbesitzers abhängig von ihren Berechtigungen abrufen, aktualisieren und löschen.</span><span class="sxs-lookup"><span data-stu-id="ca19c-106">The delegate can then create meeting requests on behalf of the mailbox owner, create appointments, respond to meeting requests, and retrieve, update, and delete meetings from the mailbox owner's Calendar folder, depending on their permissions.</span></span>
  
<span data-ttu-id="ca19c-107">Als Stellvertretung verwenden Sie dieselben Methoden und Vorgänge für den Zugriff auf den Kalenderordner eines Postfachbesitzers, den Sie für den Zugriff auf Ihren eigenen Kalenderordner verwenden.</span><span class="sxs-lookup"><span data-stu-id="ca19c-107">As a delegate, you use the same methods and operations to access a mailbox owner's Calendar folder that you use to access your own Calendar folder.</span></span> <span data-ttu-id="ca19c-108">Der Hauptunterschied besteht darin, dass Sie [expliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_explicit) zum Suchen oder Erstellen eines Kalenderelements oder eines Kalender Unterordners verwenden müssen, und nachdem Sie die Element-ID oder Ordner-ID identifiziert haben, können Sie den [impliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_implicit) zum Abrufen, aktualisieren oder Löschen des Elements verwenden.</span><span class="sxs-lookup"><span data-stu-id="ca19c-108">The main difference is that you have to use [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicit) to find or create a calendar item or calendar subfolder, and then after you identify the item ID or folder ID, you can use [implicit access](delegate-access-and-ews-in-exchange.md#bk_implicit) to get, update, or delete the item.</span></span> 
  
<span data-ttu-id="ca19c-109">**Tabelle 1. Verwaltete EWS-API Methoden und EWS-Vorgänge für den Zugriff auf einen Kalender als Stellvertretung**</span><span class="sxs-lookup"><span data-stu-id="ca19c-109">**Table 1. EWS Managed API methods and EWS operations for accessing a calendar as a delegate**</span></span>

|<span data-ttu-id="ca19c-110">**Aktion**</span><span class="sxs-lookup"><span data-stu-id="ca19c-110">**If you want to…**</span></span>|<span data-ttu-id="ca19c-111">**Verwenden Sie diese verwaltete EWS-API-Methode...**</span><span class="sxs-lookup"><span data-stu-id="ca19c-111">**Use this EWS Managed API method…**</span></span>|<span data-ttu-id="ca19c-112">**Verwenden Sie diesen EWS-Vorgang...**</span><span class="sxs-lookup"><span data-stu-id="ca19c-112">**Use this EWS operation…**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ca19c-113">Erstellen einer Besprechung oder eines Termins als Stellvertreter</span><span class="sxs-lookup"><span data-stu-id="ca19c-113">Create a meeting or appointment as a delegate</span></span>  <br/> |<span data-ttu-id="ca19c-114">[Termin. Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) , wobei der [Folder](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) -Parameter den [expliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) auf den Kalenderordner des Postfachbesitzers ermöglicht</span><span class="sxs-lookup"><span data-stu-id="ca19c-114">[Appointment.Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) where the [FolderId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Calendar folder</span></span>  <br/> |<span data-ttu-id="ca19c-115">[CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) , wobei das [Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) [-Element](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) die e-Mail-Post Fach Besitzerin angibt</span><span class="sxs-lookup"><span data-stu-id="ca19c-115">[CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) where the [Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element specifies the [EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) of the mailbox owner</span></span>  <br/> |
|<span data-ttu-id="ca19c-116">Erstellen mehrerer Besprechungen oder Termine als Stellvertreter</span><span class="sxs-lookup"><span data-stu-id="ca19c-116">Create multiple meetings or appointments as a delegate</span></span>  <br/> |<span data-ttu-id="ca19c-117">[Datei "ExchangeService. CreateItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) , wobei der **Folder** -Parameter den [expliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) auf den Kalenderordner des Postfachbesitzers ermöglicht</span><span class="sxs-lookup"><span data-stu-id="ca19c-117">[ExchangeService.CreateItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) where the **FolderId** parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Calendar folder</span></span>  <br/> |<span data-ttu-id="ca19c-118">[CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) , wobei das [Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) [-Element](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) die e-Mail-Post Fach Besitzerin angibt</span><span class="sxs-lookup"><span data-stu-id="ca19c-118">[CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) where the [Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element specifies the [EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) of the mailbox owner</span></span>  <br/> |
|<span data-ttu-id="ca19c-119">Suchen nach oder suchen nach einem Termin oder einer Besprechung als Stellvertreter</span><span class="sxs-lookup"><span data-stu-id="ca19c-119">Search for or find an appointment or meeting as a delegate</span></span>  <br/> |<span data-ttu-id="ca19c-120">[Datei "ExchangeService. FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) , wobei der **Folder** -Parameter den [expliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) auf den Kalenderordner des Postfachbesitzers ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="ca19c-120">[ExchangeService.FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) where the **FolderId** parameter provides [explicit access](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) to the mailbox owner's Calendar folder</span></span>  <br/> |<span data-ttu-id="ca19c-121">[FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) , wobei das [Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) [-Element](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) die e-Mail-Post Fach Besitzerin angibt</span><span class="sxs-lookup"><span data-stu-id="ca19c-121">[FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) where the [Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) element specifies the [EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) of the mailbox owner</span></span>  <br/> |
|<span data-ttu-id="ca19c-122">Abrufen eines Termins oder einer Besprechung als Stellvertreter</span><span class="sxs-lookup"><span data-stu-id="ca19c-122">Get an appointment or meeting as a delegate</span></span>  <br/> |[<span data-ttu-id="ca19c-123">Appointment.Bind</span><span class="sxs-lookup"><span data-stu-id="ca19c-123">Appointment.Bind</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="ca19c-124">GetItem</span><span class="sxs-lookup"><span data-stu-id="ca19c-124">GetItem</span></span>](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="ca19c-125">Aktualisieren eines Termins oder einer Besprechung als Stellvertreter</span><span class="sxs-lookup"><span data-stu-id="ca19c-125">Update an appointment or meeting as a delegate</span></span>  <br/> |<span data-ttu-id="ca19c-126">[Termin. Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) gefolgt von [Termin. Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ca19c-126">[Appointment.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) followed by [Appointment.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx)</span></span> <br/> |<span data-ttu-id="ca19c-127">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) , gefolgt von [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ca19c-127">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span></span> <br/> |
|<span data-ttu-id="ca19c-128">Löschen eines Termins oder einer Besprechung als Stellvertreter</span><span class="sxs-lookup"><span data-stu-id="ca19c-128">Delete an appointment or meeting as a delegate</span></span>  <br/> |<span data-ttu-id="ca19c-129">[Termin. Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) gefolgt von [Termin. Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ca19c-129">[Appointment.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) followed by [Appointment.Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx)</span></span> <br/> |<span data-ttu-id="ca19c-130">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) , gefolgt von [DeleteItem](../web-service-reference/deleteitem-operation.md)</span><span class="sxs-lookup"><span data-stu-id="ca19c-130">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [DeleteItem](../web-service-reference/deleteitem-operation.md)</span></span> <br/> |
   
> [!NOTE]
> <span data-ttu-id="ca19c-131">In den Codebeispielen in diesem Artikel ist Primary@contoso.com der Postfachbesitzer.</span><span class="sxs-lookup"><span data-stu-id="ca19c-131">In the code examples in this article, primary@contoso.com is the mailbox owner.</span></span> 
  
## <a name="prerequisite-tasks"></a><span data-ttu-id="ca19c-132">Erforderliche Aufgaben</span><span class="sxs-lookup"><span data-stu-id="ca19c-132">Prerequisite tasks</span></span>
<span data-ttu-id="ca19c-133"><a name="bk_prereq"> </a></span><span class="sxs-lookup"><span data-stu-id="ca19c-133"><a name="bk_prereq"> </a></span></span>

<span data-ttu-id="ca19c-134">Bevor ein Benutzer als Stellvertreter auf den Kalenderordner eines Postfachbesitzers zugreifen kann, muss der Benutzer [als Stellvertreter mit Berechtigungen](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md) für den Kalenderordner des Postfachbesitzers hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="ca19c-134">Before a user can access a mailbox owner's Calendar folder as a delegate, the user must be [added as a delegate with permissions](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md) to the mailbox owner's Calendar folder.</span></span> 
  
<span data-ttu-id="ca19c-135">Eine Stellvertretung muss über ein Postfach verfügen, das Ihrem Konto zugeordnet ist, um den Kalender eines Postfachbesitzers zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="ca19c-135">A delegate must have a mailbox attached to their account to update the calendar of a mailbox owner.</span></span>
  
<span data-ttu-id="ca19c-136">Wenn eine Stellvertretung nur mit Besprechungsanfragen und-Antworten arbeiten muss, können Sie die Stellvertretung dem Kalenderordner hinzufügen und den Standardwert [MeetingRequestsDeliveryScope. DelegatesAndSendInformationToMe](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.meetingrequestsdeliveryscope%28v=exchg.80%29.aspx) verwaltete EWS-API Aufzählungswert oder den [DeliverMeetingRequests](https://msdn.microsoft.com/library/04b999af-0b27-4e6d-a8b1-400955a1afaa%28Office.15%29.aspx) EWS-Elementwert von **DelegatesAndSendInformationToMe** verwenden, um die Anforderungen an die Stellvertretung und die Informationsmeldungen an den Postfachbesitzer zu senden.</span><span class="sxs-lookup"><span data-stu-id="ca19c-136">If a delegate needs to work with meeting requests and responses only, you can add the delegate to the Calendar folder, and use the default [MeetingRequestsDeliveryScope.DelegatesAndSendInformationToMe](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.meetingrequestsdeliveryscope%28v=exchg.80%29.aspx) EWS Managed API enumeration value or the [DeliverMeetingRequests](https://msdn.microsoft.com/library/04b999af-0b27-4e6d-a8b1-400955a1afaa%28Office.15%29.aspx) EWS element value of **DelegatesAndSendInformationToMe** to send the requests to the delegate and informational messages to the mailbox owner.</span></span> <span data-ttu-id="ca19c-137">Die Stellvertretung muss dann keinen Zugriff auf den Posteingang-Ordner des Postfachbesitzers erhalten.</span><span class="sxs-lookup"><span data-stu-id="ca19c-137">The delegate then does not need to be given access to the mailbox owner's Inbox folder.</span></span> 
  
## <a name="create-a-meeting-or-appointment-as-a-delegate-by-using-the-ews-managed-api"></a><span data-ttu-id="ca19c-138">Erstellen einer Besprechung oder eines Termins als Stellvertretung mithilfe der verwaltete EWS-API</span><span class="sxs-lookup"><span data-stu-id="ca19c-138">Create a meeting or appointment as a delegate by using the EWS Managed API</span></span>
<span data-ttu-id="ca19c-139"><a name="bk_createewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="ca19c-139"><a name="bk_createewsma"> </a></span></span>

<span data-ttu-id="ca19c-140">Mit dem verwaltete EWS-API können Sie das Dienstobjekt für den Stellvertreter Benutzer verwenden, um Kalenderelemente für den Postfachbesitzer zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ca19c-140">The EWS Managed API enables you to use the service object for the delegate user to create calendar items for the mailbox owner.</span></span> <span data-ttu-id="ca19c-141">In diesem Beispiel wird gezeigt, wie Sie mit der [Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) -Methode eine Besprechung erstellen und Besprechungsanfragen an die Teilnehmer senden.</span><span class="sxs-lookup"><span data-stu-id="ca19c-141">This example shows how to use the [Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) method to create a meeting and send meeting requests to the attendees.</span></span> 
  
<span data-ttu-id="ca19c-142">In diesem Beispiel wird davon ausgegangen, dass **Service** ein gültiges [Datei "ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objekt für die Stellvertretung ist und dass der Stellvertretung die entsprechenden Berechtigungen für den Kalenderordner des Postfachbesitzers erteilt wurden.</span><span class="sxs-lookup"><span data-stu-id="ca19c-142">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object for the delegate and that the delegate has been granted the appropriate permissions for the mailbox owner's Calendar folder.</span></span> 
  
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

<span data-ttu-id="ca19c-143">Beachten Sie, dass beim Speichern des Elements der Aufruf der [Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) -Methode den Kalenderordner des Postfachbesitzers identifizieren muss.</span><span class="sxs-lookup"><span data-stu-id="ca19c-143">Note that when you save the item, the [Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.save%28v=exchg.80%29.aspx) method call must identify the mailbox owner's Calendar folder.</span></span> <span data-ttu-id="ca19c-144">Wenn der Kalenderordner des Postfachbesitzers nicht angegeben ist, wird die Besprechungsanfrage im Kalender der Stellvertretung und nicht im Kalenderordner des Postfachbesitzers gespeichert.</span><span class="sxs-lookup"><span data-stu-id="ca19c-144">If the mailbox owner's Calendar folder is not specified, the meeting request gets saved to the delegate's calendar and not the mailbox owner's Calendar folder.</span></span> <span data-ttu-id="ca19c-145">Sie können den Kalenderordner des Postfachbesitzers in den **Save** -Methodenaufruf auf zwei Arten einschließen.</span><span class="sxs-lookup"><span data-stu-id="ca19c-145">You can include the mailbox owner's Calendar folder in the **Save** method call in two ways.</span></span> <span data-ttu-id="ca19c-146">Es wird empfohlen, dass Sie eine neue Instanz des [Folder](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) -Objekts mit dem [WellKnownFolderName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) und der SMTP-Adresse des Postfachbesitzers instanziieren.</span><span class="sxs-lookup"><span data-stu-id="ca19c-146">We recommend that you instantiate a new instance of the [FolderId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) object by using the [WellKnownFolderName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) and the SMTP address of the mailbox owner.</span></span> 
  
```cs
meeting.Save(new FolderId(WellKnownFolderName.Calendar,
    "primary@contoso.com"), SendInvitationsMode.SendToAllAndSaveCopy);
```

<span data-ttu-id="ca19c-147">Sie können jedoch auch zuerst eine [Bindung](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) an den Ordner Kalender durchführen und dann die ID des Ordners im Aufruf der **Save** -Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="ca19c-147">However, you can also [Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) to the Calendar folder first, and then use the ID of the folder in the **Save** method call.</span></span> <span data-ttu-id="ca19c-148">Beachten Sie jedoch, dass dadurch ein zusätzlicher EWS-Aufruf erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="ca19c-148">Be aware, however, that this creates an extra EWS call.</span></span> 
  
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

## <a name="create-a-meeting-or-appointment-as-a-delegate-by-using-ews"></a><span data-ttu-id="ca19c-149">Erstellen einer Besprechung oder eines Termins als Stellvertretung mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="ca19c-149">Create a meeting or appointment as a delegate by using EWS</span></span>
<span data-ttu-id="ca19c-150"><a name="bk_createews"> </a></span><span class="sxs-lookup"><span data-stu-id="ca19c-150"><a name="bk_createews"> </a></span></span>

<span data-ttu-id="ca19c-151">Mit EWS können Sie das Dienstobjekt für den Delegate-Benutzer verwenden, um Kalenderelemente für den Postfachbesitzer zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ca19c-151">EWS enables you to use the service object for the delegate user to create calendar items for the mailbox owner.</span></span> <span data-ttu-id="ca19c-152">In diesem Beispiel wird gezeigt, wie Sie mithilfe des [CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) -Vorgangs eine Besprechung erstellen und Besprechungsanfragen an die Teilnehmer senden.</span><span class="sxs-lookup"><span data-stu-id="ca19c-152">This example shows how to use the [CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) operation to create a meeting and send meeting requests to the attendees.</span></span> 
  
<span data-ttu-id="ca19c-153">Dies ist auch die XML-Anforderung, die von der verwaltete EWS-API gesendet wird, wenn Sie die **Save** -Methode verwenden, um [eine Besprechung oder einen Termin als Stellvertreter zu erstellen](#bk_createewsma).</span><span class="sxs-lookup"><span data-stu-id="ca19c-153">This is also the XML request that the EWS Managed API sends when you use the **Save** method to [create a meeting or appointment as a delegate](#bk_createewsma).</span></span>
  
<span data-ttu-id="ca19c-154">Der SOAP-Header wurde aus dem folgenden Beispiel aus Gründen der Kürze entfernt.</span><span class="sxs-lookup"><span data-stu-id="ca19c-154">The SOAP header has been removed from the following example for brevity.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
         xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
         xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="ca19c-155">Der Server antwortet auf die **CreateItem** -Anforderung mit einer [CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) -Nachricht, die den [Response Code](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) -Elementwert **noError**enthält, der angibt, dass die Besprechung erfolgreich erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="ca19c-155">The server responds to the **CreateItem** request with a [CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the meeting was created successfully.</span></span> <span data-ttu-id="ca19c-156">Die Antwort enthält auch die Element-ID der neu erstellten Besprechung.</span><span class="sxs-lookup"><span data-stu-id="ca19c-156">The response also contains the item ID of the newly created meeting.</span></span>
  
## <a name="search-for-a-meeting-or-appointment-as-a-delegate-by-using-the-ews-managed-api"></a><span data-ttu-id="ca19c-157">Suchen nach einer Besprechung oder einem Termin als Stellvertretung mithilfe der verwaltete EWS-API</span><span class="sxs-lookup"><span data-stu-id="ca19c-157">Search for a meeting or appointment as a delegate by using the EWS Managed API</span></span>
<span data-ttu-id="ca19c-158"><a name="bk_searchewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="ca19c-158"><a name="bk_searchewsma"> </a></span></span>

<span data-ttu-id="ca19c-159">Um nach einer Besprechung zu suchen, müssen Sie eine der [Datei "ExchangeService. FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) -Methoden verwenden, die einen [foldercode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) -Parameter enthält, sodass Sie den Kalenderordner des Postfachbesitzers angeben können.</span><span class="sxs-lookup"><span data-stu-id="ca19c-159">To search for a meeting, you must use one of the [ExchangeService.FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) methods that includes a [FolderId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) parameter, so that you can specify the mailbox owner's Calendar folder.</span></span> 
  
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

<span data-ttu-id="ca19c-160">Nachdem der **FindItems** -Aufruf eine Antwort mit einer ID zurückgibt, können Sie diese Besprechung abrufen, aktualisieren oder löschen, indem Sie die ID und den [impliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_implicit) verwenden – und Sie müssen die SMTP-Adresse des Postfachbesitzers nicht angeben.</span><span class="sxs-lookup"><span data-stu-id="ca19c-160">After the **FindItems** call returns a response with an ID, you can get, update or delete that meeting by using the ID and [implicit access](delegate-access-and-ews-in-exchange.md#bk_implicit) — and you do not need to specify the mailbox owner's SMTP address.</span></span> 
  
## <a name="search-for-a-meeting-or-appointment-as-a-delegate-by-using-ews"></a><span data-ttu-id="ca19c-161">Suchen nach einer Besprechung oder einem Termin als Stellvertretung mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="ca19c-161">Search for a meeting or appointment as a delegate by using EWS</span></span>
<span data-ttu-id="ca19c-162"><a name="bk_searchews"> </a></span><span class="sxs-lookup"><span data-stu-id="ca19c-162"><a name="bk_searchews"> </a></span></span>

<span data-ttu-id="ca19c-163">Mit EWS können Sie das Dienstobjekt für den Stellvertreter-Benutzer verwenden, um nach Terminen und Besprechungen zu suchen, die eine Reihe von Suchkriterien erfüllen.</span><span class="sxs-lookup"><span data-stu-id="ca19c-163">EWS enables you to use the service object for the delegate user to search for appointments and meetings that meet a set of search criteria.</span></span> <span data-ttu-id="ca19c-164">In diesem Beispiel wird gezeigt, wie Sie mithilfe des [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) -Vorgangs Besprechungen im Kalenderordner des Postfachbesitzers finden, der das Wort "Building" im Betreff enthält.</span><span class="sxs-lookup"><span data-stu-id="ca19c-164">This example shows how to use the [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) operation to find meetings in the mailbox owner's Calendar folder that contain the word "building" in the subject.</span></span> 
  
<span data-ttu-id="ca19c-165">Dies ist auch die XML-Anforderung, die von der verwaltete EWS-API gesendet wird, wenn Sie die **FindItem** -Methode verwenden, um [eine Besprechung oder einen Termin als Stellvertreter zu suchen](#bk_searchewsma).</span><span class="sxs-lookup"><span data-stu-id="ca19c-165">This is also the XML request that the EWS Managed API sends when you use the **FindItem** method to [search for a meeting or appointment as a delegate](#bk_searchewsma).</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="ca19c-166">Der Server antwortet auf die **FindItem** -Anforderung mit einer [FindItemResponse](https://msdn.microsoft.com/library/c8b316df-d4ab-49b8-96d4-8e9a016730ef%28Office.15%29.aspx) -Nachricht, die den [Response Code](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) -Elementwert **noError**enthält, der angibt, dass die Suche erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="ca19c-166">The server responds to the **FindItem** request with a [FindItemResponse](https://msdn.microsoft.com/library/c8b316df-d4ab-49b8-96d4-8e9a016730ef%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the search completed successfully.</span></span> <span data-ttu-id="ca19c-167">Die Antwort enthält ein [CalendarItem](https://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) für alle Termine oder Besprechungen, die die Suchkriterien erfüllen.</span><span class="sxs-lookup"><span data-stu-id="ca19c-167">The response contains a [CalendarItem](https://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) for any appointments or meetings that met the search criteria.</span></span> <span data-ttu-id="ca19c-168">In diesem Fall wird nur eine Besprechung gefunden.</span><span class="sxs-lookup"><span data-stu-id="ca19c-168">In this case, only one meeting is found.</span></span> 
  
<span data-ttu-id="ca19c-169">Der Wert des [ItemID](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) -Elements wurde zur Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="ca19c-169">The value of the [ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) element has been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="893"
                         MinorBuildNumber="10"
                         Version="V2_10"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body>
    <m:FindItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="ca19c-170">Nachdem Sie nun die **ItemID** für die Besprechung haben, die Ihre Kriterien erfüllt, können Sie diese Besprechung mit dem **ItemID** -und [impliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_implicit) abrufen, aktualisieren oder löschen, und Sie müssen die SMTP-Adresse des Postfachbesitzers nicht angeben.</span><span class="sxs-lookup"><span data-stu-id="ca19c-170">Now that you have the **ItemId** for the meeting that meets your criteria, you can get, update, or delete that meeting by using the **ItemId** and [implicit access](delegate-access-and-ews-in-exchange.md#bk_implicit) — and you do not need to specify the mailbox owner's SMTP address.</span></span> 
  
## <a name="get-update-or-delete-calendar-items-as-a-delegate-by-using-the-ews-managed-api"></a><span data-ttu-id="ca19c-171">Abrufen, aktualisieren oder Löschen von Kalenderelementen als Stellvertretung mithilfe der verwaltete EWS-API</span><span class="sxs-lookup"><span data-stu-id="ca19c-171">Get, update, or delete calendar items as a delegate by using the EWS Managed API</span></span>
<span data-ttu-id="ca19c-172"><a name="bk_geteswma"> </a></span><span class="sxs-lookup"><span data-stu-id="ca19c-172"><a name="bk_geteswma"> </a></span></span>

<span data-ttu-id="ca19c-173">Sie können die verwaltete EWS-API verwenden, um eine Besprechung oder einen Termin auf die gleiche Weise abzurufen, zu aktualisieren oder zu löschen, wie Sie diese Aktionen ausführen, wenn Sie keinen Stellvertretungszugriff verwenden.</span><span class="sxs-lookup"><span data-stu-id="ca19c-173">You can use the EWS Managed API to get, update, or delete a meeting or appointment in the same way that you perform these actions when you're not using delegate access.</span></span> <span data-ttu-id="ca19c-174">Der einzige Unterschied besteht darin, dass das Dienstobjekt für den Stellvertreter Benutzer ist.</span><span class="sxs-lookup"><span data-stu-id="ca19c-174">The only difference is that the service object is for the delegate user.</span></span> <span data-ttu-id="ca19c-175">Die im **Bindungs** Methodenaufruf enthaltene Element-ID identifiziert das Element im Postfachspeicher im Kalenderordner des Postfachbesitzers eindeutig.</span><span class="sxs-lookup"><span data-stu-id="ca19c-175">The item ID included in the **Bind** method call uniquely identifies the item in the mailbox store, in the mailbox owner's Calendar folder.</span></span> 
  
<span data-ttu-id="ca19c-176">**Tabelle 2. Verwaltete EWS-API Methoden zum Arbeiten mit Terminen und Besprechungen als Stellvertretung**</span><span class="sxs-lookup"><span data-stu-id="ca19c-176">**Table 2. EWS Managed API methods for working with appointments and meetings as a delegate**</span></span>

|<span data-ttu-id="ca19c-177">**Aufgabe**</span><span class="sxs-lookup"><span data-stu-id="ca19c-177">**Task**</span></span>|<span data-ttu-id="ca19c-178">**EWS Managed API-Methode**</span><span class="sxs-lookup"><span data-stu-id="ca19c-178">**EWS Managed API method**</span></span>|<span data-ttu-id="ca19c-179">**Codebeispiel**</span><span class="sxs-lookup"><span data-stu-id="ca19c-179">**Code example**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ca19c-180">Abrufen eines Termins oder einer Besprechung</span><span class="sxs-lookup"><span data-stu-id="ca19c-180">Get an appointment or meeting</span></span>  <br/> |[<span data-ttu-id="ca19c-181">Bind</span><span class="sxs-lookup"><span data-stu-id="ca19c-181">Bind</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="ca19c-182">Abrufen eines Elements mithilfe der verwaltete EWS-API</span><span class="sxs-lookup"><span data-stu-id="ca19c-182">Get an item by using the EWS Managed API</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getewsma) <br/> |
|<span data-ttu-id="ca19c-183">Aktualisieren eines Termins oder einer Besprechung</span><span class="sxs-lookup"><span data-stu-id="ca19c-183">Update an appointment or meeting</span></span>  <br/> |<span data-ttu-id="ca19c-184">[Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) gefolgt von [Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ca19c-184">[Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) followed by [Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx)</span></span> <br/> |[<span data-ttu-id="ca19c-185">Aktualisieren einer Besprechung mithilfe der verwaltete EWS-API</span><span class="sxs-lookup"><span data-stu-id="ca19c-185">Update a meeting by using the EWS Managed API</span></span>](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md#bk_UpdateMtgEWSMA) <br/> |
|<span data-ttu-id="ca19c-186">Löschen eines Termins oder einer Besprechung</span><span class="sxs-lookup"><span data-stu-id="ca19c-186">Delete an appointment or meeting</span></span>  <br/> |<span data-ttu-id="ca19c-187">[Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) gefolgt von [Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ca19c-187">[Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.bind%28v=exchg.80%29.aspx) followed by [Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.delete%28v=exchg.80%29.aspx)</span></span> <br/> |[<span data-ttu-id="ca19c-188">Löschen einer Besprechung mithilfe der verwaltete EWS-API</span><span class="sxs-lookup"><span data-stu-id="ca19c-188">Delete a meeting by using the EWS Managed API</span></span>](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md#bk_DeleteMtgEWSMA) <br/> |
   
## <a name="get-update-or-delete-calendar-items-as-a-delegate-by-using-ews"></a><span data-ttu-id="ca19c-189">Abrufen, aktualisieren oder Löschen von Kalenderelementen als Stellvertretung mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="ca19c-189">Get, update, or delete calendar items as a delegate by using EWS</span></span>
<span data-ttu-id="ca19c-190"><a name="bk_getews"> </a></span><span class="sxs-lookup"><span data-stu-id="ca19c-190"><a name="bk_getews"> </a></span></span>

<span data-ttu-id="ca19c-191">Sie können EWS verwenden, um eine Besprechung oder einen Termin auf die gleiche Weise abzurufen, zu aktualisieren oder zu löschen, wie Sie diese Aktionen ausführen, wenn Sie keinen Stellvertretungszugriff verwenden.</span><span class="sxs-lookup"><span data-stu-id="ca19c-191">You can use EWS to get, update, or delete a meeting or appointment in the same way that you perform these actions when you're not using delegate access.</span></span> <span data-ttu-id="ca19c-192">Der einzige Unterschied besteht darin, dass das Dienstobjekt für den Stellvertreter Benutzer ist.</span><span class="sxs-lookup"><span data-stu-id="ca19c-192">The only difference is that the service object is for the delegate user.</span></span> <span data-ttu-id="ca19c-193">Die Element-ID, die im [GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) -Methodenaufruf enthalten ist, identifiziert das Element im Postfachspeicher im Kalenderordner des Postfachbesitzers eindeutig.</span><span class="sxs-lookup"><span data-stu-id="ca19c-193">The item ID included in the [GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) method call uniquely identifies the item in the mailbox store, in the mailbox owner's Calendar folder.</span></span> 
  
<span data-ttu-id="ca19c-194">**Tabelle 3. EWS-Vorgänge für das Arbeiten mit Terminen und Besprechungen als Stellvertretung**</span><span class="sxs-lookup"><span data-stu-id="ca19c-194">**Table 3. EWS operations for working with appointments and meetings as a delegate**</span></span>

|<span data-ttu-id="ca19c-195">**Aufgabe**</span><span class="sxs-lookup"><span data-stu-id="ca19c-195">**Task**</span></span>|<span data-ttu-id="ca19c-196">**EWS-Funktion**</span><span class="sxs-lookup"><span data-stu-id="ca19c-196">**EWS operation**</span></span>|<span data-ttu-id="ca19c-197">**Codebeispiel**</span><span class="sxs-lookup"><span data-stu-id="ca19c-197">**Code example**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ca19c-198">Abrufen eines Termins oder einer Besprechung</span><span class="sxs-lookup"><span data-stu-id="ca19c-198">Get an appointment or meeting</span></span>  <br/> |[<span data-ttu-id="ca19c-199">GetItem</span><span class="sxs-lookup"><span data-stu-id="ca19c-199">GetItem</span></span>](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |[<span data-ttu-id="ca19c-200">Abrufen eines Elements mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="ca19c-200">Get an item by using EWS</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getews) <br/> |
|<span data-ttu-id="ca19c-201">Aktualisieren eines Termins oder einer Besprechung</span><span class="sxs-lookup"><span data-stu-id="ca19c-201">Update an appointment or meeting</span></span>  <br/> |<span data-ttu-id="ca19c-202">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) , gefolgt von [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ca19c-202">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx)</span></span> <br/> |[<span data-ttu-id="ca19c-203">Aktualisieren einer Besprechung mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="ca19c-203">Update a meeting by using EWS</span></span>](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md#bk_UpdateMtgEWS) <br/> |
|<span data-ttu-id="ca19c-204">Löschen eines Termins oder einer Besprechung</span><span class="sxs-lookup"><span data-stu-id="ca19c-204">Delete an appointment or meeting</span></span>  <br/> |<span data-ttu-id="ca19c-205">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) , gefolgt von [DeleteItem](../web-service-reference/deleteitem-operation.md)</span><span class="sxs-lookup"><span data-stu-id="ca19c-205">[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) followed by [DeleteItem](../web-service-reference/deleteitem-operation.md)</span></span> <br/> |[](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md#bk_DeleteMtgEWSMA) <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ca19c-206">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ca19c-206">See also</span></span>

- [<span data-ttu-id="ca19c-207">Stellvertretungszugriff und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="ca19c-207">Delegate access and EWS in Exchange</span></span>](delegate-access-and-ews-in-exchange.md)   
- [<span data-ttu-id="ca19c-208">Hinzufügen und Entfernen von Delegaten mithilfe der EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="ca19c-208">Add and remove delegates by using EWS in Exchange</span></span>](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md)
- [<span data-ttu-id="ca19c-209">Festlegen von Ordnerberechtigungen für einen anderen Benutzer mithilfe der EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="ca19c-209">Set folder permissions for another user by using EWS in Exchange</span></span>](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md) 
- [<span data-ttu-id="ca19c-210">Kalender und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="ca19c-210">Calendars and EWS in Exchange</span></span>](calendars-and-ews-in-exchange.md)
    

