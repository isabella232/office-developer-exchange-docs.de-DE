---
title: IsGreaterThan
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsGreaterThan
api_type:
- schema
ms.assetid: a6e9d462-cfa7-40ec-903e-128c95050352
description: Das IsGreaterThan-Element stellt einen Search-Ausdruck, der mit entweder einen konstanten Wert einer Eigenschaft oder eine andere Eigenschaft vergleicht und gibt true, wenn die erste Eigenschaft größer ist.
ms.openlocfilehash: dfa7c221bb04e59f1ae12eeb5b9f2e1f09aea3ce
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353490"
---
# <a name="isgreaterthan"></a><span data-ttu-id="26681-103">IsGreaterThan</span><span class="sxs-lookup"><span data-stu-id="26681-103">IsGreaterThan</span></span>

<span data-ttu-id="26681-104">Das **IsGreaterThan** -Element stellt einen Search-Ausdruck, der eine Eigenschaft mit einem konstanten Wert oder einen anderen-Eigenschaft und gibt **true** vergleicht, ob die erste Eigenschaft größer ist.</span><span class="sxs-lookup"><span data-stu-id="26681-104">The **IsGreaterThan** element represents a search expression that compares a property with either a constant value or another property and returns **true** if the first property is greater.</span></span> 
  
```xml
<IsGreaterThan>
   <FieldURI/>
   <FieldURIOrConstant/>
</IsGreaterThan>
```

```xml
<IsGreaterThan>
   <IndexedFieldURI/> 
   <FieldURIOrConstant/>
</IsGreaterThan>
```

```xml
<IsGreaterThan>
   <ExtendedFieldURI/>
   <FieldURIOrConstant/>
</IsGreaterThan>
```

<span data-ttu-id="26681-105">**IsGreaterThanType**</span><span class="sxs-lookup"><span data-stu-id="26681-105">**IsGreaterThanType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="26681-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="26681-106">Attributes and elements</span></span>

<span data-ttu-id="26681-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="26681-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="26681-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="26681-108">Attributes</span></span>

<span data-ttu-id="26681-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="26681-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="26681-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="26681-110">Child elements</span></span>

|<span data-ttu-id="26681-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="26681-111">**Element**</span></span>|<span data-ttu-id="26681-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="26681-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="26681-113">FieldURI</span><span class="sxs-lookup"><span data-stu-id="26681-113">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="26681-114">Identifiziert die Eigenschaften von URI häufig verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="26681-114">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="26681-115">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="26681-115">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="26681-116">Einzelne Elemente eines Wörterbuchs identifiziert.</span><span class="sxs-lookup"><span data-stu-id="26681-116">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="26681-117">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="26681-117">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="26681-118">MAPI-Eigenschaften identifiziert.</span><span class="sxs-lookup"><span data-stu-id="26681-118">Identifies MAPI properties.</span></span>  <br/> |
|[<span data-ttu-id="26681-119">FieldURIOrConstant</span><span class="sxs-lookup"><span data-stu-id="26681-119">FieldURIOrConstant</span></span>](fielduriorconstant.md) <br/> |<span data-ttu-id="26681-120">Stellt eine Eigenschaft oder einen konstanten Wert dar, der beim Vergleich mit einer anderen Eigenschaft verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="26681-120">Represents either a property or a constant value to be used when comparing with another property.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="26681-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="26681-121">Parent elements</span></span>

|<span data-ttu-id="26681-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="26681-122">**Element**</span></span>|<span data-ttu-id="26681-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="26681-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="26681-124">Einschränkung</span><span class="sxs-lookup"><span data-stu-id="26681-124">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="26681-125">Stellt die Einschränkung oder die Abfrage, die zum Filtern von Elementen oder Ordner in FindItem/FindFolder, und suchen Sie Ordner Vorgänge verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="26681-125">Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span>  <br/> |
|[<span data-ttu-id="26681-126">not</span><span class="sxs-lookup"><span data-stu-id="26681-126">Not</span></span>](not.md) <br/> |<span data-ttu-id="26681-127">Stellt einen Search-Ausdruck, der den booleschen Wert des Suchbegriffs negiert, die er enthält.</span><span class="sxs-lookup"><span data-stu-id="26681-127">Represents a search expression that negates the Boolean value of the search expression that it contains.</span></span>  <br/> |
|[<span data-ttu-id="26681-128">Und</span><span class="sxs-lookup"><span data-stu-id="26681-128">And</span></span>](and.md) <br/> |<span data-ttu-id="26681-129">Stellt einen Search-Ausdruck, der Sie einen Vorgang vom Typ Boolean und zwischen zwei oder mehr Suchausdrücke ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="26681-129">Represents a search expression that enables you to perform a Boolean And operation between two or more search expressions.</span></span> <span data-ttu-id="26681-130">Das Ergebnis der And-Operation ist **true** , wenn **alle enthaltenen das And Suchausdrücke zutreffen**.</span><span class="sxs-lookup"><span data-stu-id="26681-130">The result of the And operation is **true** if all the search expressions contained within the And are **true**.</span></span>  <br/> |
|[<span data-ttu-id="26681-131">- oder -</span><span class="sxs-lookup"><span data-stu-id="26681-131">Or</span></span>](or.md) <br/> |<span data-ttu-id="26681-132">Stellt einen Suche Ausdruck, der ein logisches OR Suchbegriffs durchführt darin enthaltenen dar.</span><span class="sxs-lookup"><span data-stu-id="26681-132">Represents a search expression that performs a logical OR on the search expression it contains.</span></span> <span data-ttu-id="26681-133">[Oder](or.md) gibt **true** zurück, wenn einer der untergeordneten **true**zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="26681-133">[Or](or.md) will return **true** if any of its children return **true**.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="26681-134">Hinweise</span><span class="sxs-lookup"><span data-stu-id="26681-134">Remarks</span></span>

<span data-ttu-id="26681-135">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="26681-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="26681-136">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="26681-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="26681-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="26681-137">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="26681-138">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="26681-138">Schema Name</span></span>  <br/> |<span data-ttu-id="26681-139">Schematypen</span><span class="sxs-lookup"><span data-stu-id="26681-139">Types schema</span></span>  <br/> |
|<span data-ttu-id="26681-140">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="26681-140">Validation File</span></span>  <br/> |<span data-ttu-id="26681-141">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="26681-141">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="26681-142">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="26681-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="26681-143">False</span><span class="sxs-lookup"><span data-stu-id="26681-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="26681-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="26681-144">See also</span></span>

- [<span data-ttu-id="26681-145">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="26681-145">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

