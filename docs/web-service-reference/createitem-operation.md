---
title: CreateItem-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateItem
api_type:
- schema
ms.assetid: 78a52120-f1d0-4ed7-8748-436e554f75b6
description: Der CreateItem-Vorgang erstellt Elemente in der Exchange-Informationsspeicher.
ms.openlocfilehash: f6aaa9ed8e8257f19780492d6137fb015c1b6136
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458866"
---
# <a name="createitem-operation"></a><span data-ttu-id="2e8d6-103">CreateItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="2e8d6-103">CreateItem operation</span></span>

<span data-ttu-id="2e8d6-104">Der CreateItem-Vorgang erstellt Elemente in der Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="2e8d6-104">The CreateItem operation creates items in the Exchange store.</span></span>
  
## <a name="using-the-createitem-operation"></a><span data-ttu-id="2e8d6-105">Verwenden des CreateItem-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="2e8d6-105">Using the CreateItem Operation</span></span>

<span data-ttu-id="2e8d6-106">Sie können den CreateItem-Vorgang verwenden, um Folgendes zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="2e8d6-106">You can use the CreateItem operation to create the following:</span></span>
  
- <span data-ttu-id="2e8d6-107">Kalenderelemente</span><span class="sxs-lookup"><span data-stu-id="2e8d6-107">Calendar items</span></span>
    
- <span data-ttu-id="2e8d6-108">E-Mails</span><span class="sxs-lookup"><span data-stu-id="2e8d6-108">E-mail messages</span></span>
    
- <span data-ttu-id="2e8d6-109">Besprechungsanfragen</span><span class="sxs-lookup"><span data-stu-id="2e8d6-109">Meeting requests</span></span>
    
- <span data-ttu-id="2e8d6-110">Aufgaben</span><span class="sxs-lookup"><span data-stu-id="2e8d6-110">Tasks</span></span>
    
- <span data-ttu-id="2e8d6-111">Kontakte</span><span class="sxs-lookup"><span data-stu-id="2e8d6-111">Contacts</span></span>
    
<span data-ttu-id="2e8d6-112">Weitere Informationen finden Sie unter [CreateItem-Vorgang (Kalenderelement)](createitem-operation-calendar-item.md), CreateItem-Vorgang [(e-Mail-Nachricht)](createitem-operation-email-message.md), [CreateItem-Vorgang (Besprechungsanfrage)](createitem-operation-meeting-request.md), CreateItem-Vorgang [(Aufgabe)](createitem-operation-task.md)und [CreateItem-Vorgang (Kontakt)](createitem-operation-contact.md).</span><span class="sxs-lookup"><span data-stu-id="2e8d6-112">For more information, see [CreateItem operation (calendar item)](createitem-operation-calendar-item.md), [CreateItem operation (email message)](createitem-operation-email-message.md), [CreateItem operation (meeting request)](createitem-operation-meeting-request.md), [CreateItem operation (task)](createitem-operation-task.md), and [CreateItem operation (contact)](createitem-operation-contact.md).</span></span>
  
<span data-ttu-id="2e8d6-113">Der CreateItem-Vorgang unterstützt die Verwendung von Response-Objekten.</span><span class="sxs-lookup"><span data-stu-id="2e8d6-113">The CreateItem operation supports the use of response objects.</span></span> <span data-ttu-id="2e8d6-114">Antwortobjekte unterstützen die Akzeptanz und Ablehnung von Besprechungen und die Handhabung von Abstimmungsschaltflächen, die in einer Standard-e-Mail-Nachricht enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="2e8d6-114">Response objects support the acceptance and rejection of meetings and the handling of voting buttons that are included in a standard e-mail message.</span></span> <span data-ttu-id="2e8d6-115">In der folgenden Tabelle sind die Response-Objekte aufgeführt, die im CreateItem-Vorgang behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="2e8d6-115">The following table lists the response objects that are handled in the CreateItem operation.</span></span>
  
