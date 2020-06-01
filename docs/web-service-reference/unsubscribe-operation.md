---
title: Vorgang des Kündigens von Abonnements
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
description: Der Vorgang zum Kündigen des Abonnements wird zum Beenden eines Pullabonnements für eine Benachrichtigung verwendet. Verwenden Sie diesen Vorgang, anstatt ein Abonnement Timeout zu lassen. Dieser Vorgang ist nur für Pull-Benachrichtigungen gültig.
ms.openlocfilehash: 054f89af1ba5c780c7de5016a6dfe34086c97f02
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468026"
---
# <a name="unsubscribe-operation"></a><span data-ttu-id="1dccb-105">Vorgang des Kündigens von Abonnements</span><span class="sxs-lookup"><span data-stu-id="1dccb-105">Unsubscribe operation</span></span>

<span data-ttu-id="1dccb-106">Der Vorgang zum Kündigen des Abonnements wird zum Beenden eines Pullabonnements für eine Benachrichtigung verwendet.</span><span class="sxs-lookup"><span data-stu-id="1dccb-106">The Unsubscribe operation is used to end a pull notification subscription.</span></span> <span data-ttu-id="1dccb-107">Verwenden Sie diesen Vorgang, anstatt ein Abonnement Timeout zu lassen.</span><span class="sxs-lookup"><span data-stu-id="1dccb-107">Use this operation rather than letting a subscription timeout.</span></span> <span data-ttu-id="1dccb-108">Dieser Vorgang ist nur für Pull-Benachrichtigungen gültig.</span><span class="sxs-lookup"><span data-stu-id="1dccb-108">This operation is only valid for pull notifications.</span></span>
  
## <a name="unsubscribe-request-example"></a><span data-ttu-id="1dccb-109">Unsubscribe-Anforderungs Beispiel</span><span class="sxs-lookup"><span data-stu-id="1dccb-109">Unsubscribe request example</span></span>

### <a name="description"></a><span data-ttu-id="1dccb-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1dccb-110">Description</span></span>

<span data-ttu-id="1dccb-111">Das folgende Beispiel zeigt die SOAP-XML-Nachricht, die gesendet wird, um das Abonnement eines Clients vom Benachrichtigungsdienst aufzuheben.</span><span class="sxs-lookup"><span data-stu-id="1dccb-111">The following example shows the SOAP XML message that is sent to unsubscribe a client from the Notification service.</span></span>
  
### <a name="code"></a><span data-ttu-id="1dccb-112">Code</span><span class="sxs-lookup"><span data-stu-id="1dccb-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <Unsubscribe xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <SubscriptionId>e6fbf5c1-7e26-4bc6-a5f2-882063d5e34e</SubscriptionId>  
    </Unsubscribe>
  </soap:Body>
</soap:Envelope>
```

### <a name="unsubscribe-request-elements"></a><span data-ttu-id="1dccb-113">Elemente zum Aufheben der Abonnementanforderung</span><span class="sxs-lookup"><span data-stu-id="1dccb-113">Unsubscribe request elements</span></span>

<span data-ttu-id="1dccb-114">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="1dccb-114">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="1dccb-115">Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="1dccb-115">Unsubscribe</span></span>](unsubscribe.md)
    
- [<span data-ttu-id="1dccb-116">Abonnement-Nr (GetEvents)</span><span class="sxs-lookup"><span data-stu-id="1dccb-116">SubscriptionId (GetEvents)</span></span>](subscriptionid-getevents.md)
    
## <a name="successful-unsubscribe-response-example"></a><span data-ttu-id="1dccb-117">Beispiel für eine erfolgreiche Kündigungs Antwort</span><span class="sxs-lookup"><span data-stu-id="1dccb-117">Successful Unsubscribe response example</span></span>

### <a name="description"></a><span data-ttu-id="1dccb-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1dccb-118">Description</span></span>

<span data-ttu-id="1dccb-119">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine unsubscribe-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="1dccb-119">The following example shows a successful response to an Unsubscribe request.</span></span>
  
### <a name="code"></a><span data-ttu-id="1dccb-120">Code</span><span class="sxs-lookup"><span data-stu-id="1dccb-120">Code</span></span>

```xml
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <UnsubscribeResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:UnsubscribeResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:UnsubscribeResponseMessage>
      </m:ResponseMessages>
    </UnsubscribeResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="unsubscribe-response-elements"></a><span data-ttu-id="1dccb-121">Elemente zum Aufheben der Abonnenten Antwort</span><span class="sxs-lookup"><span data-stu-id="1dccb-121">Unsubscribe response elements</span></span>

