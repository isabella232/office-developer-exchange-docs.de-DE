---
title: GetHoldOnMailboxes-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9157f329-80b4-4cd0-a158-378064966ae6
description: Hier finden Sie Informationen über die GetHoldOnMailboxes EWS Vorgang.
ms.openlocfilehash: 1d0bc2f9d26e11d8d2710693d67843ad2f339a5d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758690"
---
# <a name="getholdonmailboxes-operation"></a><span data-ttu-id="af5de-103">GetHoldOnMailboxes-Vorgang</span><span class="sxs-lookup"><span data-stu-id="af5de-103">GetHoldOnMailboxes operation</span></span>

<span data-ttu-id="af5de-104">Hier finden Sie Informationen zum **GetHoldOnMailboxes** EWS-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="af5de-104">Find information about the **GetHoldOnMailboxes** EWS operation.</span></span> 
  
<span data-ttu-id="af5de-105">Der Vorgang **GetHoldOnMailboxes** Ruft die Postfächer, die unter einem bestimmten Haltestatus sind, und das zugeordnete Abfrage halten.</span><span class="sxs-lookup"><span data-stu-id="af5de-105">The **GetHoldOnMailboxes** operation gets the mailboxes that are under a specific hold and the associated hold query.</span></span> 
  
<span data-ttu-id="af5de-106">Dieser Vorgang wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="af5de-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getholdonmailboxes-operation"></a><span data-ttu-id="af5de-107">Verwenden des GetHoldOnMailboxes-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="af5de-107">Using the GetHoldOnMailboxes operation</span></span>

<span data-ttu-id="af5de-108">Der Vorgang **GetHoldOnMailboxes** bietet die Clientinformationen darüber, die welche Postfächer unter einem bestimmten Haltebereich, Informationen zu der Warteschleife Abfrage jedem Haltebereich zugeordnet, sofern zutreffend und Informationen zu den Sperrstatus für jedes Postfach platziert werden.</span><span class="sxs-lookup"><span data-stu-id="af5de-108">The **GetHoldOnMailboxes** operation gives the client information about which mailboxes are placed under a specific hold, information about the hold query associated with each hold, if applicable, and information about the hold status for each mailbox.</span></span> <span data-ttu-id="af5de-109">Weitere Informationen zum Postfach enthält, einschließlich abfragebasierter Haltestatus finden Sie unter [In-Place Hold](http://technet.microsoft.com/en-us/library/ff637980%28v=exchg.150%29) auf TechNet.</span><span class="sxs-lookup"><span data-stu-id="af5de-109">For more information about mailbox holds, including query-based holds, see [In-Place Hold](http://technet.microsoft.com/en-us/library/ff637980%28v=exchg.150%29) on TechNet.</span></span> 
  
### <a name="getholdonmailboxes-operation-soap-headers"></a><span data-ttu-id="af5de-110">GetHoldOnMailboxes Vorgang SOAP-Header</span><span class="sxs-lookup"><span data-stu-id="af5de-110">GetHoldOnMailboxes operation SOAP headers</span></span>

<span data-ttu-id="af5de-111">Der Vorgang **GetHoldOnMailboxes** können die SOAP-Header, die in der folgenden Tabelle aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="af5de-111">The **GetHoldOnMailboxes** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="af5de-112">**Headername**</span><span class="sxs-lookup"><span data-stu-id="af5de-112">**Header name**</span></span>|<span data-ttu-id="af5de-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="af5de-113">**Element**</span></span>|<span data-ttu-id="af5de-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="af5de-114">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="af5de-115">**ManagementRole**</span><span class="sxs-lookup"><span data-stu-id="af5de-115">**ManagementRole**</span></span> <br/> |[<span data-ttu-id="af5de-116">ManagementRole</span><span class="sxs-lookup"><span data-stu-id="af5de-116">ManagementRole</span></span>](managementrole.md) <br/> |<span data-ttu-id="af5de-117">Identifiziert die Serverrollen, die in der Reihenfolge für den Anrufer an die Anforderung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="af5de-117">Identifies the server roles that are necessary in order for the caller to make the request.</span></span> <span data-ttu-id="af5de-118">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="af5de-118">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="af5de-119">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="af5de-119">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="af5de-120">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="af5de-120">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="af5de-121">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="af5de-121">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="af5de-122">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="af5de-122">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="af5de-123">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="af5de-123">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="af5de-124">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="af5de-124">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="af5de-125">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="af5de-125">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="af5de-126">Diese Kopfzeile gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="af5de-126">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getholdonmailboxes-operation-request-example-get-mailbox-hold-information"></a><span data-ttu-id="af5de-127">GetHoldOnMailboxes Vorgang-anforderungsbeispiel: Abrufen Postfachinformationen Haltestatus</span><span class="sxs-lookup"><span data-stu-id="af5de-127">GetHoldOnMailboxes operation request example: Get mailbox hold information</span></span>

<span data-ttu-id="af5de-128">Im folgenden Beispiel wird eine **GetHoldOnMailboxes** Vorgang Anforderung veranschaulicht, wie die Warteschleife Postfachinformationen für den Haltebereich HoldId2 Postfach abgerufen.</span><span class="sxs-lookup"><span data-stu-id="af5de-128">The following example of a **GetHoldOnMailboxes** operation request shows how to get the mailbox hold information for the HoldId2 mailbox hold.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
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

<span data-ttu-id="af5de-129">Die Anforderung SOAP-Text enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="af5de-129">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="af5de-130">GetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="af5de-130">GetHoldOnMailboxes</span></span>](getholdonmailboxes.md)
    
