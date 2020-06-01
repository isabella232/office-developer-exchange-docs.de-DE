---
title: GetAttachment-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetAttachment
api_type:
- schema
ms.assetid: 24d10a15-b942-415e-9024-a6375708f326
description: Der GetAttachment-Vorgang wird verwendet, um vorhandene Anlagen für Elemente im Exchange-Informationsspeicher abzurufen.
ms.openlocfilehash: ac7eafd61c62b077a8d20e5fd8d004924bf06cf1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461289"
---
# <a name="getattachment-operation"></a><span data-ttu-id="61f63-103">GetAttachment-Vorgang</span><span class="sxs-lookup"><span data-stu-id="61f63-103">GetAttachment operation</span></span>

<span data-ttu-id="61f63-104">Der GetAttachment-Vorgang wird verwendet, um vorhandene Anlagen für Elemente im Exchange-Informationsspeicher abzurufen.</span><span class="sxs-lookup"><span data-stu-id="61f63-104">The GetAttachment operation is used to retrieve existing attachments on items in the Exchange store.</span></span>
  
## <a name="getattachment-request-example"></a><span data-ttu-id="61f63-105">GetAttachment-Anforderungs Beispiel</span><span class="sxs-lookup"><span data-stu-id="61f63-105">GetAttachment request example</span></span>

### <a name="description"></a><span data-ttu-id="61f63-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="61f63-106">Description</span></span>

<span data-ttu-id="61f63-107">Das folgende Beispiel der GetAttachment-Anforderung zeigt, wie eine Anlage abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="61f63-107">The following example of GetAttachment request shows how to get an attachment.</span></span>
  
### <a name="code"></a><span data-ttu-id="61f63-108">Code</span><span class="sxs-lookup"><span data-stu-id="61f63-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
xmlns:xsd="http://www.w3.org/2001/XMLSchema"
xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetAttachment xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <AttachmentShape/>
      <AttachmentIds>
        <t:AttachmentId Id="AAAtAEFkbWluaX..."/>
      </AttachmentIds>
    </GetAttachment>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="61f63-109">Comments</span><span class="sxs-lookup"><span data-stu-id="61f63-109">Comments</span></span>

<span data-ttu-id="61f63-110">Mit dem [AttachmentShape](attachmentshape.md) -Element können Sie angeben, welche Anlageninformationen zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="61f63-110">The [AttachmentShape](attachmentshape.md) element allows you to specify which attachment information should be returned.</span></span> <span data-ttu-id="61f63-111">Ein leeres [AttachmentShape](attachmentshape.md) -Element ist gültig und rendert Ihre Anlagen ohne MIME-Inhalt für Element Anlagen, mit Textkörpertyp und ohne zusätzliche Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="61f63-111">An empty [AttachmentShape](attachmentshape.md) element is valid and will render your attachments without MIME content for item attachments, with a text body type, and without any additional properties.</span></span> 
  
<span data-ttu-id="61f63-112">Die [AttachmentIds](attachmentids.md) -Auflistung ermöglicht es Ihnen, einen oder mehrere Anlagen Bezeichner anzugeben, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="61f63-112">The [AttachmentIds](attachmentids.md) collection allows you to specify one or more attachment identifiers to return.</span></span> <span data-ttu-id="61f63-113">Beachten Sie, dass diese vom Typ RequestAttachmentIdType sind, sodass bei allen AttachmentIds, die Sie von **CreateAttachment** erhalten, die Attribute **RootItemId** und **RootItemChangeKey** entfernt werden müssen, bevor Sie an **GetAttachment**übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="61f63-113">Note that these are of type RequestAttachmentIdType, so any AttachmentIds that you receive from **CreateAttachment** must have the **RootItemId** and **RootItemChangeKey** attributes removed before passing them to **GetAttachment**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="61f63-114">Die Anlagen-ID und der Änderungsschlüssel wurden verkürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="61f63-114">The attachment identifier and change key have been shortened to preserve readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="61f63-115">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="61f63-115">Request elements</span></span>

<span data-ttu-id="61f63-116">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="61f63-116">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="61f63-117">GetAttachment</span><span class="sxs-lookup"><span data-stu-id="61f63-117">GetAttachment</span></span>](getattachment.md)
    
- [<span data-ttu-id="61f63-118">AttachmentShape</span><span class="sxs-lookup"><span data-stu-id="61f63-118">AttachmentShape</span></span>](attachmentshape.md)
    
- [<span data-ttu-id="61f63-119">AttachmentIds</span><span class="sxs-lookup"><span data-stu-id="61f63-119">AttachmentIds</span></span>](attachmentids.md)
    
- [<span data-ttu-id="61f63-120">Attachment-Nr (GetAttachment und DeleteAttachment-)</span><span class="sxs-lookup"><span data-stu-id="61f63-120">AttachmentId (GetAttachment and DeleteAttachment)</span></span>](attachmentid-getattachment-and-deleteattachment.md)
    
## <a name="getattachment-response-example"></a><span data-ttu-id="61f63-121">GetAttachment-Antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="61f63-121">GetAttachment response example</span></span>

### <a name="description"></a><span data-ttu-id="61f63-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="61f63-122">Description</span></span>

