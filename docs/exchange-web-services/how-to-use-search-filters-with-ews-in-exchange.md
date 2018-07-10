---
title: Verwenden Sie Suchfilter mit EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 20fc6d2d-41c2-4490-98b8-c52513977fef
description: Erfahren Sie, wie man Suchfilter mit der verwalteten EWS-API oder EWS in Exchange verwendet.
ms.openlocfilehash: 0652c36fd610c2f9dfe22b55323b368997137e0c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757023"
---
# <a name="use-search-filters-with-ews-in-exchange"></a><span data-ttu-id="8530a-103">Verwenden Sie Suchfilter mit EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="8530a-103">Use search filters with EWS in Exchange</span></span>

<span data-ttu-id="8530a-104">Erfahren Sie, wie man Suchfilter mit der verwalteten EWS-API oder EWS in Exchange verwendet.</span><span class="sxs-lookup"><span data-stu-id="8530a-104">Find out how to use search filters with the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="8530a-p101">Suchfilter sind das primäre Tool zum Ausdrücken von Suchkriterien in Ihrer verwalteten EWS-API oder EWS-Anwendung. Für folgende Vorgänge empfehlen wir Suchfilter statt [Abfragezeichenfolgen](how-to-perform-an-aqs-search-by-using-ews-in-exchange.md) zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="8530a-p101">Search filters are the primary tool for expressing search criteria in your EWS Managed API or EWS application. We recommend that you use search filters, as opposed to [query strings](how-to-perform-an-aqs-search-by-using-ews-in-exchange.md), to do the following:</span></span>
  
- <span data-ttu-id="8530a-107">Suchen nach einer bestimmten Eigenschaft oder mehreren Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8530a-107">Search on a specific property or set of properties.</span></span>  
- <span data-ttu-id="8530a-108">Suchen mithilfe von mehreren Suchkriterien</span><span class="sxs-lookup"><span data-stu-id="8530a-108">Search using multiple search criteria.</span></span>
    
<span data-ttu-id="8530a-109">Suchfilter sind Ihre einzige Option, wenn Sie einen der folgenden Vorgänge ausführen möchten:</span><span class="sxs-lookup"><span data-stu-id="8530a-109">Search filters are your only option if you are doing any of the following:</span></span>
  
- <span data-ttu-id="8530a-110">Suchen nach benutzerdefinierten Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8530a-110">Searching custom properties.</span></span>  
- <span data-ttu-id="8530a-111">Suchen nach Zeichenfolgen unter Beachtung der Groß-/Kleinschreibung</span><span class="sxs-lookup"><span data-stu-id="8530a-111">Performing case-sensitive string searches.</span></span>  
- <span data-ttu-id="8530a-112">Durchführen von Suchen in Zeichenfolgen nach Präfix- oder genauen Übereinstimmungen</span><span class="sxs-lookup"><span data-stu-id="8530a-112">Performing prefix or exact match string searches.</span></span> 
- <span data-ttu-id="8530a-113">Durchführen von Bitmaskensuchen</span><span class="sxs-lookup"><span data-stu-id="8530a-113">Performing bitmask searches.</span></span>
- <span data-ttu-id="8530a-114">Suchen nach Elementen mit einem bestimmten Eigenschaftensatz, unabhängig des Werts</span><span class="sxs-lookup"><span data-stu-id="8530a-114">Searching for items that have a specific property set, regardless of value.</span></span>
- <span data-ttu-id="8530a-115">Suchen nach Ordnern</span><span class="sxs-lookup"><span data-stu-id="8530a-115">Searching for folders.</span></span>
- <span data-ttu-id="8530a-116">Erstellen von Suchordnern</span><span class="sxs-lookup"><span data-stu-id="8530a-116">Creating search folders.</span></span>
    
## <a name="determine-what-type-of-search-filter-you-need"></a><span data-ttu-id="8530a-117">Bestimmen der benötigten Suchfiltertypen</span><span class="sxs-lookup"><span data-stu-id="8530a-117">Determine what type of search filter you need</span></span>
<span data-ttu-id="8530a-118"><a name="bk_SelectFilter"> </a></span><span class="sxs-lookup"><span data-stu-id="8530a-118"></span></span>

