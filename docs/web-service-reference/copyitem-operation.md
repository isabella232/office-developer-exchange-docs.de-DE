---
title: CopyItem Operation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CopyItem
api_type:
- schema
ms.assetid: bcc68f9e-d511-4c29-bba6-ed535524624a
description: Der Vorgang CopyItem Elemente kopiert und werden die Elemente in einem anderen Ordner platziert.
ms.openlocfilehash: 95d2371e9185aa25f40eaec37dda54276a54d321
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757725"
---
# <a name="copyitem-operation"></a><span data-ttu-id="9cd3e-103">CopyItem Operation</span><span class="sxs-lookup"><span data-stu-id="9cd3e-103">CopyItem operation</span></span>

<span data-ttu-id="9cd3e-104">Der Vorgang **CopyItem** Elemente kopiert und werden die Elemente in einem anderen Ordner platziert.</span><span class="sxs-lookup"><span data-stu-id="9cd3e-104">The **CopyItem** operation copies items and puts the items in a different folder.</span></span> 
  
## <a name="copyitem-request-example"></a><span data-ttu-id="9cd3e-105">CopyItem anforderungsbeispiel</span><span class="sxs-lookup"><span data-stu-id="9cd3e-105">CopyItem request example</span></span>

### <a name="description"></a><span data-ttu-id="9cd3e-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9cd3e-106">Description</span></span>

<span data-ttu-id="9cd3e-107">Im folgenden Beispiel wird eine Anforderung **CopyItem** veranschaulicht das Formular einer Anforderung an ein Element in den Posteingang zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="9cd3e-107">The following example of a **CopyItem** request shows how to form a request to copy an item to the Inbox.</span></span> 
  
### <a name="code"></a><span data-ttu-id="9cd3e-108">Code</span><span class="sxs-lookup"><span data-stu-id="9cd3e-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CopyItem xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ToFolderId>
        <t:DistinguishedFolderId Id="inbox"/>
      </ToFolderId>
      <ItemIds>
        <t:ItemId Id="AS4AUnV="/>
      </ItemIds>
    </CopyItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="9cd3e-109">Kommentare</span><span class="sxs-lookup"><span data-stu-id="9cd3e-109">Comments</span></span>

> [!NOTE]
> <span data-ttu-id="9cd3e-110">Die Ordner-ID und der Änderungsschlüssel wurden gekürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="9cd3e-110">The folder ID and the change key have been shortened to preserve readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="9cd3e-111">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="9cd3e-111">Request elements</span></span>

<span data-ttu-id="9cd3e-112">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="9cd3e-112">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="9cd3e-113">CopyItem</span><span class="sxs-lookup"><span data-stu-id="9cd3e-113">CopyItem</span></span>](copyitem.md)
    
- [<span data-ttu-id="9cd3e-114">ToFolderId</span><span class="sxs-lookup"><span data-stu-id="9cd3e-114">ToFolderId</span></span>](tofolderid.md)
    
- [<span data-ttu-id="9cd3e-115">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="9cd3e-115">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="9cd3e-116">Artikelnummern ein.</span><span class="sxs-lookup"><span data-stu-id="9cd3e-116">ItemIds</span></span>](itemids.md)
    
- [<span data-ttu-id="9cd3e-117">ItemId</span><span class="sxs-lookup"><span data-stu-id="9cd3e-117">ItemId</span></span>](itemid.md)
    
> [!NOTE]
> <span data-ttu-id="9cd3e-118">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="9cd3e-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span> 
  
<span data-ttu-id="9cd3e-119">Wenn andere Optionen für die Anforderungsnachricht des Vorgangs **CopyItem** suchen möchten, verwenden Sie die Schemahierarchie.</span><span class="sxs-lookup"><span data-stu-id="9cd3e-119">To find other options for the request message of the **CopyItem** operation, explore the schema hierarchy.</span></span> <span data-ttu-id="9cd3e-120">Starten Sie das [CopyItem](copyitem.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="9cd3e-120">Start at the [CopyItem](copyitem.md) element.</span></span> 
  
## <a name="successful-copyitem-response"></a><span data-ttu-id="9cd3e-121">Erfolgreiche CopyItem Antwort</span><span class="sxs-lookup"><span data-stu-id="9cd3e-121">Successful CopyItem Response</span></span>

### <a name="description"></a><span data-ttu-id="9cd3e-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9cd3e-122">Description</span></span>

<span data-ttu-id="9cd3e-123">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die Anforderung **"CopyItem"** .</span><span class="sxs-lookup"><span data-stu-id="9cd3e-123">The following example shows a successful response to the **CopyItem** request.</span></span> 
  
<span data-ttu-id="9cd3e-124">Der Elementbezeichner des neuen Elements wird in der Antwortnachricht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9cd3e-124">The item identifier of the new item is returned in the response message.</span></span> <span data-ttu-id="9cd3e-125">Element-IDs werden nicht auf Öffentliche Ordner **CopyItem** Vorgänge in Antworten für postfachübergreifenden oder Postfach zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9cd3e-125">Item identifiers are not returned in responses for cross-mailbox or mailbox to public folder **CopyItem** operations.</span></span> 
  
### <a name="code"></a><span data-ttu-id="9cd3e-126">Code</span><span class="sxs-lookup"><span data-stu-id="9cd3e-126">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <CopyItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CopyItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Message>
              <t:ItemID Id="AAMkAd" ChangeKey="FwAAABY" />
            </t:Message>
          </m:Items>
        </m:CopyItemResponseMessage>
      </m:ResponseMessages>
    </CopyItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-response-elements"></a><span data-ttu-id="9cd3e-127">Elemente einer erfolgreichen Antwort</span><span class="sxs-lookup"><span data-stu-id="9cd3e-127">Successful response elements</span></span>

<span data-ttu-id="9cd3e-128">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="9cd3e-128">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="9cd3e-129">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="9cd3e-129">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="9cd3e-130">CopyItemResponse</span><span class="sxs-lookup"><span data-stu-id="9cd3e-130">CopyItemResponse</span></span>](copyitemresponse.md)
    
