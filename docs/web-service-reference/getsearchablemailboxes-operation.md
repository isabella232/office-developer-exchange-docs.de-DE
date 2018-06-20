---
title: GetSearchableMailboxes-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 47f8ff57-4835-4d2d-9136-44afb31a4cbe
description: Hier finden Sie Informationen über die GetSearchableMailboxes EWS Vorgang.
ms.openlocfilehash: 5e14288280b23e2555eea4fce0f77743d7d210ce
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758794"
---
# <a name="getsearchablemailboxes-operation"></a><span data-ttu-id="9f375-103">GetSearchableMailboxes-Vorgang</span><span class="sxs-lookup"><span data-stu-id="9f375-103">GetSearchableMailboxes operation</span></span>

<span data-ttu-id="9f375-104">Hier finden Sie Informationen zum **GetSearchableMailboxes** EWS-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="9f375-104">Find information about the **GetSearchableMailboxes** EWS operation.</span></span> 
  
<span data-ttu-id="9f375-105">Der Vorgang **GetSearchableMailboxes** Ruft eine bestimmte Gruppe von durchsuchbaren Postfächer für Suchvorgänge Ermittlung ab.</span><span class="sxs-lookup"><span data-stu-id="9f375-105">The **GetSearchableMailboxes** operation gets a scoped set of searchable mailboxes for discovery searches.</span></span> <span data-ttu-id="9f375-106">Der Bereich der durchsuchbar Postfächer in der Antwort zurückgegeben, hängt von den Suchfilter und gibt an, ob die Verteilung der Gruppenmitgliedschaft erweitert ist.</span><span class="sxs-lookup"><span data-stu-id="9f375-106">The scope of searchable mailboxes returned in the response is determined by the search filter and whether distribution group membership is expanded.</span></span> 
  
<span data-ttu-id="9f375-107">Dieser Vorgang wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="9f375-107">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getsearchablemailboxes-operation"></a><span data-ttu-id="9f375-108">Verwenden des GetSearchableMailboxes-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="9f375-108">Using the GetSearchableMailboxes operation</span></span>

<span data-ttu-id="9f375-109">Der Vorgang **GetSearchableMailboxes** Ruft Informationen zu Postfächern durchsuchbar ab.</span><span class="sxs-lookup"><span data-stu-id="9f375-109">The **GetSearchableMailboxes** operation gets information about searchable mailboxes.</span></span> <span data-ttu-id="9f375-110">Die folgenden Argumente können in der Anforderung übergeben werden:</span><span class="sxs-lookup"><span data-stu-id="9f375-110">The following arguments can be passed in the request:</span></span> 
  
- <span data-ttu-id="9f375-111">[SearchFilter](searchfilter.md) – einen einzelne e-Mail-Alias als Argument akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="9f375-111">[SearchFilter](searchfilter.md) —Accepts a single email alias as an argument.</span></span> 
    
- <span data-ttu-id="9f375-112">[ExpandGroupMembership](expandgroupmembership.md) – gibt an, ob die Verteilung Gruppenmitgliedschaft in die in der Antwort zurückgegebenen Ergebnisse erweitert ist.</span><span class="sxs-lookup"><span data-stu-id="9f375-112">[ExpandGroupMembership](expandgroupmembership.md) — Indicates whether the distribution group membership is expanded in the results returned in the response.</span></span> 
    
