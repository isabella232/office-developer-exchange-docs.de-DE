---
title: GetDiscoverySearchConfiguration-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8a54a6dc-110c-4972-a8bc-5ddb43c4b857
description: Hier finden Sie Informationen zum GetDiscoverySearchConfiguration-EWS-Vorgang.
ms.openlocfilehash: 4db435988a9954b921e7851986b6f92ffedbad94
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461023"
---
# <a name="getdiscoverysearchconfiguration-operation"></a><span data-ttu-id="058b6-103">GetDiscoverySearchConfiguration-Vorgang</span><span class="sxs-lookup"><span data-stu-id="058b6-103">GetDiscoverySearchConfiguration operation</span></span>

<span data-ttu-id="058b6-104">Hier finden Sie Informationen zum **GetDiscoverySearchConfiguration** -EWS-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="058b6-104">Find information about the **GetDiscoverySearchConfiguration** EWS operation.</span></span> 
  
<span data-ttu-id="058b6-105">Der **GetDiscoverySearchConfiguration** -Vorgang gibt Konfigurationsinformationen für in-Place-Speicher, gespeicherte Ermittlungs suchen und die für die Discovery-Suche aktivierten Postfächer zurück.</span><span class="sxs-lookup"><span data-stu-id="058b6-105">The **GetDiscoverySearchConfiguration** operation returns configuration information for in-place holds, saved discovery searches, and the mailboxes that are enabled for discovery search.</span></span> 
  
<span data-ttu-id="058b6-106">Dieser Vorgang wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="058b6-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getdiscoverysearchconfiguration-operation"></a><span data-ttu-id="058b6-107">Verwenden des GetDiscoverySearchConfiguration-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="058b6-107">Using the GetDiscoverySearchConfiguration operation</span></span>

<span data-ttu-id="058b6-108">Der **GetDiscoverySearchConfiguration** -Vorgang enthält Konfigurationsinformationen für die Discovery-Suche.</span><span class="sxs-lookup"><span data-stu-id="058b6-108">The **GetDiscoverySearchConfiguration** operation provides configuration information for discovery search.</span></span> <span data-ttu-id="058b6-109">Anforderungen können eines oder mehrere der folgenden Argumente enthalten:</span><span class="sxs-lookup"><span data-stu-id="058b6-109">Requests can contain one or more of the following arguments:</span></span> 
  
1. <span data-ttu-id="058b6-110">[Search](searchid.md) -Kennung – identifiziert eine gespeicherte Ermittlungs Suche.</span><span class="sxs-lookup"><span data-stu-id="058b6-110">[SearchId](searchid.md) — Identifies a saved discovery search.</span></span> <span data-ttu-id="058b6-111">Wenn dieses Argument in der Anforderung gesendet wird, werden die Werte der anderen Argumente ignoriert.</span><span class="sxs-lookup"><span data-stu-id="058b6-111">If this argument is sent in the request, the values of the other arguments are ignored.</span></span> 
    
2. <span data-ttu-id="058b6-112">[ExpandGroupMembership](expandgroupmembership.md) – gibt an, ob die Gruppenmitgliedschaft in der Antwort erweitert wird.</span><span class="sxs-lookup"><span data-stu-id="058b6-112">[ExpandGroupMembership](expandgroupmembership.md) — Indicates whether group membership is expanded in the response.</span></span> <span data-ttu-id="058b6-113">Der Wert **true** gibt an, dass die Gruppenmitgliedschaft erweitert wird, sodass alle durchsuchbaren Postfächer in der Antwort zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="058b6-113">A value of **true** indicates that group membership is expanded so that all searchable mailboxes are returned in the response.</span></span> <span data-ttu-id="058b6-114">Der Wert **false** gibt an, dass nur die Gruppe in der Antwort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="058b6-114">A value of **false** indicates that only the group is returned in the response.</span></span> 
    
