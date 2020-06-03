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
description: Der CreateAttachment-Vorgang erstellt entweder ein Element oder eine Dateianlage und fügt es an das angegebene Element an.
ms.openlocfilehash: 8028c56aa306774b54b39e5ee1ac0382b9113fa0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456570"
---
# <a name="createattachment-operation"></a><span data-ttu-id="41a85-103">CreateAttachment-Vorgang</span><span class="sxs-lookup"><span data-stu-id="41a85-103">CreateAttachment operation</span></span>

<span data-ttu-id="41a85-104">Der CreateAttachment-Vorgang erstellt entweder ein Element oder eine Dateianlage und fügt es an das angegebene Element an.</span><span class="sxs-lookup"><span data-stu-id="41a85-104">The CreateAttachment operation creates either an item or file attachment and attaches it to the specified item.</span></span>
  
## <a name="file-createattachment-request-example"></a><span data-ttu-id="41a85-105">Datei-CreateAttachment-Anforderungs Beispiel</span><span class="sxs-lookup"><span data-stu-id="41a85-105">File CreateAttachment request example</span></span>

### <a name="description"></a><span data-ttu-id="41a85-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="41a85-106">Description</span></span>

<span data-ttu-id="41a85-107">Im folgenden Beispiel einer CreateAttachment-Anforderung wird gezeigt, wie eine Dateianlage erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="41a85-107">The following example of a CreateAttachment request shows how to create a file attachment.</span></span>
  
### <a name="code"></a><span data-ttu-id="41a85-108">Code</span><span class="sxs-lookup"><span data-stu-id="41a85-108">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
<soap:Body>
  <CreateAttachment xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

### <a name="comment"></a><span data-ttu-id="41a85-109">Kommentar</span><span class="sxs-lookup"><span data-stu-id="41a85-109">Comment</span></span>

<span data-ttu-id="41a85-110">Es muss ein Name für die Anlage angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="41a85-110">A name for the attachment must be provided.</span></span>
  
> [!NOTE]
> <span data-ttu-id="41a85-111">Die übergeordnete Element-ID und der Änderungsschlüssel wurden verkürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="41a85-111">The parent item identifier and change key have been shortened to preserve readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="41a85-112">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="41a85-112">Request elements</span></span>

<span data-ttu-id="41a85-113">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="41a85-113">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="41a85-114">CreateAttachment</span><span class="sxs-lookup"><span data-stu-id="41a85-114">CreateAttachment</span></span>](createattachment.md)
    
- [<span data-ttu-id="41a85-115">ParentItemId</span><span class="sxs-lookup"><span data-stu-id="41a85-115">ParentItemId</span></span>](parentitemid.md)
    
- [<span data-ttu-id="41a85-116">Anlagen</span><span class="sxs-lookup"><span data-stu-id="41a85-116">Attachments</span></span>](attachments-ex15websvcsotherref.md)
    
- [<span data-ttu-id="41a85-117">FileAttachment</span><span class="sxs-lookup"><span data-stu-id="41a85-117">FileAttachment</span></span>](fileattachment.md)
    
- [<span data-ttu-id="41a85-118">Name (AttachmentType)</span><span class="sxs-lookup"><span data-stu-id="41a85-118">Name (AttachmentType)</span></span>](name-attachmenttype.md)
    
- [<span data-ttu-id="41a85-119">Content</span><span class="sxs-lookup"><span data-stu-id="41a85-119">Content</span></span>](content.md)
    
## <a name="successful-file-createattachment-response-example"></a><span data-ttu-id="41a85-120">Beispiel für erfolgreiche Datei-CreateAttachment-Antwort</span><span class="sxs-lookup"><span data-stu-id="41a85-120">Successful File CreateAttachment response example</span></span>

### <a name="description"></a><span data-ttu-id="41a85-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="41a85-121">Description</span></span>

