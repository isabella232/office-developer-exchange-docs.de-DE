---
title: GetNonIndexableItemDetails-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9279c3ad-f7c8-4bbc-b0a7-2c78416cb39a
description: Hier finden Sie Informationen über die GetNonIndexableItemDetails EWS Vorgang.
ms.openlocfilehash: 6b0c5afd54ac98f89bc6c5199300c20862c6f207
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758741"
---
# <a name="getnonindexableitemdetails-operation"></a><span data-ttu-id="d6bab-103">GetNonIndexableItemDetails-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d6bab-103">GetNonIndexableItemDetails operation</span></span>

<span data-ttu-id="d6bab-104">Hier finden Sie Informationen zum **GetNonIndexableItemDetails** EWS-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="d6bab-104">Find information about the **GetNonIndexableItemDetails** EWS operation.</span></span> 
  
<span data-ttu-id="d6bab-105">Der Vorgang **GetNonIndexableItemDetails** ruft Details zu den Elementen, die nicht indiziert werden können.</span><span class="sxs-lookup"><span data-stu-id="d6bab-105">The **GetNonIndexableItemDetails** operation retrieves details about items that cannot be indexed.</span></span> <span data-ttu-id="d6bab-106">Dies umfasst, jedoch ist nicht beschränkt auf, die Element-ID, ein Fehlercode, eine fehlerbeschreibung, wenn versucht wurde, das Element und zusätzliche Informationen zur Datei zu indizieren.</span><span class="sxs-lookup"><span data-stu-id="d6bab-106">This includes, but is not limited to, the item identifier, an error code, an error description, when an attempt was made to index the item, and additional information about the file.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d6bab-107">Obwohl das Schema gibt an, dass mehrere Postfächer kann, in der ursprünglich freigegebenen Version von Exchange 2013 durchsucht werden, unterstützt der Dienst nur erste Elementdetails für Nonindexable Elemente in ein einzelnes Postfach.</span><span class="sxs-lookup"><span data-stu-id="d6bab-107">Although the schema indicates that more than one mailbox can be searched, in the initial release version of Exchange 2013, the service only supports getting item details for nonindexable items in a single mailbox.</span></span> 
  
<span data-ttu-id="d6bab-108">Dieser Vorgang wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d6bab-108">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getnonindexableitemdetails-operation"></a><span data-ttu-id="d6bab-109">Verwenden des GetNonIndexableItemDetails-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="d6bab-109">Using the GetNonIndexableItemDetails operation</span></span>

<span data-ttu-id="d6bab-110">Der Vorgang **GetNonIndexableItemDetails** identifiziert Postfachelemente, die nicht indiziert werden können und enthält Informationen, warum die Elemente nicht indiziert werden kann.</span><span class="sxs-lookup"><span data-stu-id="d6bab-110">The **GetNonIndexableItemDetails** operation identifies mailbox items that cannot be indexed and provides information about why the items cannot be indexed.</span></span> <span data-ttu-id="d6bab-111">Elemente, die nicht indiziert werden können, werden während eines Suchvorgangs Discovery nicht durchsucht.</span><span class="sxs-lookup"><span data-stu-id="d6bab-111">Items that cannot be indexed are not searched during a discovery search.</span></span> 
  
### <a name="getnonindexableitemdetails-operation-soap-headers"></a><span data-ttu-id="d6bab-112">GetNonIndexableItemDetails Vorgang SOAP-Header</span><span class="sxs-lookup"><span data-stu-id="d6bab-112">GetNonIndexableItemDetails operation SOAP headers</span></span>

<span data-ttu-id="d6bab-113">Der Vorgang **GetNonIndexableItemDetails** können die SOAP-Header, die in der folgenden Tabelle aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="d6bab-113">The **GetNonIndexableItemDetails** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="d6bab-114">**Headername**</span><span class="sxs-lookup"><span data-stu-id="d6bab-114">**Header name**</span></span>|<span data-ttu-id="d6bab-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="d6bab-115">**Element**</span></span>|<span data-ttu-id="d6bab-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d6bab-116">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d6bab-117">**ManagementRole**</span><span class="sxs-lookup"><span data-stu-id="d6bab-117">**ManagementRole**</span></span> <br/> |[<span data-ttu-id="d6bab-118">ManagementRole</span><span class="sxs-lookup"><span data-stu-id="d6bab-118">ManagementRole</span></span>](managementrole.md) <br/> |<span data-ttu-id="d6bab-119">Identifiziert die Serverrollen, die in der Reihenfolge für den Anrufer an die Anforderung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="d6bab-119">Identifies the server roles that are necessary in order for the caller to make the request.</span></span> <span data-ttu-id="d6bab-120">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="d6bab-120">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="d6bab-121">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="d6bab-121">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="d6bab-122">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="d6bab-122">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="d6bab-123">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="d6bab-123">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="d6bab-124">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="d6bab-124">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="d6bab-125">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="d6bab-125">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="d6bab-126">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="d6bab-126">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="d6bab-127">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="d6bab-127">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="d6bab-128">Diese Kopfzeile gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="d6bab-128">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getnonindexableitemdetails-operation-request-example-get-the-details-of-an-item-that-cannot-be-indexed"></a><span data-ttu-id="d6bab-129">GetNonIndexableItemDetails Vorgang-anforderungsbeispiel: Abrufen der Details eines Elements, die nicht indiziert werden kann</span><span class="sxs-lookup"><span data-stu-id="d6bab-129">GetNonIndexableItemDetails operation request example: Get the details of an item that cannot be indexed</span></span>

