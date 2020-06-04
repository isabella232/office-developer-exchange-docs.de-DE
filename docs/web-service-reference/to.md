---
title: An
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- To
api_type:
- schema
ms.assetid: d14e46da-14bd-4a33-a78e-8ee314d9c1d8
description: Das to-Element gibt das Ziel des Zeit Zonen Übergangs an. Das Ziel ist entweder eine Zeit Zonen Periode oder eine Gruppe von Zeit Zonen Übergängen.
ms.openlocfilehash: 8cce700eedd64035f2e21be4db6b517f3f85d98d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468796"
---
# <a name="to"></a><span data-ttu-id="35240-104">An</span><span class="sxs-lookup"><span data-stu-id="35240-104">To</span></span>

<span data-ttu-id="35240-105">Das **to** -Element gibt das Ziel des Zeit Zonen Übergangs an.</span><span class="sxs-lookup"><span data-stu-id="35240-105">The **To** element specifies the target of the time zone transition.</span></span> <span data-ttu-id="35240-106">Das Ziel ist entweder eine Zeit Zonen Periode oder eine Gruppe von Zeit Zonen Übergängen.</span><span class="sxs-lookup"><span data-stu-id="35240-106">The target is either a time zone period or a group of time zone transitions.</span></span> 
  
```xml
<To Kind=""/>
```

 <span data-ttu-id="35240-107">**TransitionTargetType**</span><span class="sxs-lookup"><span data-stu-id="35240-107">**TransitionTargetType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="35240-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="35240-108">Attributes and elements</span></span>

<span data-ttu-id="35240-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="35240-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="35240-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="35240-110">Attributes</span></span>

|<span data-ttu-id="35240-111">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="35240-111">**Attribute**</span></span>|<span data-ttu-id="35240-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="35240-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="35240-113">Art</span><span class="sxs-lookup"><span data-stu-id="35240-113">Kind</span></span>  <br/> |<span data-ttu-id="35240-114">Gibt an, ob das Zeit Zonen Übergangs Ziel eine Zeit Zonen Periode oder eine Gruppe von Zeit Zonen Übergängen ist.</span><span class="sxs-lookup"><span data-stu-id="35240-114">Indicates whether the time zone transition target is a time zone period or of a group of time zone transitions.</span></span>  <br/> |
   
#### <a name="kind-attribute-values"></a><span data-ttu-id="35240-115">Kind-Attributwerte</span><span class="sxs-lookup"><span data-stu-id="35240-115">Kind attribute values</span></span>

|<span data-ttu-id="35240-116">**Wert**</span><span class="sxs-lookup"><span data-stu-id="35240-116">**Value**</span></span>|<span data-ttu-id="35240-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="35240-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="35240-118">Punkt</span><span class="sxs-lookup"><span data-stu-id="35240-118">Period</span></span>  <br/> |<span data-ttu-id="35240-119">Gibt an, dass das Zeit Zonen Übergangs Ziel eine Zeit Zonen Periode ist.</span><span class="sxs-lookup"><span data-stu-id="35240-119">Specifies that the time zone transition target is a time zone period.</span></span>  <br/> |
|<span data-ttu-id="35240-120">Gruppe</span><span class="sxs-lookup"><span data-stu-id="35240-120">Group</span></span>  <br/> |<span data-ttu-id="35240-121">Gibt an, dass das Zeit Zonen Übergangs Ziel eine Gruppe von Zeit Zonen Übergängen ist.</span><span class="sxs-lookup"><span data-stu-id="35240-121">Specifies that the time zone transition target is a group of time zone transitions.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="35240-122">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="35240-122">Child elements</span></span>

<span data-ttu-id="35240-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="35240-123">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="35240-124">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="35240-124">Parent elements</span></span>

|<span data-ttu-id="35240-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="35240-125">**Element**</span></span>|<span data-ttu-id="35240-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="35240-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="35240-127">AbsoluteDateTransition</span><span class="sxs-lookup"><span data-stu-id="35240-127">AbsoluteDateTransition</span></span>](absolutedatetransition.md) <br/> |<span data-ttu-id="35240-128">Stellt einen Zeitzonenübergang dar, der zu einem bestimmten Datum und zu einem bestimmten Zeitpunkt erfolgt.</span><span class="sxs-lookup"><span data-stu-id="35240-128">Represents a time zone transition that occurs on a specific date and at a specific time.</span></span>  <br/> |
|[<span data-ttu-id="35240-129">RecurringDayTransition</span><span class="sxs-lookup"><span data-stu-id="35240-129">RecurringDayTransition</span></span>](recurringdaytransition.md) <br/> |<span data-ttu-id="35240-130">Stellt einen Zeitzonenübergang dar, der an demselben Tag jedes Jahr erfolgt.</span><span class="sxs-lookup"><span data-stu-id="35240-130">Represents a time zone transition that occurs on the same day each year.</span></span>  <br/> |
|[<span data-ttu-id="35240-131">RecurringDateTransition</span><span class="sxs-lookup"><span data-stu-id="35240-131">RecurringDateTransition</span></span>](recurringdatetransition.md) <br/> |<span data-ttu-id="35240-132">Stellt einen Zeitzonenübergang dar, der an einem angegebenen Tag des Jahres erfolgt.</span><span class="sxs-lookup"><span data-stu-id="35240-132">Represents a time zone transition that occurs on a specified day of the year.</span></span>  <br/> |
|[<span data-ttu-id="35240-133">Übergang</span><span class="sxs-lookup"><span data-stu-id="35240-133">Transition</span></span>](transition.md) <br/> |<span data-ttu-id="35240-134">Stellt einen Zeitzonenübergang dar.</span><span class="sxs-lookup"><span data-stu-id="35240-134">Represents a time zone transition.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="35240-135">Textwert</span><span class="sxs-lookup"><span data-stu-id="35240-135">Text value</span></span>

<span data-ttu-id="35240-136">Der Textwert ist eine Zeichenfolge, die den eindeutigen Bezeichner des [Zeitraums](period.md) oder der [Transitions](transitionsgroup.md) angibt, der das Ziel des Zeit Zonen Übergangs darstellt.</span><span class="sxs-lookup"><span data-stu-id="35240-136">The text value is a string that specifies the unique identifier of the [Period](period.md) or [TransitionsGroup](transitionsgroup.md) that is the target of the time zone transition.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="35240-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="35240-137">Remarks</span></span>

<span data-ttu-id="35240-138">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Exchange Server ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="35240-138">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="35240-139">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="35240-139">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="35240-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="35240-140">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="35240-141">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="35240-141">Schema Name</span></span>  <br/> |<span data-ttu-id="35240-142">Schematypen</span><span class="sxs-lookup"><span data-stu-id="35240-142">Types schema</span></span>  <br/> |
|<span data-ttu-id="35240-143">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="35240-143">Validation File</span></span>  <br/> |<span data-ttu-id="35240-144">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="35240-144">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="35240-145">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="35240-145">Can be Empty</span></span>  <br/> |<span data-ttu-id="35240-146">False</span><span class="sxs-lookup"><span data-stu-id="35240-146">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="35240-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="35240-147">See also</span></span>



- [<span data-ttu-id="35240-148">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="35240-148">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

