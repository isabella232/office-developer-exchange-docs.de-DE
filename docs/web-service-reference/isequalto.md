---
title: "\"IsEqualTo\""
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsEqualTo
api_type:
- schema
ms.assetid: 48e7e067-049c-4184-8026-071e6f558e8a
description: Das Element "IsEqualTo" stellt einen Search-Ausdruck, der mit entweder einen konstanten Wert einer Eigenschaft oder eine andere Eigenschaft vergleicht und wird zu True ausgewertet, falls diese gleich sind.
ms.openlocfilehash: a7a7deed79c271be74bb2ff16dd86605d468721b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830013"
---
# <a name="isequalto"></a><span data-ttu-id="c311b-103">"IsEqualTo"</span><span class="sxs-lookup"><span data-stu-id="c311b-103">IsEqualTo</span></span>

<span data-ttu-id="c311b-104">Das Element **"IsEqualTo"** stellt einen Search-Ausdruck, der mit entweder einen konstanten Wert einer Eigenschaft oder eine andere Eigenschaft vergleicht und wird zu True ausgewertet, falls diese gleich sind.</span><span class="sxs-lookup"><span data-stu-id="c311b-104">The **IsEqualTo** element represents a search expression that compares a property with either a constant value or another property and evaluates to true if they are equal.</span></span> 
  
```xml
<IsEqualTo>
   <FieldURI/>
   <FieldURIOrConstant/>
</IsEqualTo>
```

 <span data-ttu-id="c311b-105">**IsEqualToType**</span><span class="sxs-lookup"><span data-stu-id="c311b-105">**IsEqualToType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c311b-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c311b-106">Attributes and elements</span></span>

<span data-ttu-id="c311b-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c311b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c311b-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="c311b-108">Attributes</span></span>

<span data-ttu-id="c311b-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="c311b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c311b-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c311b-110">Child elements</span></span>

|<span data-ttu-id="c311b-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="c311b-111">**Element**</span></span>|<span data-ttu-id="c311b-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c311b-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c311b-113">FieldURI</span><span class="sxs-lookup"><span data-stu-id="c311b-113">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="c311b-114">Identifiziert die Eigenschaften von URI häufig verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="c311b-114">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="c311b-115">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="c311b-115">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="c311b-116">Einzelne Elemente eines Wörterbuchs identifiziert.</span><span class="sxs-lookup"><span data-stu-id="c311b-116">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="c311b-117">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="c311b-117">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="c311b-118">MAPI-Eigenschaften identifiziert.</span><span class="sxs-lookup"><span data-stu-id="c311b-118">Identifies MAPI properties.</span></span>  <br/> |
|[<span data-ttu-id="c311b-119">FieldURIOrConstant</span><span class="sxs-lookup"><span data-stu-id="c311b-119">FieldURIOrConstant</span></span>](fielduriorconstant.md) <br/> |<span data-ttu-id="c311b-120">Stellt eine Eigenschaft oder einen konstanten Wert dar, der beim Vergleich mit einer anderen Eigenschaft verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c311b-120">Represents either a property or a constant value to be used when comparing with another property.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c311b-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c311b-121">Parent elements</span></span>

|<span data-ttu-id="c311b-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="c311b-122">**Element**</span></span>|<span data-ttu-id="c311b-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c311b-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c311b-124">Einschränkung</span><span class="sxs-lookup"><span data-stu-id="c311b-124">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="c311b-125">Stellt die Einschränkung oder die Abfrage, die zum Filtern von Elementen oder Ordner in FindItem/FindFolder, und suchen Sie Ordner Vorgänge verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c311b-125">Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span>  <br/> |
|[<span data-ttu-id="c311b-126">not</span><span class="sxs-lookup"><span data-stu-id="c311b-126">Not</span></span>](not.md) <br/> |<span data-ttu-id="c311b-127">Stellt einen Search-Ausdruck, der den booleschen Wert des Suchbegriffs negiert, die er enthält.</span><span class="sxs-lookup"><span data-stu-id="c311b-127">Represents a search expression that negates the Boolean value of the search expression that it contains.</span></span>  <br/> |
|[<span data-ttu-id="c311b-128">Und</span><span class="sxs-lookup"><span data-stu-id="c311b-128">And</span></span>](and.md) <br/> |<span data-ttu-id="c311b-129">Stellt einen Search-Ausdruck, der Sie einen Vorgang vom Typ Boolean und zwischen zwei oder mehr Suchausdrücke ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="c311b-129">Represents a search expression that allows you to perform a Boolean And operation between two or more search expressions.</span></span> <span data-ttu-id="c311b-130">Das Ergebnis der And-Operation ist **true** , wenn **alle enthaltenen das And Search Ausdrücke zutreffen**.</span><span class="sxs-lookup"><span data-stu-id="c311b-130">The result of the And operation is **true** if all of the search expressions contained within the And are **true**.</span></span>  <br/> |
|[<span data-ttu-id="c311b-131">- oder -</span><span class="sxs-lookup"><span data-stu-id="c311b-131">Or</span></span>](or.md) <br/> |<span data-ttu-id="c311b-132">Stellt ein Suchbegriff, der ein logisches OR Suchbegriffs durchführt, die er enthält.</span><span class="sxs-lookup"><span data-stu-id="c311b-132">Represents a search expression that performs a logical OR on the search expression that it contains.</span></span> <span data-ttu-id="c311b-133">[Oder](or.md) wird true, wenn ein untergeordnetes Element true zurückgegeben werden, zurück.</span><span class="sxs-lookup"><span data-stu-id="c311b-133">[Or](or.md) will return true if any of its children return true.</span></span> <span data-ttu-id="c311b-134">**Oder** muss mindestens zwei untergeordnete Elemente aufweisen.</span><span class="sxs-lookup"><span data-stu-id="c311b-134">**Or** must have two or more children.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c311b-135">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c311b-135">Remarks</span></span>

<span data-ttu-id="c311b-136">Zeichenfolgenvergleiche ausgeführt werden, erwägen Sie das Element [enthält](contains.md) , wie sie Optionen für übereinstimmende Parameter, wie die Groß-/Kleinschreibung und Leerzeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="c311b-136">To perform string comparisons, consider using the [Contains](contains.md) element, as it provides options for matching parameters, such as case and white space.</span></span> <span data-ttu-id="c311b-137">Verwenden Sie das Element [nicht](not.md) in Verbindung mit dem [Contains](contains.md) -Element, um das Ergebnis zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="c311b-137">Use the [Not](not.md) element in conjunction with the [Contains](contains.md) element to negate the result.</span></span> 
  
<span data-ttu-id="c311b-138">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="c311b-138">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c311b-139">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="c311b-139">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c311b-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="c311b-140">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c311b-141">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c311b-141">Schema Name</span></span>  <br/> |<span data-ttu-id="c311b-142">Schematypen</span><span class="sxs-lookup"><span data-stu-id="c311b-142">Types schema</span></span>  <br/> |
|<span data-ttu-id="c311b-143">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c311b-143">Validation File</span></span>  <br/> |<span data-ttu-id="c311b-144">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c311b-144">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c311b-145">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="c311b-145">Can be Empty</span></span>  <br/> |<span data-ttu-id="c311b-146">False</span><span class="sxs-lookup"><span data-stu-id="c311b-146">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c311b-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c311b-147">See also</span></span>



- [<span data-ttu-id="c311b-148">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="c311b-148">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

