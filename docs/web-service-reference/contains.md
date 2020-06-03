---
title: Contains
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
description: Das Contains-Element stellt einen Suchausdruck dar, der bestimmt, ob eine bestimmte Eigenschaft den angegebenen Konstanten Zeichenfolgenwert enthält.
ms.openlocfilehash: 79529bd752bcbce954ae3c8b0085c203b4eb8777
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527117"
---
# <a name="contains"></a><span data-ttu-id="9c0b8-103">Contains</span><span class="sxs-lookup"><span data-stu-id="9c0b8-103">Contains</span></span>

<span data-ttu-id="9c0b8-104">Das **Contains** -Element stellt einen Suchausdruck dar, der bestimmt, ob eine bestimmte Eigenschaft den angegebenen Konstanten Zeichenfolgenwert enthält.</span><span class="sxs-lookup"><span data-stu-id="9c0b8-104">The **Contains** element represents a search expression that determines whether a given property contains the supplied constant string value.</span></span> 
  
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


<span data-ttu-id="9c0b8-105">**ContainsExpressionType**</span><span class="sxs-lookup"><span data-stu-id="9c0b8-105">**ContainsExpressionType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="9c0b8-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="9c0b8-106">Attributes and elements</span></span>

<span data-ttu-id="9c0b8-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="9c0b8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9c0b8-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="9c0b8-108">Attributes</span></span>

|<span data-ttu-id="9c0b8-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="9c0b8-109">**Attribute**</span></span>|<span data-ttu-id="9c0b8-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9c0b8-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9c0b8-111">**ContainmentMode**</span><span class="sxs-lookup"><span data-stu-id="9c0b8-111">**ContainmentMode**</span></span> <br/> |<span data-ttu-id="9c0b8-112">Gibt die Grenzen einer Suche an.</span><span class="sxs-lookup"><span data-stu-id="9c0b8-112">Identifies the boundaries of a search.</span></span>  <br/> |
|<span data-ttu-id="9c0b8-113">**ContainmentComparison**</span><span class="sxs-lookup"><span data-stu-id="9c0b8-113">**ContainmentComparison**</span></span> <br/> |<span data-ttu-id="9c0b8-114">Bestimmt, ob die Suche Fälle und Leerzeichen ignoriert.</span><span class="sxs-lookup"><span data-stu-id="9c0b8-114">Determines whether the search ignores cases and spaces.</span></span>  <br/> |
   
#### <a name="containmentmode-attribute-values"></a><span data-ttu-id="9c0b8-115">ContainmentMode-Attributwerte</span><span class="sxs-lookup"><span data-stu-id="9c0b8-115">ContainmentMode attribute values</span></span>

|<span data-ttu-id="9c0b8-116">**Wert**</span><span class="sxs-lookup"><span data-stu-id="9c0b8-116">**Value**</span></span>|<span data-ttu-id="9c0b8-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9c0b8-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9c0b8-118">Vollständig</span><span class="sxs-lookup"><span data-stu-id="9c0b8-118">FullString</span></span>  <br/> |<span data-ttu-id="9c0b8-119">Der Vergleich erfolgt zwischen der vollständigen Zeichenfolge und der Konstanten.</span><span class="sxs-lookup"><span data-stu-id="9c0b8-119">The comparison is between the full string and the constant.</span></span> <span data-ttu-id="9c0b8-120">Der Eigenschaftswert und die angegebene Konstante sind exakt identisch.</span><span class="sxs-lookup"><span data-stu-id="9c0b8-120">The property value and the supplied constant are precisely the same.</span></span>  <br/> |
|<span data-ttu-id="9c0b8-121">Präfix visobjtype</span><span class="sxs-lookup"><span data-stu-id="9c0b8-121">Prefixed</span></span>  <br/> |<span data-ttu-id="9c0b8-122">Der Vergleich erfolgt zwischen dem Zeichenfolgen Präfix und der Konstanten.</span><span class="sxs-lookup"><span data-stu-id="9c0b8-122">The comparison is between the string prefix and the constant.</span></span>  <br/> |
|<span data-ttu-id="9c0b8-123">Teilzeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9c0b8-123">Substring</span></span>  <br/> |<span data-ttu-id="9c0b8-124">Der Vergleich besteht zwischen einer Teilzeichenfolge der Zeichenfolge und der Konstanten.</span><span class="sxs-lookup"><span data-stu-id="9c0b8-124">The comparison is between a substring of the string and the constant.</span></span>  <br/> |
|<span data-ttu-id="9c0b8-125">PrefixOnWords</span><span class="sxs-lookup"><span data-stu-id="9c0b8-125">PrefixOnWords</span></span>  <br/> |<span data-ttu-id="9c0b8-126">Der Vergleich besteht zwischen einem Präfix für einzelne Wörter in der Zeichenfolge und der Konstante.</span><span class="sxs-lookup"><span data-stu-id="9c0b8-126">The comparison is between a prefix on individual words in the string and the constant.</span></span>  <br/> |
|<span data-ttu-id="9c0b8-127">ExactPhrase</span><span class="sxs-lookup"><span data-stu-id="9c0b8-127">ExactPhrase</span></span>  <br/> |<span data-ttu-id="9c0b8-128">Der Vergleich beruht auf einem exakten Ausdruck in der Zeichenfolge und der Konstanten.</span><span class="sxs-lookup"><span data-stu-id="9c0b8-128">The comparison is between an exact phrase in the string and the constant.</span></span>  <br/> |
   
