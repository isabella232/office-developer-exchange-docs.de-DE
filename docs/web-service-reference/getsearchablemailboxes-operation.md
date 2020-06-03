---
title: GetSearchableMailboxes-Vorgang
manager: sethgros
ms.date: 01/24/2020
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 47f8ff57-4835-4d2d-9136-44afb31a4cbe
description: Hier finden Sie Informationen zum GetSearchableMailboxes-EWS-Vorgang.
ms.openlocfilehash: e893a66eb1b638479eeccc6bd7548cb020f37243
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530839"
---
# <a name="getsearchablemailboxes-operation"></a><span data-ttu-id="f642d-103">GetSearchableMailboxes-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f642d-103">GetSearchableMailboxes operation</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f642d-104">Ab dem 1. April 2020 ist der GetSearchableMailboxes-Vorgang in Exchange Online nicht mehr verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f642d-104">Starting on April 1, 2020, the GetSearchableMailboxes operation will no longer be available in Exchange Online.</span></span> <span data-ttu-id="f642d-105">Dieser Vorgang ist in lokalen Versionen von Exchange Server nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="f642d-105">This operation won't be affected in on-premises versions of Exchange Server.</span></span> <span data-ttu-id="f642d-106">Weitere Informationen finden Sie unter [Retirement of Legacy eDiscovery Tools in Exchange Online](https://docs.microsoft.com/microsoft-365/compliance/legacy-ediscovery-retirement#getsearchablemailboxes-setholdonmailboxes-and-getholdonmailboxes-operations-in-the-ews-api).</span><span class="sxs-lookup"><span data-stu-id="f642d-106">For more information, see [Retirement of legacy eDiscovery tools in Exchange Online](https://docs.microsoft.com/microsoft-365/compliance/legacy-ediscovery-retirement#getsearchablemailboxes-setholdonmailboxes-and-getholdonmailboxes-operations-in-the-ews-api).</span></span>

<span data-ttu-id="f642d-107">Hier finden Sie Informationen zum **GetSearchableMailboxes** -EWS-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="f642d-107">Find information about the **GetSearchableMailboxes** EWS operation.</span></span> 
  
<span data-ttu-id="f642d-108">Der **GetSearchableMailboxes** -Vorgang ruft einen Bereich mit durchsuchbaren Postfächern für Ermittlungs suchen ab.</span><span class="sxs-lookup"><span data-stu-id="f642d-108">The **GetSearchableMailboxes** operation gets a scoped set of searchable mailboxes for discovery searches.</span></span> <span data-ttu-id="f642d-109">Der Umfang der durchsuchbaren Postfächer, die in der Antwort zurückgegeben werden, wird durch den Suchfilter bestimmt und ob die Mitgliedschaft in Verteilergruppen erweitert wird.</span><span class="sxs-lookup"><span data-stu-id="f642d-109">The scope of searchable mailboxes returned in the response is determined by the search filter and whether distribution group membership is expanded.</span></span> 

> [!NOTE] 
> <span data-ttu-id="f642d-110">Dieser Vorgang ist für die Verwendung mit dem Suchfilter und zum Abrufen nur der ersten paar Tausender vorgesehen. Es ist nicht für den vollständigen Abruf vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="f642d-110">This operation is intended to be used with the search filter and to retrieve only the first few thousands; it's not intended for exhaustive retrieval.</span></span>
  
<span data-ttu-id="f642d-111">Dieser Vorgang wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="f642d-111">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getsearchablemailboxes-operation"></a><span data-ttu-id="f642d-112">Verwenden des GetSearchableMailboxes-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="f642d-112">Using the GetSearchableMailboxes operation</span></span>

<span data-ttu-id="f642d-113">Der **GetSearchableMailboxes** -Vorgang ruft Informationen zu durchsuchbaren Postfächern ab.</span><span class="sxs-lookup"><span data-stu-id="f642d-113">The **GetSearchableMailboxes** operation gets information about searchable mailboxes.</span></span> <span data-ttu-id="f642d-114">Die folgenden Argumente können in der Anforderung übergeben werden:</span><span class="sxs-lookup"><span data-stu-id="f642d-114">The following arguments can be passed in the request:</span></span> 
  
- <span data-ttu-id="f642d-115">[SearchFilter](searchfilter.md) – akzeptiert einen einzelnen e-Mail-Alias als Argument.</span><span class="sxs-lookup"><span data-stu-id="f642d-115">[SearchFilter](searchfilter.md) - Accepts a single email alias as an argument.</span></span> 
    
