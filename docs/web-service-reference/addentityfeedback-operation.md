---
title: AddEntityFeedback-Vorgang
manager: luken
ms.date: 4/18/2016
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 00e40197-5794-4268-b937-bd65aa044890
description: Der AddEntityFeedback-Vorgang gibt Fehlerinformationen zurück, die serverseitigen Problemen entsprechen.
ms.openlocfilehash: a1027a0a1ee06cf3e83833b1d84c13d77b07c0b9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458439"
---
# <a name="addentityfeedback-operation"></a><span data-ttu-id="26088-103">AddEntityFeedback-Vorgang</span><span class="sxs-lookup"><span data-stu-id="26088-103">AddEntityFeedback operation</span></span>

<span data-ttu-id="26088-104">Der **AddEntityFeedback** -Vorgang gibt Fehlerinformationen zurück, die serverseitigen Problemen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="26088-104">The **AddEntityFeedback** operation returns error information corresponding to server-side issues.</span></span> 
  
<span data-ttu-id="26088-105">Dieser Vorgang basiert auf dem Typ des protokollierten Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="26088-105">This operation relies on the type of event being logged.</span></span> <span data-ttu-id="26088-106">Eines der wichtigsten Ereignisse ist **EntityAdded**, das einer Entität entspricht, die ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="26088-106">One of the most important events is **EntityAdded**, which corresponds to an entity being selected.</span></span> <span data-ttu-id="26088-107">Dieser Vorgang ist Batch, sodass er zum Protokollieren von Batches von Einträgen in einer einzelnen Anforderung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="26088-107">This operation is batch, so it can be used to log batches of entries in a single request.</span></span> 
  
## <a name="findpeople-request-examples"></a><span data-ttu-id="26088-108">FindPeople-Anforderungs Beispiele</span><span class="sxs-lookup"><span data-stu-id="26088-108">FindPeople request examples</span></span>

<span data-ttu-id="26088-109">Der **AddEntityFeedback** -Vorgang bietet Clients die Möglichkeit, Details zur Interaktion mit vom Dienst zurückgegebenen Entitäten zu protokollieren.</span><span class="sxs-lookup"><span data-stu-id="26088-109">The **AddEntityFeedback** operation provides a way for clients to log details of interaction with entities returned by the service.</span></span> <span data-ttu-id="26088-110">Dies kann als Signal verwendet werden, um die Relevanz hinter den Kulissen für jeden Client zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="26088-110">This can be used as a signal to improve relevance behind the scenes for each client.</span></span> <span data-ttu-id="26088-111">Beispielsweise können Clients diesen Vorgang verwenden, um Feedback zu Personen Entitäten bereitzustellen, die von **FindPeople**zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="26088-111">E.g., Clients can use this operation to provide feedback on people entities returned from **FindPeople**.</span></span>
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
                             xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                             xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:AddEntityFeedback>
            <m:EntityFeedbackEntries>
                  <t:EntityFeedbackEntry>
                        <t:ClientEventTimeUTC> 2015-07-05T22:16:18+00:00</t:ClientEventTimeUTC>
                        <t:ClientEventTimeLocal> 2015-07-05T22:16:18+00:00</t:ClientEventTimeLocal>
                        <t:ClientSessionId>00000000-0000-0000-0000-000000000012</t:ClientSessionId>
                        <t:ClientVersion>15.01.0101.01</t:ClientVersion>
                        <t:ClientId>Web</t:ClientId>
                        <t:TransactionId>123456789</t:TransactionId>
                        <t:EventType>EntityAdded</t:EventType>
                        <t:TargetEntityList>["a","b","c"]</t:TargetEntityList>
                        <t:SourceOfEntityAdded></t:SourceOfEntityAdded>
                        <t:JSONPropertyBag></t:JSONPropertyBag>
                  </t:EntityFeedbackEntry>
                  <t:EntityFeedbackEntry>
                  …
                  </t:EntityFeedbackEntry>
            </m:EntityFeedbackEntries>
      </m:AddEntityFeedback>
   </soap:Body>
</soap:Envelope>

