---
title: GetEvents-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetEvents
api_type:
- schema
ms.assetid: f268efe5-9a1a-41a2-b6a6-51fcde7720a1
description: Der GetEvents-Vorgang wird von Pull-Abonnementclients verwendet, um Benachrichtigungen vom Client Zugriffsserver anzufordern. Die GetEvents-Vorgangs Antwort gibt ein Array von Elementen und Ereignissen zurück, die seit der letzten Benachrichtigung in einem Postfach aufgetreten sind.
ms.openlocfilehash: 9258fd003c242911866aa7abbca5eba2b9582223
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462514"
---
# <a name="getevents-operation"></a><span data-ttu-id="fb928-104">GetEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="fb928-104">GetEvents operation</span></span>

<span data-ttu-id="fb928-105">Der **GetEvents** -Vorgang wird von Pull-Abonnementclients verwendet, um Benachrichtigungen vom Client Zugriffsserver anzufordern.</span><span class="sxs-lookup"><span data-stu-id="fb928-105">The **GetEvents** operation is used by pull subscription clients to request notifications from the Client Access server.</span></span> <span data-ttu-id="fb928-106">Die **GetEvents** -Vorgangs Antwort gibt ein Array von Elementen und Ereignissen zurück, die seit der letzten Benachrichtigung in einem Postfach aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="fb928-106">The **GetEvents** operation response returns an array of items and events that have occurred in a mailbox since the last the notification.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="fb928-107">Durch den **DeleteUserConfiguration** -Vorgang wird ein Verschiebe Ereignis für das Ereignis Benachrichtigungssystem ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="fb928-107">The **DeleteUserConfiguration** operation will trigger a move event for the event notification system.</span></span> <span data-ttu-id="fb928-108">Das Benutzer Konfigurationsobjekt wird in den Papierkorb verschoben.</span><span class="sxs-lookup"><span data-stu-id="fb928-108">The user configuration object will be moved to the dumpster.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="fb928-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fb928-109">Remarks</span></span>

<span data-ttu-id="fb928-110">Änderungen an Kalenderelementen können zur Generierung von mehreren Ereignissen führen.</span><span class="sxs-lookup"><span data-stu-id="fb928-110">Changes to Calendar items may result in the generation of multiple events.</span></span> <span data-ttu-id="fb928-111">Diese Ereignisse sind das Ergebnis von temporären Elementen, die im Postfach erstellt werden, und frei/gebucht-Datenspeicherelemente, die im Rahmen normaler Kalender Vorgänge geändert wurden, oder beides.</span><span class="sxs-lookup"><span data-stu-id="fb928-111">These events are the result of temporary items being created in the mailbox, free/busy data storage items being changed as part of the normal Calendar operations, or both.</span></span> <span data-ttu-id="fb928-112">Ereignisse für die Elementklasse "IPM. SchedulePlus. freebusy. BinaryData "sollte von Webdienstclients ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="fb928-112">Events for item class "IPM.SchedulePlus.FreeBusy.BinaryData" should be ignored by Web service clients.</span></span> <span data-ttu-id="fb928-113">Diese temporären Elemente werden nach ihrer Erstellung gelöscht. Wenn also versucht wird, diese Elemente abzurufen, wird ein Fehler zurückgegeben, der besagt, dass das Element nicht gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="fb928-113">These temporary items are deleted after they are created; therefore, if an attempt is made to retrieve these items, an error will be returned that states that the item was not found.</span></span>
  
## <a name="getevents-request-example"></a><span data-ttu-id="fb928-114">GetEvents-Anforderungs Beispiel</span><span class="sxs-lookup"><span data-stu-id="fb928-114">GetEvents request example</span></span>

### <a name="description"></a><span data-ttu-id="fb928-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fb928-115">Description</span></span>

<span data-ttu-id="fb928-116">Im folgenden Beispiel wird gezeigt, wie die Ereignisse und Elemente angefordert werden, die einem Abonnement zugeordnet sind, das durch die Abonnement-ID und das Wasserzeichen identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="fb928-116">The following example shows how to request the events and items that are associated with a subscription that is identified by the subscription identifier and watermark.</span></span>
  
