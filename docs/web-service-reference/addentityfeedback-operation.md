---
title: AddEntityFeedback-Vorgang
manager: luken
ms.date: 4/18/2016
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 00e40197-5794-4268-b937-bd65aa044890
description: Der Vorgang AddEntityFeedback gibt entsprechend der serverseitigen Probleme Fehlerinformationen zurück.
ms.openlocfilehash: b695806f543827d78aea139ffcbd7e4af58b9fef
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757227"
---
# <a name="addentityfeedback-operation"></a><span data-ttu-id="e99c5-103">AddEntityFeedback-Vorgang</span><span class="sxs-lookup"><span data-stu-id="e99c5-103">AddEntityFeedback operation</span></span>

<span data-ttu-id="e99c5-104">Der Vorgang **AddEntityFeedback** gibt entsprechend der serverseitigen Probleme Fehlerinformationen zurück.</span><span class="sxs-lookup"><span data-stu-id="e99c5-104">The **AddEntityFeedback** operation returns error information corresponding to server-side issues.</span></span> 
  
<span data-ttu-id="e99c5-105">Dieser Vorgang basiert auf den Typ des Ereignisses protokolliert wird.</span><span class="sxs-lookup"><span data-stu-id="e99c5-105">This operation relies on the type of event being logged.</span></span> <span data-ttu-id="e99c5-106">Eines der wichtigsten Ereignisse ist **EntityAdded**, der auf eine Entität auswahlwahrscheinlichkeit entspricht.</span><span class="sxs-lookup"><span data-stu-id="e99c5-106">One of the most important events is **EntityAdded**, which corresponds to an entity being selected.</span></span> <span data-ttu-id="e99c5-107">Dieser Vorgang ist Batch, damit dieser Batches von Einträgen in einer einzelnen Anforderung erfassen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="e99c5-107">This operation is batch, so it can be used to log batches of entries in a single request.</span></span> 
  
## <a name="findpeople-request-examples"></a><span data-ttu-id="e99c5-108">FindPeople-anforderungsbeispiele</span><span class="sxs-lookup"><span data-stu-id="e99c5-108">FindPeople request examples</span></span>

<span data-ttu-id="e99c5-109">Der Vorgang **AddEntityFeedback** bietet eine Möglichkeit für Clients, um die Details der Interaktion mit Entitäten, die vom Dienst zurückgegebenen melden.</span><span class="sxs-lookup"><span data-stu-id="e99c5-109">The **AddEntityFeedback** operation provides a way for clients to log details of interaction with entities returned by the service.</span></span> <span data-ttu-id="e99c5-110">Dies kann als Signal zur Verbesserung der Relevanz im Hintergrund für jeden Client verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e99c5-110">This can be used as a signal to improve relevance behind the scenes for each client.</span></span> <span data-ttu-id="e99c5-111">Z. B. können Clients diesen Vorgang Sie Feedback geben möchten auf Personen Entitäten, die von **FindPeople**zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e99c5-111">E.g., Clients can use this operation to provide feedback on people entities returned from **FindPeople**.</span></span>
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
                             xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
                             xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="the-request-soap-body-contents"></a><span data-ttu-id="e99c5-112">Die Anforderung SOAP-Body-Inhalt</span><span class="sxs-lookup"><span data-stu-id="e99c5-112">The request SOAP body contents</span></span>

<span data-ttu-id="e99c5-113">Die Soap-Anforderung enthält ein einzelnes Element **EntityFeedbackEntries**.</span><span class="sxs-lookup"><span data-stu-id="e99c5-113">The soap request contains a single element **EntityFeedbackEntries**.</span></span> <span data-ttu-id="e99c5-114">Dies enthält wiederum ein Array von **EntityFeedbackEntry** -Objekten.</span><span class="sxs-lookup"><span data-stu-id="e99c5-114">This in turn contains an array of **EntityFeedbackEntry** objects.</span></span> <span data-ttu-id="e99c5-115">Jeder Eintrag im Array kann die folgenden Elemente enthalten.</span><span class="sxs-lookup"><span data-stu-id="e99c5-115">Each entry in the array can contain the following elements.</span></span> 
  