|<span data-ttu-id="2e8d6-116">**Response-Objekt**</span><span class="sxs-lookup"><span data-stu-id="2e8d6-116">**Response object**</span></span>|<span data-ttu-id="2e8d6-117">**Action**</span><span class="sxs-lookup"><span data-stu-id="2e8d6-117">**Action**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2e8d6-118">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="2e8d6-118">AcceptItem</span></span>  <br/> |<span data-ttu-id="2e8d6-119">Annehmen einer Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="2e8d6-119">Accept a meeting request.</span></span>  <br/> |
|<span data-ttu-id="2e8d6-120">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="2e8d6-120">CancelCalendarItem</span></span>  <br/> |<span data-ttu-id="2e8d6-121">Stornieren einer Besprechung.</span><span class="sxs-lookup"><span data-stu-id="2e8d6-121">Cancel a meeting.</span></span> <span data-ttu-id="2e8d6-122">Dies unterscheidet sich vom Löschen aller Teilnehmer, da die Besprechung auch für den Organisator gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="2e8d6-122">This differs from deleting all attendees because it deletes the meeting for the organizer also.</span></span>  <br/> |
|<span data-ttu-id="2e8d6-123">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="2e8d6-123">DeclineItem</span></span>  <br/> |<span data-ttu-id="2e8d6-124">Ablehnen einer Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="2e8d6-124">Decline a meeting request.</span></span>  <br/> |
|<span data-ttu-id="2e8d6-125">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="2e8d6-125">ForwardItem</span></span>  <br/> |<span data-ttu-id="2e8d6-126">Senden Sie eine Besprechungsanfrage als Besprechungsanfrage an eine andere Person.</span><span class="sxs-lookup"><span data-stu-id="2e8d6-126">Send a meeting request to another person as a meeting request.</span></span>  <br/> |
|<span data-ttu-id="2e8d6-127">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="2e8d6-127">RemoveItem</span></span>  <br/> |<span data-ttu-id="2e8d6-128">Entfernen einer abgebrochenen Besprechung aus dem Kalender.</span><span class="sxs-lookup"><span data-stu-id="2e8d6-128">Remove a canceled meeting from the calendar.</span></span>  <br/> |
|<span data-ttu-id="2e8d6-129">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="2e8d6-129">ReplyAllToItem</span></span>  <br/> |<span data-ttu-id="2e8d6-130">Senden Sie eine Nachricht, die den Textkörper der ursprünglichen Besprechungsanfrage enthält, an alle Teilnehmer der Besprechung.</span><span class="sxs-lookup"><span data-stu-id="2e8d6-130">Send a message that includes the body of the original meeting request to all attendees of the meeting.</span></span>  <br/> |
|<span data-ttu-id="2e8d6-131">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="2e8d6-131">ReplyToItem</span></span>  <br/> |<span data-ttu-id="2e8d6-132">Senden Sie eine Nachricht, die den Textkörper der ursprünglichen Besprechungsanfrage enthält, an den Absender der Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="2e8d6-132">Send a message that includes the body of the original meeting request to the sender of the meeting request.</span></span>  <br/> |
|<span data-ttu-id="2e8d6-133">SendReadReceipt</span><span class="sxs-lookup"><span data-stu-id="2e8d6-133">SendReadReceipt</span></span>  <br/> |<span data-ttu-id="2e8d6-134">Senden Sie eine Lesebestätigung an den Absender der Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="2e8d6-134">Send a read receipt to the sender of the meeting request.</span></span>  <br/> |
|<span data-ttu-id="2e8d6-135">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="2e8d6-135">TentativelyAcceptItem</span></span>  <br/> |<span data-ttu-id="2e8d6-136">Akzeptieren Sie eine Besprechungsanfrage mit Vorbehalt.</span><span class="sxs-lookup"><span data-stu-id="2e8d6-136">Tentatively accept a meeting request.</span></span>  <br/> |
   