<span data-ttu-id="9f375-113">Wenn das e-Mail-Alias im Suchfilter festgelegt, eine Verteilergruppe ist, und die Verteilung der Gruppenmitgliedschaft wird nicht erweitert, enthält die Antwort die Postfachinformationen für die Verteilergruppe.</span><span class="sxs-lookup"><span data-stu-id="9f375-113">If the email alias set in the search filter is a distribution group and the distribution group membership is not expanded, the response will contain the mailbox information for the distribution group.</span></span> <span data-ttu-id="9f375-114">Wenn das e-Mail-Alias im Suchfilter festgelegt, eine Verteilergruppe ist und Gruppenmitgliedschaft Verteilergruppe wird erweitert, enthält die Antwort die Postfachinformationen für jedes Postfach, das Mitglied der Verteilergruppe ist.</span><span class="sxs-lookup"><span data-stu-id="9f375-114">If the email alias set in the search filter is a distribution group and the distribution group membership is expanded, the response will contain the mailbox information for each mailbox that is a member of the distribution group.</span></span> <span data-ttu-id="9f375-115">Wenn der Suchfilter Alias für einen einzelnen Benutzer enthält, wird die Antwort die Postfachinformationen für die einzelnen Benutzer enthalten.</span><span class="sxs-lookup"><span data-stu-id="9f375-115">If the search filter contains a single user's alias, the response will contain the mailbox information for the single user.</span></span> <span data-ttu-id="9f375-116">Die Antwort enthält alle Postfächer durchsucht werden, wenn das Element [GetSearchableMailboxes](getsearchablemailboxes.md) leer ist.</span><span class="sxs-lookup"><span data-stu-id="9f375-116">The response will contain all searchable mailboxes if the [GetSearchableMailboxes](getsearchablemailboxes.md) element is empty.</span></span> <span data-ttu-id="9f375-117">Dies ist dasselbe wie ein leeres Element [SearchFilter](searchfilter.md) und das [ExpandGroupMembership](expandgroupmembership.md) -Element auf **"false"** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9f375-117">This is the same as having an empty [SearchFilter](searchfilter.md) element and the [ExpandGroupMembership](expandgroupmembership.md) element set to **false**.</span></span>
  
### <a name="getsearchablemailboxes-operation-soap-headers"></a><span data-ttu-id="9f375-118">GetSearchableMailboxes Vorgang SOAP-Header</span><span class="sxs-lookup"><span data-stu-id="9f375-118">GetSearchableMailboxes operation SOAP headers</span></span>

<span data-ttu-id="9f375-119">Der Vorgang **GetSearchableMailboxes** können die SOAP-Header, die in der folgenden Tabelle aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="9f375-119">The **GetSearchableMailboxes** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="9f375-120">**Headername**</span><span class="sxs-lookup"><span data-stu-id="9f375-120">**Header name**</span></span>|<span data-ttu-id="9f375-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="9f375-121">**Element**</span></span>|<span data-ttu-id="9f375-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9f375-122">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9f375-123">**ManagementRole**</span><span class="sxs-lookup"><span data-stu-id="9f375-123">**ManagementRole**</span></span> <br/> |[<span data-ttu-id="9f375-124">ManagementRole</span><span class="sxs-lookup"><span data-stu-id="9f375-124">ManagementRole</span></span>](managementrole.md) <br/> |<span data-ttu-id="9f375-125">Identifiziert die Serverrollen, die in der Reihenfolge für den Anrufer an die Anforderung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="9f375-125">Identifies the server roles that are necessary in order for the caller to make the request.</span></span> <span data-ttu-id="9f375-126">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="9f375-126">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="9f375-127">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="9f375-127">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="9f375-128">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="9f375-128">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="9f375-129">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="9f375-129">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="9f375-130">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="9f375-130">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="9f375-131">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="9f375-131">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="9f375-132">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="9f375-132">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="9f375-133">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="9f375-133">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="9f375-134">Diese Kopfzeile gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="9f375-134">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getsearchablemailboxes-operation-request-example-request-information-about-a-distribution-group"></a><span data-ttu-id="9f375-135">GetSearchableMailboxes Vorgang-anforderungsbeispiel: Anfordern von Informationen zu einer Verteilergruppe</span><span class="sxs-lookup"><span data-stu-id="9f375-135">GetSearchableMailboxes operation request example: Request information about a distribution group</span></span>

<span data-ttu-id="9f375-136">Im folgenden Beispiel wird eine **GetSearchableMailboxes** Vorgang Anforderung veranschaulicht, wie die Postfachinformationen für die Verteilergruppe Lolgroup abgerufen.</span><span class="sxs-lookup"><span data-stu-id="9f375-136">The following example of a **GetSearchableMailboxes** operation request shows how to get the mailbox information for the lolgroup distribution group.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
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

