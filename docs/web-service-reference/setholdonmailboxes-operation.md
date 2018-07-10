---
title: SetHoldOnMailboxes-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9015a0d8-3495-461b-aa79-797d23169585
description: Hier finden Sie Informationen über die SetHoldOnMailboxes EWS Vorgang.
ms.openlocfilehash: 1091ed14ceb25dfd275499b9db47ae4e41b5f1a0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831412"
---
# <a name="setholdonmailboxes-operation"></a><span data-ttu-id="f55e0-103">SetHoldOnMailboxes-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f55e0-103">SetHoldOnMailboxes operation</span></span>

<span data-ttu-id="f55e0-104">Hier finden Sie Informationen zum **SetHoldOnMailboxes** EWS-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="f55e0-104">Find information about the **SetHoldOnMailboxes** EWS operation.</span></span> 
  
<span data-ttu-id="f55e0-105">Der Vorgang **SetHoldOnMailboxes** festgelegt Postfächer eine Aufbewahrungsrichtlinie Postfach.</span><span class="sxs-lookup"><span data-stu-id="f55e0-105">The **SetHoldOnMailboxes** operation sets a mailbox hold policy on mailboxes.</span></span> 
  
<span data-ttu-id="f55e0-106">Dieser Vorgang wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="f55e0-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-setholdonmailboxes-operation"></a><span data-ttu-id="f55e0-107">Verwenden des SetHoldOnMailboxes-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="f55e0-107">Using the SetHoldOnMailboxes operation</span></span>

<span data-ttu-id="f55e0-108">Der Vorgang **SetHoldOnMailboxes** festgelegt Postfach die Sperrung auf ein oder mehrere Postfächer.</span><span class="sxs-lookup"><span data-stu-id="f55e0-108">The **SetHoldOnMailboxes** operation sets a mailbox hold on to one or more mailboxes.</span></span> 
  
### <a name="setholdonmailboxes-operation-soap-headers"></a><span data-ttu-id="f55e0-109">SetHoldOnMailboxes Vorgang SOAP-Header</span><span class="sxs-lookup"><span data-stu-id="f55e0-109">SetHoldOnMailboxes operation SOAP headers</span></span>

<span data-ttu-id="f55e0-110">Der Vorgang **SetHoldOnMailboxes** können die SOAP-Header, die in der folgenden Tabelle aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="f55e0-110">The **SetHoldOnMailboxes** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="f55e0-111">**Headername**</span><span class="sxs-lookup"><span data-stu-id="f55e0-111">**Header name**</span></span>|<span data-ttu-id="f55e0-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="f55e0-112">**Element**</span></span>|<span data-ttu-id="f55e0-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f55e0-113">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f55e0-114">**ManagementRole**</span><span class="sxs-lookup"><span data-stu-id="f55e0-114">**ManagementRole**</span></span> <br/> |[<span data-ttu-id="f55e0-115">ManagementRole</span><span class="sxs-lookup"><span data-stu-id="f55e0-115">ManagementRole</span></span>](managementrole.md) <br/> |<span data-ttu-id="f55e0-116">Identifiziert die Serverrollen, die in der Reihenfolge für den Anrufer an die Anforderung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="f55e0-116">Identifies the server roles that are necessary in order for the caller to make the request.</span></span> <span data-ttu-id="f55e0-117">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="f55e0-117">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="f55e0-118">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="f55e0-118">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="f55e0-119">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="f55e0-119">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="f55e0-120">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="f55e0-120">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="f55e0-121">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="f55e0-121">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="f55e0-122">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="f55e0-122">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="f55e0-123">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="f55e0-123">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="f55e0-124">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="f55e0-124">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="f55e0-125">Diese Kopfzeile gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="f55e0-125">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="setholdonmailboxes-operation-request-example-apply-a-hold-on-a-mailbox"></a><span data-ttu-id="f55e0-126">SetHoldOnMailboxes Vorgang-anforderungsbeispiel: Anwenden des Haltebereichstatus auf ein Postfach</span><span class="sxs-lookup"><span data-stu-id="f55e0-126">SetHoldOnMailboxes operation request example: Apply a hold on a mailbox</span></span>

