---
title: Und
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- And
api_type:
- schema
ms.assetid: 790246c2-37ad-49a8-91b9-6186d743b011
description: Das Element und stellt einen Search-Ausdruck, der Sie einen Vorgang vom Typ Boolean und zwischen zwei oder mehr Suchausdrücke ausführen kann. Das Ergebnis der AND-Operation ist True, wenn alle dem And-Element enthaltenen Suchausdrücke zutreffen.
ms.openlocfilehash: d287d57d68aeca7127325dc8fb65fd0190e5b5eb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757265"
---
# <a name="and"></a><span data-ttu-id="eae4b-104">Und</span><span class="sxs-lookup"><span data-stu-id="eae4b-104">And</span></span>

<span data-ttu-id="eae4b-105">Das Element **und** stellt einen Search-Ausdruck, der eine Boolean **und** -Operation zwischen zwei oder mehr Suchausdrücke ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="eae4b-105">The **And** element represents a search expression that allows you to perform a Boolean **AND** operation between two or more search expressions.</span></span> <span data-ttu-id="eae4b-106">Das Ergebnis der **AND** -Operation ist **true** , wenn **alle enthaltenen das Element **und** Suchausdrücke zutreffen**.</span><span class="sxs-lookup"><span data-stu-id="eae4b-106">The result of the **AND** operation is **true** if all the search expressions contained within the **And** element are **true**.</span></span>
  
```xml
<And>
   <SearchExpression/>
   <SearchExpression/>
</And>
```

 <span data-ttu-id="eae4b-107">**AndType**</span><span class="sxs-lookup"><span data-stu-id="eae4b-107">**AndType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="eae4b-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="eae4b-108">Attributes and elements</span></span>

<span data-ttu-id="eae4b-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="eae4b-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="eae4b-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="eae4b-110">Attributes</span></span>

<span data-ttu-id="eae4b-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="eae4b-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="eae4b-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="eae4b-112">Child elements</span></span>

|<span data-ttu-id="eae4b-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="eae4b-113">**Element**</span></span>|<span data-ttu-id="eae4b-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="eae4b-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="eae4b-115">SearchExpression</span><span class="sxs-lookup"><span data-stu-id="eae4b-115">SearchExpression</span></span>](searchexpression.md) <br/> | <span data-ttu-id="eae4b-116">Stellt die Basisklasse für Ausdrücke innerhalb einer Einschränkung dar.</span><span class="sxs-lookup"><span data-stu-id="eae4b-116">Represents the base class for expressions within a restriction.</span></span> <span data-ttu-id="eae4b-117">Es muss mindestens zwei Suchausdrücke in eine And-Operation.</span><span class="sxs-lookup"><span data-stu-id="eae4b-117">There must be two or more search expressions in an And operation.</span></span><br/><br/>  <span data-ttu-id="eae4b-118">Eines der folgenden Elemente muss für das Element **SearchExpression** ersetzt werden:</span><span class="sxs-lookup"><span data-stu-id="eae4b-118">One of the following elements must be substituted for the **SearchExpression** element:</span></span><ul><li> [<span data-ttu-id="eae4b-119">Exists</span><span class="sxs-lookup"><span data-stu-id="eae4b-119">Exists</span></span>](exists.md)</li><li>[<span data-ttu-id="eae4b-120">Schließt</span><span class="sxs-lookup"><span data-stu-id="eae4b-120">Excludes</span></span>](excludes.md)</li><li>[<span data-ttu-id="eae4b-121">"IsEqualTo"</span><span class="sxs-lookup"><span data-stu-id="eae4b-121">IsEqualTo</span></span>](isequalto.md)</li><li>[<span data-ttu-id="eae4b-122">IsNotEqualTo</span><span class="sxs-lookup"><span data-stu-id="eae4b-122">IsNotEqualTo</span></span>](isnotequalto.md)</li><li>[<span data-ttu-id="eae4b-123">IsGreaterThan</span><span class="sxs-lookup"><span data-stu-id="eae4b-123">IsGreaterThan</span></span>](isgreaterthan.md)</li><li>[<span data-ttu-id="eae4b-124">IsGreaterThanOrEqualTo</span><span class="sxs-lookup"><span data-stu-id="eae4b-124">IsGreaterThanOrEqualTo</span></span>](isgreaterthanorequalto.md)</li><li>[<span data-ttu-id="eae4b-125">IsLessThan</span><span class="sxs-lookup"><span data-stu-id="eae4b-125">IsLessThan</span></span>](islessthan.md)</li><li>[<span data-ttu-id="eae4b-126">IsLessThanOrEqualTo</span><span class="sxs-lookup"><span data-stu-id="eae4b-126">IsLessThanOrEqualTo</span></span>](islessthanorequalto.md)</li><li>[<span data-ttu-id="eae4b-127">Enthält</span><span class="sxs-lookup"><span data-stu-id="eae4b-127">Contains</span></span>](contains.md)</li><li>[<span data-ttu-id="eae4b-128">not</span><span class="sxs-lookup"><span data-stu-id="eae4b-128">Not</span></span>](not.md)</li><li><span data-ttu-id="eae4b-129">**Und**</span><span class="sxs-lookup"><span data-stu-id="eae4b-129">**And**</span></span></li><li>[<span data-ttu-id="eae4b-130">- oder -</span><span class="sxs-lookup"><span data-stu-id="eae4b-130">Or</span></span>](or.md) </li></ul> |
   
