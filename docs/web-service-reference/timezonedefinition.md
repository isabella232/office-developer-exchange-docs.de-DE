---
title: TimeZoneDefinition
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- TimeZoneDefinition
api_type:
- schema
ms.assetid: b005a80c-addb-4409-beff-e5162076752c
description: Das TimeZoneDefinition-Element gibt die Punkte und Übergänge an, die eine Zeitzone definieren.
ms.openlocfilehash: 58d34556686bfc77244b5829798eada51a1df843
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466066"
---
# <a name="timezonedefinition"></a><span data-ttu-id="395ad-103">TimeZoneDefinition</span><span class="sxs-lookup"><span data-stu-id="395ad-103">TimeZoneDefinition</span></span>

<span data-ttu-id="395ad-104">Das **TimeZoneDefinition** -Element gibt die Punkte und Übergänge an, die eine Zeitzone definieren.</span><span class="sxs-lookup"><span data-stu-id="395ad-104">The **TimeZoneDefinition** element specifies the periods and transitions that define a time zone.</span></span> 
  
```XML
<TimeZoneDefinition Id="" Name="">
   <Periods/>
   <TransitionsGroups/>
   <Transitions/>
</TimeZoneDefinition>

```

 <span data-ttu-id="395ad-105">**TimeZoneDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="395ad-105">**TimeZoneDefinitionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="395ad-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="395ad-106">Attributes and elements</span></span>

<span data-ttu-id="395ad-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="395ad-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="395ad-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="395ad-108">Attributes</span></span>

|<span data-ttu-id="395ad-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="395ad-109">**Attribute**</span></span>|<span data-ttu-id="395ad-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="395ad-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="395ad-111">Id</span><span class="sxs-lookup"><span data-stu-id="395ad-111">Id</span></span>  <br/> |<span data-ttu-id="395ad-112">Stellt den eindeutigen Bezeichner der Zeitzone dar.</span><span class="sxs-lookup"><span data-stu-id="395ad-112">Represents the unique identifier of the time zone.</span></span>  <br/> |
|<span data-ttu-id="395ad-113">Name</span><span class="sxs-lookup"><span data-stu-id="395ad-113">Name</span></span>  <br/> |<span data-ttu-id="395ad-114">Stellt den beschreibenden Namen der Zeitzone dar.</span><span class="sxs-lookup"><span data-stu-id="395ad-114">Represents the descriptive name of the time zone.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="395ad-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="395ad-115">Child elements</span></span>

|<span data-ttu-id="395ad-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="395ad-116">**Element**</span></span>|<span data-ttu-id="395ad-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="395ad-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="395ad-118">Zeiten</span><span class="sxs-lookup"><span data-stu-id="395ad-118">Periods</span></span>](periods.md) <br/> |<span data-ttu-id="395ad-119">Stellt ein Array von [Period](period.md) -Elementen dar, die den Zeit Offset in unterschiedlichen Phasen der Zeitzone definieren.</span><span class="sxs-lookup"><span data-stu-id="395ad-119">Represents an array of [Period](period.md) elements that define the time offset at different stages of the time zone.</span></span>  <br/> |
|[<span data-ttu-id="395ad-120">TransitionsGroups</span><span class="sxs-lookup"><span data-stu-id="395ad-120">TransitionsGroups</span></span>](transitionsgroups.md) <br/> |<span data-ttu-id="395ad-121">Stellt ein Array von [transitiongroup](transitionsgroup.md) -Elementen dar, die Zeit zonenübergänge angeben.</span><span class="sxs-lookup"><span data-stu-id="395ad-121">Represents an array of [TransitionsGroup](transitionsgroup.md) elements that specify time zone transitions.</span></span>  <br/> |
|[<span data-ttu-id="395ad-122">Übergänge</span><span class="sxs-lookup"><span data-stu-id="395ad-122">Transitions</span></span>](transitions.md) <br/> |<span data-ttu-id="395ad-123">Stellt ein Array von Zeit Zonen Übergängen dar.</span><span class="sxs-lookup"><span data-stu-id="395ad-123">Represents an array of time zone transitions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="395ad-124">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="395ad-124">Parent elements</span></span>

|<span data-ttu-id="395ad-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="395ad-125">**Element**</span></span>|<span data-ttu-id="395ad-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="395ad-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="395ad-127">TimeZoneDefinitions</span><span class="sxs-lookup"><span data-stu-id="395ad-127">TimeZoneDefinitions</span></span>](timezonedefinitions.md) <br/> |<span data-ttu-id="395ad-128">Stellt ein Array von Zeitzonendefinitionen dar.</span><span class="sxs-lookup"><span data-stu-id="395ad-128">Represents an array of time zone definitions.</span></span>  <br/> |
|[<span data-ttu-id="395ad-129">TimeZoneContext</span><span class="sxs-lookup"><span data-stu-id="395ad-129">TimeZoneContext</span></span>](timezonecontext.md) <br/> |<span data-ttu-id="395ad-130">Stellt die standardmäßige Zeitzonendefinition dar, die zum Festlegen der DateTime-Eigenschaften von Objekten verwendet werden soll, die mithilfe von Exchange-Webdienste erstellt, aktualisiert und abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="395ad-130">Represents the default time zone definition that is to be used for scoping the DateTime properties of objects that are created, updated, and retrieved by using Exchange Web Services (EWS).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="395ad-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="395ad-131">Remarks</span></span>

<span data-ttu-id="395ad-132">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="395ad-132">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="395ad-133">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="395ad-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="395ad-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="395ad-134">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="395ad-135">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="395ad-135">Schema Name</span></span>  <br/> |<span data-ttu-id="395ad-136">Schematypen</span><span class="sxs-lookup"><span data-stu-id="395ad-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="395ad-137">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="395ad-137">Validation File</span></span>  <br/> |<span data-ttu-id="395ad-138">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="395ad-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="395ad-139">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="395ad-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="395ad-140">False</span><span class="sxs-lookup"><span data-stu-id="395ad-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="395ad-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="395ad-141">See also</span></span>



- [<span data-ttu-id="395ad-142">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="395ad-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

