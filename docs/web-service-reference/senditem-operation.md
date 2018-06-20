---
title: SendItem Operation
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
description: Den SendItem-Vorgang wird verwendet, um e-Mail-Nachrichten senden, die sich im Exchange-Speicher.
ms.openlocfilehash: 780778b1599d0d5e5f4b6e5b58b67773bbe18cda
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831336"
---
# <a name="senditem-operation"></a><span data-ttu-id="72574-103">SendItem Operation</span><span class="sxs-lookup"><span data-stu-id="72574-103">SendItem operation</span></span>

<span data-ttu-id="72574-104">Den SendItem-Vorgang wird verwendet, um e-Mail-Nachrichten senden, die sich im Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="72574-104">The SendItem operation is used to send e-mail messages that are located in the Exchange store.</span></span>
  
## <a name="senditem-e-mail-message-request-example"></a><span data-ttu-id="72574-105">Anforderungsbeispiel den SendItem (e-Mail-Nachricht)</span><span class="sxs-lookup"><span data-stu-id="72574-105">SendItem (E-mail Message) request example</span></span>

### <a name="description"></a><span data-ttu-id="72574-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="72574-106">Description</span></span>

<span data-ttu-id="72574-107">Im folgenden Beispiel wird gezeigt, wie eine e-Mail-Nachricht senden.</span><span class="sxs-lookup"><span data-stu-id="72574-107">The following example shows how to send an e-mail message.</span></span>
  
### <a name="code"></a><span data-ttu-id="72574-108">Code</span><span class="sxs-lookup"><span data-stu-id="72574-108">Code</span></span>

```XML
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <SendItem xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" 
              SaveItemToFolder="true">
      <ItemIds>
        <t:ItemId Id="AAAtAEF=" ChangeKey="CQAAABY+T" />
      </ItemIds>
    </SendItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="72574-109">Kommentare</span><span class="sxs-lookup"><span data-stu-id="72574-109">Comments</span></span>

<span data-ttu-id="72574-110">Der Elementbezeichner wurde gekürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="72574-110">The item identifier has been shortened to preserve readability.</span></span>
  
### <a name="request-elements"></a><span data-ttu-id="72574-111">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="72574-111">Request elements</span></span>

<span data-ttu-id="72574-112">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="72574-112">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="72574-113">SendItem</span><span class="sxs-lookup"><span data-stu-id="72574-113">SendItem</span></span>](senditem.md)
    
- [<span data-ttu-id="72574-114">Artikelnummern ein.</span><span class="sxs-lookup"><span data-stu-id="72574-114">ItemIds</span></span>](itemids.md)
    
- [<span data-ttu-id="72574-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="72574-115">ItemId</span></span>](itemid.md)
    
## <a name="successful-senditem-e-mail-message-response"></a><span data-ttu-id="72574-116">Antwort von den erfolgreichen SendItem (e-Mail-Nachricht)</span><span class="sxs-lookup"><span data-stu-id="72574-116">Successful SendItem (E-mail Message) Response</span></span>

### <a name="description"></a><span data-ttu-id="72574-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="72574-117">Description</span></span>

<span data-ttu-id="72574-118">Das folgende Beispiel zeigt eine erfolgreiche Antwort den SendItem.</span><span class="sxs-lookup"><span data-stu-id="72574-118">The following example shows a successful SendItem response.</span></span>
  
### <a name="code"></a><span data-ttu-id="72574-119">Code</span><span class="sxs-lookup"><span data-stu-id="72574-119">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="602" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <SendItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:SendItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:SendItemResponseMessage>
      </m:ResponseMessages>
    </SendItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-response-elements"></a><span data-ttu-id="72574-120">Elemente einer erfolgreichen Antwort</span><span class="sxs-lookup"><span data-stu-id="72574-120">Successful response elements</span></span>

<span data-ttu-id="72574-121">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="72574-121">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="72574-122">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="72574-122">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="72574-123">SendItemResponse</span><span class="sxs-lookup"><span data-stu-id="72574-123">SendItemResponse</span></span>](senditemresponse.md)
    
- [<span data-ttu-id="72574-124">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="72574-124">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="72574-125">SendItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="72574-125">SendItemResponseMessage</span></span>](senditemresponsemessage.md)
    
- [<span data-ttu-id="72574-126">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="72574-126">ResponseCode</span></span>](responsecode.md)
    
### <a name="comments"></a><span data-ttu-id="72574-127">Kommentare</span><span class="sxs-lookup"><span data-stu-id="72574-127">Comments</span></span>

<span data-ttu-id="72574-128">Eine Stellvertretung, die versucht, eine E-mail-Nachricht zu senden, im Ordner "Entwürfe" des Prinzipals mit der SendAndSaveCopy Option festlegen, um eine Kopie in gesendete Objekte speichern definierter Ordner automatisch ein Fehler auftritt, um eine Kopie des Elements gesendete auf gesendete Objekte definierten verschieben Ordner.</span><span class="sxs-lookup"><span data-stu-id="72574-128">A delegate who tries to send an e-mail message that is located in the principal's Drafts folder with the SendAndSaveCopy option set to save a copy in the Sent Items distinguished folder will silently fail to move a copy of the sent item to the Sent Items distinguished folder.</span></span> <span data-ttu-id="72574-129">Das Element verbleibt im Ordner "Entwürfe" des Prinzipals.</span><span class="sxs-lookup"><span data-stu-id="72574-129">The item will remain in the principal's Drafts folder.</span></span> <span data-ttu-id="72574-130">Die Umgehung für dieses Problem ist der Prinzipal Postfach im [DistinguishedFolderId](distinguishedfolderid.md) -Element angeben.</span><span class="sxs-lookup"><span data-stu-id="72574-130">The workaround for this issue is to specify the principal's mailbox in the [DistinguishedFolderId](distinguishedfolderid.md) element.</span></span> 
  
<span data-ttu-id="72574-131">Ein zusätzliches Szenario zu berücksichtigende ist, wenn ein Stellvertreter eine E-mail-Nachricht erstellt und ihn im Ordner "Entwürfe" des Postfachs der Stellvertretung speichert.</span><span class="sxs-lookup"><span data-stu-id="72574-131">An additional scenario to consider is when a delegate creates an e-mail message and saves it to the Drafts folder of the delegate's mailbox.</span></span> <span data-ttu-id="72574-132">Wenn die Stellvertretung versucht, senden das Element und Speichern einer Kopie des Prinzipals gesendete Objekte definierten Ordner, wird die Nachricht ordnungsgemäß gesendet die Entwurf einer Nachricht im Ordner Entwürfe der Stellvertretung, bleibt die gesendete Nachricht wird nicht in die Stellvertretung oder des Prinzipals angezeigt. Ordner Gesendete Objekte, und die Antwort erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="72574-132">If the delegate tries to send the item and save a copy to the principal's Sent Items distinguished folder, the message is sent correctly, the draft message remains in the delegate's Drafts folder, the sent message does not appear in either the delegate's or principal's Sent Items folder, and the response is a success.</span></span>
  
## <a name="invalid-senditem-e-mail-message-request-example"></a><span data-ttu-id="72574-133">Ungültige Anforderung-Beispiel für den SendItem (e-Mail-Nachricht)</span><span class="sxs-lookup"><span data-stu-id="72574-133">Invalid SendItem (E-mail Message) request example</span></span>

### <a name="description"></a><span data-ttu-id="72574-134">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="72574-134">Description</span></span>

<span data-ttu-id="72574-135">Das folgende Codebeispiel zeigt ein Beispiel für eine Anforderung mit einem ungültigen Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="72574-135">The following code sample shows an example of a request with an invalid identifier.</span></span>
  
### <a name="code"></a><span data-ttu-id="72574-136">Code</span><span class="sxs-lookup"><span data-stu-id="72574-136">Code</span></span>

```XML
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <SendItem xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" 
              SaveItemToFolder="true">
      <ItemIds>
        <t:ItemId Id="%BadItemId%" ChangeKey="CQAAABYAAA" />
      </ItemIds>
    </SendItem>
  </soap:Body>