<span data-ttu-id="8530a-p102">Bevor Sie einen Suchfilter erstellen, müssen Sie zunächst die benötigten Suchfiltertypen bestimmen. Die Filtertypen sind als nachfolgende Klassen der [SearchFilter](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.searchfilter%28v=exchg.80%29.aspx)-Klasse in der verwalteten EWS-API, und als untergeordnete Elemente des [Restriction](http://msdn.microsoft.com/library/77f19014-d112-4999-8e83-ecc32a117a73%28Office.15%29.aspx)-Elements in EWS implementiert.</span><span class="sxs-lookup"><span data-stu-id="8530a-p102">Before you create a search filter, first determine which type of filter you need. The filter types are implemented as descendant classes of the [SearchFilter](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.searchfilter%28v=exchg.80%29.aspx) class in the EWS Managed API, and as child elements of the [Restriction](http://msdn.microsoft.com/library/77f19014-d112-4999-8e83-ecc32a117a73%28Office.15%29.aspx) element in EWS.</span></span> 
  
<span data-ttu-id="8530a-121">**Tabelle 1. Suchfiltertypen**</span><span class="sxs-lookup"><span data-stu-id="8530a-121">**Table 1. Types of search filters**</span></span>

|<span data-ttu-id="8530a-122">**Filtertyp**</span><span class="sxs-lookup"><span data-stu-id="8530a-122">**Filter type**</span></span>|<span data-ttu-id="8530a-123">**Verwaltete EWS-API-Klasse**</span><span class="sxs-lookup"><span data-stu-id="8530a-123">**EWS Managed API class**</span></span>|<span data-ttu-id="8530a-124">**EWS-Element**</span><span class="sxs-lookup"><span data-stu-id="8530a-124">**EWS element**</span></span>|<span data-ttu-id="8530a-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8530a-125">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="8530a-126">"Enthält"-Filter</span><span class="sxs-lookup"><span data-stu-id="8530a-126">Contains filter</span></span>  <br/> |[<span data-ttu-id="8530a-127">ContainsSubstring</span><span class="sxs-lookup"><span data-stu-id="8530a-127">ContainsSubstring</span></span>](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.searchfilter.containssubstring%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="8530a-128">Enthält</span><span class="sxs-lookup"><span data-stu-id="8530a-128">Contains</span></span>](http://msdn.microsoft.com/library/476d059d-c243-43e9-b475-319fc413ade2%28Office.15%29.aspx) <br/> |<span data-ttu-id="8530a-p103">Der beste Filtertyp für Zeichenfolgevergleiche. Damit können Sie die Groß-/Kleinschreibung überwachen, angeben, ob Leerzeichen ignoriert werden, und den Aufnahmemodus festlegen.</span><span class="sxs-lookup"><span data-stu-id="8530a-p103">The best filter type to use for string comparisons. It allows you to control case sensitivity, whether to ignore whitespace, and set the containment mode.</span></span>  <br/> |
|<span data-ttu-id="8530a-131">Bitmaskenfilter</span><span class="sxs-lookup"><span data-stu-id="8530a-131">Bitmask filter</span></span>  <br/> |[<span data-ttu-id="8530a-132">ExcludesBitmask</span><span class="sxs-lookup"><span data-stu-id="8530a-132">ExcludesBitmask</span></span>](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.searchfilter.excludesbitmask%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="8530a-133">Schließt</span><span class="sxs-lookup"><span data-stu-id="8530a-133">Excludes</span></span>](http://msdn.microsoft.com/library/bbaeddf6-9a67-4ee0-af99-7a7a5bbdc0e1%28Office.15%29.aspx) <br/> |<span data-ttu-id="8530a-134">Damit können Sie nach ganzzahlige Eigenschaften als Bitmasken suchen und nur Ergebnisse zurückgeben, bei denen Bits entsprechend der angegebenen Bitmaske nicht festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="8530a-134">Allows you to search integer properties as bitmasks and only return results that have bits corresponding to the specified bitmask unset.</span></span>  <br/> |
|<span data-ttu-id="8530a-135">"Vorhanden"-Filter</span><span class="sxs-lookup"><span data-stu-id="8530a-135">Exists filter</span></span>  <br/> |[<span data-ttu-id="8530a-136">Exists</span><span class="sxs-lookup"><span data-stu-id="8530a-136">Exists</span></span>](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.searchfilter.exists%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="8530a-137">Exists</span><span class="sxs-lookup"><span data-stu-id="8530a-137">Exists</span></span>](http://msdn.microsoft.com/library/55d568bd-8dbc-4d50-b9d7-54b74a54d4b5%28Office.15%29.aspx) <br/> |<span data-ttu-id="8530a-138">Gibt alle Elemente zurück, bei denen die angegebene Eigenschaft vorhanden ist, unabhängig des Werts.</span><span class="sxs-lookup"><span data-stu-id="8530a-138">Returns all items that have the specified property present, regardless of value.</span></span>  <br/> |
|<span data-ttu-id="8530a-139">Gleichheitsfilter</span><span class="sxs-lookup"><span data-stu-id="8530a-139">Equality filter</span></span>  <br/> |[<span data-ttu-id="8530a-140">"IsEqualTo"</span><span class="sxs-lookup"><span data-stu-id="8530a-140">IsEqualTo</span></span>](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.searchfilter.isequalto%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="8530a-141">IsNotEqualTo</span><span class="sxs-lookup"><span data-stu-id="8530a-141">IsNotEqualTo</span></span>](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.searchfilter.isnotequalto%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="8530a-142">"IsEqualTo"</span><span class="sxs-lookup"><span data-stu-id="8530a-142">IsEqualTo</span></span>](http://msdn.microsoft.com/library/48e7e067-049c-4184-8026-071e6f558e8a%28Office.15%29.aspx) <br/> [<span data-ttu-id="8530a-143">IsNotEqualTo</span><span class="sxs-lookup"><span data-stu-id="8530a-143">IsNotEqualTo</span></span>](http://msdn.microsoft.com/library/e2eff26c-3403-45cd-bb74-1eb98c7dbfcd%28Office.15%29.aspx) <br/> |<span data-ttu-id="8530a-144">Vergleicht den Wert der angegebenen Eigenschaft mit einem angegebenen Konstantenwert oder dem Wert einer anderen Eigenschaft und gibt alle Elemente mit einem gleichen Wert (im Falle eines **IsEqualTo**-Filters) oder einen nicht gleichen Wert (im Falle eines **IsNotEqualTo**-Filters) zurück.</span><span class="sxs-lookup"><span data-stu-id="8530a-144">Compares the value of the specified property with either a specified constant value or the value of another property and return all items that have an equal value (in the case of an **IsEqualTo** filter) or a non-equal value (in the case of an **IsNotEqualTo** filter).</span></span>  <br/> |
|<span data-ttu-id="8530a-145">Relationaler Testfilter</span><span class="sxs-lookup"><span data-stu-id="8530a-145">Relational testing filter</span></span>  <br/> |[<span data-ttu-id="8530a-146">IsGreaterThan</span><span class="sxs-lookup"><span data-stu-id="8530a-146">IsGreaterThan</span></span>](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.searchfilter.isgreaterthan%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="8530a-147">IsGreaterThanOrEqualTo</span><span class="sxs-lookup"><span data-stu-id="8530a-147">IsGreaterThanOrEqualTo</span></span>](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.searchfilter.isgreaterthanorequalto%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="8530a-148">IsLessThan</span><span class="sxs-lookup"><span data-stu-id="8530a-148">IsLessThan</span></span>](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.searchfilter.islessthan%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="8530a-149">IsLessThanOrEqualTo</span><span class="sxs-lookup"><span data-stu-id="8530a-149">IsLessThanOrEqualTo</span></span>](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.searchfilter.islessthanorequalto%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="8530a-150">IsGreaterThan</span><span class="sxs-lookup"><span data-stu-id="8530a-150">IsGreaterThan</span></span>](http://msdn.microsoft.com/library/a6e9d462-cfa7-40ec-903e-128c95050352%28Office.15%29.aspx) <br/> [<span data-ttu-id="8530a-151">IsGreaterThanOrEqualTo</span><span class="sxs-lookup"><span data-stu-id="8530a-151">IsGreaterThanOrEqualTo</span></span>](http://msdn.microsoft.com/library/373cc954-314d-40e2-be03-cc08aefc0d5b%28Office.15%29.aspx) <br/> [<span data-ttu-id="8530a-152">IsLessThan</span><span class="sxs-lookup"><span data-stu-id="8530a-152">IsLessThan</span></span>](http://msdn.microsoft.com/library/2550469b-6e5d-45a5-9ecc-090d1b409296%28Office.15%29.aspx) <br/> [<span data-ttu-id="8530a-153">IsLessThanOrEqualTo</span><span class="sxs-lookup"><span data-stu-id="8530a-153">IsLessThanOrEqualTo</span></span>](http://msdn.microsoft.com/library/b5d85eb2-5e15-4d01-ad49-6289e735ad8a%28Office.15%29.aspx) <br/> |<span data-ttu-id="8530a-p104">Gibt alle Elemente zurück, die für die angegebene Eigenschaft in der entsprechenden Beziehung einen Wert für einen angegebenen Konstantenwert oder eine andere Eigenschaft besitzen. Ein **IsGreaterThan**-Filter gibt alle Elemente zurück, die einen höheren Wert besitzen als der angegebene Wert in der angegebenen Eigenschaft.  </span><span class="sxs-lookup"><span data-stu-id="8530a-p104">Returns all items that have a value for the specified property in the appropriate relation to either a specified constant value or another property. For example, an **IsGreaterThan** filter returns all items that have a value that is greater than the specified value in the specified property.  </span></span><br/> |
|<span data-ttu-id="8530a-156">Aufhebungsfilter</span><span class="sxs-lookup"><span data-stu-id="8530a-156">Negating filter</span></span>  <br/> |[<span data-ttu-id="8530a-157">Not</span><span class="sxs-lookup"><span data-stu-id="8530a-157">Not</span></span>](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.searchfilter.not%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="8530a-158">not</span><span class="sxs-lookup"><span data-stu-id="8530a-158">Not</span></span>](http://msdn.microsoft.com/library/1aa16318-7e90-4b19-bce8-dd1a20a66223%28Office.15%29.aspx) <br/> |<span data-ttu-id="8530a-159">Hebt das Ergebnis der anderen Filter auf.</span><span class="sxs-lookup"><span data-stu-id="8530a-159">Negates the result of the other filters.</span></span>  <br/> |
|<span data-ttu-id="8530a-160">Zusammengesetzter Filter</span><span class="sxs-lookup"><span data-stu-id="8530a-160">Compound filter</span></span>  <br/> |[<span data-ttu-id="8530a-161">SearchFilterCollection</span><span class="sxs-lookup"><span data-stu-id="8530a-161">SearchFilterCollection</span></span>](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.searchfilter.searchfiltercollection%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="8530a-162">Und</span><span class="sxs-lookup"><span data-stu-id="8530a-162">And</span></span>](http://msdn.microsoft.com/library/790246c2-37ad-49a8-91b9-6186d743b011%28Office.15%29.aspx) <br/> [<span data-ttu-id="8530a-163">- oder -</span><span class="sxs-lookup"><span data-stu-id="8530a-163">Or</span></span>](http://msdn.microsoft.com/library/4876d83a-73a3-4953-9d95-3048e6b76ccb%28Office.15%29.aspx) <br/> |<span data-ttu-id="8530a-164">Kombiniert mehrere Filter, damit komplexere Suchkriterien möglich sind.</span><span class="sxs-lookup"><span data-stu-id="8530a-164">Combines multiple filters, allowing for more complex search criteria.</span></span>  <br/> |
   
### <a name="contains-filter"></a><span data-ttu-id="8530a-165">"Enthält"-Filter</span><span class="sxs-lookup"><span data-stu-id="8530a-165">Contains filter</span></span>

<span data-ttu-id="8530a-p105">Ein "Enthält"-Filter ist die beste Wahl zum Durchsuchen von Zeichenfolgeneigenschaften. Mit einem "Enthält"-Filter können Sie Aspekte des Zeichenfolgeabgleichs steuern, wie z. B. die Groß-/Kleinschreibung und die Behandlung von Leerzeichen, indem Sie den Aufnahme- und Vergleichsmodus festlegen.</span><span class="sxs-lookup"><span data-stu-id="8530a-p105">A contains filter is the best choice for searching string properties. With a contains filter, you can control aspects of string matching, like case sensitivity and how whitespace is treated, by setting the containment mode and the comparison mode.</span></span>
  
#### <a name="contains-filter-in-the-ews-managed-api"></a><span data-ttu-id="8530a-168">Der "Enthält"-Filter in der verwalteten EWS-API</span><span class="sxs-lookup"><span data-stu-id="8530a-168">Contains filter in the EWS Managed API</span></span>
<span data-ttu-id="8530a-169"><a name="bk_ContainsEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="8530a-169"></span></span>

<span data-ttu-id="8530a-p106">Wenn Sie die verwaltete EWS-API verwenden, legen Sie den Aufnahmemodus fest, indem Sie die [ContainmentMode](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.searchfilter.containssubstring.containmentmode%28v=exchg.80%29.aspx)-Eigenschaft der [ContainsSubstring](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.searchfilter.containssubstring%28v=exchg.80%29.aspx)-Klasse verwenden, und Sie legen den Vergleichsmodus fest, indem Sie die [ComparisonMode](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.searchfilter.containssubstring.comparisonmode%28v=exchg.80%29.aspx)-Eigenschaft der **ContainsSubstring**-Klasse verwenden. In den folgenden Beispielen wird veranschaulicht, wie Sie einen Suchfilter erstellen, der das Betrefffeld der Elemente nach der Teilzeichenfolge „Besprechungsnotizen" durchsucht. In diesem Beispiel wird die Groß-/Kleinschreibung ignoriert, Leerzeichen jedoch nicht.</span><span class="sxs-lookup"><span data-stu-id="8530a-p106">If you're using the EWS Managed API, you set the containment mode by using the [ContainmentMode](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.searchfilter.containssubstring.containmentmode%28v=exchg.80%29.aspx) property of the [ContainsSubstring](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.searchfilter.containssubstring%28v=exchg.80%29.aspx) class, and you set the comparison mode by using the [ComparisonMode](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.searchfilter.containssubstring.comparisonmode%28v=exchg.80%29.aspx) property of the **ContainsSubstring** class. The following example shows you how to create a search filter that searches the subject field of items for the substring "meeting notes". This example ignores case, but does not ignore whitespace.</span></span> 
  
```cs
// Find all items with a subject that contain the substring
// "meeting notes", regardless of case.
// Matches include:
//   - meeting notes
//   - Meeting Notes
//   - Here are my meeting notes
SearchFilter.ContainsSubstring subjectFilter = new SearchFilter.ContainsSubstring(ItemSchema.Subject,
    "meeting notes", ContainmentMode.Substring, ComparisonMode.IgnoreCase);
```

#### <a name="contains-filter-in-ews"></a><span data-ttu-id="8530a-173">Der "Enthält"-Filter in EWS</span><span class="sxs-lookup"><span data-stu-id="8530a-173">Contains filter in EWS</span></span>
<span data-ttu-id="8530a-174"><a name="bk_ContainsEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="8530a-174"></span></span>

<span data-ttu-id="8530a-p107">In EWS legen Sie den Aufnahmemodus fest, indem Sie das **ContainmentMode**-Attribut für das [Enthält](http://msdn.microsoft.com/library/476d059d-c243-43e9-b475-319fc413ade2%28Office.15%29.aspx)-Element verwenden, und den Vergleichsmodus festlegen, indem Sie das **ContainmentComparison**-Attribut für das **Contains**-Element verwenden. Im folgenden Beispiel wird veranschaulicht, wie einen Suchfilter zum Durchsuchen des Suchfelds von Elementen nach der Teilzeichenfolge „Besprechungsnotizen" erstellen. In diesem Beispiel wird die Groß-/Kleinschreibung ignoriert, Leerzeichen jedoch nicht.</span><span class="sxs-lookup"><span data-stu-id="8530a-p107">In EWS, you set the containment mode by using the **ContainmentMode** attribute on the [Contains](http://msdn.microsoft.com/library/476d059d-c243-43e9-b475-319fc413ade2%28Office.15%29.aspx) element, and you set the comparison mode by using the **ContainmentComparison** attribute on the **Contains** element. The following example shows you how to create a search filter to search the subject field of items for the substring "meeting notes". This example ignores case, but does not ignore whitespace.</span></span> 
  
```XML
<t:Contains ContainmentMode="Substring" ContainmentComparison="IgnoreCase">
  <t:FieldURI FieldURI="item:Subject" />
  <t:Constant Value="meeting notes" />
</t:Contains>
```

### <a name="bitmask-filter"></a><span data-ttu-id="8530a-178">Bitmaskenfilter</span><span class="sxs-lookup"><span data-stu-id="8530a-178">Bitmask filter</span></span>

<span data-ttu-id="8530a-179">Mit einem Bitmaskenfilter können Sie ganzzahlige Eigenschaften als Bitmasken durchsuchen, und Ergebnisse zurückgeben, in denen bestimmte Bits nicht im Wert der angegebenen Eigenschaft festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="8530a-179">A bitmask filter enables you to search integer properties as bitmasks, and return results where specific bits are not set in the value of the specified property.</span></span>
  
#### <a name="bitmask-filter-in-the-ews-managed-api"></a><span data-ttu-id="8530a-180">Bitmaskenfilter in der verwalteten EWS-API</span><span class="sxs-lookup"><span data-stu-id="8530a-180">Bitmask filter in the EWS Managed API</span></span>

<span data-ttu-id="8530a-181">Im folgenden Beispiel wird veranschaulicht, wie Sie die verwaltete EWS-API zum Erstellen eines Suchfilters verwendet wird, um alle Elemente zurückzugeben, bei denen sich in der benutzerdefinierten **ItemIndex**-Eigenschaft ein Wert befindet (definiert im Abschnitt [Beispiel: Suchen von Elementen mithilfe eines Suchfilters und der verwalteten EWS-API](#bk_ExampleEWSMA) dieses Artikels), die den sekundären Bitsatz (10 in der Binärdatei) nicht aufweisen.</span><span class="sxs-lookup"><span data-stu-id="8530a-181">The following example shows you how to use the EWS Managed API to create a search filter to return all items that have a value in the **ItemIndex** custom property (defined in the [Example: Find items by using a search filter and the EWS Managed API](#bk_ExampleEWSMA) section of this article) that do not have the second bit (10 in binary) set.</span></span> 
  
```cs
// Find all items with a value of the custom property that does not
// have the second bit (0010) set.
// Matches include:
//   - Property not set
//   - 1 (0001)
//   - 4 (0100)
//   - 5 (0101)
//   - 8 (1000)
SearchFilter.ExcludesBitmask bit2NotSetFilter = 
    new SearchFilter.ExcludesBitmask(customPropDefinition, 2);
```

#### <a name="bitmask-filter-in-ews"></a><span data-ttu-id="8530a-182">Bitmaskenfilter in EWS</span><span class="sxs-lookup"><span data-stu-id="8530a-182">Bitmask filter in EWS</span></span>

<span data-ttu-id="8530a-183">Im folgenden Beispiel wird veranschaulicht, wie Sie mithilfe von EWS einen Suchfilter erstellen können, um alle Elemente zurückzugeben, die in der benutzerdefinierten **ItemIndex**-Eigenschaft (definiert im Abschnitt [Beispiel: Suchen von Elementen mithilfe eines Suchfilters und der verwalteten EWS-API](#bk_ExampleEWSMA) dieses Artikels), die den sekundären Bitsatz (10 in der Binärdatei) nicht aufweisen.</span><span class="sxs-lookup"><span data-stu-id="8530a-183">The following example shows you how to use EWS to create a search filter to return all items that have a value in the **ItemIndex** custom property (defined in the [Example: Find items by using a search filter and the EWS Managed API](#bk_ExampleEWSMA) section of this article) that do not have the second bit (10 in binary) set.</span></span> 
  
```XML
<t:Excludes>
  <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
  <t:Bitmask Value="2" />
</t:Excludes>
```

### <a name="exists-filter"></a><span data-ttu-id="8530a-184">"Vorhanden"-Filter</span><span class="sxs-lookup"><span data-stu-id="8530a-184">Exists filter</span></span>

<span data-ttu-id="8530a-185">Mit einem "Vorhanden"-Filter können Sie nach Elementen suchen, die unabhängig des Werts einen bestimmten Eigenschaftensatz besitzen.</span><span class="sxs-lookup"><span data-stu-id="8530a-185">An exists filter enables you to search for items that have a specific property set on them, regardless of the value.</span></span>
  
#### <a name="exists-filter-in-the-ews-managed-api"></a><span data-ttu-id="8530a-186">"Vorhanden"-Filter in der verwalteten EWS-API</span><span class="sxs-lookup"><span data-stu-id="8530a-186">Exists filter in the EWS Managed API</span></span>

<span data-ttu-id="8530a-187">Im folgenden Beispiel wird veranschaulicht, wie ein Suchfilter erstellt wird, mit dem alle Elemente zurückgegeben werden, die einen benutzerdefinierten **ItemIndex**-Eigenschaftensatz besitzen.</span><span class="sxs-lookup"><span data-stu-id="8530a-187">The following example shows you how to create a search filter to return all items that have the **ItemIndex** custom property set.</span></span> 
  
```cs
// Find all items that have the custom property set.
SearchFilter.Exists customPropSetFilter =
    new SearchFilter.Exists(customPropDefinition);
```

#### <a name="exists-filter-in-ews"></a><span data-ttu-id="8530a-188">"Vorhanden"-Filter in EWS</span><span class="sxs-lookup"><span data-stu-id="8530a-188">Exists filter in EWS</span></span>

<span data-ttu-id="8530a-189">Im folgenden Beispiel wird veranschaulicht, wie ein Suchfilter erstellt wird, um alle Elemente zurückzugeben, die den benutzerdefinierten **ItemIndex**-Eigenschaftensatz aufweisen.</span><span class="sxs-lookup"><span data-stu-id="8530a-189">The following example shows you how to create a search filter to return all items that have the **ItemIndex** custom property set.</span></span> 
  
```XML
<t:Exists>
  <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
</t:Exists>
```

### <a name="equality-filter"></a><span data-ttu-id="8530a-190">Gleichheitsfilter</span><span class="sxs-lookup"><span data-stu-id="8530a-190">Equality filter</span></span>

<span data-ttu-id="8530a-p108">Mit Gleichheitsfiltern können Sie nach allen Elementen suchen, die einen Wert für die bestimmte Eigenschaft aufweisen, die mit einem bestimmten Wert übereinstimmt oder mit einem bestimmten Wert nicht übereinstimmt. Der zu vergleichende Wert kann ein Konstantenwert oder der Wert zu einer anderen Eigenschaft jedes Elements sein.</span><span class="sxs-lookup"><span data-stu-id="8530a-p108">Equality filters enable you to search for all items that have a value for the specified property that either equals a specific value or does not equal a specific value. The value to compare with can be either a constant value or the value of another property on each item.</span></span>
  
#### <a name="equality-filter-in-the-ews-managed-api"></a><span data-ttu-id="8530a-193">Der Gleichheitsfilter in der verwalteten EWS-API</span><span class="sxs-lookup"><span data-stu-id="8530a-193">Equality filter in the EWS Managed API</span></span>

<span data-ttu-id="8530a-194">Im folgenden Beispiel wird veranschaulicht, wie Sie die verwaltete EWS-API zum Erstellen eines Suchfilters verwenden können, damit alle Elemente zurückgegeben werden, die noch nicht gelesen wurden.</span><span class="sxs-lookup"><span data-stu-id="8530a-194">The following example shows you how to use the EWS Managed API to create a search filter to return all items that have not been read.</span></span>
  
```cs
// Find all items that are not marked as read.
SearchFilter.IsEqualTo unreadFilter =
    new SearchFilter.IsEqualTo(EmailMessageSchema.IsRead, false);
```

<span data-ttu-id="8530a-195">Im folgenden Beispiel wird veranschaulicht, wie ein Suchfilter erstellt wird, um alle Elemente zurückzugeben, die einen Wert in der **ItemIndex**-Eigenschaft besitzen, der nicht mit der Größe des Elements übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="8530a-195">The following example shows you how to create a search filter to return all items that have a value in the **ItemIndex** property that is not equal to the size of the item.</span></span> 
  
```cs
// Find all items that are marked as read.
SearchFilter.IsNotEqualTo indexNotEqualToSizeFilter =
    new SearchFilter.IsNotEqualTo(customPropDefinition, ItemSchema.Size);
```

#### <a name="equality-filter-in-ews"></a><span data-ttu-id="8530a-196">Gleichheitsfilter in EWS</span><span class="sxs-lookup"><span data-stu-id="8530a-196">Equality filter in EWS</span></span>

<span data-ttu-id="8530a-197">Im folgenden Beispiel wird veranschaulicht, wie EWS zum Erstellen eines Suchfilters verwendet wird, damit alle Elemente zurückgegeben werden, die noch nicht gelesen wurden.</span><span class="sxs-lookup"><span data-stu-id="8530a-197">The following example shows you how to use EWS to create a search filter to return all items that have not been read.</span></span>
  
```XML
<t:IsEqualTo>
  <t:FieldURI FieldURI="message:IsRead" />
  <t:FieldURIOrConstant>
    <t:Constant Value="false" />
  </t:FieldURIOrConstant>
</t:IsEqualTo>
```

<span data-ttu-id="8530a-198">Im folgenden Beispiel wird veranschaulicht, wie ein Suchfilter erstellt wird, sodass alle Elemente mit einem Wert in der **ItemIndex**-Eigenschaft zurückgegeben wird, der nicht mit der Größe des Elements übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="8530a-198">The following example shows you how to create a search filter to return all items that have a value in the **ItemIndex** property that is not equal to the size of the item.</span></span> 
  
```XML
<t:IsNotEqualTo>
  <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
  <t:FieldURIOrConstant>
    <t:FieldURI FieldURI="item:Size" />
  </t:FieldURIOrConstant>
</t:IsNotEqualTo>
```

### <a name="relational-testing-filter"></a><span data-ttu-id="8530a-199">Relationaler Testfilter</span><span class="sxs-lookup"><span data-stu-id="8530a-199">Relational testing filter</span></span>

<span data-ttu-id="8530a-p109">Mit relationalen Testfiltern können Sie nach allen Elementen suchen, die in der angegebenen Eigenschaft einen Wert aufweisen, der entweder größer als (\>), größer als oder gleich (\>=), kleiner als (\<), oder kleiner als oder gleich (\<=) einem angegebenen Wert ist. Der zu vergleichende Wert kann ein Konstantenwert oder der Wert einer anderen Eigenschaft der einzelnen Elemente sein.</span><span class="sxs-lookup"><span data-stu-id="8530a-p109">Relational testing filters enable you to search for all items that have a value in the specified property that is either greater than (\>), greater than or equal to (\>=), less than (\<), or less than or equal to (\<=) a specified value. The value to compare with can be either a constant value or the value of another property on each item.</span></span>
  
#### <a name="relational-testing-filter-in-the-ews-managed-api"></a><span data-ttu-id="8530a-202">Der relational Testfilter in der verwalteten EWS-API</span><span class="sxs-lookup"><span data-stu-id="8530a-202">Relational testing filter in the EWS Managed API</span></span>

<span data-ttu-id="8530a-203">Im folgenden Beispiel wird veranschaulicht, wie die verwaltete EWS-API zum Erstellen von Suchfiltern verwendet werden kann, damit alle Elemente mit einem Wert in der **ItemIndex**-Eigenschaft zurückgegeben werden, die die angegebene Beziehung zum Konstantenwert 3 aufweisen.</span><span class="sxs-lookup"><span data-stu-id="8530a-203">The following example shows you how to use the EWS Managed API to create search filters to return all items with a value in the **ItemIndex** property that has the specified relationship to the constant value 3.</span></span> 
  
```cs
// Find all items where the custom property value is > 3.
SearchFilter.IsGreaterThan greaterThanFilter =
    new SearchFilter.IsGreaterThan(customPropDefinition, 3);
// Find all items where the custom property value is >= 3.
SearchFilter.IsGreaterThanOrEqualTo greaterThanOrEqualFilter =
    new SearchFilter.IsGreaterThanOrEqualTo(customPropDefinition, ItemSchema.Size);
// Find all items where the custom property value is < 3.
SearchFilter.IsLessThan lessThanFilter =
    new SearchFilter.IsLessThan(customPropDefinition, 3);
// Find all items where the custom property value is <= 3.
SearchFilter.IsLessThanOrEqualTo lessThanOrEqualFilter =
    new SearchFilter.IsLessThanOrEqualTo(customPropDefinition, 3);
```

#### <a name="relational-testing-filter-in-ews"></a><span data-ttu-id="8530a-204">Der relationale Testfilter in EWS</span><span class="sxs-lookup"><span data-stu-id="8530a-204">Relational testing filter in EWS</span></span>

<span data-ttu-id="8530a-205">Im folgenden Beispiel wird veranschaulicht, wie Sie EWS zum Erstellen eines Suchfilters verwenden können, damit alle Elemente mit einem Wert in der **ItemIndex**-Eigenschaft zurückgegeben werden, der höher ist als Konstantenwert 3.</span><span class="sxs-lookup"><span data-stu-id="8530a-205">The following example shows you how to use EWS to create a search filter to return all items with a value in the **ItemIndex** property that is greater than the constant value 3.</span></span> 
  
```XML
<t:IsGreaterThan>
  <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
  <t:FieldURIOrConstant>
    <t:Constant Value="3" />
  </t:FieldURIOrConstant>
</t:IsGreaterThan>
```

<span data-ttu-id="8530a-206">Im folgenden Beispiel wird veranschaulicht, wie Sie einen Suchfilter erstellen können, damit alle Elemente mit einem Wert in der **ItemIndex**-Eigenschaft zurückgegeben werden, der größer oder gleich Konstantenwert 3 ist.</span><span class="sxs-lookup"><span data-stu-id="8530a-206">The following example shows you how to create a search filter to return all items with a value in the **ItemIndex** property that is greater than or equal to the constant value 3.</span></span> 
  
```XML
<t:IsGreaterThanOrEqualTo>
  <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
  <t:FieldURIOrConstant>
    <t:Constant Value="3" />
  </t:FieldURIOrConstant>
</t:IsGreaterThanOrEqualTo>
```

<span data-ttu-id="8530a-207">Im folgenden Beispiel wird veranschaulicht, wie Sie einen Suchfilter erstellen können, damit alle Elemente mit einem Wert in der **ItemIndex**-Eigenschaft zurückgegeben werden, der kleiner ist als Konstantenwert 3.</span><span class="sxs-lookup"><span data-stu-id="8530a-207">The following example shows you how to create a search filter to return all items with a value in the **ItemIndex** property that is less than the constant value 3.</span></span> 
  
```XML
<t:IsLessThan>
  <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
  <t:FieldURIOrConstant>
    <t:Constant Value="3" />
  </t:FieldURIOrConstant>
</t:IsLessThan>
```

<span data-ttu-id="8530a-208">Im folgenden Beispiel wird veranschaulicht, wie Sie einen Suchfilter erstellen, damit alle Elemente mit einem Wert in der **ItemIndex**-Eigenschaft zurückgegeben werden, der kleiner oder gleich Konstantenwert 3 ist.</span><span class="sxs-lookup"><span data-stu-id="8530a-208">The following example shows you how to create a search filter to return all items with a value in the **ItemIndex** property that is less than or equal to the constant value 3.</span></span> 
  
```XML
<t:IsLessThanOrEqualTo>
  <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
  <t:FieldURIOrConstant>
    <t:Constant Value="3" />
  </t:FieldURIOrConstant>
</t:IsLessThanOrEqualTo>
```

### <a name="negating-filter"></a><span data-ttu-id="8530a-209">Aufhebungsfilter</span><span class="sxs-lookup"><span data-stu-id="8530a-209">Negating filter</span></span>

<span data-ttu-id="8530a-p110">Mit einem Aufhebungsfilter können Sie einen anderen Filter aufheben und gegenteilige Suchergebnisse erhalten. Während andere Filter Ergebnisse zurückgeben, die mit einem bestimmten Suchkriterium übereinstimmen, gibt ein Aufhebungsfilter Ergebnisse zurück, die nicht mit dem angegebenen Filterkriterium übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="8530a-p110">A negating filter enables you to negate another filter and get the opposite search results. While other filters return results that match specific criteria, a negating filter returns results that do not match the criteria specified by the filter it is applied to.</span></span>
  
#### <a name="negating-filter-in-the-ews-managed-api"></a><span data-ttu-id="8530a-212">Der Aufhebungsfilter in der verwalteten EWS-API</span><span class="sxs-lookup"><span data-stu-id="8530a-212">Negating filter in the EWS Managed API</span></span>

<span data-ttu-id="8530a-213">Im folgenden Beispiel wird veranschaulicht, Sie sie die verwaltete EWS-API zum Erstellen eines Suchfilters verwenden können, damit alle Elemente zurückgegeben werden, in denen die Teilzeichenfolge „Besprechungsnotizen" nicht im Betreff enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="8530a-213">The following example shows you how to use the EWS Managed API to create a search filter to return all items that do not have the substring "meeting notes" in the subject.</span></span>
  
```cs
SearchFilter.ContainsSubstring subjectFilter = new SearchFilter.ContainsSubstring(ItemSchema.Subject,
    "meeting notes", ContainmentMode.Substring, ComparisonMode.IgnoreCase);
SearchFilter.Not subjectNotFilter =
    new SearchFilter.Not(subjectFilter);
```

#### <a name="negating-filter-in-ews"></a><span data-ttu-id="8530a-214">Der Aufhebungsfilter in EWS</span><span class="sxs-lookup"><span data-stu-id="8530a-214">Negating filter in EWS</span></span>

<span data-ttu-id="8530a-215">Im folgenden Beispiel wird veranschaulicht, wie Sie einen Suchfilter erstellen können, damit alle Elemente zurückgegeben werden, in denen die Teilzeichenfolge„Besprechungsnotizen" nicht im Betreff enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="8530a-215">The following example shows you how to create a search filter to return all items that do not have the substring "meeting notes" in the subject.</span></span>
  
```XML
<t:Not>
  <t:Contains ContainmentMode="ExactPhrase" ContainmentComparison="IgnoreCase">
    <t:FieldURI FieldURI="item:Subject" />
    <t:Constant Value="meeting notes" />
  </t:Contains>
</t:Not>
```

### <a name="compound-filter"></a><span data-ttu-id="8530a-216">Zusammengesetzter Filter</span><span class="sxs-lookup"><span data-stu-id="8530a-216">Compound filter</span></span>

<span data-ttu-id="8530a-p111">Mit einem zusammengesetzten Filter können Sie mehrere Filter kombinieren, um komplexere Suchkriterien erstellen zu können. Sie können Kriterien mithilfe des logischen Operators AND oder OR kombinieren. So können Sie Suchen wie z. B. „alle Nachrichten Sadie Daniels, bei denen 'Besprechungsnotizen' im Betreff enthalten ist".</span><span class="sxs-lookup"><span data-stu-id="8530a-p111">A compound filter enables you to combine multiple filters to create more complex search criteria. You can combine criteria by using the logical operators AND or OR. In this way, you can perform searches like "all mail from Sadie Daniels that contains 'meeting notes' in the subject".</span></span>
  
#### <a name="compound-filter-in-the-ews-managed-api"></a><span data-ttu-id="8530a-220">Der zusammengesetzte Filter in der verwalteten EWS-API</span><span class="sxs-lookup"><span data-stu-id="8530a-220">Compound filter in the EWS Managed API</span></span>

<span data-ttu-id="8530a-221">Im folgenden Beispiel wird veranschaulicht, wie Sie die verwaltete EWS-API zum Erstellen eines Suchfilters verwenden können, damit alle Elemente zurückgegeben werden, die von Sadie Daniels gesendet wurden und „Besprechungsnotizen" im Betreff enthalten.</span><span class="sxs-lookup"><span data-stu-id="8530a-221">The following example shows you how to use the EWS Managed API to create a search filter that returns all items that are sent from Sadie Daniels and contain "meeting notes" in the subject.</span></span>
  
```cs
SearchFilter.ContainsSubstring subjectFilter = new SearchFilter.ContainsSubstring(ItemSchema.Subject,
    "meeting notes", ContainmentMode.Substring, ComparisonMode.IgnoreCase);
EmailAddress manager = new EmailAddress("sadie@contoso.com");
SearchFilter.IsEqualTo fromManagerFilter =
    new SearchFilter.IsEqualTo(EmailMessageSchema.Sender, manager);
SearchFilter.SearchFilterCollection compoundFilter =
    new SearchFilter.SearchFilterCollection(LogicalOperator.And, subjectFilter, fromManagerFilter);
```

#### <a name="compound-filter-in-ews"></a><span data-ttu-id="8530a-222">Der zusammengesetzte Filter in EWS</span><span class="sxs-lookup"><span data-stu-id="8530a-222">Compound filter in EWS</span></span>

<span data-ttu-id="8530a-223">Im folgenden Beispiel wird veranschaulicht, wie EWS zum Erstellen eines Suchfilters verwendet werden kann, damit alle Elemente zurückgegeben werden, die von Sadie Daniels gesendet wurden und „Besprechungsnotizen" im Betreff enthalten.</span><span class="sxs-lookup"><span data-stu-id="8530a-223">The following example shows you how to use EWS to create a search filter that returns all items that are sent from Sadie Daniels and contain "meeting notes" in the subject.</span></span>
  
```XML
<t:And>
  <t:Contains ContainmentMode="Substring" ContainmentComparison="IgnoreCase">
    <t:FieldURI FieldURI="item:Subject" />
    <t:Constant Value="meeting notes" />
  </t:Contains>
  <t:IsEqualTo>
    <t:FieldURI FieldURI="message:Sender" />
    <t:FieldURIOrConstant>
      <t:Constant Value="sadie@fourthcoffee.com" />
    </t:FieldURIOrConstant>
  </t:IsEqualTo>
</t:And>
```

## <a name="example-find-items-by-using-a-search-filter-and-the-ews-managed-api"></a><span data-ttu-id="8530a-224">Beispiel: Suchen von Elementen mithilfe eines Suchfilters und der verwalteten EWS-API</span><span class="sxs-lookup"><span data-stu-id="8530a-224">Example: Find items by using a search filter and the EWS Managed API</span></span>
<span data-ttu-id="8530a-225"><a name="bk_ExampleEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="8530a-225"></span></span>

<span data-ttu-id="8530a-226">Folgende verwaltete EWS-API-Methoden verwenden Suchfilter:</span><span class="sxs-lookup"><span data-stu-id="8530a-226">The following EWS Managed API methods use search filters:</span></span>
  
- [<span data-ttu-id="8530a-227">ExchangeService.FindItems</span><span class="sxs-lookup"><span data-stu-id="8530a-227">ExchangeService.FindItems</span></span>](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)
- [<span data-ttu-id="8530a-228">ExchangeService.FindFolders</span><span class="sxs-lookup"><span data-stu-id="8530a-228">ExchangeService.FindFolders</span></span>](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx)
- [<span data-ttu-id="8530a-229">Folder.FindFolders</span><span class="sxs-lookup"><span data-stu-id="8530a-229">Folder.FindFolders</span></span>](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx)
- [<span data-ttu-id="8530a-230">Folder.FindItems</span><span class="sxs-lookup"><span data-stu-id="8530a-230">Folder.FindItems</span></span>](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx)
    
<span data-ttu-id="8530a-p112">Im folgenden Beispiel wird die **ExchangeService.FindItems**-Methode verwendet; die gleichen Regeln und Konzepte gelten jedoch für alle Methoden. In diesem Beispiel wird eine Methode mit der Bezeichnung **SearchWithFilter** definiert. Als Parameter ist ein [ExchangeService](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt, ein [WellKnownFolderName](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx)-Objekt und ein [SearchFilter](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.searchfilter%28v=exchg.80%29.aspx)-Objekt erforderlich. In diesem Beispiel wird davon ausgegangen, dass das **ExchangeService**-Objekt mit gültigen Werten in den [Credentials](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx)- und [Url](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx)-Eigenschaften initialisiert wurde. Die **SearchFilter**-Klasse ist die Basisklasse für alle verschiedenen Suchfilter.</span><span class="sxs-lookup"><span data-stu-id="8530a-p112">The following example uses the **ExchangeService.FindItems** method; however, the same rules and concepts apply to all the methods. In this example, a method called **SearchWithFilter** is defined. It takes an [ExchangeService](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object, a [WellKnownFolderName](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) object, and a [SearchFilter](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.searchfilter%28v=exchg.80%29.aspx) object as parameters. This example assumes that the **ExchangeService** object has been initialized with valid values in the [Credentials](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) and [Url](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) properties. The **SearchFilter** class is the base class for all the different search filters.</span></span> 
  
```cs
using Microsoft.Exchange.WebServices.Data
private static Guid SearchTestGUID = new Guid("{AA3DF801-4FC7-401F-BBC1-7C93D6498C2E}");
private static ExtendedPropertyDefinition customPropDefinition =
        new ExtendedPropertyDefinition(SearchTestGUID, "ItemIndex", MapiPropertyType.Integer);
static void SearchWithFilter(ExchangeService service, WellKnownFolderName folder, SearchFilter filter)
{
    // Limit the result set to 10 items.
    ItemView view = new ItemView(10);
    view.PropertySet = new PropertySet(ItemSchema.Subject, 
                                       ItemSchema.DateTimeReceived,
                                       EmailMessageSchema.IsRead,
                                       customPropDefinition);
    // Item searches do not support Deep traversal.
    view.Traversal = ItemTraversal.Shallow;
    // Sorting.
    view.OrderBy.Add(ItemSchema.DateTimeReceived, SortDirection.Descending);
    try
    {
        FindItemsResults<Item> results = service.FindItems(folder, filter, view);
        foreach (Item item in results.Items)
        {
            Console.WriteLine("Subject: {0}", item.Subject);
            Console.WriteLine("Id: {0}", item.Id.ToString());
            if (item.ExtendedProperties.Count > 0 &&
                 item.ExtendedProperties[0].PropertyDefinition == customPropDefinition)
            {
                Console.WriteLine("Search Index: {0}", item.ExtendedProperties[0].Value);
            }
            if (item is EmailMessage)
            {
                EmailMessage message = item as EmailMessage;
                Console.WriteLine("Read: {0}", message.IsRead.ToString());
            }
        }
    }
    catch (Exception ex)
    {
        Console.WriteLine("Exception while enumerating results: {0}", ex.Message);
    }
}
```

<span data-ttu-id="8530a-p113">Sie können diese Funktion mit jedem in den Beispielen dieses Artikels veranschaulichten Suchfilter verwenden. In diesem Beispiel wird ein zusammengesetzter Filter verwendet, damit alle Elemente aus dem Posteingang von Sadie Daniels mit „Besprechungsnotizen" im Betreff zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8530a-p113">You can use this function with any of the search filters shown in the examples in this article. This example uses a compound filter to return all items in the Inbox from Sadie Daniels with "meeting notes" in the subject.</span></span>
  
```cs
SearchFilter.ContainsSubstring subjectFilter = new SearchFilter.ContainsSubstring(ItemSchema.Subject,
    "meeting notes", ContainmentMode.Substring, ComparisonMode.IgnoreCase);
EmailAddress manager = new EmailAddress("sadie@contoso.com");
SearchFilter.IsEqualTo fromManagerFilter =
    new SearchFilter.IsEqualTo(EmailMessageSchema.Sender, manager);
SearchFilter.SearchFilterCollection compoundFilter =
    new SearchFilter.SearchFilterCollection(LogicalOperator.And, subjectFilter, greaterThanFilter);
SearchWithFilter(service, WellKnownFolderName.Inbox, compoundFilter);
```

## <a name="example-find-an-item-by-using-a-search-filter-and-ews"></a><span data-ttu-id="8530a-238">Beispiel: Suchen eines Elements mithilfe eines Suchfilters und EWS</span><span class="sxs-lookup"><span data-stu-id="8530a-238">Example: Find an item by using a search filter and EWS</span></span>
<span data-ttu-id="8530a-239"><a name="bk_ExampleEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="8530a-239"></span></span>

<span data-ttu-id="8530a-240">Folgende EWS-Operationen verwenden Suchfilter:</span><span class="sxs-lookup"><span data-stu-id="8530a-240">The following EWS operations use search filters:</span></span>
  
- [<span data-ttu-id="8530a-241">FindFolder</span><span class="sxs-lookup"><span data-stu-id="8530a-241">FindFolder</span></span>](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)
- [<span data-ttu-id="8530a-242">FindItem</span><span class="sxs-lookup"><span data-stu-id="8530a-242">FindItem</span></span>](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    
<span data-ttu-id="8530a-p114">Im folgenden Beispiel wird die **FindItem**-Operation verwendet; die gleichen Regeln und Konzepte gelten jedoch für beide Operationen. Suchfilter sind im [Restriction](http://msdn.microsoft.com/library/77f19014-d112-4999-8e83-ecc32a117a73%28Office.15%29.aspx)-Element in SOAP-Anforderungen enthalten. In diesem Beispiel wird eine SOAP-Anforderung gesendet, die der Suche entspricht, die im vorangegangenen Beispiel der verwalteten EWS-API veranschaulicht wird.</span><span class="sxs-lookup"><span data-stu-id="8530a-p114">The following example uses the **FindItem** operation; however, the same rules and concepts apply to both operations. Search filters are contained in the [Restriction](http://msdn.microsoft.com/library/77f19014-d112-4999-8e83-ecc32a117a73%28Office.15%29.aspx) element in SOAP requests. This example sends a SOAP request that is equivalent to the search that is shown in the preceding EWS Managed API example.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
  <soap:Body>
    <m:FindItem Traversal="Shallow">
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
          <t:FieldURI FieldURI="item:DateTimeReceived" />
          <t:FieldURI FieldURI="message:IsRead" />
          <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:IndexedPageItemView MaxEntriesReturned="10" Offset="0" BasePoint="Beginning" />
      <m:Restriction>
        <t:And>
          <t:Contains ContainmentMode="Substring" ContainmentComparison="IgnoreCase">
            <t:FieldURI FieldURI="item:Subject" />
            <t:Constant Value="meeting notes" />
          </t:Contains>
          <t:IsEqualTo>
            <t:FieldURI FieldURI="message:Sender" />
            <t:FieldURIOrConstant>
              <t:Constant Value="sadie@contoso.com" />
            </t:FieldURIOrConstant>
          </t:IsEqualTo>
        </t:And>
      </m:Restriction>
      <m:SortOrder>
        <t:FieldOrder Order="Descending">
          <t:FieldURI FieldURI="item:DateTimeReceived" />
        </t:FieldOrder>
      </m:SortOrder>
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox" />
      </m:ParentFolderIds>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="8530a-246">Im folgenden Beispiel wird die Antwort vom Server einschließlich der Suchergebnisse veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="8530a-246">The following example shows the response from the server, including the search results.</span></span>
  
```XML
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="712" MinorBuildNumber="22" Version="V2_3" 
        xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="3" TotalItemsInView="3" IncludesLastItemInRange="true">
            <t:Items>
              <t:Message>
                <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                <t:Subject>meeting notes</t:Subject>
                <t:DateTimeReceived>2013-11-20T21:18:51Z</t:DateTimeReceived>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
                  <t:Value>5</t:Value>
                </t:ExtendedProperty>
                <t:IsRead>true</t:IsRead>
              </t:Message>
              <t:Message>
                <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                <t:Subject>Meeting Notes</t:Subject>
                <t:DateTimeReceived>2013-11-20T21:18:51Z</t:DateTimeReceived>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
                  <t:Value>6</t:Value>
                </t:ExtendedProperty>
                <t:IsRead>true</t:IsRead>
              </t:Message>
              <t:Message>
                <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                <t:Subject>Meeting notes</t:Subject>
                <t:DateTimeReceived>2013-11-20T21:18:51Z</t:DateTimeReceived>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertySetId="aa3df801-4fc7-401f-bbc1-7c93d6498c2e" PropertyName="ItemIndex" PropertyType="Integer" />
                  <t:Value>7</t:Value>
                </t:ExtendedProperty>
                <t:IsRead>true</t:IsRead>
              </t:Message>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>
```

## <a name="next-steps"></a><span data-ttu-id="8530a-247">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="8530a-247">Next steps</span></span>
<span data-ttu-id="8530a-248"><a name="bk_ExampleEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="8530a-248"></span></span>

<span data-ttu-id="8530a-249">Nun, da Sie mit der Verwendung von Suchfiltern in einfachen Suchen vertraut sind, können Sie mit den erweiterten Suchmethoden fortfahren.</span><span class="sxs-lookup"><span data-stu-id="8530a-249">Now that you're familiar with using search filters in basic searches, you can move on to more advanced search techniques.</span></span>
  
- [<span data-ttu-id="8530a-250">Führen Sie gruppierte Suchvorgänge in Exchange mithilfe der Exchange-Webdienste aus</span><span class="sxs-lookup"><span data-stu-id="8530a-250">Perform grouped searches by using EWS in Exchange</span></span>](how-to-perform-grouped-searches-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="8530a-251">Führen Sie seitenweise durch Verwenden von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="8530a-251">Perform paged searches by using EWS in Exchange</span></span>](how-to-perform-paged-searches-by-using-ews-in-exchange.md)
    
## <a name="see-also"></a><span data-ttu-id="8530a-252">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8530a-252">See also</span></span>

- [<span data-ttu-id="8530a-253">Suche und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="8530a-253">Search and EWS in Exchange</span></span>](search-and-ews-in-exchange.md)    
- [<span data-ttu-id="8530a-254">Führen Sie eine AQS-Suche mithilfe der EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="8530a-254">Perform an AQS search by using EWS in Exchange</span></span>](how-to-perform-an-aqs-search-by-using-ews-in-exchange.md)   
- [<span data-ttu-id="8530a-255">ExchangeService.FindItems</span><span class="sxs-lookup"><span data-stu-id="8530a-255">ExchangeService.FindItems</span></span>](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)    
- [<span data-ttu-id="8530a-256">ExchangeService.FindFolders</span><span class="sxs-lookup"><span data-stu-id="8530a-256">ExchangeService.FindFolders</span></span>](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx)    
- [<span data-ttu-id="8530a-257">Folder.FindFolders</span><span class="sxs-lookup"><span data-stu-id="8530a-257">Folder.FindFolders</span></span>](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx)    
- [<span data-ttu-id="8530a-258">Folder.FindItems</span><span class="sxs-lookup"><span data-stu-id="8530a-258">Folder.FindItems</span></span>](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx)    
- [<span data-ttu-id="8530a-259">FindFolder Operation</span><span class="sxs-lookup"><span data-stu-id="8530a-259">FindFolder operation</span></span>](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)   
- [<span data-ttu-id="8530a-260">FindItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="8530a-260">FindItem operation</span></span>](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    

