---
title: Führen Sie eine AQS-Suche mithilfe der EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: c136901a-313e-4adf-a223-1d090d16917a
description: Erfahren Sie, wie Sie mit Abfragezeichenfolgen und AQS in die EWS Managed API oder EWS-Anwendung zu suchen.
ms.openlocfilehash: dc859e24fa80cd5627477182979c9cc9527818d6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756997"
---
# <a name="perform-an-aqs-search-by-using-ews-in-exchange"></a><span data-ttu-id="c85cc-103">Führen Sie eine AQS-Suche mithilfe der EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="c85cc-103">Perform an AQS search by using EWS in Exchange</span></span>

<span data-ttu-id="c85cc-104">Erfahren Sie, wie Sie mit Abfragezeichenfolgen und AQS in die EWS Managed API oder EWS-Anwendung zu suchen.</span><span class="sxs-lookup"><span data-stu-id="c85cc-104">Find out how to search with query strings and AQS in your EWS Managed API or EWS application.</span></span>
  
<span data-ttu-id="c85cc-105">Abfragezeichenfolgen bieten eine Alternative zur [Suchfilter](how-to-use-search-filters-with-ews-in-exchange.md) Suchkriterien ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="c85cc-105">Query strings provide an alternative to [search filters](how-to-use-search-filters-with-ews-in-exchange.md) for expressing search criteria.</span></span> <span data-ttu-id="c85cc-106">Der größte Vorteil von Abfragezeichenfolgen ist, dass Sie nicht erforderlich sind, um eine einzelne Eigenschaft zum Suchen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="c85cc-106">The biggest advantage to using query strings is that you are not required to specify a single property to search.</span></span> <span data-ttu-id="c85cc-107">Sie können nur einen Wert angeben, und die Suche gilt für alle häufig verwendeten Felder auf die Elemente.</span><span class="sxs-lookup"><span data-stu-id="c85cc-107">You can just provide a value, and the search will apply to all commonly used fields on the items.</span></span> <span data-ttu-id="c85cc-108">Sie können auch die Suche mithilfe von (Erweiterte Query Syntax, AQS) anstelle eines einfachen Werts verfeinern.</span><span class="sxs-lookup"><span data-stu-id="c85cc-108">You can also refine your search by using Advanced Query Syntax (AQS) instead of a simple value.</span></span> <span data-ttu-id="c85cc-109">Abfragezeichenfolgen haben jedoch die folgenden Nachteile, denen Ihnen bekannt sein sollten, bevor Sie die Toolbox hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="c85cc-109">However, query strings have the following limitations that you should be aware of before you add them to your toolbox:</span></span> 
  
- <span data-ttu-id="c85cc-110">**Möglichkeit zur Suche nach bestimmten Eigenschaften.**</span><span class="sxs-lookup"><span data-stu-id="c85cc-110">**Limited ability to search specific properties.**</span></span> <span data-ttu-id="c85cc-111">Wenn Sie mit einem einfachen Wert in einer Abfragezeichenfolge suchen, wird die Suche für alle indizierten Eigenschaften ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c85cc-111">When you search with a simple value in a query string, the search is performed against all indexed properties.</span></span> <span data-ttu-id="c85cc-112">Sie können die Suche auf bestimmte Eigenschaften verfeinern, aber die Eigenschaften für die Verwendung in einer Zeichenfolge AQS verfügbar sind beschränkt.</span><span class="sxs-lookup"><span data-stu-id="c85cc-112">You can refine your search to specific properties, but the properties available to use in an AQS string are limited.</span></span> <span data-ttu-id="c85cc-113">Wenn die Eigenschaft, die Sie suchen möchten eine der Eigenschaften nicht zur Verfügung, die für AQS verfügbar sind, sollten Sie einen Suchfilter.</span><span class="sxs-lookup"><span data-stu-id="c85cc-113">If the property you want to search isn't one of the properties that are available for AQS, consider using a search filter.</span></span> 
    
- <span data-ttu-id="c85cc-114">**Benutzerdefinierte Eigenschaften werden nicht durchsucht.**</span><span class="sxs-lookup"><span data-stu-id="c85cc-114">**Custom properties aren't searched.**</span></span> <span data-ttu-id="c85cc-115">Zeichenfolgensuchen Abfrage für einen Index ausgeführt werden, und benutzerdefinierte Eigenschaften sind nicht in der betreffenden Index enthalten.</span><span class="sxs-lookup"><span data-stu-id="c85cc-115">Query string searches are performed against an index, and custom properties are not included in that index.</span></span> <span data-ttu-id="c85cc-116">Wenn Sie die Suche nach benutzerdefinierten Eigenschaften müssen, verwenden Sie stattdessen einen Suchfilter.</span><span class="sxs-lookup"><span data-stu-id="c85cc-116">If you need to search custom properties, use a search filter instead.</span></span> 
    