<span data-ttu-id="f55e0-127">Im folgenden Beispiel wird eine **SetHoldOnMailboxes** Vorgang Anforderung veranschaulicht, wie einen Haltestatus auf zwei Postfächer angewendet.</span><span class="sxs-lookup"><span data-stu-id="f55e0-127">The following example of a **SetHoldOnMailboxes** operation request shows how to apply a hold on two mailboxes.</span></span> <span data-ttu-id="f55e0-128">Die Sperre Postfach wurde mithilfe des Befehls [New-MailboxSearch](http://technet.microsoft.com/de-de/library/dd298064.aspx) erstellt.</span><span class="sxs-lookup"><span data-stu-id="f55e0-128">The mailbox hold was created by using the [New-MailboxSearch](http://technet.microsoft.com/de-de/library/dd298064.aspx) command.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:SetHoldOnMailboxes>
         <m:ActionType>Create</m:ActionType>
         <m:HoldId>HoldId2</m:HoldId>
         <m:Query>test</m:Query>
         <m:Mailboxes>
            <t:String>/o=First/ou=Exchange(DLT)/cn=Recipients/cn=1fa441ff5e4749ba43ecc0fd94c21adf-Willi</t:String>
            <t:String>/o=First/ou=Exchange(DLT)/cn=Recipients/cn=aed2346adaa34ffc9f0f339917e8de95-Micha</t:String>
         </m:Mailboxes>
         <m:Language>English</m:Language>
         <m:IncludeNonIndexableItems>false</m:IncludeNonIndexableItems>
         <m:Deduplication>true</m:Deduplication>
      </m:SetHoldOnMailboxes>
   </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="f55e0-129">Die Anforderung SOAP-Text enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="f55e0-129">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="f55e0-130">SetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="f55e0-130">SetHoldOnMailboxes</span></span>](setholdonmailboxes.md)
    
- [<span data-ttu-id="f55e0-131">ActionType (HoldActionType)</span><span class="sxs-lookup"><span data-stu-id="f55e0-131">ActionType (HoldActionType)</span></span>](actiontype-holdactiontype.md)
    
- [<span data-ttu-id="f55e0-132">HoldId</span><span class="sxs-lookup"><span data-stu-id="f55e0-132">HoldId</span></span>](holdid.md)
    
- [<span data-ttu-id="f55e0-133">Query</span><span class="sxs-lookup"><span data-stu-id="f55e0-133">Query</span></span>](query.md)
    
- [<span data-ttu-id="f55e0-134">Postfächer (ArrayOfStringsType)</span><span class="sxs-lookup"><span data-stu-id="f55e0-134">Mailboxes (ArrayOfStringsType)</span></span>](mailboxes-arrayofstringstype.md)
    
- [<span data-ttu-id="f55e0-135">String</span><span class="sxs-lookup"><span data-stu-id="f55e0-135">String</span></span>](string.md)
    
- [<span data-ttu-id="f55e0-136">Language</span><span class="sxs-lookup"><span data-stu-id="f55e0-136">Language</span></span>](language.md)
    
- [<span data-ttu-id="f55e0-137">IncludeNonIndexableItems</span><span class="sxs-lookup"><span data-stu-id="f55e0-137">IncludeNonIndexableItems</span></span>](includenonindexableitems.md)
    
- [<span data-ttu-id="f55e0-138">Datendeduplizierung</span><span class="sxs-lookup"><span data-stu-id="f55e0-138">Deduplication</span></span>](deduplication.md)
    
## <a name="successful-setholdonmailboxes-operation-response"></a><span data-ttu-id="f55e0-139">Erfolgreiche SetHoldOnMailboxes Vorgangsantwort</span><span class="sxs-lookup"><span data-stu-id="f55e0-139">Successful SetHoldOnMailboxes operation response</span></span>

<span data-ttu-id="f55e0-140">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine Anforderung **SetHoldOnMailboxes** Vorgang, um zwei Postfächer zu platzieren, klicken Sie auf halten.</span><span class="sxs-lookup"><span data-stu-id="f55e0-140">The following example shows a successful response to a **SetHoldOnMailboxes** operation request to put two mailboxes on hold.</span></span> 
  
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
      <SetHoldOnMailboxesResponse ResponseClass="Success" 
                                  xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <MailboxHoldResult>
            <HoldId xmlns="http://schemas.microsoft.com/exchange/services/2006/types">HoldId2</HoldId>
            <Query xmlns="http://schemas.microsoft.com/exchange/services/2006/types">test</Query>
            <MailboxHoldStatuses xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
               <MailboxHoldStatus>
                  <Mailbox>o=First/ou=Exchange(DLT)/cn=Recipients/cn=1fa441ff5e4749ba43ecc0fd94c21adf-Willi</Mailbox>
                  <Status>Pending</Status>
                  <AdditionalInfo/>
               </MailboxHoldStatus>
               <MailboxHoldStatus>
                  <Mailbox>/o=First/ou=Exchange(DLT)/cn=Recipients/cn=aed2346adaa34ffc9f0f339917e8de95-Micha</Mailbox>
                  <Status>Pending</Status>
                  <AdditionalInfo/>
               </MailboxHoldStatus>
            </MailboxHoldStatuses>
         </MailboxHoldResult>
      </SetHoldOnMailboxesResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="f55e0-141">Die Antwort SOAP-Text enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="f55e0-141">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="f55e0-142">SetHoldOnMailboxesResponse</span><span class="sxs-lookup"><span data-stu-id="f55e0-142">SetHoldOnMailboxesResponse</span></span>](setholdonmailboxesresponse.md)
    