<span data-ttu-id="41a85-122">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die CreateAttachment-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="41a85-122">The following example shows a successful response to the CreateAttachment request.</span></span>
  
### <a name="code"></a><span data-ttu-id="41a85-123">Code</span><span class="sxs-lookup"><span data-stu-id="41a85-123">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="653" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <CreateAttachmentResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                              xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                              xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comment"></a><span data-ttu-id="41a85-124">Kommentar</span><span class="sxs-lookup"><span data-stu-id="41a85-124">Comment</span></span>

<span data-ttu-id="41a85-125">Die Antwort enthält den Bezeichner der angefügten Datei.</span><span class="sxs-lookup"><span data-stu-id="41a85-125">The response contains the identifier of the attached file.</span></span> <span data-ttu-id="41a85-126">Es enthält auch den Bezeichner und den Änderungsschlüssel des Stammelements.</span><span class="sxs-lookup"><span data-stu-id="41a85-126">It also contains the identifier and change key of the root item.</span></span> <span data-ttu-id="41a85-127">Die Element-IDs und der Änderungsschlüssel wurden verkürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="41a85-127">The item identifiers and change key have been shortened to preserve readability.</span></span>
  
### <a name="successful-response-elements"></a><span data-ttu-id="41a85-128">Erfolgreiche Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="41a85-128">Successful response elements</span></span>

<span data-ttu-id="41a85-129">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="41a85-129">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="41a85-130">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="41a85-130">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="41a85-131">CreateAttachmentResponse</span><span class="sxs-lookup"><span data-stu-id="41a85-131">CreateAttachmentResponse</span></span>](createattachmentresponse.md)
    
- [<span data-ttu-id="41a85-132">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="41a85-132">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="41a85-133">CreateAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="41a85-133">CreateAttachmentResponseMessage</span></span>](createattachmentresponsemessage.md)
    
- [<span data-ttu-id="41a85-134">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="41a85-134">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="41a85-135">Anlagen</span><span class="sxs-lookup"><span data-stu-id="41a85-135">Attachments</span></span>](attachments-ex15websvcsotherref.md)
    
- [<span data-ttu-id="41a85-136">FileAttachment</span><span class="sxs-lookup"><span data-stu-id="41a85-136">FileAttachment</span></span>](fileattachment.md)
    
- [<span data-ttu-id="41a85-137">AttachmentId</span><span class="sxs-lookup"><span data-stu-id="41a85-137">AttachmentId</span></span>](attachmentid.md)
    
## <a name="item-createattachment-request-example"></a><span data-ttu-id="41a85-138">Element CreateAttachment-Anforderung (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="41a85-138">Item CreateAttachment request example</span></span>

### <a name="description"></a><span data-ttu-id="41a85-139">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="41a85-139">Description</span></span>

<span data-ttu-id="41a85-140">Im folgenden Beispiel einer CreateAttachment-Anforderung wird gezeigt, wie eine Elementanlage erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="41a85-140">The following example of a CreateAttachment request shows how to create an item attachment.</span></span>
  
### <a name="code"></a><span data-ttu-id="41a85-141">Code</span><span class="sxs-lookup"><span data-stu-id="41a85-141">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateAttachment xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

### <a name="comment"></a><span data-ttu-id="41a85-142">Kommentar</span><span class="sxs-lookup"><span data-stu-id="41a85-142">Comment</span></span>

<span data-ttu-id="41a85-143">Es muss ein Name für die Anlage angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="41a85-143">A name for the attachment must be provided.</span></span>
  
 <span data-ttu-id="41a85-144">**Hinweis:** Die übergeordnete Element-ID und der Änderungsschlüssel wurden verkürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="41a85-144">**Note** The parent item identifier and change key have been shortened to preserve readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="41a85-145">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="41a85-145">Request elements</span></span>

<span data-ttu-id="41a85-146">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="41a85-146">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="41a85-147">CreateAttachment</span><span class="sxs-lookup"><span data-stu-id="41a85-147">CreateAttachment</span></span>](createattachment.md)
    