3. <span data-ttu-id="058b6-115">[InPlaceHoldConfigurationOnly](inplaceholdconfigurationonly.md) – gibt an, ob alle durchsuchbaren Postfächer zusätzlich zur in-situ-Speicherkonfiguration zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="058b6-115">[InPlaceHoldConfigurationOnly](inplaceholdconfigurationonly.md) — Indicates whether all searchable mailboxes are returned in addition to the in-place hold configuration.</span></span> <span data-ttu-id="058b6-116">Der Wert **true** gibt an, dass nur die in-situ-Aufbewahrungs Konfigurationen zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="058b6-116">A value of **true** indicates that only the in-place hold configurations are returned.</span></span> <span data-ttu-id="058b6-117">Der Wert **false** gibt an, dass alle durchsuchbaren Postfachbezeichner zusätzlich zu den in-situ-Speicher-IDs zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="058b6-117">A value of **false** indicates that all searchable mailbox identifiers are returned in addition to the in-place hold identifiers.</span></span> <span data-ttu-id="058b6-118">Wenn dieses Element nicht vorhanden ist, ist das Standardverhalten das Äquivalent des Werts **false**.</span><span class="sxs-lookup"><span data-stu-id="058b6-118">If this element is not present, the default behavior is the equivalent of the value **false**.</span></span> 
    
### <a name="getdiscoverysearchconfiguration-operation-soap-headers"></a><span data-ttu-id="058b6-119">SOAP-Header des GetDiscoverySearchConfiguration-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="058b6-119">GetDiscoverySearchConfiguration operation SOAP headers</span></span>

<span data-ttu-id="058b6-120">Der **GetDiscoverySearchConfiguration** -Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="058b6-120">The **GetDiscoverySearchConfiguration** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="058b6-121">**Headername**</span><span class="sxs-lookup"><span data-stu-id="058b6-121">**Header name**</span></span>|<span data-ttu-id="058b6-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="058b6-122">**Element**</span></span>|<span data-ttu-id="058b6-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="058b6-123">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="058b6-124">**ManagementRole**</span><span class="sxs-lookup"><span data-stu-id="058b6-124">**ManagementRole**</span></span> <br/> |[<span data-ttu-id="058b6-125">ManagementRole</span><span class="sxs-lookup"><span data-stu-id="058b6-125">ManagementRole</span></span>](managementrole.md) <br/> |<span data-ttu-id="058b6-126">Gibt die Serverrollen an, die erforderlich sind, damit der Anrufer die Anforderung stellen muss.</span><span class="sxs-lookup"><span data-stu-id="058b6-126">Identifies the server roles that are necessary in order for the caller to make the request.</span></span> <span data-ttu-id="058b6-127">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="058b6-127">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="058b6-128">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="058b6-128">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="058b6-129">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="058b6-129">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="058b6-130">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="058b6-130">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="058b6-131">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="058b6-131">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="058b6-132">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="058b6-132">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="058b6-133">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="058b6-133">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="058b6-134">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="058b6-134">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="058b6-135">Diese Kopfzeile gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="058b6-135">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getdiscoverysearchconfiguration-operation-request-example-get-the-discovery-search-configuration-for-a-saved-search"></a><span data-ttu-id="058b6-136">GetDiscoverySearchConfiguration-Vorgangs Anforderungs Beispiel: Abrufen der Ermittlungs Suchkonfiguration für eine gespeicherte Suche</span><span class="sxs-lookup"><span data-stu-id="058b6-136">GetDiscoverySearchConfiguration operation request example: Get the discovery search configuration for a saved search</span></span>