```

### <a name="the-request-soap-body-contents"></a><span data-ttu-id="26088-112">Der Inhalt des SOAP-Anforderungstexts</span><span class="sxs-lookup"><span data-stu-id="26088-112">The request SOAP body contents</span></span>

<span data-ttu-id="26088-113">Die SOAP-Anforderung enthält ein einzelnes Element **EntityFeedbackEntries**.</span><span class="sxs-lookup"><span data-stu-id="26088-113">The soap request contains a single element **EntityFeedbackEntries**.</span></span> <span data-ttu-id="26088-114">Dies wiederum enthält ein Array von **EntityFeedbackEntry** -Objekten.</span><span class="sxs-lookup"><span data-stu-id="26088-114">This in turn contains an array of **EntityFeedbackEntry** objects.</span></span> <span data-ttu-id="26088-115">Jeder Eintrag im Array kann die folgenden Elemente enthalten:</span><span class="sxs-lookup"><span data-stu-id="26088-115">Each entry in the array can contain the following elements.</span></span> 
  
|<span data-ttu-id="26088-116">**Anforderungsparameter**</span><span class="sxs-lookup"><span data-stu-id="26088-116">**Request Parameters**</span></span>|<span data-ttu-id="26088-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="26088-117">**Required**</span></span>|<span data-ttu-id="26088-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="26088-118">**Description**</span></span>|<span data-ttu-id="26088-119">**Typ**</span><span class="sxs-lookup"><span data-stu-id="26088-119">**Type**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="26088-120">**ClientEventTimeUtc**</span><span class="sxs-lookup"><span data-stu-id="26088-120">**ClientEventTimeUtc**</span></span> <br/> |<span data-ttu-id="26088-121">Ja</span><span class="sxs-lookup"><span data-stu-id="26088-121">Yes</span></span>  <br/> |<span data-ttu-id="26088-122">Die UTC-Zeit, zu der das Ereignis auf Clientseite aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="26088-122">The UTC time the event occurred on the client-side.</span></span>  <br/> |<span data-ttu-id="26088-123">DateTime</span><span class="sxs-lookup"><span data-stu-id="26088-123">DateTime</span></span>  <br/> |
|<span data-ttu-id="26088-124">**ClientEventTimeLocal**</span><span class="sxs-lookup"><span data-stu-id="26088-124">**ClientEventTimeLocal**</span></span> <br/> |<span data-ttu-id="26088-125">Ja</span><span class="sxs-lookup"><span data-stu-id="26088-125">Yes</span></span>  <br/> |<span data-ttu-id="26088-126">Die lokale Zeit, zu der das Ereignis auf der Clientseite aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="26088-126">The local time the event occurred on the client side.</span></span>  <br/> |<span data-ttu-id="26088-127">DateTime</span><span class="sxs-lookup"><span data-stu-id="26088-127">DateTime</span></span>  <br/> |
|<span data-ttu-id="26088-128">**ClientID**</span><span class="sxs-lookup"><span data-stu-id="26088-128">**ClientId**</span></span> <br/> |<span data-ttu-id="26088-129">Ja</span><span class="sxs-lookup"><span data-stu-id="26088-129">Yes</span></span>  <br/> |<span data-ttu-id="26088-130">Typ des Clients (beispielsweise Outlook, OWA usw.).</span><span class="sxs-lookup"><span data-stu-id="26088-130">Type of Client (E.g., Outlook, OWA, etc.).</span></span>  <br/> |<span data-ttu-id="26088-131">ClientIDType-Aufzählung</span><span class="sxs-lookup"><span data-stu-id="26088-131">ClientIDType Enumeration</span></span>  <br/> |
|<span data-ttu-id="26088-132">**ClientSessionId**</span><span class="sxs-lookup"><span data-stu-id="26088-132">**ClientSessionId**</span></span> <br/> |<span data-ttu-id="26088-133">Ja</span><span class="sxs-lookup"><span data-stu-id="26088-133">Yes</span></span>  <br/> |<span data-ttu-id="26088-134">GUID, die die Sitzungs-ID identifiziert.</span><span class="sxs-lookup"><span data-stu-id="26088-134">GUID Identifying the session ID.</span></span> <span data-ttu-id="26088-135">Auf dem Client generiert.</span><span class="sxs-lookup"><span data-stu-id="26088-135">Generated on the client.</span></span>  <br/> |<span data-ttu-id="26088-136">GUID</span><span class="sxs-lookup"><span data-stu-id="26088-136">GUID</span></span>  <br/> |
|<span data-ttu-id="26088-137">**ClientVersion**</span><span class="sxs-lookup"><span data-stu-id="26088-137">**ClientVersion**</span></span> <br/> |<span data-ttu-id="26088-138">Ja</span><span class="sxs-lookup"><span data-stu-id="26088-138">Yes</span></span>  <br/> |<span data-ttu-id="26088-139">Version des Clients (beispielsweise 15.01.0101.000).</span><span class="sxs-lookup"><span data-stu-id="26088-139">Version of the client (E.g., 15.01.0101.000).</span></span>  <br/> |<span data-ttu-id="26088-140">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="26088-140">String</span></span>  <br/> |
|<span data-ttu-id="26088-141">**EntityAddSource**</span><span class="sxs-lookup"><span data-stu-id="26088-141">**EntityAddSource**</span></span> <br/> |<span data-ttu-id="26088-142">Nein</span><span class="sxs-lookup"><span data-stu-id="26088-142">No</span></span>  <br/> |<span data-ttu-id="26088-143">Quelle für EntityAded (E.g., EntityRelevanceAPI, types, pasted).</span><span class="sxs-lookup"><span data-stu-id="26088-143">Source for EntityAded (E.g., EntityRelevanceAPI, types, pasted).</span></span>  <br/> |<span data-ttu-id="26088-144">EntityAddSource-Aufzählung</span><span class="sxs-lookup"><span data-stu-id="26088-144">EntityAddSource Enumeration</span></span>  <br/> |
|<span data-ttu-id="26088-145">**EntrySequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="26088-145">**EntrySequenceNumber**</span></span> <br/> |<span data-ttu-id="26088-146">Ja</span><span class="sxs-lookup"><span data-stu-id="26088-146">Yes</span></span>  <br/> |<span data-ttu-id="26088-147">Eine inkrementelle ganze Zahl pro Clientsitzung.</span><span class="sxs-lookup"><span data-stu-id="26088-147">An incremental integer per client session.</span></span> <span data-ttu-id="26088-148">Wird zum Erkennen von Datenverlusten verwendet.</span><span class="sxs-lookup"><span data-stu-id="26088-148">Used for detecting data loss.</span></span>  <br/> |<span data-ttu-id="26088-149">Int</span><span class="sxs-lookup"><span data-stu-id="26088-149">Int</span></span>  <br/> |
|<span data-ttu-id="26088-150">**EventType**</span><span class="sxs-lookup"><span data-stu-id="26088-150">**EventType**</span></span> <br/> |<span data-ttu-id="26088-151">Ja</span><span class="sxs-lookup"><span data-stu-id="26088-151">Yes</span></span>  <br/> |<span data-ttu-id="26088-152">Typ des Ereignisses (z.b. Entität hinzugefügt, Entität entfernt).</span><span class="sxs-lookup"><span data-stu-id="26088-152">Type of event (E.g., Entity Added, Entity Removed).</span></span>  <br/> |<span data-ttu-id="26088-153">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="26088-153">String</span></span>  <br/> |
|<span data-ttu-id="26088-154">**JSONPropertyBag**</span><span class="sxs-lookup"><span data-stu-id="26088-154">**JSONPropertyBag**</span></span> <br/> |<span data-ttu-id="26088-155">Nein</span><span class="sxs-lookup"><span data-stu-id="26088-155">No</span></span>  <br/> |<span data-ttu-id="26088-156">Zusätzliche Eigenschaften, die dem Ereignis zugeordnet sind (JSON-BLOB von Schlüssel/Wert-Paaren).</span><span class="sxs-lookup"><span data-stu-id="26088-156">Additional properties associated with the event (JSON blob of key/value pairs).</span></span>  <br/> |<span data-ttu-id="26088-157">JSON-BLOB</span><span class="sxs-lookup"><span data-stu-id="26088-157">JSON Blob</span></span>  <br/> |
|<span data-ttu-id="26088-158">**TargetEntityList**</span><span class="sxs-lookup"><span data-stu-id="26088-158">**TargetEntityList**</span></span> <br/> |<span data-ttu-id="26088-159">Nein</span><span class="sxs-lookup"><span data-stu-id="26088-159">No</span></span>  <br/> |<span data-ttu-id="26088-160">Liste der Entitäten, die dem Ereignis zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="26088-160">List of entities associated with the event.</span></span>  <br/> |<span data-ttu-id="26088-161">JSON-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="26088-161">JSON String</span></span>  <br/> |
|<span data-ttu-id="26088-162">**TransactionId**</span><span class="sxs-lookup"><span data-stu-id="26088-162">**TransactionId**</span></span> <br/> |<span data-ttu-id="26088-163">Nein</span><span class="sxs-lookup"><span data-stu-id="26088-163">No</span></span>  <br/> |<span data-ttu-id="26088-164">ID (GUID) korrelieren der ID in Abfrageprotokollen.</span><span class="sxs-lookup"><span data-stu-id="26088-164">ID (GUID) correlating the ID in query logs.</span></span>  <br/> |<span data-ttu-id="26088-165">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="26088-165">String</span></span>  <br/> |
   
### <a name="successful-addentityfeedback-operation-response"></a><span data-ttu-id="26088-166">Erfolgreiche Reaktion des AddEntityFeedback-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="26088-166">Successful AddEntityFeedback operation response</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
    <s:Header>
        <h:ServerVersionInfo MajorVersion="15" 
                                MinorVersion="1" 
                                MajorBuildNumber="228" 
                                MinorBuildNumber="0" 
                                Version="V2_49" 
                                xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                                xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                                xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
    </s:Header>
    <s:Body>
        <AddEntityFeedbackResponse ResponseClass="Success" 
                                                              xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                                              xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                                                              xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
            <ResponseCode>NoError</ResponseCode>
            <ErrorCount>0</ErrorCount>
            <ErrorDetails />
        </AddEntityFeedbackResponse>
    </s:Body>
</s:Envelope> 

```