|<span data-ttu-id="e99c5-116">**Anforderungsparameter**</span><span class="sxs-lookup"><span data-stu-id="e99c5-116">**Request Parameters**</span></span>|<span data-ttu-id="e99c5-117">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="e99c5-117">**Required**</span></span>|<span data-ttu-id="e99c5-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e99c5-118">**Description**</span></span>|<span data-ttu-id="e99c5-119">**Typ**</span><span class="sxs-lookup"><span data-stu-id="e99c5-119">**Type**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e99c5-120">**ClientEventTimeUtc**</span><span class="sxs-lookup"><span data-stu-id="e99c5-120">**ClientEventTimeUtc**</span></span> <br/> |<span data-ttu-id="e99c5-121">Ja</span><span class="sxs-lookup"><span data-stu-id="e99c5-121">Yes</span></span>  <br/> |<span data-ttu-id="e99c5-122">Die UTC-Zeit, die das Ereignis auf der Clientseite aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="e99c5-122">The UTC time the event occurred on the client-side.</span></span>  <br/> |<span data-ttu-id="e99c5-123">DateTime</span><span class="sxs-lookup"><span data-stu-id="e99c5-123">DateTime</span></span>  <br/> |
|<span data-ttu-id="e99c5-124">**ClientEventTimeLocal**</span><span class="sxs-lookup"><span data-stu-id="e99c5-124">**ClientEventTimeLocal**</span></span> <br/> |<span data-ttu-id="e99c5-125">Ja</span><span class="sxs-lookup"><span data-stu-id="e99c5-125">Yes</span></span>  <br/> |<span data-ttu-id="e99c5-126">Die lokale Uhrzeit des Ereignisses auf dem Client aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="e99c5-126">The local time the event occurred on the client side.</span></span>  <br/> |<span data-ttu-id="e99c5-127">DateTime</span><span class="sxs-lookup"><span data-stu-id="e99c5-127">DateTime</span></span>  <br/> |
|<span data-ttu-id="e99c5-128">**ClientId**</span><span class="sxs-lookup"><span data-stu-id="e99c5-128">**ClientId**</span></span> <br/> |<span data-ttu-id="e99c5-129">Ja</span><span class="sxs-lookup"><span data-stu-id="e99c5-129">Yes</span></span>  <br/> |<span data-ttu-id="e99c5-130">Der Typ des Clients (z. B. Outlook, OWA usw.).</span><span class="sxs-lookup"><span data-stu-id="e99c5-130">Type of Client (E.g., Outlook, OWA, etc.).</span></span>  <br/> |<span data-ttu-id="e99c5-131">ClientIDType-Aufzählung</span><span class="sxs-lookup"><span data-stu-id="e99c5-131">ClientIDType Enumeration</span></span>  <br/> |
|<span data-ttu-id="e99c5-132">**ClientSessionId**</span><span class="sxs-lookup"><span data-stu-id="e99c5-132">**ClientSessionId**</span></span> <br/> |<span data-ttu-id="e99c5-133">Ja</span><span class="sxs-lookup"><span data-stu-id="e99c5-133">Yes</span></span>  <br/> |<span data-ttu-id="e99c5-134">GUID, identifiziert die ID der Sitzung.</span><span class="sxs-lookup"><span data-stu-id="e99c5-134">GUID Identifying the session ID.</span></span> <span data-ttu-id="e99c5-135">Auf dem Client generiert.</span><span class="sxs-lookup"><span data-stu-id="e99c5-135">Generated on the client.</span></span>  <br/> |<span data-ttu-id="e99c5-136">GUID</span><span class="sxs-lookup"><span data-stu-id="e99c5-136">GUID</span></span>  <br/> |
|<span data-ttu-id="e99c5-137">**ClientVersion**</span><span class="sxs-lookup"><span data-stu-id="e99c5-137">**ClientVersion**</span></span> <br/> |<span data-ttu-id="e99c5-138">Ja</span><span class="sxs-lookup"><span data-stu-id="e99c5-138">Yes</span></span>  <br/> |<span data-ttu-id="e99c5-139">Version des Clients (z. B. 15.01.0101.000).</span><span class="sxs-lookup"><span data-stu-id="e99c5-139">Version of the client (E.g., 15.01.0101.000).</span></span>  <br/> |<span data-ttu-id="e99c5-140">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e99c5-140">String</span></span>  <br/> |
|<span data-ttu-id="e99c5-141">**EntityAddSource**</span><span class="sxs-lookup"><span data-stu-id="e99c5-141">**EntityAddSource**</span></span> <br/> |<span data-ttu-id="e99c5-142">Nein</span><span class="sxs-lookup"><span data-stu-id="e99c5-142">No</span></span>  <br/> |<span data-ttu-id="e99c5-143">Quelle für EntityAded (z. B., EntityRelevanceAPI, Typen, eingefügt werden).</span><span class="sxs-lookup"><span data-stu-id="e99c5-143">Source for EntityAded (E.g., EntityRelevanceAPI, types, pasted).</span></span>  <br/> |<span data-ttu-id="e99c5-144">EntityAddSource-Aufzählung</span><span class="sxs-lookup"><span data-stu-id="e99c5-144">EntityAddSource Enumeration</span></span>  <br/> |
|<span data-ttu-id="e99c5-145">**EntrySequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="e99c5-145">**EntrySequenceNumber**</span></span> <br/> |<span data-ttu-id="e99c5-146">Ja</span><span class="sxs-lookup"><span data-stu-id="e99c5-146">Yes</span></span>  <br/> |<span data-ttu-id="e99c5-147">Inkrementelle eine ganze Zahl pro Sitzung.</span><span class="sxs-lookup"><span data-stu-id="e99c5-147">An incremental integer per client session.</span></span> <span data-ttu-id="e99c5-148">Zum Auffinden von Datenverlusten verwendet.</span><span class="sxs-lookup"><span data-stu-id="e99c5-148">Used for detecting data loss.</span></span>  <br/> |<span data-ttu-id="e99c5-149">Int</span><span class="sxs-lookup"><span data-stu-id="e99c5-149">Int</span></span>  <br/> |
|<span data-ttu-id="e99c5-150">**EventType**</span><span class="sxs-lookup"><span data-stu-id="e99c5-150">**EventType**</span></span> <br/> |<span data-ttu-id="e99c5-151">Ja</span><span class="sxs-lookup"><span data-stu-id="e99c5-151">Yes</span></span>  <br/> |<span data-ttu-id="e99c5-152">Typ des Ereignisses (z. B., Entität hinzugefügt, entfernt Entität).</span><span class="sxs-lookup"><span data-stu-id="e99c5-152">Type of event (E.g., Entity Added, Entity Removed).</span></span>  <br/> |<span data-ttu-id="e99c5-153">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e99c5-153">String</span></span>  <br/> |
|<span data-ttu-id="e99c5-154">**JSONPropertyBag**</span><span class="sxs-lookup"><span data-stu-id="e99c5-154">**JSONPropertyBag**</span></span> <br/> |<span data-ttu-id="e99c5-155">Nein</span><span class="sxs-lookup"><span data-stu-id="e99c5-155">No</span></span>  <br/> |<span data-ttu-id="e99c5-156">Zusätzliche Eigenschaften, die das Ereignis (JSON Blob Schlüssel/Wert-Paare) zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="e99c5-156">Additional properties associated with the event (JSON blob of key/value pairs).</span></span>  <br/> |<span data-ttu-id="e99c5-157">JSON Blob</span><span class="sxs-lookup"><span data-stu-id="e99c5-157">JSON Blob</span></span>  <br/> |
|<span data-ttu-id="e99c5-158">**TargetEntityList**</span><span class="sxs-lookup"><span data-stu-id="e99c5-158">**TargetEntityList**</span></span> <br/> |<span data-ttu-id="e99c5-159">Nein</span><span class="sxs-lookup"><span data-stu-id="e99c5-159">No</span></span>  <br/> |<span data-ttu-id="e99c5-160">Liste der Entitäten, die mit dem Ereignis verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="e99c5-160">List of entities associated with the event.</span></span>  <br/> |<span data-ttu-id="e99c5-161">JSON-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e99c5-161">JSON String</span></span>  <br/> |
|<span data-ttu-id="e99c5-162">**Transaktions-ID**</span><span class="sxs-lookup"><span data-stu-id="e99c5-162">**TransactionId**</span></span> <br/> |<span data-ttu-id="e99c5-163">Nein</span><span class="sxs-lookup"><span data-stu-id="e99c5-163">No</span></span>  <br/> |<span data-ttu-id="e99c5-164">ID (GUID) korrelieren der ID im abfrageprotokolle.</span><span class="sxs-lookup"><span data-stu-id="e99c5-164">ID (GUID) correlating the ID in query logs.</span></span>  <br/> |<span data-ttu-id="e99c5-165">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e99c5-165">String</span></span>  <br/> |
   
