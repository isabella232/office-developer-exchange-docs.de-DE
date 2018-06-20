---
title: GetNonIndexableItemStatistics-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ed077877-9d98-4434-b8b6-a4a905e7f7a6
description: Hier finden Sie Informationen über die GetNonIndexableItemStatistics EWS Vorgang.
ms.openlocfilehash: 35c2d3321c6e1a3154c88307d0e875cd6997e7fb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758742"
---
# <a name="getnonindexableitemstatistics-operation"></a><span data-ttu-id="220b8-103">GetNonIndexableItemStatistics-Vorgang</span><span class="sxs-lookup"><span data-stu-id="220b8-103">GetNonIndexableItemStatistics operation</span></span>

<span data-ttu-id="220b8-104">Hier finden Sie Informationen zum **GetNonIndexableItemStatistics** EWS-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="220b8-104">Find information about the **GetNonIndexableItemStatistics** EWS operation.</span></span> 
  
<span data-ttu-id="220b8-105">Der Vorgang **GetNonIndexableItemStatistics** Ruft die Anzahl der Elemente, die in einem Postfach nicht indiziert werden kann.</span><span class="sxs-lookup"><span data-stu-id="220b8-105">The **GetNonIndexableItemStatistics** operation retrieves the count of items that cannot be indexed in a mailbox.</span></span> 
  
<span data-ttu-id="220b8-106">Dieser Vorgang wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="220b8-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getnonindexableitemstatistics-operation"></a><span data-ttu-id="220b8-107">Verwenden des GetNonIndexableItemStatistics-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="220b8-107">Using the GetNonIndexableItemStatistics operation</span></span>

<span data-ttu-id="220b8-108">Der Vorgang **GetNonIndexableItemStatistics** zählt Postfachelemente, die nicht indiziert werden können.</span><span class="sxs-lookup"><span data-stu-id="220b8-108">The **GetNonIndexableItemStatistics** operation counts mailbox items that cannot be indexed.</span></span> <span data-ttu-id="220b8-109">Elemente, die nicht indiziert werden können, werden während eines Suchvorgangs Discovery nicht durchsucht.</span><span class="sxs-lookup"><span data-stu-id="220b8-109">Items that cannot be indexed are not searched during a discovery search.</span></span> 
  
### <a name="getnonindexableitemstatistics-operation-soap-headers"></a><span data-ttu-id="220b8-110">GetNonIndexableItemStatistics Vorgang SOAP-Header</span><span class="sxs-lookup"><span data-stu-id="220b8-110">GetNonIndexableItemStatistics operation SOAP headers</span></span>

<span data-ttu-id="220b8-111">Der Vorgang **GetNonIndexableItemStatistics** können die SOAP-Header, die in der folgenden Tabelle aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="220b8-111">The **GetNonIndexableItemStatistics** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="220b8-112">**Headername**</span><span class="sxs-lookup"><span data-stu-id="220b8-112">**Header name**</span></span>|<span data-ttu-id="220b8-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="220b8-113">**Element**</span></span>|<span data-ttu-id="220b8-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="220b8-114">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="220b8-115">**ManagementRole**</span><span class="sxs-lookup"><span data-stu-id="220b8-115">**ManagementRole**</span></span> <br/> |[<span data-ttu-id="220b8-116">ManagementRole</span><span class="sxs-lookup"><span data-stu-id="220b8-116">ManagementRole</span></span>](managementrole.md) <br/> |<span data-ttu-id="220b8-117">Identifiziert die Serverrollen, die in der Reihenfolge für den Anrufer an die Anforderung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="220b8-117">Identifies the server roles that are necessary in order for the caller to make the request.</span></span> <span data-ttu-id="220b8-118">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="220b8-118">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="220b8-119">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="220b8-119">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="220b8-120">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="220b8-120">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="220b8-121">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="220b8-121">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="220b8-122">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="220b8-122">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="220b8-123">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="220b8-123">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="220b8-124">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="220b8-124">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="220b8-125">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="220b8-125">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="220b8-126">Diese Kopfzeile gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="220b8-126">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getnonindexableitemstatistics-operation-request-example-get-the-count-of-items-that-cannot-be-indexed-in-a-mailbox"></a><span data-ttu-id="220b8-127">GetNonIndexableItemStatistics Vorgang-anforderungsbeispiel: Abrufen die Anzahl der Elemente, die nicht indiziert werden in einem Postfach</span><span class="sxs-lookup"><span data-stu-id="220b8-127">GetNonIndexableItemStatistics operation request example: Get the count of items that cannot be indexed in a mailbox</span></span>

