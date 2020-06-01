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
description: Das MergedFreeBusyIntervalInMinutes-Element stellt den Zeitunterschied zwischen zwei aufeinanderfolgenden Slots in der FreeBusyMerged-Ansicht dar.
ms.openlocfilehash: 6228ee5b66202634e6bb3b6c1ad6b8897a109d58
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468789"
---
# <a name="mergedfreebusyintervalinminutes"></a><span data-ttu-id="7b0ab-103">MergedFreeBusyIntervalInMinutes</span><span class="sxs-lookup"><span data-stu-id="7b0ab-103">MergedFreeBusyIntervalInMinutes</span></span>

<span data-ttu-id="7b0ab-104">Das **MergedFreeBusyIntervalInMinutes** -Element stellt den Zeitunterschied zwischen zwei aufeinanderfolgenden Slots in der **FreeBusyMerged** -Ansicht dar.</span><span class="sxs-lookup"><span data-stu-id="7b0ab-104">The **MergedFreeBusyIntervalInMinutes** element represents the time difference between two successive slots in the **FreeBusyMerged** view.</span></span> 
  
[<span data-ttu-id="7b0ab-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="7b0ab-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
[<span data-ttu-id="7b0ab-106">FreeBusyViewOptions</span><span class="sxs-lookup"><span data-stu-id="7b0ab-106">FreeBusyViewOptions</span></span>](freebusyviewoptions.md)
  
[<span data-ttu-id="7b0ab-107">MergedFreeBusyIntervalInMinutes</span><span class="sxs-lookup"><span data-stu-id="7b0ab-107">MergedFreeBusyIntervalInMinutes</span></span>](mergedfreebusyintervalinminutes.md)
  
```xml
<MergedFreeBusyIntervalInMinutes>...</MergedFreeBusyIntervalInMinutes>
```

 <span data-ttu-id="7b0ab-108">**int**</span><span class="sxs-lookup"><span data-stu-id="7b0ab-108">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7b0ab-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="7b0ab-109">Attributes and elements</span></span>

<span data-ttu-id="7b0ab-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="7b0ab-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7b0ab-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="7b0ab-111">Attributes</span></span>

<span data-ttu-id="7b0ab-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="7b0ab-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7b0ab-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7b0ab-113">Child elements</span></span>

<span data-ttu-id="7b0ab-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="7b0ab-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7b0ab-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7b0ab-115">Parent elements</span></span>

|<span data-ttu-id="7b0ab-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="7b0ab-116">**Element**</span></span>|<span data-ttu-id="7b0ab-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7b0ab-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7b0ab-118">FreeBusyViewOptions</span><span class="sxs-lookup"><span data-stu-id="7b0ab-118">FreeBusyViewOptions</span></span>](freebusyviewoptions.md) <br/> |<span data-ttu-id="7b0ab-119">Gibt den Typ der Frei/Gebucht-Informationen an, die in der Antwort zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7b0ab-119">Specifies the type of free/busy information returned in the response.</span></span>  <br/> <span data-ttu-id="7b0ab-120">Es folgt der XPath für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="7b0ab-120">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/FreeBusyViewOptions` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7b0ab-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="7b0ab-121">Text value</span></span>

<span data-ttu-id="7b0ab-122">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7b0ab-122">A text value is required.</span></span> <span data-ttu-id="7b0ab-123">Der Textwert stellt die Zeit in Minuten dar.</span><span class="sxs-lookup"><span data-stu-id="7b0ab-123">The text value represents time in minutes.</span></span> <span data-ttu-id="7b0ab-124">Der Standardwert beträgt 30 Minuten.</span><span class="sxs-lookup"><span data-stu-id="7b0ab-124">The default value is 30 minutes.</span></span> <span data-ttu-id="7b0ab-125">Sechs Minuten sind das minimale Intervall und ein Tag (1440 Minuten) das maximale Intervall für dieses Element.</span><span class="sxs-lookup"><span data-stu-id="7b0ab-125">Six minutes is the minimum interval and one day (1440 minutes) is the maximum interval for this element.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7b0ab-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7b0ab-126">Remarks</span></span>

<span data-ttu-id="7b0ab-127">Dieser Wert wird nur verwendet, wenn das [RequestedView](requestedview.md) -Element gleich **MergedOnly**, **FreeBusyMerged**oder **DetailedMerge**ist.</span><span class="sxs-lookup"><span data-stu-id="7b0ab-127">This value is used only if the [RequestedView](requestedview.md) element is equal to **MergedOnly**, **FreeBusyMerged**, or **DetailedMerge**.</span></span> <span data-ttu-id="7b0ab-128">Dies ist ein Integer-Datentyp.</span><span class="sxs-lookup"><span data-stu-id="7b0ab-128">This is an integer data type.</span></span> <span data-ttu-id="7b0ab-129">Der Datenstrom, der die durch dieses Element definierten Intervalle enthält, wird im [MergedFreeBusy](mergedfreebusy.md) -Element zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7b0ab-129">The stream that contains the intervals defined by this element is returned in the [MergedFreeBusy](mergedfreebusy.md) element.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="7b0ab-130">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="7b0ab-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7b0ab-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="7b0ab-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7b0ab-132">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="7b0ab-132">Schema Name</span></span>  <br/> |<span data-ttu-id="7b0ab-133">Schematypen</span><span class="sxs-lookup"><span data-stu-id="7b0ab-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="7b0ab-134">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="7b0ab-134">Validation File</span></span>  <br/> |<span data-ttu-id="7b0ab-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7b0ab-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7b0ab-136">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="7b0ab-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="7b0ab-137">False</span><span class="sxs-lookup"><span data-stu-id="7b0ab-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7b0ab-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7b0ab-138">See also</span></span>



[<span data-ttu-id="7b0ab-139">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="7b0ab-139">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="7b0ab-140">GetUserOofSettings-Vorgang</span><span class="sxs-lookup"><span data-stu-id="7b0ab-140">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md)


[<span data-ttu-id="7b0ab-141">Verfügbarkeit von Benutzern wird abgerufen</span><span class="sxs-lookup"><span data-stu-id="7b0ab-141">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

