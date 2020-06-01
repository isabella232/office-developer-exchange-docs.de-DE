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
description: Der CreateItem-Vorgang wird zum Erstellen von e-Mail-Nachrichten verwendet.
ms.openlocfilehash: 384ed8ff653029c2b7db0b36986d85842b0a06cf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457116"
---
# <a name="createitem-operation-email-message"></a><span data-ttu-id="39bc4-103">CreateItem-Vorgang (e-Mail-Nachricht)</span><span class="sxs-lookup"><span data-stu-id="39bc4-103">CreateItem operation (email message)</span></span>

<span data-ttu-id="39bc4-104">Der CreateItem-Vorgang wird zum Erstellen von e-Mail-Nachrichten verwendet.</span><span class="sxs-lookup"><span data-stu-id="39bc4-104">The CreateItem operation is used to create e-mail messages.</span></span>
  
## <a name="createitem-request-example"></a><span data-ttu-id="39bc4-105">CreateItem-Anforderungs Beispiel</span><span class="sxs-lookup"><span data-stu-id="39bc4-105">CreateItem request example</span></span>

### <a name="description"></a><span data-ttu-id="39bc4-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="39bc4-106">Description</span></span>

<span data-ttu-id="39bc4-107">Im folgenden Beispiel einer CreateItem-Anforderung wird gezeigt, wie Sie eine neue e-Mail-Nachricht erstellen, die Nachricht senden und eine Kopie davon im Ordner "Entwürfe" speichern.</span><span class="sxs-lookup"><span data-stu-id="39bc4-107">The following example of a CreateItem request shows how to create a new e-mail message, send the message, and save a copy of it in the drafts folder.</span></span>
  
### <a name="code"></a><span data-ttu-id="39bc4-108">Code</span><span class="sxs-lookup"><span data-stu-id="39bc4-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateItem MessageDisposition="SendAndSaveCopy" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="request-elements"></a><span data-ttu-id="39bc4-109">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="39bc4-109">Request elements</span></span>

<span data-ttu-id="39bc4-110">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="39bc4-110">The following elements are used in the request:</span></span> 
  
- [<span data-ttu-id="39bc4-111">CreateItem</span><span class="sxs-lookup"><span data-stu-id="39bc4-111">CreateItem</span></span>](createitem.md)
    
- [<span data-ttu-id="39bc4-112">SavedItemFolderId</span><span class="sxs-lookup"><span data-stu-id="39bc4-112">SavedItemFolderId</span></span>](saveditemfolderid.md)
    