<span data-ttu-id="220b8-128">Im folgenden Beispiel wird eine **GetNonIndexableItemStatistics** Vorgang Anforderung veranschaulicht, wie So fordern Sie die Anzahl der Elemente an, die in einem Postfach nicht indiziert werden kann.</span><span class="sxs-lookup"><span data-stu-id="220b8-128">The following example of a **GetNonIndexableItemStatistics** operation request shows how to request the count of items that cannot be indexed in a mailbox.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="220b8-129">Alle legacy Domänennamen in diesem Beispiel werden gekürzt, um den Erhaltung der Lesbarkeit.</span><span class="sxs-lookup"><span data-stu-id="220b8-129">All legacy domain names in this example have be shortened to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:GetNonIndexableItemStatistics>
         <m:Mailboxes>
            <t:LegacyDN>/o=First Organization/ou=Exchange Administrative Group (FYDIDLT)/cn=Recipients/cn=3518cf-Steve</t:LegacyDN>
         </m:Mailboxes>
         <m:SearchArchiveOnly>false</m:SearchArchiveOnly>
      </m:GetNonIndexableItemStatistics>
   </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="220b8-130">Die Anforderung SOAP-Text enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="220b8-130">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="220b8-131">GetNonIndexableItemStatistics</span><span class="sxs-lookup"><span data-stu-id="220b8-131">GetNonIndexableItemStatistics</span></span>](getnonindexableitemstatistics.md)
    
- [<span data-ttu-id="220b8-132">Postfächer (NonEmptyArrayOfLegacyDNsType)</span><span class="sxs-lookup"><span data-stu-id="220b8-132">Mailboxes (NonEmptyArrayOfLegacyDNsType)</span></span>](mailboxes-nonemptyarrayoflegacydnstype.md)
    
- [<span data-ttu-id="220b8-133">LegacyDN</span><span class="sxs-lookup"><span data-stu-id="220b8-133">LegacyDN</span></span>](legacydn.md)
    
- [<span data-ttu-id="220b8-134">SearchArchiveOnly</span><span class="sxs-lookup"><span data-stu-id="220b8-134">SearchArchiveOnly</span></span>](searcharchiveonly.md)
    
## <a name="successful-getnonindexableitemstatistics-operation-response"></a><span data-ttu-id="220b8-135">Erfolgreiche GetNonIndexableItemStatistics Vorgangsantwort</span><span class="sxs-lookup"><span data-stu-id="220b8-135">Successful GetNonIndexableItemStatistics operation response</span></span>

<span data-ttu-id="220b8-136">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine Anforderung des **GetNonIndexableItemStatistics** -Vorgang zum Abrufen der Anzahl der Elemente, die nicht indiziert werden in einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="220b8-136">The following example shows a successful response to a **GetNonIndexableItemStatistics** operation request to get the count of items that cannot be indexed in a mailbox.</span></span> 
  
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
      <GetNonIndexableItemStatisticsResponse ResponseClass="Success" 
                                             xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <NonIndexableItemStatistics>
            <NonIndexableItemStatistic xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
               <Mailbox>/o=First Organization/ou=Exchange Administrative Group (FYT)/cn=Recipients/cn=35181acf-Steve</Mailbox>
               <ItemCount>2</ItemCount>
            </NonIndexableItemStatistic>
         </NonIndexableItemStatistics>
      </GetNonIndexableItemStatisticsResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="220b8-137">Die Antwort SOAP-Text enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="220b8-137">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="220b8-138">GetNonIndexableItemStatisticsResponse</span><span class="sxs-lookup"><span data-stu-id="220b8-138">GetNonIndexableItemStatisticsResponse</span></span>](getnonindexableitemstatisticsresponse.md)
    
- [<span data-ttu-id="220b8-139">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="220b8-139">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="220b8-140">NonIndexableItemStatistics</span><span class="sxs-lookup"><span data-stu-id="220b8-140">NonIndexableItemStatistics</span></span>](nonindexableitemstatistics.md)
    