- [<span data-ttu-id="41a85-148">ParentItemId</span><span class="sxs-lookup"><span data-stu-id="41a85-148">ParentItemId</span></span>](parentitemid.md)
    
- [<span data-ttu-id="41a85-149">Anlagen</span><span class="sxs-lookup"><span data-stu-id="41a85-149">Attachments</span></span>](attachments-ex15websvcsotherref.md)
    
- [<span data-ttu-id="41a85-150">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="41a85-150">ItemAttachment</span></span>](itemattachment.md)
    
- [<span data-ttu-id="41a85-151">Name (AttachmentType)</span><span class="sxs-lookup"><span data-stu-id="41a85-151">Name (AttachmentType)</span></span>](name-attachmenttype.md)
    
- [<span data-ttu-id="41a85-152">Meldung</span><span class="sxs-lookup"><span data-stu-id="41a85-152">Message</span></span>](message-ex15websvcsotherref.md)
    
- [<span data-ttu-id="41a85-153">Betreff</span><span class="sxs-lookup"><span data-stu-id="41a85-153">Subject</span></span>](subject.md)
    
## <a name="successful-item-createattachment-response-example"></a><span data-ttu-id="41a85-154">Erfolgreiches Element CreateAttachment-Antwort (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="41a85-154">Successful Item CreateAttachment response example</span></span>

### <a name="description"></a><span data-ttu-id="41a85-155">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="41a85-155">Description</span></span>

<span data-ttu-id="41a85-156">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die CreateAttachment-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="41a85-156">The following example shows a successful response to the CreateAttachment request.</span></span>
  
### <a name="code"></a><span data-ttu-id="41a85-157">Code</span><span class="sxs-lookup"><span data-stu-id="41a85-157">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="653" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <CreateAttachmentResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                              xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                              xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comment"></a><span data-ttu-id="41a85-158">Kommentar</span><span class="sxs-lookup"><span data-stu-id="41a85-158">Comment</span></span>

<span data-ttu-id="41a85-159">Die Antwort enthält den Bezeichner der neuen Anlage.</span><span class="sxs-lookup"><span data-stu-id="41a85-159">The response contains the identifier of the new attachment.</span></span> <span data-ttu-id="41a85-160">Es enthält auch den Bezeichner und den Änderungsschlüssel des Stammelements.</span><span class="sxs-lookup"><span data-stu-id="41a85-160">It also contains the identifier and change key of the root item.</span></span> <span data-ttu-id="41a85-161">Das Stammelement ist das Element, das die Anlage enthält.</span><span class="sxs-lookup"><span data-stu-id="41a85-161">The root item is the item that contains the attachment.</span></span> <span data-ttu-id="41a85-162">Die Element-IDs und der Änderungsschlüssel wurden verkürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="41a85-162">The item identifiers and change key have been shortened to preserve readability.</span></span>
  
### <a name="successful-response-elements"></a><span data-ttu-id="41a85-163">Erfolgreiche Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="41a85-163">Successful response elements</span></span>

<span data-ttu-id="41a85-164">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="41a85-164">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="41a85-165">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="41a85-165">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="41a85-166">CreateAttachmentResponse</span><span class="sxs-lookup"><span data-stu-id="41a85-166">CreateAttachmentResponse</span></span>](createattachmentresponse.md)
    
- [<span data-ttu-id="41a85-167">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="41a85-167">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="41a85-168">CreateAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="41a85-168">CreateAttachmentResponseMessage</span></span>](createattachmentresponsemessage.md)
    
- [<span data-ttu-id="41a85-169">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="41a85-169">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="41a85-170">Anlagen</span><span class="sxs-lookup"><span data-stu-id="41a85-170">Attachments</span></span>](attachments-ex15websvcsotherref.md)
    
- [<span data-ttu-id="41a85-171">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="41a85-171">ItemAttachment</span></span>](itemattachment.md)
    
