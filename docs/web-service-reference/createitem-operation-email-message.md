---
title: CreateItem-Vorgang (e-Mail-Nachricht)
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
ms.assetid: fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1
description: Der CreateItem-Vorgang wird verwendet, um e-Mail-Nachrichten zu erstellen.
ms.openlocfilehash: 591209165cfbafc2d5f4036dd8fab6659523a044
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757777"
---
# <a name="createitem-operation-email-message"></a><span data-ttu-id="f718b-103">CreateItem-Vorgang (e-Mail-Nachricht)</span><span class="sxs-lookup"><span data-stu-id="f718b-103">CreateItem operation (email message)</span></span>

<span data-ttu-id="f718b-104">Der CreateItem-Vorgang wird verwendet, um e-Mail-Nachrichten zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f718b-104">The CreateItem operation is used to create e-mail messages.</span></span>
  
## <a name="createitem-request-example"></a><span data-ttu-id="f718b-105">CreateItem anforderungsbeispiel</span><span class="sxs-lookup"><span data-stu-id="f718b-105">CreateItem request example</span></span>

### <a name="description"></a><span data-ttu-id="f718b-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f718b-106">Description</span></span>

<span data-ttu-id="f718b-107">Im folgenden Beispiel wird eine Anforderung CreateItem veranschaulicht erstellen Sie eine neue e-Mail-Nachricht, senden Sie die Nachricht, und speichern eine Kopie davon im Ordner "Entwürfe".</span><span class="sxs-lookup"><span data-stu-id="f718b-107">The following example of a CreateItem request shows how to create a new e-mail message, send the message, and save a copy of it in the drafts folder.</span></span>
  
### <a name="code"></a><span data-ttu-id="f718b-108">Code</span><span class="sxs-lookup"><span data-stu-id="f718b-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateItem MessageDisposition="SendAndSaveCopy" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <SavedItemFolderId>
        <t:DistinguishedFolderId Id="drafts" />
      </SavedItemFolderId>
      <Items>
        <t:Message>
          <t:ItemClass>IPM.Note</t:ItemClass>
          <t:Subject>Project Action</t:Subject>
          <t:Body BodyType="Text">Priority - Update specification</t:Body>
          <t:ToRecipients>
            <t:Mailbox>
              <t:EmailAddress>sschmidt@example.com</t:EmailAddress>
            </t:Mailbox>
          </t:ToRecipients>
          <t:IsRead>false</t:IsRead>
        </t:Message>
      </Items>
    </CreateItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a><span data-ttu-id="f718b-109">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="f718b-109">Request elements</span></span>

<span data-ttu-id="f718b-110">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="f718b-110">The following elements are used in the request:</span></span> 
  
- [<span data-ttu-id="f718b-111">CreateItem</span><span class="sxs-lookup"><span data-stu-id="f718b-111">CreateItem</span></span>](createitem.md)
    
- [<span data-ttu-id="f718b-112">Des SavedItemFolderId</span><span class="sxs-lookup"><span data-stu-id="f718b-112">SavedItemFolderId</span></span>](saveditemfolderid.md)
    
