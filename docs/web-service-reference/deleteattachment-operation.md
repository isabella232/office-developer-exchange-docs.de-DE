---
title: DeleteAttachment-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteAttachment
api_type:
- schema
ms.assetid: 4d48e595-b98c-48e7-bbeb-cacf91d12a78
description: Der DeleteAttachment--Vorgang wird verwendet, um Datei-und Element Anlagen aus einem vorhandenen Element im Exchange-Informationsspeicher zu löschen.
ms.openlocfilehash: 1d34ce4c5ba1d955989a35dafb8ab3c5d229d505
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457333"
---
# <a name="deleteattachment-operation"></a><span data-ttu-id="ec103-103">DeleteAttachment-Vorgang</span><span class="sxs-lookup"><span data-stu-id="ec103-103">DeleteAttachment operation</span></span>

<span data-ttu-id="ec103-104">Der DeleteAttachment--Vorgang wird verwendet, um Datei-und Element Anlagen aus einem vorhandenen Element im Exchange-Informationsspeicher zu löschen.</span><span class="sxs-lookup"><span data-stu-id="ec103-104">The DeleteAttachment operation is used to delete file and item attachments from an existing item in the Exchange store.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ec103-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ec103-105">Remarks</span></span>

<span data-ttu-id="ec103-106">Mit diesem Vorgang können Sie eine oder mehrere Anlagen nach ID löschen.</span><span class="sxs-lookup"><span data-stu-id="ec103-106">This operation allows you to delete one or more attachments by ID.</span></span>
  
## <a name="deleteattachment-request-example"></a><span data-ttu-id="ec103-107">DeleteAttachment--Anforderungs Beispiel</span><span class="sxs-lookup"><span data-stu-id="ec103-107">DeleteAttachment request example</span></span>

### <a name="description"></a><span data-ttu-id="ec103-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ec103-108">Description</span></span>

<span data-ttu-id="ec103-109">Im folgenden Beispiel einer DeleteAttachment--Anforderung wird gezeigt, wie eine Elementanlage gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="ec103-109">The following example of a DeleteAttachment request shows how to delete an item attachment.</span></span>
  
### <a name="code"></a><span data-ttu-id="ec103-110">Code</span><span class="sxs-lookup"><span data-stu-id="ec103-110">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <DeleteAttachment xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <AttachmentIds>
        <t:AttachmentId Id="AAAtAEFkbWluaX"/>
      </AttachmentIds>
    </DeleteAttachment>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="ec103-111">Comments</span><span class="sxs-lookup"><span data-stu-id="ec103-111">Comments</span></span>

<span data-ttu-id="ec103-112">Die Anlagen-ID wurde verkürzt, um die Lesbarkeit beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="ec103-112">The attachment identifier has been shortened to preserve readability.</span></span>
  
### <a name="request-elements"></a><span data-ttu-id="ec103-113">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="ec103-113">Request elements</span></span>

<span data-ttu-id="ec103-114">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="ec103-114">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="ec103-115">DeleteAttachment-</span><span class="sxs-lookup"><span data-stu-id="ec103-115">DeleteAttachment</span></span>](deleteattachment.md)
    
- [<span data-ttu-id="ec103-116">AttachmentIds</span><span class="sxs-lookup"><span data-stu-id="ec103-116">AttachmentIds</span></span>](attachmentids.md)
    
- [<span data-ttu-id="ec103-117">AttachmentId</span><span class="sxs-lookup"><span data-stu-id="ec103-117">AttachmentId</span></span>](attachmentid.md)
    
## <a name="deleteattachment-response-example"></a><span data-ttu-id="ec103-118">DeleteAttachment--Antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="ec103-118">DeleteAttachment response example</span></span>

### <a name="description"></a><span data-ttu-id="ec103-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ec103-119">Description</span></span>

<span data-ttu-id="ec103-120">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine DeleteAttachment--Anforderung.</span><span class="sxs-lookup"><span data-stu-id="ec103-120">The following example shows a successful response to a DeleteAttachment request.</span></span>
  