### <a name="the-response-soap-body-contains-the-following-elements"></a><span data-ttu-id="26088-167">Der SOAP-Antworttext Körper enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="26088-167">The response SOAP body contains the following elements</span></span>

#### <a name="errors"></a><span data-ttu-id="26088-168">Fehler</span><span class="sxs-lookup"><span data-stu-id="26088-168">Errors</span></span> 
  
<span data-ttu-id="26088-169">Die API kann einen Batch von Feedback Einträgen protokollieren, wir protokollieren alles, was wir können.</span><span class="sxs-lookup"><span data-stu-id="26088-169">The API can log a batch of feedback entries, we log all that we can.</span></span> <span data-ttu-id="26088-170">Dieses Feld stellt die Anzahl der Fehlereinträge dar, die nicht protokolliert wurden.</span><span class="sxs-lookup"><span data-stu-id="26088-170">This field represents the number of error entries that were not logged.</span></span>
    
#### <a name="errordetails"></a><span data-ttu-id="26088-171">ErrorDetails</span><span class="sxs-lookup"><span data-stu-id="26088-171">ErrorDetails</span></span>
  
<span data-ttu-id="26088-172">Details zu den oben aufgeführten Fehlern werden durch getrennt `;` .</span><span class="sxs-lookup"><span data-stu-id="26088-172">Details pertaining to the errors above separates by `;`.</span></span>
    
