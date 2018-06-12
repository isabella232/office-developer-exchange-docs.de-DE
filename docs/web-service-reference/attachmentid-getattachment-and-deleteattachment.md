---
title: AttachmentId (GetAttachment und DeleteAttachment)
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
ms.assetid: 4bea1cb5-0a0f-4e14-9b09-f91af8cf9899
description: Das Element AttachmentId identifiziert eine Anlage.
ms.openlocfilehash: b0355b4a387c65e97fe973a1667e6b0a517ebf7e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757395"
---
# <a name="attachmentid-getattachment-and-deleteattachment"></a><span data-ttu-id="01a6b-103">AttachmentId (GetAttachment und DeleteAttachment)</span><span class="sxs-lookup"><span data-stu-id="01a6b-103">AttachmentId (GetAttachment and DeleteAttachment)</span></span>

<span data-ttu-id="01a6b-104">Das Element **AttachmentId** identifiziert eine Anlage.</span><span class="sxs-lookup"><span data-stu-id="01a6b-104">The **AttachmentId** element identifies a single attachment.</span></span> 
  
```xml
<AttachmentId Id="" />
```

 <span data-ttu-id="01a6b-105">**RequestAttachmentIdType**</span><span class="sxs-lookup"><span data-stu-id="01a6b-105">**RequestAttachmentIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="01a6b-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="01a6b-106">Attributes and elements</span></span>

<span data-ttu-id="01a6b-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="01a6b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="01a6b-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="01a6b-108">Attributes</span></span>

|<span data-ttu-id="01a6b-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="01a6b-109">**Attribute**</span></span>|<span data-ttu-id="01a6b-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="01a6b-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="01a6b-111">**Id**</span><span class="sxs-lookup"><span data-stu-id="01a6b-111">**Id**</span></span> <br/> |<span data-ttu-id="01a6b-112">Gibt den Bezeichner der Anlage.</span><span class="sxs-lookup"><span data-stu-id="01a6b-112">Specifies the attachment identifier.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="01a6b-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="01a6b-113">Child elements</span></span>

<span data-ttu-id="01a6b-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="01a6b-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="01a6b-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="01a6b-115">Parent elements</span></span>

|<span data-ttu-id="01a6b-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="01a6b-116">**Element**</span></span>|<span data-ttu-id="01a6b-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="01a6b-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="01a6b-118">AttachmentIds</span><span class="sxs-lookup"><span data-stu-id="01a6b-118">AttachmentIds</span></span>](attachmentids.md) <br/> | <span data-ttu-id="01a6b-119">Ein Array mit den IDs der Anlage enthält.</span><span class="sxs-lookup"><span data-stu-id="01a6b-119">Contains an array of attachment identifiers.</span></span><br/><br/>  <span data-ttu-id="01a6b-120">Folgende XPath-Ausdrücke werden für dieses Element verwendet:</span><span class="sxs-lookup"><span data-stu-id="01a6b-120">The following are the XPath expressions to this element:</span></span><br/><br/>`/DeleteAttachment/AttachmentIds`<br/><br/>`/GetAttachment/AttachmentIds` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="01a6b-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="01a6b-121">Remarks</span></span>

<span data-ttu-id="01a6b-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="01a6b-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="01a6b-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="01a6b-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="01a6b-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="01a6b-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="01a6b-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="01a6b-125">Schema Name</span></span>  <br/> |<span data-ttu-id="01a6b-126">Schematypen</span><span class="sxs-lookup"><span data-stu-id="01a6b-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="01a6b-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="01a6b-127">Validation File</span></span>  <br/> |<span data-ttu-id="01a6b-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="01a6b-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="01a6b-129">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="01a6b-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="01a6b-130">False</span><span class="sxs-lookup"><span data-stu-id="01a6b-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="01a6b-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="01a6b-131">See also</span></span>

- [<span data-ttu-id="01a6b-132">DeleteAttachment-Vorgang</span><span class="sxs-lookup"><span data-stu-id="01a6b-132">DeleteAttachment operation</span></span>](deleteattachment-operation.md)
- [<span data-ttu-id="01a6b-133">GetAttachment-Vorgang</span><span class="sxs-lookup"><span data-stu-id="01a6b-133">GetAttachment operation</span></span>](getattachment-operation.md)
