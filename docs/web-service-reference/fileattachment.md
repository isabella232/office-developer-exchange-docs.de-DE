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
description: Das FileAttachment-Element stellt eine Datei dar, die an ein Element im Exchange-Informationsspeicher angefügt ist.
ms.openlocfilehash: db9b541fb2527ae3c09cbdb33bedea7fb215bd30
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461016"
---
# <a name="fileattachment"></a><span data-ttu-id="6bf22-103">FileAttachment</span><span class="sxs-lookup"><span data-stu-id="6bf22-103">FileAttachment</span></span>

<span data-ttu-id="6bf22-104">Das **FileAttachment** -Element stellt eine Datei dar, die an ein Element im Exchange-Informationsspeicher angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="6bf22-104">The **FileAttachment** element represents a file that is attached to an item in the Exchange store.</span></span> 
  
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

 <span data-ttu-id="6bf22-105">**Fileattachmenttype**</span><span class="sxs-lookup"><span data-stu-id="6bf22-105">**FileAttachmentType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6bf22-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="6bf22-106">Attributes and elements</span></span>

<span data-ttu-id="6bf22-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="6bf22-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6bf22-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="6bf22-108">Attributes</span></span>

<span data-ttu-id="6bf22-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="6bf22-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6bf22-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6bf22-110">Child elements</span></span>

|<span data-ttu-id="6bf22-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="6bf22-111">**Element**</span></span>|<span data-ttu-id="6bf22-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6bf22-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6bf22-113">AttachmentId</span><span class="sxs-lookup"><span data-stu-id="6bf22-113">AttachmentId</span></span>](attachmentid.md) <br/> |<span data-ttu-id="6bf22-114">Identifiziert die Dateianlage.</span><span class="sxs-lookup"><span data-stu-id="6bf22-114">Identifies the file attachment.</span></span>  <br/> |
|[<span data-ttu-id="6bf22-115">Name (AttachmentType)</span><span class="sxs-lookup"><span data-stu-id="6bf22-115">Name (AttachmentType)</span></span>](name-attachmenttype.md) <br/> |<span data-ttu-id="6bf22-116">Stellt den Namen der Anlage dar.</span><span class="sxs-lookup"><span data-stu-id="6bf22-116">Represents the name of the attachment.</span></span>  <br/> |
|[<span data-ttu-id="6bf22-117">ContentType</span><span class="sxs-lookup"><span data-stu-id="6bf22-117">ContentType</span></span>](contenttype.md) <br/> |<span data-ttu-id="6bf22-118">Beschreibt die Multipurpose Internet Mail Extensions (MIME) Art des Anlage Inhalts.</span><span class="sxs-lookup"><span data-stu-id="6bf22-118">Describes the Multipurpose Internet Mail Extensions (MIME) type of the attachment content.</span></span>  <br/> |
|[<span data-ttu-id="6bf22-119">ContentId</span><span class="sxs-lookup"><span data-stu-id="6bf22-119">ContentId</span></span>](contentid.md) <br/> |<span data-ttu-id="6bf22-120">Stellt einen Bezeichner für den Inhalt einer Anlage dar.</span><span class="sxs-lookup"><span data-stu-id="6bf22-120">Represents an identifier for the contents of an attachment.</span></span> <span data-ttu-id="6bf22-121">Die [Inhalts](contentid.md) -Nr kann auf einen beliebigen Zeichenfolgenwert festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="6bf22-121">[ContentId](contentid.md) can be set to any string value.</span></span> <span data-ttu-id="6bf22-122">Anwendungen können mithilfe von [Content](contentid.md) -ID eigene Identifikations Mechanismen implementieren.</span><span class="sxs-lookup"><span data-stu-id="6bf22-122">Applications can use [ContentId](contentid.md) to implement their own identification mechanisms.</span></span>  <br/> |
|[<span data-ttu-id="6bf22-123">ContentLocation</span><span class="sxs-lookup"><span data-stu-id="6bf22-123">ContentLocation</span></span>](contentlocation.md) <br/> |<span data-ttu-id="6bf22-124">Enthält den URI (Uniform Resource Identifier), der dem Speicherort des Inhalts der Anlage entspricht.</span><span class="sxs-lookup"><span data-stu-id="6bf22-124">Contains the Uniform Resource Identifier (URI) that corresponds to the location of the content of the attachment.</span></span>  <br/> |
|[<span data-ttu-id="6bf22-125">Größe</span><span class="sxs-lookup"><span data-stu-id="6bf22-125">Size</span></span>](size.md) <br/> |<span data-ttu-id="6bf22-126">Stellt die Größe der Dateianlage in Bytes dar.</span><span class="sxs-lookup"><span data-stu-id="6bf22-126">Represents the size in bytes of the file attachment.</span></span>  <br/> |
|[<span data-ttu-id="6bf22-127">LastModifiedTime</span><span class="sxs-lookup"><span data-stu-id="6bf22-127">LastModifiedTime</span></span>](lastmodifiedtime.md) <br/> |<span data-ttu-id="6bf22-128">Stellt dar, wann die Dateianlage zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="6bf22-128">Represents when the file attachment was last modified.</span></span>  <br/> |
|[<span data-ttu-id="6bf22-129">IsInline</span><span class="sxs-lookup"><span data-stu-id="6bf22-129">IsInline</span></span>](isinline.md) <br/> |<span data-ttu-id="6bf22-130">Stellt dar, ob die Anlage Inline in einem Element angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="6bf22-130">Represents whether the attachment appears inline within an item.</span></span>  <br/> |
|[<span data-ttu-id="6bf22-131">IsContactPhoto</span><span class="sxs-lookup"><span data-stu-id="6bf22-131">IsContactPhoto</span></span>](iscontactphoto.md) <br/> |<span data-ttu-id="6bf22-132">Gibt an, ob es sich bei der Dateianlage um ein Kontaktbild handelt.</span><span class="sxs-lookup"><span data-stu-id="6bf22-132">Indicates whether the file attachment is a contact picture.</span></span>  <br/> |
|[<span data-ttu-id="6bf22-133">Content</span><span class="sxs-lookup"><span data-stu-id="6bf22-133">Content</span></span>](content.md) <br/> |<span data-ttu-id="6bf22-134">Enthält den Base64-codierten Inhalt der Dateianlage.</span><span class="sxs-lookup"><span data-stu-id="6bf22-134">Contains the Base64-encoded contents of the file attachment.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6bf22-135">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6bf22-135">Parent elements</span></span>