<span data-ttu-id="2e8d6-137">Der CreateItem-Vorgang unterstützt auch zusätzliche Besprechungsobjekte.</span><span class="sxs-lookup"><span data-stu-id="2e8d6-137">The CreateItem operation also supports additional meeting objects.</span></span> <span data-ttu-id="2e8d6-138">In der folgenden Tabelle sind zusätzliche Objekte aufgeführt, die vom CreateItem-Vorgang unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="2e8d6-138">The following table lists additional objects that the CreateItem operation supports.</span></span>
  
|<span data-ttu-id="2e8d6-139">**Besprechungsobjekt**</span><span class="sxs-lookup"><span data-stu-id="2e8d6-139">**Meeting object**</span></span>|<span data-ttu-id="2e8d6-140">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2e8d6-140">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2e8d6-141">Besprechungsnachricht</span><span class="sxs-lookup"><span data-stu-id="2e8d6-141">Meeting Message</span></span>  <br/> |<span data-ttu-id="2e8d6-142">Stellt eine Besprechungsnachricht im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="2e8d6-142">Represents a meeting message in the Exchange store.</span></span> <span data-ttu-id="2e8d6-143">Dies ist das Basisobjekt für die anderen Besprechungsobjekte.</span><span class="sxs-lookup"><span data-stu-id="2e8d6-143">This is the base object for the other meeting objects.</span></span>  <br/> |
|<span data-ttu-id="2e8d6-144">Besprechungsanfrage</span><span class="sxs-lookup"><span data-stu-id="2e8d6-144">Meeting Request</span></span>  <br/> |<span data-ttu-id="2e8d6-145">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="2e8d6-145">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|<span data-ttu-id="2e8d6-146">Besprechungsantwort</span><span class="sxs-lookup"><span data-stu-id="2e8d6-146">Meeting Response</span></span>  <br/> |<span data-ttu-id="2e8d6-147">Stellt eine Besprechungsantwort im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="2e8d6-147">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|<span data-ttu-id="2e8d6-148">Besprechungs Abbruch</span><span class="sxs-lookup"><span data-stu-id="2e8d6-148">Meeting Cancellation</span></span>  <br/> |<span data-ttu-id="2e8d6-149">Stellt eine Besprechungsabsage im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="2e8d6-149">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2e8d6-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2e8d6-150">See also</span></span>



[<span data-ttu-id="2e8d6-151">CreateItem-Vorgang (Kalenderelement)</span><span class="sxs-lookup"><span data-stu-id="2e8d6-151">CreateItem operation (calendar item)</span></span>](createitem-operation-calendar-item.md)
  
[<span data-ttu-id="2e8d6-152">CreateItem-Vorgang (Kontakt)</span><span class="sxs-lookup"><span data-stu-id="2e8d6-152">CreateItem operation (contact)</span></span>](createitem-operation-contact.md)
  
[<span data-ttu-id="2e8d6-153">CreateItem-Vorgang (e-Mail-Nachricht)</span><span class="sxs-lookup"><span data-stu-id="2e8d6-153">CreateItem operation (email message)</span></span>](createitem-operation-email-message.md)
  
[<span data-ttu-id="2e8d6-154">CreateItem-Vorgang (Besprechungsanfrage)</span><span class="sxs-lookup"><span data-stu-id="2e8d6-154">CreateItem operation (meeting request)</span></span>](createitem-operation-meeting-request.md)
  
[<span data-ttu-id="2e8d6-155">CreateItem-Vorgang (Aufgabe)</span><span class="sxs-lookup"><span data-stu-id="2e8d6-155">CreateItem operation (task)</span></span>](createitem-operation-task.md)
  
 <span data-ttu-id="2e8d6-156">**CreateItemType**</span><span class="sxs-lookup"><span data-stu-id="2e8d6-156">**CreateItemType**</span></span>