- [<span data-ttu-id="39bc4-113">Elemente (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="39bc4-113">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md)
    
- [<span data-ttu-id="39bc4-114">Nachricht</span><span class="sxs-lookup"><span data-stu-id="39bc4-114">Message</span></span>](message-ex15websvcsotherref.md)
    
- [<span data-ttu-id="39bc4-115">ItemClass</span><span class="sxs-lookup"><span data-stu-id="39bc4-115">ItemClass</span></span>](itemclass.md)
    
- [<span data-ttu-id="39bc4-116">Betreff</span><span class="sxs-lookup"><span data-stu-id="39bc4-116">Subject</span></span>](subject.md)
    
- [<span data-ttu-id="39bc4-117">Body</span><span class="sxs-lookup"><span data-stu-id="39bc4-117">Body</span></span>](body.md)
    
- [<span data-ttu-id="39bc4-118">ToRecipients</span><span class="sxs-lookup"><span data-stu-id="39bc4-118">ToRecipients</span></span>](torecipients.md)
    
- [<span data-ttu-id="39bc4-119">Postfach</span><span class="sxs-lookup"><span data-stu-id="39bc4-119">Mailbox</span></span>](mailbox.md)
    
- [<span data-ttu-id="39bc4-120">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="39bc4-120">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md)
    
- [<span data-ttu-id="39bc4-121">IsRead</span><span class="sxs-lookup"><span data-stu-id="39bc4-121">IsRead</span></span>](isread.md)
    
<span data-ttu-id="39bc4-122">Um andere Optionen für die Anforderungsnachricht des CreateItem-Vorgangs zu finden, erkunden Sie die Schemahierarchie.</span><span class="sxs-lookup"><span data-stu-id="39bc4-122">To find other options for the request message of the CreateItem operation, explore the schema hierarchy.</span></span> <span data-ttu-id="39bc4-123">Beginnen Sie beim [CreateItem](createitem.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="39bc4-123">Start at the [CreateItem](createitem.md) element.</span></span> 
  
## <a name="successful-createitem-response"></a><span data-ttu-id="39bc4-124">Erfolgreiche CreateItem-Antwort</span><span class="sxs-lookup"><span data-stu-id="39bc4-124">Successful CreateItem Response</span></span>

### <a name="description"></a><span data-ttu-id="39bc4-125">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="39bc4-125">Description</span></span>

<span data-ttu-id="39bc4-126">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die CreateItem-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="39bc4-126">The following example shows a successful response to the CreateItem request.</span></span>
  
### <a name="code"></a><span data-ttu-id="39bc4-127">Code</span><span class="sxs-lookup"><span data-stu-id="39bc4-127">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
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

### <a name="successful-response-elements"></a><span data-ttu-id="39bc4-128">Erfolgreiche Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="39bc4-128">Successful response elements</span></span>

<span data-ttu-id="39bc4-129">Die Antwort enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="39bc4-129">The following elements are included in the response:</span></span> 
  
- [<span data-ttu-id="39bc4-130">CreateItemResponse</span><span class="sxs-lookup"><span data-stu-id="39bc4-130">CreateItemResponse</span></span>](createitemresponse.md)
    
- [<span data-ttu-id="39bc4-131">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="39bc4-131">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="39bc4-132">CreateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="39bc4-132">CreateItemResponseMessage</span></span>](createitemresponsemessage.md)
    
- [<span data-ttu-id="39bc4-133">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="39bc4-133">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="39bc4-134">Items</span><span class="sxs-lookup"><span data-stu-id="39bc4-134">Items</span></span>](items.md)
    
<span data-ttu-id="39bc4-135">Um andere Optionen für die Antwortnachricht des CreateItem-Vorgangs zu finden, erkunden Sie die Schemahierarchie.</span><span class="sxs-lookup"><span data-stu-id="39bc4-135">To find other options for the response message of the CreateItem operation, explore the schema hierarchy.</span></span> <span data-ttu-id="39bc4-136">Beginnen Sie mit dem [CreateItemResponse](createitemresponse.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="39bc4-136">Start at the [CreateItemResponse](createitemresponse.md) element.</span></span> 
  
## <a name="error-createitem-response"></a><span data-ttu-id="39bc4-137">Fehler CreateItem-Antwort</span><span class="sxs-lookup"><span data-stu-id="39bc4-137">Error CreateItem Response</span></span>

### <a name="description"></a><span data-ttu-id="39bc4-138">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="39bc4-138">Description</span></span>

<span data-ttu-id="39bc4-139">Das folgende Beispiel zeigt eine Fehlerantwort auf eine CreateItem-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="39bc4-139">The following example shows an error response to a CreateItem request.</span></span>
  
### <a name="code"></a><span data-ttu-id="39bc4-140">Code</span><span class="sxs-lookup"><span data-stu-id="39bc4-140">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <CreateItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="error-response-elements"></a><span data-ttu-id="39bc4-141">Fehlerantwortelemente</span><span class="sxs-lookup"><span data-stu-id="39bc4-141">Error response elements</span></span>

<span data-ttu-id="39bc4-142">Folgende Elemente werden in der Fehlerantwort verwendet:</span><span class="sxs-lookup"><span data-stu-id="39bc4-142">The following elements are used in the error response:</span></span> 
  
- [<span data-ttu-id="39bc4-143">CreateItemResponse</span><span class="sxs-lookup"><span data-stu-id="39bc4-143">CreateItemResponse</span></span>](createitemresponse.md)
    
- [<span data-ttu-id="39bc4-144">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="39bc4-144">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="39bc4-145">CreateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="39bc4-145">CreateItemResponseMessage</span></span>](createitemresponsemessage.md)
    
- [<span data-ttu-id="39bc4-146">MessageText</span><span class="sxs-lookup"><span data-stu-id="39bc4-146">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="39bc4-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="39bc4-147">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="39bc4-148">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="39bc4-148">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="39bc4-149">Items</span><span class="sxs-lookup"><span data-stu-id="39bc4-149">Items</span></span>](items.md)
    
<span data-ttu-id="39bc4-150">Um andere Optionen für die Fehlerantwort Meldung des CreateItem-Vorgangs zu finden, erkunden Sie die Schemahierarchie.</span><span class="sxs-lookup"><span data-stu-id="39bc4-150">To find other options for the error response message of the CreateItem operation, explore the schema hierarchy.</span></span> <span data-ttu-id="39bc4-151">Beginnen Sie mit dem [CreateItemResponse](createitemresponse.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="39bc4-151">Start at the [CreateItemResponse](createitemresponse.md) element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="39bc4-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="39bc4-152">See also</span></span>



[<span data-ttu-id="39bc4-153">CreateItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="39bc4-153">CreateItem operation</span></span>](createitem-operation.md)