<span data-ttu-id="058b6-137">Im folgenden Beispiel einer **GetDiscoverySearchConfiguration** -Vorgangsanforderung wird gezeigt, wie die Konfiguration einer gespeicherten Suche mit dem Namen "MyDiscSearchFor-sbrown" angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="058b6-137">The following example of a **GetDiscoverySearchConfiguration** operation request shows how to request the configuration of a saved search called "MyDiscSearchFor-sbrown".</span></span> <span data-ttu-id="058b6-138">Die Argumente für die Elemente [ExpandGroupMembership](expandgroupmembership.md) und [InPlaceHoldConfigurationOnly](inplaceholdconfigurationonly.md) werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="058b6-138">The arguments for the [ExpandGroupMembership](expandgroupmembership.md) and [InPlaceHoldConfigurationOnly](inplaceholdconfigurationonly.md) elements are ignored.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:GetDiscoverySearchConfiguration>
         <m:SearchId>MyDiscSearchFor-sbrown</m:SearchId>
         <m:ExpandGroupMembership>true</m:ExpandGroupMembership>
         <m:InPlaceHoldConfigurationOnly>false</m:InPlaceHoldConfigurationOnly>
      </m:GetDiscoverySearchConfiguration>
   </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="058b6-139">Der SOAP-Anforderungstext Körper enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="058b6-139">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="058b6-140">GetDiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="058b6-140">GetDiscoverySearchConfiguration</span></span>](getdiscoverysearchconfiguration.md)
    
- [<span data-ttu-id="058b6-141">Suchtaste</span><span class="sxs-lookup"><span data-stu-id="058b6-141">SearchId</span></span>](searchid.md)
    
- [<span data-ttu-id="058b6-142">ExpandGroupMembership</span><span class="sxs-lookup"><span data-stu-id="058b6-142">ExpandGroupMembership</span></span>](expandgroupmembership.md)
    
- [<span data-ttu-id="058b6-143">InPlaceHoldConfigurationOnly</span><span class="sxs-lookup"><span data-stu-id="058b6-143">InPlaceHoldConfigurationOnly</span></span>](inplaceholdconfigurationonly.md)
    
## <a name="successful-getdiscoverysearchconfiguration-operation-response-request-for-a-single-saved-search"></a><span data-ttu-id="058b6-144">Erfolgreiche GetDiscoverySearchConfiguration-Vorgangs Antwort: Anforderung für eine einzelne gespeicherte Suche</span><span class="sxs-lookup"><span data-stu-id="058b6-144">Successful GetDiscoverySearchConfiguration operation response: Request for a single saved search</span></span>

<span data-ttu-id="058b6-145">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **GetDiscoverySearchConfiguration** -Vorgangsanforderung, um die Konfiguration einer gespeicherten Suche mit dem Namen "MyDiscSearchFor-sbrown" abzurufen.</span><span class="sxs-lookup"><span data-stu-id="058b6-145">The following example shows a successful response to a **GetDiscoverySearchConfiguration** operation request to get the configuration of a saved search called "MyDiscSearchFor-sbrown".</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="526" MinorBuildNumber="0" Version="Exchange2013" xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" xmlns="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetDiscoverySearchConfigurationResponse ResponseClass="Success" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <DiscoverySearchConfigurations>
        <DiscoverySearchConfiguration xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <SearchId>MyDiscSearchFor-sbrown</SearchId>
          <SearchQuery>test item</SearchQuery>
          <SearchableMailboxes>
            <SearchableMailbox>
              <Guid>3c620d04-8b22-432e-92be-5b9321599576</Guid>
              <PrimarySmtpAddress>SBrown@contoso.com</PrimarySmtpAddress>
              <IsExternalMailbox>false</IsExternalMailbox>
              <ExternalEmailAddress/>
              <DisplayName>Steven Brown</DisplayName>
              <IsMembershipGroup>false</IsMembershipGroup>
              <ReferenceId>/o=First/ou=Exchange(FYDILT)/cn=Recipients/cn=313ecf-Steve</ReferenceId>
            </SearchableMailbox>
          </SearchableMailboxes>
        </DiscoverySearchConfiguration>
      </DiscoverySearchConfigurations>
    </GetDiscoverySearchConfigurationResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="058b6-146">Der SOAP-Antworttext Körper enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="058b6-146">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="058b6-147">GetDiscoverySearchConfigurationResponse</span><span class="sxs-lookup"><span data-stu-id="058b6-147">GetDiscoverySearchConfigurationResponse</span></span>](getdiscoverysearchconfigurationresponse.md)
    
