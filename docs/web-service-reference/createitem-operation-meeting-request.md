---
title: CreateItem-Vorgang (Besprechungsanfrage)
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
ms.assetid: fe136881-a804-456a-8552-8a1bea5eb9c8
description: Der CreateItem-Vorgang wird verwendet, um Antworten auf Besprechungsanfragen.
ms.openlocfilehash: a8aea688e46376906554952ce8ec45022cf613e9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757779"
---
# <a name="createitem-operation-meeting-request"></a><span data-ttu-id="eecd1-103">CreateItem-Vorgang (Besprechungsanfrage)</span><span class="sxs-lookup"><span data-stu-id="eecd1-103">CreateItem operation (meeting request)</span></span>

<span data-ttu-id="eecd1-104">Der CreateItem-Vorgang wird verwendet, um Antworten auf Besprechungsanfragen.</span><span class="sxs-lookup"><span data-stu-id="eecd1-104">The CreateItem operation is used to respond to meeting requests.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="eecd1-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="eecd1-105">Remarks</span></span>

<span data-ttu-id="eecd1-106">Der Vorgang CreateItem bietet drei Optionen für die Reaktion auf eine Besprechungsanfrage: annehmen, mit Vorbehalt annehmen oder ablehnen.</span><span class="sxs-lookup"><span data-stu-id="eecd1-106">The CreateItem operation provides three options for responding to a meeting request: accept, tentatively accept, or decline.</span></span> 
  
## <a name="accept-meeting-request-example"></a><span data-ttu-id="eecd1-107">Anforderungsbeispiel Besprechung akzeptieren</span><span class="sxs-lookup"><span data-stu-id="eecd1-107">Accept Meeting request example</span></span>

### <a name="description"></a><span data-ttu-id="eecd1-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eecd1-108">Description</span></span>

<span data-ttu-id="eecd1-109">Das folgende Beispiel zeigt, wie Sie zum Annehmen einer Besprechungsanfrage Einladung anfordern.</span><span class="sxs-lookup"><span data-stu-id="eecd1-109">The following example shows how to accept a meeting request invitation.</span></span>
  
### <a name="code"></a><span data-ttu-id="eecd1-110">Code</span><span class="sxs-lookup"><span data-stu-id="eecd1-110">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateItem xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
                MessageDisposition="SendAndSaveCopy">
      <Items>
        <AcceptItem xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
          <ReferenceItemId Id="AAAlAFVzZ"
                           ChangeKey="CwAAABYAA"/>
        </AcceptItem>
      </Items>
    </CreateItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="eecd1-111">Kommentare</span><span class="sxs-lookup"><span data-stu-id="eecd1-111">Comments</span></span>

<span data-ttu-id="eecd1-112">Mit Vorbehalt annehmen oder ablehnen die Besprechungsanfrage, verwenden Sie die Elemente [TentativelyAcceptItem](tentativelyacceptitem.md) oder [DeclineItem](declineitem.md) anstelle der [AcceptItem](acceptitem.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="eecd1-112">To tentatively accept or to decline the meeting request, use the [TentativelyAcceptItem](tentativelyacceptitem.md) or [DeclineItem](declineitem.md) elements in place of the [AcceptItem](acceptitem.md) element.</span></span> 
  
<span data-ttu-id="eecd1-113">Die Element-ID und Key ändern wurden gekürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="eecd1-113">The item identifier and change key have been shortened to preserve readability.</span></span>
  
### <a name="accepting-meeting-request-elements"></a><span data-ttu-id="eecd1-114">Akzeptieren die Besprechung Anforderung Elemente</span><span class="sxs-lookup"><span data-stu-id="eecd1-114">Accepting Meeting Request Elements</span></span>

<span data-ttu-id="eecd1-115">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="eecd1-115">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="eecd1-116">CreateItem</span><span class="sxs-lookup"><span data-stu-id="eecd1-116">CreateItem</span></span>](createitem.md)
    