</soap:Envelope>
```

## <a name="senditem-e-mail-message-error-response"></a><span data-ttu-id="72574-137">Fehlerantwort den SendItem (e-Mail-Nachricht)</span><span class="sxs-lookup"><span data-stu-id="72574-137">SendItem (E-mail Message) error response</span></span>

### <a name="description"></a><span data-ttu-id="72574-138">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="72574-138">Description</span></span>

<span data-ttu-id="72574-139">Das folgende Beispiel zeigt eine Fehlerantwort an eine den SendItem-Anforderung, die einen ungültigen Bezeichner enthält.</span><span class="sxs-lookup"><span data-stu-id="72574-139">The following example shows an error response to a SendItem request that contains an invalid identifier.</span></span>
  
### <a name="code"></a><span data-ttu-id="72574-140">Code</span><span class="sxs-lookup"><span data-stu-id="72574-140">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="602" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <SendItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="error-response-elements"></a><span data-ttu-id="72574-141">Fehler Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="72574-141">Error response elements</span></span>

<span data-ttu-id="72574-142">Folgende Elemente werden in der Fehlerantwort verwendet:</span><span class="sxs-lookup"><span data-stu-id="72574-142">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="72574-143">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="72574-143">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="72574-144">SendItemResponse</span><span class="sxs-lookup"><span data-stu-id="72574-144">SendItemResponse</span></span>](senditemresponse.md)
    
- [<span data-ttu-id="72574-145">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="72574-145">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="72574-146">SendItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="72574-146">SendItemResponseMessage</span></span>](senditemresponsemessage.md)
    
- [<span data-ttu-id="72574-147">MessageText</span><span class="sxs-lookup"><span data-stu-id="72574-147">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="72574-148">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="72574-148">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="72574-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="72574-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="72574-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="72574-150">See also</span></span>



[<span data-ttu-id="72574-151">SendItem Operation</span><span class="sxs-lookup"><span data-stu-id="72574-151">SendItem operation</span></span>](senditem-operation.md)
  
 <span data-ttu-id="72574-152">**SendItemType**</span><span class="sxs-lookup"><span data-stu-id="72574-152">**SendItemType**</span></span>


- [<span data-ttu-id="72574-153">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="72574-153">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

