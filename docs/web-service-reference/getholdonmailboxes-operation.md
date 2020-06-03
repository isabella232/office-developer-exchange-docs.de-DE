---
title: GetHoldOnMailboxes-Vorgang
manager: sethgros
ms.date: 01/24/2020
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9157f329-80b4-4cd0-a158-378064966ae6
description: Hier finden Sie Informationen zum GetHoldOnMailboxes-EWS-Vorgang.
ms.openlocfilehash: 867f38be87e60af8708eeb0b9d0e3ac8eee6ff64
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457732"
---
# <a name="getholdonmailboxes-operation"></a><span data-ttu-id="03971-103">GetHoldOnMailboxes-Vorgang</span><span class="sxs-lookup"><span data-stu-id="03971-103">GetHoldOnMailboxes operation</span></span>

> [!IMPORTANT]
> <span data-ttu-id="03971-104">Ab dem 1. April 2020 ist der GetHoldOnMailboxes-Vorgang in Exchange Online nicht mehr verfügbar.</span><span class="sxs-lookup"><span data-stu-id="03971-104">Starting on April 1, 2020, the GetHoldOnMailboxes operation will no longer be available in Exchange Online.</span></span> <span data-ttu-id="03971-105">Dieser Vorgang ist in lokalen Versionen von Exchange Server nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="03971-105">This operation won't be affected in on-premises versions of Exchange Server.</span></span> <span data-ttu-id="03971-106">Weitere Informationen finden Sie unter [Retirement of Legacy eDiscovery Tools in Exchange Online](https://docs.microsoft.com/microsoft-365/compliance/legacy-ediscovery-retirement#getsearchablemailboxes-setholdonmailboxes-and-getholdonmailboxes-operations-in-the-ews-api).</span><span class="sxs-lookup"><span data-stu-id="03971-106">For more information, see [Retirement of legacy eDiscovery tools in Exchange Online](https://docs.microsoft.com/microsoft-365/compliance/legacy-ediscovery-retirement#getsearchablemailboxes-setholdonmailboxes-and-getholdonmailboxes-operations-in-the-ews-api).</span></span>

<span data-ttu-id="03971-107">Hier finden Sie Informationen zum **GetHoldOnMailboxes** -EWS-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="03971-107">Find information about the **GetHoldOnMailboxes** EWS operation.</span></span> 
  
<span data-ttu-id="03971-108">Der **GetHoldOnMailboxes** -Vorgang ruft die Postfächer, die sich unter einem bestimmten Haltebereich befinden, und die zugehörige halte Abfrage ab.</span><span class="sxs-lookup"><span data-stu-id="03971-108">The **GetHoldOnMailboxes** operation gets the mailboxes that are under a specific hold and the associated hold query.</span></span> 
  
<span data-ttu-id="03971-109">Dieser Vorgang wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="03971-109">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getholdonmailboxes-operation"></a><span data-ttu-id="03971-110">Verwenden des GetHoldOnMailboxes-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="03971-110">Using the GetHoldOnMailboxes operation</span></span>