- <span data-ttu-id="c85cc-117">**Eingeschränkte Steuerung für Zeichenfolge durchsucht.**</span><span class="sxs-lookup"><span data-stu-id="c85cc-117">**Limited control for string searches.**</span></span> <span data-ttu-id="c85cc-118">Abfrage Zeichenfolgensuchen immer groß-und Kleinschreibung ignorieren, und sind immer Suchvorgänge nach Teilzeichenfolgen dar.</span><span class="sxs-lookup"><span data-stu-id="c85cc-118">Query string searches always ignore case, and are always substring searches.</span></span> <span data-ttu-id="c85cc-119">Wenn Sie möchten Groß-/Kleinschreibung beachtet, Präfix oder genauen Übereinstimmung gesucht, verwenden Sie einen Filter für die Suche.</span><span class="sxs-lookup"><span data-stu-id="c85cc-119">If you want to do case-sensitive, prefix, or exact match searches, use a search filter.</span></span> 
    
- <span data-ttu-id="c85cc-120">**Nicht verfügbar für Ordner oder Suchordner.**</span><span class="sxs-lookup"><span data-stu-id="c85cc-120">**Not available for folders or search folders.**</span></span> <span data-ttu-id="c85cc-121">Der EWS-Vorgänge für die Suche nach Ordner unterstützen nicht mit einer Abfragezeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="c85cc-121">The EWS operations for searching for folders don't support using a query string.</span></span> <span data-ttu-id="c85cc-122">Darüber hinaus unterstützen keine Suchordner Abfragezeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="c85cc-122">Additionally, search folders don't support query strings.</span></span> <span data-ttu-id="c85cc-123">In beiden Fällen ist ein Suchfilter nur die Option.</span><span class="sxs-lookup"><span data-stu-id="c85cc-123">In both cases, a search filter is your only option.</span></span> 
    
## <a name="creating-a-query-string"></a><span data-ttu-id="c85cc-124">Erstellen einer Abfragezeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c85cc-124">Creating a query string</span></span>
<span data-ttu-id="c85cc-125"><a name="bk_CreateQueryString"> </a></span><span class="sxs-lookup"><span data-stu-id="c85cc-125"></span></span>

<span data-ttu-id="c85cc-126">Abfragezeichenfolgen in die EWS Managed API und EWS werden als eine Teilmenge der Syntax AQS interpretiert.</span><span class="sxs-lookup"><span data-stu-id="c85cc-126">Query strings in the EWS Managed API and EWS are interpreted as a subset of AQS syntax.</span></span> <span data-ttu-id="c85cc-127">AQS Zeichenfolgen bestehen aus Werten oder Schlüsselwort/Wert-Paaren, getrennt durch einen Doppelpunkt (:)).</span><span class="sxs-lookup"><span data-stu-id="c85cc-127">AQS strings are composed of either values or keyword/value pairs, separated by a colon (:).</span></span>
  
`keyword:value`

<span data-ttu-id="c85cc-128">Wenn Sie ein Wert ohne ein Schlüsselwort angegeben wird, werden alle indizierte Eigenschaften für den Wert durchsucht.</span><span class="sxs-lookup"><span data-stu-id="c85cc-128">When a value is specified without a keyword, all indexed properties are searched for the value.</span></span> <span data-ttu-id="c85cc-129">Wenn ein Schlüsselwort mit einem Wert kombiniert ist, gibt das Schlüsselwort Suche nach den entsprechenden Wert einer Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="c85cc-129">If a keyword is paired with a value, the keyword specifies a property to search for the corresponding value.</span></span>
  
<span data-ttu-id="c85cc-130">**In Tabelle 1. Unterstützte AQS Schlüsselwörter**</span><span class="sxs-lookup"><span data-stu-id="c85cc-130">**Table 1. Supported AQS keywords**</span></span>

