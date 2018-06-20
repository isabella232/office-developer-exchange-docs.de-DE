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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757739"
---
# <a name="createattachment-operation"></a><span data-ttu-id="7dcd0-103">CreateAttachment-Vorgang</span><span class="sxs-lookup"><span data-stu-id="7dcd0-103">CreateAttachment operation</span></span>

<span data-ttu-id="7dcd0-104">Der Vorgang CreateAttachment Anlage eines Elements oder einer Datei erstellt und fügt diese an das angegebene Element.</span><span class="sxs-lookup"><span data-stu-id="7dcd0-104">The CreateAttachment operation creates either an item or file attachment and attaches it to the specified item.</span></span>
  
## <a name="file-createattachment-request-example"></a><span data-ttu-id="7dcd0-105">Beispiel für die Datei CreateAttachment Anforderung</span><span class="sxs-lookup"><span data-stu-id="7dcd0-105">File CreateAttachment request example</span></span>

### <a name="description"></a><span data-ttu-id="7dcd0-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7dcd0-106">Description</span></span>

<span data-ttu-id="7dcd0-107">Im folgenden Beispiel wird eine Anforderung CreateAttachment veranschaulicht, wie eine Dateianlage zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7dcd0-107">The following example of a CreateAttachment request shows how to create a file attachment.</span></span>
  
### <a name="code"></a><span data-ttu-id="7dcd0-108">Code</span><span class="sxs-lookup"><span data-stu-id="7dcd0-108">Code</span></span>

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

### <a name="comment"></a><span data-ttu-id="7dcd0-109">Comment</span><span class="sxs-lookup"><span data-stu-id="7dcd0-109">Comment</span></span>

<span data-ttu-id="7dcd0-110">Ein Namen für die Anlage muss angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7dcd0-110">A name for the attachment must be provided.</span></span>
  
> [!NOTE]
> <span data-ttu-id="7dcd0-111">Das übergeordnete Element-ID und Key ändern wurden gekürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="7dcd0-111">The parent item identifier and change key have been shortened to preserve readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="7dcd0-112">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="7dcd0-112">Request elements</span></span>

<span data-ttu-id="7dcd0-113">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="7dcd0-113">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="7dcd0-114">CreateAttachment</span><span class="sxs-lookup"><span data-stu-id="7dcd0-114">CreateAttachment</span></span>](createattachment.md)
    
- [<span data-ttu-id="7dcd0-115">ParentItemId</span><span class="sxs-lookup"><span data-stu-id="7dcd0-115">ParentItemId</span></span>](parentitemid.md)
    
- [<span data-ttu-id="7dcd0-116">Anlagen</span><span class="sxs-lookup"><span data-stu-id="7dcd0-116">Attachments</span></span>](attachments-ex15websvcsotherref.md)
    
- [<span data-ttu-id="7dcd0-117">FileAttachment</span><span class="sxs-lookup"><span data-stu-id="7dcd0-117">FileAttachment</span></span>](fileattachment.md)
    
- [<span data-ttu-id="7dcd0-118">Name ("AttachmentType")</span><span class="sxs-lookup"><span data-stu-id="7dcd0-118">Name (AttachmentType)</span></span>](name-attachmenttype.md)
    
- [<span data-ttu-id="7dcd0-119">Inhalt</span><span class="sxs-lookup"><span data-stu-id="7dcd0-119">Content</span></span>](content.md)
    
## <a name="successful-file-createattachment-response-example"></a><span data-ttu-id="7dcd0-120">Erfolgreiche Datei CreateAttachment antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="7dcd0-120">Successful File CreateAttachment response example</span></span>

### <a name="description"></a><span data-ttu-id="7dcd0-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7dcd0-121">Description</span></span>

<span data-ttu-id="7dcd0-122">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die Anforderung CreateAttachment.</span><span class="sxs-lookup"><span data-stu-id="7dcd0-122">The following example shows a successful response to the CreateAttachment request.</span></span>
  
### <a name="code"></a><span data-ttu-id="7dcd0-123">Code</span><span class="sxs-lookup"><span data-stu-id="7dcd0-123">Code</span></span>

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

