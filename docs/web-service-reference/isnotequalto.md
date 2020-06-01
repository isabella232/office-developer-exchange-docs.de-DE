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
description: Das IsNotEqualTo-Element stellt einen Suchausdruck dar, der eine Eigenschaft entweder mit einem konstanten Wert oder einer anderen Eigenschaft vergleicht und true zurückgibt, wenn die Werte nicht identisch sind.
ms.openlocfilehash: 8c40fd1ce8c7c1f14b70f4fccfd3a24e4c99f1b5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44464189"
---
# <a name="isnotequalto"></a><span data-ttu-id="ea5d5-103">IsNotEqualTo</span><span class="sxs-lookup"><span data-stu-id="ea5d5-103">IsNotEqualTo</span></span>

<span data-ttu-id="ea5d5-104">Das **IsNotEqualTo** -Element stellt einen Suchausdruck dar, der eine Eigenschaft entweder mit einem konstanten Wert oder einer anderen Eigenschaft vergleicht und **true** zurückgibt, wenn die Werte nicht identisch sind.</span><span class="sxs-lookup"><span data-stu-id="ea5d5-104">The **IsNotEqualTo** element represents a search expression that compares a property with either a constant value or another property and returns **true** if the values are not the same.</span></span> 
  
```xml
<IsNotEqualTo>
   <FieldURI/>
   <FieldURIOrConstant/>
</IsNotEqualTo>
```

```xml
<IsNotEqualTo>
   <ExtendedFieldURI/> 
   <FieldURIOrConstant/>
</IsNotEqualTo>
```

```xml
<IsNotEqualTo>
   <IndexedFieldURI/>
   <FieldURIOrConstant/>
</IsNotEqualTo>
```

<span data-ttu-id="ea5d5-105">**IsNotEqualToType**</span><span class="sxs-lookup"><span data-stu-id="ea5d5-105">**IsNotEqualToType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="ea5d5-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ea5d5-106">Attributes and elements</span></span>

<span data-ttu-id="ea5d5-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ea5d5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ea5d5-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="ea5d5-108">Attributes</span></span>

<span data-ttu-id="ea5d5-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="ea5d5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ea5d5-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ea5d5-110">Child elements</span></span>

|<span data-ttu-id="ea5d5-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="ea5d5-111">**Element**</span></span>|<span data-ttu-id="ea5d5-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ea5d5-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ea5d5-113">FieldURI</span><span class="sxs-lookup"><span data-stu-id="ea5d5-113">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="ea5d5-114">Identifiziert häufig referenzierte Eigenschaften nach URI.</span><span class="sxs-lookup"><span data-stu-id="ea5d5-114">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="ea5d5-115">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="ea5d5-115">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="ea5d5-116">Identifiziert einzelne Member eines Wörterbuchs.</span><span class="sxs-lookup"><span data-stu-id="ea5d5-116">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="ea5d5-117">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="ea5d5-117">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="ea5d5-118">Identifiziert MAPI-Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ea5d5-118">Identifies MAPI properties.</span></span>  <br/> |
|[<span data-ttu-id="ea5d5-119">FieldURIOrConstant</span><span class="sxs-lookup"><span data-stu-id="ea5d5-119">FieldURIOrConstant</span></span>](fielduriorconstant.md) <br/> |<span data-ttu-id="ea5d5-120">Stellt eine Eigenschaft oder einen konstanten Wert dar, der beim Vergleich mit einer anderen Eigenschaft verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ea5d5-120">Represents either a property or a constant value to be used when comparing with another property.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ea5d5-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ea5d5-121">Parent elements</span></span>