<span data-ttu-id="d6bab-130">Im folgenden Beispiel wird eine **GetNonIndexableItemDetails** Vorgang Anforderung veranschaulicht, wie die Details für Elemente anfordern, die für ein einzelnes Postfach nicht indiziert werden kann.</span><span class="sxs-lookup"><span data-stu-id="d6bab-130">The following example of a **GetNonIndexableItemDetails** operation request shows how to request the details for items that cannot be indexed for a single mailbox.</span></span> <span data-ttu-id="d6bab-131">Die Suche erfolgt über Primär- und Postfächer zu archivieren.</span><span class="sxs-lookup"><span data-stu-id="d6bab-131">The search is performed across both primary and archive mailboxes.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d6bab-132">Alle legacy Domänennamen in diesem Beispiel werden gekürzt, um den Erhaltung der Lesbarkeit.</span><span class="sxs-lookup"><span data-stu-id="d6bab-132">All legacy domain names in this example have be shortened to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
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

<span data-ttu-id="d6bab-133">Die Anforderung SOAP-Text enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="d6bab-133">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="d6bab-134">GetNonIndexableItemDetails</span><span class="sxs-lookup"><span data-stu-id="d6bab-134">GetNonIndexableItemDetails</span></span>](getnonindexableitemdetails.md)
    
- [<span data-ttu-id="d6bab-135">Postfächer (NonEmptyArrayOfLegacyDNsType)</span><span class="sxs-lookup"><span data-stu-id="d6bab-135">Mailboxes (NonEmptyArrayOfLegacyDNsType)</span></span>](mailboxes-nonemptyarrayoflegacydnstype.md)
    
- [<span data-ttu-id="d6bab-136">LegacyDN</span><span class="sxs-lookup"><span data-stu-id="d6bab-136">LegacyDN</span></span>](legacydn.md)
    
- [<span data-ttu-id="d6bab-137">SearchArchiveOnly</span><span class="sxs-lookup"><span data-stu-id="d6bab-137">SearchArchiveOnly</span></span>](searcharchiveonly.md)
    
## <a name="successful-getnonindexableitemdetails-operation-response"></a><span data-ttu-id="d6bab-138">Erfolgreiche GetNonIndexableItemDetails Vorgangsantwort</span><span class="sxs-lookup"><span data-stu-id="d6bab-138">Successful GetNonIndexableItemDetails operation response</span></span>

<span data-ttu-id="d6bab-139">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine Anforderung des **GetNonIndexableItemDetails** -Vorgang zum Abrufen von Elementen, die nicht indiziert werden für ein einzelnes Postfach.</span><span class="sxs-lookup"><span data-stu-id="d6bab-139">The following example shows a successful response to a **GetNonIndexableItemDetails** operation request to get items that cannot be indexed for a single mailbox.</span></span> <span data-ttu-id="d6bab-140">Das Element in diesem Beispiel wird die nicht indiziert werden ist die binaryfile.abc-Datei, die ein unbekanntes Format ist.</span><span class="sxs-lookup"><span data-stu-id="d6bab-140">The item in this example that cannot be indexed is the binaryfile.abc file, which is of an unknown format.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="526" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetNonIndexableItemDetailsResponse ResponseClass="Success" 
                                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <NonIndexableItemDetailsResult>
            <Items xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="d6bab-141">Die Antwort SOAP-Text enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="d6bab-141">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="d6bab-142">GetNonIndexableItemDetailsResponse</span><span class="sxs-lookup"><span data-stu-id="d6bab-142">GetNonIndexableItemDetailsResponse</span></span>](getnonindexableitemdetailsresponse.md)
    
- [<span data-ttu-id="d6bab-143">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="d6bab-143">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="d6bab-144">NonIndexableItemDetailsResult</span><span class="sxs-lookup"><span data-stu-id="d6bab-144">NonIndexableItemDetailsResult</span></span>](nonindexableitemdetailsresult.md)
    
- [<span data-ttu-id="d6bab-145">NonIndexableItemDetail</span><span class="sxs-lookup"><span data-stu-id="d6bab-145">NonIndexableItemDetail</span></span>](nonindexableitemdetail.md)
    
- [<span data-ttu-id="d6bab-146">ItemId</span><span class="sxs-lookup"><span data-stu-id="d6bab-146">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="d6bab-147">ErrorCode (ItemIndexErrorType)</span><span class="sxs-lookup"><span data-stu-id="d6bab-147">ErrorCode (ItemIndexErrorType)</span></span>](errorcode-itemindexerrortype.md)
    