### <a name="comment"></a><span data-ttu-id="7dcd0-124">Comment</span><span class="sxs-lookup"><span data-stu-id="7dcd0-124">Comment</span></span>

<span data-ttu-id="7dcd0-125">Die Antwort enthält den Bezeichner der angehängten Datei.</span><span class="sxs-lookup"><span data-stu-id="7dcd0-125">The response contains the identifier of the attached file.</span></span> <span data-ttu-id="7dcd0-126">Sie enthält außerdem den Schlüssel-ID und ein Änderungsprotokoll das Stammelement.</span><span class="sxs-lookup"><span data-stu-id="7dcd0-126">It also contains the identifier and change key of the root item.</span></span> <span data-ttu-id="7dcd0-127">Die Element-IDs und Key ändern wurden gekürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="7dcd0-127">The item identifiers and change key have been shortened to preserve readability.</span></span>
  
### <a name="successful-response-elements"></a><span data-ttu-id="7dcd0-128">Elemente einer erfolgreichen Antwort</span><span class="sxs-lookup"><span data-stu-id="7dcd0-128">Successful response elements</span></span>

<span data-ttu-id="7dcd0-129">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="7dcd0-129">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="7dcd0-130">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="7dcd0-130">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="7dcd0-131">CreateAttachmentResponse</span><span class="sxs-lookup"><span data-stu-id="7dcd0-131">CreateAttachmentResponse</span></span>](createattachmentresponse.md)
    
- [<span data-ttu-id="7dcd0-132">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="7dcd0-132">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="7dcd0-133">CreateAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="7dcd0-133">CreateAttachmentResponseMessage</span></span>](createattachmentresponsemessage.md)
    
- [<span data-ttu-id="7dcd0-134">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="7dcd0-134">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="7dcd0-135">Anlagen</span><span class="sxs-lookup"><span data-stu-id="7dcd0-135">Attachments</span></span>](attachments-ex15websvcsotherref.md)
    
- [<span data-ttu-id="7dcd0-136">FileAttachment</span><span class="sxs-lookup"><span data-stu-id="7dcd0-136">FileAttachment</span></span>](fileattachment.md)
    
- [<span data-ttu-id="7dcd0-137">AttachmentId</span><span class="sxs-lookup"><span data-stu-id="7dcd0-137">AttachmentId</span></span>](attachmentid.md)
    
## <a name="item-createattachment-request-example"></a><span data-ttu-id="7dcd0-138">Element CreateAttachment anforderungsbeispiel</span><span class="sxs-lookup"><span data-stu-id="7dcd0-138">Item CreateAttachment request example</span></span>

### <a name="description"></a><span data-ttu-id="7dcd0-139">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7dcd0-139">Description</span></span>

<span data-ttu-id="7dcd0-140">Im folgenden Beispiel wird eine Anforderung CreateAttachment veranschaulicht, wie eine Elementanlage erstellen.</span><span class="sxs-lookup"><span data-stu-id="7dcd0-140">The following example of a CreateAttachment request shows how to create an item attachment.</span></span>
  
### <a name="code"></a><span data-ttu-id="7dcd0-141">Code</span><span class="sxs-lookup"><span data-stu-id="7dcd0-141">Code</span></span>

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

### <a name="comment"></a><span data-ttu-id="7dcd0-142">Comment</span><span class="sxs-lookup"><span data-stu-id="7dcd0-142">Comment</span></span>

<span data-ttu-id="7dcd0-143">Ein Namen für die Anlage muss angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7dcd0-143">A name for the attachment must be provided.</span></span>
  
 <span data-ttu-id="7dcd0-144">**Hinweis** Das übergeordnete Element-ID und Key ändern wurden gekürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="7dcd0-144">**Note** The parent item identifier and change key have been shortened to preserve readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="7dcd0-145">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="7dcd0-145">Request elements</span></span>

<span data-ttu-id="7dcd0-146">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="7dcd0-146">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="7dcd0-147">CreateAttachment</span><span class="sxs-lookup"><span data-stu-id="7dcd0-147">CreateAttachment</span></span>](createattachment.md)
    
