---
title: IsAssignmentEditable
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsAssignmentEditable
api_type:
- schema
ms.assetid: 0ddf9181-f65e-4ad6-ad69-7b074ea0f2e7
description: Das Element IsAssignmentEditable stellt den Aufgabentyp.
ms.openlocfilehash: 91922c4d6abd4d88ac9e36dd3d4c0224fc1ee716
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19829992"
---
# <a name="isassignmenteditable"></a><span data-ttu-id="6742c-103">IsAssignmentEditable</span><span class="sxs-lookup"><span data-stu-id="6742c-103">IsAssignmentEditable</span></span>

<span data-ttu-id="6742c-104">Das Element **IsAssignmentEditable** stellt den Aufgabentyp.</span><span class="sxs-lookup"><span data-stu-id="6742c-104">The **IsAssignmentEditable** element represents the task type.</span></span> 
  
```xml
<IsAssignmentEditable/>
```

 <span data-ttu-id="6742c-105">**ganze Zahl**</span><span class="sxs-lookup"><span data-stu-id="6742c-105">**integer**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6742c-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="6742c-106">Attributes and elements</span></span>

<span data-ttu-id="6742c-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="6742c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6742c-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="6742c-108">Attributes</span></span>

<span data-ttu-id="6742c-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="6742c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6742c-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6742c-110">Child elements</span></span>

<span data-ttu-id="6742c-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="6742c-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6742c-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6742c-112">Parent elements</span></span>

|<span data-ttu-id="6742c-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="6742c-113">**Element**</span></span>|<span data-ttu-id="6742c-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6742c-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6742c-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="6742c-115">Task</span></span>](task.md) <br/> |<span data-ttu-id="6742c-116">Stellt eine Aufgabe im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="6742c-116">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6742c-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="6742c-117">Text value</span></span>

<span data-ttu-id="6742c-118">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="6742c-118">This property is read-only.</span></span> <span data-ttu-id="6742c-119">In der folgenden Tabelle sind die möglichen Werte aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="6742c-119">The following table lists the possible values.</span></span>
  
|<span data-ttu-id="6742c-120">**Wert**</span><span class="sxs-lookup"><span data-stu-id="6742c-120">**Value**</span></span>|<span data-ttu-id="6742c-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6742c-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6742c-122">0</span><span class="sxs-lookup"><span data-stu-id="6742c-122">0</span></span>  <br/> |<span data-ttu-id="6742c-123">Die Standardeinstellung für alle Aufgabenelemente.</span><span class="sxs-lookup"><span data-stu-id="6742c-123">The default for all task items.</span></span>  <br/> |
|<span data-ttu-id="6742c-124">1</span><span class="sxs-lookup"><span data-stu-id="6742c-124">1</span></span>  <br/> |<span data-ttu-id="6742c-125">Eine Aufgabenanfrage.</span><span class="sxs-lookup"><span data-stu-id="6742c-125">A task request.</span></span>  <br/> |
|<span data-ttu-id="6742c-126">2</span><span class="sxs-lookup"><span data-stu-id="6742c-126">2</span></span>  <br/> |<span data-ttu-id="6742c-127">Die Annahme einer Aufgabe aus einem Empfänger eine Aufgabenanfrage.</span><span class="sxs-lookup"><span data-stu-id="6742c-127">A task acceptance from a recipient of a task request.</span></span>  <br/> |
|<span data-ttu-id="6742c-128">3</span><span class="sxs-lookup"><span data-stu-id="6742c-128">3</span></span>  <br/> |<span data-ttu-id="6742c-129">Eine Aufgabe Ablehnung von einem Empfänger eine Aufgabenanfrage.</span><span class="sxs-lookup"><span data-stu-id="6742c-129">A task declination from a recipient of a task request.</span></span>  <br/> |
|<span data-ttu-id="6742c-130">4</span><span class="sxs-lookup"><span data-stu-id="6742c-130">4</span></span>  <br/> |<span data-ttu-id="6742c-131">Ein Update auf eine vorherige Aufgabenanfrage.</span><span class="sxs-lookup"><span data-stu-id="6742c-131">An update to a previous task request.</span></span>  <br/> |
|<span data-ttu-id="6742c-132">5</span><span class="sxs-lookup"><span data-stu-id="6742c-132">5</span></span>  <br/> |<span data-ttu-id="6742c-133">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="6742c-133">Not used.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6742c-134">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6742c-134">Remarks</span></span>

<span data-ttu-id="6742c-135">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="6742c-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6742c-136">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="6742c-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6742c-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="6742c-137">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6742c-138">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="6742c-138">Schema Name</span></span>  <br/> |<span data-ttu-id="6742c-139">Schematypen</span><span class="sxs-lookup"><span data-stu-id="6742c-139">Types schema</span></span>  <br/> |
|<span data-ttu-id="6742c-140">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="6742c-140">Validation File</span></span>  <br/> |<span data-ttu-id="6742c-141">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6742c-141">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6742c-142">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="6742c-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="6742c-143">False</span><span class="sxs-lookup"><span data-stu-id="6742c-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6742c-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6742c-144">See also</span></span>



- [<span data-ttu-id="6742c-145">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="6742c-145">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