- [<span data-ttu-id="eecd1-117">Elemente (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="eecd1-117">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md)
    
- [<span data-ttu-id="eecd1-118">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="eecd1-118">AcceptItem</span></span>](acceptitem.md)
    
- [<span data-ttu-id="eecd1-119">ReferenceItemId</span><span class="sxs-lookup"><span data-stu-id="eecd1-119">ReferenceItemId</span></span>](referenceitemid.md)
    
## <a name="successful-accept-meeting-response-example"></a><span data-ttu-id="eecd1-120">Erfolgreiche Besprechung akzeptieren antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="eecd1-120">Successful Accept Meeting response example</span></span>

### <a name="description"></a><span data-ttu-id="eecd1-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eecd1-121">Description</span></span>

<span data-ttu-id="eecd1-122">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die CreateItem-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="eecd1-122">The following example shows a successful response to the CreateItem request.</span></span>
  
### <a name="code"></a><span data-ttu-id="eecd1-123">Code</span><span class="sxs-lookup"><span data-stu-id="eecd1-123">Code</span></span>

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
    <CreateItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items />
        </m:CreateItemResponseMessage>
      </m:ResponseMessages>
    </CreateItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-response-elements"></a><span data-ttu-id="eecd1-124">Elemente einer erfolgreichen Antwort</span><span class="sxs-lookup"><span data-stu-id="eecd1-124">Successful response elements</span></span>

<span data-ttu-id="eecd1-125">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="eecd1-125">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="eecd1-126">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="eecd1-126">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="eecd1-127">CreateItemResponse</span><span class="sxs-lookup"><span data-stu-id="eecd1-127">CreateItemResponse</span></span>](createitemresponse.md)
    
- [<span data-ttu-id="eecd1-128">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="eecd1-128">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="eecd1-129">CreateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="eecd1-129">CreateItemResponseMessage</span></span>](createitemresponsemessage.md)
    
- [<span data-ttu-id="eecd1-130">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="eecd1-130">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="eecd1-131">Elemente</span><span class="sxs-lookup"><span data-stu-id="eecd1-131">Items</span></span>](items.md)
    
## <a name="accept-meeting-error-response-example"></a><span data-ttu-id="eecd1-132">Akzeptieren Sie die Besprechung Fehler antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="eecd1-132">Accept Meeting Error response example</span></span>

### <a name="description"></a><span data-ttu-id="eecd1-133">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eecd1-133">Description</span></span>

<span data-ttu-id="eecd1-134">Das folgende Beispiel zeigt eine Fehlerantwort an CreateItem-Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="eecd1-134">The following example shows an error response to CreateItem request.</span></span> <span data-ttu-id="eecd1-135">Der Fehler tritt bei dem Versuch, eine Besprechungsanfrage annehmen können, die nicht gefunden werden kann im Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="eecd1-135">The error is caused by an attempt to accept a meeting request that cannot be found in the Exchange store.</span></span>
  
### <a name="code"></a><span data-ttu-id="eecd1-136">Code</span><span class="sxs-lookup"><span data-stu-id="eecd1-136">Code</span></span>

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
    <CreateItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateItemResponseMessage ResponseClass="Error">
          <m:MessageText>The specified object was not found in the store.</m:MessageText>
          <m:ResponseCode>ErrorItemNotFound</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:Items />
        </m:CreateItemResponseMessage>
      </m:ResponseMessages>
    </CreateItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a><span data-ttu-id="eecd1-137">Fehler Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="eecd1-137">Error response elements</span></span>

<span data-ttu-id="eecd1-138">Folgende Elemente werden in der Fehlerantwort verwendet:</span><span class="sxs-lookup"><span data-stu-id="eecd1-138">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="eecd1-139">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="eecd1-139">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="eecd1-140">CreateItemResponse</span><span class="sxs-lookup"><span data-stu-id="eecd1-140">CreateItemResponse</span></span>](createitemresponse.md)
    
- [<span data-ttu-id="eecd1-141">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="eecd1-141">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="eecd1-142">CreateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="eecd1-142">CreateItemResponseMessage</span></span>](createitemresponsemessage.md)
    
- [<span data-ttu-id="eecd1-143">MessageText</span><span class="sxs-lookup"><span data-stu-id="eecd1-143">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="eecd1-144">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="eecd1-144">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="eecd1-145">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="eecd1-145">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="eecd1-146">Elemente</span><span class="sxs-lookup"><span data-stu-id="eecd1-146">Items</span></span>](items.md)
    
## <a name="see-also"></a><span data-ttu-id="eecd1-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eecd1-147">See also</span></span>



[<span data-ttu-id="eecd1-148">CreateItem Operation</span><span class="sxs-lookup"><span data-stu-id="eecd1-148">CreateItem operation</span></span>](createitem-operation.md)
  
[<span data-ttu-id="eecd1-149">CreateItem-Vorgang (Kalenderelement)</span><span class="sxs-lookup"><span data-stu-id="eecd1-149">CreateItem operation (calendar item)</span></span>](createitem-operation-calendar-item.md)

