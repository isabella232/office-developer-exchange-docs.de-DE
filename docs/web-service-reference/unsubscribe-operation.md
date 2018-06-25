---
title: Melden Sie sich ab Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Unsubscribe
api_type:
- schema
ms.assetid: 994a9d2b-1501-4804-90f0-12bd914496ec
description: Der Vorgang zum Abmelden wird verwendet, um ein Pullabonnement Benachrichtigung zu beenden. Verwenden dieser Vorgang, anstatt einen Abonnement Timeout Navigate. Dieser Vorgang ist nur gültig für Pull-Benachrichtigungen.
ms.openlocfilehash: 64514a718d473f0fd7d0320bd1ccecddb1940ac8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839333"
---
# <a name="unsubscribe-operation"></a><span data-ttu-id="e9cb5-105">Melden Sie sich ab Vorgang</span><span class="sxs-lookup"><span data-stu-id="e9cb5-105">Unsubscribe operation</span></span>

<span data-ttu-id="e9cb5-106">Der Vorgang zum Abmelden wird verwendet, um ein Pullabonnement Benachrichtigung zu beenden.</span><span class="sxs-lookup"><span data-stu-id="e9cb5-106">The Unsubscribe operation is used to end a pull notification subscription.</span></span> <span data-ttu-id="e9cb5-107">Verwenden dieser Vorgang, anstatt einen Abonnement Timeout Navigate.</span><span class="sxs-lookup"><span data-stu-id="e9cb5-107">Use this operation rather than letting a subscription timeout.</span></span> <span data-ttu-id="e9cb5-108">Dieser Vorgang ist nur gültig für Pull-Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="e9cb5-108">This operation is only valid for pull notifications.</span></span>
  
## <a name="unsubscribe-request-example"></a><span data-ttu-id="e9cb5-109">Melden Sie sich ab anforderungsbeispiel</span><span class="sxs-lookup"><span data-stu-id="e9cb5-109">Unsubscribe request example</span></span>

### <a name="description"></a><span data-ttu-id="e9cb5-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e9cb5-110">Description</span></span>

<span data-ttu-id="e9cb5-111">Das folgende Beispiel zeigt die XML-SOAP-Nachricht, die gesendet wird, um zu einen Client Benachrichtigungsdienst kündigen.</span><span class="sxs-lookup"><span data-stu-id="e9cb5-111">The following example shows the SOAP XML message that is sent to unsubscribe a client from the Notification service.</span></span>
  
### <a name="code"></a><span data-ttu-id="e9cb5-112">Code</span><span class="sxs-lookup"><span data-stu-id="e9cb5-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <Unsubscribe xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <SubscriptionId>e6fbf5c1-7e26-4bc6-a5f2-882063d5e34e</SubscriptionId>  
    </Unsubscribe>
  </soap:Body>
</soap:Envelope>
```

### <a name="unsubscribe-request-elements"></a><span data-ttu-id="e9cb5-113">Melden Sie sich ab Anforderung Elemente</span><span class="sxs-lookup"><span data-stu-id="e9cb5-113">Unsubscribe request elements</span></span>

<span data-ttu-id="e9cb5-114">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="e9cb5-114">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="e9cb5-115">Melden Sie sich ab</span><span class="sxs-lookup"><span data-stu-id="e9cb5-115">Unsubscribe</span></span>](unsubscribe.md)
    
- [<span data-ttu-id="e9cb5-116">SubscriptionId (GetEvents)</span><span class="sxs-lookup"><span data-stu-id="e9cb5-116">SubscriptionId (GetEvents)</span></span>](subscriptionid-getevents.md)
    
## <a name="successful-unsubscribe-response-example"></a><span data-ttu-id="e9cb5-117">Erfolgreiche zum Abmelden antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="e9cb5-117">Successful Unsubscribe response example</span></span>

### <a name="description"></a><span data-ttu-id="e9cb5-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e9cb5-118">Description</span></span>

<span data-ttu-id="e9cb5-119">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine Anforderung zum Abmelden.</span><span class="sxs-lookup"><span data-stu-id="e9cb5-119">The following example shows a successful response to an Unsubscribe request.</span></span>
  
### <a name="code"></a><span data-ttu-id="e9cb5-120">Code</span><span class="sxs-lookup"><span data-stu-id="e9cb5-120">Code</span></span>

```xml
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <UnsubscribeResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:UnsubscribeResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:UnsubscribeResponseMessage>
      </m:ResponseMessages>
    </UnsubscribeResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="unsubscribe-response-elements"></a><span data-ttu-id="e9cb5-121">Melden Sie sich ab Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="e9cb5-121">Unsubscribe response elements</span></span>