- [<span data-ttu-id="058b6-148">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="058b6-148">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="058b6-149">DiscoverySearchConfigurations</span><span class="sxs-lookup"><span data-stu-id="058b6-149">DiscoverySearchConfigurations</span></span>](discoverysearchconfigurations.md)
    
- [<span data-ttu-id="058b6-150">DiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="058b6-150">DiscoverySearchConfiguration</span></span>](discoverysearchconfiguration.md)
    
- [<span data-ttu-id="058b6-151">Suchtaste</span><span class="sxs-lookup"><span data-stu-id="058b6-151">SearchId</span></span>](searchid.md)
    
- [<span data-ttu-id="058b6-152">SearchQuery</span><span class="sxs-lookup"><span data-stu-id="058b6-152">SearchQuery</span></span>](searchquery.md)
    
- [<span data-ttu-id="058b6-153">SearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="058b6-153">SearchableMailboxes</span></span>](searchablemailboxes.md)
    
- [<span data-ttu-id="058b6-154">SearchableMailbox</span><span class="sxs-lookup"><span data-stu-id="058b6-154">SearchableMailbox</span></span>](searchablemailbox.md)
    
- [<span data-ttu-id="058b6-155">Guid</span><span class="sxs-lookup"><span data-stu-id="058b6-155">Guid</span></span>](guid-ex15websvcsotherref.md)
    