- [<span data-ttu-id="41a85-172">AttachmentId</span><span class="sxs-lookup"><span data-stu-id="41a85-172">AttachmentId</span></span>](attachmentid.md)
    
## <a name="createattachment-error-response-example"></a><span data-ttu-id="41a85-173">Beispiel für eine CreateAttachment-Fehlerantwort</span><span class="sxs-lookup"><span data-stu-id="41a85-173">CreateAttachment Error response example</span></span>

### <a name="description"></a><span data-ttu-id="41a85-174">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="41a85-174">Description</span></span>

<span data-ttu-id="41a85-175">Das folgende Beispiel zeigt eine Fehlerantwort auf die CreateAttachment-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="41a85-175">The following example shows an error response to the CreateAttachment request.</span></span> <span data-ttu-id="41a85-176">Der Fehler ist darauf zurückzuführen, dass der Name der Anlage nicht angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="41a85-176">The error is due to the fact that the name of the attachment was not specified.</span></span>
  
### <a name="code"></a><span data-ttu-id="41a85-177">Code</span><span class="sxs-lookup"><span data-stu-id="41a85-177">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="653" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <CreateAttachmentResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                              xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                              xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="error-response-elements"></a><span data-ttu-id="41a85-178">Fehlerantwortelemente</span><span class="sxs-lookup"><span data-stu-id="41a85-178">Error response elements</span></span>

<span data-ttu-id="41a85-179">Folgende Elemente werden in der Fehlerantwort verwendet:</span><span class="sxs-lookup"><span data-stu-id="41a85-179">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="41a85-180">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="41a85-180">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="41a85-181">CreateAttachmentResponse</span><span class="sxs-lookup"><span data-stu-id="41a85-181">CreateAttachmentResponse</span></span>](createattachmentresponse.md)
    
- [<span data-ttu-id="41a85-182">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="41a85-182">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="41a85-183">CreateAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="41a85-183">CreateAttachmentResponseMessage</span></span>](createattachmentresponsemessage.md)
    
- [<span data-ttu-id="41a85-184">MessageText</span><span class="sxs-lookup"><span data-stu-id="41a85-184">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="41a85-185">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="41a85-185">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="41a85-186">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="41a85-186">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="41a85-187">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="41a85-187">MessageXml</span></span>](messagexml.md)
    
- [<span data-ttu-id="41a85-188">ExceptionFieldURI</span><span class="sxs-lookup"><span data-stu-id="41a85-188">ExceptionFieldURI</span></span>](exceptionfielduri.md)
    
- [<span data-ttu-id="41a85-189">Anlagen</span><span class="sxs-lookup"><span data-stu-id="41a85-189">Attachments</span></span>](attachments-ex15websvcsotherref.md)
    
## <a name="remarks"></a><span data-ttu-id="41a85-190">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="41a85-190">Remarks</span></span>

<span data-ttu-id="41a85-191">Wenn mehrere Anlagen an ein Element in einem einzelnen Roundtrip angefügt werden, ist die RootItemChangeKey in der letzten Antwortnachricht diejenige, die den neuen Änderungsschlüssel des Elements darstellt, das die Anlagen enthält.</span><span class="sxs-lookup"><span data-stu-id="41a85-191">If multiple attachments are attached to an item in a single round trip, the RootItemChangeKey in the last response message is the one that represents the new change key of the item that has the attachments.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="41a85-192">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="41a85-192">See also</span></span>



[<span data-ttu-id="41a85-193">DeleteAttachment-Vorgang</span><span class="sxs-lookup"><span data-stu-id="41a85-193">DeleteAttachment operation</span></span>](deleteattachment-operation.md)
  
[<span data-ttu-id="41a85-194">GetAttachment-Vorgang</span><span class="sxs-lookup"><span data-stu-id="41a85-194">GetAttachment operation</span></span>](getattachment-operation.md)