- [<span data-ttu-id="f55e0-143">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="f55e0-143">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="f55e0-144">MailboxHoldResult</span><span class="sxs-lookup"><span data-stu-id="f55e0-144">MailboxHoldResult</span></span>](mailboxholdresult.md)
    
- [<span data-ttu-id="f55e0-145">HoldId</span><span class="sxs-lookup"><span data-stu-id="f55e0-145">HoldId</span></span>](holdid.md)
    
- [<span data-ttu-id="f55e0-146">Query</span><span class="sxs-lookup"><span data-stu-id="f55e0-146">Query</span></span>](query.md)
    
- [<span data-ttu-id="f55e0-147">MailboxHoldStatuses</span><span class="sxs-lookup"><span data-stu-id="f55e0-147">MailboxHoldStatuses</span></span>](mailboxholdstatuses.md)
    
- [<span data-ttu-id="f55e0-148">MailboxHoldStatus</span><span class="sxs-lookup"><span data-stu-id="f55e0-148">MailboxHoldStatus</span></span>](mailboxholdstatus.md)
    
- [<span data-ttu-id="f55e0-149">Postfach (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="f55e0-149">Mailbox (string)</span></span>](mailbox-string.md)
    
- [<span data-ttu-id="f55e0-150">Status (HoldStatusType)</span><span class="sxs-lookup"><span data-stu-id="f55e0-150">Status (HoldStatusType)</span></span>](status-holdstatustype.md)
    
- [<span data-ttu-id="f55e0-151">AdditionalInfo</span><span class="sxs-lookup"><span data-stu-id="f55e0-151">AdditionalInfo</span></span>](additionalinfo.md)
    
## <a name="setholdonmailboxes-operation-error-response"></a><span data-ttu-id="f55e0-152">SetHoldOnMailboxes Vorgang Fehlerantwort</span><span class="sxs-lookup"><span data-stu-id="f55e0-152">SetHoldOnMailboxes operation error response</span></span>

<span data-ttu-id="f55e0-153">Das folgende Beispiel zeigt eine Fehlerantwort an eine **SetHoldOnMailboxes** Vorgang Anforderung.</span><span class="sxs-lookup"><span data-stu-id="f55e0-153">The following example shows an error response to a **SetHoldOnMailboxes** operation request.</span></span> <span data-ttu-id="f55e0-154">Dies ist eine Antwort auf eine Anforderung, die ein Bezeichner nicht ordnungsgemäß angegebene Postfach enthält.</span><span class="sxs-lookup"><span data-stu-id="f55e0-154">This is a response to a request that contains an incorrectly specified mailbox identifier.</span></span> 
  
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
      <SetHoldOnMailboxesResponse ResponseClass="Error" 
                                  xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>No mailbox is specified for hold operation. If specified in the request, then it could be the object does not exist in AD or is a Distribution Group.</MessageText>
         <ResponseCode>ErrorInvalidOperation</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </SetHoldOnMailboxesResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="f55e0-155">Die SOAP-Body-Fehlerantwort enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="f55e0-155">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="f55e0-156">SetHoldOnMailboxesResponse</span><span class="sxs-lookup"><span data-stu-id="f55e0-156">SetHoldOnMailboxesResponse</span></span>](setholdonmailboxesresponse.md)
    
- [<span data-ttu-id="f55e0-157">MessageText</span><span class="sxs-lookup"><span data-stu-id="f55e0-157">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="f55e0-158">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="f55e0-158">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="f55e0-159">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="f55e0-159">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="f55e0-160">Zusätzliche Fehlercodes, die für EWS generisch und für diese Operation spezifisch sind, finden Sie unter [ResponseCode](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="f55e0-160">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f55e0-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f55e0-161">See also</span></span>

- [<span data-ttu-id="f55e0-162">EWS-Operationen in Exchange</span><span class="sxs-lookup"><span data-stu-id="f55e0-162">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="f55e0-163">GetSearchableMailboxes-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f55e0-163">GetSearchableMailboxes operation</span></span>](getsearchablemailboxes-operation.md)
    
- [<span data-ttu-id="f55e0-164">SearchMailboxes-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f55e0-164">SearchMailboxes operation</span></span>](searchmailboxes-operation.md)
    
- [<span data-ttu-id="f55e0-165">GetHoldOnMailboxes-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f55e0-165">GetHoldOnMailboxes operation</span></span>](getholdonmailboxes-operation.md)
    
- [<span data-ttu-id="f55e0-166">GetDiscoverySearchConfiguration-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f55e0-166">GetDiscoverySearchConfiguration operation</span></span>](getdiscoverysearchconfiguration-operation.md)
    
- [<span data-ttu-id="f55e0-167">GetNonIndexableItemDetails-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f55e0-167">GetNonIndexableItemDetails operation</span></span>](getnonindexableitemdetails-operation.md)
    
- [<span data-ttu-id="f55e0-168">GetNonIndexableItemStatistics-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f55e0-168">GetNonIndexableItemStatistics operation</span></span>](getnonindexableitemstatistics-operation.md)
    

