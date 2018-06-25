---
title: CreateItem Operation
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
description: Der Vorgang CreateItem erstellt Elemente im Exchange-Speicher.
ms.openlocfilehash: 7e1808c685cdbaa1e8867aa7425b2cc52218d001
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757781"
---
# <a name="createitem-operation"></a><span data-ttu-id="87712-103">CreateItem Operation</span><span class="sxs-lookup"><span data-stu-id="87712-103">CreateItem operation</span></span>

<span data-ttu-id="87712-104">Der Vorgang CreateItem erstellt Elemente im Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="87712-104">The CreateItem operation creates items in the Exchange store.</span></span>
  
## <a name="using-the-createitem-operation"></a><span data-ttu-id="87712-105">Verwenden den CreateItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="87712-105">Using the CreateItem Operation</span></span>

<span data-ttu-id="87712-106">Den CreateItem-Vorgang können Sie Folgendes erstellen:</span><span class="sxs-lookup"><span data-stu-id="87712-106">You can use the CreateItem operation to create the following:</span></span>
  
- <span data-ttu-id="87712-107">Kalenderelementen (engl.)</span><span class="sxs-lookup"><span data-stu-id="87712-107">Calendar items</span></span>
    
- <span data-ttu-id="87712-108">E-Mails</span><span class="sxs-lookup"><span data-stu-id="87712-108">E-mail messages</span></span>
    
- <span data-ttu-id="87712-109">Besprechungsanfragen</span><span class="sxs-lookup"><span data-stu-id="87712-109">Meeting requests</span></span>
    
- <span data-ttu-id="87712-110">Aufgaben</span><span class="sxs-lookup"><span data-stu-id="87712-110">Tasks</span></span>
    
- <span data-ttu-id="87712-111">Kontakte</span><span class="sxs-lookup"><span data-stu-id="87712-111">Contacts</span></span>
    
<span data-ttu-id="87712-112">Weitere Informationen finden Sie unter [CreateItem Operation (Kalenderelement)](createitem-operation-calendar-item.md), [CreateItem-Vorgang (e-Mail-Nachricht)](createitem-operation-email-message.md), [CreateItem-Vorgang (Besprechungsanfrage)](createitem-operation-meeting-request.md), [CreateItem-Vorgang (Aufgabe)](createitem-operation-task.md)und [CreateItem-Vorgang (Kontakt) ](createitem-operation-contact.md).</span><span class="sxs-lookup"><span data-stu-id="87712-112">For more information, see [CreateItem operation (calendar item)](createitem-operation-calendar-item.md), [CreateItem operation (email message)](createitem-operation-email-message.md), [CreateItem operation (meeting request)](createitem-operation-meeting-request.md), [CreateItem operation (task)](createitem-operation-task.md), and [CreateItem operation (contact)](createitem-operation-contact.md).</span></span>
  
<span data-ttu-id="87712-113">Die CreateItem Operation unterstützt die Verwendung von Antwort-Objekten.</span><span class="sxs-lookup"><span data-stu-id="87712-113">The CreateItem operation supports the use of response objects.</span></span> <span data-ttu-id="87712-114">Antwortobjekte unterstützen die Annahme und Ablehnung von Besprechungen und die Behandlung von Abstimmungsoptionen Schaltflächen, die in einer standard-e-Mail-Nachricht enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="87712-114">Response objects support the acceptance and rejection of meetings and the handling of voting buttons that are included in a standard e-mail message.</span></span> <span data-ttu-id="87712-115">Die folgende Tabelle enthält die Antwortobjekte, die in der CreateItem Operation behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="87712-115">The following table lists the response objects that are handled in the CreateItem operation.</span></span>
  
