---
title: FileAttachment
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FileAttachment
api_type:
- schema
ms.assetid: 3ecea174-73d1-47fd-8917-6065cef1d565
description: Das Element FileAttachment repräsentiert eine Datei, die ein Element in der Exchange-Informationsspeicher zugeordnet ist.
ms.openlocfilehash: 5ce7aef753313aa9430f640bb3c26f652b8c1c43
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758426"
---
# <a name="fileattachment"></a><span data-ttu-id="a55a4-103">FileAttachment</span><span class="sxs-lookup"><span data-stu-id="a55a4-103">FileAttachment</span></span>

<span data-ttu-id="a55a4-104">Das Element **FileAttachment** repräsentiert eine Datei, die ein Element in der Exchange-Informationsspeicher zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a55a4-104">The **FileAttachment** element represents a file that is attached to an item in the Exchange store.</span></span> 
  
```XML
<FileAttachment>
   <AttachmentId/>
   <Name/>
   <ContentType/>
   <ContentId/>
   <ContentLocation/>
   <Size/>
   <LastModifiedTime/>
   <IsInline/>
   <IsContactPhoto/>
   <Content/>
</FileAttachment>
```

 <span data-ttu-id="a55a4-105">**FileAttachmentType**</span><span class="sxs-lookup"><span data-stu-id="a55a4-105">**FileAttachmentType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a55a4-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a55a4-106">Attributes and elements</span></span>

<span data-ttu-id="a55a4-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a55a4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a55a4-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="a55a4-108">Attributes</span></span>

<span data-ttu-id="a55a4-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="a55a4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a55a4-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a55a4-110">Child elements</span></span>

|<span data-ttu-id="a55a4-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="a55a4-111">**Element**</span></span>|<span data-ttu-id="a55a4-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a55a4-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a55a4-113">AttachmentId</span><span class="sxs-lookup"><span data-stu-id="a55a4-113">AttachmentId</span></span>](attachmentid.md) <br/> |<span data-ttu-id="a55a4-114">Identifiziert die Dateianlage.</span><span class="sxs-lookup"><span data-stu-id="a55a4-114">Identifies the file attachment.</span></span>  <br/> |
|[<span data-ttu-id="a55a4-115">Name ("AttachmentType")</span><span class="sxs-lookup"><span data-stu-id="a55a4-115">Name (AttachmentType)</span></span>](name-attachmenttype.md) <br/> |<span data-ttu-id="a55a4-116">Stellt den Namen der Anlage an.</span><span class="sxs-lookup"><span data-stu-id="a55a4-116">Represents the name of the attachment.</span></span>  <br/> |
|[<span data-ttu-id="a55a4-117">ContentType</span><span class="sxs-lookup"><span data-stu-id="a55a4-117">ContentType</span></span>](contenttype.md) <br/> |<span data-ttu-id="a55a4-118">Beschreibt den Multipurpose Internet Mail Extensions (MIME) gescannt.</span><span class="sxs-lookup"><span data-stu-id="a55a4-118">Describes the Multipurpose Internet Mail Extensions (MIME) type of the attachment content.</span></span>  <br/> |
|[<span data-ttu-id="a55a4-119">ContentId</span><span class="sxs-lookup"><span data-stu-id="a55a4-119">ContentId</span></span>](contentid.md) <br/> |<span data-ttu-id="a55a4-120">Stellt einen Bezeichner für den Inhalt einer Anlage an.</span><span class="sxs-lookup"><span data-stu-id="a55a4-120">Represents an identifier for the contents of an attachment.</span></span> <span data-ttu-id="a55a4-121">[ContentId](contentid.md) kann auf einen beliebigen Zeichenfolgenwert festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a55a4-121">[ContentId](contentid.md) can be set to any string value.</span></span> <span data-ttu-id="a55a4-122">Anwendungen können [ContentId](contentid.md) um eigene Kennung Mechanismen zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="a55a4-122">Applications can use [ContentId](contentid.md) to implement their own identification mechanisms.</span></span>  <br/> |
|[<span data-ttu-id="a55a4-123">ContentLocation</span><span class="sxs-lookup"><span data-stu-id="a55a4-123">ContentLocation</span></span>](contentlocation.md) <br/> |<span data-ttu-id="a55a4-124">Enthält den URI Uniform Resource Identifier (), die den Speicherort des Inhalts der Anlage entspricht.</span><span class="sxs-lookup"><span data-stu-id="a55a4-124">Contains the Uniform Resource Identifier (URI) that corresponds to the location of the content of the attachment.</span></span>  <br/> |
|[<span data-ttu-id="a55a4-125">Size</span><span class="sxs-lookup"><span data-stu-id="a55a4-125">Size</span></span>](size.md) <br/> |<span data-ttu-id="a55a4-126">Stellt die Größe des Dateianlage in Bytes.</span><span class="sxs-lookup"><span data-stu-id="a55a4-126">Represents the size in bytes of the file attachment.</span></span>  <br/> |
|[<span data-ttu-id="a55a4-127">ZuletztGeändertUm</span><span class="sxs-lookup"><span data-stu-id="a55a4-127">LastModifiedTime</span></span>](lastmodifiedtime.md) <br/> |<span data-ttu-id="a55a4-128">Stellt die bei die Dateianlage zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="a55a4-128">Represents when the file attachment was last modified.</span></span>  <br/> |
|[<span data-ttu-id="a55a4-129">IsInline</span><span class="sxs-lookup"><span data-stu-id="a55a4-129">IsInline</span></span>](isinline.md) <br/> |<span data-ttu-id="a55a4-130">Stellt dar, ob die Anlage Inline innerhalb eines Elements angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="a55a4-130">Represents whether the attachment appears inline within an item.</span></span>  <br/> |
|[<span data-ttu-id="a55a4-131">IsContactPhoto</span><span class="sxs-lookup"><span data-stu-id="a55a4-131">IsContactPhoto</span></span>](iscontactphoto.md) <br/> |<span data-ttu-id="a55a4-132">Gibt an, ob die Dateianlage ein Kontaktbild ist.</span><span class="sxs-lookup"><span data-stu-id="a55a4-132">Indicates whether the file attachment is a contact picture.</span></span>  <br/> |
|[<span data-ttu-id="a55a4-133">Inhalt</span><span class="sxs-lookup"><span data-stu-id="a55a4-133">Content</span></span>](content.md) <br/> |<span data-ttu-id="a55a4-134">Enthält den Base64-codierten Inhalt der Dateianlage.</span><span class="sxs-lookup"><span data-stu-id="a55a4-134">Contains the Base64-encoded contents of the file attachment.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a55a4-135">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a55a4-135">Parent elements</span></span>

