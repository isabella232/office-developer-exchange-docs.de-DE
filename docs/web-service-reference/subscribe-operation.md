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
description: Subscribe-Vorgang wird verwendet, um die Clientanwendungen auf Push oder Pull-Benachrichtigungen zu abonnieren. Es ist wichtig, beachten Sie, dass die Struktur der Anforderungsnachrichten und Antworten je nach den Typ des ereignisbenachrichtigung unterscheidet.
ms.openlocfilehash: f6cacab80c8ca2e505ab63a162a161fcf5de8585
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831619"
---
# <a name="subscribe-operation"></a><span data-ttu-id="5615d-104">Vorgang abonnieren</span><span class="sxs-lookup"><span data-stu-id="5615d-104">Subscribe operation</span></span>

<span data-ttu-id="5615d-105">Subscribe-Vorgang wird verwendet, um die Clientanwendungen auf Push oder Pull-Benachrichtigungen zu abonnieren.</span><span class="sxs-lookup"><span data-stu-id="5615d-105">The Subscribe operation is used to subscribe client applications to either push or pull notifications.</span></span> <span data-ttu-id="5615d-106">Es ist wichtig, beachten Sie, dass die Struktur der Anforderungsnachrichten und Antworten je nach den Typ des ereignisbenachrichtigung unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="5615d-106">It is important to be aware that the structure of the request messages and responses is different depending on the type of event notification.</span></span> 
  
## <a name="pull-subscription-subscribe-request-example"></a><span data-ttu-id="5615d-107">Pull-Abonnement abonnieren anforderungsbeispiel</span><span class="sxs-lookup"><span data-stu-id="5615d-107">Pull Subscription Subscribe request example</span></span>

### <a name="description"></a><span data-ttu-id="5615d-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5615d-108">Description</span></span>

<span data-ttu-id="5615d-109">Im folgenden Codebeispiel wird veranschaulicht, wie ein Ereignis-Benachrichtigung Pullabonnement abonnieren.</span><span class="sxs-lookup"><span data-stu-id="5615d-109">The following code example shows how to subscribe to a pull event notification subscription.</span></span> <span data-ttu-id="5615d-110">Das Abonnement informiert die Clientanwendung, wenn neue e-Mail-Nachrichten in den Posteingang hinzugefügt wird und wenn ein Element aus dem Posteingang gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="5615d-110">The subscription informs the client application if new mail is added to the Inbox and if an item is deleted from the Inbox.</span></span> <span data-ttu-id="5615d-111">Das Abonnement wird Timeout auf, wenn der Client keine Informationen zu Ereignissen innerhalb von zehn Minuten anfordert.</span><span class="sxs-lookup"><span data-stu-id="5615d-111">The subscription will time out if the client does not request information about events within ten minutes.</span></span> <span data-ttu-id="5615d-112">Wenn das Abonnement abläuft, muss ein neues Abonnement weiterhin Benachrichtigungen anfordern hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="5615d-112">If the subscription expires, a new subscription must be established to continue to request notifications.</span></span>
  
### <a name="code"></a><span data-ttu-id="5615d-113">Code</span><span class="sxs-lookup"><span data-stu-id="5615d-113">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <Subscribe xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="pull-subscription-subscribe-request-elements"></a><span data-ttu-id="5615d-114">Pullabonnement abonnieren Anforderung Elemente</span><span class="sxs-lookup"><span data-stu-id="5615d-114">Pull Subscription Subscribe Request Elements</span></span>

<span data-ttu-id="5615d-115">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="5615d-115">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="5615d-116">Abonnieren</span><span class="sxs-lookup"><span data-stu-id="5615d-116">Subscribe</span></span>](subscribe.md)
    
- [<span data-ttu-id="5615d-117">PullSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="5615d-117">PullSubscriptionRequest</span></span>](pullsubscriptionrequest.md)
    
- [<span data-ttu-id="5615d-118">FolderIds</span><span class="sxs-lookup"><span data-stu-id="5615d-118">FolderIds</span></span>](folderids.md)
    
- [<span data-ttu-id="5615d-119">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="5615d-119">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="5615d-120">EventTypes</span><span class="sxs-lookup"><span data-stu-id="5615d-120">EventTypes</span></span>](eventtypes.md)
    
- [<span data-ttu-id="5615d-121">EventType</span><span class="sxs-lookup"><span data-stu-id="5615d-121">EventType</span></span>](eventtype.md)
    
- [<span data-ttu-id="5615d-122">Timeout</span><span class="sxs-lookup"><span data-stu-id="5615d-122">Timeout</span></span>](timeout.md)
    
