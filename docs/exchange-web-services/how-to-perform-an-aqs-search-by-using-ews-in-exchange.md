---
title: Durchführen einer AQS-Suche mithilfe von EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: c136901a-313e-4adf-a223-1d090d16917a
description: Erfahren Sie, wie Sie mit Abfragezeichenfolgen und AQS in ihrer verwaltete EWS-API-oder EWS-Anwendung suchen.
localization_priority: Priority
ms.openlocfilehash: 9f611a8d90c6baf0f307897735c6366c82bb63c8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455716"
---
# <a name="perform-an-aqs-search-by-using-ews-in-exchange"></a><span data-ttu-id="2f1f3-103">Durchführen einer AQS-Suche mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="2f1f3-103">Perform an AQS search by using EWS in Exchange</span></span>

<span data-ttu-id="2f1f3-104">Erfahren Sie, wie Sie mit Abfragezeichenfolgen und AQS in ihrer verwaltete EWS-API-oder EWS-Anwendung suchen.</span><span class="sxs-lookup"><span data-stu-id="2f1f3-104">Find out how to search with query strings and AQS in your EWS Managed API or EWS application.</span></span>
  
<span data-ttu-id="2f1f3-105">Abfragezeichenfolgen bieten eine Alternative zu [Suchfiltern](how-to-use-search-filters-with-ews-in-exchange.md) zum Ausdrücken von Suchkriterien.</span><span class="sxs-lookup"><span data-stu-id="2f1f3-105">Query strings provide an alternative to [search filters](how-to-use-search-filters-with-ews-in-exchange.md) for expressing search criteria.</span></span> <span data-ttu-id="2f1f3-106">Der größte Vorteil bei der Verwendung von Abfragezeichenfolgen besteht darin, dass Sie keine einzelne zu durchsuchende Eigenschaft angeben müssen.</span><span class="sxs-lookup"><span data-stu-id="2f1f3-106">The biggest advantage to using query strings is that you are not required to specify a single property to search.</span></span> <span data-ttu-id="2f1f3-107">Sie können nur einen Wert angeben, und die Suche wird auf alle häufig verwendeten Felder in den Elementen angewendet.</span><span class="sxs-lookup"><span data-stu-id="2f1f3-107">You can just provide a value, and the search will apply to all commonly used fields on the items.</span></span> <span data-ttu-id="2f1f3-108">Sie können die Suche auch verfeinern, indem Sie die Erweiterte Abfrage Syntax (AQS) anstelle eines einfachen Werts verwenden.</span><span class="sxs-lookup"><span data-stu-id="2f1f3-108">You can also refine your search by using Advanced Query Syntax (AQS) instead of a simple value.</span></span> <span data-ttu-id="2f1f3-109">Abfragezeichenfolgen weisen jedoch die folgenden Einschränkungen auf, die Sie kennen sollten, bevor Sie sie ihrer Toolbox hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="2f1f3-109">However, query strings have the following limitations that you should be aware of before you add them to your toolbox:</span></span> 
  
- <span data-ttu-id="2f1f3-110">**Beschränkte Fähigkeit zum Durchsuchen bestimmter Eigenschaften.**</span><span class="sxs-lookup"><span data-stu-id="2f1f3-110">**Limited ability to search specific properties.**</span></span> <span data-ttu-id="2f1f3-111">Wenn Sie mit einem einfachen Wert in einer Abfragezeichenfolge suchen, wird die Suche für alle indizierten Eigenschaften ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2f1f3-111">When you search with a simple value in a query string, the search is performed against all indexed properties.</span></span> <span data-ttu-id="2f1f3-112">Sie können die Suche auf bestimmte Eigenschaften verfeinern, die verfügbaren Eigenschaften in einer AQS-Zeichenfolge sind jedoch limitiert.</span><span class="sxs-lookup"><span data-stu-id="2f1f3-112">You can refine your search to specific properties, but the properties available to use in an AQS string are limited.</span></span> <span data-ttu-id="2f1f3-113">Wenn die Eigenschaft, die Sie durchsuchen möchten, nicht zu den Eigenschaften gehört, die für AQS verfügbar sind, sollten Sie einen Suchfilter verwenden.</span><span class="sxs-lookup"><span data-stu-id="2f1f3-113">If the property you want to search isn't one of the properties that are available for AQS, consider using a search filter.</span></span> 
    
- <span data-ttu-id="2f1f3-114">**Benutzerdefinierte Eigenschaften werden nicht durchsucht.**</span><span class="sxs-lookup"><span data-stu-id="2f1f3-114">**Custom properties aren't searched.**</span></span> <span data-ttu-id="2f1f3-115">Abfragezeichen folgen suchen werden für einen Index ausgeführt, und benutzerdefinierte Eigenschaften sind nicht in diesem Index enthalten.</span><span class="sxs-lookup"><span data-stu-id="2f1f3-115">Query string searches are performed against an index, and custom properties are not included in that index.</span></span> <span data-ttu-id="2f1f3-116">Wenn Sie benutzerdefinierte Eigenschaften durchsuchen müssen, verwenden Sie stattdessen einen Suchfilter.</span><span class="sxs-lookup"><span data-stu-id="2f1f3-116">If you need to search custom properties, use a search filter instead.</span></span> 
    
- <span data-ttu-id="2f1f3-117">**Beschränkte Steuerung für Zeichenfolgensuchen.**</span><span class="sxs-lookup"><span data-stu-id="2f1f3-117">**Limited control for string searches.**</span></span> <span data-ttu-id="2f1f3-118">Bei Abfragezeichen folgen suchen wird Case immer ignoriert, und es werden immer unter Zeichenfolgen Suchvorgänge durchsucht.</span><span class="sxs-lookup"><span data-stu-id="2f1f3-118">Query string searches always ignore case, and are always substring searches.</span></span> <span data-ttu-id="2f1f3-119">Wenn Sie die Suche nach Groß-/Kleinschreibung, Präfix oder exakte Übereinstimmung durchführen möchten, verwenden Sie einen Suchfilter.</span><span class="sxs-lookup"><span data-stu-id="2f1f3-119">If you want to do case-sensitive, prefix, or exact match searches, use a search filter.</span></span> 
    