- <span data-ttu-id="f642d-116">[ExpandGroupMembership](expandgroupmembership.md) – gibt an, ob die Mitgliedschaft in Verteilergruppen in den Ergebnissen erweitert wird, die in der Antwort zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f642d-116">[ExpandGroupMembership](expandgroupmembership.md) - Indicates whether the distribution group membership is expanded in the results returned in the response.</span></span> 
    
<span data-ttu-id="f642d-117">Wenn der e-Mail-Aliassatz im Suchfilter eine Verteilergruppe ist und die Mitgliedschaft der Verteilergruppe nicht erweitert wird, enthält die Antwort die Postfachinformationen für die Verteilergruppe.</span><span class="sxs-lookup"><span data-stu-id="f642d-117">If the email alias set in the search filter is a distribution group and the distribution group membership is not expanded, the response will contain the mailbox information for the distribution group.</span></span> <span data-ttu-id="f642d-118">Wenn der e-Mail-Aliassatz im Suchfilter eine Verteilergruppe ist und die Mitgliedschaft der Verteilergruppe erweitert wird, enthält die Antwort die Postfachinformationen für jedes Postfach, das Mitglied der Verteilergruppe ist.</span><span class="sxs-lookup"><span data-stu-id="f642d-118">If the email alias set in the search filter is a distribution group and the distribution group membership is expanded, the response will contain the mailbox information for each mailbox that is a member of the distribution group.</span></span> <span data-ttu-id="f642d-119">Wenn der Suchfilter den Alias eines einzelnen Benutzers enthält, enthält die Antwort die Postfachinformationen für den einzelnen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="f642d-119">If the search filter contains a single user's alias, the response will contain the mailbox information for the single user.</span></span> <span data-ttu-id="f642d-120">Die Antwort enthält alle durchsuchbaren Postfächer, wenn das [GetSearchableMailboxes](getsearchablemailboxes.md) -Element leer ist.</span><span class="sxs-lookup"><span data-stu-id="f642d-120">The response will contain all searchable mailboxes if the [GetSearchableMailboxes](getsearchablemailboxes.md) element is empty.</span></span> <span data-ttu-id="f642d-121">Dies ist identisch mit einem leeren [SearchFilter](searchfilter.md) -Element und dem [ExpandGroupMembership](expandgroupmembership.md) -Element, das auf **false**festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f642d-121">This is the same as having an empty [SearchFilter](searchfilter.md) element and the [ExpandGroupMembership](expandgroupmembership.md) element set to **false**.</span></span>
  
### <a name="getsearchablemailboxes-operation-soap-headers"></a><span data-ttu-id="f642d-122">SOAP-Header des GetSearchableMailboxes-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="f642d-122">GetSearchableMailboxes operation SOAP headers</span></span>

<span data-ttu-id="f642d-123">Der **GetSearchableMailboxes** -Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="f642d-123">The **GetSearchableMailboxes** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="f642d-124">Headername</span><span class="sxs-lookup"><span data-stu-id="f642d-124">Header name</span></span>|<span data-ttu-id="f642d-125">Element</span><span class="sxs-lookup"><span data-stu-id="f642d-125">Element</span></span>|<span data-ttu-id="f642d-126">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f642d-126">Description</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f642d-127">**ManagementRole**</span><span class="sxs-lookup"><span data-stu-id="f642d-127">**ManagementRole**</span></span> <br/> |[<span data-ttu-id="f642d-128">ManagementRole</span><span class="sxs-lookup"><span data-stu-id="f642d-128">ManagementRole</span></span>](managementrole.md) <br/> |<span data-ttu-id="f642d-129">Gibt die Serverrollen an, die erforderlich sind, damit der Anrufer die Anforderung stellen muss.</span><span class="sxs-lookup"><span data-stu-id="f642d-129">Identifies the server roles that are necessary in order for the caller to make the request.</span></span> <span data-ttu-id="f642d-130">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="f642d-130">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="f642d-131">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="f642d-131">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="f642d-132">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="f642d-132">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="f642d-133">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="f642d-133">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="f642d-134">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="f642d-134">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="f642d-135">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="f642d-135">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="f642d-136">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="f642d-136">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="f642d-137">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="f642d-137">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="f642d-138">Diese Kopfzeile gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="f642d-138">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getsearchablemailboxes-operation-request-example-request-information-about-a-distribution-group"></a><span data-ttu-id="f642d-139">GetSearchableMailboxes-Vorgangs Anforderungs Beispiel: Anfordern von Informationen zu einer Verteilergruppe</span><span class="sxs-lookup"><span data-stu-id="f642d-139">GetSearchableMailboxes operation request example: Request information about a distribution group</span></span>

