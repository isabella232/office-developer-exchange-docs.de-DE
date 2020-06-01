---
title: Vorkommen (Zeitzonenübergang)
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
description: Das Vorkommen-Element stellt das Vorkommen des Wochentags in dem Monat dar, in dem der Zeitzonenübergang erfolgt.
ms.openlocfilehash: 846f6b22f43bcda07b9408d768d0845a5acfe668
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467977"
---
# <a name="occurrence-time-zone-transition"></a><span data-ttu-id="b9499-103">Vorkommen (Zeitzonenübergang)</span><span class="sxs-lookup"><span data-stu-id="b9499-103">Occurrence (Time Zone Transition)</span></span>

<span data-ttu-id="b9499-104">Das **vorkommen** -Element stellt das Vorkommen des Wochentags in dem Monat dar, in dem der Zeitzonenübergang erfolgt.</span><span class="sxs-lookup"><span data-stu-id="b9499-104">The **Occurrence** element represents the occurrence of the day of the week in the month that the time zone transition occurs.</span></span> 
  
```xml
<Occurrence/>
```

<span data-ttu-id="b9499-105">**int**</span><span class="sxs-lookup"><span data-stu-id="b9499-105">**int**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="b9499-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b9499-106">Attributes and elements</span></span>

<span data-ttu-id="b9499-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b9499-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b9499-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="b9499-108">Attributes</span></span>

<span data-ttu-id="b9499-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="b9499-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b9499-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b9499-110">Child elements</span></span>

<span data-ttu-id="b9499-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="b9499-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b9499-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b9499-112">Parent elements</span></span>

|<span data-ttu-id="b9499-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="b9499-113">**Element**</span></span>|<span data-ttu-id="b9499-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b9499-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b9499-115">RecurringDayTransition</span><span class="sxs-lookup"><span data-stu-id="b9499-115">RecurringDayTransition</span></span>](recurringdaytransition.md) <br/> |<span data-ttu-id="b9499-116">Stellt einen Zeitzonenübergang dar, der an demselben Tag jedes Jahr erfolgt.</span><span class="sxs-lookup"><span data-stu-id="b9499-116">Represents a time zone transition that occurs on the same day each year.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b9499-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="b9499-117">Text value</span></span>

<span data-ttu-id="b9499-118">Der Textwert ist eine ganze Zahl, die das Vorkommen des Wochentags in dem Monat darstellt, an dem der Zeitzonenübergang erfolgt.</span><span class="sxs-lookup"><span data-stu-id="b9499-118">The text value is an integer that represents the occurrence of the day of the week in the month that the time zone transition occurs.</span></span> <span data-ttu-id="b9499-119">In der folgenden Tabelle sind die möglichen Werte aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="b9499-119">The following table lists the possible values.</span></span>
  
|<span data-ttu-id="b9499-120">**Wert**</span><span class="sxs-lookup"><span data-stu-id="b9499-120">**Value**</span></span>|<span data-ttu-id="b9499-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b9499-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b9499-122">1</span><span class="sxs-lookup"><span data-stu-id="b9499-122">1</span></span>  <br/> |<span data-ttu-id="b9499-123">Das erste Vorkommen des angegebenen Wochentags vom Anfang des Monats.</span><span class="sxs-lookup"><span data-stu-id="b9499-123">The first occurrence of the specified day of the week from the beginning of the month.</span></span>  <br/> |
|<span data-ttu-id="b9499-124">2</span><span class="sxs-lookup"><span data-stu-id="b9499-124">2</span></span>  <br/> |<span data-ttu-id="b9499-125">Das zweite Vorkommen des angegebenen Wochentags vom Anfang des Monats.</span><span class="sxs-lookup"><span data-stu-id="b9499-125">The second occurrence of the specified day of the week from the beginning of the month.</span></span>  <br/> |
|<span data-ttu-id="b9499-126">3</span><span class="sxs-lookup"><span data-stu-id="b9499-126">3</span></span>  <br/> |<span data-ttu-id="b9499-127">Das dritte Vorkommen des angegebenen Wochentags vom Anfang des Monats.</span><span class="sxs-lookup"><span data-stu-id="b9499-127">The third occurrence of the specified day of the week from the beginning of the month.</span></span>  <br/> |
|<span data-ttu-id="b9499-128">4 </span><span class="sxs-lookup"><span data-stu-id="b9499-128">4</span></span>  <br/> |<span data-ttu-id="b9499-129">Das vierte Vorkommen des angegebenen Wochentags vom Anfang des Monats.</span><span class="sxs-lookup"><span data-stu-id="b9499-129">The fourth occurrence of the specified day of the week from the beginning of the month.</span></span>  <br/> |
|<span data-ttu-id="b9499-130">-1</span><span class="sxs-lookup"><span data-stu-id="b9499-130">-1</span></span>  <br/> |<span data-ttu-id="b9499-131">Das erste Vorkommen des angegebenen Wochentags am Ende des Monats.</span><span class="sxs-lookup"><span data-stu-id="b9499-131">The first occurrence of the specified day of the week from the end of the month.</span></span>  <br/> |
|<span data-ttu-id="b9499-132">-2</span><span class="sxs-lookup"><span data-stu-id="b9499-132">-2</span></span>  <br/> |<span data-ttu-id="b9499-133">Das zweite Vorkommen des angegebenen Wochentags am Ende des Monats.</span><span class="sxs-lookup"><span data-stu-id="b9499-133">The second occurrence of the specified day of the week from the end of the month.</span></span>  <br/> |
|<span data-ttu-id="b9499-134">-3</span><span class="sxs-lookup"><span data-stu-id="b9499-134">-3</span></span>  <br/> |<span data-ttu-id="b9499-135">Das dritte Vorkommen des angegebenen Wochentags am Ende des Monats.</span><span class="sxs-lookup"><span data-stu-id="b9499-135">The third occurrence of the specified day of the week from the end of the month.</span></span>  <br/> |
|<span data-ttu-id="b9499-136">-4</span><span class="sxs-lookup"><span data-stu-id="b9499-136">-4</span></span>  <br/> |<span data-ttu-id="b9499-137">Das vierte Vorkommen des angegebenen Wochentags am Ende des Monats.</span><span class="sxs-lookup"><span data-stu-id="b9499-137">The fourth occurrence of the specified day of the week from the end of the month.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b9499-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b9499-138">Remarks</span></span>

<span data-ttu-id="b9499-139">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Exchange Server ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="b9499-139">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b9499-140">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="b9499-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b9499-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="b9499-141">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b9499-142">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b9499-142">Schema Name</span></span>  <br/> |<span data-ttu-id="b9499-143">Schematypen</span><span class="sxs-lookup"><span data-stu-id="b9499-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="b9499-144">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b9499-144">Validation File</span></span>  <br/> |<span data-ttu-id="b9499-145">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b9499-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b9499-146">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="b9499-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="b9499-147">False</span><span class="sxs-lookup"><span data-stu-id="b9499-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b9499-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b9499-148">See also</span></span>

- [<span data-ttu-id="b9499-149">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="b9499-149">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

