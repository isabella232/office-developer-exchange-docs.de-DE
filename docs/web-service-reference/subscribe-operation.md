---
title: Vorgang abonnieren
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Subscribe
api_type:
- schema
ms.assetid: f17c3d08-c79e-41f1-ba31-6e41e7aafd87
description: Der Subscribe-Vorgang wird verwendet, um Clientanwendungen für Push-oder Pull-Benachrichtigungen zu abonnieren. Es ist wichtig zu beachten, dass die Struktur der Anforderungsnachrichten und-Antworten je nach Typ der Ereignisbenachrichtigung unterschiedlich ist.
ms.openlocfilehash: c40e0e434f698c6535ff5d03fd4d45a453959dd6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/01/2020
ms.locfileid: "44467046"
---
# <a name="subscribe-operation"></a><span data-ttu-id="575d1-104">Vorgang abonnieren</span><span class="sxs-lookup"><span data-stu-id="575d1-104">Subscribe operation</span></span>

<span data-ttu-id="575d1-105">Der Subscribe-Vorgang wird verwendet, um Clientanwendungen für Push-oder Pull-Benachrichtigungen zu abonnieren.</span><span class="sxs-lookup"><span data-stu-id="575d1-105">The Subscribe operation is used to subscribe client applications to either push or pull notifications.</span></span> <span data-ttu-id="575d1-106">Es ist wichtig zu beachten, dass die Struktur der Anforderungsnachrichten und-Antworten je nach Typ der Ereignisbenachrichtigung unterschiedlich ist.</span><span class="sxs-lookup"><span data-stu-id="575d1-106">It is important to be aware that the structure of the request messages and responses is different depending on the type of event notification.</span></span> 
  
## <a name="pull-subscription-subscribe-request-example"></a><span data-ttu-id="575d1-107">Subscribe-Abonnement-Anforderungs Beispiel für Pullabonnements</span><span class="sxs-lookup"><span data-stu-id="575d1-107">Pull Subscription Subscribe request example</span></span>

### <a name="description"></a><span data-ttu-id="575d1-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="575d1-108">Description</span></span>

<span data-ttu-id="575d1-109">Das folgende Codebeispiel zeigt, wie Sie ein Ereignis Benachrichtigungsabonnement für Pullabonnements abonnieren.</span><span class="sxs-lookup"><span data-stu-id="575d1-109">The following code example shows how to subscribe to a pull event notification subscription.</span></span> <span data-ttu-id="575d1-110">Das Abonnement informiert die Clientanwendung, wenn dem Posteingang neue e-Mails hinzugefügt werden und wenn ein Element aus dem Posteingang gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="575d1-110">The subscription informs the client application if new mail is added to the Inbox and if an item is deleted from the Inbox.</span></span> <span data-ttu-id="575d1-111">Das Abonnement hat einen Timeout, wenn der Client nicht innerhalb von zehn Minuten Informationen zu Ereignissen anfordert.</span><span class="sxs-lookup"><span data-stu-id="575d1-111">The subscription will time out if the client does not request information about events within ten minutes.</span></span> <span data-ttu-id="575d1-112">Wenn das Abonnement abläuft, muss ein neues Abonnement eingerichtet werden, um weiterhin Benachrichtigungen anzufordern.</span><span class="sxs-lookup"><span data-stu-id="575d1-112">If the subscription expires, a new subscription must be established to continue to request notifications.</span></span>
  
### <a name="code"></a><span data-ttu-id="575d1-113">Code</span><span class="sxs-lookup"><span data-stu-id="575d1-113">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <Subscribe xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <PullSubscriptionRequest>
        <t:FolderIds>
          <t:DistinguishedFolderId Id="inbox"/>
        </t:FolderIds>
        <t:EventTypes>
          <t:EventType>NewMailEvent</t:EventType>
          <t:EventType>DeletedEvent</t:EventType>
        </t:EventTypes>
        <t:Timeout>10</t:Timeout>
      </PullSubscriptionRequest>
    </Subscribe>
  </soap:Body>
