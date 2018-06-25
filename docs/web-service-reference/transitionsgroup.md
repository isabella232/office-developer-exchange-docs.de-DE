---
title: TransitionsGroup
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- TransitionsGroup
api_type:
- schema
ms.assetid: 19d56080-546a-4d53-929e-363d56186759
description: Das TransitionsGroup-Element stellt ein Array von Zeitzone Übergänge.
ms.openlocfilehash: e5991ad7f73a1694e0d4abadd8d252acc04970e5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839262"
---
# <a name="transitionsgroup"></a><span data-ttu-id="e0577-103">TransitionsGroup</span><span class="sxs-lookup"><span data-stu-id="e0577-103">TransitionsGroup</span></span>

<span data-ttu-id="e0577-104">Das **TransitionsGroup** -Element stellt ein Array von Zeitzone Übergänge.</span><span class="sxs-lookup"><span data-stu-id="e0577-104">The **TransitionsGroup** element represents an array of time zone transitions.</span></span> 
  
```xml
<TransitionsGroup Id="">
   <AbsoluteDateTransition/>
   <RecurringDayTransition/>
   <RecurringDateTransition/>
</TransitionsGroup>
```

 <span data-ttu-id="e0577-105">**ArrayOfTransitionsType**</span><span class="sxs-lookup"><span data-stu-id="e0577-105">**ArrayOfTransitionsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e0577-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e0577-106">Attributes and elements</span></span>

<span data-ttu-id="e0577-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e0577-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e0577-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="e0577-108">Attributes</span></span>

|<span data-ttu-id="e0577-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="e0577-109">**Attribute**</span></span>|<span data-ttu-id="e0577-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e0577-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e0577-111">Id</span><span class="sxs-lookup"><span data-stu-id="e0577-111">Id</span></span>  <br/> |<span data-ttu-id="e0577-112">Ein String-Wert, der den eindeutigen Bezeichner der Übergänge Gruppe darstellt.</span><span class="sxs-lookup"><span data-stu-id="e0577-112">A string value that represents the unique identifier of the transitions group.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e0577-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e0577-113">Child elements</span></span>

|<span data-ttu-id="e0577-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="e0577-114">**Element**</span></span>|<span data-ttu-id="e0577-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e0577-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e0577-116">AbsoluteDateTransition</span><span class="sxs-lookup"><span data-stu-id="e0577-116">AbsoluteDateTransition</span></span>](absolutedatetransition.md) <br/> |<span data-ttu-id="e0577-117">Stellt einen Zeitzone Übergang, die einem bestimmten Datum und zu einem bestimmten Zeitpunkt dar.</span><span class="sxs-lookup"><span data-stu-id="e0577-117">Represents a time zone transition that occurs on a specific date and at a specific time.</span></span>  <br/> |
|[<span data-ttu-id="e0577-118">RecurringDayTransition</span><span class="sxs-lookup"><span data-stu-id="e0577-118">RecurringDayTransition</span></span>](recurringdaytransition.md) <br/> |<span data-ttu-id="e0577-119">Stellt einen Zeitzone Übergang dar, bei dem gleichen Tag pro Jahr auftritt.</span><span class="sxs-lookup"><span data-stu-id="e0577-119">Represents a time zone transition that occurs on the same day each year.</span></span>  <br/> |
|[<span data-ttu-id="e0577-120">RecurringDateTransition</span><span class="sxs-lookup"><span data-stu-id="e0577-120">RecurringDateTransition</span></span>](recurringdatetransition.md) <br/> |<span data-ttu-id="e0577-121">Stellt einen Zeitzone Übergang, der auftritt, an einem angegebenen Tag des Jahres dar.</span><span class="sxs-lookup"><span data-stu-id="e0577-121">Represents a time zone transition that occurs on a specified day of the year.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e0577-122">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e0577-122">Parent elements</span></span>

|<span data-ttu-id="e0577-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="e0577-123">**Element**</span></span>|<span data-ttu-id="e0577-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e0577-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e0577-125">TransitionsGroups</span><span class="sxs-lookup"><span data-stu-id="e0577-125">TransitionsGroups</span></span>](transitionsgroups.md) <br/> |<span data-ttu-id="e0577-126">Stellt ein Array von Zeitzone Übergang Gruppen.</span><span class="sxs-lookup"><span data-stu-id="e0577-126">Represents an array of time zone transition groups.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e0577-127">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e0577-127">Remarks</span></span>

<span data-ttu-id="e0577-128">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="e0577-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e0577-129">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="e0577-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e0577-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="e0577-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e0577-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e0577-131">Schema Name</span></span>  <br/> |<span data-ttu-id="e0577-132">Schematypen</span><span class="sxs-lookup"><span data-stu-id="e0577-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="e0577-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e0577-133">Validation File</span></span>  <br/> |<span data-ttu-id="e0577-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e0577-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e0577-135">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="e0577-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="e0577-136">False</span><span class="sxs-lookup"><span data-stu-id="e0577-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e0577-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e0577-137">See also</span></span>



- [<span data-ttu-id="e0577-138">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="e0577-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

