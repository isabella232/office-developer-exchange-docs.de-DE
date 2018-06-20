---
title: Vorkommen (Übergang Zeitzone)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Occurrence
api_type:
- schema
ms.assetid: 5c1142b1-c51f-42e1-bbb2-57e00cad0fdb
description: Das Vorkommen-Element darstellt, das Vorkommen des Tags der Woche des Monats, der der Übergang zur Zeitzone auftritt.
ms.openlocfilehash: bc5160480cc6881bb9d724aa61323f5717d1f2fa
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830636"
---
# <a name="occurrence-time-zone-transition"></a><span data-ttu-id="6222a-103">Vorkommen (Übergang Zeitzone)</span><span class="sxs-lookup"><span data-stu-id="6222a-103">Occurrence (Time Zone Transition)</span></span>

<span data-ttu-id="6222a-104">Das **Vorkommen** -Element darstellt, das Vorkommen des Tags der Woche des Monats, der der Übergang zur Zeitzone auftritt.</span><span class="sxs-lookup"><span data-stu-id="6222a-104">The **Occurrence** element represents the occurrence of the day of the week in the month that the time zone transition occurs.</span></span> 
  
```xml
<Occurrence/>
```

<span data-ttu-id="6222a-105">**int**</span><span class="sxs-lookup"><span data-stu-id="6222a-105">**int**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="6222a-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="6222a-106">Attributes and elements</span></span>

<span data-ttu-id="6222a-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="6222a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6222a-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="6222a-108">Attributes</span></span>

<span data-ttu-id="6222a-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="6222a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6222a-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6222a-110">Child elements</span></span>

<span data-ttu-id="6222a-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="6222a-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6222a-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6222a-112">Parent elements</span></span>

|<span data-ttu-id="6222a-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="6222a-113">**Element**</span></span>|<span data-ttu-id="6222a-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6222a-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6222a-115">RecurringDayTransition</span><span class="sxs-lookup"><span data-stu-id="6222a-115">RecurringDayTransition</span></span>](recurringdaytransition.md) <br/> |<span data-ttu-id="6222a-116">Stellt einen Zeitzone Übergang dar, bei dem gleichen Tag pro Jahr auftritt.</span><span class="sxs-lookup"><span data-stu-id="6222a-116">Represents a time zone transition that occurs on the same day each year.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6222a-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="6222a-117">Text value</span></span>

<span data-ttu-id="6222a-118">Der Textwert ist eine ganze Zahl, die das Vorkommen des Tags der Woche im Monat darstellt, das auftritt, der Übergang zur Zeitzone.</span><span class="sxs-lookup"><span data-stu-id="6222a-118">The text value is an integer that represents the occurrence of the day of the week in the month that the time zone transition occurs.</span></span> <span data-ttu-id="6222a-119">In der folgenden Tabelle sind die möglichen Werte aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="6222a-119">The following table lists the possible values.</span></span>
  
|<span data-ttu-id="6222a-120">**Wert**</span><span class="sxs-lookup"><span data-stu-id="6222a-120">**Value**</span></span>|<span data-ttu-id="6222a-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6222a-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6222a-122">1</span><span class="sxs-lookup"><span data-stu-id="6222a-122">1</span></span>  <br/> |<span data-ttu-id="6222a-123">Das erste Auftreten des angegebenen Tags der Woche vom Beginn des Monats.</span><span class="sxs-lookup"><span data-stu-id="6222a-123">The first occurrence of the specified day of the week from the beginning of the month.</span></span>  <br/> |
|<span data-ttu-id="6222a-124">2</span><span class="sxs-lookup"><span data-stu-id="6222a-124">2</span></span>  <br/> |<span data-ttu-id="6222a-125">Das zweite Vorkommen des angegebenen Tags der Woche vom Beginn des Monats.</span><span class="sxs-lookup"><span data-stu-id="6222a-125">The second occurrence of the specified day of the week from the beginning of the month.</span></span>  <br/> |
|<span data-ttu-id="6222a-126">3</span><span class="sxs-lookup"><span data-stu-id="6222a-126">3</span></span>  <br/> |<span data-ttu-id="6222a-127">Das dritte Vorkommen des angegebenen Tags der Woche vom Beginn des Monats.</span><span class="sxs-lookup"><span data-stu-id="6222a-127">The third occurrence of the specified day of the week from the beginning of the month.</span></span>  <br/> |
|<span data-ttu-id="6222a-128">4</span><span class="sxs-lookup"><span data-stu-id="6222a-128">4</span></span>  <br/> |<span data-ttu-id="6222a-129">Das vierte der angegebene Tag der Woche vom Beginn des Monats auftreten.</span><span class="sxs-lookup"><span data-stu-id="6222a-129">The fourth occurrence of the specified day of the week from the beginning of the month.</span></span>  <br/> |
|<span data-ttu-id="6222a-130">-1</span><span class="sxs-lookup"><span data-stu-id="6222a-130">-1</span></span>  <br/> |<span data-ttu-id="6222a-131">Das erste Auftreten des angegebenen Tags der Woche vom Ende des Monats.</span><span class="sxs-lookup"><span data-stu-id="6222a-131">The first occurrence of the specified day of the week from the end of the month.</span></span>  <br/> |
|<span data-ttu-id="6222a-132">-2</span><span class="sxs-lookup"><span data-stu-id="6222a-132">-2</span></span>  <br/> |<span data-ttu-id="6222a-133">Das zweite Vorkommen des angegebenen Tags der Woche vom Ende des Monats.</span><span class="sxs-lookup"><span data-stu-id="6222a-133">The second occurrence of the specified day of the week from the end of the month.</span></span>  <br/> |
|<span data-ttu-id="6222a-134">-3</span><span class="sxs-lookup"><span data-stu-id="6222a-134">-3</span></span>  <br/> |<span data-ttu-id="6222a-135">Das dritte Vorkommen des angegebenen Tags der Woche vom Ende des Monats.</span><span class="sxs-lookup"><span data-stu-id="6222a-135">The third occurrence of the specified day of the week from the end of the month.</span></span>  <br/> |
|<span data-ttu-id="6222a-136">-4</span><span class="sxs-lookup"><span data-stu-id="6222a-136">-4</span></span>  <br/> |<span data-ttu-id="6222a-137">Das vierte der angegebene Tag der Woche vom Ende des Monats auftreten.</span><span class="sxs-lookup"><span data-stu-id="6222a-137">The fourth occurrence of the specified day of the week from the end of the month.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6222a-138">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6222a-138">Remarks</span></span>

<span data-ttu-id="6222a-139">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="6222a-139">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6222a-140">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="6222a-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6222a-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="6222a-141">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6222a-142">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="6222a-142">Schema Name</span></span>  <br/> |<span data-ttu-id="6222a-143">Schematypen</span><span class="sxs-lookup"><span data-stu-id="6222a-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="6222a-144">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="6222a-144">Validation File</span></span>  <br/> |<span data-ttu-id="6222a-145">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6222a-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6222a-146">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="6222a-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="6222a-147">False</span><span class="sxs-lookup"><span data-stu-id="6222a-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6222a-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6222a-148">See also</span></span>

- [<span data-ttu-id="6222a-149">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="6222a-149">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

