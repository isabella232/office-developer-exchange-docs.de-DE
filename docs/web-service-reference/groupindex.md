---
title: GroupIndex
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GroupIndex
api_type:
- schema
ms.assetid: 7a596ff7-6cc3-4626-a52c-538a92202337
description: Das GroupIndex-Element darstellt, den Wert der Eigenschaft, der zum Gruppieren von Elementen für die aktuelle Gruppe von Elementen in einem Aufruf der FindItem Vorgang verwendet wird.
ms.openlocfilehash: 8b23f5142a15c099c30209ea48cd04f4af4e8c6a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19829762"
---
# <a name="groupindex"></a><span data-ttu-id="70c75-103">GroupIndex</span><span class="sxs-lookup"><span data-stu-id="70c75-103">GroupIndex</span></span>

<span data-ttu-id="70c75-104">Das **GroupIndex** -Element darstellt, den Wert der Eigenschaft, der zum Gruppieren von Elementen für die aktuelle Gruppe von Elementen in einem Aufruf der [FindItem Vorgang](finditem-operation.md) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="70c75-104">The **GroupIndex** element represents the property value that is used to group items for the current group of items in a [FindItem operation](finditem-operation.md) call.</span></span> 
  
[<span data-ttu-id="70c75-105">FindItemResponse</span><span class="sxs-lookup"><span data-stu-id="70c75-105">FindItemResponse</span></span>](finditemresponse.md)
  
[<span data-ttu-id="70c75-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="70c75-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="70c75-107">FindItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="70c75-107">FindItemResponseMessage</span></span>](finditemresponsemessage.md)
  
[<span data-ttu-id="70c75-108">RootFolder (FindItemResponseMessage)</span><span class="sxs-lookup"><span data-stu-id="70c75-108">RootFolder (FindItemResponseMessage)</span></span>](rootfolder-finditemresponsemessage.md)
  
[<span data-ttu-id="70c75-109">Gruppen</span><span class="sxs-lookup"><span data-stu-id="70c75-109">Groups</span></span>](groups.md)
  
[<span data-ttu-id="70c75-110">GroupedItems</span><span class="sxs-lookup"><span data-stu-id="70c75-110">GroupedItems</span></span>](groupeditems.md)
  
[<span data-ttu-id="70c75-111">GroupIndex</span><span class="sxs-lookup"><span data-stu-id="70c75-111">GroupIndex</span></span>](groupindex.md)
  
```xml
<GroupIndex/>
```

 <span data-ttu-id="70c75-112">**string**</span><span class="sxs-lookup"><span data-stu-id="70c75-112">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="70c75-113">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="70c75-113">Attributes and elements</span></span>

<span data-ttu-id="70c75-114">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="70c75-114">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="70c75-115">Attribute</span><span class="sxs-lookup"><span data-stu-id="70c75-115">Attributes</span></span>

<span data-ttu-id="70c75-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="70c75-116">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="70c75-117">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="70c75-117">Child elements</span></span>

<span data-ttu-id="70c75-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="70c75-118">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="70c75-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="70c75-119">Parent elements</span></span>

|<span data-ttu-id="70c75-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="70c75-120">**Element**</span></span>|<span data-ttu-id="70c75-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="70c75-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="70c75-122">GroupedItems</span><span class="sxs-lookup"><span data-stu-id="70c75-122">GroupedItems</span></span>](groupeditems.md) <br/> |<span data-ttu-id="70c75-123">Stellt eine Auflistung von Elementen, die das Ergebnis einer gruppierten [FindItem Vorgang](finditem-operation.md) sind aufrufen.</span><span class="sxs-lookup"><span data-stu-id="70c75-123">Represents a collection of items that are the result of a grouped [FindItem operation](finditem-operation.md) call.</span></span>  <br/> <span data-ttu-id="70c75-124">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="70c75-124">The following is the XPath expression to this element:</span></span>  <br/>  `/FindItemResponse/ResponseMessages/FindItemResponseMessage/RootFolder/Groups/GroupedItems[i]` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="70c75-125">Textwert</span><span class="sxs-lookup"><span data-stu-id="70c75-125">Text value</span></span>

<span data-ttu-id="70c75-126">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="70c75-126">A text value is required.</span></span> <span data-ttu-id="70c75-127">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="70c75-127">This property is read-only.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="70c75-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="70c75-128">Remarks</span></span>

<span data-ttu-id="70c75-129">Dieses Element tritt nur in einer Antwort [FindItem Vorgang](finditem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="70c75-129">This element only occurs in a [FindItem operation](finditem-operation.md) response.</span></span> 
  
<span data-ttu-id="70c75-130">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="70c75-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="70c75-131">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="70c75-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="70c75-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="70c75-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="70c75-133">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="70c75-133">Schema name</span></span>  <br/> |<span data-ttu-id="70c75-134">Schematypen</span><span class="sxs-lookup"><span data-stu-id="70c75-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="70c75-135">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="70c75-135">Validation file</span></span>  <br/> |<span data-ttu-id="70c75-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="70c75-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="70c75-137">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="70c75-137">Can be empty</span></span>  <br/> |<span data-ttu-id="70c75-138">False</span><span class="sxs-lookup"><span data-stu-id="70c75-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="70c75-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="70c75-139">See also</span></span>



[<span data-ttu-id="70c75-140">FindItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="70c75-140">FindItem operation</span></span>](finditem-operation.md)


[<span data-ttu-id="70c75-141">Finding Items</span><span class="sxs-lookup"><span data-stu-id="70c75-141">Finding Items</span></span>](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

