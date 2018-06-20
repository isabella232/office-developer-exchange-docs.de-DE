---
title: MergedFreeBusyIntervalInMinutes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MergedFreeBusyIntervalInMinutes
api_type:
- schema
ms.assetid: 481cdbc6-d5aa-49fa-a3fa-9d119d3dca99
description: Das Element MergedFreeBusyIntervalInMinutes stellt den Zeitunterschied zwischen zwei aufeinanderfolgenden Slots in der Ansicht FreeBusyMerged.
ms.openlocfilehash: 99c8c69424a0a9d9594005fdf6b2ceba53e6288a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830451"
---
# <a name="mergedfreebusyintervalinminutes"></a><span data-ttu-id="abedb-103">MergedFreeBusyIntervalInMinutes</span><span class="sxs-lookup"><span data-stu-id="abedb-103">MergedFreeBusyIntervalInMinutes</span></span>

<span data-ttu-id="abedb-104">Das Element **MergedFreeBusyIntervalInMinutes** stellt den Zeitunterschied zwischen zwei aufeinanderfolgenden Slots in der Ansicht **FreeBusyMerged** .</span><span class="sxs-lookup"><span data-stu-id="abedb-104">The **MergedFreeBusyIntervalInMinutes** element represents the time difference between two successive slots in the **FreeBusyMerged** view.</span></span> 
  
[<span data-ttu-id="abedb-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="abedb-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
[<span data-ttu-id="abedb-106">FreeBusyViewOptions</span><span class="sxs-lookup"><span data-stu-id="abedb-106">FreeBusyViewOptions</span></span>](freebusyviewoptions.md)
  
[<span data-ttu-id="abedb-107">MergedFreeBusyIntervalInMinutes</span><span class="sxs-lookup"><span data-stu-id="abedb-107">MergedFreeBusyIntervalInMinutes</span></span>](mergedfreebusyintervalinminutes.md)
  
```xml
<MergedFreeBusyIntervalInMinutes>...</MergedFreeBusyIntervalInMinutes>
```

 <span data-ttu-id="abedb-108">**int**</span><span class="sxs-lookup"><span data-stu-id="abedb-108">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="abedb-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="abedb-109">Attributes and elements</span></span>

<span data-ttu-id="abedb-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="abedb-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="abedb-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="abedb-111">Attributes</span></span>

<span data-ttu-id="abedb-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="abedb-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="abedb-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="abedb-113">Child elements</span></span>

<span data-ttu-id="abedb-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="abedb-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="abedb-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="abedb-115">Parent elements</span></span>

|<span data-ttu-id="abedb-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="abedb-116">**Element**</span></span>|<span data-ttu-id="abedb-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="abedb-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="abedb-118">FreeBusyViewOptions</span><span class="sxs-lookup"><span data-stu-id="abedb-118">FreeBusyViewOptions</span></span>](freebusyviewoptions.md) <br/> |<span data-ttu-id="abedb-119">Gibt den Typ des Frei/Gebucht-Informationen in der Antwort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="abedb-119">Specifies the type of free/busy information returned in the response.</span></span>  <br/> <span data-ttu-id="abedb-120">Es folgt der XPath-Ausdruck für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="abedb-120">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/FreeBusyViewOptions` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="abedb-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="abedb-121">Text value</span></span>

<span data-ttu-id="abedb-122">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="abedb-122">A text value is required.</span></span> <span data-ttu-id="abedb-123">Der Textwert darstellt Zeit in Minuten.</span><span class="sxs-lookup"><span data-stu-id="abedb-123">The text value represents time in minutes.</span></span> <span data-ttu-id="abedb-124">Der Standardwert ist 30 Minuten.</span><span class="sxs-lookup"><span data-stu-id="abedb-124">The default value is 30 minutes.</span></span> <span data-ttu-id="abedb-125">6 Minuten ist das kürzeste Intervall und einen Tag (1.440 Minuten) ist das maximale Intervall für dieses Element.</span><span class="sxs-lookup"><span data-stu-id="abedb-125">Six minutes is the minimum interval and one day (1440 minutes) is the maximum interval for this element.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="abedb-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="abedb-126">Remarks</span></span>

<span data-ttu-id="abedb-127">Dieser Wert wird nur dann, wenn das Element [RequestedView](requestedview.md) **MergedOnly**, **FreeBusyMerged**oder **DetailedMerge**gleich ist.</span><span class="sxs-lookup"><span data-stu-id="abedb-127">This value is used only if the [RequestedView](requestedview.md) element is equal to **MergedOnly**, **FreeBusyMerged**, or **DetailedMerge**.</span></span> <span data-ttu-id="abedb-128">Dies ist ein Integer-Datentyp.</span><span class="sxs-lookup"><span data-stu-id="abedb-128">This is an integer data type.</span></span> <span data-ttu-id="abedb-129">Der Stream, der die durch dieses Element definierten Intervallen enthält, wird im [MergedFreeBusy](mergedfreebusy.md) -Element zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="abedb-129">The stream that contains the intervals defined by this element is returned in the [MergedFreeBusy](mergedfreebusy.md) element.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="abedb-130">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="abedb-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="abedb-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="abedb-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="abedb-132">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="abedb-132">Schema Name</span></span>  <br/> |<span data-ttu-id="abedb-133">Schematypen</span><span class="sxs-lookup"><span data-stu-id="abedb-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="abedb-134">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="abedb-134">Validation File</span></span>  <br/> |<span data-ttu-id="abedb-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="abedb-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="abedb-136">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="abedb-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="abedb-137">False</span><span class="sxs-lookup"><span data-stu-id="abedb-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="abedb-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="abedb-138">See also</span></span>



[<span data-ttu-id="abedb-139">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="abedb-139">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="abedb-140">GetUserOofSettings-Vorgang</span><span class="sxs-lookup"><span data-stu-id="abedb-140">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md)


[<span data-ttu-id="abedb-141">Erste Benutzer Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="abedb-141">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

