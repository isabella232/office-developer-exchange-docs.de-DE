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
ms.openlocfilehash: 320a7b821cc593e7dd60a8f8adb23bcd600f71f8
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353301"
---
# <a name="fieldorder"></a><span data-ttu-id="7374f-103">FieldOrder</span><span class="sxs-lookup"><span data-stu-id="7374f-103">FieldOrder</span></span>

<span data-ttu-id="7374f-104">Das **FieldOrder** -Element stellt ein einzelnes Feld, um die Suchergebnisse sortiert werden und gibt die Richtung für die Sortierung an.</span><span class="sxs-lookup"><span data-stu-id="7374f-104">The **FieldOrder** element represents a single field by which to sort results and indicates the direction for the sort.</span></span> 
  
```xml
<FieldOrder Order="">
   <FieldURI/>
</FieldOrder>
```

```xml
<FieldOrder Order="">
   <ExtendedFieldURI/> 
</FieldOrder>
```

```xml
<FieldOrder Order="">
   <IndexedFieldURI/>
</FieldOrder>
```

<span data-ttu-id="7374f-105">**FieldOrderType**</span><span class="sxs-lookup"><span data-stu-id="7374f-105">**FieldOrderType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="7374f-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="7374f-106">Attributes and elements</span></span>

<span data-ttu-id="7374f-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="7374f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7374f-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="7374f-108">Attributes</span></span>

|<span data-ttu-id="7374f-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="7374f-109">**Attribute**</span></span>|<span data-ttu-id="7374f-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7374f-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7374f-111">**Order**</span><span class="sxs-lookup"><span data-stu-id="7374f-111">**Order**</span></span> <br/> | <span data-ttu-id="7374f-112">Beschreibt die Sortierrichtung Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="7374f-112">Describes the sort order direction.</span></span><br/><br/> <span data-ttu-id="7374f-113">Im Folgenden sind die möglichen Werte aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="7374f-113">The following are the possible values:</span></span> <br/> <br/><span data-ttu-id="7374f-114">-Ascending</span><span class="sxs-lookup"><span data-stu-id="7374f-114">-  Ascending</span></span>  <br/><span data-ttu-id="7374f-115">-Absteigend</span><span class="sxs-lookup"><span data-stu-id="7374f-115">-  Descending</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7374f-116">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7374f-116">Child elements</span></span>

|<span data-ttu-id="7374f-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="7374f-117">**Element**</span></span>|<span data-ttu-id="7374f-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7374f-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7374f-119">FieldURI</span><span class="sxs-lookup"><span data-stu-id="7374f-119">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="7374f-120">Identifiziert die Eigenschaften von URI häufig verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="7374f-120">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="7374f-121">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="7374f-121">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="7374f-122">Einzelne Elemente eines Wörterbuchs identifiziert.</span><span class="sxs-lookup"><span data-stu-id="7374f-122">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="7374f-123">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="7374f-123">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="7374f-124">MAPI-Eigenschaften identifiziert.</span><span class="sxs-lookup"><span data-stu-id="7374f-124">Identifies MAPI properties.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7374f-125">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7374f-125">Parent elements</span></span>

|<span data-ttu-id="7374f-126">**Element**</span><span class="sxs-lookup"><span data-stu-id="7374f-126">**Element**</span></span>|<span data-ttu-id="7374f-127">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7374f-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7374f-128">SortOrder</span><span class="sxs-lookup"><span data-stu-id="7374f-128">SortOrder</span></span>](sortorder.md) <br/> |<span data-ttu-id="7374f-129">Definiert, wie Elemente in einer Anforderung FindItem sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="7374f-129">Defines how items are sorted in a FindItem request.</span></span>  <br/> <span data-ttu-id="7374f-130">Es folgt der XPath-Ausdruck, der dieses Element:`/FindItem/SortOrder`</span><span class="sxs-lookup"><span data-stu-id="7374f-130">The following is the XPath expression to this element:  `/FindItem/SortOrder`</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7374f-131">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7374f-131">Remarks</span></span>

<span data-ttu-id="7374f-132">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="7374f-132">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7374f-133">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="7374f-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7374f-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="7374f-134">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7374f-135">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="7374f-135">Schema Name</span></span>  <br/> |<span data-ttu-id="7374f-136">Schematypen</span><span class="sxs-lookup"><span data-stu-id="7374f-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="7374f-137">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="7374f-137">Validation File</span></span>  <br/> |<span data-ttu-id="7374f-138">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7374f-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7374f-139">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="7374f-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="7374f-140">False</span><span class="sxs-lookup"><span data-stu-id="7374f-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7374f-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7374f-141">See also</span></span>

- [<span data-ttu-id="7374f-142">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="7374f-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