### <a name="currently-supported-values"></a><span data-ttu-id="26088-173">Derzeit unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="26088-173">Currently supported values</span></span>

|<span data-ttu-id="26088-174">**ClientIdType-Aufzählung**</span><span class="sxs-lookup"><span data-stu-id="26088-174">**ClientIdType Enumeration**</span></span>|
|:-----|
|<span data-ttu-id="26088-175">Desktop</span><span class="sxs-lookup"><span data-stu-id="26088-175">Desktop</span></span>  <br/> |
|<span data-ttu-id="26088-176">Exchange</span><span class="sxs-lookup"><span data-stu-id="26088-176">Exchange</span></span>  <br/> |
|<span data-ttu-id="26088-177">IMAP4</span><span class="sxs-lookup"><span data-stu-id="26088-177">IMAP4</span></span>  <br/> |
|<span data-ttu-id="26088-178">Lync</span><span class="sxs-lookup"><span data-stu-id="26088-178">Lync</span></span>  <br/> |
|<span data-ttu-id="26088-179">MacMail</span><span class="sxs-lookup"><span data-stu-id="26088-179">MacMail</span></span>  <br/> |
|<span data-ttu-id="26088-180">MacOutlook</span><span class="sxs-lookup"><span data-stu-id="26088-180">MacOutlook</span></span>  <br/> |
|<span data-ttu-id="26088-181">Mobil</span><span class="sxs-lookup"><span data-stu-id="26088-181">Mobile</span></span>  <br/> |
|<span data-ttu-id="26088-182">Andere</span><span class="sxs-lookup"><span data-stu-id="26088-182">Other</span></span>  <br/> |
|<span data-ttu-id="26088-183">Outlook</span><span class="sxs-lookup"><span data-stu-id="26088-183">Outlook</span></span>  <br/> |
|<span data-ttu-id="26088-184">Outlook Service</span><span class="sxs-lookup"><span data-stu-id="26088-184">OutlookService</span></span>  <br/> |
|<span data-ttu-id="26088-185">POP3</span><span class="sxs-lookup"><span data-stu-id="26088-185">POP3</span></span>  <br/> |
|<span data-ttu-id="26088-186">Tablet</span><span class="sxs-lookup"><span data-stu-id="26088-186">Tablet</span></span>  <br/> |
|<span data-ttu-id="26088-187">Web</span><span class="sxs-lookup"><span data-stu-id="26088-187">Web</span></span>  <br/> |
   
