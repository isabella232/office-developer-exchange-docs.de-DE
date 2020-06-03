---
title: QueryString (querystringtype)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
api_name:
- QueryString
api_type:
- schema
ms.assetid: cadbf9a5-b87e-4d7f-b488-b76fb0ee7150
description: Das QueryString-Element enthält eine Post Fach Abfragezeichenfolge basierend auf der erweiterten Abfrage Syntax (AQS).
localization_priority: Priority
ms.openlocfilehash: eafbbab6de8d191197fb4b80e2b8e3cea80ab800
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459188"
---
# <a name="querystring-querystringtype"></a><span data-ttu-id="f7a28-103">QueryString (querystringtype)</span><span class="sxs-lookup"><span data-stu-id="f7a28-103">QueryString (QueryStringType)</span></span>

<span data-ttu-id="f7a28-104">Das **QueryString** -Element enthält eine Post Fach Abfragezeichenfolge basierend auf der erweiterten Abfrage Syntax (AQS).</span><span class="sxs-lookup"><span data-stu-id="f7a28-104">The **QueryString** element contains a mailbox query string based on Advanced Query Syntax (AQS).</span></span> 
  
```XML
<QueryString/>
```

 <span data-ttu-id="f7a28-105">**Querystringtype**</span><span class="sxs-lookup"><span data-stu-id="f7a28-105">**QueryStringType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f7a28-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f7a28-106">Attributes and elements</span></span>

<span data-ttu-id="f7a28-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f7a28-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f7a28-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="f7a28-108">Attributes</span></span>

|<span data-ttu-id="f7a28-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="f7a28-109">**Attribute**</span></span>|<span data-ttu-id="f7a28-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f7a28-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f7a28-111">ResetCache</span><span class="sxs-lookup"><span data-stu-id="f7a28-111">ResetCache</span></span>  <br/> |<span data-ttu-id="f7a28-112">Gibt an, dass der Cache zurückgesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f7a28-112">Indicates that the cache should be reset.</span></span>  <br/> |
|<span data-ttu-id="f7a28-113">ReturnDeletedItems</span><span class="sxs-lookup"><span data-stu-id="f7a28-113">ReturnDeletedItems</span></span>  <br/> |<span data-ttu-id="f7a28-114">Gibt an, dass gelöschte Elemente zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f7a28-114">Indicates that deleted items should be returned.</span></span>  <br/> |
|<span data-ttu-id="f7a28-115">ReturnHighlightTerms</span><span class="sxs-lookup"><span data-stu-id="f7a28-115">ReturnHighlightTerms</span></span>  <br/> |<span data-ttu-id="f7a28-116">Gibt an, dass hervorgehobene Ausdrücke zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f7a28-116">Indicates that highlighted terms should be returned.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f7a28-117">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f7a28-117">Child elements</span></span>

<span data-ttu-id="f7a28-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="f7a28-118">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f7a28-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f7a28-119">Parent elements</span></span>

|<span data-ttu-id="f7a28-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="f7a28-120">**Element**</span></span>|<span data-ttu-id="f7a28-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f7a28-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f7a28-122">FindItem</span><span class="sxs-lookup"><span data-stu-id="f7a28-122">FindItem</span></span>](finditem.md) <br/> |<span data-ttu-id="f7a28-123">Definiert eine Anforderung zum Suchen von Elementen in einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="f7a28-123">Defines a request to find items in a mailbox.</span></span>  <br/> <span data-ttu-id="f7a28-124">Im folgenden finden Sie den XPath-Ausdruck für dieses Element:/FindItem.</span><span class="sxs-lookup"><span data-stu-id="f7a28-124">The following is the XPath expression to this element: /FindItem.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f7a28-125">Textwert</span><span class="sxs-lookup"><span data-stu-id="f7a28-125">Text value</span></span>