- [<span data-ttu-id="058b6-156">PrimarySmtpAddress (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="058b6-156">PrimarySmtpAddress (string)</span></span>](primarysmtpaddress-string.md)
    
- [<span data-ttu-id="058b6-157">IsExternalMailbox</span><span class="sxs-lookup"><span data-stu-id="058b6-157">IsExternalMailbox</span></span>](isexternalmailbox.md)
    
- [<span data-ttu-id="058b6-158">ExternalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="058b6-158">ExternalEmailAddress</span></span>](externalemailaddress.md)
    
- [<span data-ttu-id="058b6-159">DisplayName (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="058b6-159">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="058b6-160">Ismembershipgroup</span><span class="sxs-lookup"><span data-stu-id="058b6-160">IsMembershipGroup</span></span>](ismembershipgroup.md)
    
- [<span data-ttu-id="058b6-161">ReferenceId</span><span class="sxs-lookup"><span data-stu-id="058b6-161">ReferenceId</span></span>](referenceid.md)
    
## <a name="successful-getdiscoverysearchconfiguration-operation-response-request-for-in-place-holds"></a><span data-ttu-id="058b6-162">Erfolgreiche Reaktion des GetDiscoverySearchConfiguration-Vorgangs: Anforderung für in-Place-Aufbewahrungen</span><span class="sxs-lookup"><span data-stu-id="058b6-162">Successful GetDiscoverySearchConfiguration operation response: Request for in-place holds</span></span>

<span data-ttu-id="058b6-163">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **GetDiscoverySearchConfiguration** -Vorgangsanforderung, um nur in-Place-Speicher zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="058b6-163">The following example shows a successful response to a **GetDiscoverySearchConfiguration** operation request to only get in-place holds.</span></span> 
  
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
      <GetDiscoverySearchConfigurationResponse ResponseClass="Success" 
                                               xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <DiscoverySearchConfigurations>
            <DiscoverySearchConfiguration xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               <SearchId>MyDiscSearchFor-sbrown</SearchId>
               <SearchQuery>test item</SearchQuery>
               <InPlaceHoldIdentity>3f37d90f53144558a80814ef0272749a9</InPlaceHoldIdentity>
               <ManagedByOrganization/>
            </DiscoverySearchConfiguration>
            <DiscoverySearchConfiguration xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               <SearchId>MyDiscSearch</SearchId>
               <SearchQuery>test</SearchQuery>
               <InPlaceHoldIdentity>6ea486f0f3f140efb044682a2e782abdf</InPlaceHoldIdentity>
               <ManagedByOrganization/>
            </DiscoverySearchConfiguration>
         </DiscoverySearchConfigurations>
      </GetDiscoverySearchConfigurationResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="058b6-164">Der SOAP-Antworttext Körper enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="058b6-164">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="058b6-165">GetDiscoverySearchConfigurationResponse</span><span class="sxs-lookup"><span data-stu-id="058b6-165">GetDiscoverySearchConfigurationResponse</span></span>](getdiscoverysearchconfigurationresponse.md)
    
- [<span data-ttu-id="058b6-166">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="058b6-166">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="058b6-167">DiscoverySearchConfigurations</span><span class="sxs-lookup"><span data-stu-id="058b6-167">DiscoverySearchConfigurations</span></span>](discoverysearchconfigurations.md)
    
- [<span data-ttu-id="058b6-168">DiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="058b6-168">DiscoverySearchConfiguration</span></span>](discoverysearchconfiguration.md)
    
- [<span data-ttu-id="058b6-169">Suchtaste</span><span class="sxs-lookup"><span data-stu-id="058b6-169">SearchId</span></span>](searchid.md)
    
- [<span data-ttu-id="058b6-170">SearchQuery</span><span class="sxs-lookup"><span data-stu-id="058b6-170">SearchQuery</span></span>](searchquery.md)
    
- [<span data-ttu-id="058b6-171">InPlaceHoldIdentity</span><span class="sxs-lookup"><span data-stu-id="058b6-171">InPlaceHoldIdentity</span></span>](inplaceholdidentity.md)
    
- [<span data-ttu-id="058b6-172">ManagedByOrganization</span><span class="sxs-lookup"><span data-stu-id="058b6-172">ManagedByOrganization</span></span>](managedbyorganization.md)
    
## <a name="successful-getdiscoverysearchconfiguration-operation-response-request-for-all-saved-discovery-search-configurations"></a><span data-ttu-id="058b6-173">Erfolgreiche GetDiscoverySearchConfiguration-Vorgangs Antwort: Anforderung für alle gespeicherten Ermittlungs Such Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="058b6-173">Successful GetDiscoverySearchConfiguration operation response: Request for all saved discovery search configurations</span></span>

<span data-ttu-id="058b6-174">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **GetDiscoverySearchConfiguration** -Vorgangsanforderung zum Abrufen aller gespeicherten Ermittlungs suchen.</span><span class="sxs-lookup"><span data-stu-id="058b6-174">The following example shows a successful response to a **GetDiscoverySearchConfiguration** operation request to get all saved discovery searches.</span></span> 
  
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
      <GetDiscoverySearchConfigurationResponse ResponseClass="Success" 
                                               xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <DiscoverySearchConfigurations>
            <DiscoverySearchConfiguration xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               <SearchId>MyDiscSearchFor-sbrown</SearchId>
               <SearchQuery>test item</SearchQuery>
               <SearchableMailboxes>
                  <SearchableMailbox>
                     <Guid>3c620d04-8b33-435e-95be-5b9351599576</Guid>
                     <PrimarySmtpAddress>SBrown@contoso.com</PrimarySmtpAddress>
                     <IsExternalMailbox>false</IsExternalMailbox>
                     <ExternalEmailAddress/>
                     <DisplayName>Steven Brown</DisplayName>
                     <IsMembershipGroup>false</IsMembershipGroup>
                     <ReferenceId>/o=First/ou=Exchange (FYLT)/cn=Recipients/cn=35381a742f0e47e395c8601a60d13ecz-Steve</ReferenceId>
                  </SearchableMailbox>
               </SearchableMailboxes>
            </DiscoverySearchConfiguration>
            <DiscoverySearchConfiguration xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
               <SearchId>MyDiscSearch</SearchId>
               <SearchQuery>test</SearchQuery>
               <SearchableMailboxes>
                  <SearchableMailbox>
                     <Guid>e788c4b0-54a2-458c-83b2-22d5bb02b23f</Guid>
                     <PrimarySmtpAddress>Administrator@contoso.com</PrimarySmtpAddress>
                     <IsExternalMailbox>false</IsExternalMailbox>
                     <ExternalEmailAddress/>
                     <DisplayName>Administrator</DisplayName>
                     <IsMembershipGroup>false</IsMembershipGroup>
                     <ReferenceId>/o=First/ou=Exchange (FYLT)/cn=Recipients/cn=ebez7871332d4595abe1c62962911a58-Admin</ReferenceId>
                  </SearchableMailbox>
                  <SearchableMailbox>
                     <Guid>6f6cff39-8967-4a60-b43f-328413c25199</Guid>
                     <PrimarySmtpAddress>ADavis@contoso.com</PrimarySmtpAddress>
                     <IsExternalMailbox>false</IsExternalMailbox>
                     <ExternalEmailAddress/>
                     <DisplayName>Anthony Davis</DisplayName>
                     <IsMembershipGroup>false</IsMembershipGroup>
                     <ReferenceId>/o=First/ou=Exchange (FYLT)/cn=Recipients/cn=f10c9f70519844beb04101d8f40c572z-Antho</ReferenceId>
                  </SearchableMailbox>
               </SearchableMailboxes>
            </DiscoverySearchConfiguration>
         </DiscoverySearchConfigurations>
      </GetDiscoverySearchConfigurationResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="058b6-175">Der SOAP-Antworttext Körper enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="058b6-175">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="058b6-176">GetDiscoverySearchConfigurationResponse</span><span class="sxs-lookup"><span data-stu-id="058b6-176">GetDiscoverySearchConfigurationResponse</span></span>](getdiscoverysearchconfigurationresponse.md)
    