- [<span data-ttu-id="f718b-113">Elemente (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="f718b-113">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md)
    
- [<span data-ttu-id="f718b-114">Message</span><span class="sxs-lookup"><span data-stu-id="f718b-114">Message</span></span>](message-ex15websvcsotherref.md)
    
- [<span data-ttu-id="f718b-115">ItemClass</span><span class="sxs-lookup"><span data-stu-id="f718b-115">ItemClass</span></span>](itemclass.md)
    
- [<span data-ttu-id="f718b-116">Betreff</span><span class="sxs-lookup"><span data-stu-id="f718b-116">Subject</span></span>](subject.md)
    
- [<span data-ttu-id="f718b-117">Body</span><span class="sxs-lookup"><span data-stu-id="f718b-117">Body</span></span>](body.md)
    
- [<span data-ttu-id="f718b-118">ToRecipients</span><span class="sxs-lookup"><span data-stu-id="f718b-118">ToRecipients</span></span>](torecipients.md)
    
- [<span data-ttu-id="f718b-119">Postfach</span><span class="sxs-lookup"><span data-stu-id="f718b-119">Mailbox</span></span>](mailbox.md)
    
- [<span data-ttu-id="f718b-120">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="f718b-120">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md)
    
- [<span data-ttu-id="f718b-121">IsRead</span><span class="sxs-lookup"><span data-stu-id="f718b-121">IsRead</span></span>](isread.md)
    
<span data-ttu-id="f718b-122">Um weitere Optionen für die Anforderung an den CreateItem Operation zu suchen, verwenden Sie die Schemahierarchie.</span><span class="sxs-lookup"><span data-stu-id="f718b-122">To find other options for the request message of the CreateItem operation, explore the schema hierarchy.</span></span> <span data-ttu-id="f718b-123">Starten Sie die [CreateItem](createitem.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="f718b-123">Start at the [CreateItem](createitem.md) element.</span></span> 
  
## <a name="successful-createitem-response"></a><span data-ttu-id="f718b-124">Erfolgreiche CreateItem-Antwort</span><span class="sxs-lookup"><span data-stu-id="f718b-124">Successful CreateItem Response</span></span>

### <a name="description"></a><span data-ttu-id="f718b-125">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f718b-125">Description</span></span>

<span data-ttu-id="f718b-126">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die CreateItem-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="f718b-126">The following example shows a successful response to the CreateItem request.</span></span>
  
### <a name="code"></a><span data-ttu-id="f718b-127">Code</span><span class="sxs-lookup"><span data-stu-id="f718b-127">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
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

### <a name="successful-response-elements"></a><span data-ttu-id="f718b-128">Elemente einer erfolgreichen Antwort</span><span class="sxs-lookup"><span data-stu-id="f718b-128">Successful response elements</span></span>

<span data-ttu-id="f718b-129">Die folgenden Elemente werden in der Antwort enthalten:</span><span class="sxs-lookup"><span data-stu-id="f718b-129">The following elements are included in the response:</span></span> 
  
- [<span data-ttu-id="f718b-130">CreateItemResponse</span><span class="sxs-lookup"><span data-stu-id="f718b-130">CreateItemResponse</span></span>](createitemresponse.md)
    
- [<span data-ttu-id="f718b-131">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="f718b-131">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="f718b-132">CreateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="f718b-132">CreateItemResponseMessage</span></span>](createitemresponsemessage.md)
    
- [<span data-ttu-id="f718b-133">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="f718b-133">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="f718b-134">Elemente</span><span class="sxs-lookup"><span data-stu-id="f718b-134">Items</span></span>](items.md)
    
<span data-ttu-id="f718b-135">Wenn andere Optionen für die Antwortnachricht des Vorgangs CreateItem suchen möchten, verwenden Sie die Schemahierarchie.</span><span class="sxs-lookup"><span data-stu-id="f718b-135">To find other options for the response message of the CreateItem operation, explore the schema hierarchy.</span></span> <span data-ttu-id="f718b-136">Starten Sie das [CreateItemResponse](createitemresponse.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="f718b-136">Start at the [CreateItemResponse](createitemresponse.md) element.</span></span> 
  
## <a name="error-createitem-response"></a><span data-ttu-id="f718b-137">CreateItem Fehlerantwort</span><span class="sxs-lookup"><span data-stu-id="f718b-137">Error CreateItem Response</span></span>

### <a name="description"></a><span data-ttu-id="f718b-138">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f718b-138">Description</span></span>

<span data-ttu-id="f718b-139">Das folgende Beispiel zeigt eine Fehlerantwort an eine CreateItem-Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="f718b-139">The following example shows an error response to a CreateItem request.</span></span>
  
### <a name="code"></a><span data-ttu-id="f718b-140">Code</span><span class="sxs-lookup"><span data-stu-id="f718b-140">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <CreateItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateItemResponseMessage ResponseClass="Error">
          <m:MessageText>The user account which was used to submit this request does not have the right to send mail on behalf of the specified sending account.</m:MessageText>
          <m:ResponseCode>ErrorSendAsDenied</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:Items />
        </m:CreateItemResponseMessage>
      </m:ResponseMessages>
    </CreateItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a><span data-ttu-id="f718b-141">Fehler Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="f718b-141">Error response elements</span></span>

<span data-ttu-id="f718b-142">Folgende Elemente werden in der Fehlerantwort verwendet:</span><span class="sxs-lookup"><span data-stu-id="f718b-142">The following elements are used in the error response:</span></span> 
  
- [<span data-ttu-id="f718b-143">CreateItemResponse</span><span class="sxs-lookup"><span data-stu-id="f718b-143">CreateItemResponse</span></span>](createitemresponse.md)
    
- [<span data-ttu-id="f718b-144">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="f718b-144">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="f718b-145">CreateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="f718b-145">CreateItemResponseMessage</span></span>](createitemresponsemessage.md)
    
- [<span data-ttu-id="f718b-146">MessageText</span><span class="sxs-lookup"><span data-stu-id="f718b-146">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="f718b-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="f718b-147">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="f718b-148">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="f718b-148">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="f718b-149">Elemente</span><span class="sxs-lookup"><span data-stu-id="f718b-149">Items</span></span>](items.md)
    
<span data-ttu-id="f718b-150">Wenn andere Optionen für die Fehlermeldung Antwort des Vorgangs CreateItem suchen möchten, verwenden Sie die Schemahierarchie.</span><span class="sxs-lookup"><span data-stu-id="f718b-150">To find other options for the error response message of the CreateItem operation, explore the schema hierarchy.</span></span> <span data-ttu-id="f718b-151">Starten Sie das [CreateItemResponse](createitemresponse.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="f718b-151">Start at the [CreateItemResponse](createitemresponse.md) element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f718b-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f718b-152">See also</span></span>



[<span data-ttu-id="f718b-153">CreateItem Operation</span><span class="sxs-lookup"><span data-stu-id="f718b-153">CreateItem operation</span></span>](createitem-operation.md)

