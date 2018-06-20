---
title: ExtendedPropertyAttributedValue
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 90f3c5c5-f612-4e1b-b1f5-f92dd8524179
description: Das ExtendedPropertyAttributedValue-Element gibt die erweiterte Eigenschaften für eine Rolle.
ms.openlocfilehash: 92e4ec7f192ccb36ea68d7862e66cb7b3349819a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758353"
---
# <a name="extendedpropertyattributedvalue"></a><span data-ttu-id="a88ca-103">ExtendedPropertyAttributedValue</span><span class="sxs-lookup"><span data-stu-id="a88ca-103">ExtendedPropertyAttributedValue</span></span>

<span data-ttu-id="a88ca-104">Das **ExtendedPropertyAttributedValue** -Element gibt die erweiterte Eigenschaften für eine Rolle.</span><span class="sxs-lookup"><span data-stu-id="a88ca-104">The **ExtendedPropertyAttributedValue** element specifies extended properties for a persona.</span></span> 
  
```XML
<ExtendedPropertyAttributedValue>
    <Value/>
    <Attributions/>
</ExtendedPropertyAttributedValue>
```

 <span data-ttu-id="a88ca-105">**ExtendedPropertyAttributedValueType**</span><span class="sxs-lookup"><span data-stu-id="a88ca-105">**ExtendedPropertyAttributedValueType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a88ca-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a88ca-106">Attributes and elements</span></span>

<span data-ttu-id="a88ca-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a88ca-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a88ca-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="a88ca-108">Attributes</span></span>

<span data-ttu-id="a88ca-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="a88ca-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a88ca-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a88ca-110">Child elements</span></span>

|<span data-ttu-id="a88ca-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="a88ca-111">**Element**</span></span>|<span data-ttu-id="a88ca-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a88ca-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a88ca-113">Wert (ExtendedPropertyType)</span><span class="sxs-lookup"><span data-stu-id="a88ca-113">Value (ExtendedPropertyType)</span></span>](value-extendedpropertytype.md) <br/> |<span data-ttu-id="a88ca-114">Gibt ein Array von erweiterten Eigenschaften für eine Rolle.</span><span class="sxs-lookup"><span data-stu-id="a88ca-114">Specifies an array of extended properties for a persona.</span></span>  <br/> |
|[<span data-ttu-id="a88ca-115">Hinweise (ArrayOfValueAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="a88ca-115">Attributions (ArrayOfValueAttributionsType)</span></span>](attributions-arrayofvalueattributionstype.md) <br/> |<span data-ttu-id="a88ca-116">Gibt ein Array von Marken für zugeordneten **Wert** Elements an.</span><span class="sxs-lookup"><span data-stu-id="a88ca-116">Specifies an array of attributions for its associated **Value** element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a88ca-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a88ca-117">Parent elements</span></span>

|<span data-ttu-id="a88ca-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="a88ca-118">**Element**</span></span>|<span data-ttu-id="a88ca-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a88ca-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a88ca-120">ExtendedProperties (ArrayOfExtendedPropertyAttributedValueType)</span><span class="sxs-lookup"><span data-stu-id="a88ca-120">ExtendedProperties (ArrayOfExtendedPropertyAttributedValueType)</span></span>](extendedproperties-arrayofextendedpropertyattributedvaluetype.md) <br/> |<span data-ttu-id="a88ca-121">Enthält die erweiterten Eigenschaften für Vorgänge Unified Contact Store verwendet.</span><span class="sxs-lookup"><span data-stu-id="a88ca-121">Contains the extended properties used for Unified Contact Store operations.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a88ca-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a88ca-122">Remarks</span></span>

<span data-ttu-id="a88ca-123">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="a88ca-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="a88ca-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="a88ca-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a88ca-125">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="a88ca-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a88ca-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="a88ca-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a88ca-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a88ca-127">Schema Name</span></span>  <br/> |<span data-ttu-id="a88ca-128">Typschema</span><span class="sxs-lookup"><span data-stu-id="a88ca-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="a88ca-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a88ca-129">Validation File</span></span>  <br/> |<span data-ttu-id="a88ca-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a88ca-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="a88ca-131">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="a88ca-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="a88ca-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a88ca-132">See also</span></span>



- [<span data-ttu-id="a88ca-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="a88ca-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