<span data-ttu-id="5615d-123">Um weitere Optionen für die Anforderung an die Subscribe-Operation zu suchen, verwenden Sie die Schemahierarchie.</span><span class="sxs-lookup"><span data-stu-id="5615d-123">To find other options for the request message of the Subscribe operation, explore the schema hierarchy.</span></span> <span data-ttu-id="5615d-124">Starten Sie das [PullSubscriptionRequest](pullsubscriptionrequest.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="5615d-124">Start at the [PullSubscriptionRequest](pullsubscriptionrequest.md) element.</span></span> 
  
## <a name="successful-pull-subscription-subscribe-response-example"></a><span data-ttu-id="5615d-125">Erfolgreiche Pull-Abonnement abonniert antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="5615d-125">Successful Pull Subscription Subscribe response example</span></span>

### <a name="description"></a><span data-ttu-id="5615d-126">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5615d-126">Description</span></span>

<span data-ttu-id="5615d-127">Das folgende Beispiel zeigt eine erfolgreiche Pull-Abonnement-Antwort.</span><span class="sxs-lookup"><span data-stu-id="5615d-127">The following example shows a successful pull subscription response.</span></span> <span data-ttu-id="5615d-128">Die Antwort enthält die Abonnement-ID und Wasserzeichen, die verwendet wird, um das Array der Ereignisse abzurufen, die ein Abonnement zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="5615d-128">The response contains the subscription identifier and watermark that is used to get the array of events that are associated with a subscription.</span></span> <span data-ttu-id="5615d-129">Die Abonnement-ID wird auch verwendet, einen Client von einem Abonnement zu kündigen.</span><span class="sxs-lookup"><span data-stu-id="5615d-129">The subscription identifier is also used to unsubscribe a client from a subscription.</span></span>
  
### <a name="code"></a><span data-ttu-id="5615d-130">Code</span><span class="sxs-lookup"><span data-stu-id="5615d-130">Code</span></span>

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
    <SubscribeResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                       xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="pull-subscription-subscribe-response-elements"></a><span data-ttu-id="5615d-131">Pull-Abonnement abonniert Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="5615d-131">Pull Subscription Subscribe response elements</span></span>

<span data-ttu-id="5615d-132">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="5615d-132">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="5615d-133">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="5615d-133">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="5615d-134">SubscribeResponse</span><span class="sxs-lookup"><span data-stu-id="5615d-134">SubscribeResponse</span></span>](subscriberesponse.md)
    
- [<span data-ttu-id="5615d-135">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="5615d-135">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="5615d-136">SubscribeResponseMessage</span><span class="sxs-lookup"><span data-stu-id="5615d-136">SubscribeResponseMessage</span></span>](subscriberesponsemessage.md)
    
- [<span data-ttu-id="5615d-137">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="5615d-137">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="5615d-138">SubscriptionId (GetEvents)</span><span class="sxs-lookup"><span data-stu-id="5615d-138">SubscriptionId (GetEvents)</span></span>](subscriptionid-getevents.md)
    
- [<span data-ttu-id="5615d-139">Wasserzeichen</span><span class="sxs-lookup"><span data-stu-id="5615d-139">Watermark</span></span>](watermark.md)
    
## <a name="pull-subscription-subscribe-error-response-example"></a><span data-ttu-id="5615d-140">Pull-Abonnement abonnieren Fehler antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="5615d-140">Pull Subscription Subscribe Error response example</span></span>

### <a name="description"></a><span data-ttu-id="5615d-141">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5615d-141">Description</span></span>

<span data-ttu-id="5615d-142">Das folgende Beispiel zeigt eine Fehlerantwort an die Subscribe-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="5615d-142">The following example shows an error response to a Subscribe request.</span></span> <span data-ttu-id="5615d-143">Der Fehler wird durch den Versuch, Abonnieren von Benachrichtigungen mithilfe von Zugriffsrechten für Stellvertretung verursacht.</span><span class="sxs-lookup"><span data-stu-id="5615d-143">The error is caused by an attempt to subscribe to notifications by using delegate access.</span></span>
  
### <a name="code"></a><span data-ttu-id="5615d-144">Code</span><span class="sxs-lookup"><span data-stu-id="5615d-144">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <SubscribeResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                       xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="pull-subscription-error-response-elements"></a><span data-ttu-id="5615d-145">Ziehen Sie Antwortelemente Abonnementfehler</span><span class="sxs-lookup"><span data-stu-id="5615d-145">Pull Subscription Error response elements</span></span>