- [<span data-ttu-id="7dcd0-148">ParentItemId</span><span class="sxs-lookup"><span data-stu-id="7dcd0-148">ParentItemId</span></span>](parentitemid.md)
    
- [<span data-ttu-id="7dcd0-149">Anlagen</span><span class="sxs-lookup"><span data-stu-id="7dcd0-149">Attachments</span></span>](attachments-ex15websvcsotherref.md)
    
- [<span data-ttu-id="7dcd0-150">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="7dcd0-150">ItemAttachment</span></span>](itemattachment.md)
    
- [<span data-ttu-id="7dcd0-151">Name ("AttachmentType")</span><span class="sxs-lookup"><span data-stu-id="7dcd0-151">Name (AttachmentType)</span></span>](name-attachmenttype.md)
    
- [<span data-ttu-id="7dcd0-152">Message</span><span class="sxs-lookup"><span data-stu-id="7dcd0-152">Message</span></span>](message-ex15websvcsotherref.md)
    
- [<span data-ttu-id="7dcd0-153">Betreff</span><span class="sxs-lookup"><span data-stu-id="7dcd0-153">Subject</span></span>](subject.md)
    
## <a name="successful-item-createattachment-response-example"></a><span data-ttu-id="7dcd0-154">Erfolgreiche Item CreateAttachment antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="7dcd0-154">Successful Item CreateAttachment response example</span></span>

### <a name="description"></a><span data-ttu-id="7dcd0-155">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7dcd0-155">Description</span></span>

<span data-ttu-id="7dcd0-156">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die Anforderung CreateAttachment.</span><span class="sxs-lookup"><span data-stu-id="7dcd0-156">The following example shows a successful response to the CreateAttachment request.</span></span>
  
### <a name="code"></a><span data-ttu-id="7dcd0-157">Code</span><span class="sxs-lookup"><span data-stu-id="7dcd0-157">Code</span></span>

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

### <a name="comment"></a><span data-ttu-id="7dcd0-158">Comment</span><span class="sxs-lookup"><span data-stu-id="7dcd0-158">Comment</span></span>

<span data-ttu-id="7dcd0-159">Die Antwort enthält den Bezeichner des neuen Anhang.</span><span class="sxs-lookup"><span data-stu-id="7dcd0-159">The response contains the identifier of the new attachment.</span></span> <span data-ttu-id="7dcd0-160">Sie enthält außerdem den Schlüssel-ID und ein Änderungsprotokoll das Stammelement.</span><span class="sxs-lookup"><span data-stu-id="7dcd0-160">It also contains the identifier and change key of the root item.</span></span> <span data-ttu-id="7dcd0-161">Das Stammelement ist das Element, das die Anlage enthält.</span><span class="sxs-lookup"><span data-stu-id="7dcd0-161">The root item is the item that contains the attachment.</span></span> <span data-ttu-id="7dcd0-162">Die Element-IDs und Key ändern wurden gekürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="7dcd0-162">The item identifiers and change key have been shortened to preserve readability.</span></span>
  
### <a name="successful-response-elements"></a><span data-ttu-id="7dcd0-163">Elemente einer erfolgreichen Antwort</span><span class="sxs-lookup"><span data-stu-id="7dcd0-163">Successful response elements</span></span>

<span data-ttu-id="7dcd0-164">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="7dcd0-164">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="7dcd0-165">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="7dcd0-165">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="7dcd0-166">CreateAttachmentResponse</span><span class="sxs-lookup"><span data-stu-id="7dcd0-166">CreateAttachmentResponse</span></span>](createattachmentresponse.md)
    
- [<span data-ttu-id="7dcd0-167">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="7dcd0-167">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="7dcd0-168">CreateAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="7dcd0-168">CreateAttachmentResponseMessage</span></span>](createattachmentresponsemessage.md)
    
- [<span data-ttu-id="7dcd0-169">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="7dcd0-169">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="7dcd0-170">Anlagen</span><span class="sxs-lookup"><span data-stu-id="7dcd0-170">Attachments</span></span>](attachments-ex15websvcsotherref.md)
    