|<span data-ttu-id="87712-116">**Response-Objekt**</span><span class="sxs-lookup"><span data-stu-id="87712-116">**Response object**</span></span>|<span data-ttu-id="87712-117">**Aktion**</span><span class="sxs-lookup"><span data-stu-id="87712-117">**Action**</span></span>|
|:-----|:-----|
|<span data-ttu-id="87712-118">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="87712-118">AcceptItem</span></span>  <br/> |<span data-ttu-id="87712-119">Annehmen von Besprechungsanfragen.</span><span class="sxs-lookup"><span data-stu-id="87712-119">Accept a meeting request.</span></span>  <br/> |
|<span data-ttu-id="87712-120">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="87712-120">CancelCalendarItem</span></span>  <br/> |<span data-ttu-id="87712-121">Stornieren einer Besprechung.</span><span class="sxs-lookup"><span data-stu-id="87712-121">Cancel a meeting.</span></span> <span data-ttu-id="87712-122">Dies unterscheidet sich von löschen alle Teilnehmer, da es für den Organisator die Besprechung auch gelöscht.</span><span class="sxs-lookup"><span data-stu-id="87712-122">This differs from deleting all attendees because it deletes the meeting for the organizer also.</span></span>  <br/> |
|<span data-ttu-id="87712-123">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="87712-123">DeclineItem</span></span>  <br/> |<span data-ttu-id="87712-124">Ablehnen einer Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="87712-124">Decline a meeting request.</span></span>  <br/> |
|<span data-ttu-id="87712-125">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="87712-125">ForwardItem</span></span>  <br/> |<span data-ttu-id="87712-126">Senden Sie eine Besprechungsanfrage an eine andere Person als eine Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="87712-126">Send a meeting request to another person as a meeting request.</span></span>  <br/> |
|<span data-ttu-id="87712-127">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="87712-127">RemoveItem</span></span>  <br/> |<span data-ttu-id="87712-128">Entfernen einer abgebrochenen Besprechung aus dem Kalender.</span><span class="sxs-lookup"><span data-stu-id="87712-128">Remove a canceled meeting from the calendar.</span></span>  <br/> |
|<span data-ttu-id="87712-129">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="87712-129">ReplyAllToItem</span></span>  <br/> |<span data-ttu-id="87712-130">Senden einer Nachricht, die den Textkörper der ursprünglichen Besprechungsanfrage an alle Teilnehmer der Besprechung enthält.</span><span class="sxs-lookup"><span data-stu-id="87712-130">Send a message that includes the body of the original meeting request to all attendees of the meeting.</span></span>  <br/> |
|<span data-ttu-id="87712-131">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="87712-131">ReplyToItem</span></span>  <br/> |<span data-ttu-id="87712-132">Senden einer Nachricht, die den Textkörper der ursprünglichen Besprechungsanfrage an den Absender der Besprechungsanfrage enthält.</span><span class="sxs-lookup"><span data-stu-id="87712-132">Send a message that includes the body of the original meeting request to the sender of the meeting request.</span></span>  <br/> |
|<span data-ttu-id="87712-133">SendReadReceipt</span><span class="sxs-lookup"><span data-stu-id="87712-133">SendReadReceipt</span></span>  <br/> |<span data-ttu-id="87712-134">Senden Sie eine lesebestätigung an den Absender der Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="87712-134">Send a read receipt to the sender of the meeting request.</span></span>  <br/> |
|<span data-ttu-id="87712-135">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="87712-135">TentativelyAcceptItem</span></span>  <br/> |<span data-ttu-id="87712-136">Mit Vorbehalt annehmen einer Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="87712-136">Tentatively accept a meeting request.</span></span>  <br/> |
   
<span data-ttu-id="87712-137">Die CreateItem Operation unterstützt auch zusätzliche Besprechung-Objekte.</span><span class="sxs-lookup"><span data-stu-id="87712-137">The CreateItem operation also supports additional meeting objects.</span></span> <span data-ttu-id="87712-138">Die folgende Tabelle enthält zusätzliche-Objekten, die CreateItem Operation unterstützt.</span><span class="sxs-lookup"><span data-stu-id="87712-138">The following table lists additional objects that the CreateItem operation supports.</span></span>
  
|<span data-ttu-id="87712-139">**Meeting-Objekt**</span><span class="sxs-lookup"><span data-stu-id="87712-139">**Meeting object**</span></span>|<span data-ttu-id="87712-140">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="87712-140">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="87712-141">Meeting-Nachricht</span><span class="sxs-lookup"><span data-stu-id="87712-141">Meeting Message</span></span>  <br/> |<span data-ttu-id="87712-142">Stellt eine Besprechungsnachricht im Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="87712-142">Represents a meeting message in the Exchange store.</span></span> <span data-ttu-id="87712-143">Dies ist das Basisobjekt für die Besprechung Objekte.</span><span class="sxs-lookup"><span data-stu-id="87712-143">This is the base object for the other meeting objects.</span></span>  <br/> |
|<span data-ttu-id="87712-144">Besprechungsanfrage</span><span class="sxs-lookup"><span data-stu-id="87712-144">Meeting Request</span></span>  <br/> |<span data-ttu-id="87712-145">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="87712-145">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|<span data-ttu-id="87712-146">Antwort auf Besprechungsanfrage</span><span class="sxs-lookup"><span data-stu-id="87712-146">Meeting Response</span></span>  <br/> |<span data-ttu-id="87712-147">Stellt eine Besprechungsantwort im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="87712-147">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|<span data-ttu-id="87712-148">Besprechungsabsagen</span><span class="sxs-lookup"><span data-stu-id="87712-148">Meeting Cancellation</span></span>  <br/> |<span data-ttu-id="87712-149">Stellt eine Besprechungsabsage im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="87712-149">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="87712-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="87712-150">See also</span></span>



[<span data-ttu-id="87712-151">CreateItem-Vorgang (Kalenderelement)</span><span class="sxs-lookup"><span data-stu-id="87712-151">CreateItem operation (calendar item)</span></span>](createitem-operation-calendar-item.md)
  
[<span data-ttu-id="87712-152">CreateItem-Vorgang (Kontakt)</span><span class="sxs-lookup"><span data-stu-id="87712-152">CreateItem operation (contact)</span></span>](createitem-operation-contact.md)
  
[<span data-ttu-id="87712-153">CreateItem-Vorgang (e-Mail-Nachricht)</span><span class="sxs-lookup"><span data-stu-id="87712-153">CreateItem operation (email message)</span></span>](createitem-operation-email-message.md)
  
[<span data-ttu-id="87712-154">CreateItem-Vorgang (Besprechungsanfrage)</span><span class="sxs-lookup"><span data-stu-id="87712-154">CreateItem operation (meeting request)</span></span>](createitem-operation-meeting-request.md)
  
[<span data-ttu-id="87712-155">CreateItem-Vorgang (Aufgabe)</span><span class="sxs-lookup"><span data-stu-id="87712-155">CreateItem operation (task)</span></span>](createitem-operation-task.md)
  
 <span data-ttu-id="87712-156">**CreateItemType**</span><span class="sxs-lookup"><span data-stu-id="87712-156">**CreateItemType**</span></span>

