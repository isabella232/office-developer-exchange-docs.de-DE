---
title: GetAppManifests-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 21a4987c-c24d-4a6e-ace4-e81edcda6303
description: Hier finden Sie Informationen über die GetAppManifests EWS Vorgang.
ms.openlocfilehash: 9c919bac9ac0042890d1c439454b37e6b7c60876
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758567"
---
# <a name="getappmanifests-operation"></a><span data-ttu-id="90c20-103">GetAppManifests-Vorgang</span><span class="sxs-lookup"><span data-stu-id="90c20-103">GetAppManifests operation</span></span>

<span data-ttu-id="90c20-104">Hier finden Sie Informationen zum **GetAppManifests** EWS-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="90c20-104">Find information about the **GetAppManifests** EWS operation.</span></span> 
  
<span data-ttu-id="90c20-105">Der Vorgang **GetAppManifests** werden die app-Manifesten abgerufen.</span><span class="sxs-lookup"><span data-stu-id="90c20-105">The **GetAppManifests** operation retrieves app manifests.</span></span> 
  
<span data-ttu-id="90c20-106">Dieser Vorgang wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="90c20-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getappmanifests-operation"></a><span data-ttu-id="90c20-107">Verwenden des GetAppManifests-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="90c20-107">Using the GetAppManifests operation</span></span>

<span data-ttu-id="90c20-108">Der **GetAppManifests** -Vorgang werden keine Argumente zum Anfordern der app-Manifeste für ein Postfach verwendet.</span><span class="sxs-lookup"><span data-stu-id="90c20-108">The **GetAppManifests** operation does not take any arguments to request the app manifests for a mailbox.</span></span> <span data-ttu-id="90c20-109">Die Antwort enthält base64-codierten XML-Manifestdateien für die jeweilige app, die in einem Postfach installiert ist.</span><span class="sxs-lookup"><span data-stu-id="90c20-109">The response will contain base64-encoded XML manifest files for each app that is installed in a mailbox.</span></span> 
  
### <a name="getappmanifests-operation-soap-headers"></a><span data-ttu-id="90c20-110">GetAppManifests Vorgang SOAP-Header</span><span class="sxs-lookup"><span data-stu-id="90c20-110">GetAppManifests operation SOAP headers</span></span>

<span data-ttu-id="90c20-111">Der Vorgang **GetAppManifests** können die SOAP-Header, die in der folgenden Tabelle aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="90c20-111">The **GetAppManifests** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="90c20-112">**Headername**</span><span class="sxs-lookup"><span data-stu-id="90c20-112">**Header name**</span></span>|<span data-ttu-id="90c20-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="90c20-113">**Element**</span></span>|<span data-ttu-id="90c20-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="90c20-114">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="90c20-115">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="90c20-115">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="90c20-116">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="90c20-116">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="90c20-117">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="90c20-117">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="90c20-118">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="90c20-118">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="90c20-119">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="90c20-119">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="90c20-120">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="90c20-120">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="90c20-121">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="90c20-121">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="90c20-122">Diese Kopfzeile gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="90c20-122">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getappmanifests-operation-request-example-get-the-app-manifests-for-a-mailbox"></a><span data-ttu-id="90c20-123">GetAppManifests Vorgang-anforderungsbeispiel: Abrufen von app-Manifeste für ein Postfach</span><span class="sxs-lookup"><span data-stu-id="90c20-123">GetAppManifests operation request example: Get the app manifests for a mailbox</span></span>

<span data-ttu-id="90c20-124">Im folgenden Beispiel wird eine **GetAppManifests** Vorgang Anforderung veranschaulicht, wie die app-Manifeste für ein Postfach abgerufen.</span><span class="sxs-lookup"><span data-stu-id="90c20-124">The following example of a **GetAppManifests** operation request shows how to get the app manifests for a mailbox.</span></span> <span data-ttu-id="90c20-125">Das Element [ApiVersionSupported](apiversionsupported.md) und das [SchemaVersionSupported](schemaversionsupported.md) -Element sind optional.</span><span class="sxs-lookup"><span data-stu-id="90c20-125">The [ApiVersionSupported](apiversionsupported.md) element and the [SchemaVersionSupported](schemaversionsupported.md) element are optional.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013_SP1" />
      <t:MailboxCulture>en-US</t:MailboxCulture>
      <t:TimeZoneContext>
         <t:TimeZoneDefinition Id="GMT Standard Time"/>
      </t:TimeZoneContext>
   </soap:Header>
   <soap:Body >
      <m:GetAppManifests>
        <m:ApiVersionSupported>1.1</m:ApiVersionSupported>
        <m:SchemaVersionSupported>1.1</m:SchemaVersionSupported>
      </m:GetAppManifests>
   </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="90c20-126">Die Anforderung SOAP-Text enthält das folgende Element:</span><span class="sxs-lookup"><span data-stu-id="90c20-126">The request SOAP body contains the following element:</span></span>
  
- [<span data-ttu-id="90c20-127">GetAppManifests</span><span class="sxs-lookup"><span data-stu-id="90c20-127">GetAppManifests</span></span>](getappmanifests.md)
    
- [<span data-ttu-id="90c20-128">ApiVersionSupported</span><span class="sxs-lookup"><span data-stu-id="90c20-128">ApiVersionSupported</span></span>](apiversionsupported.md)
    
