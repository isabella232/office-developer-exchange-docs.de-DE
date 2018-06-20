---
title: GetAttachment
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetAttachment
api_type:
- schema
ms.assetid: 9443cf96-b451-4530-b868-490dff798673
description: Das GetAttachment-Element ist das Stammelement im eine Anforderung an eine Anlage aus dem Exchange-Speicher abzurufen.
ms.openlocfilehash: fb639c86a0654e8f9e9601310f7c2f5b0fc7d729
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758582"
---
# <a name="getattachment"></a><span data-ttu-id="a590d-103">GetAttachment</span><span class="sxs-lookup"><span data-stu-id="a590d-103">GetAttachment</span></span>

<span data-ttu-id="a590d-104">Das **GetAttachment** -Element ist das Stammelement im eine Anforderung an eine Anlage aus dem Exchange-Speicher abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a590d-104">The **GetAttachment** element is the root element in a request to get an attachment from the Exchange store.</span></span> 
  
```xml
<GetAttachment>
   <AttachmentShape/>
   <AttachmentIds/>
</GetAttachment>
```

 <span data-ttu-id="a590d-105">**GetAttachmentType**</span><span class="sxs-lookup"><span data-stu-id="a590d-105">**GetAttachmentType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a590d-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a590d-106">Attributes and elements</span></span>

<span data-ttu-id="a590d-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a590d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a590d-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="a590d-108">Attributes</span></span>

<span data-ttu-id="a590d-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="a590d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a590d-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a590d-110">Child elements</span></span>

|<span data-ttu-id="a590d-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="a590d-111">**Element**</span></span>|<span data-ttu-id="a590d-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a590d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a590d-113">AttachmentShape</span><span class="sxs-lookup"><span data-stu-id="a590d-113">AttachmentShape</span></span>](attachmentshape.md) <br/> |<span data-ttu-id="a590d-114">Zusätzliche erweiterte Elementeigenschaften in einer Antwort auf eine Anforderung [GetAttachment](getattachment.md) zurückzugebenden identifiziert.</span><span class="sxs-lookup"><span data-stu-id="a590d-114">Identifies additional extended item properties to return in a response to a [GetAttachment](getattachment.md) request.</span></span> <span data-ttu-id="a590d-115">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="a590d-115">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="a590d-116">AttachmentIds</span><span class="sxs-lookup"><span data-stu-id="a590d-116">AttachmentIds</span></span>](attachmentids.md) <br/> |<span data-ttu-id="a590d-117">Ein Array mit den IDs der Anlage enthält.</span><span class="sxs-lookup"><span data-stu-id="a590d-117">Contains an array of attachment identifiers.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a590d-118">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a590d-118">Parent elements</span></span>

<span data-ttu-id="a590d-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="a590d-119">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a590d-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a590d-120">Remarks</span></span>

<span data-ttu-id="a590d-121">Das [AttachmentShape](attachmentshape.md) -Element ist nicht erforderlich, um die in der Antwort zurückgegebenen Eigenschaften zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="a590d-121">The [AttachmentShape](attachmentshape.md) element is not required to identify the properties returned in the response.</span></span> <span data-ttu-id="a590d-122">Die [-Vorgangs GetAttachment](getattachment-operation.md) gibt den Namen, ContentType, ContentId, ContentLocation und die Content-Eigenschaften für Dateianlagen zurück.</span><span class="sxs-lookup"><span data-stu-id="a590d-122">The [GetAttachment operation](getattachment-operation.md) returns the Name, ContentType, ContentId, ContentLocation, and the Content properties for file attachments.</span></span> <span data-ttu-id="a590d-123">Für Anlagen sind die zurückgegebenen Eigenschaften den Namen, ContentType, ContentId, ContentLocation und alle die angefügte Eigenschaften des Elements.</span><span class="sxs-lookup"><span data-stu-id="a590d-123">For item attachments, the returned properties are the Name, ContentType, ContentId, ContentLocation, and all the attached item's properties.</span></span> <span data-ttu-id="a590d-124">Dies ist gleichbedeutend mit mithilfe des AllProperties-Basis-Shapes in einer [GetItem](getitem.md) -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="a590d-124">This is equivalent to using the AllProperties base shape in a [GetItem](getitem.md) request.</span></span> 
  
<span data-ttu-id="a590d-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="a590d-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a590d-126">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="a590d-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a590d-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="a590d-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a590d-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a590d-128">Schema Name</span></span>  <br/> |<span data-ttu-id="a590d-129">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="a590d-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="a590d-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a590d-130">Validation File</span></span>  <br/> |<span data-ttu-id="a590d-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="a590d-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a590d-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="a590d-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="a590d-133">False</span><span class="sxs-lookup"><span data-stu-id="a590d-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a590d-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a590d-134">See also</span></span>



[<span data-ttu-id="a590d-135">GetAttachment-Vorgang</span><span class="sxs-lookup"><span data-stu-id="a590d-135">GetAttachment operation</span></span>](getattachment-operation.md)
  
[<span data-ttu-id="a590d-136">GetAttachmentResponse</span><span class="sxs-lookup"><span data-stu-id="a590d-136">GetAttachmentResponse</span></span>](getattachmentresponse.md)