<span data-ttu-id="9f375-137">Die Anforderung SOAP-Text enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="9f375-137">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="9f375-138">GetSearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="9f375-138">GetSearchableMailboxes</span></span>](getsearchablemailboxes.md)
    
- [<span data-ttu-id="9f375-139">SearchFilter</span><span class="sxs-lookup"><span data-stu-id="9f375-139">SearchFilter</span></span>](searchfilter.md)
    
- [<span data-ttu-id="9f375-140">ExpandGroupMembership</span><span class="sxs-lookup"><span data-stu-id="9f375-140">ExpandGroupMembership</span></span>](expandgroupmembership.md)
    
## <a name="successful-getsearchablemailboxes-operation-response-get-information-about-a-distribution-group"></a><span data-ttu-id="9f375-141">Erfolgreiche GetSearchableMailboxes Vorgangsantwort: Abrufen von Informationen zu einer Verteilergruppe</span><span class="sxs-lookup"><span data-stu-id="9f375-141">Successful GetSearchableMailboxes operation response: Get information about a distribution group</span></span>

<span data-ttu-id="9f375-142">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **GetSearchableMailboxes** Vorgang Anforderung zum Abrufen der Discovery-Informationen für die Verteilergruppe Lolgroup.</span><span class="sxs-lookup"><span data-stu-id="9f375-142">The following example shows a successful response to a **GetSearchableMailboxes** operation request to get the discovery information for the lolgroup distribution group.</span></span> 
  
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
      <GetSearchableMailboxesResponse ResponseClass="Success" 
                                      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <SearchableMailboxes>
            <SearchableMailbox xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="9f375-143">Die Antwort SOAP-Text enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="9f375-143">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="9f375-144">GetSearchableMailboxesResponse</span><span class="sxs-lookup"><span data-stu-id="9f375-144">GetSearchableMailboxesResponse</span></span>](getsearchablemailboxesresponse.md)
    
- [<span data-ttu-id="9f375-145">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="9f375-145">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="9f375-146">SearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="9f375-146">SearchableMailboxes</span></span>](searchablemailboxes.md)
    
- [<span data-ttu-id="9f375-147">SearchableMailbox</span><span class="sxs-lookup"><span data-stu-id="9f375-147">SearchableMailbox</span></span>](searchablemailbox.md)
    
- [<span data-ttu-id="9f375-148">Guid</span><span class="sxs-lookup"><span data-stu-id="9f375-148">Guid</span></span>](guid-ex15websvcsotherref.md)
    
- [<span data-ttu-id="9f375-149">PrimarySmtpAddress</span><span class="sxs-lookup"><span data-stu-id="9f375-149">PrimarySmtpAddress</span></span>](primarysmtpaddress.md)
    
- [<span data-ttu-id="9f375-150">IsExternalMailbox</span><span class="sxs-lookup"><span data-stu-id="9f375-150">IsExternalMailbox</span></span>](isexternalmailbox.md)
    
- [<span data-ttu-id="9f375-151">ExternalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="9f375-151">ExternalEmailAddress</span></span>](externalemailaddress.md)
    
