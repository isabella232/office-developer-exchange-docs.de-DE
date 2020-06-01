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
description: Der CreateItem-Vorgang wird verwendet, um auf Besprechungsanfragen zu reagieren.
ms.openlocfilehash: f9e6bd1742e6a30d08736ea67c0ff80b7a18e88a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457109"
---
# <a name="createitem-operation-meeting-request"></a><span data-ttu-id="0d226-103">CreateItem-Vorgang (Besprechungsanfrage)</span><span class="sxs-lookup"><span data-stu-id="0d226-103">CreateItem operation (meeting request)</span></span>

<span data-ttu-id="0d226-104">Der CreateItem-Vorgang wird verwendet, um auf Besprechungsanfragen zu reagieren.</span><span class="sxs-lookup"><span data-stu-id="0d226-104">The CreateItem operation is used to respond to meeting requests.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0d226-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0d226-105">Remarks</span></span>

<span data-ttu-id="0d226-106">Der CreateItem-Vorgang bietet drei Optionen für die Antwort auf eine Besprechungsanfrage: akzeptieren, mit Vorbehalt annehmen oder ablehnen.</span><span class="sxs-lookup"><span data-stu-id="0d226-106">The CreateItem operation provides three options for responding to a meeting request: accept, tentatively accept, or decline.</span></span> 
  
## <a name="accept-meeting-request-example"></a><span data-ttu-id="0d226-107">Beispiel für die Annahme einer Besprechungsanfrage</span><span class="sxs-lookup"><span data-stu-id="0d226-107">Accept Meeting request example</span></span>

### <a name="description"></a><span data-ttu-id="0d226-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0d226-108">Description</span></span>

<span data-ttu-id="0d226-109">Das folgende Beispiel zeigt, wie Sie eine Einladung zur Besprechungsanfrage annehmen.</span><span class="sxs-lookup"><span data-stu-id="0d226-109">The following example shows how to accept a meeting request invitation.</span></span>
  
### <a name="code"></a><span data-ttu-id="0d226-110">Code</span><span class="sxs-lookup"><span data-stu-id="0d226-110">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateItem xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                MessageDisposition="SendAndSaveCopy">
      <Items>
        <AcceptItem xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <ReferenceItemId Id="AAAlAFVzZ"
                           ChangeKey="CwAAABYAA"/>
        </AcceptItem>
      </Items>
    </CreateItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="0d226-111">Comments</span><span class="sxs-lookup"><span data-stu-id="0d226-111">Comments</span></span>

<span data-ttu-id="0d226-112">Um die Besprechungsanfrage vorläufig anzunehmen oder abzulehnen, verwenden Sie die [TentativelyAcceptItem](tentativelyacceptitem.md) -oder [DeclineItem](declineitem.md) -Elemente anstelle des [AcceptItem](acceptitem.md) -Elements.</span><span class="sxs-lookup"><span data-stu-id="0d226-112">To tentatively accept or to decline the meeting request, use the [TentativelyAcceptItem](tentativelyacceptitem.md) or [DeclineItem](declineitem.md) elements in place of the [AcceptItem](acceptitem.md) element.</span></span> 
  
<span data-ttu-id="0d226-113">Die Element-ID und der Änderungsschlüssel wurden verkürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0d226-113">The item identifier and change key have been shortened to preserve readability.</span></span>
  
### <a name="accepting-meeting-request-elements"></a><span data-ttu-id="0d226-114">Akzeptieren von Elementen der Besprechungsanfrage</span><span class="sxs-lookup"><span data-stu-id="0d226-114">Accepting Meeting Request Elements</span></span>

<span data-ttu-id="0d226-115">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="0d226-115">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="0d226-116">CreateItem</span><span class="sxs-lookup"><span data-stu-id="0d226-116">CreateItem</span></span>](createitem.md)
    
