---
title: GetStreamingEvents-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetStreamingEvents
api_type:
- schema
ms.assetid: 8da95423-72bc-4034-90a8-162eedcd059b
description: Hier finden Sie Informationen über die GetStreamingEvents EWS Vorgang.
ms.openlocfilehash: 0e93be7b14cb1ca6a2a9821b016f7bdc0e8d7772
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19829673"
---
# <a name="getstreamingevents-operation"></a><span data-ttu-id="7f563-103">GetStreamingEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="7f563-103">GetStreamingEvents operation</span></span>

<span data-ttu-id="7f563-104">Hier finden Sie Informationen zum **GetStreamingEvents** EWS-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="7f563-104">Find information about the **GetStreamingEvents** EWS operation.</span></span> 
  
<span data-ttu-id="7f563-105">Der Vorgang **GetStreamingEvents** wird vom streaming-Abonnement-Clients zur Benachrichtigungen anfordern, vom Client Access-Server verwendet.</span><span class="sxs-lookup"><span data-stu-id="7f563-105">The **GetStreamingEvents** operation is used by streaming subscription clients to request notifications from the Client Access server.</span></span> <span data-ttu-id="7f563-106">Die Antwort **GetStreamingEvents** gibt ein Array von Elementen und Ereignisse, die in einem Postfach seit dem letzten die Benachrichtigung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="7f563-106">The **GetStreamingEvents** response returns an array of items and events that have occurred in a mailbox since the last the notification.</span></span> 
  
## <a name="getstreamingevents-request-example"></a><span data-ttu-id="7f563-107">Anforderungsbeispiel GetStreamingEvents</span><span class="sxs-lookup"><span data-stu-id="7f563-107">GetStreamingEvents request example</span></span>

### <a name="description"></a><span data-ttu-id="7f563-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7f563-108">Description</span></span>

<span data-ttu-id="7f563-109">Im folgenden Beispiel wird eine Operation **GetStreamingEvents** veranschaulicht, wie zum Anfordern der Ereignisse und Elemente, die mit einem Abonnement verknüpft sind, die durch die Abonnement-ID identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="7f563-109">The following example of a **GetStreamingEvents** operation shows how to request the events and items that are associated with a subscription that is identified by the subscription identifier.</span></span> 
  
### <a name="code"></a><span data-ttu-id="7f563-110">Code</span><span class="sxs-lookup"><span data-stu-id="7f563-110">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
  xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Body>
    <GetStreamingEvents xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <SubscriptionId>f6bc657d-dde1-4f94-952d-143b95d6483d</SubscriptionId>
      <ConnectionTimeout>30</ConnectionTimeout>
    </GetStreamingEvents>
  </soap:Body>
