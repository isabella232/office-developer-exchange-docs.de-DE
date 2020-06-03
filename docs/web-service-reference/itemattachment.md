---
title: ItemAttachment
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ItemAttachment
api_type:
- schema
ms.assetid: 089ee599-f45e-46f5-a18a-5cfb3d2851ff
description: Das ItemAttachment-Element stellt ein Exchange-Element dar, das an ein anderes Exchange-Element angefügt ist.
ms.openlocfilehash: c3a07fa091c05654a03cbff58fb20204c26c9061
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526438"
---
# <a name="itemattachment"></a><span data-ttu-id="f6d50-103">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="f6d50-103">ItemAttachment</span></span>

<span data-ttu-id="f6d50-104">Das **ItemAttachment** -Element stellt ein Exchange-Element dar, das an ein anderes Exchange-Element angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="f6d50-104">The **ItemAttachment** element represents an Exchange item that is attached to another Exchange item.</span></span> 
  
```xml
<ItemAttachment>
   <AttachmentId/>
   <Name/>
   <ContentType/>
   <ContentId/>
   <ContentLocation/>
   <Size/>
   <LastModifiedTime/>
   <IsInline/>
   <Item/>
</ItemAttachment>
```

```xml
<ItemAttachment>
   <AttachmentId/>
   <Name/>
   <ContentType/>
   <ContentId/>
   <ContentLocation/>
   <Size/>
   <LastModifiedTime/>
   <IsInline/>
   <Message/>
</ItemAttachment>
```

```xml
<ItemAttachment>
   <AttachmentId/>
   <Name/>
   <ContentType/>
   <ContentId/>
   <ContentLocation/>
   <Size/>
   <LastModifiedTime/>
   <IsInline/>
   <CalendarItem/>
</ItemAttachment>
```

```xml
<ItemAttachment>
   <AttachmentId/>
   <Name/>
   <ContentType/>
   <ContentId/>
   <ContentLocation/>
   <Size/>
   <LastModifiedTime/>
   <IsInline/>
   <Contact/>
</ItemAttachment>
```

```xml
<ItemAttachment>
   <AttachmentId/>
   <Name/>
   <ContentType/>
   <ContentId/>
   <ContentLocation/>
   <Size/>
   <LastModifiedTime/>
   <IsInline/>
   <Task/>
</ItemAttachment>
```

```xml
<ItemAttachment>
   <AttachmentId/>
   <Name/>
   <ContentType/>
   <ContentId/>
   <ContentLocation/>
   <Size/>
   <LastModifiedTime/>
   <IsInline/>
   <MeetingMessage/>
</ItemAttachment>
```

```xml
<ItemAttachment>
   <AttachmentId/>
   <Name/>
   <ContentType/>
   <ContentId/>
   <ContentLocation/>
   <Size/>
   <LastModifiedTime/>
   <IsInline/>
   <MeetingRequest/>
</ItemAttachment>
```

```xml
<ItemAttachment>
   <AttachmentId/>
   <Name/>
   <ContentType/>
   <ContentId/>
   <ContentLocation/>
   <Size/>
   <LastModifiedTime/>
   <IsInline/>
   <MeetingResponse/>
</ItemAttachment>
```

```xml
<ItemAttachment>
   <AttachmentId/>
   <Name/>
   <ContentType/>
   <ContentId/>
   <ContentLocation/>
   <Size/>
   <LastModifiedTime/>
   <IsInline/>
   <MeetingCancellation/>
</ItemAttachment>
```

<span data-ttu-id="f6d50-105">**ItemAttachmentType**</span><span class="sxs-lookup"><span data-stu-id="f6d50-105">**ItemAttachmentType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="f6d50-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f6d50-106">Attributes and elements</span></span>

<span data-ttu-id="f6d50-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f6d50-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f6d50-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="f6d50-108">Attributes</span></span>

<span data-ttu-id="f6d50-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="f6d50-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f6d50-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f6d50-110">Child elements</span></span>

