---
title: GetNonIndexableItemDetails-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9279c3ad-f7c8-4bbc-b0a7-2c78416cb39a
description: Hier finden Sie Informationen zum GetNonIndexableItemDetails-EWS-Vorgang.
ms.openlocfilehash: a443e04b0622ddbaaeb1bc8c04bfd05679c6207e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530211"
---
# <a name="getnonindexableitemdetails-operation"></a><span data-ttu-id="16ca9-103">GetNonIndexableItemDetails-Vorgang</span><span class="sxs-lookup"><span data-stu-id="16ca9-103">GetNonIndexableItemDetails operation</span></span>

<span data-ttu-id="16ca9-104">Hier finden Sie Informationen zum **GetNonIndexableItemDetails** -EWS-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="16ca9-104">Find information about the **GetNonIndexableItemDetails** EWS operation.</span></span> 
  
<span data-ttu-id="16ca9-105">Der **GetNonIndexableItemDetails** -Vorgang ruft Details zu Elementen ab, die nicht indiziert werden können.</span><span class="sxs-lookup"><span data-stu-id="16ca9-105">The **GetNonIndexableItemDetails** operation retrieves details about items that cannot be indexed.</span></span> <span data-ttu-id="16ca9-106">Dies umfasst, jedoch nicht auf die Element-ID, einen Fehlercode, eine Fehlerbeschreibung, bei dem Versuch, das Element zu indizieren, sowie zusätzliche Informationen zur Datei.</span><span class="sxs-lookup"><span data-stu-id="16ca9-106">This includes, but is not limited to, the item identifier, an error code, an error description, when an attempt was made to index the item, and additional information about the file.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="16ca9-107">Obwohl das Schema angibt, dass mehr als ein Postfach durchsucht werden kann, unterstützt der Dienst in der ursprünglichen Version von Exchange 2013 nur das erhalten von Element Details für nicht indizier Bare Elemente in einem einzelnen Postfach.</span><span class="sxs-lookup"><span data-stu-id="16ca9-107">Although the schema indicates that more than one mailbox can be searched, in the initial release version of Exchange 2013, the service only supports getting item details for nonindexable items in a single mailbox.</span></span> 
  
<span data-ttu-id="16ca9-108">Dieser Vorgang wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="16ca9-108">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getnonindexableitemdetails-operation"></a><span data-ttu-id="16ca9-109">Verwenden des GetNonIndexableItemDetails-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="16ca9-109">Using the GetNonIndexableItemDetails operation</span></span>

<span data-ttu-id="16ca9-110">Der **GetNonIndexableItemDetails** -Vorgang identifiziert Postfachelemente, die nicht indiziert werden können, und enthält Informationen dazu, warum die Elemente nicht indiziert werden können.</span><span class="sxs-lookup"><span data-stu-id="16ca9-110">The **GetNonIndexableItemDetails** operation identifies mailbox items that cannot be indexed and provides information about why the items cannot be indexed.</span></span> <span data-ttu-id="16ca9-111">Elemente, die nicht indiziert werden können, werden während einer Discovery-Suche nicht durchsucht.</span><span class="sxs-lookup"><span data-stu-id="16ca9-111">Items that cannot be indexed are not searched during a discovery search.</span></span> 
  
### <a name="getnonindexableitemdetails-operation-soap-headers"></a><span data-ttu-id="16ca9-112">SOAP-Header des GetNonIndexableItemDetails-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="16ca9-112">GetNonIndexableItemDetails operation SOAP headers</span></span>