|<span data-ttu-id="c85cc-131">**Schlüsselwort**</span><span class="sxs-lookup"><span data-stu-id="c85cc-131">**Keyword**</span></span>|<span data-ttu-id="c85cc-132">**Werttyp**</span><span class="sxs-lookup"><span data-stu-id="c85cc-132">**Value type**</span></span>|<span data-ttu-id="c85cc-133">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="c85cc-133">**Example**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c85cc-134">subject</span><span class="sxs-lookup"><span data-stu-id="c85cc-134">subject</span></span>  <br/> |<span data-ttu-id="c85cc-135">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c85cc-135">String</span></span>  <br/> |<span data-ttu-id="c85cc-136">Betreff: Projekt</span><span class="sxs-lookup"><span data-stu-id="c85cc-136">subject:project</span></span>  <br/> |
|<span data-ttu-id="c85cc-137">body</span><span class="sxs-lookup"><span data-stu-id="c85cc-137">body</span></span>  <br/> |<span data-ttu-id="c85cc-138">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c85cc-138">String</span></span>  <br/> |<span data-ttu-id="c85cc-139">Body: Verkaufszahlen</span><span class="sxs-lookup"><span data-stu-id="c85cc-139">body:sales figures</span></span>  <br/> |
|<span data-ttu-id="c85cc-140">Anlage</span><span class="sxs-lookup"><span data-stu-id="c85cc-140">attachment</span></span>  <br/> |<span data-ttu-id="c85cc-141">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c85cc-141">String</span></span>  <br/> |<span data-ttu-id="c85cc-142">Anhang: Bericht</span><span class="sxs-lookup"><span data-stu-id="c85cc-142">attachment:report</span></span>  <br/> |
|<span data-ttu-id="c85cc-143">in</span><span class="sxs-lookup"><span data-stu-id="c85cc-143">to</span></span>  <br/> |<span data-ttu-id="c85cc-144">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c85cc-144">String</span></span>  <br/> |<span data-ttu-id="c85cc-145">an: "Sadie Daniels"</span><span class="sxs-lookup"><span data-stu-id="c85cc-145">to:"Sadie Daniels"</span></span>  <br/> |
|<span data-ttu-id="c85cc-146">Von</span><span class="sxs-lookup"><span data-stu-id="c85cc-146">from</span></span>  <br/> |<span data-ttu-id="c85cc-147">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c85cc-147">String</span></span>  <br/> |<span data-ttu-id="c85cc-148">von: hoffe</span><span class="sxs-lookup"><span data-stu-id="c85cc-148">from:hope</span></span>  <br/> |
|<span data-ttu-id="c85cc-149">cc</span><span class="sxs-lookup"><span data-stu-id="c85cc-149">cc</span></span>  <br/> |<span data-ttu-id="c85cc-150">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c85cc-150">String</span></span>  <br/> |<span data-ttu-id="c85cc-151">cc: "Ronnie Sturgis"</span><span class="sxs-lookup"><span data-stu-id="c85cc-151">cc:"Ronnie Sturgis"</span></span>  <br/> |
|<span data-ttu-id="c85cc-152">bcc</span><span class="sxs-lookup"><span data-stu-id="c85cc-152">bcc</span></span>  <br/> |<span data-ttu-id="c85cc-153">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c85cc-153">String</span></span>  <br/> |<span data-ttu-id="c85cc-154">Bcc:mack</span><span class="sxs-lookup"><span data-stu-id="c85cc-154">bcc:mack</span></span>  <br/> |
|<span data-ttu-id="c85cc-155">participants</span><span class="sxs-lookup"><span data-stu-id="c85cc-155">participants</span></span>  <br/> |<span data-ttu-id="c85cc-156">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c85cc-156">String</span></span>  <br/> |<span data-ttu-id="c85cc-157">Teilnehmer: sadie</span><span class="sxs-lookup"><span data-stu-id="c85cc-157">participants:sadie</span></span>  <br/> |
|<span data-ttu-id="c85cc-158">category</span><span class="sxs-lookup"><span data-stu-id="c85cc-158">category</span></span>  <br/> |<span data-ttu-id="c85cc-159">String</span><span class="sxs-lookup"><span data-stu-id="c85cc-159">String</span></span>  <br/> |<span data-ttu-id="c85cc-160">Kategorie: Projekt</span><span class="sxs-lookup"><span data-stu-id="c85cc-160">category:project</span></span>  <br/> |
|<span data-ttu-id="c85cc-161">Wichtigkeit</span><span class="sxs-lookup"><span data-stu-id="c85cc-161">importance</span></span>  <br/> |<span data-ttu-id="c85cc-162">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c85cc-162">String</span></span>  <br/> |<span data-ttu-id="c85cc-163">Wichtigkeit: hoch</span><span class="sxs-lookup"><span data-stu-id="c85cc-163">importance:high</span></span>  <br/> |
|<span data-ttu-id="c85cc-164">Art</span><span class="sxs-lookup"><span data-stu-id="c85cc-164">kind</span></span>  <br/> |<span data-ttu-id="c85cc-165">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="c85cc-165">Item type</span></span>  <br/> |<span data-ttu-id="c85cc-166">Art-Besprechungen:</span><span class="sxs-lookup"><span data-stu-id="c85cc-166">kind:meetings</span></span>  <br/> |
|<span data-ttu-id="c85cc-167">gesendet</span><span class="sxs-lookup"><span data-stu-id="c85cc-167">sent</span></span>  <br/> |<span data-ttu-id="c85cc-168">Date</span><span class="sxs-lookup"><span data-stu-id="c85cc-168">Date</span></span>  <br/> |<span data-ttu-id="c85cc-169">gesendet: 12/10/2013</span><span class="sxs-lookup"><span data-stu-id="c85cc-169">sent:12/10/2013</span></span>  <br/> |
|<span data-ttu-id="c85cc-170">empfangen</span><span class="sxs-lookup"><span data-stu-id="c85cc-170">received</span></span>  <br/> |<span data-ttu-id="c85cc-171">Date</span><span class="sxs-lookup"><span data-stu-id="c85cc-171">Date</span></span>  <br/> |<span data-ttu-id="c85cc-172">empfangen: gestern</span><span class="sxs-lookup"><span data-stu-id="c85cc-172">received:yesterday</span></span>  <br/> |
|<span data-ttu-id="c85cc-173">HasAttachment</span><span class="sxs-lookup"><span data-stu-id="c85cc-173">hasattachment</span></span>  <br/> |<span data-ttu-id="c85cc-174">Boolean</span><span class="sxs-lookup"><span data-stu-id="c85cc-174">Boolean</span></span>  <br/> |<span data-ttu-id="c85cc-175">Hat Anlage: true</span><span class="sxs-lookup"><span data-stu-id="c85cc-175">Has attachment:true</span></span>  <br/> |
|<span data-ttu-id="c85cc-176">isflagged</span><span class="sxs-lookup"><span data-stu-id="c85cc-176">isflagged</span></span>  <br/> |<span data-ttu-id="c85cc-177">Boolean</span><span class="sxs-lookup"><span data-stu-id="c85cc-177">Boolean</span></span>  <br/> |<span data-ttu-id="c85cc-178">isflagged:true</span><span class="sxs-lookup"><span data-stu-id="c85cc-178">isflagged:true</span></span>  <br/> |
|<span data-ttu-id="c85cc-179">isread</span><span class="sxs-lookup"><span data-stu-id="c85cc-179">isread</span></span>  <br/> |<span data-ttu-id="c85cc-180">Boolean</span><span class="sxs-lookup"><span data-stu-id="c85cc-180">Boolean</span></span>  <br/> |<span data-ttu-id="c85cc-181">isread:false</span><span class="sxs-lookup"><span data-stu-id="c85cc-181">isread:false</span></span>  <br/> |
|<span data-ttu-id="c85cc-182">size</span><span class="sxs-lookup"><span data-stu-id="c85cc-182">size</span></span>  <br/> |<span data-ttu-id="c85cc-183">Zahl</span><span class="sxs-lookup"><span data-stu-id="c85cc-183">Number</span></span>  <br/> |<span data-ttu-id="c85cc-184">Größe:\>5000</span><span class="sxs-lookup"><span data-stu-id="c85cc-184">size:\>5000</span></span>  <br/> |
   
