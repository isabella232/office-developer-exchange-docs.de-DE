---
title: FieldOrder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FieldOrder
api_type:
- schema
ms.assetid: b9364842-bbe2-4221-afef-bf5022bc89ec
description: Das FieldOrder-Element stellt ein einzelnes Feld, um die Suchergebnisse sortiert werden und gibt die Richtung für die Sortierung an.
ms.openlocfilehash: 10e28f066f7fa6799bf6b03b694d98825f95626d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758413"
---
# <a name="fieldorder"></a><span data-ttu-id="bc5d9-103">FieldOrder</span><span class="sxs-lookup"><span data-stu-id="bc5d9-103">FieldOrder</span></span>

<span data-ttu-id="bc5d9-104">Das **FieldOrder** -Element stellt ein einzelnes Feld, um die Suchergebnisse sortiert werden und gibt die Richtung für die Sortierung an.</span><span class="sxs-lookup"><span data-stu-id="bc5d9-104">The **FieldOrder** element represents a single field by which to sort results and indicates the direction for the sort.</span></span> 
  
```xml
<FieldOrder Order="">
   <FieldURI/>
</FieldOrder>
```

 <span data-ttu-id="bc5d9-105">**FieldOrderType**</span><span class="sxs-lookup"><span data-stu-id="bc5d9-105">**FieldOrderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bc5d9-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="bc5d9-106">Attributes and elements</span></span>

<span data-ttu-id="bc5d9-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="bc5d9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bc5d9-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="bc5d9-108">Attributes</span></span>

|<span data-ttu-id="bc5d9-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="bc5d9-109">**Attribute**</span></span>|<span data-ttu-id="bc5d9-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bc5d9-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bc5d9-111">**Order**</span><span class="sxs-lookup"><span data-stu-id="bc5d9-111">**Order**</span></span> <br/> | <span data-ttu-id="bc5d9-112">Beschreibt die Sortierrichtung Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="bc5d9-112">Describes the sort order direction.</span></span><br/><br/> <span data-ttu-id="bc5d9-113">Im Folgenden sind die möglichen Werte aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="bc5d9-113">The following are the possible values:</span></span> <br/> <br/><span data-ttu-id="bc5d9-114">-Ascending</span><span class="sxs-lookup"><span data-stu-id="bc5d9-114">-  Ascending</span></span>  <br/><span data-ttu-id="bc5d9-115">-Absteigend</span><span class="sxs-lookup"><span data-stu-id="bc5d9-115">-  Descending</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="bc5d9-116">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bc5d9-116">Child elements</span></span>

|<span data-ttu-id="bc5d9-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="bc5d9-117">**Element**</span></span>|<span data-ttu-id="bc5d9-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bc5d9-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bc5d9-119">FieldURI</span><span class="sxs-lookup"><span data-stu-id="bc5d9-119">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="bc5d9-120">Identifiziert die Eigenschaften von URI häufig verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="bc5d9-120">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="bc5d9-121">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="bc5d9-121">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="bc5d9-122">Einzelne Elemente eines Wörterbuchs identifiziert.</span><span class="sxs-lookup"><span data-stu-id="bc5d9-122">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="bc5d9-123">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="bc5d9-123">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="bc5d9-124">MAPI-Eigenschaften identifiziert.</span><span class="sxs-lookup"><span data-stu-id="bc5d9-124">Identifies MAPI properties.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="bc5d9-125">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bc5d9-125">Parent elements</span></span>

|<span data-ttu-id="bc5d9-126">**Element**</span><span class="sxs-lookup"><span data-stu-id="bc5d9-126">**Element**</span></span>|<span data-ttu-id="bc5d9-127">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bc5d9-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bc5d9-128">SortOrder</span><span class="sxs-lookup"><span data-stu-id="bc5d9-128">SortOrder</span></span>](sortorder.md) <br/> |<span data-ttu-id="bc5d9-129">Definiert, wie Elemente in einer Anforderung FindItem sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="bc5d9-129">Defines how items are sorted in a FindItem request.</span></span>  <br/> <span data-ttu-id="bc5d9-130">Es folgt der XPath-Ausdruck, der dieses Element:`/FindItem/SortOrder`</span><span class="sxs-lookup"><span data-stu-id="bc5d9-130">The following is the XPath expression to this element:  `/FindItem/SortOrder`</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bc5d9-131">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bc5d9-131">Remarks</span></span>

<span data-ttu-id="bc5d9-132">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="bc5d9-132">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bc5d9-133">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="bc5d9-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bc5d9-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="bc5d9-134">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="bc5d9-135">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="bc5d9-135">Schema Name</span></span>  <br/> |<span data-ttu-id="bc5d9-136">Schematypen</span><span class="sxs-lookup"><span data-stu-id="bc5d9-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="bc5d9-137">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="bc5d9-137">Validation File</span></span>  <br/> |<span data-ttu-id="bc5d9-138">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="bc5d9-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="bc5d9-139">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="bc5d9-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="bc5d9-140">False</span><span class="sxs-lookup"><span data-stu-id="bc5d9-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bc5d9-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bc5d9-141">See also</span></span>

- [<span data-ttu-id="bc5d9-142">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="bc5d9-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

