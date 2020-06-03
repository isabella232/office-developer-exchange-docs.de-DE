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
description: Das RootItemId-Element identifiziert das Stammelement einer gelöschten Anlage.
ms.openlocfilehash: d8badd465fd5a93e1a6354d55ac5c4b080897152
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457095"
---
# <a name="rootitemid"></a><span data-ttu-id="e6003-103">RootItemId</span><span class="sxs-lookup"><span data-stu-id="e6003-103">RootItemId</span></span>

<span data-ttu-id="e6003-104">Das **RootItemId** -Element identifiziert das Stammelement einer gelöschten Anlage.</span><span class="sxs-lookup"><span data-stu-id="e6003-104">The **RootItemId** element identifies the root item of a deleted attachment.</span></span> 
  
[<span data-ttu-id="e6003-105">DeleteAttachmentResponse</span><span class="sxs-lookup"><span data-stu-id="e6003-105">DeleteAttachmentResponse</span></span>](deleteattachmentresponse.md)
  
[<span data-ttu-id="e6003-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="e6003-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="e6003-107">DeleteAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="e6003-107">DeleteAttachmentResponseMessage</span></span>](deleteattachmentresponsemessage.md)
  
[<span data-ttu-id="e6003-108">RootItemId</span><span class="sxs-lookup"><span data-stu-id="e6003-108">RootItemId</span></span>](rootitemid.md)
  
```xml
<RootItemId RootItemId="" RootItemChangeKey="" />
```

 <span data-ttu-id="e6003-109">**RootItemIdType**</span><span class="sxs-lookup"><span data-stu-id="e6003-109">**RootItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e6003-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e6003-110">Attributes and elements</span></span>

<span data-ttu-id="e6003-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e6003-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e6003-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="e6003-112">Attributes</span></span>

|<span data-ttu-id="e6003-113">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="e6003-113">**Attribute**</span></span>|<span data-ttu-id="e6003-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e6003-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e6003-115">**RootItemId**</span><span class="sxs-lookup"><span data-stu-id="e6003-115">**RootItemId**</span></span> <br/> |<span data-ttu-id="e6003-116">Identifiziert das Stammelement einer gelöschten Anlage.</span><span class="sxs-lookup"><span data-stu-id="e6003-116">Identifies the root item of a deleted attachment.</span></span>  <br/> |
|<span data-ttu-id="e6003-117">**RootItemChangeKey**</span><span class="sxs-lookup"><span data-stu-id="e6003-117">**RootItemChangeKey**</span></span> <br/> |<span data-ttu-id="e6003-118">Gibt den neuen Änderungsschlüssel des Stammelements einer gelöschten Anlage an.</span><span class="sxs-lookup"><span data-stu-id="e6003-118">Identifies the new change key of the root item of a deleted attachment.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e6003-119">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e6003-119">Child elements</span></span>

<span data-ttu-id="e6003-120">Keine.</span><span class="sxs-lookup"><span data-stu-id="e6003-120">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e6003-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e6003-121">Parent elements</span></span>

|<span data-ttu-id="e6003-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="e6003-122">**Element**</span></span>|<span data-ttu-id="e6003-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e6003-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e6003-124">DeleteAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="e6003-124">DeleteAttachmentResponseMessage</span></span>](deleteattachmentresponsemessage.md) <br/> |<span data-ttu-id="e6003-125">Enthält den Status und das Ergebnis einer DeleteAttachment--Anforderung.</span><span class="sxs-lookup"><span data-stu-id="e6003-125">Contains the status and result of a DeleteAttachment request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e6003-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e6003-126">Remarks</span></span>

<span data-ttu-id="e6003-127">Das **RootItemId** -Element wird nur in DeleteAttachment--Antworten verwendet.</span><span class="sxs-lookup"><span data-stu-id="e6003-127">The **RootItemId** element is only used in DeleteAttachment responses.</span></span> <span data-ttu-id="e6003-128">Dadurch wird der Stammelement Bezeichner und noch wichtiger der neue Änderungsschlüssel für das übergeordnete Element identifiziert.</span><span class="sxs-lookup"><span data-stu-id="e6003-128">This identifies the root item identifier, and more importantly, the new change key to the parent item.</span></span> 
  
<span data-ttu-id="e6003-129">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="e6003-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e6003-130">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="e6003-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e6003-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="e6003-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e6003-132">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e6003-132">Schema name</span></span>  <br/> |<span data-ttu-id="e6003-133">Schematypen</span><span class="sxs-lookup"><span data-stu-id="e6003-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="e6003-134">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e6003-134">Validation file</span></span>  <br/> |<span data-ttu-id="e6003-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e6003-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e6003-136">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="e6003-136">Can be empty</span></span>  <br/> |<span data-ttu-id="e6003-137">False</span><span class="sxs-lookup"><span data-stu-id="e6003-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e6003-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e6003-138">See also</span></span>



[<span data-ttu-id="e6003-139">DeleteAttachment-</span><span class="sxs-lookup"><span data-stu-id="e6003-139">DeleteAttachment</span></span>](deleteattachment.md)
  
[<span data-ttu-id="e6003-140">DeleteAttachment-Vorgang</span><span class="sxs-lookup"><span data-stu-id="e6003-140">DeleteAttachment operation</span></span>](deleteattachment-operation.md)


- [<span data-ttu-id="e6003-141">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="e6003-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