<span data-ttu-id="c85cc-185">Sehen wir uns an, wie die verschiedenen Werttypen funktionieren.</span><span class="sxs-lookup"><span data-stu-id="c85cc-185">Let's take a look at how the different value types work.</span></span>
  
### <a name="using-a-string-value-type"></a><span data-ttu-id="c85cc-186">Verwenden einen String-Wert-Typ</span><span class="sxs-lookup"><span data-stu-id="c85cc-186">Using a string value type</span></span>

<span data-ttu-id="c85cc-187">Zeichenfolge Werttypen sind standardmäßig als Präfix Suchmethode, die Groß-/ nicht Kleinschreibung durchsucht.</span><span class="sxs-lookup"><span data-stu-id="c85cc-187">String value types are by default searched as prefix substring searches that are not case-sensitive.</span></span> <span data-ttu-id="c85cc-188">Dies bedeutet, dass die Suche nach Betreff: Project eine der folgenden Betreffzeilen würde sich eine Übereinstimmung:</span><span class="sxs-lookup"><span data-stu-id="c85cc-188">That means that searching for subject:project would match any of the following subjects:</span></span> 
  
- <span data-ttu-id="c85cc-189">Projekt Besprechungsnotizen</span><span class="sxs-lookup"><span data-stu-id="c85cc-189">Project meeting notes</span></span>
    
- <span data-ttu-id="c85cc-190">Haben Sie die Projektpläne?</span><span class="sxs-lookup"><span data-stu-id="c85cc-190">Do you have the project plans?</span></span>
    
- <span data-ttu-id="c85cc-191">Den Umsatzprognosen Dezember</span><span class="sxs-lookup"><span data-stu-id="c85cc-191">December sales projections</span></span>
    
<span data-ttu-id="c85cc-192">Sie können die ganzes Wort anstelle von übereinstimmenden Präfixe erforderlich, durch die Zeichenfolge in Anführungszeichen einschließen, um die Suche ändern.</span><span class="sxs-lookup"><span data-stu-id="c85cc-192">You can change the search to require the whole word rather than matching prefixes by enclosing the string in quotation marks.</span></span> <span data-ttu-id="c85cc-193">Suchen nach Betreff: würde ein "Projekt" den Wert "Dezember den Umsatzprognosen" aus der Liste der Übereinstimmungen.</span><span class="sxs-lookup"><span data-stu-id="c85cc-193">Searching for subject:"project" would eliminate the "December sales projections" value from the list of matches.</span></span> <span data-ttu-id="c85cc-194">Beachten Sie, dass der Wert immer noch nicht Groß-/Kleinschreibung beachtet wird.</span><span class="sxs-lookup"><span data-stu-id="c85cc-194">Note that the value is still not case-sensitive.</span></span> 
  
<span data-ttu-id="c85cc-195">Wenn Sie mehrere Wörter in einer Abfragezeichenfolge verwenden, erfordert eine Übereinstimmung, dass beide Wörter in den durchsuchten Feldern angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="c85cc-195">If you use multiple words in a query string, a match requires that both words appear in the searched fields.</span></span> <span data-ttu-id="c85cc-196">Beispielsweise würde Suchen nach Betreff: Projektplan eine der folgenden Betreffzeilen entsprechen:</span><span class="sxs-lookup"><span data-stu-id="c85cc-196">For example, searching for subject:project plan would match any of the following subjects:</span></span> 
  
- <span data-ttu-id="c85cc-197">Projektplan</span><span class="sxs-lookup"><span data-stu-id="c85cc-197">Project plan</span></span>
    
- <span data-ttu-id="c85cc-198">Haben Sie die Projektpläne?</span><span class="sxs-lookup"><span data-stu-id="c85cc-198">Do you have the project plans?</span></span>
    
- <span data-ttu-id="c85cc-199">Senden Sie mir bitte des Plans für unsere Projekt</span><span class="sxs-lookup"><span data-stu-id="c85cc-199">Please send me the plan for our project</span></span>
    
- <span data-ttu-id="c85cc-200">Planen von Projektmeilensteine</span><span class="sxs-lookup"><span data-stu-id="c85cc-200">Planning project milestones</span></span>
    
