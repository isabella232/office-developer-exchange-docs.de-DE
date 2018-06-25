---
title: CreateAttachment-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateAttachment
api_type:
- schema
ms.assetid: e066db95-6963-4507-a8d0-8efad287f550
description: Der Vorgang CreateAttachment Anlage eines Elements oder einer Datei erstellt und fügt diese an das angegebene Element.
ms.openlocfilehash: fed60275a007f2796c60d936def7a937e4982f29
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757739"
---
# <a name="createattachment-operation"></a><span data-ttu-id="3b3f2-103">CreateAttachment-Vorgang</span><span class="sxs-lookup"><span data-stu-id="3b3f2-103">CreateAttachment operation</span></span>

<span data-ttu-id="3b3f2-104">Der Vorgang CreateAttachment Anlage eines Elements oder einer Datei erstellt und fügt diese an das angegebene Element.</span><span class="sxs-lookup"><span data-stu-id="3b3f2-104">The CreateAttachment operation creates either an item or file attachment and attaches it to the specified item.</span></span>
  
## <a name="file-createattachment-request-example"></a><span data-ttu-id="3b3f2-105">Beispiel für die Datei CreateAttachment Anforderung</span><span class="sxs-lookup"><span data-stu-id="3b3f2-105">File CreateAttachment request example</span></span>

### <a name="description"></a><span data-ttu-id="3b3f2-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3b3f2-106">Description</span></span>

<span data-ttu-id="3b3f2-107">Im folgenden Beispiel wird eine Anforderung CreateAttachment veranschaulicht, wie eine Dateianlage zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3b3f2-107">The following example of a CreateAttachment request shows how to create a file attachment.</span></span>
  
### <a name="code"></a><span data-ttu-id="3b3f2-108">Code</span><span class="sxs-lookup"><span data-stu-id="3b3f2-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
<soap:Body>
  <CreateAttachment xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
                    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
    <ParentItemId Id="AAAtAE..." ChangeKey="CQAAABYA..."/>
    <Attachments>
      <t:FileAttachment>
        <t:Name>SomeFile</t:Name>
        <t:Content>AQIDBAU=</t:Content>
      </t:FileAttachment>
    </Attachments>
  </CreateAttachment>