- <span data-ttu-id="2f1f3-120">**Nicht verfügbar für Ordner oder Suchordner.**</span><span class="sxs-lookup"><span data-stu-id="2f1f3-120">**Not available for folders or search folders.**</span></span> <span data-ttu-id="2f1f3-121">Die EWS-Vorgänge für die Suche nach Ordnern unterstützen nicht die Verwendung einer Abfragezeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="2f1f3-121">The EWS operations for searching for folders don't support using a query string.</span></span> <span data-ttu-id="2f1f3-122">Außerdem unterstützen Suchordner keine Abfragezeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="2f1f3-122">Additionally, search folders don't support query strings.</span></span> <span data-ttu-id="2f1f3-123">In beiden Fällen ist ein Suchfilter die einzige Option.</span><span class="sxs-lookup"><span data-stu-id="2f1f3-123">In both cases, a search filter is your only option.</span></span> 
    
## <a name="creating-a-query-string"></a><span data-ttu-id="2f1f3-124">Erstellen einer Abfragezeichenfolge</span><span class="sxs-lookup"><span data-stu-id="2f1f3-124">Creating a query string</span></span>
<span data-ttu-id="2f1f3-125"><a name="bk_CreateQueryString"> </a></span><span class="sxs-lookup"><span data-stu-id="2f1f3-125"><a name="bk_CreateQueryString"> </a></span></span>

<span data-ttu-id="2f1f3-126">Abfragezeichenfolgen im verwaltete EWS-API und EWS werden als Teilmenge der AQS-Syntax interpretiert.</span><span class="sxs-lookup"><span data-stu-id="2f1f3-126">Query strings in the EWS Managed API and EWS are interpreted as a subset of AQS syntax.</span></span> <span data-ttu-id="2f1f3-127">AQS-Zeichenfolgen bestehen entweder aus Werten oder aus Schlüsselwort/Wert-Paaren, getrennt durch einen Doppelpunkt (:).</span><span class="sxs-lookup"><span data-stu-id="2f1f3-127">AQS strings are composed of either values or keyword/value pairs, separated by a colon (:).</span></span>
  
`keyword:value`

<span data-ttu-id="2f1f3-128">Wenn ein Wert ohne Schlüsselwort angegeben wird, werden alle indizierten Eigenschaften nach dem Wert durchsucht.</span><span class="sxs-lookup"><span data-stu-id="2f1f3-128">When a value is specified without a keyword, all indexed properties are searched for the value.</span></span> <span data-ttu-id="2f1f3-129">Wenn ein Schlüsselwort mit einem Wert gekoppelt wird, gibt das Schlüsselwort eine Eigenschaft zum Suchen nach dem entsprechenden Wert an.</span><span class="sxs-lookup"><span data-stu-id="2f1f3-129">If a keyword is paired with a value, the keyword specifies a property to search for the corresponding value.</span></span>
  
<span data-ttu-id="2f1f3-130">**Tabelle 1. Unterstützte AQS-Schlüsselwörter**</span><span class="sxs-lookup"><span data-stu-id="2f1f3-130">**Table 1. Supported AQS keywords**</span></span>