- [<span data-ttu-id="9f375-152">DisplayName (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="9f375-152">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="9f375-153">IsMembershipGroup</span><span class="sxs-lookup"><span data-stu-id="9f375-153">IsMembershipGroup</span></span>](ismembershipgroup.md)
    
- [<span data-ttu-id="9f375-154">ReferenceId</span><span class="sxs-lookup"><span data-stu-id="9f375-154">ReferenceId</span></span>](referenceid.md)
    
## <a name="successful-getsearchablemailboxes-operation-response-get-information-about-an-expanded-distribution-group"></a><span data-ttu-id="9f375-155">Erfolgreiche GetSearchableMailboxes Vorgangsantwort: Abrufen von Informationen zu einer erweiterten Verteilergruppe</span><span class="sxs-lookup"><span data-stu-id="9f375-155">Successful GetSearchableMailboxes operation response: Get information about an expanded distribution group</span></span>

<span data-ttu-id="9f375-156">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine Anforderung des **GetSearchableMailboxes** -Vorgang der Mitglieder der Verteilergruppe erweiterten Lolgroup Ermittlungsinformationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="9f375-156">The following example shows a successful response to a **GetSearchableMailboxes** operation request to get the discovery information about members of the expanded lolgroup distribution group.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="526" MinorBuildNumber="0" Version="Exchange2013" xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" xmlns="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetSearchableMailboxesResponse ResponseClass="Success" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <SearchableMailboxes>
        <SearchableMailbox xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
          <Guid>e2d42cdf-a227-1ec3-486b-6fa0ebaadb9f5</Guid>
          <PrimarySmtpAddress>JSmith@contoso.com</PrimarySmtpAddress>
          <IsExternalMailbox>false</IsExternalMailbox>
          <ExternalEmailAddress/>
          <DisplayName>Julia Smith</DisplayName>
          <IsMembershipGroup>false</IsMembershipGroup>
          <ReferenceId>/o=First Organization/ou=Exchange Administrative Group (FYDLT)/cn=Recipients/cn=0a1fc86f883846152405d60956dd02e7-Julia</ReferenceId>
        </SearchableMailbox>
        <SearchableMailbox xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
          <Guid>45d0fff1-6541-459a-a343-52453b30e12ca</Guid>
          <PrimarySmtpAddress>LMoore@contoso.com</PrimarySmtpAddress>
          <IsExternalMailbox>false</IsExternalMailbox>
          <ExternalEmailAddress/>
          <DisplayName>Laura Moore</DisplayName>
          <IsMembershipGroup>false</IsMembershipGroup>
          <ReferenceId>/o=First Organization/ou=Exchange Administrative Group (FYDLT)/cn=Recipients/cn=2910d8f8316f4378bbf9338d8f9d714b-Laura</ReferenceId>
        </SearchableMailbox>
        <SearchableMailbox xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="9f375-157">Die Antwort SOAP-Text enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="9f375-157">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="9f375-158">GetSearchableMailboxesResponse</span><span class="sxs-lookup"><span data-stu-id="9f375-158">GetSearchableMailboxesResponse</span></span>](getsearchablemailboxesresponse.md)
    
- [<span data-ttu-id="9f375-159">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="9f375-159">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="9f375-160">SearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="9f375-160">SearchableMailboxes</span></span>](searchablemailboxes.md)
    
- [<span data-ttu-id="9f375-161">SearchableMailbox</span><span class="sxs-lookup"><span data-stu-id="9f375-161">SearchableMailbox</span></span>](searchablemailbox.md)
    
- [<span data-ttu-id="9f375-162">Guid</span><span class="sxs-lookup"><span data-stu-id="9f375-162">Guid</span></span>](guid-ex15websvcsotherref.md)
    
- [<span data-ttu-id="9f375-163">PrimarySmtpAddress</span><span class="sxs-lookup"><span data-stu-id="9f375-163">PrimarySmtpAddress</span></span>](primarysmtpaddress.md)
    
- [<span data-ttu-id="9f375-164">IsExternalMailbox</span><span class="sxs-lookup"><span data-stu-id="9f375-164">IsExternalMailbox</span></span>](isexternalmailbox.md)
    
- [<span data-ttu-id="9f375-165">ExternalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="9f375-165">ExternalEmailAddress</span></span>](externalemailaddress.md)
    