### <a name="successful-addentityfeedback-operation-response"></a><span data-ttu-id="e99c5-166">Erfolgreiche AddEntityFeedback Vorgangsantwort</span><span class="sxs-lookup"><span data-stu-id="e99c5-166">Successful AddEntityFeedback operation response</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
    <s:Header>
        <h:ServerVersionInfo MajorVersion="15" 
                                MinorVersion="1" 
                                MajorBuildNumber="228" 
                                MinorBuildNumber="0" 
                                Version="V2_49" 
                                xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                                xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                                xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
    </s:Header>
    <s:Body>
        <AddEntityFeedbackResponse ResponseClass="Success" 
                                                              xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" 
                                                              xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                                                              xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
            <ResponseCode>NoError</ResponseCode>
            <ErrorCount>0</ErrorCount>
            <ErrorDetails />
        </AddEntityFeedbackResponse>
    </s:Body>
</s:Envelope> 

```

### <a name="the-response-soap-body-contains-the-following-elements"></a><span data-ttu-id="e99c5-167">Die Antwort SOAP-Text enthält die folgenden Elemente</span><span class="sxs-lookup"><span data-stu-id="e99c5-167">The response SOAP body contains the following elements</span></span>

#### <a name="errors"></a><span data-ttu-id="e99c5-168">Fehler</span><span class="sxs-lookup"><span data-stu-id="e99c5-168">Errors</span></span> 
  
<span data-ttu-id="e99c5-169">Die API ein Batches von Feedback Einträge melden kann, wir melden alle, die wir können.</span><span class="sxs-lookup"><span data-stu-id="e99c5-169">The API can log a batch of feedback entries, we log all that we can.</span></span> <span data-ttu-id="e99c5-170">Dieses Feld stellt die Anzahl der Fehlereinträge, die nicht protokolliert wurden.</span><span class="sxs-lookup"><span data-stu-id="e99c5-170">This field represents the number of error entries that were not logged.</span></span>
    
#### <a name="errordetails"></a><span data-ttu-id="e99c5-171">ErrorDetails</span><span class="sxs-lookup"><span data-stu-id="e99c5-171">ErrorDetails</span></span>
  
<span data-ttu-id="e99c5-172">Einzelheiten zu den oben genannten Fehler durch trennt `;`.</span><span class="sxs-lookup"><span data-stu-id="e99c5-172">Details pertaining to the errors above separates by `;`.</span></span>
    
### <a name="currently-supported-values"></a><span data-ttu-id="e99c5-173">Derzeit unterstützte Werte</span><span class="sxs-lookup"><span data-stu-id="e99c5-173">Currently supported values</span></span>

|<span data-ttu-id="e99c5-174">**ClientIdType-Aufzählung**</span><span class="sxs-lookup"><span data-stu-id="e99c5-174">**ClientIdType Enumeration**</span></span>|
|:-----|
|<span data-ttu-id="e99c5-175">Desktop</span><span class="sxs-lookup"><span data-stu-id="e99c5-175">Desktop</span></span>  <br/> |
|<span data-ttu-id="e99c5-176">Exchange</span><span class="sxs-lookup"><span data-stu-id="e99c5-176">Exchange</span></span>  <br/> |
|<span data-ttu-id="e99c5-177">IMAP4</span><span class="sxs-lookup"><span data-stu-id="e99c5-177">IMAP4</span></span>  <br/> |
|<span data-ttu-id="e99c5-178">Lync</span><span class="sxs-lookup"><span data-stu-id="e99c5-178">Lync</span></span>  <br/> |
|<span data-ttu-id="e99c5-179">MacMail</span><span class="sxs-lookup"><span data-stu-id="e99c5-179">MacMail</span></span>  <br/> |
|<span data-ttu-id="e99c5-180">MacOutlook</span><span class="sxs-lookup"><span data-stu-id="e99c5-180">MacOutlook</span></span>  <br/> |
|<span data-ttu-id="e99c5-181">Mobil</span><span class="sxs-lookup"><span data-stu-id="e99c5-181">Mobile</span></span>  <br/> |
|<span data-ttu-id="e99c5-182">Andere</span><span class="sxs-lookup"><span data-stu-id="e99c5-182">Other</span></span>  <br/> |
|<span data-ttu-id="e99c5-183">Outlook</span><span class="sxs-lookup"><span data-stu-id="e99c5-183">Outlook</span></span>  <br/> |
|<span data-ttu-id="e99c5-184">OutlookService</span><span class="sxs-lookup"><span data-stu-id="e99c5-184">OutlookService</span></span>  <br/> |
|<span data-ttu-id="e99c5-185">POP3</span><span class="sxs-lookup"><span data-stu-id="e99c5-185">POP3</span></span>  <br/> |
|<span data-ttu-id="e99c5-186">Tablet</span><span class="sxs-lookup"><span data-stu-id="e99c5-186">Tablet</span></span>  <br/> |
|<span data-ttu-id="e99c5-187">Web</span><span class="sxs-lookup"><span data-stu-id="e99c5-187">Web</span></span>  <br/> |
   
|<span data-ttu-id="e99c5-188">**EntityAddSource-Aufzählung**</span><span class="sxs-lookup"><span data-stu-id="e99c5-188">**EntityAddSource Enumeration**</span></span>|
|:-----|
|<span data-ttu-id="e99c5-189">ActiveDirectory-Umgebung</span><span class="sxs-lookup"><span data-stu-id="e99c5-189">ActiveDirectory</span></span>  <br/> |
|<span data-ttu-id="e99c5-190">EntityRelevanceApi</span><span class="sxs-lookup"><span data-stu-id="e99c5-190">EntityRelevanceApi</span></span>  <br/> |
|<span data-ttu-id="e99c5-191">EntityRelevanceApiCache</span><span class="sxs-lookup"><span data-stu-id="e99c5-191">EntityRelevanceApiCache</span></span>  <br/> |
|<span data-ttu-id="e99c5-192">ExplicitTyping</span><span class="sxs-lookup"><span data-stu-id="e99c5-192">ExplicitTyping</span></span>  <br/> |
|<span data-ttu-id="e99c5-193">LocalCache</span><span class="sxs-lookup"><span data-stu-id="e99c5-193">LocalCache</span></span>  <br/> |
|<span data-ttu-id="e99c5-194">LocalCacheAndEntityRelevanceAPI</span><span class="sxs-lookup"><span data-stu-id="e99c5-194">LocalCacheAndEntityRelevanceAPI</span></span>  <br/> |
|<span data-ttu-id="e99c5-195">Keine</span><span class="sxs-lookup"><span data-stu-id="e99c5-195">None</span></span>  <br/> |
|<span data-ttu-id="e99c5-196">Andere</span><span class="sxs-lookup"><span data-stu-id="e99c5-196">Other</span></span>  <br/> |
|<span data-ttu-id="e99c5-197">Einfügen</span><span class="sxs-lookup"><span data-stu-id="e99c5-197">Paste</span></span>  <br/> |
   
### <a name="addentityfeedback-operation-error-response"></a><span data-ttu-id="e99c5-198">AddEntityFeedback Vorgang Fehlerantwort</span><span class="sxs-lookup"><span data-stu-id="e99c5-198">AddEntityFeedback operation error response</span></span>

<span data-ttu-id="e99c5-199">Fehlercodes, die für EWS generisch sind, finden Sie unter [ResponseCode](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="e99c5-199">For error codes that are generic to EWS, see [ResponseCode](responsecode.md).</span></span>
  
### <a name="example-of-addentityfeedback-in-conjunction-with-findpeople"></a><span data-ttu-id="e99c5-200">Beispiel für AddEntityFeedback in Verbindung mit FindPeople</span><span class="sxs-lookup"><span data-stu-id="e99c5-200">Example of AddEntityFeedback in conjunction with FindPeople</span></span>

#### <a name="findpeople-request"></a><span data-ttu-id="e99c5-201">FindPeople Anforderung</span><span class="sxs-lookup"><span data-stu-id="e99c5-201">FindPeople request</span></span>
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
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

#### <a name="findpeople-response"></a><span data-ttu-id="e99c5-202">FindPeople Antwort</span><span class="sxs-lookup"><span data-stu-id="e99c5-202">FindPeople response</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
    <s:Header>
        <h:ServerVersionInfo MajorVersion="15" MinorVersion="1" MajorBuildNumber="302" MinorBuildNumber="0" Version="V2_68" xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
    </s:Header>
    <s:Body>
        <FindPeopleResponse ResponseClass="Success" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
            <ResponseCode>NoError</ResponseCode>
            <People>
                <Persona xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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

#### <a name="addentityfeedback-request"></a><span data-ttu-id="e99c5-203">AddEntityFeedback Anforderung</span><span class="sxs-lookup"><span data-stu-id="e99c5-203">AddEntityFeedback request</span></span>

```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
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
> <span data-ttu-id="e99c5-204">Antwort Transaktions-ID als die AddEntityFeedback Anforderungstransaktion mit FindPeople-ID.</span><span class="sxs-lookup"><span data-stu-id="e99c5-204">Using FindPeople response transaction ID as the AddEntityFeedback request transaction ID.</span></span> 
  
#### <a name="addentityfeedback-response"></a><span data-ttu-id="e99c5-205">AddEntityFeedback Antwort</span><span class="sxs-lookup"><span data-stu-id="e99c5-205">AddEntityFeedback response</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
    <s:Header>
        <h:ServerVersionInfo MajorVersion="15" MinorVersion="1" MajorBuildNumber="302" MinorBuildNumber="0" Version="V2_68" xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
    </s:Header>
    <s:Body>
        <AddEntityFeedbackResponse ResponseClass="Success" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
            <ResponseCode>NoError</ResponseCode>
            <ErrorCount>0</ErrorCount>
            <ErrorDetails />
        </AddEntityFeedbackResponse>
    </s:Body>
</s:Envelope>

```