<span data-ttu-id="16ca9-113">Der **GetNonIndexableItemDetails** -Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="16ca9-113">The **GetNonIndexableItemDetails** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="16ca9-114">**Headername**</span><span class="sxs-lookup"><span data-stu-id="16ca9-114">**Header name**</span></span>|<span data-ttu-id="16ca9-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="16ca9-115">**Element**</span></span>|<span data-ttu-id="16ca9-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="16ca9-116">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="16ca9-117">**ManagementRole**</span><span class="sxs-lookup"><span data-stu-id="16ca9-117">**ManagementRole**</span></span> <br/> |[<span data-ttu-id="16ca9-118">ManagementRole</span><span class="sxs-lookup"><span data-stu-id="16ca9-118">ManagementRole</span></span>](managementrole.md) <br/> |<span data-ttu-id="16ca9-119">Gibt die Serverrollen an, die erforderlich sind, damit der Anrufer die Anforderung stellen muss.</span><span class="sxs-lookup"><span data-stu-id="16ca9-119">Identifies the server roles that are necessary in order for the caller to make the request.</span></span> <span data-ttu-id="16ca9-120">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="16ca9-120">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="16ca9-121">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="16ca9-121">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="16ca9-122">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="16ca9-122">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="16ca9-123">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="16ca9-123">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="16ca9-124">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="16ca9-124">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="16ca9-125">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="16ca9-125">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="16ca9-126">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="16ca9-126">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="16ca9-127">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="16ca9-127">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="16ca9-128">Diese Kopfzeile gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="16ca9-128">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getnonindexableitemdetails-operation-request-example-get-the-details-of-an-item-that-cannot-be-indexed"></a><span data-ttu-id="16ca9-129">GetNonIndexableItemDetails-Vorgangs Anforderungs Beispiel: Abrufen der Details eines Elements, das nicht indiziert werden kann</span><span class="sxs-lookup"><span data-stu-id="16ca9-129">GetNonIndexableItemDetails operation request example: Get the details of an item that cannot be indexed</span></span>

<span data-ttu-id="16ca9-130">Im folgenden Beispiel einer **GetNonIndexableItemDetails** -Vorgangsanforderung wird gezeigt, wie die Details für Elemente angefordert werden, die nicht für ein einzelnes Postfach indiziert werden können.</span><span class="sxs-lookup"><span data-stu-id="16ca9-130">The following example of a **GetNonIndexableItemDetails** operation request shows how to request the details for items that cannot be indexed for a single mailbox.</span></span> <span data-ttu-id="16ca9-131">Die Suche wird sowohl in primären als auch in archivpostfächern durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="16ca9-131">The search is performed across both primary and archive mailboxes.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="16ca9-132">Alle Legacy Domänennamen in diesem Beispiel sind verkürzt worden, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="16ca9-132">All legacy domain names in this example have be shortened to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:GetNonIndexableItemDetails>
         <m:Mailboxes>
            <t:LegacyDN>/o=First Organization/ou=Exchange Administrative Group (FYT)/cn=Recipients/cn=35-Steve</t:LegacyDN>
         </m:Mailboxes>
         <m:SearchArchiveOnly>false</m:SearchArchiveOnly>
      </m:GetNonIndexableItemDetails>
   </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="16ca9-133">Der SOAP-Anforderungstext Körper enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="16ca9-133">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="16ca9-134">GetNonIndexableItemDetails</span><span class="sxs-lookup"><span data-stu-id="16ca9-134">GetNonIndexableItemDetails</span></span>](getnonindexableitemdetails.md)
    
- [<span data-ttu-id="16ca9-135">Postfächer (NonEmptyArrayOfLegacyDNsType)</span><span class="sxs-lookup"><span data-stu-id="16ca9-135">Mailboxes (NonEmptyArrayOfLegacyDNsType)</span></span>](mailboxes-nonemptyarrayoflegacydnstype.md)
    
- [<span data-ttu-id="16ca9-136">LegacyDN</span><span class="sxs-lookup"><span data-stu-id="16ca9-136">LegacyDN</span></span>](legacydn.md)
    
- [<span data-ttu-id="16ca9-137">SearchArchiveOnly</span><span class="sxs-lookup"><span data-stu-id="16ca9-137">SearchArchiveOnly</span></span>](searcharchiveonly.md)
    
## <a name="successful-getnonindexableitemdetails-operation-response"></a><span data-ttu-id="16ca9-138">Erfolgreiche Reaktion des GetNonIndexableItemDetails-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="16ca9-138">Successful GetNonIndexableItemDetails operation response</span></span>