<span data-ttu-id="c85cc-201">Wenn Sie mehrere Wörter in Anführungszeichen einschließen, werden sie als eine einzelne Phrase behandelt.</span><span class="sxs-lookup"><span data-stu-id="c85cc-201">If you enclose multiple words in quotation marks, they are treated as a single phrase.</span></span> <span data-ttu-id="c85cc-202">Suchen nach Betreff: "Projektplan" würde nur den Betreff "Projektplan" aus der vorherigen Liste übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="c85cc-202">Searching for subject:"project plan" would only match the "Project plan" subject from the previous list.</span></span> 
  
### <a name="using-an-item-type-value-type"></a><span data-ttu-id="c85cc-203">Verwenden einen Element Typ Werttyp</span><span class="sxs-lookup"><span data-stu-id="c85cc-203">Using an item type value type</span></span>

<span data-ttu-id="c85cc-204">Die folgenden Artikelwerte können mit dem Schlüsselwort **Art** Sie die Suchergebnisse auf nur einen bestimmten Typ des Elements, wie e-Mail oder Besprechungsanfragen einschränken:</span><span class="sxs-lookup"><span data-stu-id="c85cc-204">You can use the following item type values with the **kind** keyword to limit your search results to only a specific type of item, such as email or meeting requests:</span></span> 
  
- <span data-ttu-id="c85cc-205">contacts</span><span class="sxs-lookup"><span data-stu-id="c85cc-205">contacts</span></span>    
- <span data-ttu-id="c85cc-206">Dokumente</span><span class="sxs-lookup"><span data-stu-id="c85cc-206">docs</span></span>    
- <span data-ttu-id="c85cc-207">E-Mail</span><span class="sxs-lookup"><span data-stu-id="c85cc-207">email</span></span>    
- <span data-ttu-id="c85cc-208">Faxnachrichten</span><span class="sxs-lookup"><span data-stu-id="c85cc-208">faxes</span></span>    
- <span data-ttu-id="c85cc-209">Instant Messaging (Sofortnachrichten entspricht)</span><span class="sxs-lookup"><span data-stu-id="c85cc-209">im (corresponds to instant messages)</span></span>    
- <span data-ttu-id="c85cc-210">Journale</span><span class="sxs-lookup"><span data-stu-id="c85cc-210">journals</span></span>    
- <span data-ttu-id="c85cc-211">Besprechungen (entspricht Termine und Besprechungsanfragen)</span><span class="sxs-lookup"><span data-stu-id="c85cc-211">meetings (corresponds to appointments and meeting requests)</span></span>    
- <span data-ttu-id="c85cc-212">notes</span><span class="sxs-lookup"><span data-stu-id="c85cc-212">notes</span></span>    
- <span data-ttu-id="c85cc-213">posts</span><span class="sxs-lookup"><span data-stu-id="c85cc-213">posts</span></span>    
- <span data-ttu-id="c85cc-214">rssfeeds</span><span class="sxs-lookup"><span data-stu-id="c85cc-214">rssfeeds</span></span>    
- <span data-ttu-id="c85cc-215">tasks</span><span class="sxs-lookup"><span data-stu-id="c85cc-215">tasks</span></span>    
- <span data-ttu-id="c85cc-216">Voicemail</span><span class="sxs-lookup"><span data-stu-id="c85cc-216">voicemail</span></span>
    
### <a name="using-a-date-value-type"></a><span data-ttu-id="c85cc-217">Verwenden einen Datum Werttyp</span><span class="sxs-lookup"><span data-stu-id="c85cc-217">Using a date value type</span></span>

<span data-ttu-id="c85cc-218">Sie können auf unterschiedliche Arten Datumstypen Wert suchen.</span><span class="sxs-lookup"><span data-stu-id="c85cc-218">You can search date value types in a number of different ways.</span></span> <span data-ttu-id="c85cc-219">Am einfachsten ist, um nach einem bestimmten Datum zu suchen.</span><span class="sxs-lookup"><span data-stu-id="c85cc-219">The simplest is to search for a specific date.</span></span> <span data-ttu-id="c85cc-220">Suchen mit empfangen: 12/11/2013 werden alle 11 Dezember 2013 empfangenen Elemente zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c85cc-220">Searching with received:12/11/2013 will return all items received on December 11, 2013.</span></span> <span data-ttu-id="c85cc-221">Jedoch können Sie auch weniger spezifischen sein.</span><span class="sxs-lookup"><span data-stu-id="c85cc-221">However, you can also be less specific.</span></span> <span data-ttu-id="c85cc-222">Suchen mit empfangen: 12/11 werden alle am 11. Dezember des aktuellen Jahres empfangenen Elemente zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c85cc-222">Searching with received:12/11 will return all items received on December 11 of the current year.</span></span> 
  
<span data-ttu-id="c85cc-223">Eine weitere Option ist die Verwendung die Monatsnamen an.</span><span class="sxs-lookup"><span data-stu-id="c85cc-223">Another option is to use the month names.</span></span> <span data-ttu-id="c85cc-224">Für die Suche können mit empfangen: 11 Dezember 2013 oder Dezember 11 die gleichen Ergebnisse zu erhalten, empfangen: 12/11/2013 und empfangene: 12/11, jeweils.</span><span class="sxs-lookup"><span data-stu-id="c85cc-224">You can search with received:December 11, 2013 or December 11 to get the same results as received:12/11/2013 and received:12/11, respectively.</span></span> <span data-ttu-id="c85cc-225">Sie können auch mit suchen empfangen: Dezember zum Abrufen aller Elemente im Dezember, im aktuellen Jahr eingegangen.</span><span class="sxs-lookup"><span data-stu-id="c85cc-225">You can also search with received:December to get all items received in the month of December, in the current year.</span></span> 
  