- [<span data-ttu-id="7dcd0-171">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="7dcd0-171">ItemAttachment</span></span>](itemattachment.md)
    
- [<span data-ttu-id="7dcd0-172">AttachmentId</span><span class="sxs-lookup"><span data-stu-id="7dcd0-172">AttachmentId</span></span>](attachmentid.md)
    
## <a name="createattachment-error-response-example"></a><span data-ttu-id="7dcd0-173">Antwortbeispiel CreateAttachment-Fehler</span><span class="sxs-lookup"><span data-stu-id="7dcd0-173">CreateAttachment Error response example</span></span>

### <a name="description"></a><span data-ttu-id="7dcd0-174">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7dcd0-174">Description</span></span>

<span data-ttu-id="7dcd0-175">Das folgende Beispiel zeigt eine Fehlerantwort an die CreateAttachment-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="7dcd0-175">The following example shows an error response to the CreateAttachment request.</span></span> <span data-ttu-id="7dcd0-176">Der Fehler ist darauf zurückzuführen, dass der Name der Anlage nicht angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="7dcd0-176">The error is due to the fact that the name of the attachment was not specified.</span></span>
  
### <a name="code"></a><span data-ttu-id="7dcd0-177">Code</span><span class="sxs-lookup"><span data-stu-id="7dcd0-177">Code</span></span>

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

### <a name="error-response-elements"></a><span data-ttu-id="7dcd0-178">Fehler Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="7dcd0-178">Error response elements</span></span>

<span data-ttu-id="7dcd0-179">Folgende Elemente werden in der Fehlerantwort verwendet:</span><span class="sxs-lookup"><span data-stu-id="7dcd0-179">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="7dcd0-180">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="7dcd0-180">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="7dcd0-181">CreateAttachmentResponse</span><span class="sxs-lookup"><span data-stu-id="7dcd0-181">CreateAttachmentResponse</span></span>](createattachmentresponse.md)
    
- [<span data-ttu-id="7dcd0-182">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="7dcd0-182">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="7dcd0-183">CreateAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="7dcd0-183">CreateAttachmentResponseMessage</span></span>](createattachmentresponsemessage.md)
    
- [<span data-ttu-id="7dcd0-184">MessageText</span><span class="sxs-lookup"><span data-stu-id="7dcd0-184">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="7dcd0-185">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="7dcd0-185">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="7dcd0-186">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="7dcd0-186">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="7dcd0-187">MessageXml</span><span class="sxs-lookup"><span data-stu-id="7dcd0-187">MessageXml</span></span>](messagexml.md)
    
- [<span data-ttu-id="7dcd0-188">ExceptionFieldURI</span><span class="sxs-lookup"><span data-stu-id="7dcd0-188">ExceptionFieldURI</span></span>](exceptionfielduri.md)
    
- [<span data-ttu-id="7dcd0-189">Anlagen</span><span class="sxs-lookup"><span data-stu-id="7dcd0-189">Attachments</span></span>](attachments-ex15websvcsotherref.md)
    
## <a name="remarks"></a><span data-ttu-id="7dcd0-190">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7dcd0-190">Remarks</span></span>

<span data-ttu-id="7dcd0-191">Wenn mehrere Anlagen auf ein Element in einem einzigen Roundtrip angefügt sind, ist die RootItemChangeKey in der letzten Antwortnachricht diejenige, die den neuen Änderungsschlüssel des Elements darstellt, die Anlagen wurde.</span><span class="sxs-lookup"><span data-stu-id="7dcd0-191">If multiple attachments are attached to an item in a single round trip, the RootItemChangeKey in the last response message is the one that represents the new change key of the item that has the attachments.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7dcd0-192">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7dcd0-192">See also</span></span>



[<span data-ttu-id="7dcd0-193">DeleteAttachment-Vorgang</span><span class="sxs-lookup"><span data-stu-id="7dcd0-193">DeleteAttachment operation</span></span>](deleteattachment-operation.md)
  
[<span data-ttu-id="7dcd0-194">GetAttachment-Vorgang</span><span class="sxs-lookup"><span data-stu-id="7dcd0-194">GetAttachment operation</span></span>](getattachment-operation.md)

