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
description: Das StandardGroupBy-Element stellt die standardmäßigen Gruppierungs-und Aggregations Mechanismen für einen gruppierten FindItem-Vorgang dar.
ms.openlocfilehash: 3e135feba322979de3d66d5a45d423654ccc9100
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467557"
---
# <a name="standardgroupby"></a><span data-ttu-id="b73a0-103">StandardGroupBy</span><span class="sxs-lookup"><span data-stu-id="b73a0-103">StandardGroupBy</span></span>

<span data-ttu-id="b73a0-104">Das **StandardGroupBy** -Element stellt die standardmäßigen Gruppierungs-und Aggregations Mechanismen für einen gruppierten FindItem-Vorgang dar.</span><span class="sxs-lookup"><span data-stu-id="b73a0-104">The **StandardGroupBy** element represents the standard grouping and aggregating mechanisms for a grouped FindItem operation.</span></span> 
  
[<span data-ttu-id="b73a0-105">FindItem</span><span class="sxs-lookup"><span data-stu-id="b73a0-105">FindItem</span></span>](finditem.md)
  
[<span data-ttu-id="b73a0-106">DistinguishedGroupBy</span><span class="sxs-lookup"><span data-stu-id="b73a0-106">DistinguishedGroupBy</span></span>](distinguishedgroupby.md)
  
[<span data-ttu-id="b73a0-107">StandardGroupBy</span><span class="sxs-lookup"><span data-stu-id="b73a0-107">StandardGroupBy</span></span>](standardgroupby.md)
  
```xml
<StandardGroupBy/>
```

 <span data-ttu-id="b73a0-108">**StandardGroupByType**</span><span class="sxs-lookup"><span data-stu-id="b73a0-108">**StandardGroupByType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b73a0-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b73a0-109">Attributes and elements</span></span>

<span data-ttu-id="b73a0-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b73a0-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b73a0-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="b73a0-111">Attributes</span></span>

<span data-ttu-id="b73a0-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="b73a0-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b73a0-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b73a0-113">Child elements</span></span>

<span data-ttu-id="b73a0-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="b73a0-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b73a0-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b73a0-115">Parent elements</span></span>

|<span data-ttu-id="b73a0-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="b73a0-116">**Element**</span></span>|<span data-ttu-id="b73a0-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b73a0-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b73a0-118">DistinguishedGroupBy</span><span class="sxs-lookup"><span data-stu-id="b73a0-118">DistinguishedGroupBy</span></span>](distinguishedgroupby.md) <br/> |<span data-ttu-id="b73a0-119">Stellt Standardgruppierungen für FindItem-Abfragen bereit.</span><span class="sxs-lookup"><span data-stu-id="b73a0-119">Provides standard groupings for FindItem queries.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b73a0-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="b73a0-120">Text value</span></span>

<span data-ttu-id="b73a0-121">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b73a0-121">A text value is required.</span></span> <span data-ttu-id="b73a0-122">Der einzige Wert, der für dieses Element verwendet werden kann, ist **ConversationTopic**.</span><span class="sxs-lookup"><span data-stu-id="b73a0-122">The only value that can be used for this element is **ConversationTopic**.</span></span> <span data-ttu-id="b73a0-123">**ConversationTopic** Gruppen nach Nachricht: ConversationTopic und Aggregate für Element: DateTimeReceived (Maximum).</span><span class="sxs-lookup"><span data-stu-id="b73a0-123">**ConversationTopic** groups by message:ConversationTopic and aggregates on item:DateTimeReceived (maximum).</span></span> <span data-ttu-id="b73a0-124">Weitere Informationen zur Aggregation finden Sie unter [AggregateOn](aggregateon.md).</span><span class="sxs-lookup"><span data-stu-id="b73a0-124">For more information about aggregation, see [AggregateOn](aggregateon.md).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b73a0-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b73a0-125">Remarks</span></span>

<span data-ttu-id="b73a0-126">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="b73a0-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b73a0-127">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="b73a0-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b73a0-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="b73a0-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b73a0-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b73a0-129">Schema Name</span></span>  <br/> |<span data-ttu-id="b73a0-130">Schematypen</span><span class="sxs-lookup"><span data-stu-id="b73a0-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="b73a0-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b73a0-131">Validation File</span></span>  <br/> |<span data-ttu-id="b73a0-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b73a0-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b73a0-133">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="b73a0-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="b73a0-134">False</span><span class="sxs-lookup"><span data-stu-id="b73a0-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b73a0-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b73a0-135">See also</span></span>



[<span data-ttu-id="b73a0-136">FindItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="b73a0-136">FindItem operation</span></span>](finditem-operation.md)
  
[<span data-ttu-id="b73a0-137">FindItem</span><span class="sxs-lookup"><span data-stu-id="b73a0-137">FindItem</span></span>](finditem.md)


[<span data-ttu-id="b73a0-138">Suchen von Elementen</span><span class="sxs-lookup"><span data-stu-id="b73a0-138">Finding Items</span></span>](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

