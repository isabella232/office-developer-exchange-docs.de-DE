---
title: Gruppen
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Groups
api_type:
- schema
ms.assetid: 6b6b2d67-219d-4dfb-a4ed-d627b1cfb33f
description: Das groups-Element enthält eine Auflistung von Gruppen, die mit den Such-und Aggregations Kriterien gefunden werden, die in der FindItem-Vorgangsanforderung angegeben werden.
ms.openlocfilehash: 915d9dffd6d8cec1def6634e6b70642d563b5242
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530789"
---
# <a name="groups"></a><span data-ttu-id="3a234-103">Gruppen</span><span class="sxs-lookup"><span data-stu-id="3a234-103">Groups</span></span>

<span data-ttu-id="3a234-104">Das **Groups** -Element enthält eine Auflistung von Gruppen, die mit den Such-und Aggregations Kriterien gefunden werden, die in der [FindItem-Vorgangs](finditem-operation.md) Anforderung angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3a234-104">The **Groups** element contains a collection of groups that are found with the search and aggregation criteria that is identified in the [FindItem operation](finditem-operation.md) request.</span></span> 
  
```xml
<Groups>
   <GroupedItems/>
</Groups>
```

 <span data-ttu-id="3a234-105">**ArrayOfGroupedItemsType**</span><span class="sxs-lookup"><span data-stu-id="3a234-105">**ArrayOfGroupedItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3a234-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3a234-106">Attributes and elements</span></span>

<span data-ttu-id="3a234-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="3a234-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3a234-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="3a234-108">Attributes</span></span>

<span data-ttu-id="3a234-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="3a234-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3a234-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3a234-110">Child elements</span></span>

|<span data-ttu-id="3a234-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="3a234-111">**Element**</span></span>|<span data-ttu-id="3a234-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3a234-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3a234-113">GroupedItems</span><span class="sxs-lookup"><span data-stu-id="3a234-113">GroupedItems</span></span>](groupeditems.md) <br/> |<span data-ttu-id="3a234-114">Stellt eine Auflistung von Elementen dar, die das Ergebnis eines Aufrufs einer gruppierten [FindItem-Operation](finditem-operation.md) sind.</span><span class="sxs-lookup"><span data-stu-id="3a234-114">Represents a collection of items that are the result of a grouped [FindItem operation](finditem-operation.md) call.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3a234-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3a234-115">Parent elements</span></span>

|<span data-ttu-id="3a234-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="3a234-116">**Element**</span></span>|<span data-ttu-id="3a234-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3a234-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3a234-118">RootFolder (FindItemResponseMessage)</span><span class="sxs-lookup"><span data-stu-id="3a234-118">RootFolder (FindItemResponseMessage)</span></span>](rootfolder-finditemresponsemessage.md) <br/> |<span data-ttu-id="3a234-119">Enthält die Ergebnisse aus der Suche eines einzelnen Stammordners während eines Vorgangs des [FindItem-Vorgangs](finditem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="3a234-119">Contains the results from a search of a single root folder during a [FindItem operation](finditem-operation.md) operation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3a234-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3a234-120">Remarks</span></span>

<span data-ttu-id="3a234-121">Für jede unterschiedliche Gruppe innerhalb des Ergebnisses wird eine [GroupedItems](groupeditems.md) -Instanz ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3a234-121">One [GroupedItems](groupeditems.md) instance will occur for each distinct group within the result.</span></span> 
  
<span data-ttu-id="3a234-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="3a234-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3a234-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="3a234-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3a234-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="3a234-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3a234-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="3a234-125">Schema name</span></span>  <br/> |<span data-ttu-id="3a234-126">Schematypen</span><span class="sxs-lookup"><span data-stu-id="3a234-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="3a234-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="3a234-127">Validation file</span></span>  <br/> |<span data-ttu-id="3a234-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3a234-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3a234-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="3a234-129">Can be empty</span></span>  <br/> |<span data-ttu-id="3a234-130">False</span><span class="sxs-lookup"><span data-stu-id="3a234-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3a234-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3a234-131">See also</span></span>



[<span data-ttu-id="3a234-132">FindItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="3a234-132">FindItem operation</span></span>](finditem-operation.md)


[<span data-ttu-id="3a234-133">Suchen von Elementen</span><span class="sxs-lookup"><span data-stu-id="3a234-133">Finding Items</span></span>](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