|<span data-ttu-id="2f1f3-131">**Schlüsselwort**</span><span class="sxs-lookup"><span data-stu-id="2f1f3-131">**Keyword**</span></span>|<span data-ttu-id="2f1f3-132">**Werttyp**</span><span class="sxs-lookup"><span data-stu-id="2f1f3-132">**Value type**</span></span>|<span data-ttu-id="2f1f3-133">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="2f1f3-133">**Example**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2f1f3-134">Betreff</span><span class="sxs-lookup"><span data-stu-id="2f1f3-134">subject</span></span>  <br/> |<span data-ttu-id="2f1f3-135">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="2f1f3-135">String</span></span>  <br/> |<span data-ttu-id="2f1f3-136">Betreff: Project</span><span class="sxs-lookup"><span data-stu-id="2f1f3-136">subject:project</span></span>  <br/> |
|<span data-ttu-id="2f1f3-137">body</span><span class="sxs-lookup"><span data-stu-id="2f1f3-137">body</span></span>  <br/> |<span data-ttu-id="2f1f3-138">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="2f1f3-138">String</span></span>  <br/> |<span data-ttu-id="2f1f3-139">Body: Verkaufszahlen</span><span class="sxs-lookup"><span data-stu-id="2f1f3-139">body:sales figures</span></span>  <br/> |
|<span data-ttu-id="2f1f3-140">attachment</span><span class="sxs-lookup"><span data-stu-id="2f1f3-140">attachment</span></span>  <br/> |<span data-ttu-id="2f1f3-141">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="2f1f3-141">String</span></span>  <br/> |<span data-ttu-id="2f1f3-142">Anlage: Bericht</span><span class="sxs-lookup"><span data-stu-id="2f1f3-142">attachment:report</span></span>  <br/> |
|<span data-ttu-id="2f1f3-143">in</span><span class="sxs-lookup"><span data-stu-id="2f1f3-143">to</span></span>  <br/> |<span data-ttu-id="2f1f3-144">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="2f1f3-144">String</span></span>  <br/> |<span data-ttu-id="2f1f3-145">an: "Sadie Daniels"</span><span class="sxs-lookup"><span data-stu-id="2f1f3-145">to:"Sadie Daniels"</span></span>  <br/> |
|<span data-ttu-id="2f1f3-146">Von</span><span class="sxs-lookup"><span data-stu-id="2f1f3-146">from</span></span>  <br/> |<span data-ttu-id="2f1f3-147">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="2f1f3-147">String</span></span>  <br/> |<span data-ttu-id="2f1f3-148">von: Hope</span><span class="sxs-lookup"><span data-stu-id="2f1f3-148">from:hope</span></span>  <br/> |
|<span data-ttu-id="2f1f3-149">cc</span><span class="sxs-lookup"><span data-stu-id="2f1f3-149">cc</span></span>  <br/> |<span data-ttu-id="2f1f3-150">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="2f1f3-150">String</span></span>  <br/> |<span data-ttu-id="2f1f3-151">cc: "Ronnie Kardinal"</span><span class="sxs-lookup"><span data-stu-id="2f1f3-151">cc:"Ronnie Sturgis"</span></span>  <br/> |
|<span data-ttu-id="2f1f3-152">bcc</span><span class="sxs-lookup"><span data-stu-id="2f1f3-152">bcc</span></span>  <br/> |<span data-ttu-id="2f1f3-153">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="2f1f3-153">String</span></span>  <br/> |<span data-ttu-id="2f1f3-154">BCC: Mack</span><span class="sxs-lookup"><span data-stu-id="2f1f3-154">bcc:mack</span></span>  <br/> |
|<span data-ttu-id="2f1f3-155">participants</span><span class="sxs-lookup"><span data-stu-id="2f1f3-155">participants</span></span>  <br/> |<span data-ttu-id="2f1f3-156">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="2f1f3-156">String</span></span>  <br/> |<span data-ttu-id="2f1f3-157">Teilnehmer: Sadie</span><span class="sxs-lookup"><span data-stu-id="2f1f3-157">participants:sadie</span></span>  <br/> |
|<span data-ttu-id="2f1f3-158">category</span><span class="sxs-lookup"><span data-stu-id="2f1f3-158">category</span></span>  <br/> |<span data-ttu-id="2f1f3-159">String</span><span class="sxs-lookup"><span data-stu-id="2f1f3-159">String</span></span>  <br/> |<span data-ttu-id="2f1f3-160">Kategorie: Project</span><span class="sxs-lookup"><span data-stu-id="2f1f3-160">category:project</span></span>  <br/> |
|<span data-ttu-id="2f1f3-161">Wichtigkeit</span><span class="sxs-lookup"><span data-stu-id="2f1f3-161">importance</span></span>  <br/> |<span data-ttu-id="2f1f3-162">String</span><span class="sxs-lookup"><span data-stu-id="2f1f3-162">String</span></span>  <br/> |<span data-ttu-id="2f1f3-163">Wichtigkeit:Hoch</span><span class="sxs-lookup"><span data-stu-id="2f1f3-163">importance:high</span></span>  <br/> |
|<span data-ttu-id="2f1f3-164">kind</span><span class="sxs-lookup"><span data-stu-id="2f1f3-164">kind</span></span>  <br/> |<span data-ttu-id="2f1f3-165">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="2f1f3-165">Item type</span></span>  <br/> |<span data-ttu-id="2f1f3-166">Art: Besprechungen</span><span class="sxs-lookup"><span data-stu-id="2f1f3-166">kind:meetings</span></span>  <br/> |
|<span data-ttu-id="2f1f3-167">sent</span><span class="sxs-lookup"><span data-stu-id="2f1f3-167">sent</span></span>  <br/> |<span data-ttu-id="2f1f3-168">Datum</span><span class="sxs-lookup"><span data-stu-id="2f1f3-168">Date</span></span>  <br/> |<span data-ttu-id="2f1f3-169">gesendet: 12/10/2013</span><span class="sxs-lookup"><span data-stu-id="2f1f3-169">sent:12/10/2013</span></span>  <br/> |
|<span data-ttu-id="2f1f3-170">received</span><span class="sxs-lookup"><span data-stu-id="2f1f3-170">received</span></span>  <br/> |<span data-ttu-id="2f1f3-171">Datum</span><span class="sxs-lookup"><span data-stu-id="2f1f3-171">Date</span></span>  <br/> |<span data-ttu-id="2f1f3-172">empfangen: Gestern</span><span class="sxs-lookup"><span data-stu-id="2f1f3-172">received:yesterday</span></span>  <br/> |
|<span data-ttu-id="2f1f3-173">hatanlage</span><span class="sxs-lookup"><span data-stu-id="2f1f3-173">hasattachment</span></span>  <br/> |<span data-ttu-id="2f1f3-174">Boolean</span><span class="sxs-lookup"><span data-stu-id="2f1f3-174">Boolean</span></span>  <br/> |<span data-ttu-id="2f1f3-175">Has-Anlage: true</span><span class="sxs-lookup"><span data-stu-id="2f1f3-175">Has attachment:true</span></span>  <br/> |
|<span data-ttu-id="2f1f3-176">isflaged</span><span class="sxs-lookup"><span data-stu-id="2f1f3-176">isflagged</span></span>  <br/> |<span data-ttu-id="2f1f3-177">Boolean</span><span class="sxs-lookup"><span data-stu-id="2f1f3-177">Boolean</span></span>  <br/> |<span data-ttu-id="2f1f3-178">isflaged: true</span><span class="sxs-lookup"><span data-stu-id="2f1f3-178">isflagged:true</span></span>  <br/> |
|<span data-ttu-id="2f1f3-179">isread</span><span class="sxs-lookup"><span data-stu-id="2f1f3-179">isread</span></span>  <br/> |<span data-ttu-id="2f1f3-180">Boolean</span><span class="sxs-lookup"><span data-stu-id="2f1f3-180">Boolean</span></span>  <br/> |<span data-ttu-id="2f1f3-181">isread: false</span><span class="sxs-lookup"><span data-stu-id="2f1f3-181">isread:false</span></span>  <br/> |
|<span data-ttu-id="2f1f3-182">size</span><span class="sxs-lookup"><span data-stu-id="2f1f3-182">size</span></span>  <br/> |<span data-ttu-id="2f1f3-183">Nummer</span><span class="sxs-lookup"><span data-stu-id="2f1f3-183">Number</span></span>  <br/> |<span data-ttu-id="2f1f3-184">Größe: \> 5000</span><span class="sxs-lookup"><span data-stu-id="2f1f3-184">size:\>5000</span></span>  <br/> |
   