<span data-ttu-id="c85cc-226">Verwenden die Namen der Wochentage ist auch eine Option aus.</span><span class="sxs-lookup"><span data-stu-id="c85cc-226">Using the names of the days of the week is also an option.</span></span> <span data-ttu-id="c85cc-227">Suchen mit empfangen: Dienstag wird Dienstag der aktuellen Woche empfangene alle Elemente zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c85cc-227">Searching with received:Tuesday will return all items received on Tuesday of the current week.</span></span> 
  
<span data-ttu-id="c85cc-228">Datum Werttypen unterstützen auch einen Satz von Schlüsselwörtern für Suchvorgänge relativ zu der aktuellen Zeit.</span><span class="sxs-lookup"><span data-stu-id="c85cc-228">Date value types also support a set of keywords for searches relative to the current time.</span></span> <span data-ttu-id="c85cc-229">Die folgenden Schlüsselwörter werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="c85cc-229">The following keywords are supported:</span></span>
  
- <span data-ttu-id="c85cc-230">heute</span><span class="sxs-lookup"><span data-stu-id="c85cc-230">today</span></span>  
- <span data-ttu-id="c85cc-231">tomorrow</span><span class="sxs-lookup"><span data-stu-id="c85cc-231">tomorrow</span></span>
- <span data-ttu-id="c85cc-232">yesterday</span><span class="sxs-lookup"><span data-stu-id="c85cc-232">yesterday</span></span>
- <span data-ttu-id="c85cc-233">this week</span><span class="sxs-lookup"><span data-stu-id="c85cc-233">this week</span></span>    
- <span data-ttu-id="c85cc-234">Letzte Woche</span><span class="sxs-lookup"><span data-stu-id="c85cc-234">last week</span></span>    
- <span data-ttu-id="c85cc-235">nächsten Monat</span><span class="sxs-lookup"><span data-stu-id="c85cc-235">next month</span></span>    
- <span data-ttu-id="c85cc-236">letzten Monat</span><span class="sxs-lookup"><span data-stu-id="c85cc-236">past month</span></span>    
- <span data-ttu-id="c85cc-237">Jahr</span><span class="sxs-lookup"><span data-stu-id="c85cc-237">coming year</span></span>
    
<span data-ttu-id="c85cc-238">Datumstypen Wert können auch mit relationalen Operatoren wie größer oder kleiner verglichen werden als, oder als Bereich Bereich Operator **.** angegeben. Beispielsweise erhalten:\>11/30/2013 gesendet:\>= gestern und received:12/1/2013..today sind alle gültigen Abfragezeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="c85cc-238">Date value types can also be compared with relational operators like greater than or less than, or specified as a range with the range operator **..**. For example, received:\>11/30/2013, sent:\>=yesterday, and received:12/1/2013..today are all valid query strings.</span></span> 
  
### <a name="using-a-boolean-value-type"></a><span data-ttu-id="c85cc-239">Verwenden einen Wert vom Typ Boolean-Typ</span><span class="sxs-lookup"><span data-stu-id="c85cc-239">Using a Boolean value type</span></span>

<span data-ttu-id="c85cc-240">Boolescher Werttypen können "true" oder "false" sein.</span><span class="sxs-lookup"><span data-stu-id="c85cc-240">Boolean value types can be "true" or "false".</span></span> <span data-ttu-id="c85cc-241">Die Werte sind nicht Groß-/Kleinschreibung beachtet, damit Isread:false die gleichen Ergebnisse wie Isread:FALSE erzielt wird.</span><span class="sxs-lookup"><span data-stu-id="c85cc-241">The values are not case-sensitive, so isread:false will produce the same results as isread:FALSE.</span></span>
  
### <a name="using-a-number-value-type"></a><span data-ttu-id="c85cc-242">Verwenden einen Nummer Werttyp</span><span class="sxs-lookup"><span data-stu-id="c85cc-242">Using a number value type</span></span>

<span data-ttu-id="c85cc-243">Zahl Werttypen als nach genauen Übereinstimmungen durchsucht werden können, aber sie können auch durchsucht werden mit relationalen Operatoren wie größer oder kleiner als.</span><span class="sxs-lookup"><span data-stu-id="c85cc-243">Number value types can be searched as exact matches, but they can also be searched using relational operators like greater than or less than.</span></span> <span data-ttu-id="c85cc-244">Größe: 10000 werden beispielsweise nur auf Elemente mit einer Größe von genau 10000 Byte, aber Größe zurückgegeben:\>= 10000 werden Elemente mit einer Größe größer als oder gleich 10000 Byte zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c85cc-244">For example, size:10000 will return only items that have a size of exactly 10000 bytes, but size:\>=10000 will return items that have a size greater than or equal to 10000 bytes.</span></span> <span data-ttu-id="c85cc-245">Sie können auch einen Bereich mithilfe des Range-Operators ( **.**) angeben.</span><span class="sxs-lookup"><span data-stu-id="c85cc-245">You can also specify a range by using the range operator ( **..**).</span></span> <span data-ttu-id="c85cc-246">Größe: 7000..8000 gibt beispielsweise Elemente zurück, die eine Größe zwischen 7000 und 8000 aufweisen.</span><span class="sxs-lookup"><span data-stu-id="c85cc-246">For example, size:7000..8000 will return items that have a size between 7000 and 8000.</span></span> 
  
