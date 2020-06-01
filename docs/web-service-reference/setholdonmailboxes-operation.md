---
title: SetHoldOnMailboxes-Vorgang
manager: sethgros
ms.date: 01/24/2020
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9015a0d8-3495-461b-aa79-797d23169585
description: Hier finden Sie Informationen zum SetHoldOnMailboxes-EWS-Vorgang.
ms.openlocfilehash: 4d79ba9f616974b9415ae9eae23b8f5fdb0ab205
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44448394"
---
# <a name="setholdonmailboxes-operation"></a><span data-ttu-id="77b5f-103">SetHoldOnMailboxes-Vorgang</span><span class="sxs-lookup"><span data-stu-id="77b5f-103">SetHoldOnMailboxes operation</span></span>

> [!IMPORTANT]
> <span data-ttu-id="77b5f-104">Ab dem 1. April 2020 ist der SetHoldOnMailboxes-Vorgang in Exchange Online nicht mehr verfügbar.</span><span class="sxs-lookup"><span data-stu-id="77b5f-104">Starting on April 1, 2020, the SetHoldOnMailboxes operation will no longer be available in Exchange Online.</span></span> <span data-ttu-id="77b5f-105">Dieser Vorgang ist in lokalen Versionen von Exchange Server nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="77b5f-105">This operation won't be affected in on-premises versions of Exchange Server.</span></span> <span data-ttu-id="77b5f-106">Weitere Informationen finden Sie unter [Retirement of Legacy eDiscovery Tools in Exchange Online](https://docs.microsoft.com/microsoft-365/compliance/legacy-ediscovery-retirement#getsearchablemailboxes-setholdonmailboxes-and-getholdonmailboxes-operations-in-the-ews-api).</span><span class="sxs-lookup"><span data-stu-id="77b5f-106">For more information, see [Retirement of legacy eDiscovery tools in Exchange Online](https://docs.microsoft.com/microsoft-365/compliance/legacy-ediscovery-retirement#getsearchablemailboxes-setholdonmailboxes-and-getholdonmailboxes-operations-in-the-ews-api).</span></span>

<span data-ttu-id="77b5f-107">Hier finden Sie Informationen zum **SetHoldOnMailboxes** -EWS-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="77b5f-107">Find information about the **SetHoldOnMailboxes** EWS operation.</span></span> 
  
<span data-ttu-id="77b5f-108">Der **SetHoldOnMailboxes** -Vorgang legt eine Postfach-Aufbewahrungsrichtlinie für Postfächer fest.</span><span class="sxs-lookup"><span data-stu-id="77b5f-108">The **SetHoldOnMailboxes** operation sets a mailbox hold policy on mailboxes.</span></span> 
  
<span data-ttu-id="77b5f-109">Dieser Vorgang wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="77b5f-109">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-setholdonmailboxes-operation"></a><span data-ttu-id="77b5f-110">Verwenden des SetHoldOnMailboxes-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="77b5f-110">Using the SetHoldOnMailboxes operation</span></span>

<span data-ttu-id="77b5f-111">Der **SetHoldOnMailboxes** -Vorgang legt fest, dass ein Postfach für ein oder mehrere Postfächer aufbewahrt wird.</span><span class="sxs-lookup"><span data-stu-id="77b5f-111">The **SetHoldOnMailboxes** operation sets a mailbox hold on to one or more mailboxes.</span></span> 
  
### <a name="setholdonmailboxes-operation-soap-headers"></a><span data-ttu-id="77b5f-112">SOAP-Header des SetHoldOnMailboxes-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="77b5f-112">SetHoldOnMailboxes operation SOAP headers</span></span>

<span data-ttu-id="77b5f-113">Der **SetHoldOnMailboxes** -Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="77b5f-113">The **SetHoldOnMailboxes** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="77b5f-114">**Headername**</span><span class="sxs-lookup"><span data-stu-id="77b5f-114">**Header name**</span></span>|<span data-ttu-id="77b5f-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="77b5f-115">**Element**</span></span>|<span data-ttu-id="77b5f-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="77b5f-116">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="77b5f-117">**ManagementRole**</span><span class="sxs-lookup"><span data-stu-id="77b5f-117">**ManagementRole**</span></span> <br/> |[<span data-ttu-id="77b5f-118">ManagementRole</span><span class="sxs-lookup"><span data-stu-id="77b5f-118">ManagementRole</span></span>](managementrole.md) <br/> |<span data-ttu-id="77b5f-119">Gibt die Serverrollen an, die erforderlich sind, damit der Anrufer die Anforderung stellen muss.</span><span class="sxs-lookup"><span data-stu-id="77b5f-119">Identifies the server roles that are necessary in order for the caller to make the request.</span></span> <span data-ttu-id="77b5f-120">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="77b5f-120">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="77b5f-121">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="77b5f-121">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="77b5f-122">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="77b5f-122">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="77b5f-123">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="77b5f-123">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="77b5f-124">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="77b5f-124">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="77b5f-125">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="77b5f-125">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="77b5f-126">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="77b5f-126">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="77b5f-127">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="77b5f-127">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="77b5f-128">Diese Kopfzeile gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="77b5f-128">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="setholdonmailboxes-operation-request-example-apply-a-hold-on-a-mailbox"></a><span data-ttu-id="77b5f-129">SetHoldOnMailboxes-Vorgangs Anforderungs Beispiel: Anwenden eines Haltestatus für ein Postfach</span><span class="sxs-lookup"><span data-stu-id="77b5f-129">SetHoldOnMailboxes operation request example: Apply a hold on a mailbox</span></span>

