---
title: MoveItem Operation
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
description: MoveItem-Vorgang wird verwendet, um ein oder mehrere Elemente in einen gemeinsamen Zielordner zu verschieben.
ms.openlocfilehash: c5619befb02ec20ef0911992484dcc00cc2c5e92
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830492"
---
# <a name="moveitem-operation"></a><span data-ttu-id="0683e-103">MoveItem Operation</span><span class="sxs-lookup"><span data-stu-id="0683e-103">MoveItem operation</span></span>

<span data-ttu-id="0683e-104">**MoveItem** -Vorgang wird verwendet, um ein oder mehrere Elemente in einen gemeinsamen Zielordner zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="0683e-104">The **MoveItem** operation is used to move one or more items to a single destination folder.</span></span> 
  
## <a name="moveitem-request-example"></a><span data-ttu-id="0683e-105">MoveItem-anforderungsbeispiel</span><span class="sxs-lookup"><span data-stu-id="0683e-105">MoveItem request example</span></span>

### <a name="description"></a><span data-ttu-id="0683e-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0683e-106">Description</span></span>

<span data-ttu-id="0683e-107">Im folgenden Beispiel wird eine Anforderung **MoveItem** veranschaulicht, wie ein Element im Ordner Entwürfe zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="0683e-107">The following example of a **MoveItem** request shows how to move an item to the Drafts folder.</span></span> 
  
### <a name="code"></a><span data-ttu-id="0683e-108">Code</span><span class="sxs-lookup"><span data-stu-id="0683e-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
xmlns:xsd="http://www.w3.org/2001/XMLSchema"
xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <MoveItem xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

### <a name="comments"></a><span data-ttu-id="0683e-109">Kommentare</span><span class="sxs-lookup"><span data-stu-id="0683e-109">Comments</span></span>

<span data-ttu-id="0683e-110">Das [ToFolderId](tofolderid.md) -Element gibt den Ordner, in dem die Elemente verschoben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0683e-110">The [ToFolderId](tofolderid.md) element specifies the folder to which the items will be moved.</span></span> <span data-ttu-id="0683e-111">Beachten Sie, dass alle Elemente in der Auflistung [Artikelnummern ein.](itemids.md) im Zielordner resultiert.</span><span class="sxs-lookup"><span data-stu-id="0683e-111">Note that all items listed in the [ItemIds](itemids.md) collection will end up in the destination folder.</span></span> <span data-ttu-id="0683e-112">Sie müssen separate **MoveItem** platzieren Sie Elemente in unterschiedlichen Zielordner aufrufen.</span><span class="sxs-lookup"><span data-stu-id="0683e-112">You must make separate **MoveItem** calls to place items in different destination folders.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="0683e-113">Die Element-ID und Key ändern wurden gekürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0683e-113">The item identifier and change key have been shortened to preserve readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="0683e-114">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="0683e-114">Request elements</span></span>

<span data-ttu-id="0683e-115">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="0683e-115">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="0683e-116">MoveItem</span><span class="sxs-lookup"><span data-stu-id="0683e-116">MoveItem</span></span>](moveitem.md)
    
- [<span data-ttu-id="0683e-117">ToFolderId</span><span class="sxs-lookup"><span data-stu-id="0683e-117">ToFolderId</span></span>](tofolderid.md)
    
- [<span data-ttu-id="0683e-118">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="0683e-118">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="0683e-119">Artikelnummern ein.</span><span class="sxs-lookup"><span data-stu-id="0683e-119">ItemIds</span></span>](itemids.md)
    
- [<span data-ttu-id="0683e-120">ItemId</span><span class="sxs-lookup"><span data-stu-id="0683e-120">ItemId</span></span>](itemid.md)
    
## <a name="moveitem-response-example"></a><span data-ttu-id="0683e-121">MoveItem-Antwort-Beispiel</span><span class="sxs-lookup"><span data-stu-id="0683e-121">MoveItem response example</span></span>

### <a name="description"></a><span data-ttu-id="0683e-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0683e-122">Description</span></span>

<span data-ttu-id="0683e-123">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine Anforderung **MoveItem** .</span><span class="sxs-lookup"><span data-stu-id="0683e-123">The following example shows a successful response to a **MoveItem** request.</span></span> 
  
<span data-ttu-id="0683e-124">Der Elementbezeichner des neuen Elements wird in der Antwortnachricht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0683e-124">The item identifier of the new item is returned in the response message.</span></span> <span data-ttu-id="0683e-125">Element-IDs werden nicht auf Öffentliche Ordner **MoveItem** Vorgänge in Antworten für postfachübergreifenden oder Postfach zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0683e-125">Item identifiers are not returned in responses for cross-mailbox or mailbox to public folder **MoveItem** operations.</span></span> 
  
### <a name="code"></a><span data-ttu-id="0683e-126">Code</span><span class="sxs-lookup"><span data-stu-id="0683e-126">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="662" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <MoveItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a><span data-ttu-id="0683e-127">Kommentare</span><span class="sxs-lookup"><span data-stu-id="0683e-127">Comments</span></span>

<span data-ttu-id="0683e-128">**MoveItem** -Vorgang wird Erfolg anzuzeigen, wenn die Verschiebung erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="0683e-128">The **MoveItem** operation will indicate success if the move was successful.</span></span> 
  
### <a name="successful-response-elements"></a><span data-ttu-id="0683e-129">Elemente einer erfolgreichen Antwort</span><span class="sxs-lookup"><span data-stu-id="0683e-129">Successful response elements</span></span>

<span data-ttu-id="0683e-130">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="0683e-130">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="0683e-131">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="0683e-131">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="0683e-132">MoveItemResponse</span><span class="sxs-lookup"><span data-stu-id="0683e-132">MoveItemResponse</span></span>](moveitemresponse.md)
    
- [<span data-ttu-id="0683e-133">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="0683e-133">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="0683e-134">MoveItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="0683e-134">MoveItemResponseMessage</span></span>](moveitemresponsemessage.md)
    
- [<span data-ttu-id="0683e-135">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="0683e-135">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="0683e-136">Elemente</span><span class="sxs-lookup"><span data-stu-id="0683e-136">Items</span></span>](items.md)
    
## <a name="see-also"></a><span data-ttu-id="0683e-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0683e-137">See also</span></span>



- [<span data-ttu-id="0683e-138">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="0683e-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