</soap:Envelope>
```

### <a name="getstreamingevents-request-elements"></a><span data-ttu-id="7f563-111">GetStreamingEvents Anforderung Elemente</span><span class="sxs-lookup"><span data-stu-id="7f563-111">GetStreamingEvents request elements</span></span>

<span data-ttu-id="7f563-112">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="7f563-112">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="7f563-113">GetStreamingEvents</span><span class="sxs-lookup"><span data-stu-id="7f563-113">GetStreamingEvents</span></span>](getstreamingevents.md)
    
- [<span data-ttu-id="7f563-114">SubscriptionId (GetStreamingEvents)</span><span class="sxs-lookup"><span data-stu-id="7f563-114">SubscriptionId (GetStreamingEvents)</span></span>](subscriptionid-getstreamingevents.md)
    
- [<span data-ttu-id="7f563-115">ConnectionTimeout</span><span class="sxs-lookup"><span data-stu-id="7f563-115">ConnectionTimeout</span></span>](connectiontimeout.md)
    
## <a name="successful-getstreamingevents-response-example"></a><span data-ttu-id="7f563-116">Erfolgreiche GetStreamingEvents antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="7f563-116">Successful GetStreamingEvents response example</span></span>

### <a name="description"></a><span data-ttu-id="7f563-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7f563-117">Description</span></span>

<span data-ttu-id="7f563-118">Das folgende Beispiel einer Antwort **GetStreamingEvents** zeigt die Benachrichtigungen, die an den Client gesendet werden, wenn eine neue e-Mail-Nachricht empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="7f563-118">The following example of a **GetStreamingEvents** response shows the notifications that are sent to the client when a new email message is received.</span></span> <span data-ttu-id="7f563-119">Sie enthält Benachrichtigungen für die folgenden Ereignisse: CreatedEvent NewMail und ModifiedEvent.</span><span class="sxs-lookup"><span data-stu-id="7f563-119">It includes notifications for the following events: CreatedEvent, NewMail, and ModifiedEvent.</span></span> 
  
### <a name="code"></a><span data-ttu-id="7f563-120">Code</span><span class="sxs-lookup"><span data-stu-id="7f563-120">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Header xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <ServerVersionInfo xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" MajorVersion="15" MinorVersion="0" MajorBuildNumber="775" MinorBuildNumber="7" Version="V2_4" xmlns="http://schemas.microsoft.com/exchange/services/2006/types" />
</soap:Header>
<soap:Body xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <m:GetStreamingEventsResponse xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
    <m:ResponseMessages>
      <m:GetStreamingEventsResponseMessage ResponseClass="Success">
        <m:ResponseCode>NoError</m:ResponseCode>
        <m:Notifications>
          <m:Notification>
            <t:SubscriptionId>f6bc657d-dde1-4f94-952d-143b95d6483d</t:SubscriptionId>
            <t:CreatedEvent>
              <t:TimeStamp>2013-09-16T04:31:29Z</t:TimeStamp>
              <t:ItemId Id="AAMkADkzNjJjODUzLWZhMDMtNDVkMS05ZDdjLWVmMDlkYjQ1Zjc4MwBGAAAAAABSSWVKrmGUTJE+MVIvofglBwDZGACZQpSgSpyNkexYe2b7AAAAAAENAADZGACZQpSgSpyNkexYe2b7AAANGFYwAAA=" ChangeKey="CQAAAA==" />
              <t:ParentFolderId Id="AQMkADkzNjJjODUzLWZhMDMtNDVkMS05ZDdjLWVmMDlkYjQ1Zjc4MwAuAAADUkllSq5hlEyRPjFSL6H4JQEA2RgAmUKUoEqcjZHsWHtm+wAAAgENAAAA" ChangeKey="AQAAAA==" />
            </t:CreatedEvent>
            <t:NewMailEvent>
              <t:TimeStamp>2013-09-16T04:31:29Z</t:TimeStamp>
              <t:ItemId Id="AAMkADkzNjJjODUzLWZhMDMtNDVkMS05ZDdjLWVmMDlkYjQ1Zjc4MwBGAAAAAABSSWVKrmGUTJE+MVIvofglBwDZGACZQpSgSpyNkexYe2b7AAAAAAENAADZGACZQpSgSpyNkexYe2b7AAANGFYwAAA=" ChangeKey="CQAAAA==" />
              <t:ParentFolderId Id="AQMkADkzNjJjODUzLWZhMDMtNDVkMS05ZDdjLWVmMDlkYjQ1Zjc4MwAuAAADUkllSq5hlEyRPjFSL6H4JQEA2RgAmUKUoEqcjZHsWHtm+wAAAgENAAAA" ChangeKey="AQAAAA==" />
            </t:NewMailEvent>
            <t:ModifiedEvent>
              <t:TimeStamp>2013-09-16T04:31:29Z</t:TimeStamp>
              <t:FolderId Id="AQMkADkzNjJjODUzLWZhMDMtNDVkMS05ZDdjLWVmMDlkYjQ1Zjc4MwAuAAADUkllSq5hlEyRPjFSL6H4JQEA2RgAmUKUoEqcjZHsWHtm+wAAAgENAAAA" ChangeKey="AQAAAA==" />
              <t:ParentFolderId Id="AQMkADkzNjJjODUzLWZhMDMtNDVkMS05ZDdjLWVmMDlkYjQ1Zjc4MwAuAAADUkllSq5hlEyRPjFSL6H4JQEA2RgAmUKUoEqcjZHsWHtm+wAAAgEJAAAA" ChangeKey="AQAAAA==" />
              <t:UnreadCount>1</t:UnreadCount>
            </t:ModifiedEvent>
          </m:Notification>
        </m:Notifications>
      </m:GetStreamingEventsResponseMessage>
    </m:ResponseMessages>
  </m:GetStreamingEventsResponse>
</soap:Body>
```

