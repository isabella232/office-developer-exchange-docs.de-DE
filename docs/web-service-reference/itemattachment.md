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
ms.openlocfilehash: 87e0331664f1fdf8857afc78500014d138f05401
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830137"
---
# <a name="itemattachment"></a><span data-ttu-id="763a8-103">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="763a8-103">ItemAttachment</span></span>

<span data-ttu-id="763a8-104">Das **ItemAttachment** -Element stellt ein Exchange-Element, das mit einem anderen Exchange-Element zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="763a8-104">The **ItemAttachment** element represents an Exchange item that is attached to another Exchange item.</span></span> 
  
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

 <span data-ttu-id="763a8-105">**ItemAttachmentType**</span><span class="sxs-lookup"><span data-stu-id="763a8-105">**ItemAttachmentType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="763a8-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="763a8-106">Attributes and elements</span></span>

<span data-ttu-id="763a8-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="763a8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="763a8-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="763a8-108">Attributes</span></span>

<span data-ttu-id="763a8-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="763a8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="763a8-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="763a8-110">Child elements</span></span>

|<span data-ttu-id="763a8-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="763a8-111">**Element**</span></span>|<span data-ttu-id="763a8-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="763a8-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="763a8-113">AttachmentId</span><span class="sxs-lookup"><span data-stu-id="763a8-113">AttachmentId</span></span>](attachmentid.md) <br/> |<span data-ttu-id="763a8-114">Identifiziert die Anlage.</span><span class="sxs-lookup"><span data-stu-id="763a8-114">Identifies the attachment.</span></span>  <br/> |
|[<span data-ttu-id="763a8-115">Name ("AttachmentType")</span><span class="sxs-lookup"><span data-stu-id="763a8-115">Name (AttachmentType)</span></span>](name-attachmenttype.md) <br/> |<span data-ttu-id="763a8-116">Stellt den Namen der Anlage an.</span><span class="sxs-lookup"><span data-stu-id="763a8-116">Represents the name of the attachment.</span></span>  <br/> |
|[<span data-ttu-id="763a8-117">ContentType</span><span class="sxs-lookup"><span data-stu-id="763a8-117">ContentType</span></span>](contenttype.md) <br/> |<span data-ttu-id="763a8-118">Beschreibt den Multipurpose Internet Mail Extensions (MIME) gescannt.</span><span class="sxs-lookup"><span data-stu-id="763a8-118">Describes the Multipurpose Internet Mail Extensions (MIME) type of the attachment content.</span></span>  <br/> |
|[<span data-ttu-id="763a8-119">ContentId</span><span class="sxs-lookup"><span data-stu-id="763a8-119">ContentId</span></span>](contentid.md) <br/> |<span data-ttu-id="763a8-120">Stellt einen Bezeichner für den Inhalt der Anlage dar.</span><span class="sxs-lookup"><span data-stu-id="763a8-120">Represents an identifier to the contents of the attachment.</span></span> <span data-ttu-id="763a8-121">[ContentId](contentid.md) kann auf einen beliebigen Zeichenfolgenwert festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="763a8-121">[ContentId](contentid.md) can be set to any string value.</span></span> <span data-ttu-id="763a8-122">Anwendungen können [ContentId](contentid.md) um eigene Kennung Mechanismen zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="763a8-122">Applications can use [ContentId](contentid.md) to implement their own identification mechanisms.</span></span>  <br/> |
|[<span data-ttu-id="763a8-123">ContentLocation</span><span class="sxs-lookup"><span data-stu-id="763a8-123">ContentLocation</span></span>](contentlocation.md) <br/> |<span data-ttu-id="763a8-124">Enthält den URI Uniform Resource Identifier (), die den Speicherort des Inhalts der Anlage entspricht.</span><span class="sxs-lookup"><span data-stu-id="763a8-124">Contains the Uniform Resource Identifier (URI) that corresponds to the location of the content of the attachment.</span></span>  <br/> |
|[<span data-ttu-id="763a8-125">Size</span><span class="sxs-lookup"><span data-stu-id="763a8-125">Size</span></span>](size.md) <br/> |<span data-ttu-id="763a8-126">Stellt die Größe des Dateianlage in Bytes.</span><span class="sxs-lookup"><span data-stu-id="763a8-126">Represents the size in bytes of the file attachment.</span></span>  <br/> |
|[<span data-ttu-id="763a8-127">ZuletztGeändertUm</span><span class="sxs-lookup"><span data-stu-id="763a8-127">LastModifiedTime</span></span>](lastmodifiedtime.md) <br/> |<span data-ttu-id="763a8-128">Darstellt, wenn die Anlage zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="763a8-128">Represents when the attachment was last modified.</span></span>  <br/> |
|[<span data-ttu-id="763a8-129">IsInline</span><span class="sxs-lookup"><span data-stu-id="763a8-129">IsInline</span></span>](isinline.md) <br/> |<span data-ttu-id="763a8-130">Stellt dar, ob die Anlage Inline innerhalb eines Elements angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="763a8-130">Represents whether the attachment appears inline within an item.</span></span>  <br/> |
|[<span data-ttu-id="763a8-131">Element</span><span class="sxs-lookup"><span data-stu-id="763a8-131">Item</span></span>](item.md) <br/> |<span data-ttu-id="763a8-132">Stellt eine generische Exchange Element Anlage.</span><span class="sxs-lookup"><span data-stu-id="763a8-132">Represents a generic Exchange item attachment.</span></span>  <br/> |
|[<span data-ttu-id="763a8-133">Message</span><span class="sxs-lookup"><span data-stu-id="763a8-133">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="763a8-134">Stellt eine Anlage Exchange e-Mail-Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="763a8-134">Represents an Exchange e-mail message attachment.</span></span>  <br/> |
|[<span data-ttu-id="763a8-135">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="763a8-135">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="763a8-136">Anlage Element Exchange-Kalender darstellt.</span><span class="sxs-lookup"><span data-stu-id="763a8-136">Represents an Exchange calendar item attachment.</span></span>  <br/> |
|[<span data-ttu-id="763a8-137">Contact</span><span class="sxs-lookup"><span data-stu-id="763a8-137">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="763a8-138">Anlage Kontaktelement Exchange darstellt.</span><span class="sxs-lookup"><span data-stu-id="763a8-138">Represents an Exchange contact item attachment.</span></span>  <br/> |
|[<span data-ttu-id="763a8-139">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="763a8-139">Task</span></span>](task.md) <br/> |<span data-ttu-id="763a8-140">Stellt eine Exchange-Task-Anlage.</span><span class="sxs-lookup"><span data-stu-id="763a8-140">Represents an Exchange task attachment.</span></span>  <br/> |
|[<span data-ttu-id="763a8-141">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="763a8-141">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="763a8-142">Stellt eine Besprechung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="763a8-142">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="763a8-143">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="763a8-143">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="763a8-144">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="763a8-144">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="763a8-145">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="763a8-145">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="763a8-146">Stellt eine Besprechungsantwort im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="763a8-146">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="763a8-147">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="763a8-147">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="763a8-148">Stellt eine Besprechungsabsage im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="763a8-148">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="763a8-149">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="763a8-149">Parent elements</span></span>

|<span data-ttu-id="763a8-150">**Element**</span><span class="sxs-lookup"><span data-stu-id="763a8-150">**Element**</span></span>|<span data-ttu-id="763a8-151">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="763a8-151">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="763a8-152">Anlagen</span><span class="sxs-lookup"><span data-stu-id="763a8-152">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="763a8-153">Enthält die Elemente und/oder Dateien, die ein Element in der Exchange-Informationsspeicher zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="763a8-153">Contains the items and/or files that are attached to an item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="763a8-154">Textwert</span><span class="sxs-lookup"><span data-stu-id="763a8-154">Text value</span></span>

<span data-ttu-id="763a8-155">Keine.</span><span class="sxs-lookup"><span data-stu-id="763a8-155">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="763a8-156">Hinweise</span><span class="sxs-lookup"><span data-stu-id="763a8-156">Remarks</span></span>

<span data-ttu-id="763a8-157">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="763a8-157">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="763a8-158">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="763a8-158">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="763a8-159">Namespace</span><span class="sxs-lookup"><span data-stu-id="763a8-159">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="763a8-160">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="763a8-160">Schema Name</span></span>  <br/> |<span data-ttu-id="763a8-161">Schematypen</span><span class="sxs-lookup"><span data-stu-id="763a8-161">Types schema</span></span>  <br/> |
|<span data-ttu-id="763a8-162">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="763a8-162">Validation File</span></span>  <br/> |<span data-ttu-id="763a8-163">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="763a8-163">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="763a8-164">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="763a8-164">Can be Empty</span></span>  <br/> |<span data-ttu-id="763a8-165">False</span><span class="sxs-lookup"><span data-stu-id="763a8-165">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="763a8-166">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="763a8-166">See also</span></span>



- [<span data-ttu-id="763a8-167">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="763a8-167">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

