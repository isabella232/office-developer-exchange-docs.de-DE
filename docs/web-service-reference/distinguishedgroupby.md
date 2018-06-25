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
description: Das Element DistinguishedGroupBy bereit FindItem Abfragen standard Gruppen.
ms.openlocfilehash: 0635366447675bf28dedf3af4f7d76094ee5e0a4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758071"
---
# <a name="distinguishedgroupby"></a><span data-ttu-id="bfa62-103">DistinguishedGroupBy</span><span class="sxs-lookup"><span data-stu-id="bfa62-103">DistinguishedGroupBy</span></span>

<span data-ttu-id="bfa62-104">Das Element **DistinguishedGroupBy** bereit FindItem Abfragen standard Gruppen.</span><span class="sxs-lookup"><span data-stu-id="bfa62-104">The **DistinguishedGroupBy** element provides standard groupings for FindItem queries.</span></span> 
  
- [<span data-ttu-id="bfa62-105">FindItem</span><span class="sxs-lookup"><span data-stu-id="bfa62-105">FindItem</span></span>](finditem.md) 
- [<span data-ttu-id="bfa62-106">DistinguishedGroupBy</span><span class="sxs-lookup"><span data-stu-id="bfa62-106">DistinguishedGroupBy</span></span>](distinguishedgroupby.md)
  
```xml
<DistinguishedGroupBy>
   <StandardGroupBy/>
</DistinguishedGroupBy>
```

 <span data-ttu-id="bfa62-107">**DistinguishedGroupByType**</span><span class="sxs-lookup"><span data-stu-id="bfa62-107">**DistinguishedGroupByType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bfa62-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="bfa62-108">Attributes and elements</span></span>

<span data-ttu-id="bfa62-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="bfa62-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bfa62-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="bfa62-110">Attributes</span></span>

<span data-ttu-id="bfa62-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="bfa62-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bfa62-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bfa62-112">Child elements</span></span>

|<span data-ttu-id="bfa62-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="bfa62-113">**Element**</span></span>|<span data-ttu-id="bfa62-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bfa62-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bfa62-115">StandardGroupBy</span><span class="sxs-lookup"><span data-stu-id="bfa62-115">StandardGroupBy</span></span>](standardgroupby.md) <br/> |<span data-ttu-id="bfa62-116">Stellt den Standard gruppieren und Aggregieren von Mechanismen für einen gruppierten FindItem Vorgang dar.</span><span class="sxs-lookup"><span data-stu-id="bfa62-116">Represents the standard grouping and aggregating mechanisms for a grouped FindItem operation.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="bfa62-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bfa62-117">Parent elements</span></span>

|<span data-ttu-id="bfa62-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="bfa62-118">**Element**</span></span>|<span data-ttu-id="bfa62-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bfa62-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bfa62-120">FindItem</span><span class="sxs-lookup"><span data-stu-id="bfa62-120">FindItem</span></span>](finditem.md) <br/> |<span data-ttu-id="bfa62-121">Definiert eine Anforderung zum Suchen von Elementen in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="bfa62-121">Defines a request to find items in a mailbox.</span></span><br/><br/><span data-ttu-id="bfa62-122">Es folgt der XPath-Ausdruck, der dieses Element:`/FindItem`</span><span class="sxs-lookup"><span data-stu-id="bfa62-122">The following is the XPath expression to this element:  `/FindItem`</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bfa62-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bfa62-123">Remarks</span></span>

<span data-ttu-id="bfa62-124">Das Element **DistinguishedGroupBy** kann auf eine FindItem Operation hinzugefügt werden bei der Ergebnisse gesicherte stammen muss gruppiert und wenn eines der Standardgruppen die Gruppierung Anforderungen erfüllt.</span><span class="sxs-lookup"><span data-stu-id="bfa62-124">The **DistinguishedGroupBy** element can be added to a FindItem operation when the results must come backed grouped and when one of the standard groups meets the grouping requirements.</span></span> <span data-ttu-id="bfa62-125">Wenn weder das **DistinguishedGroupBy** -Element noch das [GroupBy](groupby.md) -Element angegeben ist, deren Gruppierung nicht aufgehoben FindItem Ergebnisse zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="bfa62-125">If neither the **DistinguishedGroupBy** element nor the [GroupBy](groupby.md) element is specified, FindItem results will come back ungrouped.</span></span> 
  
<span data-ttu-id="bfa62-126">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="bfa62-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bfa62-127">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="bfa62-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bfa62-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="bfa62-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="bfa62-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="bfa62-129">Schema Name</span></span>  <br/> |<span data-ttu-id="bfa62-130">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="bfa62-130">Messages schema</span></span>  <br/> |
|<span data-ttu-id="bfa62-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="bfa62-131">Validation File</span></span>  <br/> |<span data-ttu-id="bfa62-132">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="bfa62-132">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="bfa62-133">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="bfa62-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="bfa62-134">False</span><span class="sxs-lookup"><span data-stu-id="bfa62-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bfa62-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bfa62-135">See also</span></span>

- [<span data-ttu-id="bfa62-136">FindItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="bfa62-136">FindItem operation</span></span>](finditem-operation.md)
- [<span data-ttu-id="bfa62-137">Finding Items</span><span class="sxs-lookup"><span data-stu-id="bfa62-137">Finding Items</span></span>](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