- [<span data-ttu-id="d6bab-148">ErrorDescription</span><span class="sxs-lookup"><span data-stu-id="d6bab-148">ErrorDescription</span></span>](errordescription.md)
    
- [<span data-ttu-id="d6bab-149">IsPartiallyIndexed</span><span class="sxs-lookup"><span data-stu-id="d6bab-149">IsPartiallyIndexed</span></span>](ispartiallyindexed.md)
    
- [<span data-ttu-id="d6bab-150">IsPermanentFailure</span><span class="sxs-lookup"><span data-stu-id="d6bab-150">IsPermanentFailure</span></span>](ispermanentfailure.md)
    
- [<span data-ttu-id="d6bab-151">SortValue</span><span class="sxs-lookup"><span data-stu-id="d6bab-151">SortValue</span></span>](sortvalue.md)
    
- [<span data-ttu-id="d6bab-152">AttemptCount</span><span class="sxs-lookup"><span data-stu-id="d6bab-152">AttemptCount</span></span>](attemptcount.md)
    
- [<span data-ttu-id="d6bab-153">LastAttemptTime</span><span class="sxs-lookup"><span data-stu-id="d6bab-153">LastAttemptTime</span></span>](lastattempttime.md)
    
- [<span data-ttu-id="d6bab-154">AdditionalInfo</span><span class="sxs-lookup"><span data-stu-id="d6bab-154">AdditionalInfo</span></span>](additionalinfo.md)
    
## <a name="getnonindexableitemdetails-operation-error-response"></a><span data-ttu-id="d6bab-155">GetNonIndexableItemDetails Vorgang Fehlerantwort</span><span class="sxs-lookup"><span data-stu-id="d6bab-155">GetNonIndexableItemDetails operation error response</span></span>

<span data-ttu-id="d6bab-156">Das folgende Beispiel zeigt eine Fehlerantwort an eine **GetNonIndexableItemDetails** Vorgang Anforderung.</span><span class="sxs-lookup"><span data-stu-id="d6bab-156">The following example shows an error response to a **GetNonIndexableItemDetails** operation request.</span></span> <span data-ttu-id="d6bab-157">Dies ist eine Antwort auf eine Anforderung zum Abrufen von Elementdetails für Elemente, die von mehr als einem Postfach nicht indiziert werden kann.</span><span class="sxs-lookup"><span data-stu-id="d6bab-157">This is a response to a request to get item details for items that cannot be indexed from more than one mailbox.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="526" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetNonIndexableItemDetailsResponse ResponseClass="Error" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>Multiple mailboxes is currently not supported, only single mailbox is supported.</MessageText>
         <ResponseCode>ErrorInvalidArgument</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </GetNonIndexableItemDetailsResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="d6bab-158">Die SOAP-Body-Fehlerantwort enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="d6bab-158">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="d6bab-159">GetNonIndexableItemDetailsResponse</span><span class="sxs-lookup"><span data-stu-id="d6bab-159">GetNonIndexableItemDetailsResponse</span></span>](getnonindexableitemdetailsresponse.md)
    
- [<span data-ttu-id="d6bab-160">MessageText</span><span class="sxs-lookup"><span data-stu-id="d6bab-160">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="d6bab-161">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="d6bab-161">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="d6bab-162">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="d6bab-162">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="d6bab-163">Zusätzliche Fehlercodes, die für EWS generisch und für diese Operation spezifisch sind, finden Sie unter [ResponseCode](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="d6bab-163">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d6bab-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d6bab-164">See also</span></span>

- [<span data-ttu-id="d6bab-165">EWS-Operationen in Exchange</span><span class="sxs-lookup"><span data-stu-id="d6bab-165">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="d6bab-166">GetSearchableMailboxes-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d6bab-166">GetSearchableMailboxes operation</span></span>](getsearchablemailboxes-operation.md)
    
- [<span data-ttu-id="d6bab-167">SearchMailboxes-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d6bab-167">SearchMailboxes operation</span></span>](searchmailboxes-operation.md)
    
- [<span data-ttu-id="d6bab-168">GetHoldOnMailboxes-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d6bab-168">GetHoldOnMailboxes operation</span></span>](getholdonmailboxes-operation.md)
    
- [<span data-ttu-id="d6bab-169">SetHoldOnMailboxes-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d6bab-169">SetHoldOnMailboxes operation</span></span>](setholdonmailboxes-operation.md)
    
- [<span data-ttu-id="d6bab-170">GetDiscoverySearchConfiguration-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d6bab-170">GetDiscoverySearchConfiguration operation</span></span>](getdiscoverysearchconfiguration-operation.md)
    
- [<span data-ttu-id="d6bab-171">GetNonIndexableItemStatistics-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d6bab-171">GetNonIndexableItemStatistics operation</span></span>](getnonindexableitemstatistics-operation.md)
    