### <a name="using-logical-operators"></a><span data-ttu-id="c85cc-247">Verwenden von logischen Operatoren</span><span class="sxs-lookup"><span data-stu-id="c85cc-247">Using logical operators</span></span>

<span data-ttu-id="c85cc-248">Abfragezeichenfolgen unterstützt die folgenden logischen Operatoren.</span><span class="sxs-lookup"><span data-stu-id="c85cc-248">Query strings support the following logical operators.</span></span>
  
<span data-ttu-id="c85cc-249">**In Tabelle 2. Unterstützte logische Operatoren**</span><span class="sxs-lookup"><span data-stu-id="c85cc-249">**Table 2. Supported logical operators**</span></span>

|<span data-ttu-id="c85cc-250">**Operator**</span><span class="sxs-lookup"><span data-stu-id="c85cc-250">**Operator**</span></span>|<span data-ttu-id="c85cc-251">**Beispiele**</span><span class="sxs-lookup"><span data-stu-id="c85cc-251">**Examples**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c85cc-252">AND</span><span class="sxs-lookup"><span data-stu-id="c85cc-252">AND</span></span>  <br/> |<span data-ttu-id="c85cc-253">Project und aus: "Sadie Daniels"</span><span class="sxs-lookup"><span data-stu-id="c85cc-253">project AND from:"Sadie Daniels"</span></span>  <br/> <span data-ttu-id="c85cc-254">Betreff:(project AND plan)</span><span class="sxs-lookup"><span data-stu-id="c85cc-254">subject:(project AND plan)</span></span>  <br/> |
|<span data-ttu-id="c85cc-255">ODER</span><span class="sxs-lookup"><span data-stu-id="c85cc-255">OR</span></span>  <br/> |<span data-ttu-id="c85cc-256">Betreff: Besprechung oder aus: "Hoffe Brutto"</span><span class="sxs-lookup"><span data-stu-id="c85cc-256">subject:meeting OR from:"Hope Gross"</span></span>  <br/> <span data-ttu-id="c85cc-257">von: ("Sadie Daniels" oder "Hoffe Brutto")</span><span class="sxs-lookup"><span data-stu-id="c85cc-257">from:("Sadie Daniels" OR "Hope Gross")</span></span>  <br/> |
|<span data-ttu-id="c85cc-258">NOT</span><span class="sxs-lookup"><span data-stu-id="c85cc-258">NOT</span></span>  <br/> |<span data-ttu-id="c85cc-259">NICHT aus: "Ronnie Sturgis"</span><span class="sxs-lookup"><span data-stu-id="c85cc-259">NOT from:"Ronnie Sturgis"</span></span>  <br/> <span data-ttu-id="c85cc-260">empfangen: heute nicht mehr</span><span class="sxs-lookup"><span data-stu-id="c85cc-260">received:NOT today</span></span>  <br/> |
   
<span data-ttu-id="c85cc-261">Beachten Sie, dass Sie diese Operatoren zusammengefügt mehrerer Kriterien oder mehrere Werte in einem einzelnen Wert-Paar zusammengefügt verwenden können.</span><span class="sxs-lookup"><span data-stu-id="c85cc-261">Notice that you can use these operators to join multiple criteria together or to join multiple values within a single keyword/value pair together.</span></span> <span data-ttu-id="c85cc-262">Allerdings sollten bei der Teilnahme an mehrere Werte in einem einzelnen Schlüsselwort/Wert-Paar Sie Klammern verwenden mehrere Werte eingeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="c85cc-262">However, when joining multiple values in a single keyword/value pair, you should use parentheses to enclose the multiple values.</span></span> <span data-ttu-id="c85cc-263">Um dies zu verstehen, sollten Sie mit Suche: "Sadie Daniels" oder "Hoffe Bruttogewicht".</span><span class="sxs-lookup"><span data-stu-id="c85cc-263">To understand why, consider searching with from:"Sadie Daniels" OR "Hope Gross".</span></span> <span data-ttu-id="c85cc-264">Diese Suche ist als die folgenden Kriterien tatsächlich interpretiert werden:</span><span class="sxs-lookup"><span data-stu-id="c85cc-264">This search actually is interpreted as the following criteria:</span></span>
  
- <span data-ttu-id="c85cc-265">Das Element hat ihren Ursprung Sadie Daniels, OR</span><span class="sxs-lookup"><span data-stu-id="c85cc-265">The item is from Sadie Daniels, OR</span></span>
    
- <span data-ttu-id="c85cc-266">Das Element wurde dem Begriff "Hoffe Brutto" in seine indizierten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c85cc-266">The item has the phrase "Hope Gross" in any of its indexed properties.</span></span>
    