<span data-ttu-id="f7a28-126">Der Text-Wert des **QueryString** -Elements stellt eine Post Fach Abfrage dar, die mithilfe einer Teilmenge der [erweiterten Abfrage Syntax (AQS)](https://msdn.microsoft.com/library/aa965711%28VS.85%29.aspx)vorgenommen wird.</span><span class="sxs-lookup"><span data-stu-id="f7a28-126">The **QueryString** element text value represents a mailbox query that is made by using a subset of [Advanced Query Syntax (AQS)](https://msdn.microsoft.com/library/aa965711%28VS.85%29.aspx).</span></span> <span data-ttu-id="f7a28-127">Weitere Informationen zu den unterstützten Syntaxoptionen für Abfragezeichenfolgen finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="f7a28-127">See the remarks section for information about the supported syntax options for query strings.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f7a28-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f7a28-128">Remarks</span></span>

<span data-ttu-id="f7a28-129">In Exchange Server 2010 ist dieses Element ein XML-Schema Zeichenfolgen-Typ.</span><span class="sxs-lookup"><span data-stu-id="f7a28-129">In Exchange Server 2010, this element is an XML schema string type.</span></span> <span data-ttu-id="f7a28-130">In Exchange-Versionen, die mit Exchange Server 2013 beginnen, einschließlich Exchange Online, ist der Typ für dieses Element **querystringtype**.</span><span class="sxs-lookup"><span data-stu-id="f7a28-130">In versions of Exchange starting with Exchange Server 2013, including Exchange Online, the type for this element is **QueryStringType**.</span></span> <span data-ttu-id="f7a28-131">Durch diese Änderung werden keine vorhandenen Clients unterbrechen, da drei neue optionale Attribute hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="f7a28-131">This change does not break any existing clients because it adds three new optional attributes.</span></span> 
  
<span data-ttu-id="f7a28-132">Das **QueryString** -Element schließt die Verwendung von EWS-Einschränkungen aus.</span><span class="sxs-lookup"><span data-stu-id="f7a28-132">The **QueryString** element excludes the use of EWS restrictions.</span></span> <span data-ttu-id="f7a28-133">AQS in EWS unterstützt drei Arten von Einschränkungen: Wort Phasen Einschränkungen, Datumsbereichs Einschränkungen und Einschränkungen für Nachrichtentypen.</span><span class="sxs-lookup"><span data-stu-id="f7a28-133">AQS in EWS supports three types of restrictions: word phase restriction, date range restriction, and message type restriction.</span></span> <span data-ttu-id="f7a28-134">In den folgenden Tabellen werden die unterstützten Sucheigenschaften für die einzelnen Einschränkungstypen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="f7a28-134">The following tables list the supported search properties for each restriction type.</span></span> 
  
<span data-ttu-id="f7a28-135">**Word-Phasen Einschränkung**</span><span class="sxs-lookup"><span data-stu-id="f7a28-135">**Word phase restriction**</span></span>

|<span data-ttu-id="f7a28-136">**Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="f7a28-136">**Property**</span></span>|<span data-ttu-id="f7a28-137">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="f7a28-137">**Example**</span></span>|<span data-ttu-id="f7a28-138">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="f7a28-138">**Function**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f7a28-139">Von</span><span class="sxs-lookup"><span data-stu-id="f7a28-139">from</span></span>  <br/> |<span data-ttu-id="f7a28-140">Von: Dean</span><span class="sxs-lookup"><span data-stu-id="f7a28-140">From:Dean</span></span>  <br/> <span data-ttu-id="f7a28-141">Von: "Dean hehe"</span><span class="sxs-lookup"><span data-stu-id="f7a28-141">From:"Dean Halstead"</span></span>  <br/> |<span data-ttu-id="f7a28-142">Von Dean gesendete Suchelemente.</span><span class="sxs-lookup"><span data-stu-id="f7a28-142">Search items sent from Dean.</span></span>  <br/> <span data-ttu-id="f7a28-143">Von Dean hehe gesendete Suchelemente.</span><span class="sxs-lookup"><span data-stu-id="f7a28-143">Search items sent from Dean Halstead.</span></span> <span data-ttu-id="f7a28-144">Der Absender muss genau "Dean hehe" sein.</span><span class="sxs-lookup"><span data-stu-id="f7a28-144">The sender must be exactly "Dean Halstead".</span></span>  <br/> |
|<span data-ttu-id="f7a28-145">in</span><span class="sxs-lookup"><span data-stu-id="f7a28-145">to</span></span>  <br/> |<span data-ttu-id="f7a28-146">An: Dean</span><span class="sxs-lookup"><span data-stu-id="f7a28-146">To:Dean</span></span>  <br/> |<span data-ttu-id="f7a28-147">An Dean gesendete Suchelemente.</span><span class="sxs-lookup"><span data-stu-id="f7a28-147">Search items sent to Dean.</span></span>  <br/> |
|<span data-ttu-id="f7a28-148">cc</span><span class="sxs-lookup"><span data-stu-id="f7a28-148">cc</span></span>  <br/> |<span data-ttu-id="f7a28-149">Cc: Dean</span><span class="sxs-lookup"><span data-stu-id="f7a28-149">Cc:Dean</span></span>  <br/> |<span data-ttu-id="f7a28-150">Suchen Sie nach Elementen mit Dean in der CC-Zeile.</span><span class="sxs-lookup"><span data-stu-id="f7a28-150">Search for items with Dean on the Cc line.</span></span>  <br/> |
|<span data-ttu-id="f7a28-151">bcc</span><span class="sxs-lookup"><span data-stu-id="f7a28-151">bcc</span></span>  <br/> |<span data-ttu-id="f7a28-152">BCC: Dean</span><span class="sxs-lookup"><span data-stu-id="f7a28-152">Bcc:Dean</span></span>  <br/> |<span data-ttu-id="f7a28-153">Suchen Sie nach Elementen mit Dean in der Zeile Bcc.</span><span class="sxs-lookup"><span data-stu-id="f7a28-153">Search for items with Dean on the Bcc line.</span></span>  <br/> |
|<span data-ttu-id="f7a28-154">Participants</span><span class="sxs-lookup"><span data-stu-id="f7a28-154">Participants</span></span>  <br/> |<span data-ttu-id="f7a28-155">Teilnehmer: Dekan</span><span class="sxs-lookup"><span data-stu-id="f7a28-155">Participants:Dean</span></span>  <br/> |<span data-ttu-id="f7a28-156">Suchen Sie nach Elementen mit Dean in den Feldern an, CC oder Bcc.</span><span class="sxs-lookup"><span data-stu-id="f7a28-156">Search for items with Dean in the To, Cc, or Bcc fields.</span></span>  <br/> |
|<span data-ttu-id="f7a28-157">Betreff</span><span class="sxs-lookup"><span data-stu-id="f7a28-157">Subject</span></span>  <br/> |<span data-ttu-id="f7a28-158">Betreff: product</span><span class="sxs-lookup"><span data-stu-id="f7a28-158">Subject:product</span></span>  <br/> <span data-ttu-id="f7a28-159">Betreff: (Produktentwicklung)</span><span class="sxs-lookup"><span data-stu-id="f7a28-159">Subject:(product development)</span></span>  <br/> <span data-ttu-id="f7a28-160">Betreff: "Produktentwicklung"</span><span class="sxs-lookup"><span data-stu-id="f7a28-160">Subject:"product development"</span></span>  <br/> |<span data-ttu-id="f7a28-161">Suchen nach Elementen mit Produkt im Betreff.</span><span class="sxs-lookup"><span data-stu-id="f7a28-161">Search for items with product in the subject.</span></span>  <br/> <span data-ttu-id="f7a28-162">Suchen Sie nach Elementen mit Produkt und Entwicklung im Betreff.</span><span class="sxs-lookup"><span data-stu-id="f7a28-162">Search for items with product and development in the subject.</span></span>  <br/> |
|<span data-ttu-id="f7a28-163">Body</span><span class="sxs-lookup"><span data-stu-id="f7a28-163">Body</span></span>  <br/> <span data-ttu-id="f7a28-164">Inhalt</span><span class="sxs-lookup"><span data-stu-id="f7a28-164">Content</span></span>  <br/> |<span data-ttu-id="f7a28-165">Body: Fortschritt</span><span class="sxs-lookup"><span data-stu-id="f7a28-165">Body:progress</span></span>  <br/> <span data-ttu-id="f7a28-166">Inhalt: Fortschritt</span><span class="sxs-lookup"><span data-stu-id="f7a28-166">Content:progress</span></span>  <br/> |<span data-ttu-id="f7a28-167">Suchen Sie nach Elementen mit Fortschritt im Textkörper.</span><span class="sxs-lookup"><span data-stu-id="f7a28-167">Search for items with progress in the body.</span></span>  <br/> |
|<span data-ttu-id="f7a28-168">Attachment</span><span class="sxs-lookup"><span data-stu-id="f7a28-168">Attachment</span></span>  <br/> |<span data-ttu-id="f7a28-169">Anlage: Bericht</span><span class="sxs-lookup"><span data-stu-id="f7a28-169">Attachment:report</span></span>  <br/> |<span data-ttu-id="f7a28-170">Suchen Sie nach Elementen mit dem Bericht im Namen der Anlagendatei oder im Datei Text.</span><span class="sxs-lookup"><span data-stu-id="f7a28-170">Search for items with report in the attachment file name or file body.</span></span>  <br/> |
|<span data-ttu-id="f7a28-171">(Eigenschaft ist nicht angegeben)</span><span class="sxs-lookup"><span data-stu-id="f7a28-171">(property is not specified)</span></span>  <br/> |<span data-ttu-id="f7a28-172">Produktentwicklung</span><span class="sxs-lookup"><span data-stu-id="f7a28-172">Product Development</span></span>  <br/> |<span data-ttu-id="f7a28-173">Suchen Sie nach Elementen, die sowohl Produkt als auch Entwicklung in allen Word-Phaseneigenschaften enthalten.</span><span class="sxs-lookup"><span data-stu-id="f7a28-173">Search for items that contain both product and development in all word phase properties.</span></span>  <br/> |
   
<span data-ttu-id="f7a28-174">Die Übereinstimmung bei der Wort Phasen Einschränkung wird immer Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="f7a28-174">Word phase restriction match is always case insensitive.</span></span> <span data-ttu-id="f7a28-175">Die Word-Phasen Einschränkung unterstützt zwei Übereinstimmungstypen: Präfixübereinstimmung oder exakte Übereinstimmung.</span><span class="sxs-lookup"><span data-stu-id="f7a28-175">Word phase restriction supports two match types: prefix match or exact match.</span></span> <span data-ttu-id="f7a28-176">Präfixübereinstimmung ist das Standard Übereinstimmungsverhalten.</span><span class="sxs-lookup"><span data-stu-id="f7a28-176">Prefix match is the default match behavior.</span></span> <span data-ttu-id="f7a28-177">Wenn Sie exakte Übereinstimmung wünschen, verwenden Sie doppelte Anführungszeichen.</span><span class="sxs-lookup"><span data-stu-id="f7a28-177">If you want exact match, use double quotes.</span></span> <span data-ttu-id="f7a28-178">Der Betreff: "Product" entspricht beispielsweise "Product", aber nicht "Production" im Betreff.</span><span class="sxs-lookup"><span data-stu-id="f7a28-178">For example, subject:"product" matches 'product' but not 'production' in the subject.</span></span> <span data-ttu-id="f7a28-179">Mehrere Wörter in doppelten Anführungszeichen schränken sowohl die Wort Phasen als auch ihre Reihenfolge ein.</span><span class="sxs-lookup"><span data-stu-id="f7a28-179">Multiple words in double quotes restrict both word phases and their order.</span></span> <span data-ttu-id="f7a28-180">Beispielsweise entspricht "Win Product" nur "Win Product", nicht "Win95-Produkt" oder "Produkt von Win".</span><span class="sxs-lookup"><span data-stu-id="f7a28-180">For example "win product" matches only 'win product', not 'win95 product' or 'product of win'.</span></span> <span data-ttu-id="f7a28-181">Sie können ein Sternchen ( \* ) verwenden, um eine Präfixübereinstimmung mit eingeschränkter Reihenfolge zu definieren.</span><span class="sxs-lookup"><span data-stu-id="f7a28-181">You can use an asterisk (\*) to define a prefix match with order restricted.</span></span> <span data-ttu-id="f7a28-182">Beispielsweise entspricht "Win Product" " \* Win95-Produkt", "Windows-Produktionsreihe", aber nicht "Windows-neues Produkt" oder "Produkt von Win".</span><span class="sxs-lookup"><span data-stu-id="f7a28-182">For example, "win product"\* matches 'win95 product', 'windows production line' but not 'windows new product' or 'product of win'.</span></span> <span data-ttu-id="f7a28-183">Sie können alle Nachrichten durchsuchen, die von oder an eine Domäne gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="f7a28-183">You can search all messages sent from or to a domain.</span></span> <span data-ttu-id="f7a28-184">Beispielsweise von: "@Hotmail. com" gibt alle von Hotmail.com gesendeten Nachrichten zurück.</span><span class="sxs-lookup"><span data-stu-id="f7a28-184">For example, from:"@hotmail.com" returns all messages sent from hotmail.com.</span></span>
  
<span data-ttu-id="f7a28-185">In der folgenden Tabelle werden die Einschränkungen für den Datumsbereich beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f7a28-185">The following table describes date range restrictions.</span></span>
  
<span data-ttu-id="f7a28-186">**Datumsbereichs Einschränkung**</span><span class="sxs-lookup"><span data-stu-id="f7a28-186">**Date range restriction**</span></span>

|<span data-ttu-id="f7a28-187">**Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="f7a28-187">**Property**</span></span>|<span data-ttu-id="f7a28-188">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="f7a28-188">**Example**</span></span>|<span data-ttu-id="f7a28-189">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="f7a28-189">**Function**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f7a28-190">Gesendet</span><span class="sxs-lookup"><span data-stu-id="f7a28-190">Sent</span></span>  <br/> |<span data-ttu-id="f7a28-191">Gesendet: Letzte Woche</span><span class="sxs-lookup"><span data-stu-id="f7a28-191">Sent:last week</span></span>  <br/> <span data-ttu-id="f7a28-192">Sent: 01/01/2001</span><span class="sxs-lookup"><span data-stu-id="f7a28-192">Sent:01/01/2001</span></span>  <br/> <span data-ttu-id="f7a28-193">Sent: 01/01/2001.. 01/15/2001</span><span class="sxs-lookup"><span data-stu-id="f7a28-193">Sent:01/01/2001..01/15/2001</span></span>  <br/> |<span data-ttu-id="f7a28-194">Letzte Woche gesendete Suchelemente.</span><span class="sxs-lookup"><span data-stu-id="f7a28-194">Search items sent last week.</span></span>  <br/> <span data-ttu-id="f7a28-195">Suchelemente, die am 1. Januar 2001 gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="f7a28-195">Search items sent on January 1st, 2001.</span></span>  <br/> <span data-ttu-id="f7a28-196">Suchelemente, die zwischen dem 1. Januar 2001 und dem 15. Januar 2001 gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="f7a28-196">Search items sent between January 1st, 2001 and January 15th, 2001.</span></span>  <br/> |
|<span data-ttu-id="f7a28-197">Auszahlung</span><span class="sxs-lookup"><span data-stu-id="f7a28-197">Received</span></span>  <br/> |<span data-ttu-id="f7a28-198">Empfangen: heute</span><span class="sxs-lookup"><span data-stu-id="f7a28-198">Received:today</span></span>  <br/> <span data-ttu-id="f7a28-199">Empfangen: 01/01/2001</span><span class="sxs-lookup"><span data-stu-id="f7a28-199">Received:01/01/2001</span></span>  <br/> |<span data-ttu-id="f7a28-200">Suchelemente, die heute empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="f7a28-200">Search items received today.</span></span>  <br/> <span data-ttu-id="f7a28-201">Suchelemente, die am 1. Januar 2001 empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="f7a28-201">Search items received on January 1st, 2001.</span></span>  <br/> |
   
<span data-ttu-id="f7a28-202">Die beiden Punkte (..) sind ein Bereichsoperator.</span><span class="sxs-lookup"><span data-stu-id="f7a28-202">The two dots (..) is a range operator.</span></span> <span data-ttu-id="f7a28-203">Es kann verwendet werden, um einen Bereich mit einem Start-und einem Enddatum zu definieren.</span><span class="sxs-lookup"><span data-stu-id="f7a28-203">It can be used to define a range with a start and an end date.</span></span> <span data-ttu-id="f7a28-204">Um ein Datum anzugeben, können Sie relative Datumsangaben verwenden.</span><span class="sxs-lookup"><span data-stu-id="f7a28-204">To specify a date, you can use relative dates.</span></span> <span data-ttu-id="f7a28-205">Die folgenden relativen Datumsangaben werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="f7a28-205">The following relative dates are supported:</span></span>
  
- <span data-ttu-id="f7a28-206">Relative Daten: heute, morgen, gestern</span><span class="sxs-lookup"><span data-stu-id="f7a28-206">Relative dates: Today, tomorrow, yesterday</span></span>
    
- <span data-ttu-id="f7a28-207">Mehr Wort relative Daten: diese Woche, nächster Monat, letzte Woche, letzter Monat oder nächstes Jahr</span><span class="sxs-lookup"><span data-stu-id="f7a28-207">Multiword relative dates: This week, next month, last week, past month, or coming year</span></span>
    
- <span data-ttu-id="f7a28-208">Tage: Sonntag, Montag, Dienstag, Mittwoch, Donnerstag, Freitag, Samstag</span><span class="sxs-lookup"><span data-stu-id="f7a28-208">Days: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday</span></span>
    
- <span data-ttu-id="f7a28-209">Januar, Februar, März, April, Mai, Juni, Juli, August, September, Oktober, November, Dezember</span><span class="sxs-lookup"><span data-stu-id="f7a28-209">January, February, March, April, May, June, July, August, September, October, November, December</span></span>
    
<span data-ttu-id="f7a28-210">In der folgenden Tabelle werden Einschränkungen für Nachrichtentypen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f7a28-210">The following table describes message type restrictions.</span></span> 
  
<span data-ttu-id="f7a28-211">**Einschränkung des Nachrichtentyps**</span><span class="sxs-lookup"><span data-stu-id="f7a28-211">**Message type restriction**</span></span>

|<span data-ttu-id="f7a28-212">**Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="f7a28-212">**Property**</span></span>|<span data-ttu-id="f7a28-213">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="f7a28-213">**Example**</span></span>|<span data-ttu-id="f7a28-214">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="f7a28-214">**Function**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f7a28-215">Art</span><span class="sxs-lookup"><span data-stu-id="f7a28-215">Kind</span></span>  <br/> |<span data-ttu-id="f7a28-216">Kind: Tasks</span><span class="sxs-lookup"><span data-stu-id="f7a28-216">Kind:tasks</span></span>  <br/> |<span data-ttu-id="f7a28-217">Alle Aufgabenelemente durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="f7a28-217">Search all task items.</span></span>  <br/> |
   
<span data-ttu-id="f7a28-218">AQS in EWS verwendet die **Kind** -Eigenschaft, um den Nachrichtentyp anzugeben.</span><span class="sxs-lookup"><span data-stu-id="f7a28-218">AQS in EWS uses the **Kind** property to specify the message type.</span></span> <span data-ttu-id="f7a28-219">Die Kind-Eigenschaft kann mit den folgenden Elementtypen verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="f7a28-219">The Kind property can be used with the following item types:</span></span> 
  
- <span data-ttu-id="f7a28-220">email</span><span class="sxs-lookup"><span data-stu-id="f7a28-220">email</span></span>
    
- <span data-ttu-id="f7a28-221">meetings</span><span class="sxs-lookup"><span data-stu-id="f7a28-221">meetings</span></span>
    
- <span data-ttu-id="f7a28-222">tasks</span><span class="sxs-lookup"><span data-stu-id="f7a28-222">tasks</span></span>
    
- <span data-ttu-id="f7a28-223">notes</span><span class="sxs-lookup"><span data-stu-id="f7a28-223">notes</span></span>
    
- <span data-ttu-id="f7a28-224">docs</span><span class="sxs-lookup"><span data-stu-id="f7a28-224">docs</span></span>
    
- <span data-ttu-id="f7a28-225">journals</span><span class="sxs-lookup"><span data-stu-id="f7a28-225">journals</span></span>
    
- <span data-ttu-id="f7a28-226">contacts</span><span class="sxs-lookup"><span data-stu-id="f7a28-226">contacts</span></span>
    
- <span data-ttu-id="f7a28-227">im</span><span class="sxs-lookup"><span data-stu-id="f7a28-227">im</span></span>
    
<span data-ttu-id="f7a28-228">In der folgenden Tabelle wird die Gruppierung logischer Connectors beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f7a28-228">The following table describes grouping logical connectors.</span></span>
  
<span data-ttu-id="f7a28-229">**Gruppieren von logischen Connectors**</span><span class="sxs-lookup"><span data-stu-id="f7a28-229">**Grouping logical connectors**</span></span>

|<span data-ttu-id="f7a28-230">**Connector**</span><span class="sxs-lookup"><span data-stu-id="f7a28-230">**Connector**</span></span>|<span data-ttu-id="f7a28-231">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="f7a28-231">**Example**</span></span>|<span data-ttu-id="f7a28-232">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="f7a28-232">**Function**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f7a28-233">UND</span><span class="sxs-lookup"><span data-stu-id="f7a28-233">AND</span></span>  <br/> |<span data-ttu-id="f7a28-234">Betreff: Produkt und Betreff: Development</span><span class="sxs-lookup"><span data-stu-id="f7a28-234">Subject:product AND subject:development</span></span>  <br/> <span data-ttu-id="f7a28-235">Betreff: (Produkt und Entwicklung)</span><span class="sxs-lookup"><span data-stu-id="f7a28-235">Subject:(product AND development)</span></span>  <br/> <span data-ttu-id="f7a28-236">Betreff: (Produktentwicklung)</span><span class="sxs-lookup"><span data-stu-id="f7a28-236">Subject:(product development)</span></span>  <br/> |<span data-ttu-id="f7a28-237">Suchen von Elementen sowohl mit Produkt als auch mit der Entwicklung im Betreff.</span><span class="sxs-lookup"><span data-stu-id="f7a28-237">Search items with both product and development in the subject.</span></span>  <br/> |
|<span data-ttu-id="f7a28-238">ODER</span><span class="sxs-lookup"><span data-stu-id="f7a28-238">OR</span></span>  <br/> |<span data-ttu-id="f7a28-239">Body: Projekt oder Body: Vorschlag</span><span class="sxs-lookup"><span data-stu-id="f7a28-239">Body:project OR body:proposal</span></span>  <br/> <span data-ttu-id="f7a28-240">Body: (Projekt oder Vorschlag)</span><span class="sxs-lookup"><span data-stu-id="f7a28-240">Body:(project OR proposal)</span></span>  <br/> |<span data-ttu-id="f7a28-241">Suchen von Elementen mit einem Produkt oder einer Entwicklung im Textkörper.</span><span class="sxs-lookup"><span data-stu-id="f7a28-241">Search items with either product or development in the body.</span></span>  <br/> |
|<span data-ttu-id="f7a28-242">NICHT</span><span class="sxs-lookup"><span data-stu-id="f7a28-242">NOT</span></span>  <br/> |<span data-ttu-id="f7a28-243">Not Body: Vorschlag</span><span class="sxs-lookup"><span data-stu-id="f7a28-243">NOT body:proposal</span></span>  <br/> <span data-ttu-id="f7a28-244">Body: (kein Vorschlag)</span><span class="sxs-lookup"><span data-stu-id="f7a28-244">Body:(NOT proposal)</span></span>  <br/> |<span data-ttu-id="f7a28-245">Suchen nach Nachrichten ohne Vorschlag im Textkörper.</span><span class="sxs-lookup"><span data-stu-id="f7a28-245">Search messages without proposal in the body.</span></span>  <br/> |
   
<span data-ttu-id="f7a28-246">Und ist immer der standardmäßige Connector.</span><span class="sxs-lookup"><span data-stu-id="f7a28-246">AND is always the default connector.</span></span> <span data-ttu-id="f7a28-247">Beispielsweise Betreff: Project und Body: Vorschlag ist identisch mit Betreff: Project Body: Proposal.</span><span class="sxs-lookup"><span data-stu-id="f7a28-247">For example, subject:project AND body:proposal is the same as subject:project body:proposal.</span></span> <span data-ttu-id="f7a28-248">Bei logischen Connectors wird die Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="f7a28-248">Logical connectors are case sensitive.</span></span> <span data-ttu-id="f7a28-249">Body: (Project oder Proposal) sucht beispielsweise Nachrichten mit "Project", "or" und "Proposal" im Textkörper anstelle von "Project" oder "Proposal".</span><span class="sxs-lookup"><span data-stu-id="f7a28-249">For example, body:(project Or proposal) searches messages with 'project', 'or', and 'proposal' in the body instead of 'project' or 'proposal'.</span></span> <span data-ttu-id="f7a28-250">Das Plus-Symbol (+) entspricht und.</span><span class="sxs-lookup"><span data-stu-id="f7a28-250">The plus symbol (+) is equivalent to AND.</span></span> <span data-ttu-id="f7a28-251">Das Bindestrich Symbol (-) entspricht nicht.</span><span class="sxs-lookup"><span data-stu-id="f7a28-251">The hyphen symbol (-) is equivalent to NOT.</span></span> <span data-ttu-id="f7a28-252">Body: (Project-proposal) sucht beispielsweise Nachrichten mit "Project", aber ohne "Vorschlag" im Textkörper.</span><span class="sxs-lookup"><span data-stu-id="f7a28-252">For example, body:(project - proposal) searches messages with 'project' but without 'proposal' in the body.</span></span> 
  
<span data-ttu-id="f7a28-253">Die Abfragezeichenfolge kann auch nicht indizierte Eigenschaften für die Suche enthalten.</span><span class="sxs-lookup"><span data-stu-id="f7a28-253">The query string can also contain nonindexed properties for search.</span></span> <span data-ttu-id="f7a28-254">Wenn die Abfragezeichenfolge nicht indizierte Eigenschaften enthält, kann die Suche eine Exchange-Suche für die indizierten Eigenschaften und eine Speichersuche in den nicht indizierten Eigenschaften durchführen.</span><span class="sxs-lookup"><span data-stu-id="f7a28-254">If the query string contains nonindexed properties, the search might perform an Exchange search on the indexed properties and a store search on the nonindexed properties.</span></span> 
  
<span data-ttu-id="f7a28-255">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="f7a28-255">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="example"></a><span data-ttu-id="f7a28-256">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f7a28-256">Example</span></span>

<span data-ttu-id="f7a28-257">Das folgende Beispiel zeigt eine Anforderung zum Suchen nach Nachrichten im Posteingang mit AutoErmittlung im Betreff.</span><span class="sxs-lookup"><span data-stu-id="f7a28-257">The following example shows a request to search for messages in the Inbox with Autodiscover in the subject.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010" />
  </soap:Header>
  <soap:Body>
    <m:FindItem Traversal="Shallow">
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:IndexedPageItemView MaxEntriesReturned="1" Offset="0" BasePoint="Beginning" />
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox" />
      </m:ParentFolderIds>
      <m:QueryString>subject:Autodiscover</m:QueryString>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="f7a28-258">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="f7a28-258">The following example shows a successful response to the request.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="0" 
                         MajorBuildNumber="639" 
                         MinorBuildNumber="20" 
                         Version="Exchange2010" 
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="1" 
                        TotalItemsInView="5" 
                        IncludesLastItemInRange="false">
            <t:Items>
              <t:Message>
                <t:ItemId Id="AAMkADEzOTExYjJkLTYx" ChangeKey="CQAAABY" />
                <t:Subject>How to use Autodiscover</t:Subject>
              </t:Message>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>

```

## <a name="element-information"></a><span data-ttu-id="f7a28-259">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="f7a28-259">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f7a28-260">Namespace</span><span class="sxs-lookup"><span data-stu-id="f7a28-260">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f7a28-261">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f7a28-261">Schema name</span></span>  <br/> |<span data-ttu-id="f7a28-262">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="f7a28-262">Messages schema</span></span>  <br/> |
|<span data-ttu-id="f7a28-263">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f7a28-263">Validation file</span></span>  <br/> |<span data-ttu-id="f7a28-264">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="f7a28-264">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f7a28-265">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="f7a28-265">Can be empty</span></span>  <br/> |<span data-ttu-id="f7a28-266">False</span><span class="sxs-lookup"><span data-stu-id="f7a28-266">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f7a28-267">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f7a28-267">See also</span></span>



[<span data-ttu-id="f7a28-268">FindItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f7a28-268">FindItem operation</span></span>](finditem-operation.md)
  
[<span data-ttu-id="f7a28-269">FindConversation-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f7a28-269">FindConversation operation</span></span>](findconversation-operation.md)


- [<span data-ttu-id="f7a28-270">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="f7a28-270">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