#### <a name="containmentcomparison-attribute-values"></a><span data-ttu-id="9c0b8-129">ContainmentComparison-Attributwerte</span><span class="sxs-lookup"><span data-stu-id="9c0b8-129">ContainmentComparison attribute values</span></span>

|<span data-ttu-id="9c0b8-130">**Wert**</span><span class="sxs-lookup"><span data-stu-id="9c0b8-130">**Value**</span></span>|<span data-ttu-id="9c0b8-131">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9c0b8-131">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9c0b8-132">Genauen</span><span class="sxs-lookup"><span data-stu-id="9c0b8-132">Exact</span></span>  <br/> |<span data-ttu-id="9c0b8-133">Der Vergleich muss exakt sein.</span><span class="sxs-lookup"><span data-stu-id="9c0b8-133">The comparison must be exact.</span></span>  <br/> |
|<span data-ttu-id="9c0b8-134">IgnoreCase</span><span class="sxs-lookup"><span data-stu-id="9c0b8-134">IgnoreCase</span></span>  <br/> |<span data-ttu-id="9c0b8-135">Der Vergleich ignoriert die Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="9c0b8-135">The comparison ignores casing.</span></span>  <br/> |
|<span data-ttu-id="9c0b8-136">IgnoreNonSpacingCharacters</span><span class="sxs-lookup"><span data-stu-id="9c0b8-136">IgnoreNonSpacingCharacters</span></span>  <br/> |<span data-ttu-id="9c0b8-137">Der Vergleich ignoriert Zeichen ohne Zeilenabstand.</span><span class="sxs-lookup"><span data-stu-id="9c0b8-137">The comparison ignores non-spacing characters.</span></span>  <br/> |
|<span data-ttu-id="9c0b8-138">Weit</span><span class="sxs-lookup"><span data-stu-id="9c0b8-138">Loose</span></span>  <br/> |<span data-ttu-id="9c0b8-139">Entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9c0b8-139">To be removed.</span></span>  <br/> |
|<span data-ttu-id="9c0b8-140">IgnoreCaseAndNonSpacingCharacters</span><span class="sxs-lookup"><span data-stu-id="9c0b8-140">IgnoreCaseAndNonSpacingCharacters</span></span>  <br/> |<span data-ttu-id="9c0b8-141">Der Vergleich ignoriert Groß-/Kleinschreibung und Zeichen ohne Zeilenabstand.</span><span class="sxs-lookup"><span data-stu-id="9c0b8-141">The comparison ignores casing and non-spacing characters.</span></span>  <br/> |
|<span data-ttu-id="9c0b8-142">LooseAndIgnoreCase</span><span class="sxs-lookup"><span data-stu-id="9c0b8-142">LooseAndIgnoreCase</span></span>  <br/> |<span data-ttu-id="9c0b8-143">Entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9c0b8-143">To be removed.</span></span>  <br/> |
|<span data-ttu-id="9c0b8-144">LooseAndIgnoreNonSpace</span><span class="sxs-lookup"><span data-stu-id="9c0b8-144">LooseAndIgnoreNonSpace</span></span>  <br/> |<span data-ttu-id="9c0b8-145">Entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9c0b8-145">To be removed.</span></span>  <br/> |
|<span data-ttu-id="9c0b8-146">LooseAndIgnoreCaseAndIgnoreNonSpace</span><span class="sxs-lookup"><span data-stu-id="9c0b8-146">LooseAndIgnoreCaseAndIgnoreNonSpace</span></span>  <br/> |<span data-ttu-id="9c0b8-147">Entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9c0b8-147">To be removed.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9c0b8-148">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9c0b8-148">Child elements</span></span>