### <a name="code"></a><span data-ttu-id="fb928-117">Code</span><span class="sxs-lookup"><span data-stu-id="fb928-117">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetEvents xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <SubscriptionId>f6bc657d-dde1-4f94-952d-143b95d6483d</SubscriptionId>
      <Watermark>AAAAAMAGAAAAAAAAAQ==</Watermark>
    </GetEvents>
  </soap:Body>
</soap:Envelope>
```

### <a name="getevents-request-elements"></a><span data-ttu-id="fb928-118">GetEvents-anforderungselemente</span><span class="sxs-lookup"><span data-stu-id="fb928-118">GetEvents Request Elements</span></span>

<span data-ttu-id="fb928-119">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="fb928-119">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="fb928-120">GetEvents</span><span class="sxs-lookup"><span data-stu-id="fb928-120">GetEvents</span></span>](getevents.md)
    
- [<span data-ttu-id="fb928-121">Abonnement-Nr (GetEvents)</span><span class="sxs-lookup"><span data-stu-id="fb928-121">SubscriptionId (GetEvents)</span></span>](subscriptionid-getevents.md)
    
- [<span data-ttu-id="fb928-122">Watermark</span><span class="sxs-lookup"><span data-stu-id="fb928-122">Watermark</span></span>](watermark.md)
    
## <a name="successful-getevents-response-example"></a><span data-ttu-id="fb928-123">Erfolgreiches GetEvents-Antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="fb928-123">Successful GetEvents response example</span></span>

### <a name="description"></a><span data-ttu-id="fb928-124">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fb928-124">Description</span></span>

<span data-ttu-id="fb928-125">Das folgende Beispiel einer Antwort zeigt eine Benachrichtigung über das vorhanden sein zweier neuer e-Mail-Nachrichten, seit die letzte Benachrichtigungsanforderung an den Server gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="fb928-125">The following example of a response shows a notification of the existence of two new mail messages since the last notification request was sent to the server.</span></span>
  
### <a name="code"></a><span data-ttu-id="fb928-126">Code</span><span class="sxs-lookup"><span data-stu-id="fb928-126">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetEventsResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                       xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:GetEventsResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Notification>
            <t:SubscriptionId>f6bc657d-dde1-4f94-952d-143b95d6483d</t:SubscriptionId>
            <t:PreviousWatermark>AAAAAMAGAAAAAAAAAQ==</t:PreviousWatermark>
            <t:MoreEvents>false</t:MoreEvents>
            <t:NewMailEvent>
              <t:Watermark>AAAAAM4GAAAAAAAAAQ==</t:Watermark>
              <t:TimeStamp>2006-08-22T00:36:29Z</t:TimeStamp>
              <t:ItemId Id="AQApAHR" ChangeKey="CQAAAA==" />
              <t:ParentFolderId Id="AQApAH" ChangeKey="AQAAAA==" />
            </t:NewMailEvent>
            <t:NewMailEvent>
              <t:Watermark>AAAAAOQGAAAAAAAAAQ==</t:Watermark>
              <t:TimeStamp>2006-08-22T01:00:50Z</t:TimeStamp>
              <t:ItemId Id="AQApAHRw" ChangeKey="CQAAAA==" />
              <t:ParentFolderId Id="AQApAH" ChangeKey="AQAAAA==" />
            </t:NewMailEvent>
          </m:Notification>
        </m:GetEventsResponseMessage>
      </m:ResponseMessages>
    </GetEventsResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="fb928-127">Comments</span><span class="sxs-lookup"><span data-stu-id="fb928-127">Comments</span></span>

> [!NOTE]
> <span data-ttu-id="fb928-128">Die Element-und Ordner Bezeichner wurden verkürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="fb928-128">The item and folder identifiers have been shortened to preserve readability.</span></span> 
  
### <a name="getevents-response-elements"></a><span data-ttu-id="fb928-129">GetEvents-Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="fb928-129">GetEvents response elements</span></span>

<span data-ttu-id="fb928-130">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="fb928-130">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="fb928-131">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="fb928-131">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="fb928-132">GetEventsResponse</span><span class="sxs-lookup"><span data-stu-id="fb928-132">GetEventsResponse</span></span>](geteventsresponse.md)
    
- [<span data-ttu-id="fb928-133">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="fb928-133">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="fb928-134">GetEventsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="fb928-134">GetEventsResponseMessage</span></span>](geteventsresponsemessage.md)
    
- [<span data-ttu-id="fb928-135">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="fb928-135">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="fb928-136">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="fb928-136">Notification</span></span>](notification-ex15websvcsotherref.md)
    
- [<span data-ttu-id="fb928-137">Abonnement-Nr (GetEvents)</span><span class="sxs-lookup"><span data-stu-id="fb928-137">SubscriptionId (GetEvents)</span></span>](subscriptionid-getevents.md)
    
- [<span data-ttu-id="fb928-138">PreviousWatermark</span><span class="sxs-lookup"><span data-stu-id="fb928-138">PreviousWatermark</span></span>](previouswatermark.md)
    
- [<span data-ttu-id="fb928-139">MoreEvents</span><span class="sxs-lookup"><span data-stu-id="fb928-139">MoreEvents</span></span>](moreevents.md)
    
- [<span data-ttu-id="fb928-140">NewMailEvent</span><span class="sxs-lookup"><span data-stu-id="fb928-140">NewMailEvent</span></span>](newmailevent.md)
    
- [<span data-ttu-id="fb928-141">Watermark</span><span class="sxs-lookup"><span data-stu-id="fb928-141">Watermark</span></span>](watermark.md)
    
- [<span data-ttu-id="fb928-142">Timestamp</span><span class="sxs-lookup"><span data-stu-id="fb928-142">TimeStamp</span></span>](timestamp.md)
    
- [<span data-ttu-id="fb928-143">ItemId</span><span class="sxs-lookup"><span data-stu-id="fb928-143">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="fb928-144">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="fb928-144">ParentFolderId</span></span>](parentfolderid.md)
    
<span data-ttu-id="fb928-145">Um andere Optionen für die Antwortnachricht des **GetEvents** -Vorgangs zu finden, erkunden Sie die Schemahierarchie.</span><span class="sxs-lookup"><span data-stu-id="fb928-145">To find other options for the response message of the **GetEvents** operation, explore the schema hierarchy.</span></span> <span data-ttu-id="fb928-146">Beginnen Sie mit dem [Benachrichtigungs](notification-ex15websvcsotherref.md) Element.</span><span class="sxs-lookup"><span data-stu-id="fb928-146">Start at the [Notification](notification-ex15websvcsotherref.md) element.</span></span> 
  
## <a name="getevents-error-response-example"></a><span data-ttu-id="fb928-147">GetEvents-Fehlerantwort (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="fb928-147">GetEvents Error response example</span></span>

### <a name="description"></a><span data-ttu-id="fb928-148">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fb928-148">Description</span></span>

<span data-ttu-id="fb928-149">Das folgende Beispiel zeigt eine Fehlerantwort auf eine **GetEvents** -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="fb928-149">The following example shows an error response to a **GetEvents** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="fb928-150">Code</span><span class="sxs-lookup"><span data-stu-id="fb928-150">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
                 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                 xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetEventsResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:GetEventsResponseMessage ResponseClass="Error">
          <m:MessageText>Access is denied. Only the subscription owner may access the subscription.</m:MessageText>
          <m:ResponseCode>ErrorSubscriptionAccessDenied</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:GetEventsResponseMessage>
      </m:ResponseMessages>
    </GetEventsResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="remarks"></a><span data-ttu-id="fb928-151">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fb928-151">Remarks</span></span>

<span data-ttu-id="fb928-152">Bei der Verarbeitung einer **GetEvents** -Anforderung führt der Client Zugriffsserver die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="fb928-152">When processing a **GetEvents** request, the Client Access server performs the following steps:</span></span> 
  
1. <span data-ttu-id="fb928-153">Die Abonnement-Nr der Anforderung wird als gültiges Abonnement bestätigt, das auf dem Client Zugriffsserver gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="fb928-153">The SubscriptionID of the request is confirmed to be a valid subscription that is hosted on the Client Access server.</span></span> <span data-ttu-id="fb928-154">Wenn dies nicht der Fall ist, tritt beim **GetEvents** -Aufruf ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="fb928-154">If it is not, the **GetEvents** call fails.</span></span> 
    
2. <span data-ttu-id="fb928-155">Die SMTP-Adresse des authentifizierten Benutzers für die Anforderung wird mit der SMTP-Adresse des Benutzers verglichen, der das Abonnement erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="fb928-155">The SMTP address of the authenticated user for the request is compared to the SMTP address of the user who created the subscription.</span></span> <span data-ttu-id="fb928-156">Wenn Sie nicht übereinstimmen, schlägt die **GetEvents** -Anforderung fehl.</span><span class="sxs-lookup"><span data-stu-id="fb928-156">If they do not match, the **GetEvents** request fails.</span></span> 
    
3. <span data-ttu-id="fb928-157">Die Abonnement Warteschlange wird für Ereignisse abgefragt, die darauf warten, an den Client gesendet zu werden.</span><span class="sxs-lookup"><span data-stu-id="fb928-157">The subscription queue is queried for events that are waiting to be sent to the client.</span></span> <span data-ttu-id="fb928-158">Wenn die Warteschlange nicht leer ist, werden die ersten 50-Ereignisse aus der Warteschlange aus der Warteschlange gezogen und in eine Benachrichtigung codiert.</span><span class="sxs-lookup"><span data-stu-id="fb928-158">If the queue is not empty, the first 50 events from the queue are pulled from the queue and encoded into a notification.</span></span>
    
4. <span data-ttu-id="fb928-159">Wenn in der Warteschlange keine Ereignisse gefunden werden, wird ein StatusEvent generiert und in einer Benachrichtigungsantwort codiert.</span><span class="sxs-lookup"><span data-stu-id="fb928-159">If no events are found in the queue, a StatusEvent is generated and encoded into a notification response.</span></span>
    
5. <span data-ttu-id="fb928-160">Die Benachrichtigungsantwort wird an den Client zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fb928-160">The notification response is returned to the client.</span></span>
    
6. <span data-ttu-id="fb928-161">Die Ereignisse, die in der Benachrichtigung enthalten sind, werden aus der Abonnement Warteschlange entfernt, und der lokale Client Zugriffsserver-letzte Wasserzeichen für das Abonnement wird auf das Wasserzeichen des letzten zurückgegebenen Ereignisses festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fb928-161">The events that are included in the notification are removed from the subscription queue and the Client Access server local last watermark for the subscription is set to the watermark of the last event that is returned.</span></span>
    
7. <span data-ttu-id="fb928-162">Der Timeout-Zeitgeber für das Abonnement wird zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="fb928-162">The timeout timer for the subscription is reset.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fb928-163">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fb928-163">See also</span></span>



[<span data-ttu-id="fb928-164">Vorgang abonnieren</span><span class="sxs-lookup"><span data-stu-id="fb928-164">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="fb928-165">Vorgang des Kündigens von Abonnements</span><span class="sxs-lookup"><span data-stu-id="fb928-165">Unsubscribe operation</span></span>](unsubscribe-operation.md)


[<span data-ttu-id="fb928-166">Verwenden von Pullabonnements</span><span class="sxs-lookup"><span data-stu-id="fb928-166">Using Pull Subscriptions</span></span>](https://msdn.microsoft.com/library/f956bc0e-2b25-4613-966b-54c65456897c%28Office.15%29.aspx)