- [<span data-ttu-id="90c20-129">SchemaVersionSupported</span><span class="sxs-lookup"><span data-stu-id="90c20-129">SchemaVersionSupported</span></span>](schemaversionsupported.md)
    
## <a name="successful-getappmanifests-operation-response"></a><span data-ttu-id="90c20-130">Erfolgreiche GetAppManifests Vorgangsantwort</span><span class="sxs-lookup"><span data-stu-id="90c20-130">Successful GetAppManifests operation response</span></span>

<span data-ttu-id="90c20-131">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine Anforderung **GetAppManifests** Vorgang, um die app-Manifeste für ein Postfach abzurufen.</span><span class="sxs-lookup"><span data-stu-id="90c20-131">The following example shows a successful response to a **GetAppManifests** operation request to get the app manifests for a mailbox.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="90c20-132">Alle base64-app-Manifesten wurde willkürlich abgeschnitten, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="90c20-132">All base64 app manifests have been arbitrarily truncated to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="918" 
                           MinorBuildNumber="07" 
                           Version="V2_10" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetAppManifestsResponse ResponseClass="Success" 
                               xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <m:Apps xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
          <t:App xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
            <t:Manifest>WNlQXBwPg==</t:Manifest>
          </t:App>
         </m:Apps>
      </GetAppManifestsResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="90c20-133">Die Antwort SOAP-Text enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="90c20-133">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="90c20-134">GetAppManifestsResponse</span><span class="sxs-lookup"><span data-stu-id="90c20-134">GetAppManifestsResponse</span></span>](getappmanifestsresponse.md)
    
- [<span data-ttu-id="90c20-135">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="90c20-135">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="90c20-136">Apps</span><span class="sxs-lookup"><span data-stu-id="90c20-136">Apps</span></span>](apps.md)
    
- [<span data-ttu-id="90c20-137">App</span><span class="sxs-lookup"><span data-stu-id="90c20-137">App</span></span>](app.md)
    
- [<span data-ttu-id="90c20-138">Manifest</span><span class="sxs-lookup"><span data-stu-id="90c20-138">Manifest</span></span>](manifest.md)
    
<span data-ttu-id="90c20-139">Die Antwort SOAP-Text kann auch das folgende Element enthalten:</span><span class="sxs-lookup"><span data-stu-id="90c20-139">The response SOAP body can also contain the following element:</span></span>
  
- [<span data-ttu-id="90c20-140">Manifeste</span><span class="sxs-lookup"><span data-stu-id="90c20-140">Manifests</span></span>](manifests.md)
    
## <a name="getappmanifests-operation-error-response"></a><span data-ttu-id="90c20-141">GetAppManifests Vorgang Fehlerantwort</span><span class="sxs-lookup"><span data-stu-id="90c20-141">GetAppManifests operation error response</span></span>

<span data-ttu-id="90c20-142">Für diesen Vorgang zurückgegebenen Fehler beziehen sich auf ein ungültiges Format der Eingabeparameter oder generische EWS-Fehler sind.</span><span class="sxs-lookup"><span data-stu-id="90c20-142">Errors returned for this operation are related to an invalid format of the input parameters or are generic EWS errors.</span></span> <span data-ttu-id="90c20-143">Fehlercodes, die für EWS generisch und für diese Operation spezifisch sind, finden Sie unter [ResponseCode](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="90c20-143">For error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
```
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <ServerVersionInfo MajorVersion="15"
                       MinorVersion="0"
                       MajorBuildNumber="918"
                       MinorBuildNumber="07"
                       Version="V2_10"
                       xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetAppManifestsResponse ResponseClass="Error"
                             xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <MessageText>The apiVersionSupported parameter is invalid. 
                   It should be in the form of major version, minor 
                   version, separated by '.', for example '2.34'.</MessageText>
      <ResponseCode>ErrorInvalidRequest</ResponseCode>
      <DescriptiveLinkKey>0</DescriptiveLinkKey>
    </GetAppManifestsResponse>
  </s:Body>
</s:Envelope>

```

## <a name="see-also"></a><span data-ttu-id="90c20-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="90c20-144">See also</span></span>

- [<span data-ttu-id="90c20-145">EWS-Operationen in Exchange</span><span class="sxs-lookup"><span data-stu-id="90c20-145">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="90c20-146">DisableApp-Vorgang</span><span class="sxs-lookup"><span data-stu-id="90c20-146">DisableApp operation</span></span>](disableapp-operation.md)
    
- [<span data-ttu-id="90c20-147">InstallApp-Vorgang</span><span class="sxs-lookup"><span data-stu-id="90c20-147">InstallApp operation</span></span>](installapp-operation.md)
    
- [<span data-ttu-id="90c20-148">UninstallApp-Vorgang</span><span class="sxs-lookup"><span data-stu-id="90c20-148">UninstallApp operation</span></span>](uninstallapp-operation.md)
    
- [<span data-ttu-id="90c20-149">GetAppMarketplaceUrl-Vorgang</span><span class="sxs-lookup"><span data-stu-id="90c20-149">GetAppMarketplaceUrl operation</span></span>](getappmarketplaceurl-operation.md)
    