|<span data-ttu-id="6bf22-136">**Element**</span><span class="sxs-lookup"><span data-stu-id="6bf22-136">**Element**</span></span>|<span data-ttu-id="6bf22-137">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6bf22-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6bf22-138">Anlagen</span><span class="sxs-lookup"><span data-stu-id="6bf22-138">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="6bf22-139">Enthält die Elemente oder Dateien, die an ein Element im Exchange-Informationsspeicher angefügt sind.</span><span class="sxs-lookup"><span data-stu-id="6bf22-139">Contains the items or files that are attached to an item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6bf22-140">Textwert</span><span class="sxs-lookup"><span data-stu-id="6bf22-140">Text value</span></span>

<span data-ttu-id="6bf22-141">Keine.</span><span class="sxs-lookup"><span data-stu-id="6bf22-141">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6bf22-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6bf22-142">Remarks</span></span>

<span data-ttu-id="6bf22-143">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="6bf22-143">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6bf22-144">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="6bf22-144">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6bf22-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="6bf22-145">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6bf22-146">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="6bf22-146">Schema name</span></span>  <br/> |<span data-ttu-id="6bf22-147">Schematypen</span><span class="sxs-lookup"><span data-stu-id="6bf22-147">Types schema</span></span>  <br/> |
|<span data-ttu-id="6bf22-148">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="6bf22-148">Validation file</span></span>  <br/> |<span data-ttu-id="6bf22-149">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6bf22-149">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6bf22-150">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="6bf22-150">Can be empty</span></span>  <br/> |<span data-ttu-id="6bf22-151">False</span><span class="sxs-lookup"><span data-stu-id="6bf22-151">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6bf22-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6bf22-152">See also</span></span>



- [<span data-ttu-id="6bf22-153">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="6bf22-153">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

