---
title: POX-AutoErmittlungsantwort für Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 08c6c5a2-a67a-4141-a8bd-1b5d560b90a7
description: Die Antwort der AutoErmittlung enthält eine Antwort auf die AutoErmittlung-Anforderung, die eine Liste der URLs enthält, die zum Erstellen einer Bindung zu den Exchange-Webdiensten verwendet werden.
ms.openlocfilehash: 0d903d9829fa6dc1273d8b25a1eeb0b68700d5da
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462283"
---
# <a name="pox-autodiscover-response-for-exchange"></a><span data-ttu-id="6a179-103">POX-AutoErmittlungsantwort für Exchange</span><span class="sxs-lookup"><span data-stu-id="6a179-103">POX Autodiscover response for Exchange</span></span>

<span data-ttu-id="6a179-104">Die Antwort der AutoErmittlung enthält eine Antwort auf die AutoErmittlung-Anforderung, die eine Liste der URLs enthält, die zum Erstellen einer Bindung zu den Exchange-Webdiensten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6a179-104">The Autodiscover response contains a response to an Autodiscover request that includes a list of URLs that are used to establish a binding with Exchange Web Services (EWS).</span></span>
  
## <a name="autodiscover-response-example"></a><span data-ttu-id="6a179-105">AutoErmittlung-Antwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="6a179-105">Autodiscover response example</span></span>

### <a name="description"></a><span data-ttu-id="6a179-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6a179-106">Description</span></span>

<span data-ttu-id="6a179-107">Im folgenden Beispiel ist eine erfolgreiche AutoErmittlung-Antwort dargestellt.</span><span class="sxs-lookup"><span data-stu-id="6a179-107">The following example shows a successful Autodiscover response.</span></span>
  
### <a name="code"></a><span data-ttu-id="6a179-108">Code</span><span class="sxs-lookup"><span data-stu-id="6a179-108">Code</span></span>

```XML
<Autodiscover xmlns="https://schemas.microsoft.com/exchange/autodiscover/responseschema/2006">
  <Response xmlns="https://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a">
    <User>
      <DisplayName>First Last</DisplayName>
      <LegacyDN>/o=contoso/ou=First Administrative Group/cn=Recipients/cn=iuser885646</LegacyDN>
      <DeploymentId>644560b8-a1ce-429c-8ace-23395843f701</DeploymentId>
    </User>
    <Account>
      <AccountType>email</AccountType>
      <Action>settings</Action>
      <Protocol>
        <Type>EXCH</Type>
        <Server>MBX-SERVER.mail.internal.contoso.com</Server>
        <ServerDN>/o=contoso/ou=Exchange Administrative Group (FYDIBOHF23SPDLT)/cn=Configuration/cn=Servers/cn=MBX-SERVER</ServerDN>
        <ServerVersion>72008287</ServerVersion>
        <MdbDN>/o=contoso/ou=Exchange Administrative Group (FYDIBOHF23SPDLT)/cn=Configuration/cn=Servers/cn=MBX-SERVER/cn=Microsoft Private MDB</MdbDN>
        <ASUrl>https://mail.contoso.com/ews/exchange.asmx</ASUrl>
        <OOFUrl>https://mail.contoso.com/ews/exchange.asmx</OOFUrl>
        <UMUrl>https://mail.contoso.com/unifiedmessaging/service.asmx</UMUrl>
        <OABUrl>https://mail.contoso.com/OAB/d29844a9-724e-468c-8820-0f7b345b767b/</OABUrl>
      </Protocol>
      <Protocol>
        <Type>EXPR</Type>
        <Server>Exchange.contoso.com</Server>
        <ASUrl>https://mail.contoso.com/ews/exchange.asmx</ASUrl>
        <OOFUrl>https://mail.contoso.com/ews/exchange.asmx</OOFUrl>
        <UMUrl>https://mail.contoso.com/unifiedmessaging/service.asmx</UMUrl>
        <OABUrl>https://mail.contoso.com/OAB/d29844a9-724e-468c-8820-0f7b345b767b/</OABUrl>
      </Protocol>
      <Protocol>
        <Type>WEB</Type>
        <Internal>
          <OWAUrl AuthenticationMethod="Ntlm, WindowsIntegrated">https://cas-01-server.mail.internal.contoso.com/owa</OWAUrl>
          <OWAUrl AuthenticationMethod="Ntlm, WindowsIntegrated">https://cas-02-server.mail.internal.contoso.com/owa</OWAUrl>
          <OWAUrl AuthenticationMethod="Basic">https://cas-04-server.mail.internal.contoso.com/owa</OWAUrl>
          <OWAUrl AuthenticationMethod="Ntlm, WindowsIntegrated">https://cas-05-server.mail.internal.contoso.com/owa</OWAUrl>
        </Internal>
      </Protocol>
    </Account>
  </Response>
</Autodiscover>
```