</soap:Body>
</soap:Envelope>
```

### <a name="comment"></a><span data-ttu-id="3b3f2-109">Comment</span><span class="sxs-lookup"><span data-stu-id="3b3f2-109">Comment</span></span>

<span data-ttu-id="3b3f2-110">Ein Namen für die Anlage muss angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3b3f2-110">A name for the attachment must be provided.</span></span>
  
> [!NOTE]
> <span data-ttu-id="3b3f2-111">Das übergeordnete Element-ID und Key ändern wurden gekürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="3b3f2-111">The parent item identifier and change key have been shortened to preserve readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="3b3f2-112">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="3b3f2-112">Request elements</span></span>

<span data-ttu-id="3b3f2-113">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="3b3f2-113">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="3b3f2-114">CreateAttachment</span><span class="sxs-lookup"><span data-stu-id="3b3f2-114">CreateAttachment</span></span>](createattachment.md)
    
- [<span data-ttu-id="3b3f2-115">ParentItemId</span><span class="sxs-lookup"><span data-stu-id="3b3f2-115">ParentItemId</span></span>](parentitemid.md)
    
- [<span data-ttu-id="3b3f2-116">Anlagen</span><span class="sxs-lookup"><span data-stu-id="3b3f2-116">Attachments</span></span>](attachments-ex15websvcsotherref.md)
    
- [<span data-ttu-id="3b3f2-117">FileAttachment</span><span class="sxs-lookup"><span data-stu-id="3b3f2-117">FileAttachment</span></span>](fileattachment.md)
    
- [<span data-ttu-id="3b3f2-118">Name ("AttachmentType")</span><span class="sxs-lookup"><span data-stu-id="3b3f2-118">Name (AttachmentType)</span></span>](name-attachmenttype.md)
    
- [<span data-ttu-id="3b3f2-119">Inhalt</span><span class="sxs-lookup"><span data-stu-id="3b3f2-119">Content</span></span>](content.md)
    
## <a name="successful-file-createattachment-response-example"></a><span data-ttu-id="3b3f2-120">Erfolgreiche Datei CreateAttachment antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="3b3f2-120">Successful File CreateAttachment response example</span></span>

### <a name="description"></a><span data-ttu-id="3b3f2-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3b3f2-121">Description</span></span>

<span data-ttu-id="3b3f2-122">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die Anforderung CreateAttachment.</span><span class="sxs-lookup"><span data-stu-id="3b3f2-122">The following example shows a successful response to the CreateAttachment request.</span></span>
  
### <a name="code"></a><span data-ttu-id="3b3f2-123">Code</span><span class="sxs-lookup"><span data-stu-id="3b3f2-123">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="653" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <CreateAttachmentResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                              xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                              xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateAttachmentResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Attachments>
            <t:FileAttachment>
              <t:AttachmentId Id="AAAtAE=" RootItemId="AAAtAEFk=" RootItemChangeKey="CQAAAB"/>
            </t:FileAttachment>
          </m:Attachments>
        </m:CreateAttachmentResponseMessage>
      </m:ResponseMessages>
    </CreateAttachmentResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comment"></a><span data-ttu-id="3b3f2-124">Comment</span><span class="sxs-lookup"><span data-stu-id="3b3f2-124">Comment</span></span>

<span data-ttu-id="3b3f2-125">Die Antwort enthält den Bezeichner der angehängten Datei.</span><span class="sxs-lookup"><span data-stu-id="3b3f2-125">The response contains the identifier of the attached file.</span></span> <span data-ttu-id="3b3f2-126">Sie enthält außerdem den Schlüssel-ID und ein Änderungsprotokoll das Stammelement.</span><span class="sxs-lookup"><span data-stu-id="3b3f2-126">It also contains the identifier and change key of the root item.</span></span> <span data-ttu-id="3b3f2-127">Die Element-IDs und Key ändern wurden gekürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="3b3f2-127">The item identifiers and change key have been shortened to preserve readability.</span></span>
  
### <a name="successful-response-elements"></a><span data-ttu-id="3b3f2-128">Elemente einer erfolgreichen Antwort</span><span class="sxs-lookup"><span data-stu-id="3b3f2-128">Successful response elements</span></span>

<span data-ttu-id="3b3f2-129">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="3b3f2-129">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="3b3f2-130">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="3b3f2-130">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="3b3f2-131">CreateAttachmentResponse</span><span class="sxs-lookup"><span data-stu-id="3b3f2-131">CreateAttachmentResponse</span></span>](createattachmentresponse.md)
    
- [<span data-ttu-id="3b3f2-132">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="3b3f2-132">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="3b3f2-133">CreateAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="3b3f2-133">CreateAttachmentResponseMessage</span></span>](createattachmentresponsemessage.md)
    
- [<span data-ttu-id="3b3f2-134">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="3b3f2-134">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="3b3f2-135">Anlagen</span><span class="sxs-lookup"><span data-stu-id="3b3f2-135">Attachments</span></span>](attachments-ex15websvcsotherref.md)
    
- [<span data-ttu-id="3b3f2-136">FileAttachment</span><span class="sxs-lookup"><span data-stu-id="3b3f2-136">FileAttachment</span></span>](fileattachment.md)
    
- [<span data-ttu-id="3b3f2-137">AttachmentId</span><span class="sxs-lookup"><span data-stu-id="3b3f2-137">AttachmentId</span></span>](attachmentid.md)
    
## <a name="item-createattachment-request-example"></a><span data-ttu-id="3b3f2-138">Element CreateAttachment anforderungsbeispiel</span><span class="sxs-lookup"><span data-stu-id="3b3f2-138">Item CreateAttachment request example</span></span>

### <a name="description"></a><span data-ttu-id="3b3f2-139">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3b3f2-139">Description</span></span>

<span data-ttu-id="3b3f2-140">Im folgenden Beispiel wird eine Anforderung CreateAttachment veranschaulicht, wie eine Elementanlage erstellen.</span><span class="sxs-lookup"><span data-stu-id="3b3f2-140">The following example of a CreateAttachment request shows how to create an item attachment.</span></span>
  
### <a name="code"></a><span data-ttu-id="3b3f2-141">Code</span><span class="sxs-lookup"><span data-stu-id="3b3f2-141">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateAttachment xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <ParentItemId Id="AAAtAE=" ChangeKey="CQAAABYA"/>
      <Attachments>
        <t:ItemAttachment>
          <t:Name>An item attachment</t:Name>
          <t:Message>
            <t:Subject>A message to attach</t:Subject>
          </t:Message>
        </t:ItemAttachment>
      </Attachments>
    </CreateAttachment>
  </soap:Body>
</soap:Envelope>
```

### <a name="comment"></a><span data-ttu-id="3b3f2-142">Comment</span><span class="sxs-lookup"><span data-stu-id="3b3f2-142">Comment</span></span>

<span data-ttu-id="3b3f2-143">Ein Namen für die Anlage muss angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3b3f2-143">A name for the attachment must be provided.</span></span>
  
 <span data-ttu-id="3b3f2-144">**Hinweis** Das übergeordnete Element-ID und Key ändern wurden gekürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="3b3f2-144">**Note** The parent item identifier and change key have been shortened to preserve readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="3b3f2-145">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="3b3f2-145">Request elements</span></span>