</soap:Envelope>
```

### <a name="pull-subscription-subscribe-request-elements"></a><span data-ttu-id="575d1-114">Subscribe-Abonnement anforderungselemente abrufen</span><span class="sxs-lookup"><span data-stu-id="575d1-114">Pull Subscription Subscribe Request Elements</span></span>

<span data-ttu-id="575d1-115">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="575d1-115">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="575d1-116">Abonnieren</span><span class="sxs-lookup"><span data-stu-id="575d1-116">Subscribe</span></span>](subscribe.md)
    
- [<span data-ttu-id="575d1-117">PullSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="575d1-117">PullSubscriptionRequest</span></span>](pullsubscriptionrequest.md)
    
- [<span data-ttu-id="575d1-118">FolderIds</span><span class="sxs-lookup"><span data-stu-id="575d1-118">FolderIds</span></span>](folderids.md)
    
- [<span data-ttu-id="575d1-119">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="575d1-119">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="575d1-120">EventTypes</span><span class="sxs-lookup"><span data-stu-id="575d1-120">EventTypes</span></span>](eventtypes.md)
    
- [<span data-ttu-id="575d1-121">EventType</span><span class="sxs-lookup"><span data-stu-id="575d1-121">EventType</span></span>](eventtype.md)
    
- [<span data-ttu-id="575d1-122">Timeout</span><span class="sxs-lookup"><span data-stu-id="575d1-122">Timeout</span></span>](timeout.md)
    
<span data-ttu-id="575d1-123">Um andere Optionen für die Anforderungsnachricht des Subscribe-Vorgangs zu finden, erkunden Sie die Schemahierarchie.</span><span class="sxs-lookup"><span data-stu-id="575d1-123">To find other options for the request message of the Subscribe operation, explore the schema hierarchy.</span></span> <span data-ttu-id="575d1-124">Beginnen Sie mit dem [PullSubscriptionRequest](pullsubscriptionrequest.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="575d1-124">Start at the [PullSubscriptionRequest](pullsubscriptionrequest.md) element.</span></span> 
  
## <a name="successful-pull-subscription-subscribe-response-example"></a><span data-ttu-id="575d1-125">Beispiel für eine erfolgreiche Abonnement Antwort für Pullabonnements</span><span class="sxs-lookup"><span data-stu-id="575d1-125">Successful Pull Subscription Subscribe response example</span></span>

### <a name="description"></a><span data-ttu-id="575d1-126">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="575d1-126">Description</span></span>

<span data-ttu-id="575d1-127">Im folgenden Beispiel wird eine erfolgreiche Antwort auf das Pullabonnement dargestellt.</span><span class="sxs-lookup"><span data-stu-id="575d1-127">The following example shows a successful pull subscription response.</span></span> <span data-ttu-id="575d1-128">Die Antwort enthält die Abonnement-ID und das Wasserzeichen, das verwendet wird, um das Array von Ereignissen abzurufen, die einem Abonnement zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="575d1-128">The response contains the subscription identifier and watermark that is used to get the array of events that are associated with a subscription.</span></span> <span data-ttu-id="575d1-129">Die Abonnement-ID wird auch verwendet, um das Abonnement eines Clients von einem Abonnement abzumelden.</span><span class="sxs-lookup"><span data-stu-id="575d1-129">The subscription identifier is also used to unsubscribe a client from a subscription.</span></span>
  
### <a name="code"></a><span data-ttu-id="575d1-130">Code</span><span class="sxs-lookup"><span data-stu-id="575d1-130">Code</span></span>

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
    <SubscribeResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                       xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:SubscribeResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:SubscriptionId>39ea5d0f-f062-455e-a1e9-89c0304390f4</m:SubscriptionId>
          <m:Watermark>AAAAAHgGAAAAAAAAAQ==</m:Watermark>
        </m:SubscribeResponseMessage>
      </m:ResponseMessages>
    </SubscribeResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="pull-subscription-subscribe-response-elements"></a><span data-ttu-id="575d1-131">Subscribe-Abonnement-Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="575d1-131">Pull Subscription Subscribe response elements</span></span>

<span data-ttu-id="575d1-132">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="575d1-132">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="575d1-133">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="575d1-133">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="575d1-134">SubscribeResponse</span><span class="sxs-lookup"><span data-stu-id="575d1-134">SubscribeResponse</span></span>](subscriberesponse.md)
    
- [<span data-ttu-id="575d1-135">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="575d1-135">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="575d1-136">SubscribeResponseMessage</span><span class="sxs-lookup"><span data-stu-id="575d1-136">SubscribeResponseMessage</span></span>](subscriberesponsemessage.md)
    
- [<span data-ttu-id="575d1-137">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="575d1-137">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="575d1-138">Abonnement-Nr (GetEvents)</span><span class="sxs-lookup"><span data-stu-id="575d1-138">SubscriptionId (GetEvents)</span></span>](subscriptionid-getevents.md)
    
- [<span data-ttu-id="575d1-139">Watermark</span><span class="sxs-lookup"><span data-stu-id="575d1-139">Watermark</span></span>](watermark.md)
    
## <a name="pull-subscription-subscribe-error-response-example"></a><span data-ttu-id="575d1-140">Beispiel für subscribe-Fehlerantwort für Pullabonnement</span><span class="sxs-lookup"><span data-stu-id="575d1-140">Pull Subscription Subscribe Error response example</span></span>

### <a name="description"></a><span data-ttu-id="575d1-141">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="575d1-141">Description</span></span>

<span data-ttu-id="575d1-142">Im folgenden Beispiel wird eine Fehlerantwort auf eine subscribe-Anforderung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="575d1-142">The following example shows an error response to a Subscribe request.</span></span> <span data-ttu-id="575d1-143">Der Fehler wird durch den Versuch verursacht, Benachrichtigungen mithilfe des Stellvertretungs Zugriffs zu abonnieren.</span><span class="sxs-lookup"><span data-stu-id="575d1-143">The error is caused by an attempt to subscribe to notifications by using delegate access.</span></span>
  
### <a name="code"></a><span data-ttu-id="575d1-144">Code</span><span class="sxs-lookup"><span data-stu-id="575d1-144">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <SubscribeResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                       xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:SubscribeResponseMessage ResponseClass="Error">
          <m:MessageText>Subscriptions are not supported for delegate user access.</m:MessageText>
          <m:ResponseCode>ErrorSubscriptionDelegateAccessNotSupported</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:SubscribeResponseMessage>
      </m:ResponseMessages>
    </SubscribeResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="pull-subscription-error-response-elements"></a><span data-ttu-id="575d1-145">Elemente des Pull-Abonnement-Fehlerantwort Elements</span><span class="sxs-lookup"><span data-stu-id="575d1-145">Pull Subscription Error response elements</span></span>

<span data-ttu-id="575d1-146">Folgende Elemente werden in der Fehlerantwort verwendet:</span><span class="sxs-lookup"><span data-stu-id="575d1-146">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="575d1-147">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="575d1-147">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="575d1-148">SubscribeResponse</span><span class="sxs-lookup"><span data-stu-id="575d1-148">SubscribeResponse</span></span>](subscriberesponse.md)
    
- [<span data-ttu-id="575d1-149">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="575d1-149">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="575d1-150">SubscribeResponseMessage</span><span class="sxs-lookup"><span data-stu-id="575d1-150">SubscribeResponseMessage</span></span>](subscriberesponsemessage.md)
    
- [<span data-ttu-id="575d1-151">MessageText</span><span class="sxs-lookup"><span data-stu-id="575d1-151">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="575d1-152">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="575d1-152">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="575d1-153">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="575d1-153">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="push-subscription-request-example"></a><span data-ttu-id="575d1-154">Push-Abonnementanforderung (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="575d1-154">Push Subscription request example</span></span>

### <a name="description"></a><span data-ttu-id="575d1-155">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="575d1-155">Description</span></span>

<span data-ttu-id="575d1-156">Im folgenden Codebeispiel wird gezeigt, wie Sie ein Push-Ereignis Benachrichtigungsabonnement abonnieren.</span><span class="sxs-lookup"><span data-stu-id="575d1-156">The following code example shows how to subscribe to a push event notification subscription.</span></span> <span data-ttu-id="575d1-157">Die Anforderung identifiziert die zu überwachenden Ordner, die zu überwachenden Ereignistypen, die Häufigkeit der Statusbenachrichtigungen und die URL des Client-Webdiensts, der die Push-Benachrichtigungen überwacht.</span><span class="sxs-lookup"><span data-stu-id="575d1-157">The request identifies the folders to monitor, the types of events to monitor, the frequency of status notifications, and the URL of the client Web service that listens for the push notifications.</span></span>
  
### <a name="code"></a><span data-ttu-id="575d1-158">Code</span><span class="sxs-lookup"><span data-stu-id="575d1-158">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <Subscribe xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <PushSubscriptionRequest xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
        <FolderIds xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <DistinguishedFolderId Id="inbox" />
        </FolderIds>
        <EventTypes xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <EventType>NewMailEvent</EventType>
          <EventType>CopiedEvent</EventType>
          <EventType>CreatedEvent</EventType>
          <EventType>DeletedEvent</EventType>
          <EventType>ModifiedEvent</EventType>
          <EventType>MovedEvent</EventType>
        </EventTypes>
        <StatusFrequency xmlns="https://schemas.microsoft.com/exchange/services/2006/types">1</StatusFrequency>
        <URL xmlns="https://schemas.microsoft.com/exchange/services/2006/types">http://clientWebService/Service.asmx</URL>
      </PushSubscriptionRequest>
    </Subscribe>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="575d1-159">Comments</span><span class="sxs-lookup"><span data-stu-id="575d1-159">Comments</span></span>

<span data-ttu-id="575d1-160">Der Client-Webdienst muss eingerichtet sein, bevor die Push Notification subscribe-Anforderung gesendet wird. Andernfalls wird die erste Benachrichtigung nicht an einen gültigen Endpunkt gesendet, und die Push-Benachrichtigung wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="575d1-160">The client Web service must be set up before the push notification subscribe request is sent; otherwise, the first notification will not be sent to a valid endpoint and the push notification will fail.</span></span> <span data-ttu-id="575d1-161">Weitere Informationen finden Sie unter [Push Notification-Beispielanwendung](https://msdn.microsoft.com/library/db1f8523-fa44-483f-bdb6-ab5939b52eee%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="575d1-161">For more information, see [Push Notification Sample Application](https://msdn.microsoft.com/library/db1f8523-fa44-483f-bdb6-ab5939b52eee%28Office.15%29.aspx).</span></span>
  
<span data-ttu-id="575d1-162">Beim erneuten Abonnieren wird eine neue [Abonnement-Startwert (GetEvents)](subscriptionid-getevents.md) erstellt.</span><span class="sxs-lookup"><span data-stu-id="575d1-162">A new [SubscriptionId (GetEvents)](subscriptionid-getevents.md) is created when you resubscribe.</span></span> <span data-ttu-id="575d1-163">Verwenden Sie das Wasserzeichen eines vorherigen Abonnements zum erneuten Abonnieren an der Stelle, an der das vorherige Abonnement endete.</span><span class="sxs-lookup"><span data-stu-id="575d1-163">Use the watermark of a previous subscription to resubscribe at the point where the previous subscription ended.</span></span> 
  
### <a name="push-subscription-request-elements"></a><span data-ttu-id="575d1-164">Push-Abonnement anforderungselemente</span><span class="sxs-lookup"><span data-stu-id="575d1-164">Push Subscription Request Elements</span></span>

<span data-ttu-id="575d1-165">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="575d1-165">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="575d1-166">Abonnieren</span><span class="sxs-lookup"><span data-stu-id="575d1-166">Subscribe</span></span>](subscribe.md)
    
- [<span data-ttu-id="575d1-167">PushSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="575d1-167">PushSubscriptionRequest</span></span>](pushsubscriptionrequest.md)
    
- [<span data-ttu-id="575d1-168">FolderIds</span><span class="sxs-lookup"><span data-stu-id="575d1-168">FolderIds</span></span>](folderids.md)
    
- [<span data-ttu-id="575d1-169">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="575d1-169">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="575d1-170">EventTypes</span><span class="sxs-lookup"><span data-stu-id="575d1-170">EventTypes</span></span>](eventtypes.md)
    
- [<span data-ttu-id="575d1-171">EventType</span><span class="sxs-lookup"><span data-stu-id="575d1-171">EventType</span></span>](eventtype.md)
    
- [<span data-ttu-id="575d1-172">StatusFrequency</span><span class="sxs-lookup"><span data-stu-id="575d1-172">StatusFrequency</span></span>](statusfrequency.md)
    
- [<span data-ttu-id="575d1-173">URL</span><span class="sxs-lookup"><span data-stu-id="575d1-173">Url </span></span>](url-ex15websvcsotherref.md)
    
## <a name="successful-push-subscription-response-example"></a><span data-ttu-id="575d1-174">Beispiel für eine erfolgreiche Push-Abonnement Antwort</span><span class="sxs-lookup"><span data-stu-id="575d1-174">Successful Push Subscription response example</span></span>

### <a name="description"></a><span data-ttu-id="575d1-175">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="575d1-175">Description</span></span>

<span data-ttu-id="575d1-176">Das folgende Beispiel zeigt eine erfolgreiche Push-Abonnement Antwort.</span><span class="sxs-lookup"><span data-stu-id="575d1-176">The following example shows a successful push subscription response.</span></span> 
  
### <a name="code"></a><span data-ttu-id="575d1-177">Code</span><span class="sxs-lookup"><span data-stu-id="575d1-177">Code</span></span>

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
    <SubscribeResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                       xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseMessages>
        <SubscribeResponseMessage ResponseClass="Success">
          <ResponseCode>NoError</ResponseCode>
          <SubscriptionId>83826921-afdf-48be-b469-628cc02b5f49</SubscriptionId>
          <Watermark>AQAAAOpvG0LURVdOhQkPOWZLPcI8EgAAAAAAAAE=</Watermark>
        </SubscribeResponseMessage>
      </ResponseMessages>
    </SubscribeResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="push-subscription-response-elements"></a><span data-ttu-id="575d1-178">Push-Abonnement-Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="575d1-178">Push Subscription response elements</span></span>

<span data-ttu-id="575d1-179">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="575d1-179">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="575d1-180">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="575d1-180">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="575d1-181">SubscribeResponse</span><span class="sxs-lookup"><span data-stu-id="575d1-181">SubscribeResponse</span></span>](subscriberesponse.md)
    
- [<span data-ttu-id="575d1-182">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="575d1-182">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="575d1-183">SubscribeResponseMessage</span><span class="sxs-lookup"><span data-stu-id="575d1-183">SubscribeResponseMessage</span></span>](subscriberesponsemessage.md)
    
- [<span data-ttu-id="575d1-184">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="575d1-184">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="575d1-185">Abonnement-Nr (GetEvents)</span><span class="sxs-lookup"><span data-stu-id="575d1-185">SubscriptionId (GetEvents)</span></span>](subscriptionid-getevents.md)
    
- [<span data-ttu-id="575d1-186">Watermark</span><span class="sxs-lookup"><span data-stu-id="575d1-186">Watermark</span></span>](watermark.md)
    
## <a name="see-also"></a><span data-ttu-id="575d1-187">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="575d1-187">See also</span></span>



[<span data-ttu-id="575d1-188">Vorgang des Kündigens von Abonnements</span><span class="sxs-lookup"><span data-stu-id="575d1-188">Unsubscribe operation</span></span>](unsubscribe-operation.md)
  
[<span data-ttu-id="575d1-189">GetEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="575d1-189">GetEvents operation</span></span>](getevents-operation.md)


[<span data-ttu-id="575d1-190">Verwenden von Pullabonnements</span><span class="sxs-lookup"><span data-stu-id="575d1-190">Using Pull Subscriptions</span></span>](https://msdn.microsoft.com/library/f956bc0e-2b25-4613-966b-54c65456897c%28Office.15%29.aspx)
  
[<span data-ttu-id="575d1-191">Beispielanwendung für Pushbenachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="575d1-191">Push Notification Sample Application</span></span>](https://msdn.microsoft.com/library/db1f8523-fa44-483f-bdb6-ab5939b52eee%28Office.15%29.aspx)

