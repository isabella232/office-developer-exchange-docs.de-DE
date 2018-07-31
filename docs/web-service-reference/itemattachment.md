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
description: Das ItemAttachment-Element stellt ein Exchange-Element, das mit einem anderen Exchange-Element zugeordnet ist.
ms.openlocfilehash: 7bd3d22430fe04f1b28ae240102500609fe8d703
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353147"
---
# <a name="itemattachment"></a><span data-ttu-id="9227e-103">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="9227e-103">ItemAttachment</span></span>

<span data-ttu-id="9227e-104">Das **ItemAttachment** -Element stellt ein Exchange-Element, das mit einem anderen Exchange-Element zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="9227e-104">The **ItemAttachment** element represents an Exchange item that is attached to another Exchange item.</span></span> 
  
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

<span data-ttu-id="9227e-105">**ItemAttachmentType**</span><span class="sxs-lookup"><span data-stu-id="9227e-105">**ItemAttachmentType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="9227e-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="9227e-106">Attributes and elements</span></span>

<span data-ttu-id="9227e-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="9227e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9227e-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="9227e-108">Attributes</span></span>

<span data-ttu-id="9227e-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="9227e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9227e-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9227e-110">Child elements</span></span>

|<span data-ttu-id="9227e-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="9227e-111">**Element**</span></span>|<span data-ttu-id="9227e-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9227e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9227e-113">AttachmentId</span><span class="sxs-lookup"><span data-stu-id="9227e-113">AttachmentId</span></span>](attachmentid.md) <br/> |<span data-ttu-id="9227e-114">Identifiziert die Anlage.</span><span class="sxs-lookup"><span data-stu-id="9227e-114">Identifies the attachment.</span></span>  <br/> |
|[<span data-ttu-id="9227e-115">Name (AttachmentType)</span><span class="sxs-lookup"><span data-stu-id="9227e-115">Name (AttachmentType)</span></span>](name-attachmenttype.md) <br/> |<span data-ttu-id="9227e-116">Stellt den Namen der Anlage an.</span><span class="sxs-lookup"><span data-stu-id="9227e-116">Represents the name of the attachment.</span></span>  <br/> |
|[<span data-ttu-id="9227e-117">ContentType</span><span class="sxs-lookup"><span data-stu-id="9227e-117">ContentType</span></span>](contenttype.md) <br/> |<span data-ttu-id="9227e-118">Beschreibt den Multipurpose Internet Mail Extensions (MIME) gescannt.</span><span class="sxs-lookup"><span data-stu-id="9227e-118">Describes the Multipurpose Internet Mail Extensions (MIME) type of the attachment content.</span></span>  <br/> |
|[<span data-ttu-id="9227e-119">ContentId</span><span class="sxs-lookup"><span data-stu-id="9227e-119">ContentId</span></span>](contentid.md) <br/> |<span data-ttu-id="9227e-120">Stellt einen Bezeichner für den Inhalt der Anlage dar.</span><span class="sxs-lookup"><span data-stu-id="9227e-120">Represents an identifier to the contents of the attachment.</span></span> <span data-ttu-id="9227e-121">[ContentId](contentid.md) kann auf einen beliebigen Zeichenfolgenwert festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="9227e-121">[ContentId](contentid.md) can be set to any string value.</span></span> <span data-ttu-id="9227e-122">Anwendungen können [ContentId](contentid.md) um eigene Kennung Mechanismen zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="9227e-122">Applications can use [ContentId](contentid.md) to implement their own identification mechanisms.</span></span>  <br/> |
|[<span data-ttu-id="9227e-123">ContentLocation</span><span class="sxs-lookup"><span data-stu-id="9227e-123">ContentLocation</span></span>](contentlocation.md) <br/> |<span data-ttu-id="9227e-124">Enthält den URI Uniform Resource Identifier (), die den Speicherort des Inhalts der Anlage entspricht.</span><span class="sxs-lookup"><span data-stu-id="9227e-124">Contains the Uniform Resource Identifier (URI) that corresponds to the location of the content of the attachment.</span></span>  <br/> |
|[<span data-ttu-id="9227e-125">Size</span><span class="sxs-lookup"><span data-stu-id="9227e-125">Size</span></span>](size.md) <br/> |<span data-ttu-id="9227e-126">Stellt die Größe des Dateianlage in Bytes.</span><span class="sxs-lookup"><span data-stu-id="9227e-126">Represents the size in bytes of the file attachment.</span></span>  <br/> |
|[<span data-ttu-id="9227e-127">LastModifiedTime</span><span class="sxs-lookup"><span data-stu-id="9227e-127">LastModifiedTime</span></span>](lastmodifiedtime.md) <br/> |<span data-ttu-id="9227e-128">Darstellt, wenn die Anlage zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="9227e-128">Represents when the attachment was last modified.</span></span>  <br/> |
|[<span data-ttu-id="9227e-129">IsInline</span><span class="sxs-lookup"><span data-stu-id="9227e-129">IsInline</span></span>](isinline.md) <br/> |<span data-ttu-id="9227e-130">Stellt dar, ob die Anlage Inline innerhalb eines Elements angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="9227e-130">Represents whether the attachment appears inline within an item.</span></span>  <br/> |
|[<span data-ttu-id="9227e-131">Element</span><span class="sxs-lookup"><span data-stu-id="9227e-131">Item</span></span>](item.md) <br/> |<span data-ttu-id="9227e-132">Stellt eine generische Exchange Element Anlage.</span><span class="sxs-lookup"><span data-stu-id="9227e-132">Represents a generic Exchange item attachment.</span></span>  <br/> |
|[<span data-ttu-id="9227e-133">Meldung</span><span class="sxs-lookup"><span data-stu-id="9227e-133">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="9227e-134">Stellt eine Anlage Exchange e-Mail-Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="9227e-134">Represents an Exchange e-mail message attachment.</span></span>  <br/> |
|[<span data-ttu-id="9227e-135">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="9227e-135">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="9227e-136">Anlage Element Exchange-Kalender darstellt.</span><span class="sxs-lookup"><span data-stu-id="9227e-136">Represents an Exchange calendar item attachment.</span></span>  <br/> |
|[<span data-ttu-id="9227e-137">Contact</span><span class="sxs-lookup"><span data-stu-id="9227e-137">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="9227e-138">Anlage Kontaktelement Exchange darstellt.</span><span class="sxs-lookup"><span data-stu-id="9227e-138">Represents an Exchange contact item attachment.</span></span>  <br/> |
|[<span data-ttu-id="9227e-139">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="9227e-139">Task</span></span>](task.md) <br/> |<span data-ttu-id="9227e-140">Stellt eine Exchange-Task-Anlage.</span><span class="sxs-lookup"><span data-stu-id="9227e-140">Represents an Exchange task attachment.</span></span>  <br/> |
|[<span data-ttu-id="9227e-141">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="9227e-141">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="9227e-142">Stellt eine Besprechung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="9227e-142">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="9227e-143">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="9227e-143">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="9227e-144">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="9227e-144">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="9227e-145">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="9227e-145">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="9227e-146">Stellt eine Besprechungsantwort im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="9227e-146">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="9227e-147">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="9227e-147">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="9227e-148">Stellt eine Besprechungsabsage im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="9227e-148">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9227e-149">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9227e-149">Parent elements</span></span>

|<span data-ttu-id="9227e-150">**Element**</span><span class="sxs-lookup"><span data-stu-id="9227e-150">**Element**</span></span>|<span data-ttu-id="9227e-151">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9227e-151">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9227e-152">Anlagen</span><span class="sxs-lookup"><span data-stu-id="9227e-152">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="9227e-153">Enthält die Elemente und/oder Dateien, die ein Element in der Exchange-Informationsspeicher zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="9227e-153">Contains the items and/or files that are attached to an item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="9227e-154">Textwert</span><span class="sxs-lookup"><span data-stu-id="9227e-154">Text value</span></span>

<span data-ttu-id="9227e-155">Keine.</span><span class="sxs-lookup"><span data-stu-id="9227e-155">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9227e-156">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9227e-156">Remarks</span></span>

<span data-ttu-id="9227e-157">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="9227e-157">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9227e-158">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="9227e-158">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9227e-159">Namespace</span><span class="sxs-lookup"><span data-stu-id="9227e-159">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9227e-160">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="9227e-160">Schema Name</span></span>  <br/> |<span data-ttu-id="9227e-161">Schematypen</span><span class="sxs-lookup"><span data-stu-id="9227e-161">Types schema</span></span>  <br/> |
|<span data-ttu-id="9227e-162">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="9227e-162">Validation File</span></span>  <br/> |<span data-ttu-id="9227e-163">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9227e-163">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9227e-164">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="9227e-164">Can be Empty</span></span>  <br/> |<span data-ttu-id="9227e-165">False</span><span class="sxs-lookup"><span data-stu-id="9227e-165">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9227e-166">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9227e-166">See also</span></span>

- [<span data-ttu-id="9227e-167">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="9227e-167">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

