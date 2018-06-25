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
description: Der Vorgang GetAttachment wird verwendet, um vorhandene Anlagen für Elemente im Exchange-Speicher abzurufen.
ms.openlocfilehash: c260033208bf49c60463c09041d8ffcc52a8f5c2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758585"
---
# <a name="getattachment-operation"></a><span data-ttu-id="3529d-103">GetAttachment-Vorgang</span><span class="sxs-lookup"><span data-stu-id="3529d-103">GetAttachment operation</span></span>

<span data-ttu-id="3529d-104">Der Vorgang GetAttachment wird verwendet, um vorhandene Anlagen für Elemente im Exchange-Speicher abzurufen.</span><span class="sxs-lookup"><span data-stu-id="3529d-104">The GetAttachment operation is used to retrieve existing attachments on items in the Exchange store.</span></span>
  
## <a name="getattachment-request-example"></a><span data-ttu-id="3529d-105">GetAttachment anforderungsbeispiel</span><span class="sxs-lookup"><span data-stu-id="3529d-105">GetAttachment request example</span></span>

### <a name="description"></a><span data-ttu-id="3529d-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3529d-106">Description</span></span>

<span data-ttu-id="3529d-107">Im folgenden Beispiel wird der GetAttachment Anforderung veranschaulicht, wie eine Anlage abgerufen.</span><span class="sxs-lookup"><span data-stu-id="3529d-107">The following example of GetAttachment request shows how to get an attachment.</span></span>
  
### <a name="code"></a><span data-ttu-id="3529d-108">Code</span><span class="sxs-lookup"><span data-stu-id="3529d-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
xmlns:xsd="http://www.w3.org/2001/XMLSchema"
xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetAttachment xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <AttachmentShape/>
      <AttachmentIds>
        <t:AttachmentId Id="AAAtAEFkbWluaX..."/>
      </AttachmentIds>
    </GetAttachment>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="3529d-109">Kommentare</span><span class="sxs-lookup"><span data-stu-id="3529d-109">Comments</span></span>

<span data-ttu-id="3529d-110">Das [AttachmentShape](attachmentshape.md) -Element können Sie angeben, welche Informationen über die Anlage zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3529d-110">The [AttachmentShape](attachmentshape.md) element allows you to specify which attachment information should be returned.</span></span> <span data-ttu-id="3529d-111">Ein leeres Element [AttachmentShape](attachmentshape.md) ist gültig und Ihre Anlagen ohne MIME-Inhaltstyp für das elementanlagen, mit dem Text Texttyp und ohne zusätzlichen Eigenschaften rendert.</span><span class="sxs-lookup"><span data-stu-id="3529d-111">An empty [AttachmentShape](attachmentshape.md) element is valid and will render your attachments without MIME content for item attachments, with a text body type, and without any additional properties.</span></span> 
  
<span data-ttu-id="3529d-112">Die [AttachmentIds](attachmentids.md) -Auflistung können Sie eine oder mehrere Anlagen Bezeichner zurückzugebenden angeben.</span><span class="sxs-lookup"><span data-stu-id="3529d-112">The [AttachmentIds](attachmentids.md) collection allows you to specify one or more attachment identifiers to return.</span></span> <span data-ttu-id="3529d-113">Beachten Sie, dass diese vom Typ RequestAttachmentIdType, damit alle AttachmentIds, die Sie aus **CreateAttachment** erhalten die Attribute **RootItemId** und **RootItemChangeKey** verfügen müssen vor der Übergabe an **GetAttachment**entfernt.</span><span class="sxs-lookup"><span data-stu-id="3529d-113">Note that these are of type RequestAttachmentIdType, so any AttachmentIds that you receive from **CreateAttachment** must have the **RootItemId** and **RootItemChangeKey** attributes removed before passing them to **GetAttachment**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="3529d-114">Die Anlage-ID und Key ändern wurden gekürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="3529d-114">The attachment identifier and change key have been shortened to preserve readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="3529d-115">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="3529d-115">Request elements</span></span>

<span data-ttu-id="3529d-116">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="3529d-116">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="3529d-117">GetAttachment</span><span class="sxs-lookup"><span data-stu-id="3529d-117">GetAttachment</span></span>](getattachment.md)
    
- [<span data-ttu-id="3529d-118">AttachmentShape</span><span class="sxs-lookup"><span data-stu-id="3529d-118">AttachmentShape</span></span>](attachmentshape.md)
    
- [<span data-ttu-id="3529d-119">AttachmentIds</span><span class="sxs-lookup"><span data-stu-id="3529d-119">AttachmentIds</span></span>](attachmentids.md)
    
- [<span data-ttu-id="3529d-120">AttachmentId (GetAttachment und DeleteAttachment)</span><span class="sxs-lookup"><span data-stu-id="3529d-120">AttachmentId (GetAttachment and DeleteAttachment)</span></span>](attachmentid-getattachment-and-deleteattachment.md)
    
## <a name="getattachment-response-example"></a><span data-ttu-id="3529d-121">GetAttachment antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="3529d-121">GetAttachment response example</span></span>

### <a name="description"></a><span data-ttu-id="3529d-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3529d-122">Description</span></span>

