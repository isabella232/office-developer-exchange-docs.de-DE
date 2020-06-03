---
title: GetNonIndexableItemStatistics-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ed077877-9d98-4434-b8b6-a4a905e7f7a6
description: Hier finden Sie Informationen zum GetNonIndexableItemStatistics-EWS-Vorgang.
ms.openlocfilehash: c7d49f9e0d7b4191c7403cb4d1a20e70a96c3882
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44452818"
---
# <a name="getnonindexableitemstatistics-operation"></a><span data-ttu-id="57266-103">GetNonIndexableItemStatistics-Vorgang</span><span class="sxs-lookup"><span data-stu-id="57266-103">GetNonIndexableItemStatistics operation</span></span>

<span data-ttu-id="57266-104">Hier finden Sie Informationen zum **GetNonIndexableItemStatistics** -EWS-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="57266-104">Find information about the **GetNonIndexableItemStatistics** EWS operation.</span></span> 
  
<span data-ttu-id="57266-105">Der **GetNonIndexableItemStatistics** -Vorgang ruft die Anzahl der Elemente ab, die nicht in einem Postfach indiziert werden können.</span><span class="sxs-lookup"><span data-stu-id="57266-105">The **GetNonIndexableItemStatistics** operation retrieves the count of items that cannot be indexed in a mailbox.</span></span> 
  
<span data-ttu-id="57266-106">Dieser Vorgang wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="57266-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getnonindexableitemstatistics-operation"></a><span data-ttu-id="57266-107">Verwenden des GetNonIndexableItemStatistics-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="57266-107">Using the GetNonIndexableItemStatistics operation</span></span>

<span data-ttu-id="57266-108">Der **GetNonIndexableItemStatistics** -Vorgang zählt Postfachelemente, die nicht indiziert werden können.</span><span class="sxs-lookup"><span data-stu-id="57266-108">The **GetNonIndexableItemStatistics** operation counts mailbox items that cannot be indexed.</span></span> <span data-ttu-id="57266-109">Elemente, die nicht indiziert werden können, werden während einer Discovery-Suche nicht durchsucht.</span><span class="sxs-lookup"><span data-stu-id="57266-109">Items that cannot be indexed are not searched during a discovery search.</span></span> 
  
### <a name="getnonindexableitemstatistics-operation-soap-headers"></a><span data-ttu-id="57266-110">SOAP-Header des GetNonIndexableItemStatistics-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="57266-110">GetNonIndexableItemStatistics operation SOAP headers</span></span>

<span data-ttu-id="57266-111">Der **GetNonIndexableItemStatistics** -Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="57266-111">The **GetNonIndexableItemStatistics** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="57266-112">**Headername**</span><span class="sxs-lookup"><span data-stu-id="57266-112">**Header name**</span></span>|<span data-ttu-id="57266-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="57266-113">**Element**</span></span>|<span data-ttu-id="57266-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="57266-114">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="57266-115">**ManagementRole**</span><span class="sxs-lookup"><span data-stu-id="57266-115">**ManagementRole**</span></span> <br/> |[<span data-ttu-id="57266-116">ManagementRole</span><span class="sxs-lookup"><span data-stu-id="57266-116">ManagementRole</span></span>](managementrole.md) <br/> |<span data-ttu-id="57266-117">Gibt die Serverrollen an, die erforderlich sind, damit der Anrufer die Anforderung stellen muss.</span><span class="sxs-lookup"><span data-stu-id="57266-117">Identifies the server roles that are necessary in order for the caller to make the request.</span></span> <span data-ttu-id="57266-118">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="57266-118">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="57266-119">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="57266-119">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="57266-120">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="57266-120">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="57266-121">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="57266-121">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="57266-122">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="57266-122">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="57266-123">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="57266-123">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="57266-124">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="57266-124">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="57266-125">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="57266-125">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="57266-126">Diese Kopfzeile gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="57266-126">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getnonindexableitemstatistics-operation-request-example-get-the-count-of-items-that-cannot-be-indexed-in-a-mailbox"></a><span data-ttu-id="57266-127">GetNonIndexableItemStatistics-Vorgangs Anforderungs Beispiel: Abrufen der Anzahl von Elementen, die nicht in einem Postfach indiziert werden können</span><span class="sxs-lookup"><span data-stu-id="57266-127">GetNonIndexableItemStatistics operation request example: Get the count of items that cannot be indexed in a mailbox</span></span>