<span data-ttu-id="2f1f3-185">Werfen wir einen Blick auf die Funktionsweise der unterschiedlichen Wertetypen.</span><span class="sxs-lookup"><span data-stu-id="2f1f3-185">Let's take a look at how the different value types work.</span></span>
  
### <a name="using-a-string-value-type"></a><span data-ttu-id="2f1f3-186">Verwenden eines Zeichenfolgen Werttyp</span><span class="sxs-lookup"><span data-stu-id="2f1f3-186">Using a string value type</span></span>

<span data-ttu-id="2f1f3-187">Zeichenfolgenwerte Typen werden standardmäßig als Präfix-Teil Zeichenfolgensuche durchsucht, bei denen die Groß-/Kleinschreibung nicht beachtet wird.</span><span class="sxs-lookup"><span data-stu-id="2f1f3-187">String value types are by default searched as prefix substring searches that are not case-sensitive.</span></span> <span data-ttu-id="2f1f3-188">Das bedeutet, dass die Suche nach Subject: Project mit einem der folgenden Themen übereinstimmen würde:</span><span class="sxs-lookup"><span data-stu-id="2f1f3-188">That means that searching for subject:project would match any of the following subjects:</span></span> 
  
- <span data-ttu-id="2f1f3-189">Projekt-Besprechungsnotizen</span><span class="sxs-lookup"><span data-stu-id="2f1f3-189">Project meeting notes</span></span>
    
- <span data-ttu-id="2f1f3-190">Haben Sie die Projektpläne?</span><span class="sxs-lookup"><span data-stu-id="2f1f3-190">Do you have the project plans?</span></span>
    
- <span data-ttu-id="2f1f3-191">Verkaufsprognosen im Dezember</span><span class="sxs-lookup"><span data-stu-id="2f1f3-191">December sales projections</span></span>
    
<span data-ttu-id="2f1f3-192">Sie können die Suche so ändern, dass das ganze Wort statt übereinstimmender Präfixe erforderlich ist, indem Sie die Zeichenfolge in Anführungszeichen einschließen.</span><span class="sxs-lookup"><span data-stu-id="2f1f3-192">You can change the search to require the whole word rather than matching prefixes by enclosing the string in quotation marks.</span></span> <span data-ttu-id="2f1f3-193">Durchsuchen des Betreffs: "Project" würde den Wert "Dezember Sales Projektionen" aus der Liste der Übereinstimmungen ausschließen.</span><span class="sxs-lookup"><span data-stu-id="2f1f3-193">Searching for subject:"project" would eliminate the "December sales projections" value from the list of matches.</span></span> <span data-ttu-id="2f1f3-194">Beachten Sie, dass bei dem Wert weiterhin die Groß-/Kleinschreibung beachtet wird.</span><span class="sxs-lookup"><span data-stu-id="2f1f3-194">Note that the value is still not case-sensitive.</span></span> 
  
<span data-ttu-id="2f1f3-195">Wenn Sie mehrere Wörter in einer Abfragezeichenfolge verwenden, erfordert eine Übereinstimmung, dass beide Wörter in den durchsuchten Feldern angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="2f1f3-195">If you use multiple words in a query string, a match requires that both words appear in the searched fields.</span></span> <span data-ttu-id="2f1f3-196">Beispielsweise würde die Suche nach Subject: Project Plan mit einem der folgenden Themen übereinstimmen:</span><span class="sxs-lookup"><span data-stu-id="2f1f3-196">For example, searching for subject:project plan would match any of the following subjects:</span></span> 
  
- <span data-ttu-id="2f1f3-197">Projektplan</span><span class="sxs-lookup"><span data-stu-id="2f1f3-197">Project plan</span></span>
    
- <span data-ttu-id="2f1f3-198">Haben Sie die Projektpläne?</span><span class="sxs-lookup"><span data-stu-id="2f1f3-198">Do you have the project plans?</span></span>
    
- <span data-ttu-id="2f1f3-199">Bitte senden Sie mir den Plan für unser Projekt</span><span class="sxs-lookup"><span data-stu-id="2f1f3-199">Please send me the plan for our project</span></span>
    
- <span data-ttu-id="2f1f3-200">Planen von Projektmeilensteinen</span><span class="sxs-lookup"><span data-stu-id="2f1f3-200">Planning project milestones</span></span>
    
<span data-ttu-id="2f1f3-201">Wenn Sie mehrere Wörter in Anführungszeichen einschließen, werden Sie als einzelne Phrase behandelt.</span><span class="sxs-lookup"><span data-stu-id="2f1f3-201">If you enclose multiple words in quotation marks, they are treated as a single phrase.</span></span> <span data-ttu-id="2f1f3-202">Die Suche nach Betreff: "Projektplan" würde nur dem Betreff "Projektplan" aus der vorherigen Liste entsprechen.</span><span class="sxs-lookup"><span data-stu-id="2f1f3-202">Searching for subject:"project plan" would only match the "Project plan" subject from the previous list.</span></span> 
  
