---
title: SendItem-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SendItem
api_type:
- schema
ms.assetid: 337b89ef-e1b7-45ed-92f3-8abe4200e4c7
description: Der SendItem-Vorgang wird zum Senden von e-Mail-Nachrichten verwendet, die sich im Exchange-Informationsspeicher befinden.
ms.openlocfilehash: 9136379e50723211fe5a483c7f113da4fa125fc1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530338"
---
# <a name="senditem-operation"></a><span data-ttu-id="321dd-103">SendItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="321dd-103">SendItem operation</span></span>

<span data-ttu-id="321dd-104">Der SendItem-Vorgang wird zum Senden von e-Mail-Nachrichten verwendet, die sich im Exchange-Informationsspeicher befinden.</span><span class="sxs-lookup"><span data-stu-id="321dd-104">The SendItem operation is used to send e-mail messages that are located in the Exchange store.</span></span>
  
## <a name="senditem-e-mail-message-request-example"></a><span data-ttu-id="321dd-105">SendItem (e-Mail-Nachricht)-Anforderungs Beispiel</span><span class="sxs-lookup"><span data-stu-id="321dd-105">SendItem (E-mail Message) request example</span></span>

### <a name="description"></a><span data-ttu-id="321dd-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="321dd-106">Description</span></span>

<span data-ttu-id="321dd-107">Das folgende Beispiel zeigt, wie Sie eine e-Mail-Nachricht senden.</span><span class="sxs-lookup"><span data-stu-id="321dd-107">The following example shows how to send an e-mail message.</span></span>
  
### <a name="code"></a><span data-ttu-id="321dd-108">Code</span><span class="sxs-lookup"><span data-stu-id="321dd-108">Code</span></span>

```XML
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <SendItem xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" 
              SaveItemToFolder="true">
      <ItemIds>
        <t:ItemId Id="AAAtAEF=" ChangeKey="CQAAABY+T" />
      </ItemIds>
    </SendItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="321dd-109">Comments</span><span class="sxs-lookup"><span data-stu-id="321dd-109">Comments</span></span>

<span data-ttu-id="321dd-110">Die Element-ID wurde verkürzt, um die Lesbarkeit beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="321dd-110">The item identifier has been shortened to preserve readability.</span></span>
  
### <a name="request-elements"></a><span data-ttu-id="321dd-111">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="321dd-111">Request elements</span></span>

<span data-ttu-id="321dd-112">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="321dd-112">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="321dd-113">SendItem</span><span class="sxs-lookup"><span data-stu-id="321dd-113">SendItem</span></span>](senditem.md)
    
- [<span data-ttu-id="321dd-114">ItemIds</span><span class="sxs-lookup"><span data-stu-id="321dd-114">ItemIds</span></span>](itemids.md)
    
- [<span data-ttu-id="321dd-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="321dd-115">ItemId</span></span>](itemid.md)
    
## <a name="successful-senditem-e-mail-message-response"></a><span data-ttu-id="321dd-116">Erfolgreiche SendItem-Antwort (e-Mail-Nachricht)</span><span class="sxs-lookup"><span data-stu-id="321dd-116">Successful SendItem (E-mail Message) Response</span></span>

### <a name="description"></a><span data-ttu-id="321dd-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="321dd-117">Description</span></span>

<span data-ttu-id="321dd-118">Das folgende Beispiel zeigt eine erfolgreiche SendItem-Antwort.</span><span class="sxs-lookup"><span data-stu-id="321dd-118">The following example shows a successful SendItem response.</span></span>
  
### <a name="code"></a><span data-ttu-id="321dd-119">Code</span><span class="sxs-lookup"><span data-stu-id="321dd-119">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="602" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <SendItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:SendItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:SendItemResponseMessage>
      </m:ResponseMessages>
    </SendItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-response-elements"></a><span data-ttu-id="321dd-120">Erfolgreiche Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="321dd-120">Successful response elements</span></span>

<span data-ttu-id="321dd-121">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="321dd-121">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="321dd-122">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="321dd-122">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="321dd-123">SendItemResponse</span><span class="sxs-lookup"><span data-stu-id="321dd-123">SendItemResponse</span></span>](senditemresponse.md)
    
- [<span data-ttu-id="321dd-124">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="321dd-124">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="321dd-125">SendItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="321dd-125">SendItemResponseMessage</span></span>](senditemresponsemessage.md)
    
- [<span data-ttu-id="321dd-126">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="321dd-126">ResponseCode</span></span>](responsecode.md)
    
### <a name="comments"></a><span data-ttu-id="321dd-127">Kommentare</span><span class="sxs-lookup"><span data-stu-id="321dd-127">Comments</span></span>

<span data-ttu-id="321dd-128">Ein Stellvertreter, der versucht, eine e-Mail-Nachricht zu senden, die sich im Ordner "Entwürfe" des Prinzipals befindet, wobei die Option SendAndSaveCopy, um eine Kopie im Distinguished Folder gesendete Elemente zu speichern, automatisch fehlschlägt, um eine Kopie des gesendeten Elements in den Distinguished Folder für gesendete Elemente zu verlegen.</span><span class="sxs-lookup"><span data-stu-id="321dd-128">A delegate who tries to send an e-mail message that is located in the principal's Drafts folder with the SendAndSaveCopy option set to save a copy in the Sent Items distinguished folder will silently fail to move a copy of the sent item to the Sent Items distinguished folder.</span></span> <span data-ttu-id="321dd-129">Das Element bleibt im Ordner Entwürfe des Prinzipals erhalten.</span><span class="sxs-lookup"><span data-stu-id="321dd-129">The item will remain in the principal's Drafts folder.</span></span> <span data-ttu-id="321dd-130">Die Problemumgehung für dieses Problem besteht darin, das Postfach des Prinzipals im [DistinguishedFolderId](distinguishedfolderid.md) -Element anzugeben.</span><span class="sxs-lookup"><span data-stu-id="321dd-130">The workaround for this issue is to specify the principal's mailbox in the [DistinguishedFolderId](distinguishedfolderid.md) element.</span></span> 
  
<span data-ttu-id="321dd-131">Ein weiteres zu berücksichtigender Fall ist, wenn eine Stellvertretung eine e-Mail-Nachricht erstellt und im Ordner "Entwürfe" des Postfachs des Stellvertreters speichert.</span><span class="sxs-lookup"><span data-stu-id="321dd-131">An additional scenario to consider is when a delegate creates an e-mail message and saves it to the Drafts folder of the delegate's mailbox.</span></span> <span data-ttu-id="321dd-132">Wenn der Stellvertreter versucht, das Element zu senden und eine Kopie im Distinguished Items-Ordner des Prinzipals zu speichern, die Nachricht ordnungsgemäß gesendet wird, die Entwurfsnachricht im Ordner "Entwürfe" des Stellvertreters verbleibt, wird die gesendete Nachricht nicht im Ordner "Gesendete Elemente" des Stellvertreters oder des Prinzipals angezeigt, und die Antwort ist erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="321dd-132">If the delegate tries to send the item and save a copy to the principal's Sent Items distinguished folder, the message is sent correctly, the draft message remains in the delegate's Drafts folder, the sent message does not appear in either the delegate's or principal's Sent Items folder, and the response is a success.</span></span>
  
## <a name="invalid-senditem-e-mail-message-request-example"></a><span data-ttu-id="321dd-133">Ungültiges SendItem (e-Mail-Nachricht)-Anforderungs Beispiel</span><span class="sxs-lookup"><span data-stu-id="321dd-133">Invalid SendItem (E-mail Message) request example</span></span>

### <a name="description"></a><span data-ttu-id="321dd-134">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="321dd-134">Description</span></span>

<span data-ttu-id="321dd-135">Das folgende Codebeispiel zeigt ein Beispiel für eine Anforderung mit einem ungültigen Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="321dd-135">The following code sample shows an example of a request with an invalid identifier.</span></span>
  
### <a name="code"></a><span data-ttu-id="321dd-136">Code</span><span class="sxs-lookup"><span data-stu-id="321dd-136">Code</span></span>

```XML
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <SendItem xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" 
              SaveItemToFolder="true">
      <ItemIds>
        <t:ItemId Id="%BadItemId%" ChangeKey="CQAAABYAAA" />
      </ItemIds>
    </SendItem>
  </soap:Body>