<span data-ttu-id="16ca9-139">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **GetNonIndexableItemDetails** -Vorgangsanforderung zum Abrufen von Elementen, die nicht für ein einzelnes Postfach indiziert werden können.</span><span class="sxs-lookup"><span data-stu-id="16ca9-139">The following example shows a successful response to a **GetNonIndexableItemDetails** operation request to get items that cannot be indexed for a single mailbox.</span></span> <span data-ttu-id="16ca9-140">Das Element in diesem Beispiel, das nicht indiziert werden kann, ist die Datei binarydatei. ABC, die ein unbekanntes Format aufweist.</span><span class="sxs-lookup"><span data-stu-id="16ca9-140">The item in this example that cannot be indexed is the binaryfile.abc file, which is of an unknown format.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="526" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetNonIndexableItemDetailsResponse ResponseClass="Success" 
                                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <NonIndexableItemDetailsResult>
            <Items xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               <NonIndexableItemDetail>
                  <ItemId Id="AQMkAGVmNDAyOQAAAY2fUAAAAA==" ChangeKey="CQAAAA=="/>
                  <ErrorCode>DocumentParserFailure</ErrorCode>
                  <ErrorDescription>The document parser encountered a processing error.</ErrorDescription>
                  <IsPartiallyIndexed>false</IsPartiallyIndexed>
                  <IsPermanentFailure>true</IsPermanentFailure>
                  <SortValue>502511175756</SortValue>
                  <AttemptCount>0</AttemptCount>
                  <LastAttemptTime>2012-11-15T01:56:11Z</LastAttemptTime>
                  <AdditionalInfo> 301002 Error parsing document 'exchange://localhost/Attachment/d987b1f4-9aa7-42b3-aa8c-9515a35dfa1a/1f3047d4-c287-41e4-910c-feb70c1a59f0/ef402830-3d33-4a0d-a4e9-d8576900060d/85b83861-0026-418f-8464-be2036696333/502511175756.0/binaryfile.abc'. Document has an undetectable format and will not be parsed.</AdditionalInfo>
               </NonIndexableItemDetail>
            </Items>
         </NonIndexableItemDetailsResult>
      </GetNonIndexableItemDetailsResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="16ca9-141">Der SOAP-Antworttext Körper enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="16ca9-141">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="16ca9-142">GetNonIndexableItemDetailsResponse</span><span class="sxs-lookup"><span data-stu-id="16ca9-142">GetNonIndexableItemDetailsResponse</span></span>](getnonindexableitemdetailsresponse.md)
    
- [<span data-ttu-id="16ca9-143">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="16ca9-143">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="16ca9-144">NonIndexableItemDetailsResult</span><span class="sxs-lookup"><span data-stu-id="16ca9-144">NonIndexableItemDetailsResult</span></span>](nonindexableitemdetailsresult.md)
    
- [<span data-ttu-id="16ca9-145">NonIndexableItemDetail</span><span class="sxs-lookup"><span data-stu-id="16ca9-145">NonIndexableItemDetail</span></span>](nonindexableitemdetail.md)
    
- [<span data-ttu-id="16ca9-146">ItemId</span><span class="sxs-lookup"><span data-stu-id="16ca9-146">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="16ca9-147">ErrorCode (ItemIndexErrorType)</span><span class="sxs-lookup"><span data-stu-id="16ca9-147">ErrorCode (ItemIndexErrorType)</span></span>](errorcode-itemindexerrortype.md)
    
- [<span data-ttu-id="16ca9-148">ErrorDescription</span><span class="sxs-lookup"><span data-stu-id="16ca9-148">ErrorDescription</span></span>](errordescription.md)
    
- [<span data-ttu-id="16ca9-149">IsPartiallyIndexed</span><span class="sxs-lookup"><span data-stu-id="16ca9-149">IsPartiallyIndexed</span></span>](ispartiallyindexed.md)
    
- [<span data-ttu-id="16ca9-150">IsPermanentFailure</span><span class="sxs-lookup"><span data-stu-id="16ca9-150">IsPermanentFailure</span></span>](ispermanentfailure.md)
    
- [<span data-ttu-id="16ca9-151">Sortvalue</span><span class="sxs-lookup"><span data-stu-id="16ca9-151">SortValue</span></span>](sortvalue.md)
    
- [<span data-ttu-id="16ca9-152">AttemptCount</span><span class="sxs-lookup"><span data-stu-id="16ca9-152">AttemptCount</span></span>](attemptcount.md)
    
