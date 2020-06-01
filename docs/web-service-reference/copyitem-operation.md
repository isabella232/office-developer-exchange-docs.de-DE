---
title: CopyItem-Vorgang
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
description: Der CopyItem-Vorgang kopiert Elemente und fügt die Elemente in einen anderen Ordner ein.
ms.openlocfilehash: ec07700a5ebbdc8774aa2134919634b8dfd02406
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462178"
---
# <a name="copyitem-operation"></a><span data-ttu-id="5dfa5-103">CopyItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="5dfa5-103">CopyItem operation</span></span>

<span data-ttu-id="5dfa5-104">Der **CopyItem** -Vorgang kopiert Elemente und fügt die Elemente in einen anderen Ordner ein.</span><span class="sxs-lookup"><span data-stu-id="5dfa5-104">The **CopyItem** operation copies items and puts the items in a different folder.</span></span> 
  
## <a name="copyitem-request-example"></a><span data-ttu-id="5dfa5-105">CopyItem-Anforderungs Beispiel</span><span class="sxs-lookup"><span data-stu-id="5dfa5-105">CopyItem request example</span></span>

### <a name="description"></a><span data-ttu-id="5dfa5-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5dfa5-106">Description</span></span>

<span data-ttu-id="5dfa5-107">Im folgenden Beispiel einer **CopyItem** -Anforderung wird gezeigt, wie eine Anforderung zum Kopieren eines Elements in den Posteingang bildet.</span><span class="sxs-lookup"><span data-stu-id="5dfa5-107">The following example of a **CopyItem** request shows how to form a request to copy an item to the Inbox.</span></span> 
  
### <a name="code"></a><span data-ttu-id="5dfa5-108">Code</span><span class="sxs-lookup"><span data-stu-id="5dfa5-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CopyItem xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a><span data-ttu-id="5dfa5-109">Comments</span><span class="sxs-lookup"><span data-stu-id="5dfa5-109">Comments</span></span>

> [!NOTE]
> <span data-ttu-id="5dfa5-110">Die Ordner-ID und der Change-Schlüssel wurden verkürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="5dfa5-110">The folder ID and the change key have been shortened to preserve readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="5dfa5-111">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="5dfa5-111">Request elements</span></span>

<span data-ttu-id="5dfa5-112">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="5dfa5-112">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="5dfa5-113">CopyItem</span><span class="sxs-lookup"><span data-stu-id="5dfa5-113">CopyItem</span></span>](copyitem.md)
    
- [<span data-ttu-id="5dfa5-114">Tofolder-Datei</span><span class="sxs-lookup"><span data-stu-id="5dfa5-114">ToFolderId</span></span>](tofolderid.md)
    
- [<span data-ttu-id="5dfa5-115">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="5dfa5-115">DistinguishedFolderId</span></span>](distinguishedfolderid.md)
    
- [<span data-ttu-id="5dfa5-116">ItemIds</span><span class="sxs-lookup"><span data-stu-id="5dfa5-116">ItemIds</span></span>](itemids.md)
    
- [<span data-ttu-id="5dfa5-117">ItemId</span><span class="sxs-lookup"><span data-stu-id="5dfa5-117">ItemId</span></span>](itemid.md)
    
> [!NOTE]
> <span data-ttu-id="5dfa5-118">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="5dfa5-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span> 
  
<span data-ttu-id="5dfa5-119">Um andere Optionen für die Anforderungsnachricht des **CopyItem** -Vorgangs zu finden, erkunden Sie die Schemahierarchie.</span><span class="sxs-lookup"><span data-stu-id="5dfa5-119">To find other options for the request message of the **CopyItem** operation, explore the schema hierarchy.</span></span> <span data-ttu-id="5dfa5-120">Beginnen Sie mit dem [CopyItem](copyitem.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="5dfa5-120">Start at the [CopyItem](copyitem.md) element.</span></span> 
  
## <a name="successful-copyitem-response"></a><span data-ttu-id="5dfa5-121">Erfolgreiche CopyItem-Antwort</span><span class="sxs-lookup"><span data-stu-id="5dfa5-121">Successful CopyItem Response</span></span>

### <a name="description"></a><span data-ttu-id="5dfa5-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5dfa5-122">Description</span></span>

<span data-ttu-id="5dfa5-123">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die **CopyItem** -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="5dfa5-123">The following example shows a successful response to the **CopyItem** request.</span></span> 
  
<span data-ttu-id="5dfa5-124">Die Element-ID des neuen Elements wird in der Antwortnachricht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5dfa5-124">The item identifier of the new item is returned in the response message.</span></span> <span data-ttu-id="5dfa5-125">Element-IDs werden nicht in den Antworten für Postfächer-oder Postfach- **CopyItem** -Vorgänge im öffentlichen Ordner zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5dfa5-125">Item identifiers are not returned in responses for cross-mailbox or mailbox to public folder **CopyItem** operations.</span></span> 
  
### <a name="code"></a><span data-ttu-id="5dfa5-126">Code</span><span class="sxs-lookup"><span data-stu-id="5dfa5-126">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <CopyItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="successful-response-elements"></a><span data-ttu-id="5dfa5-127">Erfolgreiche Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="5dfa5-127">Successful response elements</span></span>

<span data-ttu-id="5dfa5-128">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="5dfa5-128">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="5dfa5-129">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="5dfa5-129">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="5dfa5-130">CopyItemResponse</span><span class="sxs-lookup"><span data-stu-id="5dfa5-130">CopyItemResponse</span></span>](copyitemresponse.md)
    
