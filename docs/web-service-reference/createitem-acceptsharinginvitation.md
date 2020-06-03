---
title: CreateItem (AcceptSharingInvitation)
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
ms.assetid: 710c893a-3037-4f04-b336-aefedd36c406
description: Der CreateItem-Vorgang wird verwendet, um eine Einladung zur Freigabe von Kalender-oder Kontaktdaten eines anderen Benutzers zu akzeptieren.
ms.openlocfilehash: eda846b72f42fe886497b355d9cddade7c5f4044
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457515"
---
# <a name="createitem-acceptsharinginvitation"></a><span data-ttu-id="c25ac-103">CreateItem (AcceptSharingInvitation)</span><span class="sxs-lookup"><span data-stu-id="c25ac-103">CreateItem (AcceptSharingInvitation)</span></span>

<span data-ttu-id="c25ac-104">Der **CreateItem** -Vorgang wird verwendet, um eine Einladung zur Freigabe von Kalender-oder Kontaktdaten eines anderen Benutzers zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="c25ac-104">The **CreateItem** operation is used to accept an invitation to share another user's calendar or contacts data.</span></span> 
  
## <a name="accept-sharing-invitation-request-example"></a><span data-ttu-id="c25ac-105">Beispiel für Freigabe Einladungsanforderung akzeptieren</span><span class="sxs-lookup"><span data-stu-id="c25ac-105">Accept Sharing Invitation request example</span></span>

### <a name="description"></a><span data-ttu-id="c25ac-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c25ac-106">Description</span></span>

<span data-ttu-id="c25ac-107">Das folgende Beispiel zeigt, wie Sie eine Freigabeeinladung annehmen.</span><span class="sxs-lookup"><span data-stu-id="c25ac-107">The following example shows how to accept a sharing invitation.</span></span>
  
### <a name="code"></a><span data-ttu-id="c25ac-108">Code</span><span class="sxs-lookup"><span data-stu-id="c25ac-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateItem xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <Items xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
        <AcceptSharingInvitation xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <ReferenceItemId Id="AAAlAFVzZ" ChangeKey="CwAAABYAA" />
        </AcceptSharingInvitation>
      </Items>
    </CreateItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a><span data-ttu-id="c25ac-109">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="c25ac-109">Request elements</span></span>

<span data-ttu-id="c25ac-110">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="c25ac-110">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="c25ac-111">CreateItem</span><span class="sxs-lookup"><span data-stu-id="c25ac-111">CreateItem</span></span>](createitem.md)
    
- [<span data-ttu-id="c25ac-112">Elemente</span><span class="sxs-lookup"><span data-stu-id="c25ac-112">Items</span></span>](items.md)
    
- [<span data-ttu-id="c25ac-113">AcceptSharingInvitation</span><span class="sxs-lookup"><span data-stu-id="c25ac-113">AcceptSharingInvitation</span></span>](acceptsharinginvitation.md)
    
- [<span data-ttu-id="c25ac-114">ReferenceItemId</span><span class="sxs-lookup"><span data-stu-id="c25ac-114">ReferenceItemId</span></span>](referenceitemid.md)
    
### <a name="comments"></a><span data-ttu-id="c25ac-115">Kommentare</span><span class="sxs-lookup"><span data-stu-id="c25ac-115">Comments</span></span>

<span data-ttu-id="c25ac-116">Die Element-ID und der Änderungsschlüssel wurden verkürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c25ac-116">The item identifier and change key have been shortened to preserve readability.</span></span>
  
## <a name="successful-accept-sharing-invitation-response-example"></a><span data-ttu-id="c25ac-117">Beispiel für die erfolgreiche Annahme von Freigabe Einladungsantworten</span><span class="sxs-lookup"><span data-stu-id="c25ac-117">Successful Accept Sharing Invitation response example</span></span>

### <a name="description"></a><span data-ttu-id="c25ac-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c25ac-118">Description</span></span>