### <a name="using-an-item-type-value-type"></a><span data-ttu-id="2f1f3-203">Verwenden eines Werttyp Werts für den Typ "Item"</span><span class="sxs-lookup"><span data-stu-id="2f1f3-203">Using an item type value type</span></span>

<span data-ttu-id="2f1f3-204">Sie können die folgenden Elementtyp Werte mit dem Schlüsselwort **Kind** verwenden, um die Suchergebnisse auf einen bestimmten Elementtyp wie e-Mail oder Besprechungsanfragen einzuschränken:</span><span class="sxs-lookup"><span data-stu-id="2f1f3-204">You can use the following item type values with the **kind** keyword to limit your search results to only a specific type of item, such as email or meeting requests:</span></span> 
  
- <span data-ttu-id="2f1f3-205">contacts</span><span class="sxs-lookup"><span data-stu-id="2f1f3-205">contacts</span></span>    
- <span data-ttu-id="2f1f3-206">docs</span><span class="sxs-lookup"><span data-stu-id="2f1f3-206">docs</span></span>    
- <span data-ttu-id="2f1f3-207">email</span><span class="sxs-lookup"><span data-stu-id="2f1f3-207">email</span></span>    
- <span data-ttu-id="2f1f3-208">faxes</span><span class="sxs-lookup"><span data-stu-id="2f1f3-208">faxes</span></span>    
- <span data-ttu-id="2f1f3-209">Chat (entspricht Chatnachrichten)</span><span class="sxs-lookup"><span data-stu-id="2f1f3-209">im (corresponds to instant messages)</span></span>    
- <span data-ttu-id="2f1f3-210">journals</span><span class="sxs-lookup"><span data-stu-id="2f1f3-210">journals</span></span>    
- <span data-ttu-id="2f1f3-211">Besprechungen (entspricht Terminen und Besprechungsanfragen)</span><span class="sxs-lookup"><span data-stu-id="2f1f3-211">meetings (corresponds to appointments and meeting requests)</span></span>    
- <span data-ttu-id="2f1f3-212">notes</span><span class="sxs-lookup"><span data-stu-id="2f1f3-212">notes</span></span>    
- <span data-ttu-id="2f1f3-213">posts</span><span class="sxs-lookup"><span data-stu-id="2f1f3-213">posts</span></span>    
- <span data-ttu-id="2f1f3-214">rssfeeds</span><span class="sxs-lookup"><span data-stu-id="2f1f3-214">rssfeeds</span></span>    
- <span data-ttu-id="2f1f3-215">tasks</span><span class="sxs-lookup"><span data-stu-id="2f1f3-215">tasks</span></span>    
- <span data-ttu-id="2f1f3-216">voicemail</span><span class="sxs-lookup"><span data-stu-id="2f1f3-216">voicemail</span></span>
    
### <a name="using-a-date-value-type"></a><span data-ttu-id="2f1f3-217">Verwenden eines Datums Werttyp</span><span class="sxs-lookup"><span data-stu-id="2f1f3-217">Using a date value type</span></span>

<span data-ttu-id="2f1f3-218">Sie können Datumswert Typen auf verschiedene Weise durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="2f1f3-218">You can search date value types in a number of different ways.</span></span> <span data-ttu-id="2f1f3-219">Am einfachsten ist die Suche nach einem bestimmten Datum.</span><span class="sxs-lookup"><span data-stu-id="2f1f3-219">The simplest is to search for a specific date.</span></span> <span data-ttu-id="2f1f3-220">Bei der Suche mit Received: 12/11/2013 werden alle Elemente zurückgegeben, die am 11. Dezember 2013 empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="2f1f3-220">Searching with received:12/11/2013 will return all items received on December 11, 2013.</span></span> <span data-ttu-id="2f1f3-221">Sie können jedoch auch nicht so spezifisch sein.</span><span class="sxs-lookup"><span data-stu-id="2f1f3-221">However, you can also be less specific.</span></span> <span data-ttu-id="2f1f3-222">Bei der Suche mit Received: 12/11 werden alle Elemente zurückgegeben, die am 11. Dezember des aktuellen Jahres empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="2f1f3-222">Searching with received:12/11 will return all items received on December 11 of the current year.</span></span> 
  
<span data-ttu-id="2f1f3-223">Eine weitere Option besteht darin, die Monatsnamen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="2f1f3-223">Another option is to use the month names.</span></span> <span data-ttu-id="2f1f3-224">Sie können mit received suchen: 11. Dezember 2013 oder 11. Dezember, um die gleichen Ergebnisse wie empfangen zu erhalten: 12/11/2013 und Received: 12/11, beziehungsweise.</span><span class="sxs-lookup"><span data-stu-id="2f1f3-224">You can search with received:December 11, 2013 or December 11 to get the same results as received:12/11/2013 and received:12/11, respectively.</span></span> <span data-ttu-id="2f1f3-225">Sie können auch mit Received: Dezember suchen, um alle Elemente abzurufen, die im Monat Dezember im aktuellen Jahr empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="2f1f3-225">You can also search with received:December to get all items received in the month of December, in the current year.</span></span> 
  
<span data-ttu-id="2f1f3-226">Die Verwendung der Namen der Wochentage ist ebenfalls eine Option.</span><span class="sxs-lookup"><span data-stu-id="2f1f3-226">Using the names of the days of the week is also an option.</span></span> <span data-ttu-id="2f1f3-227">Bei der Suche mit Received: Dienstag werden alle Elemente zurückgegeben, die am Dienstag der aktuellen Woche empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="2f1f3-227">Searching with received:Tuesday will return all items received on Tuesday of the current week.</span></span> 
  
