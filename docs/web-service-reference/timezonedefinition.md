---
title: Zeitzonendefinition
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
description: Das Zeitzonendefinition-Element gibt die Zeiträume und Übergänge, die eine Zeitzone definiert.
ms.openlocfilehash: ffd5ed0c862af794e4aff2387f508849b1d5fd5d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839224"
---
# <a name="timezonedefinition"></a><span data-ttu-id="a30fe-103">Zeitzonendefinition</span><span class="sxs-lookup"><span data-stu-id="a30fe-103">TimeZoneDefinition</span></span>

<span data-ttu-id="a30fe-104">Das **Zeitzonendefinition** -Element gibt die Zeiträume und Übergänge, die eine Zeitzone definiert.</span><span class="sxs-lookup"><span data-stu-id="a30fe-104">The **TimeZoneDefinition** element specifies the periods and transitions that define a time zone.</span></span> 
  
```XML
<TimeZoneDefinition Id="" Name="">
   <Periods/>
   <TransitionsGroups/>
   <Transitions/>
</TimeZoneDefinition>

```

 <span data-ttu-id="a30fe-105">**TimeZoneDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="a30fe-105">**TimeZoneDefinitionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a30fe-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a30fe-106">Attributes and elements</span></span>

<span data-ttu-id="a30fe-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a30fe-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a30fe-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="a30fe-108">Attributes</span></span>

|<span data-ttu-id="a30fe-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="a30fe-109">**Attribute**</span></span>|<span data-ttu-id="a30fe-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a30fe-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a30fe-111">Id</span><span class="sxs-lookup"><span data-stu-id="a30fe-111">Id</span></span>  <br/> |<span data-ttu-id="a30fe-112">Den eindeutigen Bezeichner der Zeitzone darstellt.</span><span class="sxs-lookup"><span data-stu-id="a30fe-112">Represents the unique identifier of the time zone.</span></span>  <br/> |
|<span data-ttu-id="a30fe-113">Name</span><span class="sxs-lookup"><span data-stu-id="a30fe-113">Name</span></span>  <br/> |<span data-ttu-id="a30fe-114">Stellt den beschreibenden Namen der Zeitzone.</span><span class="sxs-lookup"><span data-stu-id="a30fe-114">Represents the descriptive name of the time zone.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a30fe-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a30fe-115">Child elements</span></span>

|<span data-ttu-id="a30fe-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="a30fe-116">**Element**</span></span>|<span data-ttu-id="a30fe-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a30fe-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a30fe-118">Perioden</span><span class="sxs-lookup"><span data-stu-id="a30fe-118">Periods</span></span>](periods.md) <br/> |<span data-ttu-id="a30fe-119">Stellt ein Array von [Periode](period.md) -Elementen, die den Uhrzeit-Offset in verschiedenen Phasen der Zeitzone definieren.</span><span class="sxs-lookup"><span data-stu-id="a30fe-119">Represents an array of [Period](period.md) elements that define the time offset at different stages of the time zone.</span></span>  <br/> |
|[<span data-ttu-id="a30fe-120">TransitionsGroups</span><span class="sxs-lookup"><span data-stu-id="a30fe-120">TransitionsGroups</span></span>](transitionsgroups.md) <br/> |<span data-ttu-id="a30fe-121">Stellt ein Array von [TransitionsGroup](transitionsgroup.md) -Elementen, die Zeitzone Übergänge angeben.</span><span class="sxs-lookup"><span data-stu-id="a30fe-121">Represents an array of [TransitionsGroup](transitionsgroup.md) elements that specify time zone transitions.</span></span>  <br/> |
|[<span data-ttu-id="a30fe-122">Übergänge</span><span class="sxs-lookup"><span data-stu-id="a30fe-122">Transitions</span></span>](transitions.md) <br/> |<span data-ttu-id="a30fe-123">Stellt ein Array von Zeitzone Übergänge.</span><span class="sxs-lookup"><span data-stu-id="a30fe-123">Represents an array of time zone transitions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a30fe-124">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a30fe-124">Parent elements</span></span>

|<span data-ttu-id="a30fe-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="a30fe-125">**Element**</span></span>|<span data-ttu-id="a30fe-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a30fe-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a30fe-127">TimeZoneDefinitions</span><span class="sxs-lookup"><span data-stu-id="a30fe-127">TimeZoneDefinitions</span></span>](timezonedefinitions.md) <br/> |<span data-ttu-id="a30fe-128">Stellt ein Array von Zeitzonendefinitionen.</span><span class="sxs-lookup"><span data-stu-id="a30fe-128">Represents an array of time zone definitions.</span></span>  <br/> |
|[<span data-ttu-id="a30fe-129">TimeZoneContext</span><span class="sxs-lookup"><span data-stu-id="a30fe-129">TimeZoneContext</span></span>](timezonecontext.md) <br/> |<span data-ttu-id="a30fe-130">Stellt die Definition der Standard-Zeitzone, die verwendet werden soll, für das Festlegen des Gültigkeitsbereichs der DateTime-Eigenschaft der Objekte, die erstellt, aktualisiert und mithilfe der Exchange-Webdienste (EWS) abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="a30fe-130">Represents the default time zone definition that is to be used for scoping the DateTime properties of objects that are created, updated, and retrieved by using Exchange Web Services (EWS).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a30fe-131">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a30fe-131">Remarks</span></span>

<span data-ttu-id="a30fe-132">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="a30fe-132">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a30fe-133">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="a30fe-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a30fe-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="a30fe-134">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a30fe-135">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a30fe-135">Schema Name</span></span>  <br/> |<span data-ttu-id="a30fe-136">Schematypen</span><span class="sxs-lookup"><span data-stu-id="a30fe-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="a30fe-137">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a30fe-137">Validation File</span></span>  <br/> |<span data-ttu-id="a30fe-138">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a30fe-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a30fe-139">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="a30fe-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="a30fe-140">False</span><span class="sxs-lookup"><span data-stu-id="a30fe-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a30fe-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a30fe-141">See also</span></span>



- [<span data-ttu-id="a30fe-142">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="a30fe-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