<span data-ttu-id="c25ac-119">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **CreateItem** -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="c25ac-119">The following example shows a successful response to a **CreateItem** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="c25ac-120">Code</span><span class="sxs-lookup"><span data-stu-id="c25ac-120">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="0" 
                         MajorBuildNumber="639" 
                         MinorBuildNumber="11" 
                         Version="Exchange2010" 
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

### <a name="successful-response-elements"></a><span data-ttu-id="c25ac-121">Erfolgreiche Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="c25ac-121">Successful response elements</span></span>

<span data-ttu-id="c25ac-122">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="c25ac-122">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="c25ac-123">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="c25ac-123">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="c25ac-124">CreateItemResponse</span><span class="sxs-lookup"><span data-stu-id="c25ac-124">CreateItemResponse</span></span>](createitemresponse.md)
    
- [<span data-ttu-id="c25ac-125">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="c25ac-125">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="c25ac-126">CreateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="c25ac-126">CreateItemResponseMessage</span></span>](createitemresponsemessage.md)
    
- [<span data-ttu-id="c25ac-127">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="c25ac-127">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="c25ac-128">Elemente</span><span class="sxs-lookup"><span data-stu-id="c25ac-128">Items</span></span>](items.md)
    
## <a name="accept-sharing-invitation-error-response-example"></a><span data-ttu-id="c25ac-129">Beispiel für Fehler bei der Freigabeeinladung annehmen</span><span class="sxs-lookup"><span data-stu-id="c25ac-129">Accept Sharing Invitation Error response example</span></span>

### <a name="description"></a><span data-ttu-id="c25ac-130">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c25ac-130">Description</span></span>

<span data-ttu-id="c25ac-131">Das folgende Beispiel zeigt eine Fehlerantwort auf eine **CreateItem** -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="c25ac-131">The following example shows an error response to a **CreateItem** request.</span></span> <span data-ttu-id="c25ac-132">Der Fehler wird durch den Versuch verursacht, eine Freigabeeinladung zu akzeptieren, die im Exchange-Informationsspeicher nicht gefunden werden kann.</span><span class="sxs-lookup"><span data-stu-id="c25ac-132">The error is caused by an attempt to accept a sharing invitation that cannot be found in the Exchange store.</span></span> 
  
### <a name="code"></a><span data-ttu-id="c25ac-133">Code</span><span class="sxs-lookup"><span data-stu-id="c25ac-133">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="0" 
                         MajorBuildNumber="639" 
                         MinorBuildNumber="11" 
                         Version="Exchange2010" 
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

### <a name="error-response-elements"></a><span data-ttu-id="c25ac-134">Fehlerantwortelemente</span><span class="sxs-lookup"><span data-stu-id="c25ac-134">Error response elements</span></span>

<span data-ttu-id="c25ac-135">Folgende Elemente werden in der Fehlerantwort verwendet:</span><span class="sxs-lookup"><span data-stu-id="c25ac-135">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="c25ac-136">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="c25ac-136">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="c25ac-137">CreateItemResponse</span><span class="sxs-lookup"><span data-stu-id="c25ac-137">CreateItemResponse</span></span>](createitemresponse.md)
    
- [<span data-ttu-id="c25ac-138">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="c25ac-138">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="c25ac-139">CreateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="c25ac-139">CreateItemResponseMessage</span></span>](createitemresponsemessage.md)
    
- [<span data-ttu-id="c25ac-140">MessageText</span><span class="sxs-lookup"><span data-stu-id="c25ac-140">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="c25ac-141">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="c25ac-141">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="c25ac-142">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="c25ac-142">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="c25ac-143">Elemente</span><span class="sxs-lookup"><span data-stu-id="c25ac-143">Items</span></span>](items.md)
    
## <a name="see-also"></a><span data-ttu-id="c25ac-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c25ac-144">See also</span></span>



[<span data-ttu-id="c25ac-145">CreateItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="c25ac-145">CreateItem operation</span></span>](createitem-operation.md)