<span data-ttu-id="e9cb5-122">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="e9cb5-122">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="e9cb5-123">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="e9cb5-123">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="e9cb5-124">Melden Sie sich ab</span><span class="sxs-lookup"><span data-stu-id="e9cb5-124">Unsubscribe</span></span>](unsubscribe.md)
    
- [<span data-ttu-id="e9cb5-125">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="e9cb5-125">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="e9cb5-126">UnsubscribeResponseMessage</span><span class="sxs-lookup"><span data-stu-id="e9cb5-126">UnsubscribeResponseMessage</span></span>](unsubscriberesponsemessage.md)
    
- [<span data-ttu-id="e9cb5-127">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="e9cb5-127">ResponseCode</span></span>](responsecode.md)
    
## <a name="unsubscribe-error-response-example"></a><span data-ttu-id="e9cb5-128">Melden Sie sich ab Fehler antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="e9cb5-128">Unsubscribe Error response example</span></span>

### <a name="description"></a><span data-ttu-id="e9cb5-129">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e9cb5-129">Description</span></span>

<span data-ttu-id="e9cb5-130">Im folgenden Beispiel wird eine Fehlerantwort kündigen wird als Reaktion auf ein Versuch, kündigen mithilfe einer Abonnement-ID, die nicht gefunden werden kann im Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="e9cb5-130">The following example of an Unsubscribe error response occurs in response to an attempt to unsubscribe by using a subscription identifier that cannot be located in the Exchange store.</span></span>
  
### <a name="code"></a><span data-ttu-id="e9cb5-131">Code</span><span class="sxs-lookup"><span data-stu-id="e9cb5-131">Code</span></span>

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
    <UnsubscribeResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:UnsubscribeResponseMessage ResponseClass="Error">
          <m:MessageText>The specified subscription was not found.</m:MessageText>
          <m:ResponseCode>ErrorSubscriptionNotFound</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:UnsubscribeResponseMessage>
      </m:ResponseMessages>
    </UnsubscribeResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="unsubscribe-error-response-elements"></a><span data-ttu-id="e9cb5-132">Melden Sie sich ab Antwortelemente Fehler</span><span class="sxs-lookup"><span data-stu-id="e9cb5-132">Unsubscribe Error response elements</span></span>

<span data-ttu-id="e9cb5-133">Folgende Elemente werden in der Fehlerantwort verwendet:</span><span class="sxs-lookup"><span data-stu-id="e9cb5-133">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="e9cb5-134">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="e9cb5-134">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="e9cb5-135">UnsubscribeResponse</span><span class="sxs-lookup"><span data-stu-id="e9cb5-135">UnsubscribeResponse</span></span>](unsubscriberesponse.md)
    
- [<span data-ttu-id="e9cb5-136">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="e9cb5-136">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="e9cb5-137">UnsubscribeResponseMessage</span><span class="sxs-lookup"><span data-stu-id="e9cb5-137">UnsubscribeResponseMessage</span></span>](unsubscriberesponsemessage.md)
    
- [<span data-ttu-id="e9cb5-138">MessageText</span><span class="sxs-lookup"><span data-stu-id="e9cb5-138">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="e9cb5-139">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="e9cb5-139">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="e9cb5-140">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="e9cb5-140">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="e9cb5-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e9cb5-141">See also</span></span>

- [<span data-ttu-id="e9cb5-142">Vorgang abonnieren</span><span class="sxs-lookup"><span data-stu-id="e9cb5-142">Subscribe operation</span></span>](subscribe-operation.md)
- [<span data-ttu-id="e9cb5-143">GetEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="e9cb5-143">GetEvents operation</span></span>](getevents-operation.md)
- [<span data-ttu-id="e9cb5-144">Mithilfe von Pullabonnements</span><span class="sxs-lookup"><span data-stu-id="e9cb5-144">Using Pull Subscriptions</span></span>](http://msdn.microsoft.com/library/f956bc0e-2b25-4613-966b-54c65456897c%28Office.15%29.aspx)