- [<span data-ttu-id="9cd3e-131">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="9cd3e-131">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="9cd3e-132">CopyItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="9cd3e-132">CopyItemResponseMessage</span></span>](copyitemresponsemessage.md)
    
- [<span data-ttu-id="9cd3e-133">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="9cd3e-133">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="9cd3e-134">Elemente</span><span class="sxs-lookup"><span data-stu-id="9cd3e-134">Items</span></span>](items.md)
    
<span data-ttu-id="9cd3e-135">Wenn andere Optionen für die Antwortnachricht des Vorgangs **CopyItem** suchen möchten, verwenden Sie die Schemahierarchie.</span><span class="sxs-lookup"><span data-stu-id="9cd3e-135">To find other options for the response message of the **CopyItem** operation, explore the schema hierarchy.</span></span> <span data-ttu-id="9cd3e-136">Starten Sie das [CopyItemResponse](copyitemresponse.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="9cd3e-136">Start at the [CopyItemResponse](copyitemresponse.md) element.</span></span> 
  
## <a name="copyitem-error-response"></a><span data-ttu-id="9cd3e-137">CopyItem Fehlerantwort</span><span class="sxs-lookup"><span data-stu-id="9cd3e-137">CopyItem error response</span></span>

### <a name="description"></a><span data-ttu-id="9cd3e-138">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9cd3e-138">Description</span></span>

<span data-ttu-id="9cd3e-139">Das folgende Beispiel zeigt eine Fehlerantwort an einer **"CopyItem"** Anforderung.</span><span class="sxs-lookup"><span data-stu-id="9cd3e-139">The following example shows an error response to a **CopyItem** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="9cd3e-140">Code</span><span class="sxs-lookup"><span data-stu-id="9cd3e-140">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <CopyItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CopyItemResponseMessage ResponseClass="Error">
          <m:MessageText>Id is malformed.</m:MessageText>
          <m:ResponseCode>ErrorInvalidIdMalformed</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:Items />
        </m:CopyItemResponseMessage>
      </m:ResponseMessages>
    </CopyItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a><span data-ttu-id="9cd3e-141">Fehler Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="9cd3e-141">Error response elements</span></span>

<span data-ttu-id="9cd3e-142">Folgende Elemente werden in der Fehlerantwort verwendet:</span><span class="sxs-lookup"><span data-stu-id="9cd3e-142">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="9cd3e-143">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="9cd3e-143">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="9cd3e-144">CopyItemResponse</span><span class="sxs-lookup"><span data-stu-id="9cd3e-144">CopyItemResponse</span></span>](copyitemresponse.md)
    
- [<span data-ttu-id="9cd3e-145">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="9cd3e-145">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="9cd3e-146">CopyItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="9cd3e-146">CopyItemResponseMessage</span></span>](copyitemresponsemessage.md)
    
- [<span data-ttu-id="9cd3e-147">MessageText</span><span class="sxs-lookup"><span data-stu-id="9cd3e-147">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="9cd3e-148">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="9cd3e-148">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="9cd3e-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="9cd3e-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="9cd3e-150">Elemente</span><span class="sxs-lookup"><span data-stu-id="9cd3e-150">Items</span></span>](items.md)
    
<span data-ttu-id="9cd3e-151">Wenn andere Optionen für die Fehlermeldung Antwort des Vorgangs **CopyItem** suchen möchten, verwenden Sie die Schemahierarchie.</span><span class="sxs-lookup"><span data-stu-id="9cd3e-151">To find other options for the error response message of the **CopyItem** operation, explore the schema hierarchy.</span></span> <span data-ttu-id="9cd3e-152">Starten Sie das [CopyItemResponse](copyitemresponse.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="9cd3e-152">Start at the [CopyItemResponse](copyitemresponse.md) element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9cd3e-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9cd3e-153">See also</span></span>



- [<span data-ttu-id="9cd3e-154">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="9cd3e-154">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