<span data-ttu-id="57266-128">Im folgenden Beispiel einer **GetNonIndexableItemStatistics** -Vorgangsanforderung wird veranschaulicht, wie die Anzahl der Elemente angefordert wird, die nicht in einem Postfach indiziert werden können.</span><span class="sxs-lookup"><span data-stu-id="57266-128">The following example of a **GetNonIndexableItemStatistics** operation request shows how to request the count of items that cannot be indexed in a mailbox.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="57266-129">Alle Legacy Domänennamen in diesem Beispiel sind verkürzt worden, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="57266-129">All legacy domain names in this example have be shortened to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
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

<span data-ttu-id="57266-130">Der SOAP-Anforderungstext Körper enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="57266-130">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="57266-131">GetNonIndexableItemStatistics</span><span class="sxs-lookup"><span data-stu-id="57266-131">GetNonIndexableItemStatistics</span></span>](getnonindexableitemstatistics.md)
    
- [<span data-ttu-id="57266-132">Postfächer (NonEmptyArrayOfLegacyDNsType)</span><span class="sxs-lookup"><span data-stu-id="57266-132">Mailboxes (NonEmptyArrayOfLegacyDNsType)</span></span>](mailboxes-nonemptyarrayoflegacydnstype.md)
    
- [<span data-ttu-id="57266-133">LegacyDN</span><span class="sxs-lookup"><span data-stu-id="57266-133">LegacyDN</span></span>](legacydn.md)
    
- [<span data-ttu-id="57266-134">SearchArchiveOnly</span><span class="sxs-lookup"><span data-stu-id="57266-134">SearchArchiveOnly</span></span>](searcharchiveonly.md)
    
## <a name="successful-getnonindexableitemstatistics-operation-response"></a><span data-ttu-id="57266-135">Erfolgreiche Reaktion des GetNonIndexableItemStatistics-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="57266-135">Successful GetNonIndexableItemStatistics operation response</span></span>

<span data-ttu-id="57266-136">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **GetNonIndexableItemStatistics** -Vorgangsanforderung zum Abrufen der Anzahl von Elementen, die nicht in einem Postfach indiziert werden können.</span><span class="sxs-lookup"><span data-stu-id="57266-136">The following example shows a successful response to a **GetNonIndexableItemStatistics** operation request to get the count of items that cannot be indexed in a mailbox.</span></span> 
  
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
      <GetNonIndexableItemStatisticsResponse ResponseClass="Success" 
                                             xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <NonIndexableItemStatistics>
            <NonIndexableItemStatistic xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               <Mailbox>/o=First Organization/ou=Exchange Administrative Group (FYT)/cn=Recipients/cn=35181acf-Steve</Mailbox>
               <ItemCount>2</ItemCount>
            </NonIndexableItemStatistic>
         </NonIndexableItemStatistics>
      </GetNonIndexableItemStatisticsResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="57266-137">Der SOAP-Antworttext Körper enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="57266-137">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="57266-138">GetNonIndexableItemStatisticsResponse</span><span class="sxs-lookup"><span data-stu-id="57266-138">GetNonIndexableItemStatisticsResponse</span></span>](getnonindexableitemstatisticsresponse.md)
    
- [<span data-ttu-id="57266-139">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="57266-139">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="57266-140">NonIndexableItemStatistics</span><span class="sxs-lookup"><span data-stu-id="57266-140">NonIndexableItemStatistics</span></span>](nonindexableitemstatistics.md)
    
- [<span data-ttu-id="57266-141">NonIndexableItemStatistic</span><span class="sxs-lookup"><span data-stu-id="57266-141">NonIndexableItemStatistic</span></span>](nonindexableitemstatistic.md)
    