<span data-ttu-id="03971-111">Der **GetHoldOnMailboxes** -Vorgang gibt dem Clientinformationen darüber, welche Postfächer unter einem bestimmten Haltebereich gespeichert sind, Informationen zur halte Abfrage, die jedem Haltestatus zugeordnet sind, falls zutreffend, sowie Informationen zum Aufbewahrungs Status für jedes Postfach.</span><span class="sxs-lookup"><span data-stu-id="03971-111">The **GetHoldOnMailboxes** operation gives the client information about which mailboxes are placed under a specific hold, information about the hold query associated with each hold, if applicable, and information about the hold status for each mailbox.</span></span> <span data-ttu-id="03971-112">Weitere Informationen zu Postfachspeichern, einschließlich abfragebasierter Haltestatus, finden Sie unter [in-situ-](https://technet.microsoft.com/library/ff637980%28v=exchg.150%29) Speicher auf TechNet.</span><span class="sxs-lookup"><span data-stu-id="03971-112">For more information about mailbox holds, including query-based holds, see [In-Place Hold](https://technet.microsoft.com/library/ff637980%28v=exchg.150%29) on TechNet.</span></span> 
  
### <a name="getholdonmailboxes-operation-soap-headers"></a><span data-ttu-id="03971-113">SOAP-Header des GetHoldOnMailboxes-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="03971-113">GetHoldOnMailboxes operation SOAP headers</span></span>

<span data-ttu-id="03971-114">Der **GetHoldOnMailboxes** -Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="03971-114">The **GetHoldOnMailboxes** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="03971-115">**Headername**</span><span class="sxs-lookup"><span data-stu-id="03971-115">**Header name**</span></span>|<span data-ttu-id="03971-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="03971-116">**Element**</span></span>|<span data-ttu-id="03971-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="03971-117">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="03971-118">**ManagementRole**</span><span class="sxs-lookup"><span data-stu-id="03971-118">**ManagementRole**</span></span> <br/> |[<span data-ttu-id="03971-119">ManagementRole</span><span class="sxs-lookup"><span data-stu-id="03971-119">ManagementRole</span></span>](managementrole.md) <br/> |<span data-ttu-id="03971-120">Gibt die Serverrollen an, die erforderlich sind, damit der Anrufer die Anforderung stellen muss.</span><span class="sxs-lookup"><span data-stu-id="03971-120">Identifies the server roles that are necessary in order for the caller to make the request.</span></span> <span data-ttu-id="03971-121">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="03971-121">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="03971-122">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="03971-122">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="03971-123">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="03971-123">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="03971-124">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="03971-124">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="03971-125">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="03971-125">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="03971-126">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="03971-126">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="03971-127">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="03971-127">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="03971-128">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="03971-128">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="03971-129">Diese Kopfzeile gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="03971-129">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getholdonmailboxes-operation-request-example-get-mailbox-hold-information"></a><span data-ttu-id="03971-130">GetHoldOnMailboxes-Vorgangs Anforderungs Beispiel: Abrufen von Informationen zu Postfachspeichern</span><span class="sxs-lookup"><span data-stu-id="03971-130">GetHoldOnMailboxes operation request example: Get mailbox hold information</span></span>

<span data-ttu-id="03971-131">Im folgenden Beispiel einer **GetHoldOnMailboxes** -Vorgangsanforderung wird gezeigt, wie Sie die Postfachspeicher Informationen für das HoldId2-Post Fach Postfach speichern.</span><span class="sxs-lookup"><span data-stu-id="03971-131">The following example of a **GetHoldOnMailboxes** operation request shows how to get the mailbox hold information for the HoldId2 mailbox hold.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:GetHoldOnMailboxes>
         <m:HoldId>HoldId2</m:HoldId>
      </m:GetHoldOnMailboxes>
   </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="03971-132">Der SOAP-Anforderungstext Körper enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="03971-132">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="03971-133">GetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="03971-133">GetHoldOnMailboxes</span></span>](getholdonmailboxes.md)
    
- [<span data-ttu-id="03971-134">Haltestatus</span><span class="sxs-lookup"><span data-stu-id="03971-134">HoldId</span></span>](holdid.md)
    
## <a name="successful-getholdonmailboxes-operation-response"></a><span data-ttu-id="03971-135">Erfolgreiche Reaktion des GetHoldOnMailboxes-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="03971-135">Successful GetHoldOnMailboxes operation response</span></span>

<span data-ttu-id="03971-136">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **GetHoldOnMailboxes** -Vorgangsanforderung zum Abrufen der Postfachspeicher Informationen für das HoldId2-Postfach.</span><span class="sxs-lookup"><span data-stu-id="03971-136">The following example shows a successful response to a **GetHoldOnMailboxes** operation request to get the mailbox hold information for the HoldId2 mailbox hold.</span></span> 
  
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
      <GetHoldOnMailboxesResponse ResponseClass="Success" 
                                  xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <MailboxHoldResult>
            <HoldId xmlns="https://schemas.microsoft.com/exchange/services/2006/types">HoldId2</HoldId>
            <Query xmlns="https://schemas.microsoft.com/exchange/services/2006/types">test</Query>
            <MailboxHoldStatuses xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               <MailboxHoldStatus>
                  <Mailbox>/o=First Organization/ou=Exchange Administrative Group (FYDIBPDLT)/cn=Recipients/cn=ecc0fd98c2cadf-Willi</Mailbox>
                  <Status>OnHold</Status>
                  <AdditionalInfo/>
               </MailboxHoldStatus>
               <MailboxHoldStatus>
                  <Mailbox>/o=First Organization/ou=Exchange Administrative Group (FYDIBPDLT)/cn=Recipients/cn=dasdat341q8de95-Micha</Mailbox>
                  <Status>OnHold</Status>
                  <AdditionalInfo/>
               </MailboxHoldStatus>
            </MailboxHoldStatuses>
         </MailboxHoldResult>
      </GetHoldOnMailboxesResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="03971-137">Der SOAP-Antworttext Körper enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="03971-137">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="03971-138">GetHoldOnMailboxesResponse</span><span class="sxs-lookup"><span data-stu-id="03971-138">GetHoldOnMailboxesResponse</span></span>](getholdonmailboxesresponse.md)
    
- [<span data-ttu-id="03971-139">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="03971-139">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="03971-140">MailboxHoldResult</span><span class="sxs-lookup"><span data-stu-id="03971-140">MailboxHoldResult</span></span>](mailboxholdresult.md)
    