- [<span data-ttu-id="5dfa5-131">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="5dfa5-131">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="5dfa5-132">CopyItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="5dfa5-132">CopyItemResponseMessage</span></span>](copyitemresponsemessage.md)
    
- [<span data-ttu-id="5dfa5-133">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="5dfa5-133">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="5dfa5-134">Items</span><span class="sxs-lookup"><span data-stu-id="5dfa5-134">Items</span></span>](items.md)
    
<span data-ttu-id="5dfa5-135">Um andere Optionen für die Antwortnachricht des **CopyItem** -Vorgangs zu finden, erkunden Sie die Schemahierarchie.</span><span class="sxs-lookup"><span data-stu-id="5dfa5-135">To find other options for the response message of the **CopyItem** operation, explore the schema hierarchy.</span></span> <span data-ttu-id="5dfa5-136">Beginnen Sie mit dem [CopyItemResponse](copyitemresponse.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="5dfa5-136">Start at the [CopyItemResponse](copyitemresponse.md) element.</span></span> 
  
## <a name="copyitem-error-response"></a><span data-ttu-id="5dfa5-137">CopyItem-Fehlerantwort</span><span class="sxs-lookup"><span data-stu-id="5dfa5-137">CopyItem error response</span></span>

### <a name="description"></a><span data-ttu-id="5dfa5-138">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5dfa5-138">Description</span></span>

<span data-ttu-id="5dfa5-139">Das folgende Beispiel zeigt eine Fehlerantwort auf eine **CopyItem** -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="5dfa5-139">The following example shows an error response to a **CopyItem** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="5dfa5-140">Code</span><span class="sxs-lookup"><span data-stu-id="5dfa5-140">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <CopyItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="error-response-elements"></a><span data-ttu-id="5dfa5-141">Fehlerantwortelemente</span><span class="sxs-lookup"><span data-stu-id="5dfa5-141">Error response elements</span></span>

<span data-ttu-id="5dfa5-142">Folgende Elemente werden in der Fehlerantwort verwendet:</span><span class="sxs-lookup"><span data-stu-id="5dfa5-142">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="5dfa5-143">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="5dfa5-143">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="5dfa5-144">CopyItemResponse</span><span class="sxs-lookup"><span data-stu-id="5dfa5-144">CopyItemResponse</span></span>](copyitemresponse.md)
    
- [<span data-ttu-id="5dfa5-145">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="5dfa5-145">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="5dfa5-146">CopyItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="5dfa5-146">CopyItemResponseMessage</span></span>](copyitemresponsemessage.md)
    
- [<span data-ttu-id="5dfa5-147">MessageText</span><span class="sxs-lookup"><span data-stu-id="5dfa5-147">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="5dfa5-148">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="5dfa5-148">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="5dfa5-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="5dfa5-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="5dfa5-150">Items</span><span class="sxs-lookup"><span data-stu-id="5dfa5-150">Items</span></span>](items.md)
    
<span data-ttu-id="5dfa5-151">Weitere Optionen für die Fehlerantwort Meldung des **CopyItem** -Vorgangs finden Sie unter Durchsuchen der Schemahierarchie.</span><span class="sxs-lookup"><span data-stu-id="5dfa5-151">To find other options for the error response message of the **CopyItem** operation, explore the schema hierarchy.</span></span> <span data-ttu-id="5dfa5-152">Beginnen Sie mit dem [CopyItemResponse](copyitemresponse.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="5dfa5-152">Start at the [CopyItemResponse](copyitemresponse.md) element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5dfa5-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5dfa5-153">See also</span></span>



- [<span data-ttu-id="5dfa5-154">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="5dfa5-154">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