|<span data-ttu-id="26088-188">**EntityAddSource-Aufzählung**</span><span class="sxs-lookup"><span data-stu-id="26088-188">**EntityAddSource Enumeration**</span></span>|
|:-----|
|<span data-ttu-id="26088-189">ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="26088-189">ActiveDirectory</span></span>  <br/> |
|<span data-ttu-id="26088-190">EntityRelevanceApi</span><span class="sxs-lookup"><span data-stu-id="26088-190">EntityRelevanceApi</span></span>  <br/> |
|<span data-ttu-id="26088-191">EntityRelevanceApiCache</span><span class="sxs-lookup"><span data-stu-id="26088-191">EntityRelevanceApiCache</span></span>  <br/> |
|<span data-ttu-id="26088-192">ExplicitTyping</span><span class="sxs-lookup"><span data-stu-id="26088-192">ExplicitTyping</span></span>  <br/> |
|<span data-ttu-id="26088-193">LocalCache</span><span class="sxs-lookup"><span data-stu-id="26088-193">LocalCache</span></span>  <br/> |
|<span data-ttu-id="26088-194">LocalCacheAndEntityRelevanceAPI</span><span class="sxs-lookup"><span data-stu-id="26088-194">LocalCacheAndEntityRelevanceAPI</span></span>  <br/> |
|<span data-ttu-id="26088-195">Keine</span><span class="sxs-lookup"><span data-stu-id="26088-195">None</span></span>  <br/> |
|<span data-ttu-id="26088-196">Andere</span><span class="sxs-lookup"><span data-stu-id="26088-196">Other</span></span>  <br/> |
|<span data-ttu-id="26088-197">Einfügen</span><span class="sxs-lookup"><span data-stu-id="26088-197">Paste</span></span>  <br/> |
   
### <a name="addentityfeedback-operation-error-response"></a><span data-ttu-id="26088-198">Fehlerantwort des AddEntityFeedback-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="26088-198">AddEntityFeedback operation error response</span></span>