<span data-ttu-id="2f1f3-228">Datumswert Typen unterstützen auch eine Reihe von Schlüsselwörtern für Suchvorgänge relativ zur aktuellen Uhrzeit.</span><span class="sxs-lookup"><span data-stu-id="2f1f3-228">Date value types also support a set of keywords for searches relative to the current time.</span></span> <span data-ttu-id="2f1f3-229">Die folgenden Schlüsselwörter werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="2f1f3-229">The following keywords are supported:</span></span>
  
- <span data-ttu-id="2f1f3-230">heute</span><span class="sxs-lookup"><span data-stu-id="2f1f3-230">today</span></span>  
- <span data-ttu-id="2f1f3-231">morgen</span><span class="sxs-lookup"><span data-stu-id="2f1f3-231">tomorrow</span></span>
- <span data-ttu-id="2f1f3-232">yesterday</span><span class="sxs-lookup"><span data-stu-id="2f1f3-232">yesterday</span></span>
- <span data-ttu-id="2f1f3-233">this week</span><span class="sxs-lookup"><span data-stu-id="2f1f3-233">this week</span></span>    
- <span data-ttu-id="2f1f3-234">Letzte Woche</span><span class="sxs-lookup"><span data-stu-id="2f1f3-234">last week</span></span>    
- <span data-ttu-id="2f1f3-235">Nächster Monat</span><span class="sxs-lookup"><span data-stu-id="2f1f3-235">next month</span></span>    
- <span data-ttu-id="2f1f3-236">vergangener Monat</span><span class="sxs-lookup"><span data-stu-id="2f1f3-236">past month</span></span>    
- <span data-ttu-id="2f1f3-237">kommendes Jahr</span><span class="sxs-lookup"><span data-stu-id="2f1f3-237">coming year</span></span>
    
<span data-ttu-id="2f1f3-238">Datumswert Typen können auch mit relationalen Operatoren wie größer als oder kleiner als oder als Bereich mit dem Range-Operator angegeben werden **..**. Angenommen: \> 11/30/2013, Sent: \> = Yesterday und Received: 12/1/2013.. heute sind alle gültigen Abfragezeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="2f1f3-238">Date value types can also be compared with relational operators like greater than or less than, or specified as a range with the range operator **..**. For example, received:\>11/30/2013, sent:\>=yesterday, and received:12/1/2013..today are all valid query strings.</span></span> 
  
### <a name="using-a-boolean-value-type"></a><span data-ttu-id="2f1f3-239">Verwenden eines Werts vom Typ Boolean</span><span class="sxs-lookup"><span data-stu-id="2f1f3-239">Using a Boolean value type</span></span>

<span data-ttu-id="2f1f3-240">Boolesche Wertetypen können "true" oder "false" lauten.</span><span class="sxs-lookup"><span data-stu-id="2f1f3-240">Boolean value types can be "true" or "false".</span></span> <span data-ttu-id="2f1f3-241">Bei den Werten wird die Groß-/Kleinschreibung nicht beachtet, daher erzeugt isread: false dieselben Ergebnisse wie isread: false.</span><span class="sxs-lookup"><span data-stu-id="2f1f3-241">The values are not case-sensitive, so isread:false will produce the same results as isread:FALSE.</span></span>
  
### <a name="using-a-number-value-type"></a><span data-ttu-id="2f1f3-242">Verwenden eines Zahlen Werttyp</span><span class="sxs-lookup"><span data-stu-id="2f1f3-242">Using a number value type</span></span>

<span data-ttu-id="2f1f3-243">Zahl Wert Typen können als exakte Übereinstimmungen durchsucht werden, Sie können aber auch mithilfe relationaler Operatoren wie größer als oder kleiner als durchsucht werden.</span><span class="sxs-lookup"><span data-stu-id="2f1f3-243">Number value types can be searched as exact matches, but they can also be searched using relational operators like greater than or less than.</span></span> <span data-ttu-id="2f1f3-244">Beispielsweise gibt size: 10000 nur Elemente zurück, die eine Größe von genau 10000 Bytes aufweisen, aber size: \> = 10000 gibt Elemente zurück, deren Größe größer als oder gleich 10000 Bytes ist.</span><span class="sxs-lookup"><span data-stu-id="2f1f3-244">For example, size:10000 will return only items that have a size of exactly 10000 bytes, but size:\>=10000 will return items that have a size greater than or equal to 10000 bytes.</span></span> <span data-ttu-id="2f1f3-245">Sie können auch einen Bereich mithilfe des Bereichsoperators ( **..**) angeben.</span><span class="sxs-lookup"><span data-stu-id="2f1f3-245">You can also specify a range by using the range operator ( **..**).</span></span> <span data-ttu-id="2f1f3-246">Beispielsweise gibt size: 7000.. 8000 Elemente zurück, die eine Größe zwischen 7000 und 8000 haben.</span><span class="sxs-lookup"><span data-stu-id="2f1f3-246">For example, size:7000..8000 will return items that have a size between 7000 and 8000.</span></span> 
  
### <a name="using-logical-operators"></a><span data-ttu-id="2f1f3-247">Verwenden von logischen Operatoren</span><span class="sxs-lookup"><span data-stu-id="2f1f3-247">Using logical operators</span></span>

<span data-ttu-id="2f1f3-248">Abfragezeichenfolgen unterstützen die folgenden logischen Operatoren.</span><span class="sxs-lookup"><span data-stu-id="2f1f3-248">Query strings support the following logical operators.</span></span>
  
<span data-ttu-id="2f1f3-249">**Tabelle 2. Unterstützte logische Operatoren**</span><span class="sxs-lookup"><span data-stu-id="2f1f3-249">**Table 2. Supported logical operators**</span></span>

