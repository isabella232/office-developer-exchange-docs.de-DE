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
description: Das IsLessThanOrEqualTo-Element darstellt, die mit entweder einen konstanten Wert einer Eigenschaft oder eine andere Eigenschaft vergleicht und gibt true, wenn die erste Eigenschaft kleiner als oder gleich dem zweiten ist Suchbegriff.
ms.openlocfilehash: 9aeb688ec68e13635ac3083119899bcd55045f7a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830043"
---
# <a name="islessthanorequalto"></a><span data-ttu-id="70002-103">IsLessThanOrEqualTo</span><span class="sxs-lookup"><span data-stu-id="70002-103">IsLessThanOrEqualTo</span></span>

<span data-ttu-id="70002-104">Das **IsLessThanOrEqualTo** -Element darstellt, die vergleicht eine Eigenschaft mit einen konstanten Wert oder einen anderen-Eigenschaft und gibt **true,** Wenn die erste Eigenschaft kleiner als oder gleich dem zweiten ist Suchbegriff.</span><span class="sxs-lookup"><span data-stu-id="70002-104">The **IsLessThanOrEqualTo** element represents a search expression that compares a property with either a constant value or another property and returns **true** if the first property is less than or equal to the second.</span></span> 
  
```xml
<IsLessThanOrEqualTo>
   <FieldURI/>
   <FieldURIOrConstant/>
</IsLessThanOrEqualTo>
```

 <span data-ttu-id="70002-105">**IsLessThanOrEqualToType**</span><span class="sxs-lookup"><span data-stu-id="70002-105">**IsLessThanOrEqualToType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="70002-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="70002-106">Attributes and elements</span></span>

<span data-ttu-id="70002-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="70002-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="70002-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="70002-108">Attributes</span></span>

<span data-ttu-id="70002-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="70002-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="70002-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="70002-110">Child elements</span></span>

|<span data-ttu-id="70002-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="70002-111">**Element**</span></span>|<span data-ttu-id="70002-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="70002-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="70002-113">FieldURI</span><span class="sxs-lookup"><span data-stu-id="70002-113">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="70002-114">Identifiziert die Eigenschaften von URI häufig verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="70002-114">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="70002-115">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="70002-115">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="70002-116">Einzelne Elemente eines Wörterbuchs identifiziert.</span><span class="sxs-lookup"><span data-stu-id="70002-116">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="70002-117">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="70002-117">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="70002-118">MAPI-Eigenschaften identifiziert.</span><span class="sxs-lookup"><span data-stu-id="70002-118">Identifies MAPI properties.</span></span>  <br/> |
|[<span data-ttu-id="70002-119">FieldURIOrConstant</span><span class="sxs-lookup"><span data-stu-id="70002-119">FieldURIOrConstant</span></span>](fielduriorconstant.md) <br/> |<span data-ttu-id="70002-120">Stellt eine Eigenschaft oder einen konstanten Wert dar, der beim Vergleich mit einer anderen Eigenschaft verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="70002-120">Represents either a property or a constant value to be used when comparing with another property.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="70002-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="70002-121">Parent elements</span></span>

|<span data-ttu-id="70002-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="70002-122">**Element**</span></span>|<span data-ttu-id="70002-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="70002-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="70002-124">Einschränkung</span><span class="sxs-lookup"><span data-stu-id="70002-124">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="70002-125">Stellt die Einschränkung oder die Abfrage, die zum Filtern von Elementen oder Ordner in FindItem/FindFolder, und suchen Sie Ordner Vorgänge verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="70002-125">Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span>  <br/> |
|[<span data-ttu-id="70002-126">not</span><span class="sxs-lookup"><span data-stu-id="70002-126">Not</span></span>](not.md) <br/> |<span data-ttu-id="70002-127">Stellt einen Search-Ausdruck, der den booleschen Wert des Suchbegriffs negiert darin enthaltenen dar.</span><span class="sxs-lookup"><span data-stu-id="70002-127">Represents a search expression that negates the Boolean value of the search expression it contains.</span></span>  <br/> |
|[<span data-ttu-id="70002-128">Und</span><span class="sxs-lookup"><span data-stu-id="70002-128">And</span></span>](and.md) <br/> |<span data-ttu-id="70002-129">Stellt einen Search-Ausdruck, der Sie einen Vorgang vom Typ Boolean und zwischen zwei oder mehr Suchausdrücke ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="70002-129">Represents a search expression that enables you to perform a Boolean And operation between two or more search expressions.</span></span> <span data-ttu-id="70002-130">Das Ergebnis der And-Operation ist **true** , wenn **alle enthaltenen das And Search Ausdrücke zutreffen**.</span><span class="sxs-lookup"><span data-stu-id="70002-130">The result of the And operation is **true** if all of the search expressions contained within the And are **true**.</span></span>  <br/> |
|[<span data-ttu-id="70002-131">- oder -</span><span class="sxs-lookup"><span data-stu-id="70002-131">Or</span></span>](or.md) <br/> |<span data-ttu-id="70002-132">Stellt einen Suche Ausdruck, der ein logisches OR Suchbegriffs durchführt darin enthaltenen dar.</span><span class="sxs-lookup"><span data-stu-id="70002-132">Represents a search expression that performs a logical OR on the search expression it contains.</span></span> <span data-ttu-id="70002-133">[Oder](or.md) gibt **true** zurück, wenn einer der untergeordneten true zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="70002-133">[Or](or.md) will return **true** if any of its children return true.</span></span> <span data-ttu-id="70002-134">[Oder](or.md) muss mindestens zwei untergeordnete Elemente aufweisen.</span><span class="sxs-lookup"><span data-stu-id="70002-134">[Or](or.md) must have two or more children.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="70002-135">Hinweise</span><span class="sxs-lookup"><span data-stu-id="70002-135">Remarks</span></span>

<span data-ttu-id="70002-136">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="70002-136">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="70002-137">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="70002-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="70002-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="70002-138">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="70002-139">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="70002-139">Schema Name</span></span>  <br/> |<span data-ttu-id="70002-140">Schematypen</span><span class="sxs-lookup"><span data-stu-id="70002-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="70002-141">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="70002-141">Validation File</span></span>  <br/> |<span data-ttu-id="70002-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="70002-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="70002-143">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="70002-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="70002-144">False</span><span class="sxs-lookup"><span data-stu-id="70002-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="70002-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="70002-145">See also</span></span>



- [<span data-ttu-id="70002-146">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="70002-146">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