<span data-ttu-id="3b3f2-146">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="3b3f2-146">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="3b3f2-147">CreateAttachment</span><span class="sxs-lookup"><span data-stu-id="3b3f2-147">CreateAttachment</span></span>](createattachment.md)
    
- [<span data-ttu-id="3b3f2-148">ParentItemId</span><span class="sxs-lookup"><span data-stu-id="3b3f2-148">ParentItemId</span></span>](parentitemid.md)
    
- [<span data-ttu-id="3b3f2-149">Anlagen</span><span class="sxs-lookup"><span data-stu-id="3b3f2-149">Attachments</span></span>](attachments-ex15websvcsotherref.md)
    
- [<span data-ttu-id="3b3f2-150">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="3b3f2-150">ItemAttachment</span></span>](itemattachment.md)
    
- [<span data-ttu-id="3b3f2-151">Name ("AttachmentType")</span><span class="sxs-lookup"><span data-stu-id="3b3f2-151">Name (AttachmentType)</span></span>](name-attachmenttype.md)
    
- [<span data-ttu-id="3b3f2-152">Message</span><span class="sxs-lookup"><span data-stu-id="3b3f2-152">Message</span></span>](message-ex15websvcsotherref.md)
    
- [<span data-ttu-id="3b3f2-153">Betreff</span><span class="sxs-lookup"><span data-stu-id="3b3f2-153">Subject</span></span>](subject.md)
    
## <a name="successful-item-createattachment-response-example"></a><span data-ttu-id="3b3f2-154">Erfolgreiche Item CreateAttachment antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="3b3f2-154">Successful Item CreateAttachment response example</span></span>

### <a name="description"></a><span data-ttu-id="3b3f2-155">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3b3f2-155">Description</span></span>

<span data-ttu-id="3b3f2-156">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die Anforderung CreateAttachment.</span><span class="sxs-lookup"><span data-stu-id="3b3f2-156">The following example shows a successful response to the CreateAttachment request.</span></span>
  
### <a name="code"></a><span data-ttu-id="3b3f2-157">Code</span><span class="sxs-lookup"><span data-stu-id="3b3f2-157">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="653" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <CreateAttachmentResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                              xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                              xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateAttachmentResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Attachments>
            <t:ItemAttachment>
              <t:AttachmentId Id="AAAtAEFk=" RootItemId="AAAtAEFkb=" RootItemChangeKey="CQAAABYA"/>
            </t:ItemAttachment>
          </m:Attachments>
        </m:CreateAttachmentResponseMessage>
      </m:ResponseMessages>
    </CreateAttachmentResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comment"></a><span data-ttu-id="3b3f2-158">Comment</span><span class="sxs-lookup"><span data-stu-id="3b3f2-158">Comment</span></span>

<span data-ttu-id="3b3f2-159">Die Antwort enthält den Bezeichner des neuen Anhang.</span><span class="sxs-lookup"><span data-stu-id="3b3f2-159">The response contains the identifier of the new attachment.</span></span> <span data-ttu-id="3b3f2-160">Sie enthält außerdem den Schlüssel-ID und ein Änderungsprotokoll das Stammelement.</span><span class="sxs-lookup"><span data-stu-id="3b3f2-160">It also contains the identifier and change key of the root item.</span></span> <span data-ttu-id="3b3f2-161">Das Stammelement ist das Element, das die Anlage enthält.</span><span class="sxs-lookup"><span data-stu-id="3b3f2-161">The root item is the item that contains the attachment.</span></span> <span data-ttu-id="3b3f2-162">Die Element-IDs und Key ändern wurden gekürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="3b3f2-162">The item identifiers and change key have been shortened to preserve readability.</span></span>
  
### <a name="successful-response-elements"></a><span data-ttu-id="3b3f2-163">Elemente einer erfolgreichen Antwort</span><span class="sxs-lookup"><span data-stu-id="3b3f2-163">Successful response elements</span></span>

<span data-ttu-id="3b3f2-164">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="3b3f2-164">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="3b3f2-165">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="3b3f2-165">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="3b3f2-166">CreateAttachmentResponse</span><span class="sxs-lookup"><span data-stu-id="3b3f2-166">CreateAttachmentResponse</span></span>](createattachmentresponse.md)
    
- [<span data-ttu-id="3b3f2-167">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="3b3f2-167">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="3b3f2-168">CreateAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="3b3f2-168">CreateAttachmentResponseMessage</span></span>](createattachmentresponsemessage.md)
    
- [<span data-ttu-id="3b3f2-169">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="3b3f2-169">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="3b3f2-170">Anlagen</span><span class="sxs-lookup"><span data-stu-id="3b3f2-170">Attachments</span></span>](attachments-ex15websvcsotherref.md)
    