### <a name="getstreamingevents-response-elements"></a><span data-ttu-id="7f563-121">GetStreamingEvents Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="7f563-121">GetStreamingEvents response elements</span></span>

<span data-ttu-id="7f563-122">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="7f563-122">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="7f563-123">GetStreamingEventsResponse</span><span class="sxs-lookup"><span data-stu-id="7f563-123">GetStreamingEventsResponse</span></span>](getstreamingeventsresponse.md)
    
- [<span data-ttu-id="7f563-124">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="7f563-124">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="7f563-125">GetStreamingEventsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="7f563-125">GetStreamingEventsResponseMessage</span></span>](getstreamingeventsresponsemessage.md)
    
- [<span data-ttu-id="7f563-126">NotesFolderPermissionLevel</span><span class="sxs-lookup"><span data-stu-id="7f563-126">NotesFolderPermissionLevel</span></span>](notesfolderpermissionlevel.md)
    
- [<span data-ttu-id="7f563-127">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="7f563-127">Notification</span></span>](notification-ex15websvcsotherref.md)
    
- [<span data-ttu-id="7f563-128">SubscriptionId (GetStreamingEvents)</span><span class="sxs-lookup"><span data-stu-id="7f563-128">SubscriptionId (GetStreamingEvents)</span></span>](subscriptionid-getstreamingevents.md)
    
