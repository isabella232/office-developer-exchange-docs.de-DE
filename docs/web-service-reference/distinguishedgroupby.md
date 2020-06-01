---
title: DistinguishedGroupBy
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DistinguishedGroupBy
api_type:
- schema
ms.assetid: 6ff3ac48-02ba-40ec-a71b-c401bb2b127c
description: Das DistinguishedGroupBy-Element stellt Standardgruppierungen für FindItem-Abfragen bereit.
ms.openlocfilehash: 004613d55419a19f69e960203ae13d8d906b74c8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463139"
---
# <a name="distinguishedgroupby"></a><span data-ttu-id="d5aea-103">DistinguishedGroupBy</span><span class="sxs-lookup"><span data-stu-id="d5aea-103">DistinguishedGroupBy</span></span>

<span data-ttu-id="d5aea-104">Das **DistinguishedGroupBy** -Element stellt Standardgruppierungen für FindItem-Abfragen bereit.</span><span class="sxs-lookup"><span data-stu-id="d5aea-104">The **DistinguishedGroupBy** element provides standard groupings for FindItem queries.</span></span> 
  
- [<span data-ttu-id="d5aea-105">FindItem</span><span class="sxs-lookup"><span data-stu-id="d5aea-105">FindItem</span></span>](finditem.md) 
- [<span data-ttu-id="d5aea-106">DistinguishedGroupBy</span><span class="sxs-lookup"><span data-stu-id="d5aea-106">DistinguishedGroupBy</span></span>](distinguishedgroupby.md)
  
```xml
<DistinguishedGroupBy>
   <StandardGroupBy/>
</DistinguishedGroupBy>
```

 <span data-ttu-id="d5aea-107">**DistinguishedGroupByType**</span><span class="sxs-lookup"><span data-stu-id="d5aea-107">**DistinguishedGroupByType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d5aea-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d5aea-108">Attributes and elements</span></span>

<span data-ttu-id="d5aea-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d5aea-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d5aea-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="d5aea-110">Attributes</span></span>

<span data-ttu-id="d5aea-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="d5aea-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d5aea-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d5aea-112">Child elements</span></span>

|<span data-ttu-id="d5aea-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="d5aea-113">**Element**</span></span>|<span data-ttu-id="d5aea-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d5aea-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d5aea-115">StandardGroupBy</span><span class="sxs-lookup"><span data-stu-id="d5aea-115">StandardGroupBy</span></span>](standardgroupby.md) <br/> |<span data-ttu-id="d5aea-116">Stellt die standardmäßigen Gruppierungs-und Aggregations Mechanismen für einen gruppierten FindItem-Vorgang dar.</span><span class="sxs-lookup"><span data-stu-id="d5aea-116">Represents the standard grouping and aggregating mechanisms for a grouped FindItem operation.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d5aea-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d5aea-117">Parent elements</span></span>

|<span data-ttu-id="d5aea-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="d5aea-118">**Element**</span></span>|<span data-ttu-id="d5aea-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d5aea-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d5aea-120">FindItem</span><span class="sxs-lookup"><span data-stu-id="d5aea-120">FindItem</span></span>](finditem.md) <br/> |<span data-ttu-id="d5aea-121">Definiert eine Anforderung zum Suchen von Elementen in einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="d5aea-121">Defines a request to find items in a mailbox.</span></span><br/><br/><span data-ttu-id="d5aea-122">Im folgenden finden Sie den XPath-Ausdruck für dieses Element:`/FindItem`</span><span class="sxs-lookup"><span data-stu-id="d5aea-122">The following is the XPath expression to this element:  `/FindItem`</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d5aea-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d5aea-123">Remarks</span></span>

<span data-ttu-id="d5aea-124">Das **DistinguishedGroupBy** -Element kann einem FindItem-Vorgang hinzugefügt werden, wenn die Ergebnisse gruppiert zurückgegeben werden müssen und wenn eine der Standardgruppen die Gruppierungs Anforderungen erfüllt.</span><span class="sxs-lookup"><span data-stu-id="d5aea-124">The **DistinguishedGroupBy** element can be added to a FindItem operation when the results must come backed grouped and when one of the standard groups meets the grouping requirements.</span></span> <span data-ttu-id="d5aea-125">Wenn weder das **DistinguishedGroupBy** -Element noch das [GroupBy](groupby.md) -Element angegeben wird, werden die FindItem-Ergebnisse ungruppiert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d5aea-125">If neither the **DistinguishedGroupBy** element nor the [GroupBy](groupby.md) element is specified, FindItem results will come back ungrouped.</span></span> 
  
<span data-ttu-id="d5aea-126">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="d5aea-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d5aea-127">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="d5aea-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d5aea-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="d5aea-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d5aea-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d5aea-129">Schema Name</span></span>  <br/> |<span data-ttu-id="d5aea-130">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="d5aea-130">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d5aea-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d5aea-131">Validation File</span></span>  <br/> |<span data-ttu-id="d5aea-132">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="d5aea-132">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d5aea-133">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d5aea-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="d5aea-134">False</span><span class="sxs-lookup"><span data-stu-id="d5aea-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d5aea-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d5aea-135">See also</span></span>

- [<span data-ttu-id="d5aea-136">FindItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d5aea-136">FindItem operation</span></span>](finditem-operation.md)
- [<span data-ttu-id="d5aea-137">Finding Items</span><span class="sxs-lookup"><span data-stu-id="d5aea-137">Finding Items</span></span>](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