- [<span data-ttu-id="03971-141">Haltestatus</span><span class="sxs-lookup"><span data-stu-id="03971-141">HoldId</span></span>](holdid.md)
    
- [<span data-ttu-id="03971-142">Query</span><span class="sxs-lookup"><span data-stu-id="03971-142">Query</span></span>](query.md)
    
- [<span data-ttu-id="03971-143">MailboxHoldStatuses</span><span class="sxs-lookup"><span data-stu-id="03971-143">MailboxHoldStatuses</span></span>](mailboxholdstatuses.md)
    
- [<span data-ttu-id="03971-144">MailboxHoldStatus</span><span class="sxs-lookup"><span data-stu-id="03971-144">MailboxHoldStatus</span></span>](mailboxholdstatus.md)
    
- [<span data-ttu-id="03971-145">Postfach (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="03971-145">Mailbox (string)</span></span>](mailbox-string.md)
    
- [<span data-ttu-id="03971-146">Status (HoldStatusType)</span><span class="sxs-lookup"><span data-stu-id="03971-146">Status (HoldStatusType)</span></span>](status-holdstatustype.md)
    
- [<span data-ttu-id="03971-147">AdditionalInfo</span><span class="sxs-lookup"><span data-stu-id="03971-147">AdditionalInfo</span></span>](additionalinfo.md)
    
## <a name="getholdonmailboxes-operation-error-response"></a><span data-ttu-id="03971-148">Fehlerantwort des GetHoldOnMailboxes-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="03971-148">GetHoldOnMailboxes operation error response</span></span>

<span data-ttu-id="03971-149">Das folgende Beispiel zeigt eine Fehlerantwort auf eine **GetHoldOnMailboxes** -Vorgangsanforderung.</span><span class="sxs-lookup"><span data-stu-id="03971-149">The following example shows an error response to a **GetHoldOnMailboxes** operation request.</span></span> <span data-ttu-id="03971-150">Dies ist eine Antwort auf eine Anforderung zum Abrufen eines Haltestatus, der gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="03971-150">This is a response to a request to get a hold that has been deleted.</span></span> 
  
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
      <GetHoldOnMailboxesResponse ResponseClass="Error" 
                                  xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>The specific query-based hold is not found.</MessageText>
         <ResponseCode>ErrorMailboxHoldNotFound</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </GetHoldOnMailboxesResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="03971-151">Der SOAP-Textkörper der Fehlerantwort enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="03971-151">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="03971-152">GetHoldOnMailboxesResponse</span><span class="sxs-lookup"><span data-stu-id="03971-152">GetHoldOnMailboxesResponse</span></span>](getholdonmailboxesresponse.md)
    
- [<span data-ttu-id="03971-153">MessageText</span><span class="sxs-lookup"><span data-stu-id="03971-153">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="03971-154">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="03971-154">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="03971-155">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="03971-155">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="03971-156">Weitere Fehlercodes, die für EWS allgemein und spezifisch für diesen Vorgang sind, finden Sie unter [Response Code](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="03971-156">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="03971-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="03971-157">See also</span></span>

- [<span data-ttu-id="03971-158">EWS-Operationen in Exchange</span><span class="sxs-lookup"><span data-stu-id="03971-158">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="03971-159">GetSearchableMailboxes-Vorgang</span><span class="sxs-lookup"><span data-stu-id="03971-159">GetSearchableMailboxes operation</span></span>](getsearchablemailboxes-operation.md)
    
- [<span data-ttu-id="03971-160">SearchMailboxes-Vorgang</span><span class="sxs-lookup"><span data-stu-id="03971-160">SearchMailboxes operation</span></span>](searchmailboxes-operation.md)
    
- [<span data-ttu-id="03971-161">SetHoldOnMailboxes-Vorgang</span><span class="sxs-lookup"><span data-stu-id="03971-161">SetHoldOnMailboxes operation</span></span>](setholdonmailboxes-operation.md)
    
- [<span data-ttu-id="03971-162">GetDiscoverySearchConfiguration-Vorgang</span><span class="sxs-lookup"><span data-stu-id="03971-162">GetDiscoverySearchConfiguration operation</span></span>](getdiscoverysearchconfiguration-operation.md)
    
- [<span data-ttu-id="03971-163">GetNonIndexableItemDetails-Vorgang</span><span class="sxs-lookup"><span data-stu-id="03971-163">GetNonIndexableItemDetails operation</span></span>](getnonindexableitemdetails-operation.md)
    
- [<span data-ttu-id="03971-164">GetNonIndexableItemStatistics-Vorgang</span><span class="sxs-lookup"><span data-stu-id="03971-164">GetNonIndexableItemStatistics operation</span></span>](getnonindexableitemstatistics-operation.md)
    