</soap:Envelope>
```

## <a name="senditem-e-mail-message-error-response"></a><span data-ttu-id="321dd-137">SendItem (e-Mail-Nachricht)-Fehlerantwort</span><span class="sxs-lookup"><span data-stu-id="321dd-137">SendItem (E-mail Message) error response</span></span>

### <a name="description"></a><span data-ttu-id="321dd-138">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="321dd-138">Description</span></span>

<span data-ttu-id="321dd-139">Das folgende Beispiel zeigt eine Fehlerantwort auf eine SendItem-Anforderung, die einen ungültigen Bezeichner enthält.</span><span class="sxs-lookup"><span data-stu-id="321dd-139">The following example shows an error response to a SendItem request that contains an invalid identifier.</span></span>
  
### <a name="code"></a><span data-ttu-id="321dd-140">Code</span><span class="sxs-lookup"><span data-stu-id="321dd-140">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="602" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <SendItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:SendItemResponseMessage ResponseClass="Error">
          <m:MessageText>Id is malformed.</m:MessageText>
          <m:ResponseCode>ErrorInvalidIdMalformed</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:SendItemResponseMessage>
      </m:ResponseMessages>
    </SendItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a><span data-ttu-id="321dd-141">Fehlerantwortelemente</span><span class="sxs-lookup"><span data-stu-id="321dd-141">Error response elements</span></span>

<span data-ttu-id="321dd-142">Folgende Elemente werden in der Fehlerantwort verwendet:</span><span class="sxs-lookup"><span data-stu-id="321dd-142">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="321dd-143">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="321dd-143">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="321dd-144">SendItemResponse</span><span class="sxs-lookup"><span data-stu-id="321dd-144">SendItemResponse</span></span>](senditemresponse.md)
    
- [<span data-ttu-id="321dd-145">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="321dd-145">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="321dd-146">SendItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="321dd-146">SendItemResponseMessage</span></span>](senditemresponsemessage.md)
    
- [<span data-ttu-id="321dd-147">MessageText</span><span class="sxs-lookup"><span data-stu-id="321dd-147">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="321dd-148">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="321dd-148">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="321dd-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="321dd-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="321dd-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="321dd-150">See also</span></span>



[<span data-ttu-id="321dd-151">SendItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="321dd-151">SendItem operation</span></span>](senditem-operation.md)
  
 <span data-ttu-id="321dd-152">**SendItemType**</span><span class="sxs-lookup"><span data-stu-id="321dd-152">**SendItemType**</span></span>


- [<span data-ttu-id="321dd-153">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="321dd-153">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

