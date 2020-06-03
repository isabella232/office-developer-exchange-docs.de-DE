---
title: Transitiongroup
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
description: Das transitiongroup-Element stellt ein Array von Zeit Zonen Übergängen dar.
ms.openlocfilehash: 9f08dec048d410dadab9580e7886b2499d943176
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467417"
---
# <a name="transitionsgroup"></a><span data-ttu-id="4119f-103">Transitiongroup</span><span class="sxs-lookup"><span data-stu-id="4119f-103">TransitionsGroup</span></span>

<span data-ttu-id="4119f-104">Das **transitiongroup** -Element stellt ein Array von Zeit Zonen Übergängen dar.</span><span class="sxs-lookup"><span data-stu-id="4119f-104">The **TransitionsGroup** element represents an array of time zone transitions.</span></span> 
  
```xml
<TransitionsGroup Id="">
   <AbsoluteDateTransition/>
   <RecurringDayTransition/>
   <RecurringDateTransition/>
</TransitionsGroup>
```

 <span data-ttu-id="4119f-105">**ArrayOfTransitionsType**</span><span class="sxs-lookup"><span data-stu-id="4119f-105">**ArrayOfTransitionsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4119f-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="4119f-106">Attributes and elements</span></span>

<span data-ttu-id="4119f-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="4119f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4119f-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="4119f-108">Attributes</span></span>

|<span data-ttu-id="4119f-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="4119f-109">**Attribute**</span></span>|<span data-ttu-id="4119f-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4119f-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4119f-111">Id</span><span class="sxs-lookup"><span data-stu-id="4119f-111">Id</span></span>  <br/> |<span data-ttu-id="4119f-112">Ein String-Wert, der den eindeutigen Bezeichner der Transitions-Gruppe darstellt.</span><span class="sxs-lookup"><span data-stu-id="4119f-112">A string value that represents the unique identifier of the transitions group.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4119f-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4119f-113">Child elements</span></span>

|<span data-ttu-id="4119f-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="4119f-114">**Element**</span></span>|<span data-ttu-id="4119f-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4119f-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4119f-116">AbsoluteDateTransition</span><span class="sxs-lookup"><span data-stu-id="4119f-116">AbsoluteDateTransition</span></span>](absolutedatetransition.md) <br/> |<span data-ttu-id="4119f-117">Stellt einen Zeitzonenübergang dar, der zu einem bestimmten Datum und zu einem bestimmten Zeitpunkt erfolgt.</span><span class="sxs-lookup"><span data-stu-id="4119f-117">Represents a time zone transition that occurs on a specific date and at a specific time.</span></span>  <br/> |
|[<span data-ttu-id="4119f-118">RecurringDayTransition</span><span class="sxs-lookup"><span data-stu-id="4119f-118">RecurringDayTransition</span></span>](recurringdaytransition.md) <br/> |<span data-ttu-id="4119f-119">Stellt einen Zeitzonenübergang dar, der an demselben Tag jedes Jahr erfolgt.</span><span class="sxs-lookup"><span data-stu-id="4119f-119">Represents a time zone transition that occurs on the same day each year.</span></span>  <br/> |
|[<span data-ttu-id="4119f-120">RecurringDateTransition</span><span class="sxs-lookup"><span data-stu-id="4119f-120">RecurringDateTransition</span></span>](recurringdatetransition.md) <br/> |<span data-ttu-id="4119f-121">Stellt einen Zeitzonenübergang dar, der an einem angegebenen Tag des Jahres erfolgt.</span><span class="sxs-lookup"><span data-stu-id="4119f-121">Represents a time zone transition that occurs on a specified day of the year.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4119f-122">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4119f-122">Parent elements</span></span>

|<span data-ttu-id="4119f-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="4119f-123">**Element**</span></span>|<span data-ttu-id="4119f-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4119f-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4119f-125">TransitionsGroups</span><span class="sxs-lookup"><span data-stu-id="4119f-125">TransitionsGroups</span></span>](transitionsgroups.md) <br/> |<span data-ttu-id="4119f-126">Stellt ein Array von Zeit Zonen Übergangs Gruppen dar.</span><span class="sxs-lookup"><span data-stu-id="4119f-126">Represents an array of time zone transition groups.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4119f-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4119f-127">Remarks</span></span>

<span data-ttu-id="4119f-128">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Exchange Server ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="4119f-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4119f-129">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="4119f-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4119f-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="4119f-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4119f-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="4119f-131">Schema Name</span></span>  <br/> |<span data-ttu-id="4119f-132">Schematypen</span><span class="sxs-lookup"><span data-stu-id="4119f-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="4119f-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="4119f-133">Validation File</span></span>  <br/> |<span data-ttu-id="4119f-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4119f-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4119f-135">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="4119f-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="4119f-136">False</span><span class="sxs-lookup"><span data-stu-id="4119f-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4119f-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4119f-137">See also</span></span>



- [<span data-ttu-id="4119f-138">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="4119f-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

