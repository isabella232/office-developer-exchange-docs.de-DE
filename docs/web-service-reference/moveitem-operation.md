---
title: MoveItem-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MoveItem
api_type:
- schema
ms.assetid: dcf40fa7-7796-4a5c-bf5b-7a509a18d208
description: Der MoveItem-Vorgang wird verwendet, um ein oder mehrere Elemente in einen einzelnen Zielordner zu verlagern.
ms.openlocfilehash: 6a455e483ad2e5c84b91cfaa7562f4f1ec46a112
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465681"
---
# <a name="moveitem-operation"></a><span data-ttu-id="47966-103">MoveItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="47966-103">MoveItem operation</span></span>

<span data-ttu-id="47966-104">Der **MoveItem** -Vorgang wird verwendet, um ein oder mehrere Elemente in einen einzelnen Zielordner zu verlagern.</span><span class="sxs-lookup"><span data-stu-id="47966-104">The **MoveItem** operation is used to move one or more items to a single destination folder.</span></span> 
  
## <a name="moveitem-request-example"></a><span data-ttu-id="47966-105">MoveItem-Anforderungs Beispiel</span><span class="sxs-lookup"><span data-stu-id="47966-105">MoveItem request example</span></span>

### <a name="description"></a><span data-ttu-id="47966-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="47966-106">Description</span></span>

<span data-ttu-id="47966-107">Im folgenden Beispiel einer **MoveItem** -Anforderung wird gezeigt, wie ein Element in den Ordner Entwürfe verschiebt wird.</span><span class="sxs-lookup"><span data-stu-id="47966-107">The following example of a **MoveItem** request shows how to move an item to the Drafts folder.</span></span> 
  
### <a name="code"></a><span data-ttu-id="47966-108">Code</span><span class="sxs-lookup"><span data-stu-id="47966-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
xmlns:xsd="http://www.w3.org/2001/XMLSchema"
xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <MoveItem xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <ToFolderId>
        <t:DistinguishedFolderId Id="drafts"/>
      </ToFolderId>
      <ItemIds>
        <t:ItemId Id="AAAtAEF/swbAAA=" ChangeKey="EwAAABYA/s4b"/>
      </ItemIds>
    </MoveItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="47966-109">Comments</span><span class="sxs-lookup"><span data-stu-id="47966-109">Comments</span></span>

<span data-ttu-id="47966-110">Das [tofolder](tofolderid.md) -Element gibt den Ordner an, in den die Elemente verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="47966-110">The [ToFolderId](tofolderid.md) element specifies the folder to which the items will be moved.</span></span> <span data-ttu-id="47966-111">Beachten Sie, dass alle Elemente, die in der [itemids](itemids.md) -Auflistung aufgeführt sind, im Zielordner enden.</span><span class="sxs-lookup"><span data-stu-id="47966-111">Note that all items listed in the [ItemIds](itemids.md) collection will end up in the destination folder.</span></span> <span data-ttu-id="47966-112">Sie müssen separate **MoveItem** -Aufrufe ausführen, um Elemente in unterschiedlichen Zielordnern zu platzieren.</span><span class="sxs-lookup"><span data-stu-id="47966-112">You must make separate **MoveItem** calls to place items in different destination folders.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="47966-113">Die Element-ID und der Änderungsschlüssel wurden verkürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="47966-113">The item identifier and change key have been shortened to preserve readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="47966-114">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="47966-114">Request elements</span></span>

<span data-ttu-id="47966-115">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="47966-115">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="47966-116">MoveItem</span><span class="sxs-lookup"><span data-stu-id="47966-116">MoveItem</span></span>](moveitem.md)
    
- [<span data-ttu-id="47966-117">Tofolder-Datei</span><span class="sxs-lookup"><span data-stu-id="47966-117">ToFolderId</span></span>](tofolderid.md)
    
- [<span data-ttu-id="47966-118">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="47966-118">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="47966-119">ItemIds</span><span class="sxs-lookup"><span data-stu-id="47966-119">ItemIds</span></span>](itemids.md)
    
- [<span data-ttu-id="47966-120">ItemId</span><span class="sxs-lookup"><span data-stu-id="47966-120">ItemId</span></span>](itemid.md)
    
## <a name="moveitem-response-example"></a><span data-ttu-id="47966-121">MoveItem-Antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="47966-121">MoveItem response example</span></span>

### <a name="description"></a><span data-ttu-id="47966-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="47966-122">Description</span></span>

<span data-ttu-id="47966-123">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **MoveItem** -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="47966-123">The following example shows a successful response to a **MoveItem** request.</span></span> 
  
<span data-ttu-id="47966-124">Die Element-ID des neuen Elements wird in der Antwortnachricht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="47966-124">The item identifier of the new item is returned in the response message.</span></span> <span data-ttu-id="47966-125">Element-IDs werden nicht in den Antworten für Postfächer-oder Postfach- **MoveItem** -Vorgänge im öffentlichen Ordner zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="47966-125">Item identifiers are not returned in responses for cross-mailbox or mailbox to public folder **MoveItem** operations.</span></span> 
  
### <a name="code"></a><span data-ttu-id="47966-126">Code</span><span class="sxs-lookup"><span data-stu-id="47966-126">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="662" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <MoveItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:MoveItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Message>
              <t:ItemID Id="AAMkAd" ChangeKey="FwAAABY" />
            </t:Message>
          </m:Items>
        </m:MoveItemResponseMessage>
      </m:ResponseMessages>
    </MoveItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="47966-127">Comments</span><span class="sxs-lookup"><span data-stu-id="47966-127">Comments</span></span>

<span data-ttu-id="47966-128">Der **MoveItem** -Vorgang zeigt den Erfolg an, wenn die Migration erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="47966-128">The **MoveItem** operation will indicate success if the move was successful.</span></span> 
  
### <a name="successful-response-elements"></a><span data-ttu-id="47966-129">Erfolgreiche Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="47966-129">Successful response elements</span></span>

<span data-ttu-id="47966-130">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="47966-130">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="47966-131">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="47966-131">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="47966-132">MoveItemResponse</span><span class="sxs-lookup"><span data-stu-id="47966-132">MoveItemResponse</span></span>](moveitemresponse.md)
    
- [<span data-ttu-id="47966-133">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="47966-133">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="47966-134">MoveItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="47966-134">MoveItemResponseMessage</span></span>](moveitemresponsemessage.md)
    
- [<span data-ttu-id="47966-135">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="47966-135">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="47966-136">Items</span><span class="sxs-lookup"><span data-stu-id="47966-136">Items</span></span>](items.md)
    
## <a name="see-also"></a><span data-ttu-id="47966-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="47966-137">See also</span></span>



- [<span data-ttu-id="47966-138">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="47966-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