- [<span data-ttu-id="16ca9-153">LastAttemptTime</span><span class="sxs-lookup"><span data-stu-id="16ca9-153">LastAttemptTime</span></span>](lastattempttime.md)
    
- [<span data-ttu-id="16ca9-154">AdditionalInfo</span><span class="sxs-lookup"><span data-stu-id="16ca9-154">AdditionalInfo</span></span>](additionalinfo.md)
    
## <a name="getnonindexableitemdetails-operation-error-response"></a><span data-ttu-id="16ca9-155">Fehlerantwort des GetNonIndexableItemDetails-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="16ca9-155">GetNonIndexableItemDetails operation error response</span></span>

<span data-ttu-id="16ca9-156">Das folgende Beispiel zeigt eine Fehlerantwort auf eine **GetNonIndexableItemDetails** -Vorgangsanforderung.</span><span class="sxs-lookup"><span data-stu-id="16ca9-156">The following example shows an error response to a **GetNonIndexableItemDetails** operation request.</span></span> <span data-ttu-id="16ca9-157">Dies ist eine Antwort auf eine Anforderung zum Abrufen von Element Details für Elemente, die nicht aus mehr als einem Postfach indiziert werden können.</span><span class="sxs-lookup"><span data-stu-id="16ca9-157">This is a response to a request to get item details for items that cannot be indexed from more than one mailbox.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="526" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetNonIndexableItemDetailsResponse ResponseClass="Error" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>Multiple mailboxes is currently not supported, only single mailbox is supported.</MessageText>
         <ResponseCode>ErrorInvalidArgument</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </GetNonIndexableItemDetailsResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="16ca9-158">Der SOAP-Textkörper der Fehlerantwort enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="16ca9-158">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="16ca9-159">GetNonIndexableItemDetailsResponse</span><span class="sxs-lookup"><span data-stu-id="16ca9-159">GetNonIndexableItemDetailsResponse</span></span>](getnonindexableitemdetailsresponse.md)
    
- [<span data-ttu-id="16ca9-160">MessageText</span><span class="sxs-lookup"><span data-stu-id="16ca9-160">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="16ca9-161">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="16ca9-161">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="16ca9-162">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="16ca9-162">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="16ca9-163">Weitere Fehlercodes, die für EWS allgemein und spezifisch für diesen Vorgang sind, finden Sie unter [Response Code](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="16ca9-163">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="16ca9-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="16ca9-164">See also</span></span>

- [<span data-ttu-id="16ca9-165">EWS-Operationen in Exchange</span><span class="sxs-lookup"><span data-stu-id="16ca9-165">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="16ca9-166">GetSearchableMailboxes-Vorgang</span><span class="sxs-lookup"><span data-stu-id="16ca9-166">GetSearchableMailboxes operation</span></span>](getsearchablemailboxes-operation.md)
    
- [<span data-ttu-id="16ca9-167">SearchMailboxes-Vorgang</span><span class="sxs-lookup"><span data-stu-id="16ca9-167">SearchMailboxes operation</span></span>](searchmailboxes-operation.md)
    
- [<span data-ttu-id="16ca9-168">GetHoldOnMailboxes-Vorgang</span><span class="sxs-lookup"><span data-stu-id="16ca9-168">GetHoldOnMailboxes operation</span></span>](getholdonmailboxes-operation.md)
    
- [<span data-ttu-id="16ca9-169">SetHoldOnMailboxes-Vorgang</span><span class="sxs-lookup"><span data-stu-id="16ca9-169">SetHoldOnMailboxes operation</span></span>](setholdonmailboxes-operation.md)
    
- [<span data-ttu-id="16ca9-170">GetDiscoverySearchConfiguration-Vorgang</span><span class="sxs-lookup"><span data-stu-id="16ca9-170">GetDiscoverySearchConfiguration operation</span></span>](getdiscoverysearchconfiguration-operation.md)
    
- [<span data-ttu-id="16ca9-171">GetNonIndexableItemStatistics-Vorgang</span><span class="sxs-lookup"><span data-stu-id="16ca9-171">GetNonIndexableItemStatistics operation</span></span>](getnonindexableitemstatistics-operation.md)
    