<span data-ttu-id="c85cc-267">Im Gegensatz dazu aus: ("Sadie Daniels" oder "Hoffe Brutto") als interpretiert wird:</span><span class="sxs-lookup"><span data-stu-id="c85cc-267">In contrast, from:("Sadie Daniels" OR "Hope Gross") is interpreted as:</span></span> 
  
- <span data-ttu-id="c85cc-268">Das Element hat ihren Ursprung Sadie Daniels, OR</span><span class="sxs-lookup"><span data-stu-id="c85cc-268">The item is from Sadie Daniels, OR</span></span>
    
- <span data-ttu-id="c85cc-269">Das Element hat ihren Ursprung hoffe Brutto</span><span class="sxs-lookup"><span data-stu-id="c85cc-269">The item is from Hope Gross</span></span>
    
<span data-ttu-id="c85cc-270">Ist der Standardoperator, wenn mehrere Kriterien angegeben werden, jedoch kein logischer Operator enthalten ist und.</span><span class="sxs-lookup"><span data-stu-id="c85cc-270">The default operator when multiple criteria are specified but no logical operator is included is AND.</span></span> <span data-ttu-id="c85cc-271">Beispielsweise hat Anlage: True Betreff: Projekt entspricht hat: Anlage: True und Betreff: Projekt.</span><span class="sxs-lookup"><span data-stu-id="c85cc-271">For example, has attachment:true subject:project is equivalent to has:attachment:true AND subject:project.</span></span>
  
## <a name="example-find-items-by-using-a-query-string-and-the-ews-managed-api"></a><span data-ttu-id="c85cc-272">Beispiel: Suchen von Elementen mithilfe von einer Abfragezeichenfolge und die EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="c85cc-272">Example: Find items by using a query string and the EWS Managed API</span></span>
<span data-ttu-id="c85cc-273"><a name="bk_ExampleEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="c85cc-273"></span></span>

<span data-ttu-id="c85cc-274">In diesem Beispiel wird eine Methode namens **SearchWithQueryString** definiert.</span><span class="sxs-lookup"><span data-stu-id="c85cc-274">In this example, a method called **SearchWithQueryString** is defined.</span></span> <span data-ttu-id="c85cc-275">Es wird ein [ExchangeService](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objekt, ein [WellKnownFolderName](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) -Objekt und ein **String** -Objekt, das als Parameter die Abfragezeichenfolge darstellt.</span><span class="sxs-lookup"><span data-stu-id="c85cc-275">It takes an [ExchangeService](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object, a [WellKnownFolderName](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) object, and a **string** object that represents the query string as parameters.</span></span> <span data-ttu-id="c85cc-276">In diesem Beispiel wird davon ausgegangen, dass das **ExchangeService**-Objekt mit gültigen Werten in den [Credentials](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx)- und [Url](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx)-Eigenschaften initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="c85cc-276">This example assumes that the **ExchangeService** object has been initialized with valid values in the [Credentials](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) and [Url](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) properties.</span></span> 
  
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

<span data-ttu-id="c85cc-277">Mit dieser Methode können Sie für alle Elemente mit dem Ausdruck "Projektplan" in der Betreffzeile suchen, wie im folgenden Beispiel dargestellt.</span><span class="sxs-lookup"><span data-stu-id="c85cc-277">You can use this method to search for all items with the phrase "project plan" in the subject, as shown in this example.</span></span>
  
```cs
string queryString = "subject:\"project plan\"";
SearchWithQueryString(service, WellKnownFolderName.Inbox, queryString);
```

## <a name="example-find-items-by-using-a-query-string-and-ews"></a><span data-ttu-id="c85cc-278">Beispiel: Suchen von Elementen mithilfe eines Abfragezeichenfolge und Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="c85cc-278">Example: Find items by using a query string and EWS</span></span>
<span data-ttu-id="c85cc-279"><a name="bk_ExampleEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="c85cc-279"></span></span>

<span data-ttu-id="c85cc-280">In diesem Beispiel sucht eine Anforderung SOAP- [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) alle Elemente im Posteingang mit dem Begriff "Projektplan" im Betreff.</span><span class="sxs-lookup"><span data-stu-id="c85cc-280">In this example, a SOAP [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) request finds all items in the Inbox with the phrase "project plan" in the subject.</span></span> 
  
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

<span data-ttu-id="c85cc-281">Das folgende Beispiel zeigt die Antwort vom Server mit den Suchergebnissen.</span><span class="sxs-lookup"><span data-stu-id="c85cc-281">The following example shows the response from the server with the search results.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="712" MinorBuildNumber="22" Version="V2_3" 
        xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="see-also"></a><span data-ttu-id="c85cc-282">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c85cc-282">See also</span></span>

- [<span data-ttu-id="c85cc-283">Suche und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="c85cc-283">Search and EWS in Exchange</span></span>](search-and-ews-in-exchange.md)    
- [<span data-ttu-id="c85cc-284">Verwenden Sie Suchfilter mit EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="c85cc-284">Use search filters with EWS in Exchange</span></span>](how-to-use-search-filters-with-ews-in-exchange.md)    
- [<span data-ttu-id="c85cc-285">ExchangeService.FindItems</span><span class="sxs-lookup"><span data-stu-id="c85cc-285">ExchangeService.FindItems</span></span>](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)    
- [<span data-ttu-id="c85cc-286">FindItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="c85cc-286">FindItem operation</span></span>](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    

