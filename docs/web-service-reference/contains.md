---
title: Enthält
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Contains
api_type:
- schema
ms.assetid: 476d059d-c243-43e9-b475-319fc413ade2
description: Das Contains-Element stellt einen Search-Ausdruck, der bestimmt, ob eine bestimmte Eigenschaft den angegebenen Konstante String-Wert enthält.
ms.openlocfilehash: b25b69aadf2c331527a17ad81ed46f61aa7b93c2
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2018
ms.locfileid: "21354288"
---
# <a name="contains"></a><span data-ttu-id="9b3b1-103">Enthält</span><span class="sxs-lookup"><span data-stu-id="9b3b1-103">Contains</span></span>

<span data-ttu-id="9b3b1-104">Das **Contains** -Element stellt einen Search-Ausdruck, der bestimmt, ob eine bestimmte Eigenschaft den angegebenen Konstante String-Wert enthält.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-104">The **Contains** element represents a search expression that determines whether a given property contains the supplied constant string value.</span></span> 
  
```xml
<Contains ContainmentMode="" ContainmentComparison="">
   <FieldURI/>
   <Constant/>
</Contains>
```

```xml
<Contains ContainmentMode="" ContainmentComparison="">
   <ExtendedFieldURI/>
   <Constant/>
</Contains>
```

```xml
<Contains ContainmentMode="" ContainmentComparison="">
   <IndexedFieldURI/>
   <Constant/>
</Contains>
```


<span data-ttu-id="9b3b1-105">**ContainsExpressionType**</span><span class="sxs-lookup"><span data-stu-id="9b3b1-105">**ContainsExpressionType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="9b3b1-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="9b3b1-106">Attributes and elements</span></span>

<span data-ttu-id="9b3b1-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9b3b1-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="9b3b1-108">Attributes</span></span>

|<span data-ttu-id="9b3b1-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="9b3b1-109">**Attribute**</span></span>|<span data-ttu-id="9b3b1-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9b3b1-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9b3b1-111">**ContainmentMode**</span><span class="sxs-lookup"><span data-stu-id="9b3b1-111">**ContainmentMode**</span></span> <br/> |<span data-ttu-id="9b3b1-112">Identifiziert die Grenzen einer Suche an.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-112">Identifies the boundaries of a search.</span></span>  <br/> |
|<span data-ttu-id="9b3b1-113">**ContainmentComparison**</span><span class="sxs-lookup"><span data-stu-id="9b3b1-113">**ContainmentComparison**</span></span> <br/> |<span data-ttu-id="9b3b1-114">Bestimmt, ob die Suche Anfragen und Leerzeichen werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-114">Determines whether the search ignores cases and spaces.</span></span>  <br/> |
   
#### <a name="containmentmode-attribute-values"></a><span data-ttu-id="9b3b1-115">Attributwerte ContainmentMode</span><span class="sxs-lookup"><span data-stu-id="9b3b1-115">ContainmentMode attribute values</span></span>

|<span data-ttu-id="9b3b1-116">**Wert**</span><span class="sxs-lookup"><span data-stu-id="9b3b1-116">**Value**</span></span>|<span data-ttu-id="9b3b1-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9b3b1-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9b3b1-118">FullString</span><span class="sxs-lookup"><span data-stu-id="9b3b1-118">FullString</span></span>  <br/> |<span data-ttu-id="9b3b1-119">Vergleich wird zwischen der vollständigen Zeichenfolge sowie die Konstante.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-119">The comparison is between the full string and the constant.</span></span> <span data-ttu-id="9b3b1-120">Wert der Eigenschaft und die angegebene Konstante sind exakt identisch.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-120">The property value and the supplied constant are precisely the same.</span></span>  <br/> |
|<span data-ttu-id="9b3b1-121">Das Präfix</span><span class="sxs-lookup"><span data-stu-id="9b3b1-121">Prefixed</span></span>  <br/> |<span data-ttu-id="9b3b1-122">Vergleich wird zwischen dem Präfix Zeichenfolge sowie die Konstante.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-122">The comparison is between the string prefix and the constant.</span></span>  <br/> |
|<span data-ttu-id="9b3b1-123">Teilzeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9b3b1-123">Substring</span></span>  <br/> |<span data-ttu-id="9b3b1-124">Vergleich wird zwischen der Zeichenfolge eine Teilzeichenfolge sowie die Konstante.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-124">The comparison is between a substring of the string and the constant.</span></span>  <br/> |
|<span data-ttu-id="9b3b1-125">PrefixOnWords</span><span class="sxs-lookup"><span data-stu-id="9b3b1-125">PrefixOnWords</span></span>  <br/> |<span data-ttu-id="9b3b1-126">Vergleich wird zwischen einem Präfix auf einzelne Wörter in der Zeichenfolge und die Konstante die.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-126">The comparison is between a prefix on individual words in the string and the constant.</span></span>  <br/> |
|<span data-ttu-id="9b3b1-127">ExactPhrase</span><span class="sxs-lookup"><span data-stu-id="9b3b1-127">ExactPhrase</span></span>  <br/> |<span data-ttu-id="9b3b1-128">Vergleich wird zwischen einem exakten Wortlaut in der Zeichenfolge sowie die Konstante die.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-128">The comparison is between an exact phrase in the string and the constant.</span></span>  <br/> |
   
