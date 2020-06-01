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
description: Das GetAttachment-Element ist das Stammelement in einer Anforderung zum Abrufen einer Anlage aus dem Exchange-Informationsspeicher.
ms.openlocfilehash: d03d086ff443db87b0104a2ec83599eb9eaea6b9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463979"
---
# <a name="getattachment"></a><span data-ttu-id="ce09a-103">GetAttachment</span><span class="sxs-lookup"><span data-stu-id="ce09a-103">GetAttachment</span></span>

<span data-ttu-id="ce09a-104">Das **GetAttachment** -Element ist das Stammelement in einer Anforderung zum Abrufen einer Anlage aus dem Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="ce09a-104">The **GetAttachment** element is the root element in a request to get an attachment from the Exchange store.</span></span> 
  
```xml
<GetAttachment>
   <AttachmentShape/>
   <AttachmentIds/>
</GetAttachment>
```

 <span data-ttu-id="ce09a-105">**Getattachmenttype**</span><span class="sxs-lookup"><span data-stu-id="ce09a-105">**GetAttachmentType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ce09a-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ce09a-106">Attributes and elements</span></span>

<span data-ttu-id="ce09a-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ce09a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ce09a-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="ce09a-108">Attributes</span></span>

<span data-ttu-id="ce09a-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="ce09a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ce09a-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ce09a-110">Child elements</span></span>

|<span data-ttu-id="ce09a-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="ce09a-111">**Element**</span></span>|<span data-ttu-id="ce09a-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ce09a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ce09a-113">AttachmentShape</span><span class="sxs-lookup"><span data-stu-id="ce09a-113">AttachmentShape</span></span>](attachmentshape.md) <br/> |<span data-ttu-id="ce09a-114">Identifiziert zusätzliche erweiterte Elementeigenschaften, die in einer Antwort auf eine [GetAttachment](getattachment.md) -Anforderung zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ce09a-114">Identifies additional extended item properties to return in a response to a [GetAttachment](getattachment.md) request.</span></span> <span data-ttu-id="ce09a-115">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="ce09a-115">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="ce09a-116">AttachmentIds</span><span class="sxs-lookup"><span data-stu-id="ce09a-116">AttachmentIds</span></span>](attachmentids.md) <br/> |<span data-ttu-id="ce09a-117">Enthält ein Array von Anlagen Bezeichnern.</span><span class="sxs-lookup"><span data-stu-id="ce09a-117">Contains an array of attachment identifiers.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ce09a-118">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ce09a-118">Parent elements</span></span>

<span data-ttu-id="ce09a-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="ce09a-119">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ce09a-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ce09a-120">Remarks</span></span>

<span data-ttu-id="ce09a-121">Das [AttachmentShape](attachmentshape.md) -Element ist nicht erforderlich, um die Eigenschaften zu identifizieren, die in der Antwort zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ce09a-121">The [AttachmentShape](attachmentshape.md) element is not required to identify the properties returned in the response.</span></span> <span data-ttu-id="ce09a-122">Der [GetAttachment-Vorgang](getattachment-operation.md) gibt den Namen, den ContentType, die Inhalts-ContentLocation und die Inhaltseigenschaften für Dateianlagen zurück.</span><span class="sxs-lookup"><span data-stu-id="ce09a-122">The [GetAttachment operation](getattachment-operation.md) returns the Name, ContentType, ContentId, ContentLocation, and the Content properties for file attachments.</span></span> <span data-ttu-id="ce09a-123">Bei Element Anlagen sind die zurückgegebenen Eigenschaften der Name, der ContentType, die Inhalts-ContentLocation und alle Eigenschaften des angefügten Elements.</span><span class="sxs-lookup"><span data-stu-id="ce09a-123">For item attachments, the returned properties are the Name, ContentType, ContentId, ContentLocation, and all the attached item's properties.</span></span> <span data-ttu-id="ce09a-124">Dies entspricht der Verwendung des allproperties-Basis-Shapes in einer [GetItem](getitem.md) -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="ce09a-124">This is equivalent to using the AllProperties base shape in a [GetItem](getitem.md) request.</span></span> 
  
<span data-ttu-id="ce09a-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="ce09a-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ce09a-126">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="ce09a-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ce09a-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="ce09a-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ce09a-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ce09a-128">Schema Name</span></span>  <br/> |<span data-ttu-id="ce09a-129">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="ce09a-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ce09a-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ce09a-130">Validation File</span></span>  <br/> |<span data-ttu-id="ce09a-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="ce09a-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ce09a-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="ce09a-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="ce09a-133">False</span><span class="sxs-lookup"><span data-stu-id="ce09a-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ce09a-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ce09a-134">See also</span></span>



[<span data-ttu-id="ce09a-135">GetAttachment-Vorgang</span><span class="sxs-lookup"><span data-stu-id="ce09a-135">GetAttachment operation</span></span>](getattachment-operation.md)
  
[<span data-ttu-id="ce09a-136">GetAttachmentResponse</span><span class="sxs-lookup"><span data-stu-id="ce09a-136">GetAttachmentResponse</span></span>](getattachmentresponse.md)