<span data-ttu-id="7f563-129">Wenn andere Optionen für die Antwortnachricht des Vorgangs **GetStreamingEvents** suchen möchten, verwenden Sie die Schemahierarchie.</span><span class="sxs-lookup"><span data-stu-id="7f563-129">To find other options for the response message of the **GetStreamingEvents** operation, explore the schema hierarchy.</span></span> <span data-ttu-id="7f563-130">Starten Sie die [Benachrichtigung](notification-ex15websvcsotherref.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="7f563-130">Start at the [Notification](notification-ex15websvcsotherref.md) element.</span></span> 
  
## <a name="getstreamingevents-error-response-example"></a><span data-ttu-id="7f563-131">GetStreamingEvents Fehler antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="7f563-131">GetStreamingEvents error response example</span></span>

### <a name="description"></a><span data-ttu-id="7f563-132">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7f563-132">Description</span></span>

<span data-ttu-id="7f563-133">Das folgende Beispiel zeigt eine Fehlerantwort an eine **GetStreamingEvents** -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="7f563-133">The following example shows an error response to a **GetStreamingEvents** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="7f563-134">Code</span><span class="sxs-lookup"><span data-stu-id="7f563-134">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetStreamingEventsResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                       xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:GetStreamingEventsResponseMessage ResponseClass="Error">
        <m:MessageText></m:MessageText>
        <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        <m:ResponseCode>ErrorInvalidSubscription</m:ResponseCode>
        <m:ConnectionStatus>Closed</m:ConnectionStatus>
      </m:ResponseMessages>
    </GetStreamingEventsResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="remarks"></a><span data-ttu-id="7f563-135">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7f563-135">Remarks</span></span>

<span data-ttu-id="7f563-136">Bei der Verarbeitung einer Anforderung **GetStreamingEvents** führt der Clientzugriffs-Server die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="7f563-136">When processing a **GetStreamingEvents** request, the Client Access server performs the following steps:</span></span> 
  
1. <span data-ttu-id="7f563-137">Die [SubscriptionId (GetStreamingEvents)](subscriptionid-getstreamingevents.md) der Anforderung wird bestätigt, um ein gültiges Abonnement sein, das auf dem Client Access Server gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="7f563-137">The [SubscriptionId (GetStreamingEvents)](subscriptionid-getstreamingevents.md) of the request is confirmed to be a valid subscription that is hosted on the Client Access server.</span></span> <span data-ttu-id="7f563-138">Wenn sie nicht der Fall ist, schlägt der **GetStreamingEvents** -Aufruf.</span><span class="sxs-lookup"><span data-stu-id="7f563-138">If it is not, the **GetStreamingEvents** call fails.</span></span> 
    
2. <span data-ttu-id="7f563-139">Die SMTP-Adresse des authentifizierten Benutzers für die Anforderung wird überprüft, um Identitätswechsel Rechte verfügen.</span><span class="sxs-lookup"><span data-stu-id="7f563-139">The SMTP address of the authenticated user for the request is validated to have impersonation rights.</span></span> <span data-ttu-id="7f563-140">Ist dies nicht der Fall ist, schlägt die Anforderung **GetStreamingEvents** .</span><span class="sxs-lookup"><span data-stu-id="7f563-140">If they do not, the **GetStreamingEvents** request fails.</span></span> 
    
3. <span data-ttu-id="7f563-141">Die Abonnement-Warteschlange abgefragt wird für Ereignisse, die darauf warten, an den Client gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="7f563-141">The subscription queue is queried for events that are waiting to be sent to the client.</span></span> <span data-ttu-id="7f563-142">Wenn die Warteschlange nicht leer ist, werden die ersten 50 Ereignisse aus der Warteschlange aus der Warteschlange abgerufen und in eine Benachrichtigung codiert.</span><span class="sxs-lookup"><span data-stu-id="7f563-142">If the queue is not empty, the first 50 events from the queue are pulled from the queue and encoded into a notification.</span></span>
    
4. <span data-ttu-id="7f563-143">Wenn keine Ereignisse in der Warteschlange gefunden werden, wird ein [StatusEvent](statusevent.md) generiert und in einer Benachrichtigungsantwort codiert.</span><span class="sxs-lookup"><span data-stu-id="7f563-143">If no events are found in the queue, a [StatusEvent](statusevent.md) is generated and encoded into a notification response.</span></span> 
    
5. <span data-ttu-id="7f563-144">Die Benachrichtigungsantwort wird an den Client zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7f563-144">The notification response is returned to the client.</span></span>
    
6. <span data-ttu-id="7f563-145">Die Ereignisse, die in der Benachrichtigung enthalten sind, werden aus der Warteschlange Abonnement entfernt und Client Access Server-Local letzte Wasserzeichen für das Abonnement festgelegt ist, können Sie dem Wasserzeichen des letzten-Ereignisses, das zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7f563-145">The events that are included in the notification are removed from the subscription queue and the Client Access server-local last watermark for the subscription is set to the watermark of the last event that is returned.</span></span>
    
7. <span data-ttu-id="7f563-146">Der Timeout-Zeitgeber für das Abonnement wird zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="7f563-146">The timeout timer for the subscription is reset.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7f563-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7f563-147">See also</span></span>



[<span data-ttu-id="7f563-148">Vorgang abonnieren</span><span class="sxs-lookup"><span data-stu-id="7f563-148">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="7f563-149">Vorgang des Kündigens von Abonnements</span><span class="sxs-lookup"><span data-stu-id="7f563-149">Unsubscribe operation</span></span>](unsubscribe-operation.md)

