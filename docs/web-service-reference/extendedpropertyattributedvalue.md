---
title: ExtendedPropertyAttributedValue
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 90f3c5c5-f612-4e1b-b1f5-f92dd8524179
description: Das ExtendedPropertyAttributedValue-Element gibt erweiterte Eigenschaften für eine Rolle an.
ms.openlocfilehash: 5c2ad5918d7ac666d5e26af6597b2c4c3dde6202
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460127"
---
# <a name="extendedpropertyattributedvalue"></a><span data-ttu-id="85612-103">ExtendedPropertyAttributedValue</span><span class="sxs-lookup"><span data-stu-id="85612-103">ExtendedPropertyAttributedValue</span></span>

<span data-ttu-id="85612-104">Das **ExtendedPropertyAttributedValue** -Element gibt erweiterte Eigenschaften für eine Rolle an.</span><span class="sxs-lookup"><span data-stu-id="85612-104">The **ExtendedPropertyAttributedValue** element specifies extended properties for a persona.</span></span> 
  
```XML
<ExtendedPropertyAttributedValue>
    <Value/>
    <Attributions/>
</ExtendedPropertyAttributedValue>
```

 <span data-ttu-id="85612-105">**ExtendedPropertyAttributedValueType**</span><span class="sxs-lookup"><span data-stu-id="85612-105">**ExtendedPropertyAttributedValueType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="85612-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="85612-106">Attributes and elements</span></span>

<span data-ttu-id="85612-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="85612-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="85612-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="85612-108">Attributes</span></span>

<span data-ttu-id="85612-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="85612-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="85612-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="85612-110">Child elements</span></span>

|<span data-ttu-id="85612-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="85612-111">**Element**</span></span>|<span data-ttu-id="85612-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="85612-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="85612-113">Wert (extendedpropertytype Schematyp)</span><span class="sxs-lookup"><span data-stu-id="85612-113">Value (ExtendedPropertyType)</span></span>](value-extendedpropertytype.md) <br/> |<span data-ttu-id="85612-114">Gibt ein Array von erweiterten Eigenschaften für eine Rolle an.</span><span class="sxs-lookup"><span data-stu-id="85612-114">Specifies an array of extended properties for a persona.</span></span>  <br/> |
|[<span data-ttu-id="85612-115">Zuordnungen (ArrayOfValueAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="85612-115">Attributions (ArrayOfValueAttributionsType)</span></span>](attributions-arrayofvalueattributionstype.md) <br/> |<span data-ttu-id="85612-116">Gibt ein Array von Attributes für das zugehörige **value** -Element an.</span><span class="sxs-lookup"><span data-stu-id="85612-116">Specifies an array of attributions for its associated **Value** element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="85612-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="85612-117">Parent elements</span></span>

|<span data-ttu-id="85612-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="85612-118">**Element**</span></span>|<span data-ttu-id="85612-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="85612-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="85612-120">ExtendedProperties (ArrayOfExtendedPropertyAttributedValueType)</span><span class="sxs-lookup"><span data-stu-id="85612-120">ExtendedProperties (ArrayOfExtendedPropertyAttributedValueType)</span></span>](extendedproperties-arrayofextendedpropertyattributedvaluetype.md) <br/> |<span data-ttu-id="85612-121">Enthält die erweiterten Eigenschaften, die für einheitliche Kontaktspeicher Vorgänge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="85612-121">Contains the extended properties used for Unified Contact Store operations.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="85612-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="85612-122">Remarks</span></span>

<span data-ttu-id="85612-123">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="85612-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="85612-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="85612-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="85612-125">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="85612-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="85612-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="85612-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="85612-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="85612-127">Schema Name</span></span>  <br/> |<span data-ttu-id="85612-128">Typschema</span><span class="sxs-lookup"><span data-stu-id="85612-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="85612-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="85612-129">Validation File</span></span>  <br/> |<span data-ttu-id="85612-130">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="85612-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="85612-131">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="85612-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="85612-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="85612-132">See also</span></span>



- [<span data-ttu-id="85612-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="85612-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