- [<span data-ttu-id="220b8-141">NonIndexableItemStatistic</span><span class="sxs-lookup"><span data-stu-id="220b8-141">NonIndexableItemStatistic</span></span>](nonindexableitemstatistic.md)
    
- [<span data-ttu-id="220b8-142">Postfach (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="220b8-142">Mailbox (string)</span></span>](mailbox-string.md)
    
- [<span data-ttu-id="220b8-143">ItemCount</span><span class="sxs-lookup"><span data-stu-id="220b8-143">ItemCount</span></span>](itemcount.md)
    
## <a name="getnonindexableitemstatistics-operation-error-response"></a><span data-ttu-id="220b8-144">GetNonIndexableItemStatistics Vorgang Fehlerantwort</span><span class="sxs-lookup"><span data-stu-id="220b8-144">GetNonIndexableItemStatistics operation error response</span></span>

<span data-ttu-id="220b8-145">Das folgende Beispiel zeigt eine Fehlerantwort an eine **GetNonIndexableItemStatistics** Vorgang Anforderung.</span><span class="sxs-lookup"><span data-stu-id="220b8-145">The following example shows an error response to a **GetNonIndexableItemStatistics** operation request.</span></span> <span data-ttu-id="220b8-146">Dies ist eine Antwort auf eine Anforderung an die Anzahl von Elementen abzurufen, die von mehr als einem Postfach nicht indiziert werden kann.</span><span class="sxs-lookup"><span data-stu-id="220b8-146">This is a response to a request to get the count of items that cannot be indexed from more than one mailbox.</span></span> 
  
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
      <GetNonIndexableItemStatisticsResponse ResponseClass="Error" 
                                             xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>Multiple mailboxes is currently not supported, only single mailbox is supported.</MessageText>
         <ResponseCode>ErrorInvalidArgument</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </GetNonIndexableItemStatisticsResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="220b8-147">Die SOAP-Body-Fehlerantwort enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="220b8-147">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="220b8-148">GetNonIndexableItemStatisticsResponse</span><span class="sxs-lookup"><span data-stu-id="220b8-148">GetNonIndexableItemStatisticsResponse</span></span>](getnonindexableitemstatisticsresponse.md)
    
- [<span data-ttu-id="220b8-149">MessageText</span><span class="sxs-lookup"><span data-stu-id="220b8-149">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="220b8-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="220b8-150">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="220b8-151">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="220b8-151">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="220b8-152">Zusätzliche Fehlercodes, die für EWS generisch und für diese Operation spezifisch sind, finden Sie unter [ResponseCode](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="220b8-152">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="220b8-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="220b8-153">See also</span></span>

- [<span data-ttu-id="220b8-154">EWS-Operationen in Exchange</span><span class="sxs-lookup"><span data-stu-id="220b8-154">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="220b8-155">GetSearchableMailboxes-Vorgang</span><span class="sxs-lookup"><span data-stu-id="220b8-155">GetSearchableMailboxes operation</span></span>](getsearchablemailboxes-operation.md)
    
- [<span data-ttu-id="220b8-156">SearchMailboxes-Vorgang</span><span class="sxs-lookup"><span data-stu-id="220b8-156">SearchMailboxes operation</span></span>](searchmailboxes-operation.md)
    
- [<span data-ttu-id="220b8-157">GetHoldOnMailboxes-Vorgang</span><span class="sxs-lookup"><span data-stu-id="220b8-157">GetHoldOnMailboxes operation</span></span>](getholdonmailboxes-operation.md)
    
- [<span data-ttu-id="220b8-158">SetHoldOnMailboxes-Vorgang</span><span class="sxs-lookup"><span data-stu-id="220b8-158">SetHoldOnMailboxes operation</span></span>](setholdonmailboxes-operation.md)
    
- [<span data-ttu-id="220b8-159">GetDiscoverySearchConfiguration-Vorgang</span><span class="sxs-lookup"><span data-stu-id="220b8-159">GetDiscoverySearchConfiguration operation</span></span>](getdiscoverysearchconfiguration-operation.md)
    
- [<span data-ttu-id="220b8-160">GetNonIndexableItemDetails-Vorgang</span><span class="sxs-lookup"><span data-stu-id="220b8-160">GetNonIndexableItemDetails operation</span></span>](getnonindexableitemdetails-operation.md)
    