### <a name="parent-elements"></a><span data-ttu-id="eae4b-131">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="eae4b-131">Parent elements</span></span>

|<span data-ttu-id="eae4b-132">**Element**</span><span class="sxs-lookup"><span data-stu-id="eae4b-132">**Element**</span></span>|<span data-ttu-id="eae4b-133">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="eae4b-133">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="eae4b-134">Einschränkung</span><span class="sxs-lookup"><span data-stu-id="eae4b-134">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="eae4b-135">Stellt die Einschränkung oder die Abfrage, die zum Filtern von Elementen oder Ordner in FindItem/FindFolder, und suchen Sie Ordner Vorgänge verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="eae4b-135">Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span>  <br/> |
|[<span data-ttu-id="eae4b-136">not</span><span class="sxs-lookup"><span data-stu-id="eae4b-136">Not</span></span>](not.md) <br/> |<span data-ttu-id="eae4b-137">Stellt einen Search-Ausdruck, der den booleschen Wert des Suchbegriffs negiert, die er enthält.</span><span class="sxs-lookup"><span data-stu-id="eae4b-137">Represents a search expression that negates the Boolean value of the search expression that it contains.</span></span>  <br/> |
|<span data-ttu-id="eae4b-138">**Und**</span><span class="sxs-lookup"><span data-stu-id="eae4b-138">**And**</span></span> <br/> |<span data-ttu-id="eae4b-139">Stellt einen Search-Ausdruck, der eine Boolean **und** -Operation zwischen zwei oder mehr Suchausdrücke ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="eae4b-139">Represents a search expression that allows you to perform a Boolean **AND** operation between two or more search expressions.</span></span> <span data-ttu-id="eae4b-140">Das Ergebnis der **AND** -Operation ist **true** , wenn **Alle Suchausdrücke **und** -Element enthaltenen zutreffen**.</span><span class="sxs-lookup"><span data-stu-id="eae4b-140">The result of the **AND** operation is **true** if all of the search expressions contained within the **And** element are **true**.</span></span>  <br/> |
|[<span data-ttu-id="eae4b-141">- oder -</span><span class="sxs-lookup"><span data-stu-id="eae4b-141">Or</span></span>](or.md) <br/> |<span data-ttu-id="eae4b-142">Stellt einen Search-Ausdruck, der eine logische **OR** -Operation für den Suchbegriff durchführt, die er enthält.</span><span class="sxs-lookup"><span data-stu-id="eae4b-142">Represents a search expression that performs a logical **OR** operation on the search expression that it contains.</span></span> <span data-ttu-id="eae4b-143">**Oder** gibt **true** zurück, wenn einer der untergeordneten **true**zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="eae4b-143">**Or** will return **true** if any of its children return **true**.</span></span> <span data-ttu-id="eae4b-144">**Oder** muss mindestens zwei untergeordnete Elemente aufweisen.</span><span class="sxs-lookup"><span data-stu-id="eae4b-144">**Or** must have two or more children.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eae4b-145">Hinweise</span><span class="sxs-lookup"><span data-stu-id="eae4b-145">Remarks</span></span>

<span data-ttu-id="eae4b-146">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="eae4b-146">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="eae4b-147">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="eae4b-147">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="eae4b-148">Namespace</span><span class="sxs-lookup"><span data-stu-id="eae4b-148">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="eae4b-149">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="eae4b-149">Schema Name</span></span>  <br/> |<span data-ttu-id="eae4b-150">Schematypen</span><span class="sxs-lookup"><span data-stu-id="eae4b-150">Types schema</span></span>  <br/> |
|<span data-ttu-id="eae4b-151">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="eae4b-151">Validation File</span></span>  <br/> |<span data-ttu-id="eae4b-152">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="eae4b-152">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="eae4b-153">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="eae4b-153">Can be Empty</span></span>  <br/> |<span data-ttu-id="eae4b-154">False</span><span class="sxs-lookup"><span data-stu-id="eae4b-154">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="eae4b-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eae4b-155">See also</span></span>

- [<span data-ttu-id="eae4b-156">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="eae4b-156">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