### <a name="code"></a><span data-ttu-id="ec103-121">Code</span><span class="sxs-lookup"><span data-stu-id="ec103-121">Code</span></span>

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
    <DeleteAttachmentResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                              xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                              xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:DeleteAttachmentResponseMessage xsi:type="m:DeleteAttachmentResponseMessageType" ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootItemId RootItemId="AAAtAEFkbWluaXN..." RootItemChangeKey="CQAAABYAA..."/>
        </m:DeleteAttachmentResponseMessage>
      </m:ResponseMessages>
    </DeleteAttachmentResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="ec103-122">Comments</span><span class="sxs-lookup"><span data-stu-id="ec103-122">Comments</span></span>

<span data-ttu-id="ec103-123">Der CreateAttachment-Vorgang gibt ein Element vom Typ AttachmentIdType zurück, das eine **RootItemId** -und **RootItemChangeKey**-Komponente enthält.</span><span class="sxs-lookup"><span data-stu-id="ec103-123">The CreateAttachment operation returns an element of AttachmentIdType type that includes a **RootItemId** and **RootItemChangeKey**.</span></span> <span data-ttu-id="ec103-124">Diese Attribute sind für Bezeichner in einer DeleteAttachment--Anforderung nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="ec103-124">These attributes are not permitted for identifiers within a DeleteAttachment request.</span></span> <span data-ttu-id="ec103-125">DeleteAttachment-verwendet Elemente vom Typ RequestAttachmentIdType, die diese Attribute nicht enthalten.</span><span class="sxs-lookup"><span data-stu-id="ec103-125">DeleteAttachment uses elements of type RequestAttachmentIdType, which does not include these attributes.</span></span>
  
<span data-ttu-id="ec103-126">Die DeleteAttachment--Antwort enthält die ID des übergeordneten Elements.</span><span class="sxs-lookup"><span data-stu-id="ec103-126">The DeleteAttachment response includes the ID of the parent item.</span></span> <span data-ttu-id="ec103-127">Wenn Anlagen aus einem Element entfernt werden, wird der Änderungsschlüssel des Elements geändert.</span><span class="sxs-lookup"><span data-stu-id="ec103-127">When attachments are removed from an item, the item's change key is modified.</span></span> <span data-ttu-id="ec103-128">Der neue Element Änderungsschlüssel kann aus der DeleteAttachment--Antwort abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="ec103-128">The new item change key can be obtained from the DeleteAttachment response.</span></span>
  
> [!NOTE]
> <span data-ttu-id="ec103-129">Die [RootItemId](rootitemid.md) -ID und ChangeKey wurden verkürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ec103-129">The [RootItemId](rootitemid.md) identifier and ChangeKey have been shortened to preserve readability.</span></span> 
  
### <a name="successful-response-elements"></a><span data-ttu-id="ec103-130">Erfolgreiche Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="ec103-130">Successful response elements</span></span>

<span data-ttu-id="ec103-131">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="ec103-131">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="ec103-132">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="ec103-132">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="ec103-133">DeleteAttachmentResponse</span><span class="sxs-lookup"><span data-stu-id="ec103-133">DeleteAttachmentResponse</span></span>](deleteattachmentresponse.md)
    
- [<span data-ttu-id="ec103-134">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="ec103-134">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="ec103-135">DeleteAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="ec103-135">DeleteAttachmentResponseMessage</span></span>](deleteattachmentresponsemessage.md)
    
- [<span data-ttu-id="ec103-136">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="ec103-136">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="ec103-137">RootItemId</span><span class="sxs-lookup"><span data-stu-id="ec103-137">RootItemId</span></span>](rootitemid.md)
    
## <a name="see-also"></a><span data-ttu-id="ec103-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ec103-138">See also</span></span>

- [<span data-ttu-id="ec103-139">CreateAttachment-Vorgang</span><span class="sxs-lookup"><span data-stu-id="ec103-139">CreateAttachment operation</span></span>](createattachment-operation.md) 
- [<span data-ttu-id="ec103-140">GetAttachment-Vorgang</span><span class="sxs-lookup"><span data-stu-id="ec103-140">GetAttachment operation</span></span>](getattachment-operation.md)