- [<span data-ttu-id="0d226-117">Elemente (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="0d226-117">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md)
    
- [<span data-ttu-id="0d226-118">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="0d226-118">AcceptItem</span></span>](acceptitem.md)
    
- [<span data-ttu-id="0d226-119">ReferenceItemId</span><span class="sxs-lookup"><span data-stu-id="0d226-119">ReferenceItemId</span></span>](referenceitemid.md)
    
## <a name="successful-accept-meeting-response-example"></a><span data-ttu-id="0d226-120">Beispiel für erfolgreiche Annahme einer Besprechungsantwort</span><span class="sxs-lookup"><span data-stu-id="0d226-120">Successful Accept Meeting response example</span></span>

### <a name="description"></a><span data-ttu-id="0d226-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0d226-121">Description</span></span>

<span data-ttu-id="0d226-122">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die CreateItem-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="0d226-122">The following example shows a successful response to the CreateItem request.</span></span>
  
### <a name="code"></a><span data-ttu-id="0d226-123">Code</span><span class="sxs-lookup"><span data-stu-id="0d226-123">Code</span></span>

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
    <CreateItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="successful-response-elements"></a><span data-ttu-id="0d226-124">Erfolgreiche Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="0d226-124">Successful response elements</span></span>

<span data-ttu-id="0d226-125">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="0d226-125">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="0d226-126">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="0d226-126">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="0d226-127">CreateItemResponse</span><span class="sxs-lookup"><span data-stu-id="0d226-127">CreateItemResponse</span></span>](createitemresponse.md)
    
- [<span data-ttu-id="0d226-128">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="0d226-128">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="0d226-129">CreateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="0d226-129">CreateItemResponseMessage</span></span>](createitemresponsemessage.md)
    
- [<span data-ttu-id="0d226-130">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="0d226-130">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="0d226-131">Items</span><span class="sxs-lookup"><span data-stu-id="0d226-131">Items</span></span>](items.md)
    
## <a name="accept-meeting-error-response-example"></a><span data-ttu-id="0d226-132">Beispiel für die Annahme einer Besprechungs Fehlerantwort</span><span class="sxs-lookup"><span data-stu-id="0d226-132">Accept Meeting Error response example</span></span>

### <a name="description"></a><span data-ttu-id="0d226-133">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0d226-133">Description</span></span>

<span data-ttu-id="0d226-134">Das folgende Beispiel zeigt eine Fehlerantwort auf CreateItem-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="0d226-134">The following example shows an error response to CreateItem request.</span></span> <span data-ttu-id="0d226-135">Der Fehler wird durch den Versuch verursacht, eine Besprechungsanfrage anzunehmen, die im Exchange-Informationsspeicher nicht gefunden werden kann.</span><span class="sxs-lookup"><span data-stu-id="0d226-135">The error is caused by an attempt to accept a meeting request that cannot be found in the Exchange store.</span></span>
  
### <a name="code"></a><span data-ttu-id="0d226-136">Code</span><span class="sxs-lookup"><span data-stu-id="0d226-136">Code</span></span>

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
    <CreateItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="error-response-elements"></a><span data-ttu-id="0d226-137">Fehlerantwortelemente</span><span class="sxs-lookup"><span data-stu-id="0d226-137">Error response elements</span></span>

<span data-ttu-id="0d226-138">Folgende Elemente werden in der Fehlerantwort verwendet:</span><span class="sxs-lookup"><span data-stu-id="0d226-138">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="0d226-139">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="0d226-139">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="0d226-140">CreateItemResponse</span><span class="sxs-lookup"><span data-stu-id="0d226-140">CreateItemResponse</span></span>](createitemresponse.md)
    
- [<span data-ttu-id="0d226-141">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="0d226-141">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="0d226-142">CreateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="0d226-142">CreateItemResponseMessage</span></span>](createitemresponsemessage.md)
    
- [<span data-ttu-id="0d226-143">MessageText</span><span class="sxs-lookup"><span data-stu-id="0d226-143">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="0d226-144">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="0d226-144">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="0d226-145">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="0d226-145">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="0d226-146">Items</span><span class="sxs-lookup"><span data-stu-id="0d226-146">Items</span></span>](items.md)
    
## <a name="see-also"></a><span data-ttu-id="0d226-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0d226-147">See also</span></span>



[<span data-ttu-id="0d226-148">CreateItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="0d226-148">CreateItem operation</span></span>](createitem-operation.md)
  
[<span data-ttu-id="0d226-149">CreateItem-Vorgang (Kalenderelement)</span><span class="sxs-lookup"><span data-stu-id="0d226-149">CreateItem operation (calendar item)</span></span>](createitem-operation-calendar-item.md)