|<span data-ttu-id="a55a4-136">**Element**</span><span class="sxs-lookup"><span data-stu-id="a55a4-136">**Element**</span></span>|<span data-ttu-id="a55a4-137">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a55a4-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a55a4-138">Anlagen</span><span class="sxs-lookup"><span data-stu-id="a55a4-138">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="a55a4-139">Enthält die Elemente oder Dateien, die ein Element in der Exchange-Informationsspeicher zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="a55a4-139">Contains the items or files that are attached to an item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a55a4-140">Textwert</span><span class="sxs-lookup"><span data-stu-id="a55a4-140">Text value</span></span>

<span data-ttu-id="a55a4-141">Keine.</span><span class="sxs-lookup"><span data-stu-id="a55a4-141">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a55a4-142">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a55a4-142">Remarks</span></span>

<span data-ttu-id="a55a4-143">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="a55a4-143">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a55a4-144">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="a55a4-144">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a55a4-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="a55a4-145">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a55a4-146">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a55a4-146">Schema name</span></span>  <br/> |<span data-ttu-id="a55a4-147">Schematypen</span><span class="sxs-lookup"><span data-stu-id="a55a4-147">Types schema</span></span>  <br/> |
|<span data-ttu-id="a55a4-148">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a55a4-148">Validation file</span></span>  <br/> |<span data-ttu-id="a55a4-149">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a55a4-149">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a55a4-150">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="a55a4-150">Can be empty</span></span>  <br/> |<span data-ttu-id="a55a4-151">False</span><span class="sxs-lookup"><span data-stu-id="a55a4-151">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a55a4-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a55a4-152">See also</span></span>



- [<span data-ttu-id="a55a4-153">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="a55a4-153">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

