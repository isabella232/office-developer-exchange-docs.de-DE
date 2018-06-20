---
title: StandardGroupBy
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- StandardGroupBy
api_type:
- schema
ms.assetid: 04a84f71-b7eb-44dc-ac2c-ed504b52c463
description: Das StandardGroupBy-Element darstellt, den Standard gruppieren und Aggregieren von Mechanismen für einen gruppierten FindItem-Vorgang.
ms.openlocfilehash: 8e2ec72a79ebafc2e5757d6dcebb27c0c53ec0b5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831542"
---
# <a name="standardgroupby"></a><span data-ttu-id="39998-103">StandardGroupBy</span><span class="sxs-lookup"><span data-stu-id="39998-103">StandardGroupBy</span></span>

<span data-ttu-id="39998-104">Das **StandardGroupBy** -Element darstellt, den Standard gruppieren und Aggregieren von Mechanismen für einen gruppierten FindItem-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="39998-104">The **StandardGroupBy** element represents the standard grouping and aggregating mechanisms for a grouped FindItem operation.</span></span> 
  
[<span data-ttu-id="39998-105">FindItem</span><span class="sxs-lookup"><span data-stu-id="39998-105">FindItem</span></span>](finditem.md)
  
[<span data-ttu-id="39998-106">DistinguishedGroupBy</span><span class="sxs-lookup"><span data-stu-id="39998-106">DistinguishedGroupBy</span></span>](distinguishedgroupby.md)
  
[<span data-ttu-id="39998-107">StandardGroupBy</span><span class="sxs-lookup"><span data-stu-id="39998-107">StandardGroupBy</span></span>](standardgroupby.md)
  
```xml
<StandardGroupBy/>
```

 <span data-ttu-id="39998-108">**StandardGroupByType**</span><span class="sxs-lookup"><span data-stu-id="39998-108">**StandardGroupByType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="39998-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="39998-109">Attributes and elements</span></span>

<span data-ttu-id="39998-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="39998-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="39998-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="39998-111">Attributes</span></span>

<span data-ttu-id="39998-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="39998-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="39998-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="39998-113">Child elements</span></span>

<span data-ttu-id="39998-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="39998-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="39998-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="39998-115">Parent elements</span></span>

|<span data-ttu-id="39998-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="39998-116">**Element**</span></span>|<span data-ttu-id="39998-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="39998-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="39998-118">DistinguishedGroupBy</span><span class="sxs-lookup"><span data-stu-id="39998-118">DistinguishedGroupBy</span></span>](distinguishedgroupby.md) <br/> |<span data-ttu-id="39998-119">FindItem Abfragen bereit standard Gruppen.</span><span class="sxs-lookup"><span data-stu-id="39998-119">Provides standard groupings for FindItem queries.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="39998-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="39998-120">Text value</span></span>

<span data-ttu-id="39998-121">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="39998-121">A text value is required.</span></span> <span data-ttu-id="39998-122">**ConversationTopic**wird nur ein Wert, der für dieses Element verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="39998-122">The only value that can be used for this element is **ConversationTopic**.</span></span> <span data-ttu-id="39998-123">**ConversationTopic** gruppiert nach Nachricht: ConversationTopic und Aggregate auf Element: DateTimeReceived (maximal).</span><span class="sxs-lookup"><span data-stu-id="39998-123">**ConversationTopic** groups by message:ConversationTopic and aggregates on item:DateTimeReceived (maximum).</span></span> <span data-ttu-id="39998-124">Weitere Informationen über die Aggregation finden Sie unter [AggregateOn](aggregateon.md).</span><span class="sxs-lookup"><span data-stu-id="39998-124">For more information about aggregation, see [AggregateOn](aggregateon.md).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="39998-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="39998-125">Remarks</span></span>

<span data-ttu-id="39998-126">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="39998-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="39998-127">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="39998-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="39998-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="39998-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="39998-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="39998-129">Schema Name</span></span>  <br/> |<span data-ttu-id="39998-130">Schematypen</span><span class="sxs-lookup"><span data-stu-id="39998-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="39998-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="39998-131">Validation File</span></span>  <br/> |<span data-ttu-id="39998-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="39998-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="39998-133">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="39998-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="39998-134">False</span><span class="sxs-lookup"><span data-stu-id="39998-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="39998-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="39998-135">See also</span></span>



[<span data-ttu-id="39998-136">FindItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="39998-136">FindItem operation</span></span>](finditem-operation.md)
  
[<span data-ttu-id="39998-137">FindItem</span><span class="sxs-lookup"><span data-stu-id="39998-137">FindItem</span></span>](finditem.md)


[<span data-ttu-id="39998-138">Finding Items</span><span class="sxs-lookup"><span data-stu-id="39998-138">Finding Items</span></span>](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