- [<span data-ttu-id="3b3f2-171">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="3b3f2-171">ItemAttachment</span></span>](itemattachment.md)
    
- [<span data-ttu-id="3b3f2-172">AttachmentId</span><span class="sxs-lookup"><span data-stu-id="3b3f2-172">AttachmentId</span></span>](attachmentid.md)
    
## <a name="createattachment-error-response-example"></a><span data-ttu-id="3b3f2-173">Antwortbeispiel CreateAttachment-Fehler</span><span class="sxs-lookup"><span data-stu-id="3b3f2-173">CreateAttachment Error response example</span></span>

### <a name="description"></a><span data-ttu-id="3b3f2-174">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3b3f2-174">Description</span></span>

<span data-ttu-id="3b3f2-175">Das folgende Beispiel zeigt eine Fehlerantwort an die CreateAttachment-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="3b3f2-175">The following example shows an error response to the CreateAttachment request.</span></span> <span data-ttu-id="3b3f2-176">Der Fehler ist darauf zurückzuführen, dass der Name der Anlage nicht angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="3b3f2-176">The error is due to the fact that the name of the attachment was not specified.</span></span>
  
### <a name="code"></a><span data-ttu-id="3b3f2-177">Code</span><span class="sxs-lookup"><span data-stu-id="3b3f2-177">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="653" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <CreateAttachmentResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                              xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                              xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateAttachmentResponseMessage ResponseClass="Error">
          <m:MessageText>Required property is missing.</m:MessageText>
          <m:ResponseCode>ErrorRequiredPropertyMissing</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:MessageXml>
            <t:ExceptionFieldURI FieldURI="attachment:Name"/>
          </m:MessageXml>
          <m:Attachments/>
        </m:CreateAttachmentResponseMessage>
      </m:ResponseMessages>
    </CreateAttachmentResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a><span data-ttu-id="3b3f2-178">Fehler Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="3b3f2-178">Error response elements</span></span>

<span data-ttu-id="3b3f2-179">Folgende Elemente werden in der Fehlerantwort verwendet:</span><span class="sxs-lookup"><span data-stu-id="3b3f2-179">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="3b3f2-180">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="3b3f2-180">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="3b3f2-181">CreateAttachmentResponse</span><span class="sxs-lookup"><span data-stu-id="3b3f2-181">CreateAttachmentResponse</span></span>](createattachmentresponse.md)
    
- [<span data-ttu-id="3b3f2-182">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="3b3f2-182">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="3b3f2-183">CreateAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="3b3f2-183">CreateAttachmentResponseMessage</span></span>](createattachmentresponsemessage.md)
    
- [<span data-ttu-id="3b3f2-184">MessageText</span><span class="sxs-lookup"><span data-stu-id="3b3f2-184">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="3b3f2-185">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="3b3f2-185">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="3b3f2-186">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="3b3f2-186">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="3b3f2-187">MessageXml</span><span class="sxs-lookup"><span data-stu-id="3b3f2-187">MessageXml</span></span>](messagexml.md)
    
- [<span data-ttu-id="3b3f2-188">ExceptionFieldURI</span><span class="sxs-lookup"><span data-stu-id="3b3f2-188">ExceptionFieldURI</span></span>](exceptionfielduri.md)
    
- [<span data-ttu-id="3b3f2-189">Anlagen</span><span class="sxs-lookup"><span data-stu-id="3b3f2-189">Attachments</span></span>](attachments-ex15websvcsotherref.md)
    
## <a name="remarks"></a><span data-ttu-id="3b3f2-190">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3b3f2-190">Remarks</span></span>

<span data-ttu-id="3b3f2-191">Wenn mehrere Anlagen auf ein Element in einem einzigen Roundtrip angefügt sind, ist die RootItemChangeKey in der letzten Antwortnachricht diejenige, die den neuen Änderungsschlüssel des Elements darstellt, die Anlagen wurde.</span><span class="sxs-lookup"><span data-stu-id="3b3f2-191">If multiple attachments are attached to an item in a single round trip, the RootItemChangeKey in the last response message is the one that represents the new change key of the item that has the attachments.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3b3f2-192">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3b3f2-192">See also</span></span>



[<span data-ttu-id="3b3f2-193">DeleteAttachment-Vorgang</span><span class="sxs-lookup"><span data-stu-id="3b3f2-193">DeleteAttachment operation</span></span>](deleteattachment-operation.md)
  
[<span data-ttu-id="3b3f2-194">GetAttachment-Vorgang</span><span class="sxs-lookup"><span data-stu-id="3b3f2-194">GetAttachment operation</span></span>](getattachment-operation.md)