<span data-ttu-id="3529d-123">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine Anforderung GetAttachment.</span><span class="sxs-lookup"><span data-stu-id="3529d-123">The following example shows a successful response to a GetAttachment request.</span></span> <span data-ttu-id="3529d-124">Dieses Beispiel gibt eine Dateianlage.</span><span class="sxs-lookup"><span data-stu-id="3529d-124">This example returns a file attachment.</span></span>
  
### <a name="code"></a><span data-ttu-id="3529d-125">Code</span><span class="sxs-lookup"><span data-stu-id="3529d-125">Code</span></span>

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
    <GetAttachmentResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                           xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a><span data-ttu-id="3529d-126">Kommentare</span><span class="sxs-lookup"><span data-stu-id="3529d-126">Comments</span></span>

<span data-ttu-id="3529d-127">Die Antwortnachrichten für GetAttachment werden immer die vollständige Anlage enthalten. d. h., werden alle Eigenschaften immer eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="3529d-127">The response messages for GetAttachment will always contain the full attachment; that is, all properties will always be included.</span></span> <span data-ttu-id="3529d-128">Für Dateianlagen sind diese Eigenschaften [Name (AttachmentType)](name-attachmenttype.md), [ContentType](contenttype.md), [ContentId](contentid.md), [ContentLocation](contentlocation.md)und [Content](content.md).</span><span class="sxs-lookup"><span data-stu-id="3529d-128">For file attachments, those properties are [Name (AttachmentType)](name-attachmenttype.md), [ContentType](contenttype.md), [ContentId](contentid.md), [ContentLocation](contentlocation.md), and [Content](content.md).</span></span> <span data-ttu-id="3529d-129">Für Anlagen, diese Eigenschaften sind [Name (AttachmentType)](name-attachmenttype.md), [ContentType](contenttype.md), [ContentId](contentid.md), [ContentLocation](contentlocation.md) und alle Eigenschaften des Elements, als ob die Form **AllProperties** verwendet wurden im Gespräch GetItem.</span><span class="sxs-lookup"><span data-stu-id="3529d-129">For item attachments, those properties are [Name (AttachmentType)](name-attachmenttype.md), [ContentType](contenttype.md), [ContentId](contentid.md), [ContentLocation](contentlocation.md) and all of the item's properties, as if the **AllProperties** shape had been used in a GetItem call.</span></span> <span data-ttu-id="3529d-130">Das [AttachmentShape](attachmentshape.md) -Element, kann falls vorhanden, so fordern Sie zusätzliche erweiterte Eigenschaften für das elementanlagen an eine Consumeranwendung ansetzt.</span><span class="sxs-lookup"><span data-stu-id="3529d-130">The [AttachmentShape](attachmentshape.md) element, if present, will allow a consumer application to request additional extended properties for item attachments.</span></span> 
  
### <a name="successful-response-elements"></a><span data-ttu-id="3529d-131">Elemente einer erfolgreichen Antwort</span><span class="sxs-lookup"><span data-stu-id="3529d-131">Successful response elements</span></span>

<span data-ttu-id="3529d-132">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="3529d-132">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="3529d-133">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="3529d-133">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="3529d-134">GetAttachmentResponse</span><span class="sxs-lookup"><span data-stu-id="3529d-134">GetAttachmentResponse</span></span>](getattachmentresponse.md)
    
- [<span data-ttu-id="3529d-135">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="3529d-135">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="3529d-136">GetAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="3529d-136">GetAttachmentResponseMessage</span></span>](getattachmentresponsemessage.md)
    
- [<span data-ttu-id="3529d-137">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="3529d-137">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="3529d-138">Anlagen</span><span class="sxs-lookup"><span data-stu-id="3529d-138">Attachments</span></span>](attachments-ex15websvcsotherref.md)
    
- [<span data-ttu-id="3529d-139">FileAttachment</span><span class="sxs-lookup"><span data-stu-id="3529d-139">FileAttachment</span></span>](fileattachment.md)
    
- [<span data-ttu-id="3529d-140">AttachmentId (GetAttachment und DeleteAttachment)</span><span class="sxs-lookup"><span data-stu-id="3529d-140">AttachmentId (GetAttachment and DeleteAttachment)</span></span>](attachmentid-getattachment-and-deleteattachment.md)
    
- [<span data-ttu-id="3529d-141">Name ("AttachmentType")</span><span class="sxs-lookup"><span data-stu-id="3529d-141">Name (AttachmentType)</span></span>](name-attachmenttype.md)
    
- [<span data-ttu-id="3529d-142">Inhalt</span><span class="sxs-lookup"><span data-stu-id="3529d-142">Content</span></span>](content.md)
    
## <a name="see-also"></a><span data-ttu-id="3529d-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3529d-143">See also</span></span>



[<span data-ttu-id="3529d-144">CreateAttachment-Vorgang</span><span class="sxs-lookup"><span data-stu-id="3529d-144">CreateAttachment operation</span></span>](createattachment-operation.md)
  
[<span data-ttu-id="3529d-145">DeleteAttachment-Vorgang</span><span class="sxs-lookup"><span data-stu-id="3529d-145">DeleteAttachment operation</span></span>](deleteattachment-operation.md)

