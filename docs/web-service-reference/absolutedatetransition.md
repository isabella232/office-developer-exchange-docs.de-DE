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
description: Das AbsoluteDateTransition-Element stellt einen Zeitzonenübergang dar, der zu einem bestimmten Datum und zu einem bestimmten Zeitpunkt erfolgt.
ms.openlocfilehash: 514464f69c3be5496aedbe184848ef9ed9f296b9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461723"
---
# <a name="absolutedatetransition"></a><span data-ttu-id="a7c7a-103">AbsoluteDateTransition</span><span class="sxs-lookup"><span data-stu-id="a7c7a-103">AbsoluteDateTransition</span></span>

<span data-ttu-id="a7c7a-104">Das **AbsoluteDateTransition** -Element stellt einen Zeitzonenübergang dar, der zu einem bestimmten Datum und zu einem bestimmten Zeitpunkt erfolgt.</span><span class="sxs-lookup"><span data-stu-id="a7c7a-104">The **AbsoluteDateTransition** element represents a time zone transition that occurs on a specific date and at a specific time.</span></span> 
  
```xml
<AbsoluteDateTransition>
   <To/>
   <DateTime/>
</AbsoluteDateTransition>
```

<span data-ttu-id="a7c7a-105">**AbsoluteDateTransitionType**</span><span class="sxs-lookup"><span data-stu-id="a7c7a-105">**AbsoluteDateTransitionType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="a7c7a-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a7c7a-106">Attributes and elements</span></span>

<span data-ttu-id="a7c7a-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a7c7a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a7c7a-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="a7c7a-108">Attributes</span></span>

<span data-ttu-id="a7c7a-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="a7c7a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a7c7a-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a7c7a-110">Child elements</span></span>

|<span data-ttu-id="a7c7a-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="a7c7a-111">**Element**</span></span>|<span data-ttu-id="a7c7a-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a7c7a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a7c7a-113">To</span><span class="sxs-lookup"><span data-stu-id="a7c7a-113">To</span></span>](to.md) <br/> |<span data-ttu-id="a7c7a-114">Gibt den [Zeitraum](period.md) oder die [Transitions](transitionsgroup.md) an, der das Ziel des Zeit Zonen Übergangs darstellt.</span><span class="sxs-lookup"><span data-stu-id="a7c7a-114">Specifies the [Period](period.md) or [TransitionsGroup](transitionsgroup.md) that is the target of the time zone transition.</span></span>  <br/> |
|[<span data-ttu-id="a7c7a-115">DateTime</span><span class="sxs-lookup"><span data-stu-id="a7c7a-115">DateTime</span></span>](datetime.md) <br/> |<span data-ttu-id="a7c7a-116">Stellt das Datum und die Uhrzeit dar, zu der der Zeitzonenübergang erfolgt.</span><span class="sxs-lookup"><span data-stu-id="a7c7a-116">Represents the date and time at which the time zone transition occurs.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a7c7a-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a7c7a-117">Parent elements</span></span>

|<span data-ttu-id="a7c7a-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="a7c7a-118">**Element**</span></span>|<span data-ttu-id="a7c7a-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a7c7a-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a7c7a-120">Übergänge</span><span class="sxs-lookup"><span data-stu-id="a7c7a-120">Transitions</span></span>](transitions.md) <br/> |<span data-ttu-id="a7c7a-121">Stellt eine Auflistung von Zeit Zonen Übergängen dar.</span><span class="sxs-lookup"><span data-stu-id="a7c7a-121">Represents a collection of time zone transitions.</span></span>  <br/> |
|[<span data-ttu-id="a7c7a-122">Transitiongroup</span><span class="sxs-lookup"><span data-stu-id="a7c7a-122">TransitionsGroup</span></span>](transitionsgroup.md) <br/> |<span data-ttu-id="a7c7a-123">Stellt eine Auflistung von Zeit Zonen Übergängen dar.</span><span class="sxs-lookup"><span data-stu-id="a7c7a-123">Represents a collection of time zone transitions.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a7c7a-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a7c7a-124">Remarks</span></span>

<span data-ttu-id="a7c7a-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="a7c7a-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a7c7a-126">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="a7c7a-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a7c7a-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="a7c7a-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a7c7a-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a7c7a-128">Schema Name</span></span>  <br/> |<span data-ttu-id="a7c7a-129">Schematypen</span><span class="sxs-lookup"><span data-stu-id="a7c7a-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="a7c7a-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a7c7a-130">Validation File</span></span>  <br/> |<span data-ttu-id="a7c7a-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a7c7a-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a7c7a-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="a7c7a-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="a7c7a-133">False</span><span class="sxs-lookup"><span data-stu-id="a7c7a-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a7c7a-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a7c7a-134">See also</span></span>

- [<span data-ttu-id="a7c7a-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="a7c7a-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

