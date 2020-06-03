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
description: Das FieldOrder-Element stellt ein einzelnes Feld dar, nach dem Ergebnisse sortiert werden, und gibt die Richtung für die Sortierung an.
ms.openlocfilehash: 19dee7175d541dd99b53e004ea8ccd785b619184
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461261"
---
# <a name="fieldorder"></a><span data-ttu-id="ac409-103">FieldOrder</span><span class="sxs-lookup"><span data-stu-id="ac409-103">FieldOrder</span></span>

<span data-ttu-id="ac409-104">Das **FieldOrder** -Element stellt ein einzelnes Feld dar, nach dem Ergebnisse sortiert werden, und gibt die Richtung für die Sortierung an.</span><span class="sxs-lookup"><span data-stu-id="ac409-104">The **FieldOrder** element represents a single field by which to sort results and indicates the direction for the sort.</span></span> 
  
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

<span data-ttu-id="ac409-105">**FieldOrderType**</span><span class="sxs-lookup"><span data-stu-id="ac409-105">**FieldOrderType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="ac409-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ac409-106">Attributes and elements</span></span>

<span data-ttu-id="ac409-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ac409-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ac409-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="ac409-108">Attributes</span></span>

|<span data-ttu-id="ac409-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="ac409-109">**Attribute**</span></span>|<span data-ttu-id="ac409-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ac409-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ac409-111">**Order**</span><span class="sxs-lookup"><span data-stu-id="ac409-111">**Order**</span></span> <br/> | <span data-ttu-id="ac409-112">Beschreibt die Richtung der Sortierreihenfolge.</span><span class="sxs-lookup"><span data-stu-id="ac409-112">Describes the sort order direction.</span></span><br/><br/> <span data-ttu-id="ac409-113">Im Folgenden sind die möglichen Werte aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="ac409-113">The following are the possible values:</span></span> <br/> <br/><span data-ttu-id="ac409-114">-Aufsteigend</span><span class="sxs-lookup"><span data-stu-id="ac409-114">-  Ascending</span></span>  <br/><span data-ttu-id="ac409-115">-Absteigend</span><span class="sxs-lookup"><span data-stu-id="ac409-115">-  Descending</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ac409-116">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ac409-116">Child elements</span></span>

|<span data-ttu-id="ac409-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="ac409-117">**Element**</span></span>|<span data-ttu-id="ac409-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ac409-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ac409-119">FieldURI</span><span class="sxs-lookup"><span data-stu-id="ac409-119">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="ac409-120">Identifiziert häufig referenzierte Eigenschaften nach URI.</span><span class="sxs-lookup"><span data-stu-id="ac409-120">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="ac409-121">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="ac409-121">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="ac409-122">Identifiziert einzelne Member eines Wörterbuchs.</span><span class="sxs-lookup"><span data-stu-id="ac409-122">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="ac409-123">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="ac409-123">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="ac409-124">Identifiziert MAPI-Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ac409-124">Identifies MAPI properties.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ac409-125">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ac409-125">Parent elements</span></span>

|<span data-ttu-id="ac409-126">**Element**</span><span class="sxs-lookup"><span data-stu-id="ac409-126">**Element**</span></span>|<span data-ttu-id="ac409-127">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ac409-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ac409-128">SortOrder</span><span class="sxs-lookup"><span data-stu-id="ac409-128">SortOrder</span></span>](sortorder.md) <br/> |<span data-ttu-id="ac409-129">Definiert, wie Elemente in einer FindItem-Anforderung sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="ac409-129">Defines how items are sorted in a FindItem request.</span></span>  <br/> <span data-ttu-id="ac409-130">Im folgenden finden Sie den XPath-Ausdruck für dieses Element:`/FindItem/SortOrder`</span><span class="sxs-lookup"><span data-stu-id="ac409-130">The following is the XPath expression to this element:  `/FindItem/SortOrder`</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ac409-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ac409-131">Remarks</span></span>

<span data-ttu-id="ac409-132">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="ac409-132">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ac409-133">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="ac409-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ac409-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="ac409-134">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ac409-135">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ac409-135">Schema Name</span></span>  <br/> |<span data-ttu-id="ac409-136">Schematypen</span><span class="sxs-lookup"><span data-stu-id="ac409-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="ac409-137">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ac409-137">Validation File</span></span>  <br/> |<span data-ttu-id="ac409-138">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ac409-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ac409-139">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="ac409-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="ac409-140">False</span><span class="sxs-lookup"><span data-stu-id="ac409-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ac409-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ac409-141">See also</span></span>

- [<span data-ttu-id="ac409-142">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="ac409-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