- [<span data-ttu-id="57266-142">Postfach (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="57266-142">Mailbox (string)</span></span>](mailbox-string.md)
    
- [<span data-ttu-id="57266-143">ItemCount</span><span class="sxs-lookup"><span data-stu-id="57266-143">ItemCount</span></span>](itemcount.md)
    
## <a name="getnonindexableitemstatistics-operation-error-response"></a><span data-ttu-id="57266-144">Fehlerantwort des GetNonIndexableItemStatistics-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="57266-144">GetNonIndexableItemStatistics operation error response</span></span>

<span data-ttu-id="57266-145">Das folgende Beispiel zeigt eine Fehlerantwort auf eine **GetNonIndexableItemStatistics** -Vorgangsanforderung.</span><span class="sxs-lookup"><span data-stu-id="57266-145">The following example shows an error response to a **GetNonIndexableItemStatistics** operation request.</span></span> <span data-ttu-id="57266-146">Dies ist eine Antwort auf eine Anforderung zum Abrufen der Anzahl von Elementen, die nicht aus mehr als einem Postfach indiziert werden können.</span><span class="sxs-lookup"><span data-stu-id="57266-146">This is a response to a request to get the count of items that cannot be indexed from more than one mailbox.</span></span> 
  
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
      <GetNonIndexableItemStatisticsResponse ResponseClass="Error" 
                                             xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>Multiple mailboxes is currently not supported, only single mailbox is supported.</MessageText>
         <ResponseCode>ErrorInvalidArgument</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </GetNonIndexableItemStatisticsResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="57266-147">Der SOAP-Textkörper der Fehlerantwort enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="57266-147">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="57266-148">GetNonIndexableItemStatisticsResponse</span><span class="sxs-lookup"><span data-stu-id="57266-148">GetNonIndexableItemStatisticsResponse</span></span>](getnonindexableitemstatisticsresponse.md)
    
- [<span data-ttu-id="57266-149">MessageText</span><span class="sxs-lookup"><span data-stu-id="57266-149">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="57266-150">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="57266-150">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="57266-151">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="57266-151">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="57266-152">Weitere Fehlercodes, die für EWS allgemein und spezifisch für diesen Vorgang sind, finden Sie unter [Response Code](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="57266-152">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="57266-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="57266-153">See also</span></span>

- [<span data-ttu-id="57266-154">EWS-Operationen in Exchange</span><span class="sxs-lookup"><span data-stu-id="57266-154">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="57266-155">GetSearchableMailboxes-Vorgang</span><span class="sxs-lookup"><span data-stu-id="57266-155">GetSearchableMailboxes operation</span></span>](getsearchablemailboxes-operation.md)
    
- [<span data-ttu-id="57266-156">SearchMailboxes-Vorgang</span><span class="sxs-lookup"><span data-stu-id="57266-156">SearchMailboxes operation</span></span>](searchmailboxes-operation.md)
    
- [<span data-ttu-id="57266-157">GetHoldOnMailboxes-Vorgang</span><span class="sxs-lookup"><span data-stu-id="57266-157">GetHoldOnMailboxes operation</span></span>](getholdonmailboxes-operation.md)
    
- [<span data-ttu-id="57266-158">SetHoldOnMailboxes-Vorgang</span><span class="sxs-lookup"><span data-stu-id="57266-158">SetHoldOnMailboxes operation</span></span>](setholdonmailboxes-operation.md)
    
- [<span data-ttu-id="57266-159">GetDiscoverySearchConfiguration-Vorgang</span><span class="sxs-lookup"><span data-stu-id="57266-159">GetDiscoverySearchConfiguration operation</span></span>](getdiscoverysearchconfiguration-operation.md)
    
- [<span data-ttu-id="57266-160">GetNonIndexableItemDetails-Vorgang</span><span class="sxs-lookup"><span data-stu-id="57266-160">GetNonIndexableItemDetails operation</span></span>](getnonindexableitemdetails-operation.md)
    