- [<span data-ttu-id="af5de-131">HoldId</span><span class="sxs-lookup"><span data-stu-id="af5de-131">HoldId</span></span>](holdid.md)
    
## <a name="successful-getholdonmailboxes-operation-response"></a><span data-ttu-id="af5de-132">Erfolgreiche GetHoldOnMailboxes Vorgangsantwort</span><span class="sxs-lookup"><span data-stu-id="af5de-132">Successful GetHoldOnMailboxes operation response</span></span>

<span data-ttu-id="af5de-133">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **GetHoldOnMailboxes** Operation anfordern, um das Postfach abzurufen enthalten Informationen für die HoldId2 Postfach halten.</span><span class="sxs-lookup"><span data-stu-id="af5de-133">The following example shows a successful response to a **GetHoldOnMailboxes** operation request to get the mailbox hold information for the HoldId2 mailbox hold.</span></span> 
  
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
      <GetHoldOnMailboxesResponse ResponseClass="Success" 
                                  xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <MailboxHoldResult>
            <HoldId xmlns="http://schemas.microsoft.com/exchange/services/2006/types">HoldId2</HoldId>
            <Query xmlns="http://schemas.microsoft.com/exchange/services/2006/types">test</Query>
            <MailboxHoldStatuses xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="af5de-134">Die Antwort SOAP-Text enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="af5de-134">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="af5de-135">GetHoldOnMailboxesResponse</span><span class="sxs-lookup"><span data-stu-id="af5de-135">GetHoldOnMailboxesResponse</span></span>](getholdonmailboxesresponse.md)
    
- [<span data-ttu-id="af5de-136">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="af5de-136">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="af5de-137">MailboxHoldResult</span><span class="sxs-lookup"><span data-stu-id="af5de-137">MailboxHoldResult</span></span>](mailboxholdresult.md)
    
- [<span data-ttu-id="af5de-138">HoldId</span><span class="sxs-lookup"><span data-stu-id="af5de-138">HoldId</span></span>](holdid.md)
    
- [<span data-ttu-id="af5de-139">Query</span><span class="sxs-lookup"><span data-stu-id="af5de-139">Query</span></span>](query.md)
    
- [<span data-ttu-id="af5de-140">MailboxHoldStatuses</span><span class="sxs-lookup"><span data-stu-id="af5de-140">MailboxHoldStatuses</span></span>](mailboxholdstatuses.md)
    
- [<span data-ttu-id="af5de-141">MailboxHoldStatus</span><span class="sxs-lookup"><span data-stu-id="af5de-141">MailboxHoldStatus</span></span>](mailboxholdstatus.md)
    