<span data-ttu-id="26088-199">Informationen zu Fehlercodes, die für EWS allgemein sind, finden Sie unter [Response Code](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="26088-199">For error codes that are generic to EWS, see [ResponseCode](responsecode.md).</span></span>
  
### <a name="example-of-addentityfeedback-in-conjunction-with-findpeople"></a><span data-ttu-id="26088-200">Beispiel für AddEntityFeedback in Verbindung mit FindPeople</span><span class="sxs-lookup"><span data-stu-id="26088-200">Example of AddEntityFeedback in conjunction with FindPeople</span></span>

#### <a name="findpeople-request"></a><span data-ttu-id="26088-201">FindPeople-Anforderung</span><span class="sxs-lookup"><span data-stu-id="26088-201">FindPeople request</span></span>
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
<soap:Body >
    <m:FindPeople>
      <m:IndexedPageItemView BasePoint="Beginning" MaxEntriesReturned="100" Offset="0"/>
      <m:QueryString>user1</m:QueryString>
      <m:SearchPeopleSuggestionIndex>true</m:SearchPeopleSuggestionIndex>
    </m:FindPeople>
  </soap:Body>
</soap:Envelope>    
    
```

#### <a name="findpeople-response"></a><span data-ttu-id="26088-202">FindPeople-Antwort</span><span class="sxs-lookup"><span data-stu-id="26088-202">FindPeople response</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
    <s:Header>
        <h:ServerVersionInfo MajorVersion="15" MinorVersion="1" MajorBuildNumber="302" MinorBuildNumber="0" Version="V2_68" xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
    </s:Header>
    <s:Body>
        <FindPeopleResponse ResponseClass="Success" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
            <ResponseCode>NoError</ResponseCode>
            <People>
                <Persona xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
                    <PersonaId Id="AAUQAFjZ4UxX8SZCqSPFsmh0cSo=" />
                    <PersonaType>Person</PersonaType>
                    <CreationTime>2015-10-02T23:25:42</CreationTime>
                    <DisplayName>user2</DisplayName>
…
                  </Persona>
            </People>
            <TotalNumberOfPeopleInView>0</TotalNumberOfPeopleInView>
            <FirstMatchingRowIndex>0</FirstMatchingRowIndex>
            <FirstLoadedRowIndex>0</FirstLoadedRowIndex>
            <TransactionId>b56ad16e-5d5a-4574-90f8-b8dd57382be6</TransactionId>
        </FindPeopleResponse>
    </s:Body>
</s:Envelope>

```

#### <a name="addentityfeedback-request"></a><span data-ttu-id="26088-203">AddEntityFeedback-Anforderung</span><span class="sxs-lookup"><span data-stu-id="26088-203">AddEntityFeedback request</span></span>

```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:AddEntityFeedback>
<m:EntityFeedbackEntries>
<t:EntityFeedbackEntry>
         <t:ClientEventTimeUtc>2015-07-05T22:16:18+00:00</t:ClientEventTimeUtc>
         <t:ClientEventTimeLocal>2015-07-05T22:16:18+00:00</t:ClientEventTimeLocal>
         <t:ClientSessionId>00000000-0000-0000-0000-000000000012</t:ClientSessionId>
         <t:ClientVersion>15.01.0101.01</t:ClientVersion>
         <t:ClientId>Web</t:ClientId>
         <t:TransactionId>b56ad16e-5d5a-4574-90f8-b8dd57382be6</t:TransactionId>
         <t:EventType>EntityAdded</t:EventType>
         <t:TargetEntityList>["user1@ms7.com"]</t:TargetEntityList>
         <t:SourceOfEntityAdded>EntityRelevanceApi</t:SourceOfEntityAdded>
         <t:JSONPropertyBag></t:JSONPropertyBag>
</t:EntityFeedbackEntry>
</m:EntityFeedbackEntries>
      </m:AddEntityFeedback>
   </soap:Body>
</soap:Envelope>

```

> [!NOTE]
> <span data-ttu-id="26088-204">Verwenden der FindPeople-Antwort Transaktions-ID als AddEntityFeedback-Anforderungs Transaktions-ID.</span><span class="sxs-lookup"><span data-stu-id="26088-204">Using FindPeople response transaction ID as the AddEntityFeedback request transaction ID.</span></span> 
  
#### <a name="addentityfeedback-response"></a><span data-ttu-id="26088-205">AddEntityFeedback-Antwort</span><span class="sxs-lookup"><span data-stu-id="26088-205">AddEntityFeedback response</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
    <s:Header>
        <h:ServerVersionInfo MajorVersion="15" MinorVersion="1" MajorBuildNumber="302" MinorBuildNumber="0" Version="V2_68" xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
    </s:Header>
    <s:Body>
        <AddEntityFeedbackResponse ResponseClass="Success" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
            <ResponseCode>NoError</ResponseCode>
            <ErrorCount>0</ErrorCount>
            <ErrorDetails />
        </AddEntityFeedbackResponse>
    </s:Body>
</s:Envelope>

```


