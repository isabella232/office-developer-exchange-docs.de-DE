---
title: AttachmentId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AttachmentId
api_type:
- schema
ms.assetid: 55a5fd77-60d1-40fa-8144-770600cedc6a
description: Das Element AttachmentId identifiziert eine Anlage Element oder eine Datei. Dieses Element wird in CreateAttachment Antworten verwendet.
ms.openlocfilehash: 2910503d1661ca3aaeeb4e319deb39f6b57c5c0a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757393"
---
# <a name="attachmentid"></a><span data-ttu-id="5f858-104">AttachmentId</span><span class="sxs-lookup"><span data-stu-id="5f858-104">AttachmentId</span></span>

<span data-ttu-id="5f858-105">Das Element **AttachmentId** identifiziert eine Anlage Element oder eine Datei.</span><span class="sxs-lookup"><span data-stu-id="5f858-105">The **AttachmentId** element identifies an item or file attachment.</span></span> <span data-ttu-id="5f858-106">Dieses Element wird in CreateAttachment Antworten verwendet.</span><span class="sxs-lookup"><span data-stu-id="5f858-106">This element is used in CreateAttachment responses.</span></span> 
  
```xml
<AttachmentId Id="" RootItemId="" RootItemChangeKey="" />
```

 <span data-ttu-id="5f858-107">**AttachmentIdType**</span><span class="sxs-lookup"><span data-stu-id="5f858-107">**AttachmentIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5f858-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="5f858-108">Attributes and elements</span></span>

<span data-ttu-id="5f858-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="5f858-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5f858-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="5f858-110">Attributes</span></span>

|<span data-ttu-id="5f858-111">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="5f858-111">**Attribute**</span></span>|<span data-ttu-id="5f858-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5f858-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5f858-113">**Id**</span><span class="sxs-lookup"><span data-stu-id="5f858-113">**Id**</span></span> <br/> |<span data-ttu-id="5f858-114">Gibt die eindeutige ID der Anlage an.</span><span class="sxs-lookup"><span data-stu-id="5f858-114">Identifies the unique identifier of the attachment.</span></span>  <br/> |
|<span data-ttu-id="5f858-115">**RootItemId**</span><span class="sxs-lookup"><span data-stu-id="5f858-115">**RootItemId**</span></span> <br/> |<span data-ttu-id="5f858-116">Gibt den eindeutigen Bezeichner des Elements Stamm-Speicher, dem die Anlage angefügt werden.</span><span class="sxs-lookup"><span data-stu-id="5f858-116">Identifies the unique identifier of the root store item to which the attachment is attached.</span></span>  <br/> |
|<span data-ttu-id="5f858-117">**RootItemChangeKey**</span><span class="sxs-lookup"><span data-stu-id="5f858-117">**RootItemChangeKey**</span></span> <br/> |<span data-ttu-id="5f858-118">Identifiziert die Key ändern des Elements Stamm-Speicher, dem die Anlage angefügt werden.</span><span class="sxs-lookup"><span data-stu-id="5f858-118">Identifies the change key of the root store item to which the attachment is attached.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="5f858-119">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5f858-119">Child elements</span></span>

<span data-ttu-id="5f858-120">Keine.</span><span class="sxs-lookup"><span data-stu-id="5f858-120">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5f858-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5f858-121">Parent elements</span></span>

|<span data-ttu-id="5f858-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="5f858-122">**Element**</span></span>|<span data-ttu-id="5f858-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5f858-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5f858-124">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="5f858-124">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="5f858-125">Stellt ein Exchange-Element, das mit einem anderen Exchange-Element zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="5f858-125">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="5f858-126">FileAttachment</span><span class="sxs-lookup"><span data-stu-id="5f858-126">FileAttachment</span></span>](fileattachment.md) <br/> |<span data-ttu-id="5f858-127">Stellt eine Datei, die ein Element in der Exchange-Informationsspeicher zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="5f858-127">Represents a file that is attached to an item in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5f858-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5f858-128">Remarks</span></span>

<span data-ttu-id="5f858-129">Es ist wichtig, beachten Sie, dass wenn eine Anlage erstellt wird, der Key ändern die Stamm-Elements geändert wird.</span><span class="sxs-lookup"><span data-stu-id="5f858-129">It is important to note that when an attachment is created, the change key of the root item is altered.</span></span>
  
<span data-ttu-id="5f858-130">Das Element [AttachmentId (GetAttachment und DeleteAttachment)](attachmentid-getattachment-and-deleteattachment.md) wird in DeleteAttachment und GetAttachment Anforderungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="5f858-130">The [AttachmentId (GetAttachment and DeleteAttachment)](attachmentid-getattachment-and-deleteattachment.md) element is used in DeleteAttachment and GetAttachment requests.</span></span> 
  
<span data-ttu-id="5f858-131">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="5f858-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5f858-132">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="5f858-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5f858-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="5f858-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5f858-134">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="5f858-134">Schema name</span></span>  <br/> |<span data-ttu-id="5f858-135">Schematypen</span><span class="sxs-lookup"><span data-stu-id="5f858-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="5f858-136">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="5f858-136">Validation file</span></span>  <br/> |<span data-ttu-id="5f858-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5f858-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5f858-138">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="5f858-138">Can be empty</span></span>  <br/> |<span data-ttu-id="5f858-139">False</span><span class="sxs-lookup"><span data-stu-id="5f858-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5f858-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5f858-140">See also</span></span>

- [<span data-ttu-id="5f858-141">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="5f858-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