- [<span data-ttu-id="af5de-142">Postfach (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="af5de-142">Mailbox (string)</span></span>](mailbox-string.md)
    
- [<span data-ttu-id="af5de-143">Status (HoldStatusType)</span><span class="sxs-lookup"><span data-stu-id="af5de-143">Status (HoldStatusType)</span></span>](status-holdstatustype.md)
    
- [<span data-ttu-id="af5de-144">AdditionalInfo</span><span class="sxs-lookup"><span data-stu-id="af5de-144">AdditionalInfo</span></span>](additionalinfo.md)
    
## <a name="getholdonmailboxes-operation-error-response"></a><span data-ttu-id="af5de-145">GetHoldOnMailboxes Vorgang Fehlerantwort</span><span class="sxs-lookup"><span data-stu-id="af5de-145">GetHoldOnMailboxes operation error response</span></span>

<span data-ttu-id="af5de-146">Das folgende Beispiel zeigt eine Fehlerantwort an eine **GetHoldOnMailboxes** Vorgang Anforderung.</span><span class="sxs-lookup"><span data-stu-id="af5de-146">The following example shows an error response to a **GetHoldOnMailboxes** operation request.</span></span> <span data-ttu-id="af5de-147">Dies ist eine Antwort auf eine Anforderung an einen Haltestatus erhalten möchten, der gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="af5de-147">This is a response to a request to get a hold that has been deleted.</span></span> 
  
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
      <GetHoldOnMailboxesResponse ResponseClass="Error" 
                                  xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>The specific query-based hold is not found.</MessageText>
         <ResponseCode>ErrorMailboxHoldNotFound</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </GetHoldOnMailboxesResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="af5de-148">Die SOAP-Body-Fehlerantwort enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="af5de-148">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="af5de-149">GetHoldOnMailboxesResponse</span><span class="sxs-lookup"><span data-stu-id="af5de-149">GetHoldOnMailboxesResponse</span></span>](getholdonmailboxesresponse.md)
    
- [<span data-ttu-id="af5de-150">MessageText</span><span class="sxs-lookup"><span data-stu-id="af5de-150">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="af5de-151">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="af5de-151">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="af5de-152">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="af5de-152">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="af5de-153">Zusätzliche Fehlercodes, die für EWS generisch und für diese Operation spezifisch sind, finden Sie unter [ResponseCode](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="af5de-153">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="af5de-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="af5de-154">See also</span></span>

- [<span data-ttu-id="af5de-155">EWS-Operationen in Exchange</span><span class="sxs-lookup"><span data-stu-id="af5de-155">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="af5de-156">GetSearchableMailboxes-Vorgang</span><span class="sxs-lookup"><span data-stu-id="af5de-156">GetSearchableMailboxes operation</span></span>](getsearchablemailboxes-operation.md)
    
- [<span data-ttu-id="af5de-157">SearchMailboxes-Vorgang</span><span class="sxs-lookup"><span data-stu-id="af5de-157">SearchMailboxes operation</span></span>](searchmailboxes-operation.md)
    
- [<span data-ttu-id="af5de-158">SetHoldOnMailboxes-Vorgang</span><span class="sxs-lookup"><span data-stu-id="af5de-158">SetHoldOnMailboxes operation</span></span>](setholdonmailboxes-operation.md)
    
- [<span data-ttu-id="af5de-159">GetDiscoverySearchConfiguration-Vorgang</span><span class="sxs-lookup"><span data-stu-id="af5de-159">GetDiscoverySearchConfiguration operation</span></span>](getdiscoverysearchconfiguration-operation.md)
    
- [<span data-ttu-id="af5de-160">GetNonIndexableItemDetails-Vorgang</span><span class="sxs-lookup"><span data-stu-id="af5de-160">GetNonIndexableItemDetails operation</span></span>](getnonindexableitemdetails-operation.md)
    
- [<span data-ttu-id="af5de-161">GetNonIndexableItemStatistics-Vorgang</span><span class="sxs-lookup"><span data-stu-id="af5de-161">GetNonIndexableItemStatistics operation</span></span>](getnonindexableitemstatistics-operation.md)
    

