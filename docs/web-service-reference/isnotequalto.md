---
title: IsNotEqualTo
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsNotEqualTo
api_type:
- schema
ms.assetid: e2eff26c-3403-45cd-bb74-1eb98c7dbfcd
description: Das IsNotEqualTo-Element stellt einen Search-Ausdruck, der vergleicht eine Eigenschaft mit entweder einen konstanten Wert oder eine andere Eigenschaft und gibt true, wenn die Werte nicht identisch sind.
ms.openlocfilehash: c11f5ba5b8c0672bba0b9ae2a76211ac7d5d94ad
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830059"
---
# <a name="isnotequalto"></a><span data-ttu-id="4f34a-103">IsNotEqualTo</span><span class="sxs-lookup"><span data-stu-id="4f34a-103">IsNotEqualTo</span></span>

<span data-ttu-id="4f34a-104">Das **IsNotEqualTo** -Element stellt einen Search-Ausdruck, der eine Eigenschaft mit einem konstanten Wert oder einen anderen-Eigenschaft und gibt **true** vergleicht, ob die Werte nicht identisch sind.</span><span class="sxs-lookup"><span data-stu-id="4f34a-104">The **IsNotEqualTo** element represents a search expression that compares a property with either a constant value or another property and returns **true** if the values are not the same.</span></span> 
  
```xml
<IsNotEqualTo>
   <FieldURI/>
   <FieldURIOrConstant/>
</IsNotEqualTo>
```

 <span data-ttu-id="4f34a-105">**IsNotEqualToType**</span><span class="sxs-lookup"><span data-stu-id="4f34a-105">**IsNotEqualToType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4f34a-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="4f34a-106">Attributes and elements</span></span>

<span data-ttu-id="4f34a-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="4f34a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4f34a-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="4f34a-108">Attributes</span></span>

<span data-ttu-id="4f34a-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="4f34a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4f34a-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4f34a-110">Child elements</span></span>

|<span data-ttu-id="4f34a-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="4f34a-111">**Element**</span></span>|<span data-ttu-id="4f34a-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4f34a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4f34a-113">FieldURI</span><span class="sxs-lookup"><span data-stu-id="4f34a-113">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="4f34a-114">Identifiziert die Eigenschaften von URI häufig verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="4f34a-114">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="4f34a-115">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="4f34a-115">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="4f34a-116">Einzelne Elemente eines Wörterbuchs identifiziert.</span><span class="sxs-lookup"><span data-stu-id="4f34a-116">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="4f34a-117">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="4f34a-117">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="4f34a-118">MAPI-Eigenschaften identifiziert.</span><span class="sxs-lookup"><span data-stu-id="4f34a-118">Identifies MAPI properties.</span></span>  <br/> |
|[<span data-ttu-id="4f34a-119">FieldURIOrConstant</span><span class="sxs-lookup"><span data-stu-id="4f34a-119">FieldURIOrConstant</span></span>](fielduriorconstant.md) <br/> |<span data-ttu-id="4f34a-120">Stellt eine Eigenschaft oder einen konstanten Wert dar, der beim Vergleich mit einer anderen Eigenschaft verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4f34a-120">Represents either a property or a constant value to be used when comparing with another property.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4f34a-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4f34a-121">Parent elements</span></span>

|<span data-ttu-id="4f34a-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="4f34a-122">**Element**</span></span>|<span data-ttu-id="4f34a-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4f34a-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4f34a-124">Einschränkung</span><span class="sxs-lookup"><span data-stu-id="4f34a-124">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="4f34a-125">Stellt die Einschränkung oder die Abfrage, die zum Filtern von Elementen oder Ordner in FindItem/FindFolder, und suchen Sie Ordner Vorgänge verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4f34a-125">Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span>  <br/> |
|[<span data-ttu-id="4f34a-126">not</span><span class="sxs-lookup"><span data-stu-id="4f34a-126">Not</span></span>](not.md) <br/> |<span data-ttu-id="4f34a-127">Stellt einen Search-Ausdruck, der den booleschen Wert des Suchbegriffs negiert, die er enthält.</span><span class="sxs-lookup"><span data-stu-id="4f34a-127">Represents a search expression that negates the Boolean value of the search expression that it contains.</span></span>  <br/> |
|[<span data-ttu-id="4f34a-128">Und</span><span class="sxs-lookup"><span data-stu-id="4f34a-128">And</span></span>](and.md) <br/> |<span data-ttu-id="4f34a-129">Stellt einen Search-Ausdruck, der Sie einen Vorgang vom Typ Boolean und zwischen zwei oder mehr Suchausdrücke ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="4f34a-129">Represents a search expression that allows you to perform a Boolean And operation between two or more search expressions.</span></span> <span data-ttu-id="4f34a-130">Das Ergebnis der And-Operation ist **true** , wenn **alle enthaltenen das And Search Ausdrücke zutreffen**.</span><span class="sxs-lookup"><span data-stu-id="4f34a-130">The result of the And operation is **true** if all of the search expressions contained within the And are **true**.</span></span>  <br/> |
|[<span data-ttu-id="4f34a-131">- oder -</span><span class="sxs-lookup"><span data-stu-id="4f34a-131">Or</span></span>](or.md) <br/> |<span data-ttu-id="4f34a-132">Stellt ein Suchbegriff, der ein logisches OR Suchbegriffs durchführt, die er enthält.</span><span class="sxs-lookup"><span data-stu-id="4f34a-132">Represents a search expression that performs a logical OR on the search expression that it contains.</span></span> <span data-ttu-id="4f34a-133">[Oder](or.md) gibt **true** zurück, wenn einer der untergeordneten **true**zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4f34a-133">[Or](or.md) will return **true** if any of its children return **true**.</span></span> <span data-ttu-id="4f34a-134">**Oder** muss mindestens zwei untergeordnete Elemente aufweisen.</span><span class="sxs-lookup"><span data-stu-id="4f34a-134">**Or** must have two or more children.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4f34a-135">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4f34a-135">Remarks</span></span>

<span data-ttu-id="4f34a-136">Zeichenfolgenvergleiche ausgeführt werden, erwägen Sie das Element [enthält](contains.md) , wie sie Optionen für übereinstimmende Parameter wie Groß-/Kleinschreibung und Leerzeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="4f34a-136">To perform string comparisons, consider using the [Contains](contains.md) element, as it provides options for matching parameters such as case and white space.</span></span> <span data-ttu-id="4f34a-137">Verwenden Sie das Element [nicht](not.md) in Verbindung mit dem [Contains](contains.md) -Element, um das Ergebnis zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="4f34a-137">Use the [Not](not.md) element in conjunction with the [Contains](contains.md) element to negate the result.</span></span> 
  
<span data-ttu-id="4f34a-138">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="4f34a-138">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4f34a-139">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="4f34a-139">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4f34a-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="4f34a-140">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4f34a-141">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="4f34a-141">Schema Name</span></span>  <br/> |<span data-ttu-id="4f34a-142">Schematypen</span><span class="sxs-lookup"><span data-stu-id="4f34a-142">Types schema</span></span>  <br/> |
|<span data-ttu-id="4f34a-143">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="4f34a-143">Validation File</span></span>  <br/> |<span data-ttu-id="4f34a-144">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4f34a-144">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4f34a-145">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="4f34a-145">Can be Empty</span></span>  <br/> |<span data-ttu-id="4f34a-146">False</span><span class="sxs-lookup"><span data-stu-id="4f34a-146">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4f34a-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4f34a-147">See also</span></span>



- [<span data-ttu-id="4f34a-148">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="4f34a-148">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

