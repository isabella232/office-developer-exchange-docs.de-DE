---
title: Vorschlagen einer neuen Besprechungszeit mithilfe der EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: d5ac8e5b-3876-4f20-b4d3-44505e066042
description: Erfahren Sie, wie in der Exchange-Clientanwendung Besprechungszeiten vorschlagen mithilfe der EWS in Exchange.
ms.openlocfilehash: f9edd8511332474a728635a6aa369a772da24786
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756981"
---
# <a name="propose-a-new-meeting-time-by-using-ews-in-exchange"></a><span data-ttu-id="654c1-103">Vorschlagen einer neuen Besprechungszeit mithilfe der EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="654c1-103">Propose a new meeting time by using EWS in Exchange</span></span>

<span data-ttu-id="654c1-104">Erfahren Sie, wie in der Exchange-Clientanwendung Besprechungszeiten vorschlagen mithilfe der EWS in Exchange.</span><span class="sxs-lookup"><span data-stu-id="654c1-104">Find out how to propose new meeting times from your Exchange client application by using EWS in Exchange.</span></span>
  
<span data-ttu-id="654c1-105">Das neue Feature Zeit für vorschlagen ermöglicht es den Teilnehmern Besprechungszeiten Organisator der Besprechung als Teil des Exchange-Kalender Workflows vorschlagen.</span><span class="sxs-lookup"><span data-stu-id="654c1-105">The propose new time feature enables attendees to propose new meeting times to the meeting organizer as part of the Exchange calendar workflow.</span></span> <span data-ttu-id="654c1-106">Wenn ein Teilnehmer eine neue Besprechung vorschlägt, kann der Organisator verwenden der vorgeschlagene neue Besprechungszeit zum Aktualisieren der Besprechung und Aktualisierungen an alle Teilnehmer senden.</span><span class="sxs-lookup"><span data-stu-id="654c1-106">When an attendee proposes a new meeting, the organizer can use the proposed new meeting time to update the meeting and send updates to all attendees.</span></span> <span data-ttu-id="654c1-107">Bevor Sie Teilnehmer Besprechungszeiten vorschlagen aktivieren können, müssen Sie bestimmen, ob der Organisator für Vorschläge für neue Zeit zulässt.</span><span class="sxs-lookup"><span data-stu-id="654c1-107">Before you can enable attendees to propose new meeting times, you need to determine whether the organizer allows for new time proposals.</span></span> <span data-ttu-id="654c1-108">In diesem Artikel wird beschrieben, wie um festzustellen, ob Sie ein neues vorschlagen können Zeit- und wie Sie EWS verwenden, um eine neue Zeit vorschlagen.</span><span class="sxs-lookup"><span data-stu-id="654c1-108">This article describes how to determine whether you can propose a new time and how to use EWS to propose a new time.</span></span>
  
> [!NOTE]
> <span data-ttu-id="654c1-109">[!HINWEIS] Die verwaltete EWS-API implementiert diese Funktion nicht.</span><span class="sxs-lookup"><span data-stu-id="654c1-109">The EWS Managed API does not implement this functionality.</span></span> 
  
## <a name="determine-whether-you-can-propose-a-new-time-for-a-meeting-by-using-ews"></a><span data-ttu-id="654c1-110">Bestimmen Sie, ob Sie eine neue Zeit für eine Besprechung vorschlagen können mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="654c1-110">Determine whether you can propose a new time for a meeting by using EWS</span></span>
<span data-ttu-id="654c1-111"><a name="bk_Determine"> </a></span><span class="sxs-lookup"><span data-stu-id="654c1-111"></span></span>

<span data-ttu-id="654c1-112">Bevor Sie eine neue Zeit für eine Besprechung vorschlagen können, müssen Sie hier finden einen Verweis auf diese Besprechung und festzustellen, ob der Organisator der Besprechung die Besprechung zur Unterstützung von neue Zeit Vorschläge konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="654c1-112">Before you can propose a new time for a meeting, you need to find a reference to that meeting and determine whether the meeting organizer configured the meeting to support new time proposals.</span></span> <span data-ttu-id="654c1-113">Sie können einen Verweis auf eine Besprechung erhalten, indem Sie eines der folgenden:</span><span class="sxs-lookup"><span data-stu-id="654c1-113">You can get a reference to a meeting by doing either of the following:</span></span> 
  