### <a name="comments"></a><span data-ttu-id="6a179-109">Comments</span><span class="sxs-lookup"><span data-stu-id="6a179-109">Comments</span></span>

<span data-ttu-id="6a179-110">Verwenden Sie zum Erstellen einer Bindung zu den Exchange-Webdiensten die vom [ASUrl (POX)](asurl-pox.md)-Element identifizierte URL.</span><span class="sxs-lookup"><span data-stu-id="6a179-110">To bind to Exchange Web Services, use the URL identified by the [ASUrl (POX)](asurl-pox.md) element.</span></span> 
  
### <a name="response-element"></a><span data-ttu-id="6a179-111">Antwortelement</span><span class="sxs-lookup"><span data-stu-id="6a179-111">Response Element</span></span>

<span data-ttu-id="6a179-112">Folgende Elemente werden im Antworttext verwendet:</span><span class="sxs-lookup"><span data-stu-id="6a179-112">The following elements are used in the response body:</span></span>
  
- [<span data-ttu-id="6a179-113">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="6a179-113">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
    
- [<span data-ttu-id="6a179-114">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="6a179-114">Response (POX)</span></span>](response-pox.md)
    
- [<span data-ttu-id="6a179-115">Benutzer (POX)</span><span class="sxs-lookup"><span data-stu-id="6a179-115">User (POX)</span></span>](user-pox.md)
    
- [<span data-ttu-id="6a179-116">DisplayName (POX)</span><span class="sxs-lookup"><span data-stu-id="6a179-116">DisplayName (POX)</span></span>](displayname-pox.md)
    
- [<span data-ttu-id="6a179-117">LegacyDN (POX)</span><span class="sxs-lookup"><span data-stu-id="6a179-117">LegacyDN (POX)</span></span>](legacydn-pox.md)
    
- [<span data-ttu-id="6a179-118">DeploymentId (POX)</span><span class="sxs-lookup"><span data-stu-id="6a179-118">DeploymentId (POX)</span></span>](deploymentid-pox.md)
    
- [<span data-ttu-id="6a179-119">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="6a179-119">Account (POX)</span></span>](account-pox.md)
    
- [<span data-ttu-id="6a179-120">AccountType (POX)</span><span class="sxs-lookup"><span data-stu-id="6a179-120">AccountType (POX)</span></span>](accounttype-pox.md)
    
- [<span data-ttu-id="6a179-121">Aktion (POX)</span><span class="sxs-lookup"><span data-stu-id="6a179-121">Action (POX)</span></span>](action-pox.md)
    
- [<span data-ttu-id="6a179-122">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="6a179-122">Protocol (POX)</span></span>](protocol-pox.md)
    
- [<span data-ttu-id="6a179-123">Typ (POX)</span><span class="sxs-lookup"><span data-stu-id="6a179-123">Type (POX)</span></span>](type-pox.md)
    
- [<span data-ttu-id="6a179-124">Server (POX)</span><span class="sxs-lookup"><span data-stu-id="6a179-124">Server (POX)</span></span>](server-pox.md)
    
- [<span data-ttu-id="6a179-125">ServerDN (POX)</span><span class="sxs-lookup"><span data-stu-id="6a179-125">ServerDN (POX)</span></span>](serverdn-pox.md)
    
- [<span data-ttu-id="6a179-126">ServerVersion (POX)</span><span class="sxs-lookup"><span data-stu-id="6a179-126">ServerVersion (POX)</span></span>](serverversion-pox.md)
    
- [<span data-ttu-id="6a179-127">MdbDN (POX)</span><span class="sxs-lookup"><span data-stu-id="6a179-127">MdbDN (POX)</span></span>](mdbdn-pox.md)
    
- [<span data-ttu-id="6a179-128">ASUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="6a179-128">ASUrl (POX)</span></span>](asurl-pox.md)
    
- [<span data-ttu-id="6a179-129">OOFUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="6a179-129">OOFUrl (POX)</span></span>](oofurl-pox.md)
    
- [<span data-ttu-id="6a179-130">UMUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="6a179-130">UMUrl (POX)</span></span>](umurl-pox.md)
    
- [<span data-ttu-id="6a179-131">OABUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="6a179-131">OABUrl (POX)</span></span>](oaburl-pox.md)
    
- [<span data-ttu-id="6a179-132">Interne (POX)</span><span class="sxs-lookup"><span data-stu-id="6a179-132">Internal (POX)</span></span>](internal-pox.md)
    
- [<span data-ttu-id="6a179-133">OWAUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="6a179-133">OWAUrl (POX)</span></span>](owaurl-pox.md)
    
## <a name="autodiscover-error-response-example"></a><span data-ttu-id="6a179-134">Autoermittlung-Fehlerantwortbeispiel</span><span class="sxs-lookup"><span data-stu-id="6a179-134">Autodiscover Error response example</span></span>

### <a name="description"></a><span data-ttu-id="6a179-135">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6a179-135">Description</span></span>

<span data-ttu-id="6a179-136">Im folgenden Beispiel ist eine Fehlerantwort für die AutoErmittlung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="6a179-136">The following example shows an Autodiscover error response.</span></span>
  
### <a name="code"></a><span data-ttu-id="6a179-137">Code</span><span class="sxs-lookup"><span data-stu-id="6a179-137">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<Autodiscover xmlns="https://schemas.microsoft.com/exchange/autodiscover/responseschema/2006">
  <Response xmlns="https://schemas.microsoft.com/exchange/autodiscover/responseschema/2006">
    <Error Time="21:25:04.8897083" Id="4130155072">
      <ErrorCode>600</ErrorCode>
      <Message>Invalid Request</Message>
      <DebugData />
    </Error>
  </Response>
</Autodiscover>
```

### <a name="error-response-element"></a><span data-ttu-id="6a179-138">Fehlerantwortelement</span><span class="sxs-lookup"><span data-stu-id="6a179-138">Error response element</span></span>

<span data-ttu-id="6a179-139">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="6a179-139">The following elements are used in the response body:</span></span>
  
- [<span data-ttu-id="6a179-140">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="6a179-140">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
    
- [<span data-ttu-id="6a179-141">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="6a179-141">Response (POX)</span></span>](response-pox.md)
    
- [<span data-ttu-id="6a179-142">Fehler (POX)</span><span class="sxs-lookup"><span data-stu-id="6a179-142">Error (POX)</span></span>](error-pox.md)
    
- [<span data-ttu-id="6a179-143">ErrorCode (POX)</span><span class="sxs-lookup"><span data-stu-id="6a179-143">ErrorCode (POX)</span></span>](errorcode-pox.md)
    
- [<span data-ttu-id="6a179-144">Nachricht (POX)</span><span class="sxs-lookup"><span data-stu-id="6a179-144">Message (POX)</span></span>](message-pox.md)
    
- [<span data-ttu-id="6a179-145">DebugData (POX)</span><span class="sxs-lookup"><span data-stu-id="6a179-145">DebugData (POX)</span></span>](debugdata-pox.md)
    
## <a name="see-also"></a><span data-ttu-id="6a179-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6a179-146">See also</span></span>

- [<span data-ttu-id="6a179-147">POX-Anforderung der AutoErmittlung für Exchange</span><span class="sxs-lookup"><span data-stu-id="6a179-147">POX Autodiscover request for Exchange</span></span>](pox-autodiscover-request-for-exchange.md)
- [<span data-ttu-id="6a179-148">Referenz zum POX-AutoErmittlungwebdienst für Exchange</span><span class="sxs-lookup"><span data-stu-id="6a179-148">POX Autodiscover web service reference for Exchange</span></span>](pox-autodiscover-web-service-reference-for-exchange.md) 
- [<span data-ttu-id="6a179-149">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="6a179-149">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