<span data-ttu-id="77b5f-130">Im folgenden Beispiel einer **SetHoldOnMailboxes** -Vorgangsanforderung wird gezeigt, wie ein Haltestatus auf zwei Postfächer angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="77b5f-130">The following example of a **SetHoldOnMailboxes** operation request shows how to apply a hold on two mailboxes.</span></span> <span data-ttu-id="77b5f-131">Die Postfachsperre wurde mithilfe des Befehls [New-MailboxSearch](https://technet.microsoft.com/library/dd298064.aspx) erstellt.</span><span class="sxs-lookup"><span data-stu-id="77b5f-131">The mailbox hold was created by using the [New-MailboxSearch](https://technet.microsoft.com/library/dd298064.aspx) command.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
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

<span data-ttu-id="77b5f-132">Der SOAP-Anforderungstext Körper enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="77b5f-132">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="77b5f-133">SetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="77b5f-133">SetHoldOnMailboxes</span></span>](setholdonmailboxes.md)
    
- [<span data-ttu-id="77b5f-134">Action Type (HoldActionType)</span><span class="sxs-lookup"><span data-stu-id="77b5f-134">ActionType (HoldActionType)</span></span>](actiontype-holdactiontype.md)
    
- [<span data-ttu-id="77b5f-135">Haltestatus</span><span class="sxs-lookup"><span data-stu-id="77b5f-135">HoldId</span></span>](holdid.md)
    
- [<span data-ttu-id="77b5f-136">Query</span><span class="sxs-lookup"><span data-stu-id="77b5f-136">Query</span></span>](query.md)
    
- [<span data-ttu-id="77b5f-137">Postfächer (ArrayOfStringsType)</span><span class="sxs-lookup"><span data-stu-id="77b5f-137">Mailboxes (ArrayOfStringsType)</span></span>](mailboxes-arrayofstringstype.md)
    
- [<span data-ttu-id="77b5f-138">String</span><span class="sxs-lookup"><span data-stu-id="77b5f-138">String</span></span>](string.md)
    
- [<span data-ttu-id="77b5f-139">Sprache</span><span class="sxs-lookup"><span data-stu-id="77b5f-139">Language</span></span>](language.md)
    
- [<span data-ttu-id="77b5f-140">IncludeNonIndexableItems</span><span class="sxs-lookup"><span data-stu-id="77b5f-140">IncludeNonIndexableItems</span></span>](includenonindexableitems.md)
    
- [<span data-ttu-id="77b5f-141">Deduplizierung</span><span class="sxs-lookup"><span data-stu-id="77b5f-141">Deduplication</span></span>](deduplication.md)
    
## <a name="successful-setholdonmailboxes-operation-response"></a><span data-ttu-id="77b5f-142">Erfolgreiche Reaktion des SetHoldOnMailboxes-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="77b5f-142">Successful SetHoldOnMailboxes operation response</span></span>

<span data-ttu-id="77b5f-143">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **SetHoldOnMailboxes** -Vorgangsanforderung, um zwei Postfächer in die Warteschleife zu versetzen.</span><span class="sxs-lookup"><span data-stu-id="77b5f-143">The following example shows a successful response to a **SetHoldOnMailboxes** operation request to put two mailboxes on hold.</span></span> 
  
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
      <SetHoldOnMailboxesResponse ResponseClass="Success" 
                                  xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <MailboxHoldResult>
            <HoldId xmlns="https://schemas.microsoft.com/exchange/services/2006/types">HoldId2</HoldId>
            <Query xmlns="https://schemas.microsoft.com/exchange/services/2006/types">test</Query>
            <MailboxHoldStatuses xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="77b5f-144">Der SOAP-Antworttext Körper enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="77b5f-144">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="77b5f-145">SetHoldOnMailboxesResponse</span><span class="sxs-lookup"><span data-stu-id="77b5f-145">SetHoldOnMailboxesResponse</span></span>](setholdonmailboxesresponse.md)
    
- [<span data-ttu-id="77b5f-146">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="77b5f-146">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="77b5f-147">MailboxHoldResult</span><span class="sxs-lookup"><span data-stu-id="77b5f-147">MailboxHoldResult</span></span>](mailboxholdresult.md)
    
- [<span data-ttu-id="77b5f-148">Haltestatus</span><span class="sxs-lookup"><span data-stu-id="77b5f-148">HoldId</span></span>](holdid.md)
    