#### <a name="containmentcomparison-attribute-values"></a><span data-ttu-id="9b3b1-129">Attributwerte ContainmentComparison</span><span class="sxs-lookup"><span data-stu-id="9b3b1-129">ContainmentComparison attribute values</span></span>

|<span data-ttu-id="9b3b1-130">**Wert**</span><span class="sxs-lookup"><span data-stu-id="9b3b1-130">**Value**</span></span>|<span data-ttu-id="9b3b1-131">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9b3b1-131">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9b3b1-132">Exact</span><span class="sxs-lookup"><span data-stu-id="9b3b1-132">Exact</span></span>  <br/> |<span data-ttu-id="9b3b1-133">Der Vergleich muss exakt sein.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-133">The comparison must be exact.</span></span>  <br/> |
|<span data-ttu-id="9b3b1-134">IgnoreCase</span><span class="sxs-lookup"><span data-stu-id="9b3b1-134">IgnoreCase</span></span>  <br/> |<span data-ttu-id="9b3b1-135">Der Vergleich wird zur Groß-und Kleinschreibung ignoriert.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-135">The comparison ignores casing.</span></span>  <br/> |
|<span data-ttu-id="9b3b1-136">IgnoreNonSpacingCharacters</span><span class="sxs-lookup"><span data-stu-id="9b3b1-136">IgnoreNonSpacingCharacters</span></span>  <br/> |<span data-ttu-id="9b3b1-137">Der Vergleich ignoriert nicht-gesperrte Zeichen.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-137">The comparison ignores non-spacing characters.</span></span>  <br/> |
|<span data-ttu-id="9b3b1-138">Weit</span><span class="sxs-lookup"><span data-stu-id="9b3b1-138">Loose</span></span>  <br/> |<span data-ttu-id="9b3b1-139">Entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-139">To be removed.</span></span>  <br/> |
|<span data-ttu-id="9b3b1-140">IgnoreCaseAndNonSpacingCharacters</span><span class="sxs-lookup"><span data-stu-id="9b3b1-140">IgnoreCaseAndNonSpacingCharacters</span></span>  <br/> |<span data-ttu-id="9b3b1-141">Der Vergleich wird die Groß-/Kleinschreibung sowie nicht-gesperrte Zeichen ignoriert.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-141">The comparison ignores casing and non-spacing characters.</span></span>  <br/> |
|<span data-ttu-id="9b3b1-142">LooseAndIgnoreCase</span><span class="sxs-lookup"><span data-stu-id="9b3b1-142">LooseAndIgnoreCase</span></span>  <br/> |<span data-ttu-id="9b3b1-143">Entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-143">To be removed.</span></span>  <br/> |
|<span data-ttu-id="9b3b1-144">LooseAndIgnoreNonSpace</span><span class="sxs-lookup"><span data-stu-id="9b3b1-144">LooseAndIgnoreNonSpace</span></span>  <br/> |<span data-ttu-id="9b3b1-145">Entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-145">To be removed.</span></span>  <br/> |
|<span data-ttu-id="9b3b1-146">LooseAndIgnoreCaseAndIgnoreNonSpace</span><span class="sxs-lookup"><span data-stu-id="9b3b1-146">LooseAndIgnoreCaseAndIgnoreNonSpace</span></span>  <br/> |<span data-ttu-id="9b3b1-147">Entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-147">To be removed.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9b3b1-148">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9b3b1-148">Child elements</span></span>