|<span data-ttu-id="2f1f3-250">**Operator**</span><span class="sxs-lookup"><span data-stu-id="2f1f3-250">**Operator**</span></span>|<span data-ttu-id="2f1f3-251">**Beispiele**</span><span class="sxs-lookup"><span data-stu-id="2f1f3-251">**Examples**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2f1f3-252">UND</span><span class="sxs-lookup"><span data-stu-id="2f1f3-252">AND</span></span>  <br/> |<span data-ttu-id="2f1f3-253">Projekt und von: "Sadie Daniels"</span><span class="sxs-lookup"><span data-stu-id="2f1f3-253">project AND from:"Sadie Daniels"</span></span>  <br/> <span data-ttu-id="2f1f3-254">Subject: (Projekt und Plan)</span><span class="sxs-lookup"><span data-stu-id="2f1f3-254">subject:(project AND plan)</span></span>  <br/> |
|<span data-ttu-id="2f1f3-255">ODER</span><span class="sxs-lookup"><span data-stu-id="2f1f3-255">OR</span></span>  <br/> |<span data-ttu-id="2f1f3-256">Betreff: Meeting oder von: "Hope gross"</span><span class="sxs-lookup"><span data-stu-id="2f1f3-256">subject:meeting OR from:"Hope Gross"</span></span>  <br/> <span data-ttu-id="2f1f3-257">aus:("Sadie Daniels" oder "Hope gross")</span><span class="sxs-lookup"><span data-stu-id="2f1f3-257">from:("Sadie Daniels" OR "Hope Gross")</span></span>  <br/> |
|<span data-ttu-id="2f1f3-258">NICHT</span><span class="sxs-lookup"><span data-stu-id="2f1f3-258">NOT</span></span>  <br/> |<span data-ttu-id="2f1f3-259">Nicht von: "Ronnie McCulloch"</span><span class="sxs-lookup"><span data-stu-id="2f1f3-259">NOT from:"Ronnie Sturgis"</span></span>  <br/> <span data-ttu-id="2f1f3-260">empfangen: nicht heute</span><span class="sxs-lookup"><span data-stu-id="2f1f3-260">received:NOT today</span></span>  <br/> |
   
<span data-ttu-id="2f1f3-261">Beachten Sie, dass Sie diese Operatoren verwenden können, um mehrere Kriterien miteinander zu verknüpfen oder um mehrere Werte in einem einzelnen Schlüsselwort/Wert-Paar miteinander zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="2f1f3-261">Notice that you can use these operators to join multiple criteria together or to join multiple values within a single keyword/value pair together.</span></span> <span data-ttu-id="2f1f3-262">Wenn Sie jedoch mehrere Werte in einem einzelnen Schlüsselwort/Wert-Paar verknüpfen, sollten Sie Klammern verwenden, um mehrere Werte einzuschließen.</span><span class="sxs-lookup"><span data-stu-id="2f1f3-262">However, when joining multiple values in a single keyword/value pair, you should use parentheses to enclose the multiple values.</span></span> <span data-ttu-id="2f1f3-263">Um zu verstehen, warum, sollten Sie die Suche mit von: "Sadie Daniels" oder "Hope gross".</span><span class="sxs-lookup"><span data-stu-id="2f1f3-263">To understand why, consider searching with from:"Sadie Daniels" OR "Hope Gross".</span></span> <span data-ttu-id="2f1f3-264">Diese Suche wird tatsächlich als die folgenden Kriterien interpretiert:</span><span class="sxs-lookup"><span data-stu-id="2f1f3-264">This search actually is interpreted as the following criteria:</span></span>
  
- <span data-ttu-id="2f1f3-265">Das Element stammt aus Sadie Daniels oder</span><span class="sxs-lookup"><span data-stu-id="2f1f3-265">The item is from Sadie Daniels, OR</span></span>
    
- <span data-ttu-id="2f1f3-266">Das Element hat den Ausdruck "Hope gross" in einer seiner indizierten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2f1f3-266">The item has the phrase "Hope Gross" in any of its indexed properties.</span></span>
    
<span data-ttu-id="2f1f3-267">Im Gegensatz dazu wird aus:("Sadie Daniels" oder "Hope gross") als Folgendes interpretiert:</span><span class="sxs-lookup"><span data-stu-id="2f1f3-267">In contrast, from:("Sadie Daniels" OR "Hope Gross") is interpreted as:</span></span> 
  
- <span data-ttu-id="2f1f3-268">Das Element stammt aus Sadie Daniels oder</span><span class="sxs-lookup"><span data-stu-id="2f1f3-268">The item is from Sadie Daniels, OR</span></span>
    
- <span data-ttu-id="2f1f3-269">Das Element ist von der Hoffnung Brutto</span><span class="sxs-lookup"><span data-stu-id="2f1f3-269">The item is from Hope Gross</span></span>
    
<span data-ttu-id="2f1f3-270">Der Standardoperator, wenn mehrere Kriterien angegeben werden, aber kein logischer Operator enthalten ist, ist und.</span><span class="sxs-lookup"><span data-stu-id="2f1f3-270">The default operator when multiple criteria are specified but no logical operator is included is AND.</span></span> <span data-ttu-id="2f1f3-271">Enthält beispielsweise Attachment: true Subject: Project entspricht has: Attachment: true und Subject: Project.</span><span class="sxs-lookup"><span data-stu-id="2f1f3-271">For example, has attachment:true subject:project is equivalent to has:attachment:true AND subject:project.</span></span>
  
## <a name="example-find-items-by-using-a-query-string-and-the-ews-managed-api"></a><span data-ttu-id="2f1f3-272">Beispiel: Suchen von Elementen mithilfe einer Abfragezeichenfolge und der verwaltete EWS-API</span><span class="sxs-lookup"><span data-stu-id="2f1f3-272">Example: Find items by using a query string and the EWS Managed API</span></span>
<span data-ttu-id="2f1f3-273"><a name="bk_ExampleEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="2f1f3-273"><a name="bk_ExampleEWSMA"> </a></span></span>