- [<span data-ttu-id="058b6-177">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="058b6-177">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="058b6-178">DiscoverySearchConfigurations</span><span class="sxs-lookup"><span data-stu-id="058b6-178">DiscoverySearchConfigurations</span></span>](discoverysearchconfigurations.md)
    
- [<span data-ttu-id="058b6-179">DiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="058b6-179">DiscoverySearchConfiguration</span></span>](discoverysearchconfiguration.md)
    
- [<span data-ttu-id="058b6-180">Suchtaste</span><span class="sxs-lookup"><span data-stu-id="058b6-180">SearchId</span></span>](searchid.md)
    
- [<span data-ttu-id="058b6-181">SearchQuery</span><span class="sxs-lookup"><span data-stu-id="058b6-181">SearchQuery</span></span>](searchquery.md)
    
- [<span data-ttu-id="058b6-182">SearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="058b6-182">SearchableMailboxes</span></span>](searchablemailboxes.md)
    
- [<span data-ttu-id="058b6-183">SearchableMailbox</span><span class="sxs-lookup"><span data-stu-id="058b6-183">SearchableMailbox</span></span>](searchablemailbox.md)
    
- [<span data-ttu-id="058b6-184">Guid</span><span class="sxs-lookup"><span data-stu-id="058b6-184">Guid</span></span>](guid-ex15websvcsotherref.md)
    
