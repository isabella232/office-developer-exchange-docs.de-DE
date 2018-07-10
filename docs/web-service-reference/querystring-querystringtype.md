---
title: QueryString (QueryStringType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- QueryString
api_type:
- schema
ms.assetid: cadbf9a5-b87e-4d7f-b488-b76fb0ee7150
description: Das QueryString-Element enthält eine Postfach-Abfragezeichenfolge basierend auf Erweiterte Query Syntax (AQS).
ms.openlocfilehash: 410405638b3f8628dc589049873cfea1f153310c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830943"
---
# <a name="querystring-querystringtype"></a><span data-ttu-id="f4fb1-103">QueryString (QueryStringType)</span><span class="sxs-lookup"><span data-stu-id="f4fb1-103">QueryString (QueryStringType)</span></span>

<span data-ttu-id="f4fb1-104">Das **QueryString** -Element enthält eine Postfach-Abfragezeichenfolge basierend auf Erweiterte Query Syntax (AQS).</span><span class="sxs-lookup"><span data-stu-id="f4fb1-104">The **QueryString** element contains a mailbox query string based on Advanced Query Syntax (AQS).</span></span> 
  
```XML
<QueryString/>
```

 <span data-ttu-id="f4fb1-105">**QueryStringType**</span><span class="sxs-lookup"><span data-stu-id="f4fb1-105">**QueryStringType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f4fb1-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f4fb1-106">Attributes and elements</span></span>

<span data-ttu-id="f4fb1-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f4fb1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f4fb1-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="f4fb1-108">Attributes</span></span>

|<span data-ttu-id="f4fb1-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="f4fb1-109">**Attribute**</span></span>|<span data-ttu-id="f4fb1-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f4fb1-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f4fb1-111">ResetCache</span><span class="sxs-lookup"><span data-stu-id="f4fb1-111">ResetCache</span></span>  <br/> |<span data-ttu-id="f4fb1-112">Gibt an, dass der Cache zurückgesetzt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f4fb1-112">Indicates that the cache should be reset.</span></span>  <br/> |
|<span data-ttu-id="f4fb1-113">ReturnDeletedItems</span><span class="sxs-lookup"><span data-stu-id="f4fb1-113">ReturnDeletedItems</span></span>  <br/> |<span data-ttu-id="f4fb1-114">Gibt an, dass gelöschte Elemente zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f4fb1-114">Indicates that deleted items should be returned.</span></span>  <br/> |
|<span data-ttu-id="f4fb1-115">ReturnHighlightTerms</span><span class="sxs-lookup"><span data-stu-id="f4fb1-115">ReturnHighlightTerms</span></span>  <br/> |<span data-ttu-id="f4fb1-116">Gibt an, dass hervorgehobene Begriffe zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f4fb1-116">Indicates that highlighted terms should be returned.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f4fb1-117">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f4fb1-117">Child elements</span></span>

<span data-ttu-id="f4fb1-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="f4fb1-118">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f4fb1-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f4fb1-119">Parent elements</span></span>

|<span data-ttu-id="f4fb1-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="f4fb1-120">**Element**</span></span>|<span data-ttu-id="f4fb1-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f4fb1-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f4fb1-122">FindItem</span><span class="sxs-lookup"><span data-stu-id="f4fb1-122">FindItem</span></span>](finditem.md) <br/> |<span data-ttu-id="f4fb1-123">Definiert eine Anforderung zum Suchen von Elementen in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="f4fb1-123">Defines a request to find items in a mailbox.</span></span>  <br/> <span data-ttu-id="f4fb1-124">Im folgenden werden der XPath-Ausdruck, der dieses Element: /FindItem.</span><span class="sxs-lookup"><span data-stu-id="f4fb1-124">The following is the XPath expression to this element: /FindItem.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f4fb1-125">Textwert</span><span class="sxs-lookup"><span data-stu-id="f4fb1-125">Text value</span></span>

<span data-ttu-id="f4fb1-126">Der Textwert der **QueryString** -Element stellt eine Postfach-Abfrage, die mithilfe einer Teilmenge der [(Erweiterte Query Syntax, AQS)](http://msdn.microsoft.com/de-de/library/aa965711%28VS.85%29.aspx)erfolgt ist.</span><span class="sxs-lookup"><span data-stu-id="f4fb1-126">The **QueryString** element text value represents a mailbox query that is made by using a subset of [Advanced Query Syntax (AQS)](http://msdn.microsoft.com/de-de/library/aa965711%28VS.85%29.aspx).</span></span> <span data-ttu-id="f4fb1-127">Finden Sie im Abschnitt "Hinweise" Informationen zu den unterstützten Syntaxoptionen für Abfragezeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="f4fb1-127">See the remarks section for information about the supported syntax options for query strings.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f4fb1-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f4fb1-128">Remarks</span></span>

<span data-ttu-id="f4fb1-129">Exchange Server 2010 ist dieses Element vom Typ String XML-Schema.</span><span class="sxs-lookup"><span data-stu-id="f4fb1-129">In Exchange Server 2010, this element is an XML schema string type.</span></span> <span data-ttu-id="f4fb1-130">In Versionen von Exchange, beginnend mit Exchange Server 2013 ist einschließlich Exchange Online, den Typ für dieses Element **QueryStringType**.</span><span class="sxs-lookup"><span data-stu-id="f4fb1-130">In versions of Exchange starting with Exchange Server 2013, including Exchange Online, the type for this element is **QueryStringType**.</span></span> <span data-ttu-id="f4fb1-131">Diese Änderung wird alle vorhandenen Clients werden nicht umbrochen, da drei neue optionale Attribute hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f4fb1-131">This change does not break any existing clients because it adds three new optional attributes.</span></span> 
  
<span data-ttu-id="f4fb1-132">Das Element **QueryString** schließt die Verwendung der EWS-Einschränkungen aus.</span><span class="sxs-lookup"><span data-stu-id="f4fb1-132">The **QueryString** element excludes the use of EWS restrictions.</span></span> <span data-ttu-id="f4fb1-133">AQS im EWS unterstützt drei Arten von Beschränkungen: word-Phase Einschränkung, Datum Bereich Einschränkung und Nachricht Typ Einschränkung.</span><span class="sxs-lookup"><span data-stu-id="f4fb1-133">AQS in EWS supports three types of restrictions: word phase restriction, date range restriction, and message type restriction.</span></span> <span data-ttu-id="f4fb1-134">Den folgenden Tabellen sind die unterstützten Sucheigenschaften für jeden Einschränkungstyp.</span><span class="sxs-lookup"><span data-stu-id="f4fb1-134">The following tables list the supported search properties for each restriction type.</span></span> 
  
<span data-ttu-id="f4fb1-135">**Word Phase Einschränkung**</span><span class="sxs-lookup"><span data-stu-id="f4fb1-135">**Word phase restriction**</span></span>

|<span data-ttu-id="f4fb1-136">**Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="f4fb1-136">**Property**</span></span>|<span data-ttu-id="f4fb1-137">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="f4fb1-137">**Example**</span></span>|<span data-ttu-id="f4fb1-138">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="f4fb1-138">**Function**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f4fb1-139">Von</span><span class="sxs-lookup"><span data-stu-id="f4fb1-139">from</span></span>  <br/> |<span data-ttu-id="f4fb1-140">Von: Dominik</span><span class="sxs-lookup"><span data-stu-id="f4fb1-140">From:Dean</span></span>  <br/> <span data-ttu-id="f4fb1-141">Aus: "Dominik Halstead"</span><span class="sxs-lookup"><span data-stu-id="f4fb1-141">From:"Dean Halstead"</span></span>  <br/> |<span data-ttu-id="f4fb1-142">Suchen von Dominik gesendete Elemente.</span><span class="sxs-lookup"><span data-stu-id="f4fb1-142">Search items sent from Dean.</span></span>  <br/> <span data-ttu-id="f4fb1-143">Suchen von Dean Halstead gesendete Elemente.</span><span class="sxs-lookup"><span data-stu-id="f4fb1-143">Search items sent from Dean Halstead.</span></span> <span data-ttu-id="f4fb1-144">Der Absender muss genau "Dominik Halstead".</span><span class="sxs-lookup"><span data-stu-id="f4fb1-144">The sender must be exactly "Dean Halstead".</span></span>  <br/> |
|<span data-ttu-id="f4fb1-145">in</span><span class="sxs-lookup"><span data-stu-id="f4fb1-145">to</span></span>  <br/> |<span data-ttu-id="f4fb1-146">An: Dominik</span><span class="sxs-lookup"><span data-stu-id="f4fb1-146">To:Dean</span></span>  <br/> |<span data-ttu-id="f4fb1-147">Suchen Sie Elemente, die an Dominik gesendet.</span><span class="sxs-lookup"><span data-stu-id="f4fb1-147">Search items sent to Dean.</span></span>  <br/> |
|<span data-ttu-id="f4fb1-148">cc</span><span class="sxs-lookup"><span data-stu-id="f4fb1-148">cc</span></span>  <br/> |<span data-ttu-id="f4fb1-149">Cc:Dean</span><span class="sxs-lookup"><span data-stu-id="f4fb1-149">Cc:Dean</span></span>  <br/> |<span data-ttu-id="f4fb1-150">Suchen Sie nach Elementen mit Dominik in der Zeile Cc.</span><span class="sxs-lookup"><span data-stu-id="f4fb1-150">Search for items with Dean on the Cc line.</span></span>  <br/> |
|<span data-ttu-id="f4fb1-151">bcc</span><span class="sxs-lookup"><span data-stu-id="f4fb1-151">bcc</span></span>  <br/> |<span data-ttu-id="f4fb1-152">Bcc:Dean</span><span class="sxs-lookup"><span data-stu-id="f4fb1-152">Bcc:Dean</span></span>  <br/> |<span data-ttu-id="f4fb1-153">Suchen Sie nach Elementen mit Dominik in der Bcc-Zeile.</span><span class="sxs-lookup"><span data-stu-id="f4fb1-153">Search for items with Dean on the Bcc line.</span></span>  <br/> |
|<span data-ttu-id="f4fb1-154">Teilnehmer</span><span class="sxs-lookup"><span data-stu-id="f4fb1-154">Participants</span></span>  <br/> |<span data-ttu-id="f4fb1-155">Teilnehmer: Dominik</span><span class="sxs-lookup"><span data-stu-id="f4fb1-155">Participants:Dean</span></span>  <br/> |<span data-ttu-id="f4fb1-156">Suchen Sie nach Elementen mit Dominik in an, Cc oder Bcc Felder.</span><span class="sxs-lookup"><span data-stu-id="f4fb1-156">Search for items with Dean in the To, Cc, or Bcc fields.</span></span>  <br/> |
|<span data-ttu-id="f4fb1-157">Subject</span><span class="sxs-lookup"><span data-stu-id="f4fb1-157">Subject</span></span>  <br/> |<span data-ttu-id="f4fb1-158">Betreff: Produkt</span><span class="sxs-lookup"><span data-stu-id="f4fb1-158">Subject:product</span></span>  <br/> <span data-ttu-id="f4fb1-159">Betreff:(product development)</span><span class="sxs-lookup"><span data-stu-id="f4fb1-159">Subject:(product development)</span></span>  <br/> <span data-ttu-id="f4fb1-160">Betreff: "Produktentwicklung"</span><span class="sxs-lookup"><span data-stu-id="f4fb1-160">Subject:"product development"</span></span>  <br/> |<span data-ttu-id="f4fb1-161">Suchen Sie nach Elementen mit Produkt im Betreff.</span><span class="sxs-lookup"><span data-stu-id="f4fb1-161">Search for items with product in the subject.</span></span>  <br/> <span data-ttu-id="f4fb1-162">Suchen Sie nach Elementen mit Produkt- und Entwicklung im Betreff.</span><span class="sxs-lookup"><span data-stu-id="f4fb1-162">Search for items with product and development in the subject.</span></span>  <br/> |
|<span data-ttu-id="f4fb1-163">Textkörper</span><span class="sxs-lookup"><span data-stu-id="f4fb1-163">Body</span></span>  <br/> <span data-ttu-id="f4fb1-164">Inhalt</span><span class="sxs-lookup"><span data-stu-id="f4fb1-164">Content</span></span>  <br/> |<span data-ttu-id="f4fb1-165">Body: Status</span><span class="sxs-lookup"><span data-stu-id="f4fb1-165">Body:progress</span></span>  <br/> <span data-ttu-id="f4fb1-166">Inhalt: Status</span><span class="sxs-lookup"><span data-stu-id="f4fb1-166">Content:progress</span></span>  <br/> |<span data-ttu-id="f4fb1-167">Suchen Sie nach Elementen mit dem Fortschritt im Textkörper.</span><span class="sxs-lookup"><span data-stu-id="f4fb1-167">Search for items with progress in the body.</span></span>  <br/> |
|<span data-ttu-id="f4fb1-168">Anlage</span><span class="sxs-lookup"><span data-stu-id="f4fb1-168">Attachment</span></span>  <br/> |<span data-ttu-id="f4fb1-169">Anhang: Bericht</span><span class="sxs-lookup"><span data-stu-id="f4fb1-169">Attachment:report</span></span>  <br/> |<span data-ttu-id="f4fb1-170">Suchen Sie nach Elementen mit Bericht der Name oder die Datei Textkörper Anlage-Datei.</span><span class="sxs-lookup"><span data-stu-id="f4fb1-170">Search for items with report in the attachment file name or file body.</span></span>  <br/> |
|<span data-ttu-id="f4fb1-171">(die Eigenschaft ist nicht angegeben)</span><span class="sxs-lookup"><span data-stu-id="f4fb1-171">(property is not specified)</span></span>  <br/> |<span data-ttu-id="f4fb1-172">Produktentwicklung</span><span class="sxs-lookup"><span data-stu-id="f4fb1-172">Product Development</span></span>  <br/> |<span data-ttu-id="f4fb1-173">Suchen Sie nach Elementen, die Produkt- und Entwicklung Word Phase Eigenschaften enthalten.</span><span class="sxs-lookup"><span data-stu-id="f4fb1-173">Search for items that contain both product and development in all word phase properties.</span></span>  <br/> |
   
<span data-ttu-id="f4fb1-174">Word Phase Einschränkung Übereinstimmung ist immer zwischen Groß-und Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="f4fb1-174">Word phase restriction match is always case insensitive.</span></span> <span data-ttu-id="f4fb1-175">Word Phase Beschränkung unterstützt zwei Übereinstimmungstypen: Präfix oder genaue Entsprechung.</span><span class="sxs-lookup"><span data-stu-id="f4fb1-175">Word phase restriction supports two match types: prefix match or exact match.</span></span> <span data-ttu-id="f4fb1-176">Präfixübereinstimmung ist das Standardverhalten für die Übereinstimmung.</span><span class="sxs-lookup"><span data-stu-id="f4fb1-176">Prefix match is the default match behavior.</span></span> <span data-ttu-id="f4fb1-177">Wenn Sie eine genaue Übereinstimmung möchten, verwenden Sie doppelte Anführungszeichen.</span><span class="sxs-lookup"><span data-stu-id="f4fb1-177">If you want exact match, use double quotes.</span></span> <span data-ttu-id="f4fb1-178">Z. B. Betreff: "Produkt" stimmt mit 'Product' aber nicht 'Backup' im Betreff.</span><span class="sxs-lookup"><span data-stu-id="f4fb1-178">For example, subject:"product" matches 'product' but not 'production' in the subject.</span></span> <span data-ttu-id="f4fb1-179">Mehrere Wörter in doppelte Anführungszeichen einschränken Word Phasen und deren Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="f4fb1-179">Multiple words in double quotes restrict both word phases and their order.</span></span> <span data-ttu-id="f4fb1-180">Produkt beispielsweise "win" ermittelt nur "Win Produkt", nicht "Windows 95 Produkt" oder "Produkt des Win".</span><span class="sxs-lookup"><span data-stu-id="f4fb1-180">For example "win product" matches only 'win product', not 'win95 product' or 'product of win'.</span></span> <span data-ttu-id="f4fb1-181">Sie können ein Sternchen (\*) so definieren Sie eine präfixübereinstimmung mit Reihenfolge eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="f4fb1-181">You can use an asterisk (\*) to define a prefix match with order restricted.</span></span> <span data-ttu-id="f4fb1-182">Beispielsweise "win Produkt"\* 'Windows 95 Produkt', 'Windows Produktion Line', aber nicht "Windows neue Produkt" oder "Produkt des Win" entspricht.</span><span class="sxs-lookup"><span data-stu-id="f4fb1-182">For example, "win product"\* matches 'win95 product', 'windows production line' but not 'windows new product' or 'product of win'.</span></span> <span data-ttu-id="f4fb1-183">Sie können alle Nachrichten aus oder einer Domäne suchen.</span><span class="sxs-lookup"><span data-stu-id="f4fb1-183">You can search all messages sent from or to a domain.</span></span> <span data-ttu-id="f4fb1-184">Beispielsweise from:"@hotmail.com" gibt alle Nachrichten von hotmail.com zurück.</span><span class="sxs-lookup"><span data-stu-id="f4fb1-184">For example, from:"@hotmail.com" returns all messages sent from hotmail.com.</span></span>
  
<span data-ttu-id="f4fb1-185">Die folgende Tabelle beschreibt Datum Bereich Einschränkungen.</span><span class="sxs-lookup"><span data-stu-id="f4fb1-185">The following table describes date range restrictions.</span></span>
  
<span data-ttu-id="f4fb1-186">**Datum Bereich Einschränkung**</span><span class="sxs-lookup"><span data-stu-id="f4fb1-186">**Date range restriction**</span></span>

|<span data-ttu-id="f4fb1-187">**Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="f4fb1-187">**Property**</span></span>|<span data-ttu-id="f4fb1-188">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="f4fb1-188">**Example**</span></span>|<span data-ttu-id="f4fb1-189">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="f4fb1-189">**Function**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f4fb1-190">Gesendet</span><span class="sxs-lookup"><span data-stu-id="f4fb1-190">Sent</span></span>  <br/> |<span data-ttu-id="f4fb1-191">Gesendet: letzte Woche</span><span class="sxs-lookup"><span data-stu-id="f4fb1-191">Sent:last week</span></span>  <br/> <span data-ttu-id="f4fb1-192">Gesendet: 01/01/2001</span><span class="sxs-lookup"><span data-stu-id="f4fb1-192">Sent:01/01/2001</span></span>  <br/> <span data-ttu-id="f4fb1-193">Sent:01/01/2001..01/15/2001</span><span class="sxs-lookup"><span data-stu-id="f4fb1-193">Sent:01/01/2001..01/15/2001</span></span>  <br/> |<span data-ttu-id="f4fb1-194">Search-Elemente, die letzte Woche gesendet.</span><span class="sxs-lookup"><span data-stu-id="f4fb1-194">Search items sent last week.</span></span>  <br/> <span data-ttu-id="f4fb1-195">Suchen Sie am 1. Januar 2001 gesendete Elemente.</span><span class="sxs-lookup"><span data-stu-id="f4fb1-195">Search items sent on January 1st, 2001.</span></span>  <br/> <span data-ttu-id="f4fb1-196">Suchen Sie Elemente, die zwischen dem 1. Januar 2001 und dem 15. Januar 2001 gesendet.</span><span class="sxs-lookup"><span data-stu-id="f4fb1-196">Search items sent between January 1st, 2001 and January 15th, 2001.</span></span>  <br/> |
|<span data-ttu-id="f4fb1-197">Auszahlung</span><span class="sxs-lookup"><span data-stu-id="f4fb1-197">Received</span></span>  <br/> |<span data-ttu-id="f4fb1-198">Empfangen: heute</span><span class="sxs-lookup"><span data-stu-id="f4fb1-198">Received:today</span></span>  <br/> <span data-ttu-id="f4fb1-199">Empfangen: 01/01/2001</span><span class="sxs-lookup"><span data-stu-id="f4fb1-199">Received:01/01/2001</span></span>  <br/> |<span data-ttu-id="f4fb1-200">Suchen Sie noch heute empfangenen Elemente.</span><span class="sxs-lookup"><span data-stu-id="f4fb1-200">Search items received today.</span></span>  <br/> <span data-ttu-id="f4fb1-201">Suchen Sie am 1. Januar 2001 empfangenen Elemente.</span><span class="sxs-lookup"><span data-stu-id="f4fb1-201">Search items received on January 1st, 2001.</span></span>  <br/> |
   
<span data-ttu-id="f4fb1-202">Die zwei Punkte (.) ist ein Range-Operator.</span><span class="sxs-lookup"><span data-stu-id="f4fb1-202">The two dots (..) is a range operator.</span></span> <span data-ttu-id="f4fb1-203">Hiermit können Sie einen Bereich mit einer Start- und Enddatum zu definieren.</span><span class="sxs-lookup"><span data-stu-id="f4fb1-203">It can be used to define a range with a start and an end date.</span></span> <span data-ttu-id="f4fb1-204">Um ein Datum angeben, können Sie die relative Daten verwenden.</span><span class="sxs-lookup"><span data-stu-id="f4fb1-204">To specify a date, you can use relative dates.</span></span> <span data-ttu-id="f4fb1-205">Die folgenden relativen Datumsangaben werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="f4fb1-205">The following relative dates are supported:</span></span>
  
- <span data-ttu-id="f4fb1-206">Relative Datumsangaben: heute, morgen, gestern</span><span class="sxs-lookup"><span data-stu-id="f4fb1-206">Relative dates: Today, tomorrow, yesterday</span></span>
    
- <span data-ttu-id="f4fb1-207">Relative Datumsangaben aus: Diese Woche, nächsten Monat, letzte Woche, letzten Monat oder Jahr</span><span class="sxs-lookup"><span data-stu-id="f4fb1-207">Multiword relative dates: This week, next month, last week, past month, or coming year</span></span>
    
- <span data-ttu-id="f4fb1-208">Tage: Sonntag, Montag, Dienstag, Mittwoch, Donnerstag, Freitag, Samstag</span><span class="sxs-lookup"><span data-stu-id="f4fb1-208">Days: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday</span></span>
    
- <span data-ttu-id="f4fb1-209">Januar, Februar, März, Mai April, Juni, Juli, August, September, Oktober, November, Dezember</span><span class="sxs-lookup"><span data-stu-id="f4fb1-209">January, February, March, April, May, June, July, August, September, October, November, December</span></span>
    
<span data-ttu-id="f4fb1-210">Die folgende Tabelle beschreibt die Nachricht Typ Einschränkungen.</span><span class="sxs-lookup"><span data-stu-id="f4fb1-210">The following table describes message type restrictions.</span></span> 
  
<span data-ttu-id="f4fb1-211">**Beschränkung der Nachricht-Typ**</span><span class="sxs-lookup"><span data-stu-id="f4fb1-211">**Message type restriction**</span></span>

|<span data-ttu-id="f4fb1-212">**Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="f4fb1-212">**Property**</span></span>|<span data-ttu-id="f4fb1-213">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="f4fb1-213">**Example**</span></span>|<span data-ttu-id="f4fb1-214">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="f4fb1-214">**Function**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f4fb1-215">Art</span><span class="sxs-lookup"><span data-stu-id="f4fb1-215">Kind</span></span>  <br/> |<span data-ttu-id="f4fb1-216">Art-Aufgaben:</span><span class="sxs-lookup"><span data-stu-id="f4fb1-216">Kind:tasks</span></span>  <br/> |<span data-ttu-id="f4fb1-217">Durchsuchen Sie alle Aufgabenelemente.</span><span class="sxs-lookup"><span data-stu-id="f4fb1-217">Search all task items.</span></span>  <br/> |
   
<span data-ttu-id="f4fb1-218">AQS im EWS verwendet die **Art** -Eigenschaft den Nachrichtentyp an.</span><span class="sxs-lookup"><span data-stu-id="f4fb1-218">AQS in EWS uses the **Kind** property to specify the message type.</span></span> <span data-ttu-id="f4fb1-219">Die Kind-Eigenschaft kann mit den folgenden Elementtypen verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="f4fb1-219">The Kind property can be used with the following item types:</span></span> 
  
- <span data-ttu-id="f4fb1-220">E-Mail</span><span class="sxs-lookup"><span data-stu-id="f4fb1-220">email</span></span>
    
- <span data-ttu-id="f4fb1-221">Besprechungen</span><span class="sxs-lookup"><span data-stu-id="f4fb1-221">meetings</span></span>
    
- <span data-ttu-id="f4fb1-222">tasks</span><span class="sxs-lookup"><span data-stu-id="f4fb1-222">tasks</span></span>
    
- <span data-ttu-id="f4fb1-223">notes</span><span class="sxs-lookup"><span data-stu-id="f4fb1-223">notes</span></span>
    
- <span data-ttu-id="f4fb1-224">Dokumente</span><span class="sxs-lookup"><span data-stu-id="f4fb1-224">docs</span></span>
    
- <span data-ttu-id="f4fb1-225">Journale</span><span class="sxs-lookup"><span data-stu-id="f4fb1-225">journals</span></span>
    
- <span data-ttu-id="f4fb1-226">contacts</span><span class="sxs-lookup"><span data-stu-id="f4fb1-226">contacts</span></span>
    
- <span data-ttu-id="f4fb1-227">Instant Messaging</span><span class="sxs-lookup"><span data-stu-id="f4fb1-227">im</span></span>
    
<span data-ttu-id="f4fb1-228">Die folgende Tabelle beschreibt die logische Connectors gruppieren.</span><span class="sxs-lookup"><span data-stu-id="f4fb1-228">The following table describes grouping logical connectors.</span></span>
  
<span data-ttu-id="f4fb1-229">**Logische Gruppierung-connectors**</span><span class="sxs-lookup"><span data-stu-id="f4fb1-229">**Grouping logical connectors**</span></span>

|<span data-ttu-id="f4fb1-230">**Connector**</span><span class="sxs-lookup"><span data-stu-id="f4fb1-230">**Connector**</span></span>|<span data-ttu-id="f4fb1-231">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="f4fb1-231">**Example**</span></span>|<span data-ttu-id="f4fb1-232">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="f4fb1-232">**Function**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f4fb1-233">AND</span><span class="sxs-lookup"><span data-stu-id="f4fb1-233">AND</span></span>  <br/> |<span data-ttu-id="f4fb1-234">Betreff: Produkt-und Thema: Entwicklung</span><span class="sxs-lookup"><span data-stu-id="f4fb1-234">Subject:product AND subject:development</span></span>  <br/> <span data-ttu-id="f4fb1-235">Betreff:(product AND development)</span><span class="sxs-lookup"><span data-stu-id="f4fb1-235">Subject:(product AND development)</span></span>  <br/> <span data-ttu-id="f4fb1-236">Betreff:(product development)</span><span class="sxs-lookup"><span data-stu-id="f4fb1-236">Subject:(product development)</span></span>  <br/> |<span data-ttu-id="f4fb1-237">Durchsuchen Sie Elemente mit Produkt- und Entwicklung im Betreff.</span><span class="sxs-lookup"><span data-stu-id="f4fb1-237">Search items with both product and development in the subject.</span></span>  <br/> |
|<span data-ttu-id="f4fb1-238">ODER</span><span class="sxs-lookup"><span data-stu-id="f4fb1-238">OR</span></span>  <br/> |<span data-ttu-id="f4fb1-239">Body: Project oder Text Vorschlag:</span><span class="sxs-lookup"><span data-stu-id="f4fb1-239">Body:project OR body:proposal</span></span>  <br/> <span data-ttu-id="f4fb1-240">Body:(project OR proposal)</span><span class="sxs-lookup"><span data-stu-id="f4fb1-240">Body:(project OR proposal)</span></span>  <br/> |<span data-ttu-id="f4fb1-241">Suchen Sie Elemente mit dem Produkt oder Entwicklung im Textkörper.</span><span class="sxs-lookup"><span data-stu-id="f4fb1-241">Search items with either product or development in the body.</span></span>  <br/> |
|<span data-ttu-id="f4fb1-242">NOT</span><span class="sxs-lookup"><span data-stu-id="f4fb1-242">NOT</span></span>  <br/> |<span data-ttu-id="f4fb1-243">NICHT Body: Vorschlag</span><span class="sxs-lookup"><span data-stu-id="f4fb1-243">NOT body:proposal</span></span>  <br/> <span data-ttu-id="f4fb1-244">Body:(NOT proposal)</span><span class="sxs-lookup"><span data-stu-id="f4fb1-244">Body:(NOT proposal)</span></span>  <br/> |<span data-ttu-id="f4fb1-245">Suchen Sie im Textkörper Nachrichten ohne Vorschlag.</span><span class="sxs-lookup"><span data-stu-id="f4fb1-245">Search messages without proposal in the body.</span></span>  <br/> |
   
<span data-ttu-id="f4fb1-246">UND ist immer der Standard-Connector.</span><span class="sxs-lookup"><span data-stu-id="f4fb1-246">AND is always the default connector.</span></span> <span data-ttu-id="f4fb1-247">Beispielsweise Betreff: Projekt und Textkörper: Vorschlag entspricht dem Betreff: Body: Projektvorschlag.</span><span class="sxs-lookup"><span data-stu-id="f4fb1-247">For example, subject:project AND body:proposal is the same as subject:project body:proposal.</span></span> <span data-ttu-id="f4fb1-248">Logische Verbinder sind Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="f4fb1-248">Logical connectors are case sensitive.</span></span> <span data-ttu-id="f4fb1-249">Beispielsweise body:(project Or proposal) sucht Nachrichten mit "Projekt", "oder" und "Vorschlag" im Nachrichtentext anstelle von "Project" oder "Vorschlag".</span><span class="sxs-lookup"><span data-stu-id="f4fb1-249">For example, body:(project Or proposal) searches messages with 'project', 'or', and 'proposal' in the body instead of 'project' or 'proposal'.</span></span> <span data-ttu-id="f4fb1-250">Das Pluszeichen (+) entspricht und.</span><span class="sxs-lookup"><span data-stu-id="f4fb1-250">The plus symbol (+) is equivalent to AND.</span></span> <span data-ttu-id="f4fb1-251">Das Symbol Bindestrich (-) entspricht nicht.</span><span class="sxs-lookup"><span data-stu-id="f4fb1-251">The hyphen symbol (-) is equivalent to NOT.</span></span> <span data-ttu-id="f4fb1-252">Beispielsweise body:(project-proposal) Nachrichten mit "Projekt", jedoch ohne 'Vorschlag' im Text durchsucht.</span><span class="sxs-lookup"><span data-stu-id="f4fb1-252">For example, body:(project - proposal) searches messages with 'project' but without 'proposal' in the body.</span></span> 
  
<span data-ttu-id="f4fb1-253">Die Abfragezeichenfolge kann auch nicht indizierte Eigenschaften für die Suche enthalten.</span><span class="sxs-lookup"><span data-stu-id="f4fb1-253">The query string can also contain nonindexed properties for search.</span></span> <span data-ttu-id="f4fb1-254">Wenn die Abfragezeichenfolge nicht indizierte Eigenschaften enthält, kann die Suche eine Exchange-Suche auf indizierten Eigenschaften sowie eine Store-Suche in nicht indizierten Eigenschaften ausführen.</span><span class="sxs-lookup"><span data-stu-id="f4fb1-254">If the query string contains nonindexed properties, the search might perform an Exchange search on the indexed properties and a store search on the nonindexed properties.</span></span> 
  
<span data-ttu-id="f4fb1-255">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="f4fb1-255">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="example"></a><span data-ttu-id="f4fb1-256">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f4fb1-256">Example</span></span>

<span data-ttu-id="f4fb1-257">Das folgende Beispiel zeigt eine Anforderung an die Nachrichten im Posteingang mit der AutoErmittlung in den Betreff gesucht.</span><span class="sxs-lookup"><span data-stu-id="f4fb1-257">The following example shows a request to search for messages in the Inbox with Autodiscover in the subject.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
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

<span data-ttu-id="f4fb1-258">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die Anforderung.</span><span class="sxs-lookup"><span data-stu-id="f4fb1-258">The following example shows a successful response to the request.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="0" 
                         MajorBuildNumber="639" 
                         MinorBuildNumber="20" 
                         Version="Exchange2010" 
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="element-information"></a><span data-ttu-id="f4fb1-259">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="f4fb1-259">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f4fb1-260">Namespace</span><span class="sxs-lookup"><span data-stu-id="f4fb1-260">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f4fb1-261">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f4fb1-261">Schema name</span></span>  <br/> |<span data-ttu-id="f4fb1-262">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="f4fb1-262">Messages schema</span></span>  <br/> |
|<span data-ttu-id="f4fb1-263">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f4fb1-263">Validation file</span></span>  <br/> |<span data-ttu-id="f4fb1-264">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="f4fb1-264">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f4fb1-265">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="f4fb1-265">Can be empty</span></span>  <br/> |<span data-ttu-id="f4fb1-266">False</span><span class="sxs-lookup"><span data-stu-id="f4fb1-266">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f4fb1-267">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f4fb1-267">See also</span></span>



[<span data-ttu-id="f4fb1-268">FindItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f4fb1-268">FindItem operation</span></span>](finditem-operation.md)
  
[<span data-ttu-id="f4fb1-269">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="f4fb1-269">FindConversation operation</span></span>](findconversation-operation.md)


- [<span data-ttu-id="f4fb1-270">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="f4fb1-270">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