<span data-ttu-id="2f1f3-274">In diesem Beispiel wird eine Methode namens " **SearchWithQueryString** " definiert.</span><span class="sxs-lookup"><span data-stu-id="2f1f3-274">In this example, a method called **SearchWithQueryString** is defined.</span></span> <span data-ttu-id="2f1f3-275">Es benötigt ein [Datei "ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objekt, ein [WellKnownFolderName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) -Objekt und ein **String** -Objekt, das die Abfragezeichenfolge als Parameter darstellt.</span><span class="sxs-lookup"><span data-stu-id="2f1f3-275">It takes an [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object, a [WellKnownFolderName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) object, and a **string** object that represents the query string as parameters.</span></span> <span data-ttu-id="2f1f3-276">In diesem Beispiel wird davon ausgegangen, dass das **ExchangeService**-Objekt mit gültigen Werten in den [Credentials](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx)- und [Url](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx)-Eigenschaften initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="2f1f3-276">This example assumes that the **ExchangeService** object has been initialized with valid values in the [Credentials](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) and [Url](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) properties.</span></span> 
  
```cs
using Microsoft.Exchange.WebServices.Data;
static void SearchWithQueryString(ExchangeService service, WellKnownFolderName folder, string queryString)
{
    // Limit the result set to 10 items.
    ItemView view = new ItemView(10);
    view.PropertySet = new PropertySet(ItemSchema.Subject,
                                       ItemSchema.DateTimeReceived,
                                       ItemSchema.Size,
                                       ItemSchema.Importance,
                                       EmailMessageSchema.IsRead);
    // Item searches do not support Deep traversal.
    view.Traversal = ItemTraversal.Shallow;
    // Sorting
    view.OrderBy.Add(ItemSchema.DateTimeReceived, SortDirection.Descending);
    try
    {
        // Execute the search based on the query string.
        // Example: "subject:project plan"
        FindItemsResults<Item> results = service.FindItems(folder, queryString, view);
        foreach (Item item in results.Items)
        {
            Console.WriteLine("Subject: {0}", item.Subject);
            Console.WriteLine("Received: {0}", item.DateTimeReceived.ToString());
            Console.WriteLine("Size: {0}", item.Size.ToString());
            Console.WriteLine("Importance: {0}", item.Importance.ToString());
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

<span data-ttu-id="2f1f3-277">Sie können diese Methode verwenden, um nach allen Elementen mit dem Ausdruck "Projektplan" im Betreff zu suchen, wie in diesem Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="2f1f3-277">You can use this method to search for all items with the phrase "project plan" in the subject, as shown in this example.</span></span>
  
```cs
string queryString = "subject:\"project plan\"";
SearchWithQueryString(service, WellKnownFolderName.Inbox, queryString);
```

## <a name="example-find-items-by-using-a-query-string-and-ews"></a><span data-ttu-id="2f1f3-278">Beispiel: Suchen von Elementen mithilfe einer Abfragezeichenfolge und EWS</span><span class="sxs-lookup"><span data-stu-id="2f1f3-278">Example: Find items by using a query string and EWS</span></span>
<span data-ttu-id="2f1f3-279"><a name="bk_ExampleEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="2f1f3-279"><a name="bk_ExampleEWS"> </a></span></span>

<span data-ttu-id="2f1f3-280">In diesem Beispiel findet eine SOAP- [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) -Anforderung alle Elemente im Posteingang mit dem Ausdruck "Projektplan" im Betreff.</span><span class="sxs-lookup"><span data-stu-id="2f1f3-280">In this example, a SOAP [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) request finds all items in the Inbox with the phrase "project plan" in the subject.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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
          <t:FieldURI FieldURI="item:Size" />
          <t:FieldURI FieldURI="item:Importance" />
          <t:FieldURI FieldURI="message:IsRead" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:IndexedPageItemView MaxEntriesReturned="10" Offset="0" BasePoint="Beginning" />
      <m:SortOrder>
        <t:FieldOrder Order="Descending">
          <t:FieldURI FieldURI="item:DateTimeReceived" />
        </t:FieldOrder>
      </m:SortOrder>
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox" />
      </m:ParentFolderIds>
      <m:QueryString>subject:"project plan"</m:QueryString>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="2f1f3-281">Im folgenden Beispiel wird die Antwort vom Server mit den Suchergebnissen dargestellt.</span><span class="sxs-lookup"><span data-stu-id="2f1f3-281">The following example shows the response from the server with the search results.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="712" MinorBuildNumber="22" Version="V2_3" 
        xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="1" TotalItemsInView="1" IncludesLastItemInRange="true">
            <t:Items>
              <t:Message>
                <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                <t:Subject>project plan</t:Subject>
                <t:DateTimeReceived>2013-12-11T15:42:02Z</t:DateTimeReceived>
                <t:Size>7406</t:Size>
                <t:Importance>Normal</t:Importance>
                <t:IsRead>false</t:IsRead>
              </t:Message>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="2f1f3-282">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2f1f3-282">See also</span></span>

- [<span data-ttu-id="2f1f3-283">Suche und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="2f1f3-283">Search and EWS in Exchange</span></span>](search-and-ews-in-exchange.md)    
- [<span data-ttu-id="2f1f3-284">Verwenden von Suchfiltern mit EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="2f1f3-284">Use search filters with EWS in Exchange</span></span>](how-to-use-search-filters-with-ews-in-exchange.md)    
- [<span data-ttu-id="2f1f3-285">ExchangeService.FindItems</span><span class="sxs-lookup"><span data-stu-id="2f1f3-285">ExchangeService.FindItems</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)    
- [<span data-ttu-id="2f1f3-286">FindItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="2f1f3-286">FindItem operation</span></span>](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    