- [<span data-ttu-id="9f375-166">DisplayName (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="9f375-166">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="9f375-167">IsMembershipGroup</span><span class="sxs-lookup"><span data-stu-id="9f375-167">IsMembershipGroup</span></span>](ismembershipgroup.md)
    
- [<span data-ttu-id="9f375-168">ReferenceId</span><span class="sxs-lookup"><span data-stu-id="9f375-168">ReferenceId</span></span>](referenceid.md)
    
## <a name="getsearchablemailboxes-operation-error-response"></a><span data-ttu-id="9f375-169">GetSearchableMailboxes Vorgang Fehlerantwort</span><span class="sxs-lookup"><span data-stu-id="9f375-169">GetSearchableMailboxes operation error response</span></span>

<span data-ttu-id="9f375-170">Das folgende Beispiel zeigt eine Fehlerantwort an eine **GetSearchableMailboxes** Vorgang Anforderung.</span><span class="sxs-lookup"><span data-stu-id="9f375-170">The following example shows an error response to a **GetSearchableMailboxes** operation request.</span></span> <span data-ttu-id="9f375-171">Dies ist eine Antwort auf eine Anforderung an alle durchsuchbaren Postfächer zu erhalten, wenn das **ExpandGroupMembership** -Argument auf **true**festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="9f375-171">This is a response to a request to get all searchable mailboxes when the **ExpandGroupMembership** argument is set to **true**.</span></span> 
  
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
      <GetSearchableMailboxesResponse ResponseClass="Error" 
                                      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>Cannot use wildcard or empty query when auto group expansion is enabled.</MessageText>
         <ResponseCode>ErrorInvalidArgument</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
         <SearchableMailboxes/>
      </GetSearchableMailboxesResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="9f375-172">Die SOAP-Body-Fehlerantwort enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="9f375-172">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="9f375-173">GetSearchableMailboxesResponse</span><span class="sxs-lookup"><span data-stu-id="9f375-173">GetSearchableMailboxesResponse</span></span>](getsearchablemailboxesresponse.md)
    
- [<span data-ttu-id="9f375-174">MessageText</span><span class="sxs-lookup"><span data-stu-id="9f375-174">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="9f375-175">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="9f375-175">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="9f375-176">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="9f375-176">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="9f375-177">SearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="9f375-177">SearchableMailboxes</span></span>](searchablemailboxes.md)
    
<span data-ttu-id="9f375-178">Zusätzliche Fehlercodes, die für EWS generisch und für diese Operation spezifisch sind, finden Sie unter [ResponseCode](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="9f375-178">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9f375-179">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9f375-179">See also</span></span>

- [<span data-ttu-id="9f375-180">EWS-Operationen in Exchange</span><span class="sxs-lookup"><span data-stu-id="9f375-180">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="9f375-181">SetHoldOnMailboxes-Vorgang</span><span class="sxs-lookup"><span data-stu-id="9f375-181">SetHoldOnMailboxes operation</span></span>](setholdonmailboxes-operation.md)
    
- [<span data-ttu-id="9f375-182">SearchMailboxes-Vorgang</span><span class="sxs-lookup"><span data-stu-id="9f375-182">SearchMailboxes operation</span></span>](searchmailboxes-operation.md)
    
- [<span data-ttu-id="9f375-183">GetHoldOnMailboxes-Vorgang</span><span class="sxs-lookup"><span data-stu-id="9f375-183">GetHoldOnMailboxes operation</span></span>](getholdonmailboxes-operation.md)
    
- [<span data-ttu-id="9f375-184">GetDiscoverySearchConfiguration-Vorgang</span><span class="sxs-lookup"><span data-stu-id="9f375-184">GetDiscoverySearchConfiguration operation</span></span>](getdiscoverysearchconfiguration-operation.md)
    
- [<span data-ttu-id="9f375-185">GetNonIndexableItemDetails-Vorgang</span><span class="sxs-lookup"><span data-stu-id="9f375-185">GetNonIndexableItemDetails operation</span></span>](getnonindexableitemdetails-operation.md)
    
- [<span data-ttu-id="9f375-186">GetNonIndexableItemStatistics-Vorgang</span><span class="sxs-lookup"><span data-stu-id="9f375-186">GetNonIndexableItemStatistics operation</span></span>](getnonindexableitemstatistics-operation.md)
    