- [<span data-ttu-id="77b5f-149">Query</span><span class="sxs-lookup"><span data-stu-id="77b5f-149">Query</span></span>](query.md)
    
- [<span data-ttu-id="77b5f-150">MailboxHoldStatuses</span><span class="sxs-lookup"><span data-stu-id="77b5f-150">MailboxHoldStatuses</span></span>](mailboxholdstatuses.md)
    
- [<span data-ttu-id="77b5f-151">MailboxHoldStatus</span><span class="sxs-lookup"><span data-stu-id="77b5f-151">MailboxHoldStatus</span></span>](mailboxholdstatus.md)
    
- [<span data-ttu-id="77b5f-152">Postfach (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="77b5f-152">Mailbox (string)</span></span>](mailbox-string.md)
    
- [<span data-ttu-id="77b5f-153">Status (HoldStatusType)</span><span class="sxs-lookup"><span data-stu-id="77b5f-153">Status (HoldStatusType)</span></span>](status-holdstatustype.md)
    
- [<span data-ttu-id="77b5f-154">AdditionalInfo</span><span class="sxs-lookup"><span data-stu-id="77b5f-154">AdditionalInfo</span></span>](additionalinfo.md)
    
## <a name="setholdonmailboxes-operation-error-response"></a><span data-ttu-id="77b5f-155">Fehlerantwort des SetHoldOnMailboxes-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="77b5f-155">SetHoldOnMailboxes operation error response</span></span>

<span data-ttu-id="77b5f-156">Das folgende Beispiel zeigt eine Fehlerantwort auf eine **SetHoldOnMailboxes** -Vorgangsanforderung.</span><span class="sxs-lookup"><span data-stu-id="77b5f-156">The following example shows an error response to a **SetHoldOnMailboxes** operation request.</span></span> <span data-ttu-id="77b5f-157">Dies ist eine Antwort auf eine Anforderung, die eine falsch angegebene Post Fach Kennung enthält.</span><span class="sxs-lookup"><span data-stu-id="77b5f-157">This is a response to a request that contains an incorrectly specified mailbox identifier.</span></span> 
  
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
      <SetHoldOnMailboxesResponse ResponseClass="Error" 
                                  xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>No mailbox is specified for hold operation. If specified in the request, then it could be the object does not exist in AD or is a Distribution Group.</MessageText>
         <ResponseCode>ErrorInvalidOperation</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </SetHoldOnMailboxesResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="77b5f-158">Der SOAP-Textkörper der Fehlerantwort enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="77b5f-158">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="77b5f-159">SetHoldOnMailboxesResponse</span><span class="sxs-lookup"><span data-stu-id="77b5f-159">SetHoldOnMailboxesResponse</span></span>](setholdonmailboxesresponse.md)
    
- [<span data-ttu-id="77b5f-160">MessageText</span><span class="sxs-lookup"><span data-stu-id="77b5f-160">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="77b5f-161">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="77b5f-161">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="77b5f-162">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="77b5f-162">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="77b5f-163">Weitere Fehlercodes, die für EWS allgemein und spezifisch für diesen Vorgang sind, finden Sie unter [Response Code](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="77b5f-163">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="77b5f-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="77b5f-164">See also</span></span>

- [<span data-ttu-id="77b5f-165">EWS-Operationen in Exchange</span><span class="sxs-lookup"><span data-stu-id="77b5f-165">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="77b5f-166">GetSearchableMailboxes-Vorgang</span><span class="sxs-lookup"><span data-stu-id="77b5f-166">GetSearchableMailboxes operation</span></span>](getsearchablemailboxes-operation.md)
    
- [<span data-ttu-id="77b5f-167">SearchMailboxes-Vorgang</span><span class="sxs-lookup"><span data-stu-id="77b5f-167">SearchMailboxes operation</span></span>](searchmailboxes-operation.md)
    
- [<span data-ttu-id="77b5f-168">GetHoldOnMailboxes-Vorgang</span><span class="sxs-lookup"><span data-stu-id="77b5f-168">GetHoldOnMailboxes operation</span></span>](getholdonmailboxes-operation.md)
    
- [<span data-ttu-id="77b5f-169">GetDiscoverySearchConfiguration-Vorgang</span><span class="sxs-lookup"><span data-stu-id="77b5f-169">GetDiscoverySearchConfiguration operation</span></span>](getdiscoverysearchconfiguration-operation.md)
    
- [<span data-ttu-id="77b5f-170">GetNonIndexableItemDetails-Vorgang</span><span class="sxs-lookup"><span data-stu-id="77b5f-170">GetNonIndexableItemDetails operation</span></span>](getnonindexableitemdetails-operation.md)
    
- [<span data-ttu-id="77b5f-171">GetNonIndexableItemStatistics-Vorgang</span><span class="sxs-lookup"><span data-stu-id="77b5f-171">GetNonIndexableItemStatistics operation</span></span>](getnonindexableitemstatistics-operation.md)
    