<span data-ttu-id="5615d-146">Folgende Elemente werden in der Fehlerantwort verwendet:</span><span class="sxs-lookup"><span data-stu-id="5615d-146">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="5615d-147">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="5615d-147">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="5615d-148">SubscribeResponse</span><span class="sxs-lookup"><span data-stu-id="5615d-148">SubscribeResponse</span></span>](subscriberesponse.md)
    
- [<span data-ttu-id="5615d-149">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="5615d-149">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="5615d-150">SubscribeResponseMessage</span><span class="sxs-lookup"><span data-stu-id="5615d-150">SubscribeResponseMessage</span></span>](subscriberesponsemessage.md)
    
- [<span data-ttu-id="5615d-151">MessageText</span><span class="sxs-lookup"><span data-stu-id="5615d-151">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="5615d-152">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="5615d-152">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="5615d-153">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="5615d-153">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="push-subscription-request-example"></a><span data-ttu-id="5615d-154">Push-Abonnement-anforderungsbeispiel</span><span class="sxs-lookup"><span data-stu-id="5615d-154">Push Subscription request example</span></span>

### <a name="description"></a><span data-ttu-id="5615d-155">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5615d-155">Description</span></span>

<span data-ttu-id="5615d-156">Im folgenden Codebeispiel wird veranschaulicht, wie ein Push-Ereignis Benachrichtigungsabonnement abonnieren.</span><span class="sxs-lookup"><span data-stu-id="5615d-156">The following code example shows how to subscribe to a push event notification subscription.</span></span> <span data-ttu-id="5615d-157">Die Anforderung identifiziert den Ordner überwacht werden, die Typen der zu überwachenden Ereignisse, die Häufigkeit der statusbenachrichtigungen und die URL des Clients Webdienst, der die Pushbenachrichtigungen überwacht.</span><span class="sxs-lookup"><span data-stu-id="5615d-157">The request identifies the folders to monitor, the types of events to monitor, the frequency of status notifications, and the URL of the client Web service that listens for the push notifications.</span></span>
  
### <a name="code"></a><span data-ttu-id="5615d-158">Code</span><span class="sxs-lookup"><span data-stu-id="5615d-158">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <Subscribe xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <PushSubscriptionRequest xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
        <FolderIds xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
          <DistinguishedFolderId Id="inbox" />
        </FolderIds>
        <EventTypes xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
          <EventType>NewMailEvent</EventType>
          <EventType>CopiedEvent</EventType>
          <EventType>CreatedEvent</EventType>
          <EventType>DeletedEvent</EventType>
          <EventType>ModifiedEvent</EventType>
          <EventType>MovedEvent</EventType>
        </EventTypes>
        <StatusFrequency xmlns="http://schemas.microsoft.com/exchange/services/2006/types">1</StatusFrequency>
        <URL xmlns="http://schemas.microsoft.com/exchange/services/2006/types">http://clientWebService/Service.asmx</URL>
      </PushSubscriptionRequest>
    </Subscribe>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="5615d-159">Kommentare</span><span class="sxs-lookup"><span data-stu-id="5615d-159">Comments</span></span>

<span data-ttu-id="5615d-160">Der Client Web Service eingerichtet werden muss, bevor das Push Notification abonnieren Anforderung wird gesendet. Andernfalls wird die erste Benachrichtigung an einen gültigen Endpunkt nicht gesendet, und das Push Notification schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="5615d-160">The client Web service must be set up before the push notification subscribe request is sent; otherwise, the first notification will not be sent to a valid endpoint and the push notification will fail.</span></span> <span data-ttu-id="5615d-161">Weitere Informationen finden Sie unter [Push Notification Beispielanwendung](http://msdn.microsoft.com/library/db1f8523-fa44-483f-bdb6-ab5939b52eee%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="5615d-161">For more information, see [Push Notification Sample Application](http://msdn.microsoft.com/library/db1f8523-fa44-483f-bdb6-ab5939b52eee%28Office.15%29.aspx).</span></span>
  
<span data-ttu-id="5615d-162">Eine neue [SubscriptionId (GetEvents)](subscriptionid-getevents.md) wird erstellt, sobald Sie erneut abonnieren.</span><span class="sxs-lookup"><span data-stu-id="5615d-162">A new [SubscriptionId (GetEvents)](subscriptionid-getevents.md) is created when you resubscribe.</span></span> <span data-ttu-id="5615d-163">Verwenden Sie das Wasserzeichen des vorherigen-Abonnements, um an der Stelle erneut abonnieren, in dem das vorherige Abonnement beendet.</span><span class="sxs-lookup"><span data-stu-id="5615d-163">Use the watermark of a previous subscription to resubscribe at the point where the previous subscription ended.</span></span> 
  
### <a name="push-subscription-request-elements"></a><span data-ttu-id="5615d-164">Push-Abonnement Anforderung Elemente</span><span class="sxs-lookup"><span data-stu-id="5615d-164">Push Subscription Request Elements</span></span>

<span data-ttu-id="5615d-165">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="5615d-165">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="5615d-166">Abonnieren</span><span class="sxs-lookup"><span data-stu-id="5615d-166">Subscribe</span></span>](subscribe.md)
    
- [<span data-ttu-id="5615d-167">PushSubscriptionRequest</span><span class="sxs-lookup"><span data-stu-id="5615d-167">PushSubscriptionRequest</span></span>](pushsubscriptionrequest.md)
    
- [<span data-ttu-id="5615d-168">FolderIds</span><span class="sxs-lookup"><span data-stu-id="5615d-168">FolderIds</span></span>](folderids.md)
    
- [<span data-ttu-id="5615d-169">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="5615d-169">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="5615d-170">EventTypes</span><span class="sxs-lookup"><span data-stu-id="5615d-170">EventTypes</span></span>](eventtypes.md)
    
- [<span data-ttu-id="5615d-171">EventType</span><span class="sxs-lookup"><span data-stu-id="5615d-171">EventType</span></span>](eventtype.md)
    
- [<span data-ttu-id="5615d-172">StatusFrequency</span><span class="sxs-lookup"><span data-stu-id="5615d-172">StatusFrequency</span></span>](statusfrequency.md)
    
- [<span data-ttu-id="5615d-173">URL</span><span class="sxs-lookup"><span data-stu-id="5615d-173">Url </span></span>](url-ex15websvcsotherref.md)
    
## <a name="successful-push-subscription-response-example"></a><span data-ttu-id="5615d-174">Erfolgreiche Pushabonnement antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="5615d-174">Successful Push Subscription response example</span></span>

### <a name="description"></a><span data-ttu-id="5615d-175">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5615d-175">Description</span></span>

<span data-ttu-id="5615d-176">Das folgende Beispiel zeigt eine erfolgreiche Push-Abonnement-Antwort.</span><span class="sxs-lookup"><span data-stu-id="5615d-176">The following example shows a successful push subscription response.</span></span> 
  
### <a name="code"></a><span data-ttu-id="5615d-177">Code</span><span class="sxs-lookup"><span data-stu-id="5615d-177">Code</span></span>

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
    <SubscribeResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                       xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="push-subscription-response-elements"></a><span data-ttu-id="5615d-178">Schieben Antwortelemente Abonnement</span><span class="sxs-lookup"><span data-stu-id="5615d-178">Push Subscription response elements</span></span>

<span data-ttu-id="5615d-179">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="5615d-179">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="5615d-180">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="5615d-180">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="5615d-181">SubscribeResponse</span><span class="sxs-lookup"><span data-stu-id="5615d-181">SubscribeResponse</span></span>](subscriberesponse.md)
    