- <span data-ttu-id="654c1-114">Suchen nach der Besprechungsanfrage im Posteingang</span><span class="sxs-lookup"><span data-stu-id="654c1-114">Finding the meeting request in the Inbox</span></span>
    
- <span data-ttu-id="654c1-115">Suchen den Termin im Kalender</span><span class="sxs-lookup"><span data-stu-id="654c1-115">Finding the appointment in the calendar</span></span>
    
<span data-ttu-id="654c1-116">Gehen Sie folgendermaßen vor, um einen Verweis Besprechung zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="654c1-116">Use the following steps to find a meeting reference:</span></span>
  
1. <span data-ttu-id="654c1-117">Verwenden Sie [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) EWS-Vorgangs (oder die [Folder.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.finditems%28v=EXCHG.80%29.aspx) EWS Managed API-Methode) zum Suchen nach der-Ziel meeting Anforderung oder Kalenderelement.</span><span class="sxs-lookup"><span data-stu-id="654c1-117">Use the [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) EWS operation (or the [Folder.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.finditems%28v=EXCHG.80%29.aspx) EWS Managed API method) to find the target meeting request or calendar item.</span></span> <span data-ttu-id="654c1-118">Alternativ können Sie [SyncFolderItems](http://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx) EWS-Vorgangs verwenden, um den Bezeichner des Ziels meeting Anforderung oder Kalenderelement abzurufen.</span><span class="sxs-lookup"><span data-stu-id="654c1-118">Alternatively, you can use the [SyncFolderItems](http://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx) EWS operation to get the identifier of the target meeting request or calendar item.</span></span> 
    
2. <span data-ttu-id="654c1-119">Analysieren Sie die Ergebnisse der **FindItem** -Vorgang (oder **Folder.FindItems** -Methode) zum Abrufen der Elementbezeichner des Besprechungselements.</span><span class="sxs-lookup"><span data-stu-id="654c1-119">Parse the results of the **FindItem** operation (or **Folder.FindItems** method) to get the item identifier of the meeting item.</span></span> 
    
3. <span data-ttu-id="654c1-120">Verwenden Sie den [GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) -EWS-Vorgang, um die Antwortobjekte für die Besprechung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="654c1-120">Use the [GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) EWS operation to get the response objects for the meeting.</span></span> 
    
<span data-ttu-id="654c1-121">Das folgende XML zeigt, was gesendet wird, um die Antwortobjekte für ein Element anzufordern.</span><span class="sxs-lookup"><span data-stu-id="654c1-121">The following XML shows what is sent to request the response objects on an item.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
    <t:MailboxCulture>en-US</t:MailboxCulture>
  </soap:Header>
  <soap:Body>
    <m:GetItem>
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:ResponseObjects"/>
          <t:FieldURI FieldURI="item:Subject"/>
          <t:FieldURI FieldURI="calendar:Start"/>
          <t:FieldURI FieldURI="calendar:End"/>
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:ItemIds>
        <t:ItemId Id="AAMkADEzOTExYjJkL1AAA=" ChangeKey="CwAAAB/G6X"/>
      </m:ItemIds>
    </m:GetItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="654c1-122">**GetItem** Operation Antwort sieht ungefähr wie die folgende XML-Code, wenn Sie die Element-ID, die Besprechung starten und Endzeit, die Antwort objektauflistung anfordern und der Organisator vorgeschlagenen Änderungen an die Besprechungszeit ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="654c1-122">The **GetItem** operation response will look similar to the following XML if you request the item identifier, the meeting start and end time, the response object collection, and if the organizer allows for proposed changes to the meeting time.</span></span> <span data-ttu-id="654c1-123">Die Antwort-Auflistung-Objekt, das durch das [ResponseObjects](http://msdn.microsoft.com/library/ad29e064-3f3d-4b7b-aa4c-9ec27326381d%28Office.15%29.aspx) -Element dargestellt wird, enthält den Satz von Antworten, die für das Kalenderelement gültig sind.</span><span class="sxs-lookup"><span data-stu-id="654c1-123">The response object collection, which is represented by the [ResponseObjects](http://msdn.microsoft.com/library/ad29e064-3f3d-4b7b-aa4c-9ec27326381d%28Office.15%29.aspx) element, contains the set of responses that are valid for the calendar item.</span></span> <span data-ttu-id="654c1-124">Das **ProposeNewTime** -Element ist ein Antwortobjekt, der angibt, dass der Benutzer eine neue Zeit für die Besprechung vorschlagen kann.</span><span class="sxs-lookup"><span data-stu-id="654c1-124">The **ProposeNewTime** element is a response object that indicates that the user can propose a new time for the meeting.</span></span> <span data-ttu-id="654c1-125">Die [AcceptItem](http://msdn.microsoft.com/library/05a15431-77e1-411a-a16b-5481d364d3cc%28Office.15%29.aspx) [TentativelyAcceptItem](http://msdn.microsoft.com/library/ce6f50ef-ad8a-47e4-915a-487b2ef7a2e0%28Office.15%29.aspx)und [DeclineItem](http://msdn.microsoft.com/library/2d8d2389-924e-4d03-a324-35d56cf0d6b1%28Office.15%29.aspx) -Elemente darstellen, die Antwortobjekte, die Sie verwenden können, der Besprechungsorganisator eine neue Besprechungszeit vorschlagen.</span><span class="sxs-lookup"><span data-stu-id="654c1-125">The [AcceptItem](http://msdn.microsoft.com/library/05a15431-77e1-411a-a16b-5481d364d3cc%28Office.15%29.aspx), [TentativelyAcceptItem](http://msdn.microsoft.com/library/ce6f50ef-ad8a-47e4-915a-487b2ef7a2e0%28Office.15%29.aspx), and [DeclineItem](http://msdn.microsoft.com/library/2d8d2389-924e-4d03-a324-35d56cf0d6b1%28Office.15%29.aspx) elements represent the response objects that you can use to propose a new meeting time to the meeting organizer.</span></span> 
  
```XML
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" 
                         MinorVersion="0" 
                         MajorBuildNumber="815" 
                         MinorBuildNumber="6" 
                         Version="V2_7" 
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:MeetingRequest>
              <t:ItemId Id="AAMkADEzOTExYjJkL1AAA=" ChangeKey="CwAAAB/G6X"/>
              <t:Subject>Competitive analysis: kick off meeting</t:Subject>
              <t:ResponseObjects>
                <t:AcceptItem/>
                <t:TentativelyAcceptItem/>
                <t:DeclineItem/>
                <t:ProposeNewTime/>
                <t:ReplyToItem/>
                <t:ReplyAllToItem/>
                <t:ForwardItem/>
              </t:ResponseObjects>
              <t:Start>2013-11-09T17:00:00Z</t:Start>
              <t:End>2013-11-09T17:30:00Z</t:End>
            </t:MeetingRequest>
          </m:Items>
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </m:GetItemResponse>
  </s:Body>
</s:Envelope>
```

## <a name="propose-a-new-meeting-time-by-using-ews"></a><span data-ttu-id="654c1-126">Vorschlagen einer neuen Besprechungszeit mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="654c1-126">Propose a new meeting time by using EWS</span></span>
<span data-ttu-id="654c1-127"><a name="bk_Propose"> </a></span><span class="sxs-lookup"><span data-stu-id="654c1-127"></span></span>

<span data-ttu-id="654c1-128">Wenn Sie ein Antwortobjekt **ProposeNewTime** erhalten, wenn Sie die **GetItem** Operation verwendet, um ein Kalenderelement oder einer Besprechungsanfrage erhalten möchten, können Sie mit einer vorgeschlagenen neuen Besprechungszeit reagieren.</span><span class="sxs-lookup"><span data-stu-id="654c1-128">If you received a **ProposeNewTime** response object when you used the **GetItem** operation to get a calendar item or meeting request, you can respond with a proposed new meeting time.</span></span> <span data-ttu-id="654c1-129">Wenn Sie eine **ProposeNewTime** Response-Objekt nicht erhalten haben, werden Sie kann nicht als Teil des Workflows Kalender eine neue Besprechungszeit vorschlagen.</span><span class="sxs-lookup"><span data-stu-id="654c1-129">If you didn't receive a **ProposeNewTime** response object, you won't be able to propose a new meeting time as part of the calendar workflow.</span></span> <span data-ttu-id="654c1-130">Sie können jedoch auf der Organisator eine neuen Besprechungszeit anfordern antworten.</span><span class="sxs-lookup"><span data-stu-id="654c1-130">You can, however, reply to the organizer to request a new meeting time.</span></span> <span data-ttu-id="654c1-131">Ein Antwortobjekt **ProposeNewTime** gemeldet werden, können Sie durch einen Verweis auf den Bezeichner für die Besprechung reagieren und vorschlagen eine neuen Besprechungszeit an den Organisator.</span><span class="sxs-lookup"><span data-stu-id="654c1-131">If you receive a **ProposeNewTime** response object, you can respond to the meeting by referencing its identifier, and propose a new meeting time to the organizer.</span></span> <span data-ttu-id="654c1-132">Dies ist, in dem das Antwortobjekt **ProposeNewTime** dem normalen Reaktionszeit Objekt Muster unterscheidet, dass Sie nicht mit einem **ProposeNewTime** Antwortobjekt Antworten.</span><span class="sxs-lookup"><span data-stu-id="654c1-132">This is where the **ProposeNewTime** response object is different than the typical response object pattern in that you don't respond with a **ProposeNewTime** response object.</span></span> <span data-ttu-id="654c1-133">Verwenden Sie eine der anderen meeting Antwortobjekte wie **AcceptItem**, **TentativelyAcceptItem**oder **DeclineItem**, eine neue Besprechung vorschlagen.</span><span class="sxs-lookup"><span data-stu-id="654c1-133">You use one of the other meeting response objects, such as **AcceptItem**, **TentativelyAcceptItem**, or **DeclineItem**, to propose a new meeting.</span></span> <span data-ttu-id="654c1-134">In diesem Beispiel wird das **AcceptItem** Response-Objekt.</span><span class="sxs-lookup"><span data-stu-id="654c1-134">This example uses the **AcceptItem** response object.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013"/>
  </soap:Header>
  <soap:Body>
    <m:CreateItem>
      <m:Items>
        <t:AcceptItem>
          <t:Body BodyType="Text">This time works better for the HiPPO.</t:Body>
          <t:ReferenceItemId Id="AAMkADEzOTExYjJkL1AAA=" ChangeKey="CwAAAB/G6X"/>
          <t:ProposedStart>2013-11-28T04:00:00Z</t:ProposedStart>
          <t:ProposedEnd>2013-11-28T04:30:00Z</t:ProposedEnd>
        </t:AcceptItem>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="654c1-135">Die Antwort auf diese Anforderung enthält die ID des Kalenderelements an, das Kalender des Teilnehmers hinzugefügt wurde, und eine Kopie der Besprechungsanfrage, die im Ordner für die Teilnehmer Gelöschte Objekte getätigt wurde.</span><span class="sxs-lookup"><span data-stu-id="654c1-135">The response to this request contains the identifier of the calendar item that was added to the attendee's calendar and a copy of the meeting request that was placed in the attendee's Deleted Items folder.</span></span> <span data-ttu-id="654c1-136">Die Response-Nachricht mit dem neuen Uhrzeit Vorschlag wurde auch im Ordner für die Teilnehmer gesendete Objekte gespeichert (müssen Sie die Besprechung suchen Antwortnachricht zu handhaben darauf).</span><span class="sxs-lookup"><span data-stu-id="654c1-136">The response message with the new time proposal was also saved in the attendee's Sent Items folder (you will need to find the meeting response message to get a handle on it).</span></span>
  
```XML
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" 
                         MinorVersion="0" 
                         MajorBuildNumber="815" 
                         MinorBuildNumber="6" 
                         Version="V2_7" 
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:CreateItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:CreateItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:CalendarItem>
              <t:ItemId Id="AAMkAGRmOWE2OWAAA=" ChangeKey="DwAAJsmU"/>
            </t:CalendarItem>
            <t:MeetingRequest>
              <t:ItemId Id="AAMkAGRmOWE2AAABB=" ChangeKey="AAAGJu1A"/>
            </t:MeetingRequest>
          </m:Items>
        </m:CreateItemResponseMessage>
      </m:ResponseMessages>
    </m:CreateItemResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="654c1-137">Der Organisator erhalten eine [MeetingResponse](http://msdn.microsoft.com/library/9f798e79-dafd-4d4d-9967-95fd8e5c0502%28Office.15%29.aspx) -Nachricht, wenn der Teilnehmer mit einer vorgeschlagenen neuen Besprechungszeit antwortet.</span><span class="sxs-lookup"><span data-stu-id="654c1-137">The organizer will receive a [MeetingResponse](http://msdn.microsoft.com/library/9f798e79-dafd-4d4d-9967-95fd8e5c0502%28Office.15%29.aspx) message when the attendee responds with a proposed new meeting time.</span></span> <span data-ttu-id="654c1-138">Die **MeetingResponse** -Nachricht enthält die vorgeschlagene neue Besprechung Startzeit und Endzeit und die ID des zugeordneten Kalenderelements im Kalender des Organisierer vorhanden.</span><span class="sxs-lookup"><span data-stu-id="654c1-138">The **MeetingResponse** message contains the proposed new meeting start time and end time, and the identifier of the associated calendar item in the organizer's calendar.</span></span> <span data-ttu-id="654c1-139">Der Organisator kann diese Informationen verwenden, um ihre vorhandene Kalenderelement für die Besprechung zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="654c1-139">The organizer can use that information to update their existing calendar item for the meeting.</span></span> <span data-ttu-id="654c1-140">Es folgt der Workflow für den Organisator Antworten auf eine **MeetingResponse** -Nachrichten, die eine neue Besprechungszeit vorgeschlagen:</span><span class="sxs-lookup"><span data-stu-id="654c1-140">The following is the workflow for the organizer to respond to a **MeetingResponse** message that proposes a new meeting time:</span></span> 
  
1. <span data-ttu-id="654c1-141">Bestimmen Sie, ob die **ProposedStart** oder **ProposedEnd** -Elemente in der **MeetingResponse**festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="654c1-141">Determine whether the **ProposedStart** or **ProposedEnd** elements have been set in the **MeetingResponse**.</span></span> <span data-ttu-id="654c1-142">Wenn dies der Fall ist, fahren Sie mit Schritt 2.</span><span class="sxs-lookup"><span data-stu-id="654c1-142">If so, go to step 2.</span></span> <span data-ttu-id="654c1-143">Wenn dies nicht der Fall ist, wird die Nachricht **MeetingResponse** nur gibt an, ob der Teilnehmer hat akzeptiert, mit Vorbehalt angenommen oder die Besprechung wurde abgesagt.</span><span class="sxs-lookup"><span data-stu-id="654c1-143">If not, the **MeetingResponse** message only indicates whether the attendee has accepted, tentatively accepted, or declined the meeting.</span></span> 
    
2. <span data-ttu-id="654c1-144">Rufen Sie vorhandene Kalenderelement der Organisator für die Besprechung, mithilfe des EWS-Bezeichners im **AssociatedCalendarItemId** Element zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="654c1-144">Get the organizer's existing calendar item for the meeting by using the EWS identifier returned in the **AssociatedCalendarItemId** element.</span></span> 
    
3. <span data-ttu-id="654c1-145">Vergleichen Sie die ursprünglichen Start- und Endzeit mit vorgeschlagenen neuen Besprechungszeit.</span><span class="sxs-lookup"><span data-stu-id="654c1-145">Compare the original start and end time with the proposed new meeting time.</span></span> <span data-ttu-id="654c1-146">Wenn die vorgeschlagene neue Besprechungszeit an den Organisator akzeptabel ist, fahren Sie mit Schritt 4.</span><span class="sxs-lookup"><span data-stu-id="654c1-146">If the proposed new meeting time is acceptable to the organizer, go to step 4.</span></span> <span data-ttu-id="654c1-147">Der Organisator der Besprechung Anderenfalls kann entweder ignorieren die Uhrzeit der vorgeschlagenen Besprechung oder senden eine e-Mail-Antwort an die Teilnehmer, die die neue Besprechungszeit vorgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="654c1-147">Otherwise, the meeting organizer can either ignore the proposed meeting time, or send an email response to the attendee that proposed the new meeting time.</span></span>
    
4. <span data-ttu-id="654c1-148">(Optional) Führen Sie einen Anruf [GetUserAvailability](http://msdn.microsoft.com/library/8da17226-5d3a-4525-9ffa-d83730f47bb1%28Office.15%29.aspx) EWS-Vorgang, um herauszufinden, ob die vorgeschlagene Zeit für alle Teilnehmer, einschließlich der Postfächer Raum- und Ressource funktioniert.</span><span class="sxs-lookup"><span data-stu-id="654c1-148">(Optional) Perform a [GetUserAvailability](http://msdn.microsoft.com/library/8da17226-5d3a-4525-9ffa-d83730f47bb1%28Office.15%29.aspx) EWS operation call to find out whether the proposed time will work for all attendees, including room and resource mailboxes.</span></span> <span data-ttu-id="654c1-149">(Sie können die [ExchangeService.GetUserAvailability](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.getuseravailability%28v=exchg.80%29.aspx) EWS Managed API-Methode auch verwenden, dazu.)</span><span class="sxs-lookup"><span data-stu-id="654c1-149">(You can also use the [ExchangeService.GetUserAvailability](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.getuseravailability%28v=exchg.80%29.aspx) EWS Managed API method to do this.)</span></span> 
    
5. <span data-ttu-id="654c1-150">Der Organisator kann dann aktualisieren Sie ihre Besprechung mit der vorgeschlagenen Besprechungszeiten und senden die Updates an alle Teilnehmer mithilfe der [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) EWS-Vorgang (oder die [Appointment.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx) EWS Managed API-Methode).</span><span class="sxs-lookup"><span data-stu-id="654c1-150">The organizer can then update their meeting with the new proposed meeting times and send the updates to all attendees by using the [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) EWS operation (or the [Appointment.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx) EWS Managed API method).</span></span> 
    
<span data-ttu-id="654c1-151">Die folgende Abbildung zeigt den Prozess, der zwischen der Organisator der Besprechung, die Teilnehmer und der Exchange-Server, der die EWS-Aufrufe behandelt.</span><span class="sxs-lookup"><span data-stu-id="654c1-151">The following figure shows the process that occurs between the meeting organizer, the attendee, and the Exchange server that handled the EWS calls.</span></span>
  
<span data-ttu-id="654c1-152">**Abbildung 1. Prozess zum Vorschlagen einer neuen Besprechungszeit**</span><span class="sxs-lookup"><span data-stu-id="654c1-152">**Figure 1. Process for proposing a new meeting time**</span></span>

![In der Abbildung wird der Workflow zwischen dem Organisator, Exchange und einem Teilnehmer dargestellt, wenn eine neue Besprechungszeit vorgeschlagen wird. Wenn der Organisator neue Vorschläge für Besprechungen zulässt, kann ein Teilnehmer eine neue Besprechungszeit mit einem Antwortobjekt vorschlagen.](media/Ex_ProposeNewMeetingTime.png)
  
## <a name="version-differences"></a><span data-ttu-id="654c1-155">Versionsunterschiede</span><span class="sxs-lookup"><span data-stu-id="654c1-155">Version differences</span></span>
<span data-ttu-id="654c1-156"><a name="bk_Behavior"> </a></span><span class="sxs-lookup"><span data-stu-id="654c1-156"></span></span>

<span data-ttu-id="654c1-157">Das neue Feature Zeit für vorschlagen wurde in Exchange Buildversion 15.00.0800.007 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="654c1-157">The propose new time feature was introduced in Exchange build version 15.00.0800.007.</span></span> <span data-ttu-id="654c1-158">In früheren Versionen von Exchange müssen Benutzer EWS-Anwendung senden eine separate e-Mail an den Organisator der Besprechung eine andere Besprechungszeit anfordern.</span><span class="sxs-lookup"><span data-stu-id="654c1-158">In earlier versions of Exchange, EWS application users have to send a separate email to the meeting organizer to request a different meeting time.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="654c1-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="654c1-159">See also</span></span>


- [<span data-ttu-id="654c1-160">Kalender und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="654c1-160">Calendars and EWS in Exchange</span></span>](calendars-and-ews-in-exchange.md)
    
- [<span data-ttu-id="654c1-161">Erstellen von Terminen und Besprechungen mithilfe von EWS in Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="654c1-161">Create appointments and meetings by using EWS in Exchange 2013</span></span>](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [<span data-ttu-id="654c1-162">Abrufen von Terminen und Besprechungen mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="654c1-162">Get appointments and meetings by using EWS in Exchange</span></span>](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="654c1-163">Aktualisieren von Terminen und Besprechungen mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="654c1-163">Update appointments and meetings by using EWS in Exchange</span></span>](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="654c1-164">Löschen von Terminen und Abbrechen an Besprechungen mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="654c1-164">Delete appointments and cancel meetings by using EWS in Exchange</span></span>](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)
    

