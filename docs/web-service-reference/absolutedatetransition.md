---
title: AbsoluteDateTransition
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AbsoluteDateTransition
api_type:
- schema
ms.assetid: 8f5731eb-bed0-45bf-ba89-4aaf20c34a39
description: Das AbsoluteDateTransition-Element stellt einen Zeitzone Übergang, die einem bestimmten Datum und zu einem bestimmten Zeitpunkt dar.
ms.openlocfilehash: 1e9e5f3f2269814a82b827efe46c71a172e21348
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757208"
---
# <a name="absolutedatetransition"></a><span data-ttu-id="d4ae8-103">AbsoluteDateTransition</span><span class="sxs-lookup"><span data-stu-id="d4ae8-103">AbsoluteDateTransition</span></span>

<span data-ttu-id="d4ae8-104">Das **AbsoluteDateTransition** -Element stellt einen Zeitzone Übergang, die einem bestimmten Datum und zu einem bestimmten Zeitpunkt dar.</span><span class="sxs-lookup"><span data-stu-id="d4ae8-104">The **AbsoluteDateTransition** element represents a time zone transition that occurs on a specific date and at a specific time.</span></span> 
  
```xml
<AbsoluteDateTransition>
   <To/>
   <DateTime/>
</AbsoluteDateTransition>
```

<span data-ttu-id="d4ae8-105">**AbsoluteDateTransitionType**</span><span class="sxs-lookup"><span data-stu-id="d4ae8-105">**AbsoluteDateTransitionType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="d4ae8-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d4ae8-106">Attributes and elements</span></span>

<span data-ttu-id="d4ae8-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d4ae8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d4ae8-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d4ae8-108">Attributes</span></span>

<span data-ttu-id="d4ae8-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="d4ae8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d4ae8-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d4ae8-110">Child elements</span></span>

|<span data-ttu-id="d4ae8-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="d4ae8-111">**Element**</span></span>|<span data-ttu-id="d4ae8-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d4ae8-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d4ae8-113">To</span><span class="sxs-lookup"><span data-stu-id="d4ae8-113">To</span></span>](to.md) <br/> |<span data-ttu-id="d4ae8-114">Gibt den [Zeitraum](period.md) oder [TransitionsGroup](transitionsgroup.md) , das das Ziel des Übergangs Zeitzone ist.</span><span class="sxs-lookup"><span data-stu-id="d4ae8-114">Specifies the [Period](period.md) or [TransitionsGroup](transitionsgroup.md) that is the target of the time zone transition.</span></span>  <br/> |
|[<span data-ttu-id="d4ae8-115">DateTime</span><span class="sxs-lookup"><span data-stu-id="d4ae8-115">DateTime</span></span>](datetime.md) <br/> |<span data-ttu-id="d4ae8-116">Stellt das Datum und Uhrzeit an der erfolgt der Übergang zur Zeitzone.</span><span class="sxs-lookup"><span data-stu-id="d4ae8-116">Represents the date and time at which the time zone transition occurs.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d4ae8-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d4ae8-117">Parent elements</span></span>

|<span data-ttu-id="d4ae8-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="d4ae8-118">**Element**</span></span>|<span data-ttu-id="d4ae8-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d4ae8-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d4ae8-120">Übergänge</span><span class="sxs-lookup"><span data-stu-id="d4ae8-120">Transitions</span></span>](transitions.md) <br/> |<span data-ttu-id="d4ae8-121">Stellt eine Auflistung der Zeitzone Übergänge.</span><span class="sxs-lookup"><span data-stu-id="d4ae8-121">Represents a collection of time zone transitions.</span></span>  <br/> |
|[<span data-ttu-id="d4ae8-122">TransitionsGroup</span><span class="sxs-lookup"><span data-stu-id="d4ae8-122">TransitionsGroup</span></span>](transitionsgroup.md) <br/> |<span data-ttu-id="d4ae8-123">Stellt eine Auflistung der Zeitzone Übergänge.</span><span class="sxs-lookup"><span data-stu-id="d4ae8-123">Represents a collection of time zone transitions.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d4ae8-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d4ae8-124">Remarks</span></span>

<span data-ttu-id="d4ae8-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="d4ae8-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d4ae8-126">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="d4ae8-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d4ae8-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="d4ae8-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d4ae8-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d4ae8-128">Schema Name</span></span>  <br/> |<span data-ttu-id="d4ae8-129">Schematypen</span><span class="sxs-lookup"><span data-stu-id="d4ae8-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="d4ae8-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d4ae8-130">Validation File</span></span>  <br/> |<span data-ttu-id="d4ae8-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d4ae8-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d4ae8-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d4ae8-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="d4ae8-133">False</span><span class="sxs-lookup"><span data-stu-id="d4ae8-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d4ae8-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d4ae8-134">See also</span></span>

- [<span data-ttu-id="d4ae8-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="d4ae8-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