<span data-ttu-id="f642d-140">Im folgenden Beispiel einer **GetSearchableMailboxes** -Vorgangsanforderung wird gezeigt, wie die Postfachinformationen für die lolgroup-Verteilergruppe abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f642d-140">The following example of a **GetSearchableMailboxes** operation request shows how to get the mailbox information for the lolgroup distribution group.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:GetSearchableMailboxes>
         <m:SearchFilter>lolgroup</m:SearchFilter>
         <m:ExpandGroupMembership>false</m:ExpandGroupMembership>
      </m:GetSearchableMailboxes>
   </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="f642d-141">Der SOAP-Anforderungstext Körper enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="f642d-141">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="f642d-142">GetSearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="f642d-142">GetSearchableMailboxes</span></span>](getsearchablemailboxes.md)   
- [<span data-ttu-id="f642d-143">SearchFilter</span><span class="sxs-lookup"><span data-stu-id="f642d-143">SearchFilter</span></span>](searchfilter.md)    
- [<span data-ttu-id="f642d-144">ExpandGroupMembership</span><span class="sxs-lookup"><span data-stu-id="f642d-144">ExpandGroupMembership</span></span>](expandgroupmembership.md)
    
## <a name="successful-getsearchablemailboxes-operation-response-get-information-about-a-distribution-group"></a><span data-ttu-id="f642d-145">Erfolgreiche GetSearchableMailboxes-Vorgangs Antwort: Abrufen von Informationen zu einer Verteilergruppe</span><span class="sxs-lookup"><span data-stu-id="f642d-145">Successful GetSearchableMailboxes operation response: Get information about a distribution group</span></span>

<span data-ttu-id="f642d-146">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **GetSearchableMailboxes** -Vorgangsanforderung zum Abrufen der Ermittlungsinformationen für die lolgroup-Verteilergruppe.</span><span class="sxs-lookup"><span data-stu-id="f642d-146">The following example shows a successful response to a **GetSearchableMailboxes** operation request to get the discovery information for the lolgroup distribution group.</span></span> 
  
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
      <GetSearchableMailboxesResponse ResponseClass="Success" 
                                      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <SearchableMailboxes>
            <SearchableMailbox xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               <Guid>33a408fe-2574-4e3b-49f5-5e1e000a3035</Guid>
               <PrimarySmtpAddress>LOLgroup@contoso.com</PrimarySmtpAddress>
               <IsExternalMailbox>false</IsExternalMailbox>
               <ExternalEmailAddress/>
               <DisplayName>LOLgroup</DisplayName>
               <IsMembershipGroup>true</IsMembershipGroup>
               <ReferenceId>/o=First/ou=Exchange(FYLT)/cn=Recipients/cn=81213b958a0b5295b13b3f02b812bf1bc-LOLgroup</ReferenceId>
            </SearchableMailbox>
         </SearchableMailboxes>
      </GetSearchableMailboxesResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="f642d-147">Der SOAP-Antworttext Körper enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="f642d-147">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="f642d-148">GetSearchableMailboxesResponse</span><span class="sxs-lookup"><span data-stu-id="f642d-148">GetSearchableMailboxesResponse</span></span>](getsearchablemailboxesresponse.md)   