- [<span data-ttu-id="058b6-185">PrimarySmtpAddress (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="058b6-185">PrimarySmtpAddress (string)</span></span>](primarysmtpaddress-string.md)
    
- [<span data-ttu-id="058b6-186">IsExternalMailbox</span><span class="sxs-lookup"><span data-stu-id="058b6-186">IsExternalMailbox</span></span>](isexternalmailbox.md)
    
- [<span data-ttu-id="058b6-187">ExternalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="058b6-187">ExternalEmailAddress</span></span>](externalemailaddress.md)
    
- [<span data-ttu-id="058b6-188">DisplayName (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="058b6-188">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="058b6-189">Ismembershipgroup</span><span class="sxs-lookup"><span data-stu-id="058b6-189">IsMembershipGroup</span></span>](ismembershipgroup.md)
    
- [<span data-ttu-id="058b6-190">ReferenceId</span><span class="sxs-lookup"><span data-stu-id="058b6-190">ReferenceId</span></span>](referenceid.md)
    
## <a name="getdiscoverysearchconfiguration-operation-error-response"></a><span data-ttu-id="058b6-191">Fehlerantwort des GetDiscoverySearchConfiguration-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="058b6-191">GetDiscoverySearchConfiguration operation error response</span></span>

<span data-ttu-id="058b6-192">Das folgende Beispiel zeigt eine Fehlerantwort auf eine **GetDiscoverySearchConfiguration** -Vorgangsanforderung.</span><span class="sxs-lookup"><span data-stu-id="058b6-192">The following example shows an error response to a **GetDiscoverySearchConfiguration** operation request.</span></span> <span data-ttu-id="058b6-193">Dies ist eine Antwort auf eine Anforderung zum Abrufen einer gespeicherten Suche, die auf dem Server nicht gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="058b6-193">This is a response to a request to get a saved search that is not found on the server.</span></span> 
  
```XML
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
      <GetDiscoverySearchConfigurationResponse ResponseClass="Error" 
                                               xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>Search configuration corresponding to the search id was not found.</MessageText>
         <ResponseCode>ErrorInvalidArgument</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
         <DiscoverySearchConfigurations/>
      </GetDiscoverySearchConfigurationResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="058b6-194">Der SOAP-Textkörper der Fehlerantwort enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="058b6-194">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="058b6-195">GetDiscoverySearchConfigurationResponse</span><span class="sxs-lookup"><span data-stu-id="058b6-195">GetDiscoverySearchConfigurationResponse</span></span>](getdiscoverysearchconfigurationresponse.md)
    
- [<span data-ttu-id="058b6-196">MessageText</span><span class="sxs-lookup"><span data-stu-id="058b6-196">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="058b6-197">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="058b6-197">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="058b6-198">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="058b6-198">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="058b6-199">DiscoverySearchConfigurations</span><span class="sxs-lookup"><span data-stu-id="058b6-199">DiscoverySearchConfigurations</span></span>](discoverysearchconfigurations.md)
    
<span data-ttu-id="058b6-200">Weitere Fehlercodes, die für EWS allgemein und spezifisch für diesen Vorgang sind, finden Sie unter [Response Code](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="058b6-200">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="058b6-201">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="058b6-201">See also</span></span>

- [<span data-ttu-id="058b6-202">EWS-Operationen in Exchange</span><span class="sxs-lookup"><span data-stu-id="058b6-202">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="058b6-203">GetSearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="058b6-203">GetSearchableMailboxes</span></span>](getsearchablemailboxes.md)
    
- [<span data-ttu-id="058b6-204">SearchMailboxes</span><span class="sxs-lookup"><span data-stu-id="058b6-204">SearchMailboxes</span></span>](searchmailboxes.md)
    
- [<span data-ttu-id="058b6-205">GetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="058b6-205">GetHoldOnMailboxes</span></span>](getholdonmailboxes.md)
    
- [<span data-ttu-id="058b6-206">SetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="058b6-206">SetHoldOnMailboxes</span></span>](setholdonmailboxes.md)
    
- [<span data-ttu-id="058b6-207">GetNonIndexableItemDetails</span><span class="sxs-lookup"><span data-stu-id="058b6-207">GetNonIndexableItemDetails</span></span>](getnonindexableitemdetails.md)
    
- [<span data-ttu-id="058b6-208">GetNonIndexableItemStatistics</span><span class="sxs-lookup"><span data-stu-id="058b6-208">GetNonIndexableItemStatistics</span></span>](getnonindexableitemstatistics.md)
    

