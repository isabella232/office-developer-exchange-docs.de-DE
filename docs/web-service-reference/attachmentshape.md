---
title: AttachmentShape
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AttachmentShape
api_type:
- schema
ms.assetid: 734914b5-3a16-4744-90a5-741fd30c4676
description: Das AttachmentShape-Element identifiziert zusätzliche Eigenschaften in einer Antwort auf eine Anforderung GetAttachment zurückgegeben werden sollen.
ms.openlocfilehash: dc6769faa5fd28ce31b796f86c507aec54abff7a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757397"
---
# <a name="attachmentshape"></a><span data-ttu-id="77041-103">AttachmentShape</span><span class="sxs-lookup"><span data-stu-id="77041-103">AttachmentShape</span></span>

<span data-ttu-id="77041-104">Das **AttachmentShape** -Element identifiziert zusätzliche Eigenschaften in einer Antwort auf eine Anforderung [GetAttachment](getattachment.md) zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="77041-104">The **AttachmentShape** element identifies additional properties to return in a response to a [GetAttachment](getattachment.md) request.</span></span> 
  
- [<span data-ttu-id="77041-105">GetAttachment</span><span class="sxs-lookup"><span data-stu-id="77041-105">GetAttachment</span></span>](getattachment.md)
  
- [<span data-ttu-id="77041-106">AttachmentShape</span><span class="sxs-lookup"><span data-stu-id="77041-106">AttachmentShape</span></span>](attachmentshape.md)
  
```xml
<AttachmentShape>
   <IncludeMimeContent/>
   <BodyType/>
   <FilterHtmlContent/>
   <AdditionalProperties/>
</AttachmentShape>
```

 <span data-ttu-id="77041-107">**AttachmentResponseShapeType**</span><span class="sxs-lookup"><span data-stu-id="77041-107">**AttachmentResponseShapeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="77041-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="77041-108">Attributes and elements</span></span>

<span data-ttu-id="77041-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="77041-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="77041-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="77041-110">Attributes</span></span>

<span data-ttu-id="77041-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="77041-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="77041-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="77041-112">Child elements</span></span>

|<span data-ttu-id="77041-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="77041-113">**Element**</span></span>|<span data-ttu-id="77041-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="77041-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="77041-115">IncludeMimeContent</span><span class="sxs-lookup"><span data-stu-id="77041-115">IncludeMimeContent</span></span>](includemimecontent.md) <br/> |<span data-ttu-id="77041-116">Gibt an, ob der Inhalt Multipurpose Internet Mail Extensions (MIME) eines Elements oder die Anlage in der Antwort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="77041-116">Specifies whether the Multipurpose Internet Mail Extensions (MIME) content of an item or attachment is returned in the response.</span></span> <span data-ttu-id="77041-117">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="77041-117">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="77041-118">BodyType</span><span class="sxs-lookup"><span data-stu-id="77041-118">BodyType</span></span>](bodytype.md) <br/> |<span data-ttu-id="77041-119">Gibt an, wie der Textkörper in der Antwort formatiert ist.</span><span class="sxs-lookup"><span data-stu-id="77041-119">Identifies how the body text is formatted in the response.</span></span> <span data-ttu-id="77041-120">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="77041-120">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="77041-121">FilterHtmlContent</span><span class="sxs-lookup"><span data-stu-id="77041-121">FilterHtmlContent</span></span>](filterhtmlcontent.md) <br/> |<span data-ttu-id="77041-122">Gibt an, ob potenziell unsichere HTML-Inhalte aus einer Anlage gefiltert wird.</span><span class="sxs-lookup"><span data-stu-id="77041-122">Specifies whether potentially unsafe HTML content is filtered from an attachment.</span></span> <span data-ttu-id="77041-123">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="77041-123">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="77041-124">AdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="77041-124">AdditionalProperties</span></span>](additionalproperties.md) <br/> |<span data-ttu-id="77041-125">Bezeichnet die zusätzliche Eigenschaften, die in eine Antwort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="77041-125">Identifies additional properties to return in a response.</span></span> <span data-ttu-id="77041-126">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="77041-126">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="77041-127">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="77041-127">Parent elements</span></span>

|<span data-ttu-id="77041-128">**Element**</span><span class="sxs-lookup"><span data-stu-id="77041-128">**Element**</span></span>|<span data-ttu-id="77041-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="77041-129">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="77041-130">GetAttachment</span><span class="sxs-lookup"><span data-stu-id="77041-130">GetAttachment</span></span>](getattachment.md) <br/> |<span data-ttu-id="77041-131">Das Element, das eine Anforderung definiert an eine Anlage aus einem Postfach im Exchange-Speicher abzurufen.</span><span class="sxs-lookup"><span data-stu-id="77041-131">The element that defines a request to get an attachment from a mailbox in the Exchange store.</span></span>  <br/> <span data-ttu-id="77041-132">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="77041-132">The following is the XPath expression to this element:</span></span>  <br/>  `/GetAttachment` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="77041-133">Textwert</span><span class="sxs-lookup"><span data-stu-id="77041-133">Text value</span></span>

<span data-ttu-id="77041-134">Keine.</span><span class="sxs-lookup"><span data-stu-id="77041-134">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="77041-135">Hinweise</span><span class="sxs-lookup"><span data-stu-id="77041-135">Remarks</span></span>

<span data-ttu-id="77041-136">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="77041-136">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="77041-137">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="77041-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="77041-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="77041-138">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="77041-139">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="77041-139">Schema Name</span></span>  <br/> |<span data-ttu-id="77041-140">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="77041-140">Messages schema</span></span>  <br/> |
|<span data-ttu-id="77041-141">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="77041-141">Validation File</span></span>  <br/> |<span data-ttu-id="77041-142">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="77041-142">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="77041-143">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="77041-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="77041-144">False</span><span class="sxs-lookup"><span data-stu-id="77041-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="77041-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="77041-145">See also</span></span>

- [<span data-ttu-id="77041-146">GetAttachment-Vorgang</span><span class="sxs-lookup"><span data-stu-id="77041-146">GetAttachment operation</span></span>](getattachment-operation.md)
- [<span data-ttu-id="77041-147">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="77041-147">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