|<span data-ttu-id="9b3b1-149">**Element**</span><span class="sxs-lookup"><span data-stu-id="9b3b1-149">**Element**</span></span>|<span data-ttu-id="9b3b1-150">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9b3b1-150">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9b3b1-151">FieldURI</span><span class="sxs-lookup"><span data-stu-id="9b3b1-151">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="9b3b1-152">Identifiziert die Eigenschaften von URI häufig verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-152">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="9b3b1-153">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="9b3b1-153">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="9b3b1-154">Einzelne Elemente eines Wörterbuchs identifiziert.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-154">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="9b3b1-155">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="9b3b1-155">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="9b3b1-156">MAPI-Eigenschaften identifiziert.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-156">Identifies MAPI properties.</span></span>  <br/> |
|[<span data-ttu-id="9b3b1-157">Konstante</span><span class="sxs-lookup"><span data-stu-id="9b3b1-157">Constant</span></span>](constant.md) <br/> |<span data-ttu-id="9b3b1-158">Gibt einen konstanten Wert in einer Einschränkung.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-158">Identifies a constant value in a restriction.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9b3b1-159">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9b3b1-159">Parent elements</span></span>

|<span data-ttu-id="9b3b1-160">**Element**</span><span class="sxs-lookup"><span data-stu-id="9b3b1-160">**Element**</span></span>|<span data-ttu-id="9b3b1-161">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9b3b1-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9b3b1-162">Einschränkung</span><span class="sxs-lookup"><span data-stu-id="9b3b1-162">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="9b3b1-163">Stellt die Einschränkung oder die Abfrage, die zum Filtern von Elementen oder Ordner in FindItem/FindFolder, und suchen Sie Ordner Vorgänge verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-163">Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span>  <br/> |
|[<span data-ttu-id="9b3b1-164">not</span><span class="sxs-lookup"><span data-stu-id="9b3b1-164">Not</span></span>](not.md) <br/> |<span data-ttu-id="9b3b1-165">Stellt einen Search-Ausdruck, der den booleschen Wert des Suchbegriffs negiert darin enthaltenen dar.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-165">Represents a search expression that negates the Boolean value of the search expression it contains.</span></span>  <br/> |
|[<span data-ttu-id="9b3b1-166">Und</span><span class="sxs-lookup"><span data-stu-id="9b3b1-166">And</span></span>](and.md) <br/> |<span data-ttu-id="9b3b1-167">Stellt einen Search-Ausdruck, der Sie einen Vorgang vom Typ Boolean und zwischen zwei oder mehr Suchausdrücke ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-167">Represents a search expression that allows you to perform a Boolean And operation between two or more search expressions.</span></span> <span data-ttu-id="9b3b1-168">Das Ergebnis der And-Operation ist **true** , wenn **alle enthaltenen das And Search Ausdrücke zutreffen**.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-168">The result of the And operation is **true** if all of the search expressions contained within the And are **true**.</span></span>  <br/> |
|[<span data-ttu-id="9b3b1-169">- oder -</span><span class="sxs-lookup"><span data-stu-id="9b3b1-169">Or</span></span>](or.md) <br/> |<span data-ttu-id="9b3b1-170">Stellt einen Suche Ausdruck, der ein logisches OR Suchbegriffs durchführt darin enthaltenen dar.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-170">Represents a search expression that performs a logical OR on the search expression it contains.</span></span> <span data-ttu-id="9b3b1-171">Das Element [oder](or.md) gibt **true** zurück, wenn ein untergeordnetes Element **true**zurück.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-171">The [Or](or.md) element will return **true** if any of its children return **true**.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9b3b1-172">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9b3b1-172">Remarks</span></span>

<span data-ttu-id="9b3b1-173">Die Attribute werden verwendet, um zu bestimmen, wie die Elemente zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-173">The attributes are used to determine how the elements are matched.</span></span>
  
<span data-ttu-id="9b3b1-174">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="9b3b1-174">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9b3b1-175">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="9b3b1-175">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9b3b1-176">Namespace</span><span class="sxs-lookup"><span data-stu-id="9b3b1-176">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9b3b1-177">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="9b3b1-177">Schema Name</span></span>  <br/> |<span data-ttu-id="9b3b1-178">Schematypen</span><span class="sxs-lookup"><span data-stu-id="9b3b1-178">Types schema</span></span>  <br/> |
|<span data-ttu-id="9b3b1-179">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="9b3b1-179">Validation File</span></span>  <br/> |<span data-ttu-id="9b3b1-180">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9b3b1-180">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9b3b1-181">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="9b3b1-181">Can be Empty</span></span>  <br/> |<span data-ttu-id="9b3b1-182">False</span><span class="sxs-lookup"><span data-stu-id="9b3b1-182">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9b3b1-183">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9b3b1-183">See also</span></span>

- [<span data-ttu-id="9b3b1-184">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="9b3b1-184">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

