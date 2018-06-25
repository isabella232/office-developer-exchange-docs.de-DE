---
title: RootItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RootItemId
api_type:
- schema
ms.assetid: f613c705-17ce-48ce-aa64-4dc2cea25e31
description: Das RootItemId-Element identifiziert das Stammelement der Anlage zu einer gelöschten.
ms.openlocfilehash: 484b185db63c9692eaca7e43c49d6e95375a1a98
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831251"
---
# <a name="rootitemid"></a><span data-ttu-id="34c37-103">RootItemId</span><span class="sxs-lookup"><span data-stu-id="34c37-103">RootItemId</span></span>

<span data-ttu-id="34c37-104">Das **RootItemId** -Element identifiziert das Stammelement der Anlage zu einer gelöschten.</span><span class="sxs-lookup"><span data-stu-id="34c37-104">The **RootItemId** element identifies the root item of a deleted attachment.</span></span> 
  
[<span data-ttu-id="34c37-105">DeleteAttachmentResponse</span><span class="sxs-lookup"><span data-stu-id="34c37-105">DeleteAttachmentResponse</span></span>](deleteattachmentresponse.md)
  
[<span data-ttu-id="34c37-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="34c37-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="34c37-107">DeleteAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="34c37-107">DeleteAttachmentResponseMessage</span></span>](deleteattachmentresponsemessage.md)
  
[<span data-ttu-id="34c37-108">RootItemId</span><span class="sxs-lookup"><span data-stu-id="34c37-108">RootItemId</span></span>](rootitemid.md)
  
```xml
<RootItemId RootItemId="" RootItemChangeKey="" />
```

 <span data-ttu-id="34c37-109">**RootItemIdType**</span><span class="sxs-lookup"><span data-stu-id="34c37-109">**RootItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="34c37-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="34c37-110">Attributes and elements</span></span>

<span data-ttu-id="34c37-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="34c37-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="34c37-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="34c37-112">Attributes</span></span>

|<span data-ttu-id="34c37-113">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="34c37-113">**Attribute**</span></span>|<span data-ttu-id="34c37-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="34c37-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="34c37-115">**RootItemId**</span><span class="sxs-lookup"><span data-stu-id="34c37-115">**RootItemId**</span></span> <br/> |<span data-ttu-id="34c37-116">Das Stammelement der Anlage zu einer gelöschten identifiziert.</span><span class="sxs-lookup"><span data-stu-id="34c37-116">Identifies the root item of a deleted attachment.</span></span>  <br/> |
|<span data-ttu-id="34c37-117">**RootItemChangeKey**</span><span class="sxs-lookup"><span data-stu-id="34c37-117">**RootItemChangeKey**</span></span> <br/> |<span data-ttu-id="34c37-118">Gibt den neuen Änderungsschlüssel des Elements Stamm einer gelöschten Anlage.</span><span class="sxs-lookup"><span data-stu-id="34c37-118">Identifies the new change key of the root item of a deleted attachment.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="34c37-119">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="34c37-119">Child elements</span></span>

<span data-ttu-id="34c37-120">Keine.</span><span class="sxs-lookup"><span data-stu-id="34c37-120">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="34c37-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="34c37-121">Parent elements</span></span>

|<span data-ttu-id="34c37-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="34c37-122">**Element**</span></span>|<span data-ttu-id="34c37-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="34c37-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="34c37-124">DeleteAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="34c37-124">DeleteAttachmentResponseMessage</span></span>](deleteattachmentresponsemessage.md) <br/> |<span data-ttu-id="34c37-125">Enthält den Status und das Ergebnis einer Anforderung DeleteAttachment.</span><span class="sxs-lookup"><span data-stu-id="34c37-125">Contains the status and result of a DeleteAttachment request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="34c37-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="34c37-126">Remarks</span></span>

<span data-ttu-id="34c37-127">Das Element **RootItemId** wird nur in DeleteAttachment Antworten verwendet.</span><span class="sxs-lookup"><span data-stu-id="34c37-127">The **RootItemId** element is only used in DeleteAttachment responses.</span></span> <span data-ttu-id="34c37-128">Der Elementbezeichner Stamm und darüber hinaus die neue Key ändern, die dem übergeordneten Element identifiziert.</span><span class="sxs-lookup"><span data-stu-id="34c37-128">This identifies the root item identifier, and more importantly, the new change key to the parent item.</span></span> 
  
<span data-ttu-id="34c37-129">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="34c37-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="34c37-130">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="34c37-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="34c37-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="34c37-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="34c37-132">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="34c37-132">Schema name</span></span>  <br/> |<span data-ttu-id="34c37-133">Schematypen</span><span class="sxs-lookup"><span data-stu-id="34c37-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="34c37-134">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="34c37-134">Validation file</span></span>  <br/> |<span data-ttu-id="34c37-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="34c37-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="34c37-136">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="34c37-136">Can be empty</span></span>  <br/> |<span data-ttu-id="34c37-137">False</span><span class="sxs-lookup"><span data-stu-id="34c37-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="34c37-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="34c37-138">See also</span></span>



[<span data-ttu-id="34c37-139">DeleteAttachment</span><span class="sxs-lookup"><span data-stu-id="34c37-139">DeleteAttachment</span></span>](deleteattachment.md)
  
[<span data-ttu-id="34c37-140">DeleteAttachment-Vorgang</span><span class="sxs-lookup"><span data-stu-id="34c37-140">DeleteAttachment operation</span></span>](deleteattachment-operation.md)


- [<span data-ttu-id="34c37-141">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="34c37-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