- [<span data-ttu-id="f642d-149">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="f642d-149">ResponseCode</span></span>](responsecode.md)   
- [<span data-ttu-id="f642d-150">SearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="f642d-150">SearchableMailboxes</span></span>](searchablemailboxes.md)    
- [<span data-ttu-id="f642d-151">SearchableMailbox</span><span class="sxs-lookup"><span data-stu-id="f642d-151">SearchableMailbox</span></span>](searchablemailbox.md)    
- [<span data-ttu-id="f642d-152">Guid</span><span class="sxs-lookup"><span data-stu-id="f642d-152">Guid</span></span>](guid-ex15websvcsotherref.md)    
- [<span data-ttu-id="f642d-153">PrimarySmtpAddress</span><span class="sxs-lookup"><span data-stu-id="f642d-153">PrimarySmtpAddress</span></span>](primarysmtpaddress.md)    
- [<span data-ttu-id="f642d-154">IsExternalMailbox</span><span class="sxs-lookup"><span data-stu-id="f642d-154">IsExternalMailbox</span></span>](isexternalmailbox.md)   
- [<span data-ttu-id="f642d-155">ExternalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="f642d-155">ExternalEmailAddress</span></span>](externalemailaddress.md)    
- [<span data-ttu-id="f642d-156">DisplayName (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="f642d-156">DisplayName (string)</span></span>](displayname-string.md)    
- [<span data-ttu-id="f642d-157">Ismembershipgroup</span><span class="sxs-lookup"><span data-stu-id="f642d-157">IsMembershipGroup</span></span>](ismembershipgroup.md)    
- [<span data-ttu-id="f642d-158">ReferenceId</span><span class="sxs-lookup"><span data-stu-id="f642d-158">ReferenceId</span></span>](referenceid.md)
    
## <a name="successful-getsearchablemailboxes-operation-response-get-information-about-an-expanded-distribution-group"></a><span data-ttu-id="f642d-159">Erfolgreiche GetSearchableMailboxes-Vorgangs Antwort: Abrufen von Informationen zu einer erweiterten Verteilergruppe</span><span class="sxs-lookup"><span data-stu-id="f642d-159">Successful GetSearchableMailboxes operation response: Get information about an expanded distribution group</span></span>

<span data-ttu-id="f642d-160">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **GetSearchableMailboxes** -Vorgangsanforderung zum Abrufen der Ermittlungsinformationen über Mitglieder der erweiterten lolgroup-Verteilergruppe.</span><span class="sxs-lookup"><span data-stu-id="f642d-160">The following example shows a successful response to a **GetSearchableMailboxes** operation request to get the discovery information about members of the expanded lolgroup distribution group.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="526" MinorBuildNumber="0" Version="Exchange2013" xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" xmlns="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetSearchableMailboxesResponse ResponseClass="Success" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <SearchableMailboxes>
        <SearchableMailbox xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <Guid>e2d42cdf-a227-1ec3-486b-6fa0ebaadb9f5</Guid>
          <PrimarySmtpAddress>JSmith@contoso.com</PrimarySmtpAddress>
          <IsExternalMailbox>false</IsExternalMailbox>
          <ExternalEmailAddress/>
          <DisplayName>Julia Smith</DisplayName>
          <IsMembershipGroup>false</IsMembershipGroup>
          <ReferenceId>/o=First Organization/ou=Exchange Administrative Group (FYDLT)/cn=Recipients/cn=0a1fc86f883846152405d60956dd02e7-Julia</ReferenceId>
        </SearchableMailbox>
        <SearchableMailbox xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <Guid>45d0fff1-6541-459a-a343-52453b30e12ca</Guid>
          <PrimarySmtpAddress>LMoore@contoso.com</PrimarySmtpAddress>
          <IsExternalMailbox>false</IsExternalMailbox>
          <ExternalEmailAddress/>
          <DisplayName>Laura Moore</DisplayName>
          <IsMembershipGroup>false</IsMembershipGroup>
          <ReferenceId>/o=First Organization/ou=Exchange Administrative Group (FYDLT)/cn=Recipients/cn=2910d8f8316f4378bbf9338d8f9d714b-Laura</ReferenceId>
        </SearchableMailbox>
        <SearchableMailbox xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <Guid>3c620d04-8b33-435a-95be-5b939375576</Guid>
          <PrimarySmtpAddress>SBrown@contoso.com</PrimarySmtpAddress>
          <IsExternalMailbox>false</IsExternalMailbox>
          <ExternalEmailAddress/>
          <DisplayName>Steven Brown</DisplayName>
          <IsMembershipGroup>false</IsMembershipGroup>
          <ReferenceId>/o=First Organization/ou=Exchange Administrative Group (FYDLT)/cn=Recipients/cn=90312341a742f0e47e392c80a60d13ecf-Steve</ReferenceId>
        </SearchableMailbox>
      </SearchableMailboxes>
    </GetSearchableMailboxesResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="f642d-161">Der SOAP-Antworttext Körper enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="f642d-161">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="f642d-162">GetSearchableMailboxesResponse</span><span class="sxs-lookup"><span data-stu-id="f642d-162">GetSearchableMailboxesResponse</span></span>](getsearchablemailboxesresponse.md)    