|<span data-ttu-id="f6d50-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="f6d50-111">**Element**</span></span>|<span data-ttu-id="f6d50-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f6d50-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f6d50-113">AttachmentId</span><span class="sxs-lookup"><span data-stu-id="f6d50-113">AttachmentId</span></span>](attachmentid.md) <br/> |<span data-ttu-id="f6d50-114">Identifiziert die Anlage.</span><span class="sxs-lookup"><span data-stu-id="f6d50-114">Identifies the attachment.</span></span>  <br/> |
|[<span data-ttu-id="f6d50-115">Name (AttachmentType)</span><span class="sxs-lookup"><span data-stu-id="f6d50-115">Name (AttachmentType)</span></span>](name-attachmenttype.md) <br/> |<span data-ttu-id="f6d50-116">Stellt den Namen der Anlage dar.</span><span class="sxs-lookup"><span data-stu-id="f6d50-116">Represents the name of the attachment.</span></span>  <br/> |
|[<span data-ttu-id="f6d50-117">ContentType</span><span class="sxs-lookup"><span data-stu-id="f6d50-117">ContentType</span></span>](contenttype.md) <br/> |<span data-ttu-id="f6d50-118">Beschreibt die Multipurpose Internet Mail Extensions (MIME) Art des Anlage Inhalts.</span><span class="sxs-lookup"><span data-stu-id="f6d50-118">Describes the Multipurpose Internet Mail Extensions (MIME) type of the attachment content.</span></span>  <br/> |
|[<span data-ttu-id="f6d50-119">ContentId</span><span class="sxs-lookup"><span data-stu-id="f6d50-119">ContentId</span></span>](contentid.md) <br/> |<span data-ttu-id="f6d50-120">Stellt einen Bezeichner für den Inhalt der Anlage dar.</span><span class="sxs-lookup"><span data-stu-id="f6d50-120">Represents an identifier to the contents of the attachment.</span></span> <span data-ttu-id="f6d50-121">Die [Inhalts](contentid.md) -Nr kann auf einen beliebigen Zeichenfolgenwert festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f6d50-121">[ContentId](contentid.md) can be set to any string value.</span></span> <span data-ttu-id="f6d50-122">Anwendungen können mithilfe von [Content](contentid.md) -ID eigene Identifikations Mechanismen implementieren.</span><span class="sxs-lookup"><span data-stu-id="f6d50-122">Applications can use [ContentId](contentid.md) to implement their own identification mechanisms.</span></span>  <br/> |
|[<span data-ttu-id="f6d50-123">ContentLocation</span><span class="sxs-lookup"><span data-stu-id="f6d50-123">ContentLocation</span></span>](contentlocation.md) <br/> |<span data-ttu-id="f6d50-124">Enthält den URI (Uniform Resource Identifier), der dem Speicherort des Inhalts der Anlage entspricht.</span><span class="sxs-lookup"><span data-stu-id="f6d50-124">Contains the Uniform Resource Identifier (URI) that corresponds to the location of the content of the attachment.</span></span>  <br/> |
|[<span data-ttu-id="f6d50-125">Größe</span><span class="sxs-lookup"><span data-stu-id="f6d50-125">Size</span></span>](size.md) <br/> |<span data-ttu-id="f6d50-126">Stellt die Größe der Dateianlage in Bytes dar.</span><span class="sxs-lookup"><span data-stu-id="f6d50-126">Represents the size in bytes of the file attachment.</span></span>  <br/> |
|[<span data-ttu-id="f6d50-127">LastModifiedTime</span><span class="sxs-lookup"><span data-stu-id="f6d50-127">LastModifiedTime</span></span>](lastmodifiedtime.md) <br/> |<span data-ttu-id="f6d50-128">Stellt dar, wann die Anlage zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="f6d50-128">Represents when the attachment was last modified.</span></span>  <br/> |
|[<span data-ttu-id="f6d50-129">IsInline</span><span class="sxs-lookup"><span data-stu-id="f6d50-129">IsInline</span></span>](isinline.md) <br/> |<span data-ttu-id="f6d50-130">Stellt dar, ob die Anlage Inline in einem Element angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="f6d50-130">Represents whether the attachment appears inline within an item.</span></span>  <br/> |
|[<span data-ttu-id="f6d50-131">Element</span><span class="sxs-lookup"><span data-stu-id="f6d50-131">Item</span></span>](item.md) <br/> |<span data-ttu-id="f6d50-132">Stellt eine generische Exchange-Elementanlage dar.</span><span class="sxs-lookup"><span data-stu-id="f6d50-132">Represents a generic Exchange item attachment.</span></span>  <br/> |
|[<span data-ttu-id="f6d50-133">Meldung</span><span class="sxs-lookup"><span data-stu-id="f6d50-133">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="f6d50-134">Stellt eine Exchange-e-Mail-Nachrichtenanlage dar.</span><span class="sxs-lookup"><span data-stu-id="f6d50-134">Represents an Exchange e-mail message attachment.</span></span>  <br/> |
|[<span data-ttu-id="f6d50-135">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="f6d50-135">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="f6d50-136">Stellt eine Exchange-Kalenderelement Anlage dar.</span><span class="sxs-lookup"><span data-stu-id="f6d50-136">Represents an Exchange calendar item attachment.</span></span>  <br/> |
|[<span data-ttu-id="f6d50-137">Contact</span><span class="sxs-lookup"><span data-stu-id="f6d50-137">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="f6d50-138">Stellt eine Exchange-Kontaktelement Anlage dar.</span><span class="sxs-lookup"><span data-stu-id="f6d50-138">Represents an Exchange contact item attachment.</span></span>  <br/> |
|[<span data-ttu-id="f6d50-139">Task</span><span class="sxs-lookup"><span data-stu-id="f6d50-139">Task</span></span>](task.md) <br/> |<span data-ttu-id="f6d50-140">Stellt eine Exchange-Aufgabenanlage dar.</span><span class="sxs-lookup"><span data-stu-id="f6d50-140">Represents an Exchange task attachment.</span></span>  <br/> |
|[<span data-ttu-id="f6d50-141">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="f6d50-141">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="f6d50-142">Stellt eine Besprechung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="f6d50-142">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="f6d50-143">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="f6d50-143">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="f6d50-144">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="f6d50-144">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="f6d50-145">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="f6d50-145">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="f6d50-146">Stellt eine Besprechungsantwort im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="f6d50-146">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="f6d50-147">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="f6d50-147">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="f6d50-148">Stellt eine Besprechungsabsage im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="f6d50-148">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f6d50-149">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f6d50-149">Parent elements</span></span>

|<span data-ttu-id="f6d50-150">**Element**</span><span class="sxs-lookup"><span data-stu-id="f6d50-150">**Element**</span></span>|<span data-ttu-id="f6d50-151">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f6d50-151">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f6d50-152">Anlagen</span><span class="sxs-lookup"><span data-stu-id="f6d50-152">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="f6d50-153">Enthält die Elemente und/oder Dateien, die an ein Element im Exchange-Informationsspeicher angefügt sind.</span><span class="sxs-lookup"><span data-stu-id="f6d50-153">Contains the items and/or files that are attached to an item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f6d50-154">Textwert</span><span class="sxs-lookup"><span data-stu-id="f6d50-154">Text value</span></span>

<span data-ttu-id="f6d50-155">Keine.</span><span class="sxs-lookup"><span data-stu-id="f6d50-155">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f6d50-156">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f6d50-156">Remarks</span></span>

<span data-ttu-id="f6d50-157">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="f6d50-157">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f6d50-158">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="f6d50-158">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f6d50-159">Namespace</span><span class="sxs-lookup"><span data-stu-id="f6d50-159">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f6d50-160">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f6d50-160">Schema Name</span></span>  <br/> |<span data-ttu-id="f6d50-161">Schematypen</span><span class="sxs-lookup"><span data-stu-id="f6d50-161">Types schema</span></span>  <br/> |
|<span data-ttu-id="f6d50-162">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f6d50-162">Validation File</span></span>  <br/> |<span data-ttu-id="f6d50-163">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f6d50-163">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f6d50-164">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="f6d50-164">Can be Empty</span></span>  <br/> |<span data-ttu-id="f6d50-165">False</span><span class="sxs-lookup"><span data-stu-id="f6d50-165">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f6d50-166">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f6d50-166">See also</span></span>

- [<span data-ttu-id="f6d50-167">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="f6d50-167">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

