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
description: Das IsAssignmentEditable-Element stellt den Vorgangstyp dar.
ms.openlocfilehash: 5eb091b24e2c97f7aa6072044fed998b6c9c1651
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468054"
---
# <a name="isassignmenteditable"></a><span data-ttu-id="9706f-103">IsAssignmentEditable</span><span class="sxs-lookup"><span data-stu-id="9706f-103">IsAssignmentEditable</span></span>

<span data-ttu-id="9706f-104">Das **IsAssignmentEditable** -Element stellt den Vorgangstyp dar.</span><span class="sxs-lookup"><span data-stu-id="9706f-104">The **IsAssignmentEditable** element represents the task type.</span></span> 
  
```xml
<IsAssignmentEditable/>
```

 <span data-ttu-id="9706f-105">**Integer**</span><span class="sxs-lookup"><span data-stu-id="9706f-105">**integer**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9706f-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="9706f-106">Attributes and elements</span></span>

<span data-ttu-id="9706f-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="9706f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9706f-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="9706f-108">Attributes</span></span>

<span data-ttu-id="9706f-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="9706f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9706f-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9706f-110">Child elements</span></span>

<span data-ttu-id="9706f-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="9706f-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9706f-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9706f-112">Parent elements</span></span>

|<span data-ttu-id="9706f-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="9706f-113">**Element**</span></span>|<span data-ttu-id="9706f-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9706f-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9706f-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="9706f-115">Task</span></span>](task.md) <br/> |<span data-ttu-id="9706f-116">Stellt eine Aufgabe im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="9706f-116">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="9706f-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="9706f-117">Text value</span></span>

<span data-ttu-id="9706f-118">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="9706f-118">This property is read-only.</span></span> <span data-ttu-id="9706f-119">In der folgenden Tabelle sind die möglichen Werte aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="9706f-119">The following table lists the possible values.</span></span>
  
|<span data-ttu-id="9706f-120">**Wert**</span><span class="sxs-lookup"><span data-stu-id="9706f-120">**Value**</span></span>|<span data-ttu-id="9706f-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9706f-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9706f-122">0</span><span class="sxs-lookup"><span data-stu-id="9706f-122">0</span></span>  <br/> |<span data-ttu-id="9706f-123">Der Standardwert für alle Aufgabenelemente.</span><span class="sxs-lookup"><span data-stu-id="9706f-123">The default for all task items.</span></span>  <br/> |
|<span data-ttu-id="9706f-124">1 </span><span class="sxs-lookup"><span data-stu-id="9706f-124">1</span></span>  <br/> |<span data-ttu-id="9706f-125">Eine Aufgabenanforderung.</span><span class="sxs-lookup"><span data-stu-id="9706f-125">A task request.</span></span>  <br/> |
|<span data-ttu-id="9706f-126">2</span><span class="sxs-lookup"><span data-stu-id="9706f-126">2</span></span>  <br/> |<span data-ttu-id="9706f-127">Eine Aufgaben Akzeptanz durch einen Empfänger einer Aufgabenanfrage.</span><span class="sxs-lookup"><span data-stu-id="9706f-127">A task acceptance from a recipient of a task request.</span></span>  <br/> |
|<span data-ttu-id="9706f-128">3</span><span class="sxs-lookup"><span data-stu-id="9706f-128">3</span></span>  <br/> |<span data-ttu-id="9706f-129">Eine Aufgabe, die von einem Empfänger einer Aufgabenanfrage abnimmt.</span><span class="sxs-lookup"><span data-stu-id="9706f-129">A task declination from a recipient of a task request.</span></span>  <br/> |
|<span data-ttu-id="9706f-130">4 </span><span class="sxs-lookup"><span data-stu-id="9706f-130">4</span></span>  <br/> |<span data-ttu-id="9706f-131">Eine Aktualisierung einer vorherigen Aufgabenanforderung.</span><span class="sxs-lookup"><span data-stu-id="9706f-131">An update to a previous task request.</span></span>  <br/> |
|<span data-ttu-id="9706f-132">5 </span><span class="sxs-lookup"><span data-stu-id="9706f-132">5</span></span>  <br/> |<span data-ttu-id="9706f-133">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="9706f-133">Not used.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9706f-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9706f-134">Remarks</span></span>

<span data-ttu-id="9706f-135">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="9706f-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9706f-136">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="9706f-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9706f-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="9706f-137">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9706f-138">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="9706f-138">Schema Name</span></span>  <br/> |<span data-ttu-id="9706f-139">Schematypen</span><span class="sxs-lookup"><span data-stu-id="9706f-139">Types schema</span></span>  <br/> |
|<span data-ttu-id="9706f-140">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="9706f-140">Validation File</span></span>  <br/> |<span data-ttu-id="9706f-141">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9706f-141">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9706f-142">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="9706f-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="9706f-143">False</span><span class="sxs-lookup"><span data-stu-id="9706f-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9706f-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9706f-144">See also</span></span>



- [<span data-ttu-id="9706f-145">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="9706f-145">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

