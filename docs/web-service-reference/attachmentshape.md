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
description: Das AttachmentShape-Element identifiziert zusätzliche Eigenschaften, die in einer Antwort auf eine GetAttachment-Anforderung zurückgegeben werden sollen.
ms.openlocfilehash: e70fbaad0f649c5afdc151b777efef0f8927ba1c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529665"
---
# <a name="attachmentshape"></a><span data-ttu-id="27c97-103">AttachmentShape</span><span class="sxs-lookup"><span data-stu-id="27c97-103">AttachmentShape</span></span>

<span data-ttu-id="27c97-104">Das **AttachmentShape** -Element identifiziert zusätzliche Eigenschaften, die in einer Antwort auf eine [GetAttachment](getattachment.md) -Anforderung zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="27c97-104">The **AttachmentShape** element identifies additional properties to return in a response to a [GetAttachment](getattachment.md) request.</span></span> 
  
- [<span data-ttu-id="27c97-105">GetAttachment</span><span class="sxs-lookup"><span data-stu-id="27c97-105">GetAttachment</span></span>](getattachment.md)
  
- [<span data-ttu-id="27c97-106">AttachmentShape</span><span class="sxs-lookup"><span data-stu-id="27c97-106">AttachmentShape</span></span>](attachmentshape.md)
  
```xml
<AttachmentShape>
   <IncludeMimeContent/>
   <BodyType/>
   <FilterHtmlContent/>
   <AdditionalProperties/>
</AttachmentShape>
```

 <span data-ttu-id="27c97-107">**AttachmentResponseShapeType**</span><span class="sxs-lookup"><span data-stu-id="27c97-107">**AttachmentResponseShapeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="27c97-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="27c97-108">Attributes and elements</span></span>

<span data-ttu-id="27c97-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="27c97-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="27c97-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="27c97-110">Attributes</span></span>

<span data-ttu-id="27c97-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="27c97-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="27c97-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="27c97-112">Child elements</span></span>

|<span data-ttu-id="27c97-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="27c97-113">**Element**</span></span>|<span data-ttu-id="27c97-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="27c97-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="27c97-115">IncludeMimeContent</span><span class="sxs-lookup"><span data-stu-id="27c97-115">IncludeMimeContent</span></span>](includemimecontent.md) <br/> |<span data-ttu-id="27c97-116">Gibt an, ob der Multipurpose Internet Mail Extensions (MIME) Inhalt eines Elements oder einer Anlage in der Antwort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="27c97-116">Specifies whether the Multipurpose Internet Mail Extensions (MIME) content of an item or attachment is returned in the response.</span></span> <span data-ttu-id="27c97-117">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="27c97-117">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="27c97-118">BodyType</span><span class="sxs-lookup"><span data-stu-id="27c97-118">BodyType</span></span>](bodytype.md) <br/> |<span data-ttu-id="27c97-119">Gibt an, wie der Textkörper in der Antwort formatiert wird.</span><span class="sxs-lookup"><span data-stu-id="27c97-119">Identifies how the body text is formatted in the response.</span></span> <span data-ttu-id="27c97-120">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="27c97-120">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="27c97-121">FilterHtmlContent</span><span class="sxs-lookup"><span data-stu-id="27c97-121">FilterHtmlContent</span></span>](filterhtmlcontent.md) <br/> |<span data-ttu-id="27c97-122">Gibt an, ob potenziell unsichere HTML-Inhalte aus einer Anlage gefiltert werden.</span><span class="sxs-lookup"><span data-stu-id="27c97-122">Specifies whether potentially unsafe HTML content is filtered from an attachment.</span></span> <span data-ttu-id="27c97-123">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="27c97-123">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="27c97-124">AdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="27c97-124">AdditionalProperties</span></span>](additionalproperties.md) <br/> |<span data-ttu-id="27c97-125">Identifiziert zusätzliche Eigenschaften, die in einer Antwort zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="27c97-125">Identifies additional properties to return in a response.</span></span> <span data-ttu-id="27c97-126">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="27c97-126">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="27c97-127">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="27c97-127">Parent elements</span></span>

|<span data-ttu-id="27c97-128">**Element**</span><span class="sxs-lookup"><span data-stu-id="27c97-128">**Element**</span></span>|<span data-ttu-id="27c97-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="27c97-129">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="27c97-130">GetAttachment</span><span class="sxs-lookup"><span data-stu-id="27c97-130">GetAttachment</span></span>](getattachment.md) <br/> |<span data-ttu-id="27c97-131">Das-Element, das eine Anforderung zum Abrufen einer Anlage aus einem Postfach im Exchange-Informationsspeicher definiert.</span><span class="sxs-lookup"><span data-stu-id="27c97-131">The element that defines a request to get an attachment from a mailbox in the Exchange store.</span></span>  <br/> <span data-ttu-id="27c97-132">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="27c97-132">The following is the XPath expression to this element:</span></span>  <br/>  `/GetAttachment` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="27c97-133">Textwert</span><span class="sxs-lookup"><span data-stu-id="27c97-133">Text value</span></span>

<span data-ttu-id="27c97-134">Keine.</span><span class="sxs-lookup"><span data-stu-id="27c97-134">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="27c97-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="27c97-135">Remarks</span></span>

<span data-ttu-id="27c97-136">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="27c97-136">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="27c97-137">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="27c97-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="27c97-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="27c97-138">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="27c97-139">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="27c97-139">Schema Name</span></span>  <br/> |<span data-ttu-id="27c97-140">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="27c97-140">Messages schema</span></span>  <br/> |
|<span data-ttu-id="27c97-141">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="27c97-141">Validation File</span></span>  <br/> |<span data-ttu-id="27c97-142">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="27c97-142">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="27c97-143">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="27c97-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="27c97-144">False</span><span class="sxs-lookup"><span data-stu-id="27c97-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="27c97-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="27c97-145">See also</span></span>

- [<span data-ttu-id="27c97-146">GetAttachment-Vorgang</span><span class="sxs-lookup"><span data-stu-id="27c97-146">GetAttachment operation</span></span>](getattachment-operation.md)
- [<span data-ttu-id="27c97-147">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="27c97-147">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

