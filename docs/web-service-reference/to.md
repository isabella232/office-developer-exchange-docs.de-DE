---
title: Zweck
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
description: To-Element gibt das Ziel des Übergangs Zeitzone. Das Ziel ist eine Zeitzone Zeitraum oder eine Gruppe von Zeitzone Übergänge.
ms.openlocfilehash: dc7df8ed3ddd6a9b4222ffab4c2b47b00ee4ba0c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839218"
---
# <a name="to"></a><span data-ttu-id="f986b-104">Zweck</span><span class="sxs-lookup"><span data-stu-id="f986b-104">To</span></span>

<span data-ttu-id="f986b-105">**To** -Element gibt das Ziel des Übergangs Zeitzone.</span><span class="sxs-lookup"><span data-stu-id="f986b-105">The **To** element specifies the target of the time zone transition.</span></span> <span data-ttu-id="f986b-106">Das Ziel ist eine Zeitzone Zeitraum oder eine Gruppe von Zeitzone Übergänge.</span><span class="sxs-lookup"><span data-stu-id="f986b-106">The target is either a time zone period or a group of time zone transitions.</span></span> 
  
```xml
<To Kind=""/>
```

 <span data-ttu-id="f986b-107">**TransitionTargetType**</span><span class="sxs-lookup"><span data-stu-id="f986b-107">**TransitionTargetType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f986b-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f986b-108">Attributes and elements</span></span>

<span data-ttu-id="f986b-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f986b-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f986b-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="f986b-110">Attributes</span></span>

|<span data-ttu-id="f986b-111">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="f986b-111">**Attribute**</span></span>|<span data-ttu-id="f986b-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f986b-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f986b-113">Art</span><span class="sxs-lookup"><span data-stu-id="f986b-113">Kind</span></span>  <br/> |<span data-ttu-id="f986b-114">Gibt an, ob das Ziel des Vorgangs Übergang Zeitzone eine Zeitzone läuft oder einer Gruppe von Zeitzone Übergänge.</span><span class="sxs-lookup"><span data-stu-id="f986b-114">Indicates whether the time zone transition target is a time zone period or of a group of time zone transitions.</span></span>  <br/> |
   
#### <a name="kind-attribute-values"></a><span data-ttu-id="f986b-115">Kind Attributwerte</span><span class="sxs-lookup"><span data-stu-id="f986b-115">Kind attribute values</span></span>

|<span data-ttu-id="f986b-116">**Wert**</span><span class="sxs-lookup"><span data-stu-id="f986b-116">**Value**</span></span>|<span data-ttu-id="f986b-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f986b-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f986b-118">Punkt</span><span class="sxs-lookup"><span data-stu-id="f986b-118">Period</span></span>  <br/> |<span data-ttu-id="f986b-119">Gibt an, dass die Zeitzone Übergang als Ziel eines Zeitraums Zeitzone fungiert.</span><span class="sxs-lookup"><span data-stu-id="f986b-119">Specifies that the time zone transition target is a time zone period.</span></span>  <br/> |
|<span data-ttu-id="f986b-120">Gruppe</span><span class="sxs-lookup"><span data-stu-id="f986b-120">Group</span></span>  <br/> |<span data-ttu-id="f986b-121">Gibt an, dass die Zeitzone Übergang als Ziel einer Gruppe von Zeitzone Übergänge fungiert.</span><span class="sxs-lookup"><span data-stu-id="f986b-121">Specifies that the time zone transition target is a group of time zone transitions.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f986b-122">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f986b-122">Child elements</span></span>

<span data-ttu-id="f986b-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="f986b-123">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f986b-124">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f986b-124">Parent elements</span></span>

|<span data-ttu-id="f986b-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="f986b-125">**Element**</span></span>|<span data-ttu-id="f986b-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f986b-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f986b-127">AbsoluteDateTransition</span><span class="sxs-lookup"><span data-stu-id="f986b-127">AbsoluteDateTransition</span></span>](absolutedatetransition.md) <br/> |<span data-ttu-id="f986b-128">Stellt einen Zeitzone Übergang, die einem bestimmten Datum und zu einem bestimmten Zeitpunkt dar.</span><span class="sxs-lookup"><span data-stu-id="f986b-128">Represents a time zone transition that occurs on a specific date and at a specific time.</span></span>  <br/> |
|[<span data-ttu-id="f986b-129">RecurringDayTransition</span><span class="sxs-lookup"><span data-stu-id="f986b-129">RecurringDayTransition</span></span>](recurringdaytransition.md) <br/> |<span data-ttu-id="f986b-130">Stellt einen Zeitzone Übergang dar, bei dem gleichen Tag pro Jahr auftritt.</span><span class="sxs-lookup"><span data-stu-id="f986b-130">Represents a time zone transition that occurs on the same day each year.</span></span>  <br/> |
|[<span data-ttu-id="f986b-131">RecurringDateTransition</span><span class="sxs-lookup"><span data-stu-id="f986b-131">RecurringDateTransition</span></span>](recurringdatetransition.md) <br/> |<span data-ttu-id="f986b-132">Stellt einen Zeitzone Übergang, der auftritt, an einem angegebenen Tag des Jahres dar.</span><span class="sxs-lookup"><span data-stu-id="f986b-132">Represents a time zone transition that occurs on a specified day of the year.</span></span>  <br/> |
|[<span data-ttu-id="f986b-133">Übergang</span><span class="sxs-lookup"><span data-stu-id="f986b-133">Transition</span></span>](transition.md) <br/> |<span data-ttu-id="f986b-134">Stellt einen Zeitzone Übergang dar.</span><span class="sxs-lookup"><span data-stu-id="f986b-134">Represents a time zone transition.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f986b-135">Textwert</span><span class="sxs-lookup"><span data-stu-id="f986b-135">Text value</span></span>

<span data-ttu-id="f986b-136">Der Textwert ist eine Zeichenfolge, die gibt die eindeutige ID des [Zeitraums](period.md) oder [TransitionsGroup](transitionsgroup.md) , das das Ziel des Übergangs Zeitzone ist.</span><span class="sxs-lookup"><span data-stu-id="f986b-136">The text value is a string that specifies the unique identifier of the [Period](period.md) or [TransitionsGroup](transitionsgroup.md) that is the target of the time zone transition.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f986b-137">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f986b-137">Remarks</span></span>

<span data-ttu-id="f986b-138">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="f986b-138">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f986b-139">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="f986b-139">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f986b-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="f986b-140">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f986b-141">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f986b-141">Schema Name</span></span>  <br/> |<span data-ttu-id="f986b-142">Schematypen</span><span class="sxs-lookup"><span data-stu-id="f986b-142">Types schema</span></span>  <br/> |
|<span data-ttu-id="f986b-143">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f986b-143">Validation File</span></span>  <br/> |<span data-ttu-id="f986b-144">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f986b-144">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f986b-145">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="f986b-145">Can be Empty</span></span>  <br/> |<span data-ttu-id="f986b-146">False</span><span class="sxs-lookup"><span data-stu-id="f986b-146">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f986b-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f986b-147">See also</span></span>



- [<span data-ttu-id="f986b-148">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="f986b-148">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