- [<span data-ttu-id="5615d-182">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="5615d-182">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="5615d-183">SubscribeResponseMessage</span><span class="sxs-lookup"><span data-stu-id="5615d-183">SubscribeResponseMessage</span></span>](subscriberesponsemessage.md)
    
- [<span data-ttu-id="5615d-184">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="5615d-184">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="5615d-185">SubscriptionId (GetEvents)</span><span class="sxs-lookup"><span data-stu-id="5615d-185">SubscriptionId (GetEvents)</span></span>](subscriptionid-getevents.md)
    
- [<span data-ttu-id="5615d-186">Wasserzeichen</span><span class="sxs-lookup"><span data-stu-id="5615d-186">Watermark</span></span>](watermark.md)
    
## <a name="see-also"></a><span data-ttu-id="5615d-187">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5615d-187">See also</span></span>



[<span data-ttu-id="5615d-188">Vorgang des Kündigens von Abonnements</span><span class="sxs-lookup"><span data-stu-id="5615d-188">Unsubscribe operation</span></span>](unsubscribe-operation.md)
  
[<span data-ttu-id="5615d-189">GetEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="5615d-189">GetEvents operation</span></span>](getevents-operation.md)


[<span data-ttu-id="5615d-190">Mithilfe von Pullabonnements</span><span class="sxs-lookup"><span data-stu-id="5615d-190">Using Pull Subscriptions</span></span>](http://msdn.microsoft.com/library/f956bc0e-2b25-4613-966b-54c65456897c%28Office.15%29.aspx)
  
[<span data-ttu-id="5615d-191">Beispielanwendung für Pushbenachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="5615d-191">Push Notification Sample Application</span></span>](http://msdn.microsoft.com/library/db1f8523-fa44-483f-bdb6-ab5939b52eee%28Office.15%29.aspx)