- [<span data-ttu-id="f642d-163">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="f642d-163">ResponseCode</span></span>](responsecode.md)   
- [<span data-ttu-id="f642d-164">SearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="f642d-164">SearchableMailboxes</span></span>](searchablemailboxes.md)    
- [<span data-ttu-id="f642d-165">SearchableMailbox</span><span class="sxs-lookup"><span data-stu-id="f642d-165">SearchableMailbox</span></span>](searchablemailbox.md)    
- [<span data-ttu-id="f642d-166">Guid</span><span class="sxs-lookup"><span data-stu-id="f642d-166">Guid</span></span>](guid-ex15websvcsotherref.md)    
- [<span data-ttu-id="f642d-167">PrimarySmtpAddress</span><span class="sxs-lookup"><span data-stu-id="f642d-167">PrimarySmtpAddress</span></span>](primarysmtpaddress.md)    
- [<span data-ttu-id="f642d-168">IsExternalMailbox</span><span class="sxs-lookup"><span data-stu-id="f642d-168">IsExternalMailbox</span></span>](isexternalmailbox.md)    
- [<span data-ttu-id="f642d-169">ExternalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="f642d-169">ExternalEmailAddress</span></span>](externalemailaddress.md)    
- [<span data-ttu-id="f642d-170">DisplayName (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="f642d-170">DisplayName (string)</span></span>](displayname-string.md)    
- [<span data-ttu-id="f642d-171">Ismembershipgroup</span><span class="sxs-lookup"><span data-stu-id="f642d-171">IsMembershipGroup</span></span>](ismembershipgroup.md)    
- [<span data-ttu-id="f642d-172">ReferenceId</span><span class="sxs-lookup"><span data-stu-id="f642d-172">ReferenceId</span></span>](referenceid.md)
    
## <a name="getsearchablemailboxes-operation-error-response"></a><span data-ttu-id="f642d-173">Fehlerantwort des GetSearchableMailboxes-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="f642d-173">GetSearchableMailboxes operation error response</span></span>

<span data-ttu-id="f642d-174">Das folgende Beispiel zeigt eine Fehlerantwort auf eine **GetSearchableMailboxes** -Vorgangsanforderung.</span><span class="sxs-lookup"><span data-stu-id="f642d-174">The following example shows an error response to a **GetSearchableMailboxes** operation request.</span></span> <span data-ttu-id="f642d-175">Dies ist eine Antwort auf eine Anforderung zum Abrufen aller durchsuchbaren Postfächer, wenn das **ExpandGroupMembership** -Argument auf **true**festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f642d-175">This is a response to a request to get all searchable mailboxes when the **ExpandGroupMembership** argument is set to **true**.</span></span> 
  
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
      <GetSearchableMailboxesResponse ResponseClass="Error" 
                                      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>Cannot use wildcard or empty query when auto group expansion is enabled.</MessageText>
         <ResponseCode>ErrorInvalidArgument</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
         <SearchableMailboxes/>
      </GetSearchableMailboxesResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="f642d-176">Der SOAP-Textkörper der Fehlerantwort enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="f642d-176">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="f642d-177">GetSearchableMailboxesResponse</span><span class="sxs-lookup"><span data-stu-id="f642d-177">GetSearchableMailboxesResponse</span></span>](getsearchablemailboxesresponse.md)  
- [<span data-ttu-id="f642d-178">MessageText</span><span class="sxs-lookup"><span data-stu-id="f642d-178">MessageText</span></span>](messagetext.md)   
- [<span data-ttu-id="f642d-179">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="f642d-179">ResponseCode</span></span>](responsecode.md)   
- [<span data-ttu-id="f642d-180">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="f642d-180">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) 
- [<span data-ttu-id="f642d-181">SearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="f642d-181">SearchableMailboxes</span></span>](searchablemailboxes.md)
    
<span data-ttu-id="f642d-182">Weitere Fehlercodes, die für EWS allgemein und spezifisch für diesen Vorgang sind, finden Sie unter [Response Code](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="f642d-182">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f642d-183">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f642d-183">See also</span></span>

- [<span data-ttu-id="f642d-184">EWS-Operationen in Exchange</span><span class="sxs-lookup"><span data-stu-id="f642d-184">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)   
- [<span data-ttu-id="f642d-185">SetHoldOnMailboxes-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f642d-185">SetHoldOnMailboxes operation</span></span>](setholdonmailboxes-operation.md)   
- [<span data-ttu-id="f642d-186">SearchMailboxes-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f642d-186">SearchMailboxes operation</span></span>](searchmailboxes-operation.md)   
- [<span data-ttu-id="f642d-187">GetHoldOnMailboxes-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f642d-187">GetHoldOnMailboxes operation</span></span>](getholdonmailboxes-operation.md)    
- [<span data-ttu-id="f642d-188">GetDiscoverySearchConfiguration-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f642d-188">GetDiscoverySearchConfiguration operation</span></span>](getdiscoverysearchconfiguration-operation.md)   
- [<span data-ttu-id="f642d-189">GetNonIndexableItemDetails-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f642d-189">GetNonIndexableItemDetails operation</span></span>](getnonindexableitemdetails-operation.md)   
- [<span data-ttu-id="f642d-190">GetNonIndexableItemStatistics-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f642d-190">GetNonIndexableItemStatistics operation</span></span>](getnonindexableitemstatistics-operation.md)
    

