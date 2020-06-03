---
title: Vorschlagen einer neuen Besprechungszeit mithilfe von EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: d5ac8e5b-3876-4f20-b4d3-44505e066042
description: Erfahren Sie, wie Sie neue Besprechungszeiten in Ihrer Exchange-Clientanwendung mithilfe von EWS in Exchange vorschlagen.
ms.openlocfilehash: 4f001bb82d2325624b567412620283619b51f25b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456811"
---
# <a name="propose-a-new-meeting-time-by-using-ews-in-exchange"></a><span data-ttu-id="35571-103">Vorschlagen einer neuen Besprechungszeit mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="35571-103">Propose a new meeting time by using EWS in Exchange</span></span>

<span data-ttu-id="35571-104">Erfahren Sie, wie Sie neue Besprechungszeiten in Ihrer Exchange-Clientanwendung mithilfe von EWS in Exchange vorschlagen.</span><span class="sxs-lookup"><span data-stu-id="35571-104">Find out how to propose new meeting times from your Exchange client application by using EWS in Exchange.</span></span>
  
<span data-ttu-id="35571-105">Mit dem Feature neue Zeit vorschlagen können Teilnehmer dem Besprechungsorganisator neue Besprechungszeiten als Teil des Exchange-Kalender Workflows vorschlagen.</span><span class="sxs-lookup"><span data-stu-id="35571-105">The propose new time feature enables attendees to propose new meeting times to the meeting organizer as part of the Exchange calendar workflow.</span></span> <span data-ttu-id="35571-106">Wenn ein Teilnehmer eine neue Besprechung vorschlägt, kann der Organisator die vorgeschlagene neue Besprechungszeit verwenden, um die Besprechung zu aktualisieren und Updates an alle Teilnehmer zu senden.</span><span class="sxs-lookup"><span data-stu-id="35571-106">When an attendee proposes a new meeting, the organizer can use the proposed new meeting time to update the meeting and send updates to all attendees.</span></span> <span data-ttu-id="35571-107">Bevor Sie Teilnehmern die Möglichkeit geben, neue Besprechungszeiten vorzuschlagen, müssen Sie ermitteln, ob der Organisator neue Zeit Vorschläge zulässt.</span><span class="sxs-lookup"><span data-stu-id="35571-107">Before you can enable attendees to propose new meeting times, you need to determine whether the organizer allows for new time proposals.</span></span> <span data-ttu-id="35571-108">In diesem Artikel wird beschrieben, wie Sie bestimmen können, ob Sie eine neue Zeit vorschlagen und wie Sie EWS verwenden, um eine neue Zeit anzubieten.</span><span class="sxs-lookup"><span data-stu-id="35571-108">This article describes how to determine whether you can propose a new time and how to use EWS to propose a new time.</span></span>
  
> [!NOTE]
> <span data-ttu-id="35571-109">Die verwaltete EWS-API implementiert diese Funktion nicht.</span><span class="sxs-lookup"><span data-stu-id="35571-109">The EWS Managed API does not implement this functionality.</span></span> 
  
## <a name="determine-whether-you-can-propose-a-new-time-for-a-meeting-by-using-ews"></a><span data-ttu-id="35571-110">Ermitteln, ob Sie eine neue Zeit für eine Besprechung mithilfe von EWS vorschlagen können</span><span class="sxs-lookup"><span data-stu-id="35571-110">Determine whether you can propose a new time for a meeting by using EWS</span></span>
<span data-ttu-id="35571-111"><a name="bk_Determine"> </a></span><span class="sxs-lookup"><span data-stu-id="35571-111"><a name="bk_Determine"> </a></span></span>

<span data-ttu-id="35571-112">Bevor Sie eine neue Zeit für eine Besprechung vorschlagen können, müssen Sie einen Verweis auf diese Besprechung finden und bestimmen, ob der Besprechungsorganisator die Besprechung so konfiguriert hat, dass neue Zeit Vorschläge unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="35571-112">Before you can propose a new time for a meeting, you need to find a reference to that meeting and determine whether the meeting organizer configured the meeting to support new time proposals.</span></span> <span data-ttu-id="35571-113">Sie können einen Verweis auf eine Besprechung erhalten, indem Sie einen der folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="35571-113">You can get a reference to a meeting by doing either of the following:</span></span> 
  