|<span data-ttu-id="ea5d5-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="ea5d5-122">**Element**</span></span>|<span data-ttu-id="ea5d5-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ea5d5-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ea5d5-124">Restriction</span><span class="sxs-lookup"><span data-stu-id="ea5d5-124">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="ea5d5-125">Stellt die Einschränkung oder Abfrage dar, die zum Filtern von Elementen oder Ordnern in FindItem/FindFolder und Suchordner Vorgängen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ea5d5-125">Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span>  <br/> |
|[<span data-ttu-id="ea5d5-126">Not</span><span class="sxs-lookup"><span data-stu-id="ea5d5-126">Not</span></span>](not.md) <br/> |<span data-ttu-id="ea5d5-127">Stellt einen Suchausdruck dar, der den booleschen Wert des darin enthaltenen Suchausdrucks negiert.</span><span class="sxs-lookup"><span data-stu-id="ea5d5-127">Represents a search expression that negates the Boolean value of the search expression that it contains.</span></span>  <br/> |
|[<span data-ttu-id="ea5d5-128">Und</span><span class="sxs-lookup"><span data-stu-id="ea5d5-128">And</span></span>](and.md) <br/> |<span data-ttu-id="ea5d5-129">Stellt einen Suchausdruck dar, mit dem Sie einen booleschen Wert und eine Operation zwischen zwei oder mehr Suchausdrücken ausführen können.</span><span class="sxs-lookup"><span data-stu-id="ea5d5-129">Represents a search expression that allows you to perform a Boolean And operation between two or more search expressions.</span></span> <span data-ttu-id="ea5d5-130">Das Ergebnis der and-Operation ist **true** , wenn alle in der enthaltenen Suchausdrücke auf **true**festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="ea5d5-130">The result of the And operation is **true** if all of the search expressions contained within the And are **true**.</span></span>  <br/> |
|[<span data-ttu-id="ea5d5-131">- oder -</span><span class="sxs-lookup"><span data-stu-id="ea5d5-131">Or</span></span>](or.md) <br/> |<span data-ttu-id="ea5d5-132">Stellt einen Suchausdruck dar, der einen logischen oder den darin enthaltenen Suchausdruck ausführt.</span><span class="sxs-lookup"><span data-stu-id="ea5d5-132">Represents a search expression that performs a logical OR on the search expression that it contains.</span></span> <span data-ttu-id="ea5d5-133">[Oder](or.md) gibt **true** zurück, wenn eines der untergeordneten Elemente **true**zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="ea5d5-133">[Or](or.md) will return **true** if any of its children return **true**.</span></span> <span data-ttu-id="ea5d5-134">**Oder** muss mindestens zwei untergeordnete Elemente aufweisen.</span><span class="sxs-lookup"><span data-stu-id="ea5d5-134">**Or** must have two or more children.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ea5d5-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ea5d5-135">Remarks</span></span>

<span data-ttu-id="ea5d5-136">Wenn Sie Zeichenfolgenvergleiche ausführen möchten, sollten Sie das [Contains](contains.md) -Element verwenden, da es Optionen zum Vergleichen von Parametern wie Groß-/Kleinschreibung und Leerzeichen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="ea5d5-136">To perform string comparisons, consider using the [Contains](contains.md) element, as it provides options for matching parameters such as case and white space.</span></span> <span data-ttu-id="ea5d5-137">Verwenden Sie das [Not](not.md) -Element in Verbindung mit dem [Contains](contains.md) -Element, um das Ergebnis zu negieren.</span><span class="sxs-lookup"><span data-stu-id="ea5d5-137">Use the [Not](not.md) element in conjunction with the [Contains](contains.md) element to negate the result.</span></span> 
  
<span data-ttu-id="ea5d5-138">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="ea5d5-138">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ea5d5-139">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="ea5d5-139">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ea5d5-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="ea5d5-140">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ea5d5-141">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ea5d5-141">Schema Name</span></span>  <br/> |<span data-ttu-id="ea5d5-142">Schematypen</span><span class="sxs-lookup"><span data-stu-id="ea5d5-142">Types schema</span></span>  <br/> |
|<span data-ttu-id="ea5d5-143">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ea5d5-143">Validation File</span></span>  <br/> |<span data-ttu-id="ea5d5-144">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ea5d5-144">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ea5d5-145">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="ea5d5-145">Can be Empty</span></span>  <br/> |<span data-ttu-id="ea5d5-146">False</span><span class="sxs-lookup"><span data-stu-id="ea5d5-146">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ea5d5-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ea5d5-147">See also</span></span>

- [<span data-ttu-id="ea5d5-148">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="ea5d5-148">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

