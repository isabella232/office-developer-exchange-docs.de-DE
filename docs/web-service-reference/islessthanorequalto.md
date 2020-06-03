---
title: IsLessThanOrEqualTo
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsLessThanOrEqualTo
api_type:
- schema
ms.assetid: b5d85eb2-5e15-4d01-ad49-6289e735ad8a
description: Das IsLessThanOrEqualTo-Element stellt einen Suchausdruck dar, der eine Eigenschaft mit einem konstanten Wert oder einer anderen Eigenschaft vergleicht und true zurückgibt, wenn die erste Eigenschaft kleiner oder gleich der zweiten ist.
ms.openlocfilehash: 7b153803b1c895c86e74428468c8e592c02a0acc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530029"
---
# <a name="islessthanorequalto"></a><span data-ttu-id="7b57d-103">IsLessThanOrEqualTo</span><span class="sxs-lookup"><span data-stu-id="7b57d-103">IsLessThanOrEqualTo</span></span>

<span data-ttu-id="7b57d-104">Das **IsLessThanOrEqualTo** -Element stellt einen Suchausdruck dar, der eine Eigenschaft mit einem konstanten Wert oder einer anderen Eigenschaft vergleicht und **true** zurückgibt, wenn die erste Eigenschaft kleiner oder gleich der zweiten ist.</span><span class="sxs-lookup"><span data-stu-id="7b57d-104">The **IsLessThanOrEqualTo** element represents a search expression that compares a property with either a constant value or another property and returns **true** if the first property is less than or equal to the second.</span></span> 
  
```xml
<IsLessThanOrEqualTo>
   <FieldURI/>
   <FieldURIOrConstant/>
</IsLessThanOrEqualTo>
```

```xml
<IsLessThanOrEqualTo>
   <IndexedFieldURI/> 
   <FieldURIOrConstant/>
</IsLessThanOrEqualTo>
```

```xml
<IsLessThanOrEqualTo>
   <ExtendedFieldURI/> 
   <FieldURIOrConstant/>
</IsLessThanOrEqualTo>
```

<span data-ttu-id="7b57d-105">**IsLessThanOrEqualToType**</span><span class="sxs-lookup"><span data-stu-id="7b57d-105">**IsLessThanOrEqualToType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="7b57d-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="7b57d-106">Attributes and elements</span></span>

<span data-ttu-id="7b57d-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="7b57d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7b57d-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="7b57d-108">Attributes</span></span>

<span data-ttu-id="7b57d-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="7b57d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7b57d-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7b57d-110">Child elements</span></span>

|<span data-ttu-id="7b57d-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="7b57d-111">**Element**</span></span>|<span data-ttu-id="7b57d-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7b57d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7b57d-113">FieldURI</span><span class="sxs-lookup"><span data-stu-id="7b57d-113">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="7b57d-114">Identifiziert häufig referenzierte Eigenschaften nach URI.</span><span class="sxs-lookup"><span data-stu-id="7b57d-114">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="7b57d-115">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="7b57d-115">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="7b57d-116">Identifiziert einzelne Member eines Wörterbuchs.</span><span class="sxs-lookup"><span data-stu-id="7b57d-116">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="7b57d-117">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="7b57d-117">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="7b57d-118">Identifiziert MAPI-Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7b57d-118">Identifies MAPI properties.</span></span>  <br/> |
|[<span data-ttu-id="7b57d-119">FieldURIOrConstant</span><span class="sxs-lookup"><span data-stu-id="7b57d-119">FieldURIOrConstant</span></span>](fielduriorconstant.md) <br/> |<span data-ttu-id="7b57d-120">Stellt eine Eigenschaft oder einen konstanten Wert dar, der beim Vergleich mit einer anderen Eigenschaft verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7b57d-120">Represents either a property or a constant value to be used when comparing with another property.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7b57d-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7b57d-121">Parent elements</span></span>

|<span data-ttu-id="7b57d-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="7b57d-122">**Element**</span></span>|<span data-ttu-id="7b57d-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7b57d-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7b57d-124">Einschränkung</span><span class="sxs-lookup"><span data-stu-id="7b57d-124">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="7b57d-125">Stellt die Einschränkung oder Abfrage dar, die zum Filtern von Elementen oder Ordnern in FindItem/FindFolder und Suchordner Vorgängen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7b57d-125">Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span>  <br/> |
|[<span data-ttu-id="7b57d-126">not</span><span class="sxs-lookup"><span data-stu-id="7b57d-126">Not</span></span>](not.md) <br/> |<span data-ttu-id="7b57d-127">Stellt einen Suchausdruck dar, der den booleschen Wert des darin enthaltenen Suchausdrucks negiert.</span><span class="sxs-lookup"><span data-stu-id="7b57d-127">Represents a search expression that negates the Boolean value of the search expression it contains.</span></span>  <br/> |
|[<span data-ttu-id="7b57d-128">Und</span><span class="sxs-lookup"><span data-stu-id="7b57d-128">And</span></span>](and.md) <br/> |<span data-ttu-id="7b57d-129">Stellt einen Suchausdruck dar, mit dem Sie einen booleschen Wert und eine Operation zwischen zwei oder mehr Suchausdrücken ausführen können.</span><span class="sxs-lookup"><span data-stu-id="7b57d-129">Represents a search expression that enables you to perform a Boolean And operation between two or more search expressions.</span></span> <span data-ttu-id="7b57d-130">Das Ergebnis der and-Operation ist **true** , wenn alle in der enthaltenen Suchausdrücke auf **true**festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="7b57d-130">The result of the And operation is **true** if all of the search expressions contained within the And are **true**.</span></span>  <br/> |
|[<span data-ttu-id="7b57d-131">- oder -</span><span class="sxs-lookup"><span data-stu-id="7b57d-131">Or</span></span>](or.md) <br/> |<span data-ttu-id="7b57d-132">Stellt einen Suchausdruck dar, der eine logische OR-Anweisung für den darin enthaltenen Suchausdruck ausführt.</span><span class="sxs-lookup"><span data-stu-id="7b57d-132">Represents a search expression that performs a logical OR on the search expression it contains.</span></span> <span data-ttu-id="7b57d-133">[Oder](or.md) gibt **true** zurück, wenn eines der untergeordneten Elemente true zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="7b57d-133">[Or](or.md) will return **true** if any of its children return true.</span></span> <span data-ttu-id="7b57d-134">[Oder](or.md) muss mindestens zwei untergeordnete Elemente aufweisen.</span><span class="sxs-lookup"><span data-stu-id="7b57d-134">[Or](or.md) must have two or more children.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7b57d-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7b57d-135">Remarks</span></span>

<span data-ttu-id="7b57d-136">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="7b57d-136">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7b57d-137">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="7b57d-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7b57d-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="7b57d-138">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7b57d-139">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="7b57d-139">Schema Name</span></span>  <br/> |<span data-ttu-id="7b57d-140">Schematypen</span><span class="sxs-lookup"><span data-stu-id="7b57d-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="7b57d-141">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="7b57d-141">Validation File</span></span>  <br/> |<span data-ttu-id="7b57d-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7b57d-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7b57d-143">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="7b57d-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="7b57d-144">False</span><span class="sxs-lookup"><span data-stu-id="7b57d-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7b57d-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7b57d-145">See also</span></span>

- [<span data-ttu-id="7b57d-146">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="7b57d-146">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