<span data-ttu-id="61f63-123">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine GetAttachment-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="61f63-123">The following example shows a successful response to a GetAttachment request.</span></span> <span data-ttu-id="61f63-124">In diesem Beispiel wird eine Dateianlage zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="61f63-124">This example returns a file attachment.</span></span>
  
### <a name="code"></a><span data-ttu-id="61f63-125">Code</span><span class="sxs-lookup"><span data-stu-id="61f63-125">Code</span></span>

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
    <GetAttachmentResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                           xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:GetAttachmentResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Attachments>
            <t:FileAttachment>
              <t:AttachmentId Id="AAAtAEFkbWluaX..."/>
              <t:Name>SomeFile</t:Name>
              <t:Content>AQIDBAU=</t:Content>
            </t:FileAttachment>
          </m:Attachments>
        </m:GetAttachmentResponseMessage>
      </m:ResponseMessages>
    </GetAttachmentResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="61f63-126">Comments</span><span class="sxs-lookup"><span data-stu-id="61f63-126">Comments</span></span>

<span data-ttu-id="61f63-127">Die Antwortnachrichten für GetAttachment enthalten immer die vollständige Anlage; Dies bedeutet, dass alle Eigenschaften immer eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="61f63-127">The response messages for GetAttachment will always contain the full attachment; that is, all properties will always be included.</span></span> <span data-ttu-id="61f63-128">Für Dateianlagen sind diese Eigenschaften [Name (AttachmentType)](name-attachmenttype.md), [ContentType](contenttype.md), [Inhalts](contentid.md)- [ContentLocation](contentlocation.md)und [Inhalt](content.md).</span><span class="sxs-lookup"><span data-stu-id="61f63-128">For file attachments, those properties are [Name (AttachmentType)](name-attachmenttype.md), [ContentType](contenttype.md), [ContentId](contentid.md), [ContentLocation](contentlocation.md), and [Content](content.md).</span></span> <span data-ttu-id="61f63-129">Für Element Anlagen sind diese Eigenschaften [Name (AttachmentType)](name-attachmenttype.md), [ContentType](contenttype.md), [Inhalts](contentid.md)- [ContentLocation](contentlocation.md) und alle Eigenschaften des Elements, als ob die **allproperties** -Form in einem GetItem-Aufruf verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="61f63-129">For item attachments, those properties are [Name (AttachmentType)](name-attachmenttype.md), [ContentType](contenttype.md), [ContentId](contentid.md), [ContentLocation](contentlocation.md) and all of the item's properties, as if the **AllProperties** shape had been used in a GetItem call.</span></span> <span data-ttu-id="61f63-130">Das [AttachmentShape](attachmentshape.md) -Element, falls vorhanden, ermöglicht einer Consumer-Anwendung, zusätzliche erweiterte Eigenschaften für Element Anlagen anzufordern.</span><span class="sxs-lookup"><span data-stu-id="61f63-130">The [AttachmentShape](attachmentshape.md) element, if present, will allow a consumer application to request additional extended properties for item attachments.</span></span> 
  
### <a name="successful-response-elements"></a><span data-ttu-id="61f63-131">Erfolgreiche Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="61f63-131">Successful response elements</span></span>

<span data-ttu-id="61f63-132">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="61f63-132">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="61f63-133">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="61f63-133">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="61f63-134">GetAttachmentResponse</span><span class="sxs-lookup"><span data-stu-id="61f63-134">GetAttachmentResponse</span></span>](getattachmentresponse.md)
    
- [<span data-ttu-id="61f63-135">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="61f63-135">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="61f63-136">GetAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="61f63-136">GetAttachmentResponseMessage</span></span>](getattachmentresponsemessage.md)
    
- [<span data-ttu-id="61f63-137">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="61f63-137">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="61f63-138">Anlagen</span><span class="sxs-lookup"><span data-stu-id="61f63-138">Attachments</span></span>](attachments-ex15websvcsotherref.md)
    
- [<span data-ttu-id="61f63-139">FileAttachment</span><span class="sxs-lookup"><span data-stu-id="61f63-139">FileAttachment</span></span>](fileattachment.md)
    
- [<span data-ttu-id="61f63-140">Attachment-Nr (GetAttachment und DeleteAttachment-)</span><span class="sxs-lookup"><span data-stu-id="61f63-140">AttachmentId (GetAttachment and DeleteAttachment)</span></span>](attachmentid-getattachment-and-deleteattachment.md)
    
- [<span data-ttu-id="61f63-141">Name (AttachmentType)</span><span class="sxs-lookup"><span data-stu-id="61f63-141">Name (AttachmentType)</span></span>](name-attachmenttype.md)
    
- [<span data-ttu-id="61f63-142">Content</span><span class="sxs-lookup"><span data-stu-id="61f63-142">Content</span></span>](content.md)
    
## <a name="see-also"></a><span data-ttu-id="61f63-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="61f63-143">See also</span></span>



[<span data-ttu-id="61f63-144">CreateAttachment-Vorgang</span><span class="sxs-lookup"><span data-stu-id="61f63-144">CreateAttachment operation</span></span>](createattachment-operation.md)
  
[<span data-ttu-id="61f63-145">DeleteAttachment-Vorgang</span><span class="sxs-lookup"><span data-stu-id="61f63-145">DeleteAttachment operation</span></span>](deleteattachment-operation.md)