|<span data-ttu-id="9c0b8-149">**Element**</span><span class="sxs-lookup"><span data-stu-id="9c0b8-149">**Element**</span></span>|<span data-ttu-id="9c0b8-150">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9c0b8-150">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9c0b8-151">FieldURI</span><span class="sxs-lookup"><span data-stu-id="9c0b8-151">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="9c0b8-152">Identifiziert häufig referenzierte Eigenschaften nach URI.</span><span class="sxs-lookup"><span data-stu-id="9c0b8-152">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="9c0b8-153">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="9c0b8-153">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="9c0b8-154">Identifiziert einzelne Member eines Wörterbuchs.</span><span class="sxs-lookup"><span data-stu-id="9c0b8-154">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="9c0b8-155">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="9c0b8-155">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="9c0b8-156">Identifiziert MAPI-Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9c0b8-156">Identifies MAPI properties.</span></span>  <br/> |
|[<span data-ttu-id="9c0b8-157">Konstante</span><span class="sxs-lookup"><span data-stu-id="9c0b8-157">Constant</span></span>](constant.md) <br/> |<span data-ttu-id="9c0b8-158">Gibt einen konstanten Wert in einer Einschränkung an.</span><span class="sxs-lookup"><span data-stu-id="9c0b8-158">Identifies a constant value in a restriction.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9c0b8-159">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9c0b8-159">Parent elements</span></span>

|<span data-ttu-id="9c0b8-160">**Element**</span><span class="sxs-lookup"><span data-stu-id="9c0b8-160">**Element**</span></span>|<span data-ttu-id="9c0b8-161">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9c0b8-161">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9c0b8-162">Einschränkung</span><span class="sxs-lookup"><span data-stu-id="9c0b8-162">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="9c0b8-163">Stellt die Einschränkung oder Abfrage dar, die zum Filtern von Elementen oder Ordnern in FindItem/FindFolder und Suchordner Vorgängen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9c0b8-163">Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span>  <br/> |
|[<span data-ttu-id="9c0b8-164">not</span><span class="sxs-lookup"><span data-stu-id="9c0b8-164">Not</span></span>](not.md) <br/> |<span data-ttu-id="9c0b8-165">Stellt einen Suchausdruck dar, der den booleschen Wert des darin enthaltenen Suchausdrucks negiert.</span><span class="sxs-lookup"><span data-stu-id="9c0b8-165">Represents a search expression that negates the Boolean value of the search expression it contains.</span></span>  <br/> |
|[<span data-ttu-id="9c0b8-166">Und</span><span class="sxs-lookup"><span data-stu-id="9c0b8-166">And</span></span>](and.md) <br/> |<span data-ttu-id="9c0b8-167">Stellt einen Suchausdruck dar, mit dem Sie einen booleschen Wert und eine Operation zwischen zwei oder mehr Suchausdrücken ausführen können.</span><span class="sxs-lookup"><span data-stu-id="9c0b8-167">Represents a search expression that allows you to perform a Boolean And operation between two or more search expressions.</span></span> <span data-ttu-id="9c0b8-168">Das Ergebnis der and-Operation ist **true** , wenn alle in der enthaltenen Suchausdrücke auf **true**festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="9c0b8-168">The result of the And operation is **true** if all of the search expressions contained within the And are **true**.</span></span>  <br/> |
|[<span data-ttu-id="9c0b8-169">- oder -</span><span class="sxs-lookup"><span data-stu-id="9c0b8-169">Or</span></span>](or.md) <br/> |<span data-ttu-id="9c0b8-170">Stellt einen Suchausdruck dar, der eine logische OR-Anweisung für den darin enthaltenen Suchausdruck ausführt.</span><span class="sxs-lookup"><span data-stu-id="9c0b8-170">Represents a search expression that performs a logical OR on the search expression it contains.</span></span> <span data-ttu-id="9c0b8-171">Das [or](or.md) -Element gibt **true** zurück, wenn eines der untergeordneten Elemente **true**zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="9c0b8-171">The [Or](or.md) element will return **true** if any of its children return **true**.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9c0b8-172">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9c0b8-172">Remarks</span></span>

<span data-ttu-id="9c0b8-173">Die Attribute werden verwendet, um zu bestimmen, wie die Elemente abgeglichen werden.</span><span class="sxs-lookup"><span data-stu-id="9c0b8-173">The attributes are used to determine how the elements are matched.</span></span>
  
<span data-ttu-id="9c0b8-174">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="9c0b8-174">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9c0b8-175">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="9c0b8-175">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9c0b8-176">Namespace</span><span class="sxs-lookup"><span data-stu-id="9c0b8-176">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9c0b8-177">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="9c0b8-177">Schema Name</span></span>  <br/> |<span data-ttu-id="9c0b8-178">Schematypen</span><span class="sxs-lookup"><span data-stu-id="9c0b8-178">Types schema</span></span>  <br/> |
|<span data-ttu-id="9c0b8-179">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="9c0b8-179">Validation File</span></span>  <br/> |<span data-ttu-id="9c0b8-180">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9c0b8-180">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9c0b8-181">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="9c0b8-181">Can be Empty</span></span>  <br/> |<span data-ttu-id="9c0b8-182">False</span><span class="sxs-lookup"><span data-stu-id="9c0b8-182">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9c0b8-183">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9c0b8-183">See also</span></span>

- [<span data-ttu-id="9c0b8-184">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="9c0b8-184">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