<span data-ttu-id="1dccb-122">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="1dccb-122">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="1dccb-123">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="1dccb-123">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="1dccb-124">Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="1dccb-124">Unsubscribe</span></span>](unsubscribe.md)
    
- [<span data-ttu-id="1dccb-125">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="1dccb-125">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="1dccb-126">UnsubscribeResponseMessage</span><span class="sxs-lookup"><span data-stu-id="1dccb-126">UnsubscribeResponseMessage</span></span>](unsubscriberesponsemessage.md)
    
- [<span data-ttu-id="1dccb-127">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="1dccb-127">ResponseCode</span></span>](responsecode.md)
    
## <a name="unsubscribe-error-response-example"></a><span data-ttu-id="1dccb-128">Beispiel für unsubscribe-Fehlerantwort</span><span class="sxs-lookup"><span data-stu-id="1dccb-128">Unsubscribe Error response example</span></span>

### <a name="description"></a><span data-ttu-id="1dccb-129">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1dccb-129">Description</span></span>

<span data-ttu-id="1dccb-130">Das folgende Beispiel einer unsubscribe-Fehlerantwort tritt auf, wenn Sie versuchen, das Abonnement abzumelden, indem Sie einen Subskriptions Bezeichner verwenden, der sich nicht im Exchange-Informationsspeicher befinden kann.</span><span class="sxs-lookup"><span data-stu-id="1dccb-130">The following example of an Unsubscribe error response occurs in response to an attempt to unsubscribe by using a subscription identifier that cannot be located in the Exchange store.</span></span>
  
### <a name="code"></a><span data-ttu-id="1dccb-131">Code</span><span class="sxs-lookup"><span data-stu-id="1dccb-131">Code</span></span>

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
    <UnsubscribeResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="unsubscribe-error-response-elements"></a><span data-ttu-id="1dccb-132">Fehlerantwort Elemente für das Abonnement kündigen</span><span class="sxs-lookup"><span data-stu-id="1dccb-132">Unsubscribe Error response elements</span></span>

<span data-ttu-id="1dccb-133">Folgende Elemente werden in der Fehlerantwort verwendet:</span><span class="sxs-lookup"><span data-stu-id="1dccb-133">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="1dccb-134">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="1dccb-134">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="1dccb-135">UnsubscribeResponse</span><span class="sxs-lookup"><span data-stu-id="1dccb-135">UnsubscribeResponse</span></span>](unsubscriberesponse.md)
    
- [<span data-ttu-id="1dccb-136">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="1dccb-136">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="1dccb-137">UnsubscribeResponseMessage</span><span class="sxs-lookup"><span data-stu-id="1dccb-137">UnsubscribeResponseMessage</span></span>](unsubscriberesponsemessage.md)
    
- [<span data-ttu-id="1dccb-138">MessageText</span><span class="sxs-lookup"><span data-stu-id="1dccb-138">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="1dccb-139">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="1dccb-139">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="1dccb-140">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="1dccb-140">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="1dccb-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1dccb-141">See also</span></span>

- [<span data-ttu-id="1dccb-142">Vorgang abonnieren</span><span class="sxs-lookup"><span data-stu-id="1dccb-142">Subscribe operation</span></span>](subscribe-operation.md)
- [<span data-ttu-id="1dccb-143">GetEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="1dccb-143">GetEvents operation</span></span>](getevents-operation.md)
- [<span data-ttu-id="1dccb-144">Verwenden von Pullabonnements</span><span class="sxs-lookup"><span data-stu-id="1dccb-144">Using Pull Subscriptions</span></span>](https://msdn.microsoft.com/library/f956bc0e-2b25-4613-966b-54c65456897c%28Office.15%29.aspx)