- <span data-ttu-id="35571-114">Suchen der Besprechungsanfrage im Posteingang</span><span class="sxs-lookup"><span data-stu-id="35571-114">Finding the meeting request in the Inbox</span></span>
    
- <span data-ttu-id="35571-115">Suchen des Termins im Kalender</span><span class="sxs-lookup"><span data-stu-id="35571-115">Finding the appointment in the calendar</span></span>
    
<span data-ttu-id="35571-116">Führen Sie die folgenden Schritte aus, um eine Besprechungs Referenz zu finden:</span><span class="sxs-lookup"><span data-stu-id="35571-116">Use the following steps to find a meeting reference:</span></span>
  
1. <span data-ttu-id="35571-117">Verwenden Sie den [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) -EWS-Vorgang (oder die [Folder. FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.finditems%28v=EXCHG.80%29.aspx) verwaltete EWS-API-Methode), um die Ziel-Besprechungsanfrage oder das Kalenderelement zu finden.</span><span class="sxs-lookup"><span data-stu-id="35571-117">Use the [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) EWS operation (or the [Folder.FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.finditems%28v=EXCHG.80%29.aspx) EWS Managed API method) to find the target meeting request or calendar item.</span></span> <span data-ttu-id="35571-118">Alternativ können Sie den [SyncFolderItems](https://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx) -EWS-Vorgang verwenden, um den Bezeichner der Ziel-Besprechungsanfrage oder des Kalenderelements abzurufen.</span><span class="sxs-lookup"><span data-stu-id="35571-118">Alternatively, you can use the [SyncFolderItems](https://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx) EWS operation to get the identifier of the target meeting request or calendar item.</span></span> 
    
2. <span data-ttu-id="35571-119">Analysieren Sie die Ergebnisse des **FindItem** -Vorgangs (oder der **Folder. FindItems** -Methode), um den Elementbezeichner des Besprechungselements abzurufen.</span><span class="sxs-lookup"><span data-stu-id="35571-119">Parse the results of the **FindItem** operation (or **Folder.FindItems** method) to get the item identifier of the meeting item.</span></span> 
    
3. <span data-ttu-id="35571-120">Verwenden Sie den [GetItem](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) -EWS-Vorgang, um die Response-Objekte für die Besprechung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="35571-120">Use the [GetItem](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) EWS operation to get the response objects for the meeting.</span></span> 
    
<span data-ttu-id="35571-121">Der folgende XML-Code zeigt, was gesendet wird, um die Response-Objekte für ein Element anzufordern.</span><span class="sxs-lookup"><span data-stu-id="35571-121">The following XML shows what is sent to request the response objects on an item.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
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

<span data-ttu-id="35571-122">Die **GetItem** -Vorgangs Antwort sieht ähnlich wie beim folgenden XML-Code aus, wenn Sie die Element-ID, die Start-und Endzeit der Besprechung, die Auflistung der Antwortobjekte anfordern und die vorgeschlagene Änderung an der Besprechungszeit durch den Organisator ermöglicht wird.</span><span class="sxs-lookup"><span data-stu-id="35571-122">The **GetItem** operation response will look similar to the following XML if you request the item identifier, the meeting start and end time, the response object collection, and if the organizer allows for proposed changes to the meeting time.</span></span> <span data-ttu-id="35571-123">Die Response-Objektsammlung, die durch das [ResponseObjects](https://msdn.microsoft.com/library/ad29e064-3f3d-4b7b-aa4c-9ec27326381d%28Office.15%29.aspx) -Element dargestellt wird, enthält die Gruppe von Antworten, die für das Kalenderelement gültig sind.</span><span class="sxs-lookup"><span data-stu-id="35571-123">The response object collection, which is represented by the [ResponseObjects](https://msdn.microsoft.com/library/ad29e064-3f3d-4b7b-aa4c-9ec27326381d%28Office.15%29.aspx) element, contains the set of responses that are valid for the calendar item.</span></span> <span data-ttu-id="35571-124">Das **ProposeNewTime** -Element ist ein Response-Objekt, das angibt, dass der Benutzer eine neue Zeit für die Besprechung vorschlagen kann.</span><span class="sxs-lookup"><span data-stu-id="35571-124">The **ProposeNewTime** element is a response object that indicates that the user can propose a new time for the meeting.</span></span> <span data-ttu-id="35571-125">Die [AcceptItem](https://msdn.microsoft.com/library/05a15431-77e1-411a-a16b-5481d364d3cc%28Office.15%29.aspx)-, [TentativelyAcceptItem](https://msdn.microsoft.com/library/ce6f50ef-ad8a-47e4-915a-487b2ef7a2e0%28Office.15%29.aspx)-und [DeclineItem](https://msdn.microsoft.com/library/2d8d2389-924e-4d03-a324-35d56cf0d6b1%28Office.15%29.aspx) -Elemente stellen die Response-Objekte dar, die Sie verwenden können, um dem Besprechungsorganisator eine neue Besprechungszeit vorzuschlagen.</span><span class="sxs-lookup"><span data-stu-id="35571-125">The [AcceptItem](https://msdn.microsoft.com/library/05a15431-77e1-411a-a16b-5481d364d3cc%28Office.15%29.aspx), [TentativelyAcceptItem](https://msdn.microsoft.com/library/ce6f50ef-ad8a-47e4-915a-487b2ef7a2e0%28Office.15%29.aspx), and [DeclineItem](https://msdn.microsoft.com/library/2d8d2389-924e-4d03-a324-35d56cf0d6b1%28Office.15%29.aspx) elements represent the response objects that you can use to propose a new meeting time to the meeting organizer.</span></span> 
  
```XML
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" 
                         MinorVersion="0" 
                         MajorBuildNumber="815" 
                         MinorBuildNumber="6" 
                         Version="V2_7" 
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="propose-a-new-meeting-time-by-using-ews"></a><span data-ttu-id="35571-126">Vorschlagen einer neuen Besprechungszeit mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="35571-126">Propose a new meeting time by using EWS</span></span>
<span data-ttu-id="35571-127"><a name="bk_Propose"> </a></span><span class="sxs-lookup"><span data-stu-id="35571-127"><a name="bk_Propose"> </a></span></span>

<span data-ttu-id="35571-128">Wenn Sie ein **ProposeNewTime** -Antwortobjekt erhalten haben, als Sie den **GetItem** -Vorgang zum Abrufen eines Kalenderelements oder einer Besprechungsanfrage verwendet haben, können Sie mit einer vorgeschlagenen neuen Besprechungszeit Antworten.</span><span class="sxs-lookup"><span data-stu-id="35571-128">If you received a **ProposeNewTime** response object when you used the **GetItem** operation to get a calendar item or meeting request, you can respond with a proposed new meeting time.</span></span> <span data-ttu-id="35571-129">Wenn Sie kein **ProposeNewTime** -Antwortobjekt erhalten haben, können Sie im Rahmen des Kalender Workflows keine neue Besprechungszeit vorschlagen.</span><span class="sxs-lookup"><span data-stu-id="35571-129">If you didn't receive a **ProposeNewTime** response object, you won't be able to propose a new meeting time as part of the calendar workflow.</span></span> <span data-ttu-id="35571-130">Sie können jedoch dem Organisator Antworten, um eine neue Besprechungszeit anzufordern.</span><span class="sxs-lookup"><span data-stu-id="35571-130">You can, however, reply to the organizer to request a new meeting time.</span></span> <span data-ttu-id="35571-131">Wenn Sie ein **ProposeNewTime** -Antwortobjekt erhalten, können Sie auf die Besprechung Antworten, indem Sie auf Ihren Bezeichner verweisen, und dem Organisator eine neue Besprechungszeit vorschlagen.</span><span class="sxs-lookup"><span data-stu-id="35571-131">If you receive a **ProposeNewTime** response object, you can respond to the meeting by referencing its identifier, and propose a new meeting time to the organizer.</span></span> <span data-ttu-id="35571-132">Hier unterscheidet sich das **ProposeNewTime** -Antwortobjekt von dem typischen Antwortobjekt Muster darin, dass Sie nicht mit einem **ProposeNewTime** -Antwortobjekt Antworten.</span><span class="sxs-lookup"><span data-stu-id="35571-132">This is where the **ProposeNewTime** response object is different than the typical response object pattern in that you don't respond with a **ProposeNewTime** response object.</span></span> <span data-ttu-id="35571-133">Sie verwenden eines der anderen Besprechungsantwort Objekte wie **AcceptItem**, **TentativelyAcceptItem**oder **DeclineItem**, um eine neue Besprechung vorzuschlagen.</span><span class="sxs-lookup"><span data-stu-id="35571-133">You use one of the other meeting response objects, such as **AcceptItem**, **TentativelyAcceptItem**, or **DeclineItem**, to propose a new meeting.</span></span> <span data-ttu-id="35571-134">In diesem Beispiel wird das **AcceptItem** -Antwortobjekt verwendet.</span><span class="sxs-lookup"><span data-stu-id="35571-134">This example uses the **AcceptItem** response object.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
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

<span data-ttu-id="35571-135">Die Antwort auf diese Anforderung enthält den Bezeichner des Kalenderelements, das dem Kalender des Teilnehmers hinzugefügt wurde, und eine Kopie der Besprechungsanfrage, die im Ordner Gelöschte Elemente des Teilnehmers eingefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="35571-135">The response to this request contains the identifier of the calendar item that was added to the attendee's calendar and a copy of the meeting request that was placed in the attendee's Deleted Items folder.</span></span> <span data-ttu-id="35571-136">Die Antwortnachricht mit dem neuen Zeitvorschlag wurde auch im Ordner "Gesendete Elemente" des Teilnehmers gespeichert (Sie müssen die Antwortnachricht für die Besprechung finden, damit ein Handle darauf abgerufen wird).</span><span class="sxs-lookup"><span data-stu-id="35571-136">The response message with the new time proposal was also saved in the attendee's Sent Items folder (you will need to find the meeting response message to get a handle on it).</span></span>
  
```XML
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" 
                         MinorVersion="0" 
                         MajorBuildNumber="815" 
                         MinorBuildNumber="6" 
                         Version="V2_7" 
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:CreateItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="35571-137">Der Organisator erhält eine [MeetingResponse](https://msdn.microsoft.com/library/9f798e79-dafd-4d4d-9967-95fd8e5c0502%28Office.15%29.aspx) -Nachricht, wenn der Teilnehmer mit einer vorgeschlagenen neuen Besprechungszeit antwortet.</span><span class="sxs-lookup"><span data-stu-id="35571-137">The organizer will receive a [MeetingResponse](https://msdn.microsoft.com/library/9f798e79-dafd-4d4d-9967-95fd8e5c0502%28Office.15%29.aspx) message when the attendee responds with a proposed new meeting time.</span></span> <span data-ttu-id="35571-138">Die **MeetingResponse** -Nachricht enthält die vorgeschlagene neue Start Zeit für die Besprechung und die Endzeit sowie den Bezeichner des zugeordneten Kalenderelements im Kalender des Organisators.</span><span class="sxs-lookup"><span data-stu-id="35571-138">The **MeetingResponse** message contains the proposed new meeting start time and end time, and the identifier of the associated calendar item in the organizer's calendar.</span></span> <span data-ttu-id="35571-139">Der Organisator kann diese Informationen verwenden, um das vorhandene Kalenderelement für die Besprechung zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="35571-139">The organizer can use that information to update their existing calendar item for the meeting.</span></span> <span data-ttu-id="35571-140">Im folgenden finden Sie den Workflow für den Organisator, der auf eine **MeetingResponse** -Nachricht antwortet, die eine neue Besprechungszeit vorschlägt:</span><span class="sxs-lookup"><span data-stu-id="35571-140">The following is the workflow for the organizer to respond to a **MeetingResponse** message that proposes a new meeting time:</span></span> 
  
1. <span data-ttu-id="35571-141">Bestimmen Sie, ob die **ProposedStart** -oder **ProposedEnd** -Elemente in der **MeetingResponse**festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="35571-141">Determine whether the **ProposedStart** or **ProposedEnd** elements have been set in the **MeetingResponse**.</span></span> <span data-ttu-id="35571-142">Wenn dies der Fall ist, fahren Sie mit Schritt 2 fort.</span><span class="sxs-lookup"><span data-stu-id="35571-142">If so, go to step 2.</span></span> <span data-ttu-id="35571-143">Wenn dies nicht der Fall ist, gibt die **MeetingResponse** -Nachricht nur an, ob der Teilnehmer die Besprechung akzeptiert, mit Vorbehalt angenommen oder abgelehnt hat.</span><span class="sxs-lookup"><span data-stu-id="35571-143">If not, the **MeetingResponse** message only indicates whether the attendee has accepted, tentatively accepted, or declined the meeting.</span></span> 
    
2. <span data-ttu-id="35571-144">Abrufen des vorhandenen Kalenderelements des Organisators für die Besprechung mithilfe der EWS-ID, die im **AssociatedCalendarItemId** -Element zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="35571-144">Get the organizer's existing calendar item for the meeting by using the EWS identifier returned in the **AssociatedCalendarItemId** element.</span></span> 
    
3. <span data-ttu-id="35571-145">Vergleichen Sie die ursprüngliche Anfangs-und Endzeit mit der vorgeschlagenen neuen Besprechungszeit.</span><span class="sxs-lookup"><span data-stu-id="35571-145">Compare the original start and end time with the proposed new meeting time.</span></span> <span data-ttu-id="35571-146">Wenn die vorgeschlagene neue Besprechungszeit für den Organisator akzeptabel ist, fahren Sie mit Schritt 4 fort.</span><span class="sxs-lookup"><span data-stu-id="35571-146">If the proposed new meeting time is acceptable to the organizer, go to step 4.</span></span> <span data-ttu-id="35571-147">Andernfalls kann der Besprechungsorganisator entweder die vorgeschlagene Besprechungszeit ignorieren oder eine e-Mail-Antwort an den Teilnehmer senden, der die neue Besprechungszeit vorgeschlagen hat.</span><span class="sxs-lookup"><span data-stu-id="35571-147">Otherwise, the meeting organizer can either ignore the proposed meeting time, or send an email response to the attendee that proposed the new meeting time.</span></span>
    
4. <span data-ttu-id="35571-148">Optional Führen Sie einen [GetUserAvailability](https://msdn.microsoft.com/library/8da17226-5d3a-4525-9ffa-d83730f47bb1%28Office.15%29.aspx) -EWS-Vorgangsaufruf aus, um herauszufinden, ob die vorgeschlagene Zeit für alle Teilnehmer, einschließlich Raum-und Ressourcenpostfächern funktionieren soll.</span><span class="sxs-lookup"><span data-stu-id="35571-148">(Optional) Perform a [GetUserAvailability](https://msdn.microsoft.com/library/8da17226-5d3a-4525-9ffa-d83730f47bb1%28Office.15%29.aspx) EWS operation call to find out whether the proposed time will work for all attendees, including room and resource mailboxes.</span></span> <span data-ttu-id="35571-149">(Sie können dazu auch die verwaltete EWS-API-Methode [Datei "ExchangeService. GetUserAvailability](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.getuseravailability%28v=exchg.80%29.aspx) verwenden.)</span><span class="sxs-lookup"><span data-stu-id="35571-149">(You can also use the [ExchangeService.GetUserAvailability](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.getuseravailability%28v=exchg.80%29.aspx) EWS Managed API method to do this.)</span></span> 
    
5. <span data-ttu-id="35571-150">Der Organisator kann dann seine Besprechung mit den neuen vorgeschlagenen Besprechungszeiten aktualisieren und die Updates an alle Teilnehmer mit dem [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) -EWS-Vorgang (oder der [Termin. Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx) verwaltete EWS-API-Methode) senden.</span><span class="sxs-lookup"><span data-stu-id="35571-150">The organizer can then update their meeting with the new proposed meeting times and send the updates to all attendees by using the [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) EWS operation (or the [Appointment.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.update%28v=exchg.80%29.aspx) EWS Managed API method).</span></span> 
    
<span data-ttu-id="35571-151">In der folgenden Abbildung ist der Prozess dargestellt, der zwischen dem Besprechungsorganisator, dem Teilnehmer und dem Exchange-Server stattfindet, der die EWS-Anrufe verarbeitet hat.</span><span class="sxs-lookup"><span data-stu-id="35571-151">The following figure shows the process that occurs between the meeting organizer, the attendee, and the Exchange server that handled the EWS calls.</span></span>
  
<span data-ttu-id="35571-152">**Abbildung 1. Prozess für das vorschlagen einer neuen Besprechungszeit**</span><span class="sxs-lookup"><span data-stu-id="35571-152">**Figure 1. Process for proposing a new meeting time**</span></span>

![In der Abbildung wird der Workflow zwischen dem Organisator, Exchange und einem Teilnehmer dargestellt, wenn eine neue Besprechungszeit vorgeschlagen wird. Wenn der Organisator neue Vorschläge für Besprechungen zulässt, kann ein Teilnehmer eine neue Besprechungszeit mit einem Antwortobjekt vorschlagen.](media/Ex_ProposeNewMeetingTime.png)
  
## <a name="version-differences"></a><span data-ttu-id="35571-155">Versionsunterschiede</span><span class="sxs-lookup"><span data-stu-id="35571-155">Version differences</span></span>
<span data-ttu-id="35571-156"><a name="bk_Behavior"> </a></span><span class="sxs-lookup"><span data-stu-id="35571-156"><a name="bk_Behavior"> </a></span></span>

<span data-ttu-id="35571-157">Das Feature "neue Zeit vorschlagen" wurde in Exchange Build Version 15.00.0800.007 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="35571-157">The propose new time feature was introduced in Exchange build version 15.00.0800.007.</span></span> <span data-ttu-id="35571-158">In früheren Versionen von Exchange müssen Benutzer von EWS-Anwendungen eine separate e-Mail an den Besprechungsorganisator senden, um eine andere Besprechungszeit anzufordern.</span><span class="sxs-lookup"><span data-stu-id="35571-158">In earlier versions of Exchange, EWS application users have to send a separate email to the meeting organizer to request a different meeting time.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="35571-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="35571-159">See also</span></span>


- [<span data-ttu-id="35571-160">Kalender und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="35571-160">Calendars and EWS in Exchange</span></span>](calendars-and-ews-in-exchange.md)
    
- [<span data-ttu-id="35571-161">Erstellen von Terminen und Besprechungen mithilfe von EWS in Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="35571-161">Create appointments and meetings by using EWS in Exchange 2013</span></span>](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)
    
- [<span data-ttu-id="35571-162">Abrufen von Terminen und Besprechungen mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="35571-162">Get appointments and meetings by using EWS in Exchange</span></span>](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="35571-163">Aktualisieren von Terminen und Besprechungen mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="35571-163">Update appointments and meetings by using EWS in Exchange</span></span>](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="35571-164">Löschen von Terminen und Absagen von Besprechungen mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="35571-164">Delete appointments and cancel meetings by using EWS in Exchange</span></span>](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)
    

