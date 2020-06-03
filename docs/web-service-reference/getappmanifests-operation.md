---
title: GetAppManifests-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 21a4987c-c24d-4a6e-ace4-e81edcda6303
description: Hier finden Sie Informationen zum GetAppManifests-EWS-Vorgang.
ms.openlocfilehash: 4d4c1d32f14cf144335ddfdf8c9cd4c88a4421d0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463006"
---
# <a name="getappmanifests-operation"></a><span data-ttu-id="f79c8-103">GetAppManifests-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f79c8-103">GetAppManifests operation</span></span>

<span data-ttu-id="f79c8-104">Hier finden Sie Informationen zum **GetAppManifests** -EWS-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="f79c8-104">Find information about the **GetAppManifests** EWS operation.</span></span> 
  
<span data-ttu-id="f79c8-105">Der **GetAppManifests** -Vorgang ruft App-Manifeste ab.</span><span class="sxs-lookup"><span data-stu-id="f79c8-105">The **GetAppManifests** operation retrieves app manifests.</span></span> 
  
<span data-ttu-id="f79c8-106">Dieser Vorgang wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="f79c8-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getappmanifests-operation"></a><span data-ttu-id="f79c8-107">Verwenden des GetAppManifests-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="f79c8-107">Using the GetAppManifests operation</span></span>

<span data-ttu-id="f79c8-108">Der **GetAppManifests** -Vorgang benötigt keine Argumente, um die APP-Manifeste für ein Postfach anzufordern.</span><span class="sxs-lookup"><span data-stu-id="f79c8-108">The **GetAppManifests** operation does not take any arguments to request the app manifests for a mailbox.</span></span> <span data-ttu-id="f79c8-109">Die Antwort enthält Base64-codierte XML-Manifestdateien für jede APP, die in einem Postfach installiert ist.</span><span class="sxs-lookup"><span data-stu-id="f79c8-109">The response will contain base64-encoded XML manifest files for each app that is installed in a mailbox.</span></span> 
  
### <a name="getappmanifests-operation-soap-headers"></a><span data-ttu-id="f79c8-110">SOAP-Header des GetAppManifests-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="f79c8-110">GetAppManifests operation SOAP headers</span></span>

<span data-ttu-id="f79c8-111">Der **GetAppManifests** -Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="f79c8-111">The **GetAppManifests** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="f79c8-112">**Headername**</span><span class="sxs-lookup"><span data-stu-id="f79c8-112">**Header name**</span></span>|<span data-ttu-id="f79c8-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="f79c8-113">**Element**</span></span>|<span data-ttu-id="f79c8-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f79c8-114">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f79c8-115">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="f79c8-115">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="f79c8-116">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="f79c8-116">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="f79c8-117">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="f79c8-117">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="f79c8-118">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="f79c8-118">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="f79c8-119">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="f79c8-119">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="f79c8-120">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="f79c8-120">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="f79c8-121">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="f79c8-121">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="f79c8-122">Diese Kopfzeile gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="f79c8-122">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getappmanifests-operation-request-example-get-the-app-manifests-for-a-mailbox"></a><span data-ttu-id="f79c8-123">GetAppManifests-Vorgangs Anforderungs Beispiel: Abrufen der APP-Manifeste für ein Postfach</span><span class="sxs-lookup"><span data-stu-id="f79c8-123">GetAppManifests operation request example: Get the app manifests for a mailbox</span></span>

<span data-ttu-id="f79c8-124">Im folgenden Beispiel einer **GetAppManifests** -Vorgangsanforderung wird gezeigt, wie die APP-Manifeste für ein Postfach abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f79c8-124">The following example of a **GetAppManifests** operation request shows how to get the app manifests for a mailbox.</span></span> <span data-ttu-id="f79c8-125">Das [ApiVersionSupported](apiversionsupported.md) -Element und das [SchemaVersionSupported](schemaversionsupported.md) -Element sind optional.</span><span class="sxs-lookup"><span data-stu-id="f79c8-125">The [ApiVersionSupported](apiversionsupported.md) element and the [SchemaVersionSupported](schemaversionsupported.md) element are optional.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
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

<span data-ttu-id="f79c8-126">Der SOAP-Anforderungstext Körper enthält das folgende Element:</span><span class="sxs-lookup"><span data-stu-id="f79c8-126">The request SOAP body contains the following element:</span></span>
  
- [<span data-ttu-id="f79c8-127">GetAppManifests</span><span class="sxs-lookup"><span data-stu-id="f79c8-127">GetAppManifests</span></span>](getappmanifests.md)
    
- [<span data-ttu-id="f79c8-128">ApiVersionSupported</span><span class="sxs-lookup"><span data-stu-id="f79c8-128">ApiVersionSupported</span></span>](apiversionsupported.md)
    
- [<span data-ttu-id="f79c8-129">SchemaVersionSupported</span><span class="sxs-lookup"><span data-stu-id="f79c8-129">SchemaVersionSupported</span></span>](schemaversionsupported.md)
    
## <a name="successful-getappmanifests-operation-response"></a><span data-ttu-id="f79c8-130">Erfolgreiche Reaktion des GetAppManifests-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="f79c8-130">Successful GetAppManifests operation response</span></span>

<span data-ttu-id="f79c8-131">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **GetAppManifests** -Vorgangsanforderung, um die APP-Manifeste für ein Postfach abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f79c8-131">The following example shows a successful response to a **GetAppManifests** operation request to get the app manifests for a mailbox.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f79c8-132">Alle Base64-App-Manifeste wurden willkürlich abgeschnitten, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f79c8-132">All base64 app manifests have been arbitrarily truncated to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="918" 
                           MinorBuildNumber="07" 
                           Version="V2_10" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetAppManifestsResponse ResponseClass="Success" 
                               xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <m:Apps xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
          <t:App xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
            <t:Manifest>WNlQXBwPg==</t:Manifest>
          </t:App>
         </m:Apps>
      </GetAppManifestsResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="f79c8-133">Der SOAP-Antworttext Körper enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="f79c8-133">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="f79c8-134">GetAppManifestsResponse</span><span class="sxs-lookup"><span data-stu-id="f79c8-134">GetAppManifestsResponse</span></span>](getappmanifestsresponse.md)
    
- [<span data-ttu-id="f79c8-135">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="f79c8-135">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="f79c8-136">Apps</span><span class="sxs-lookup"><span data-stu-id="f79c8-136">Apps</span></span>](apps.md)
    
- [<span data-ttu-id="f79c8-137">App</span><span class="sxs-lookup"><span data-stu-id="f79c8-137">App</span></span>](app.md)
    
- [<span data-ttu-id="f79c8-138">Manifest</span><span class="sxs-lookup"><span data-stu-id="f79c8-138">Manifest</span></span>](manifest.md)
    
<span data-ttu-id="f79c8-139">Der SOAP-Antworttext Körper kann auch das folgende Element enthalten:</span><span class="sxs-lookup"><span data-stu-id="f79c8-139">The response SOAP body can also contain the following element:</span></span>
  
- [<span data-ttu-id="f79c8-140">Manifeste</span><span class="sxs-lookup"><span data-stu-id="f79c8-140">Manifests</span></span>](manifests.md)
    
## <a name="getappmanifests-operation-error-response"></a><span data-ttu-id="f79c8-141">Fehlerantwort des GetAppManifests-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="f79c8-141">GetAppManifests operation error response</span></span>

<span data-ttu-id="f79c8-142">Fehler, die für diesen Vorgang zurückgegeben werden, beziehen sich auf ein ungültiges Format der Eingabeparameter oder sind generische EWS-Fehler.</span><span class="sxs-lookup"><span data-stu-id="f79c8-142">Errors returned for this operation are related to an invalid format of the input parameters or are generic EWS errors.</span></span> <span data-ttu-id="f79c8-143">Informationen zu Fehlercodes, die für EWS allgemein und spezifisch für diesen Vorgang sind, finden Sie unter [Response Code](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="f79c8-143">For error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
```
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <ServerVersionInfo MajorVersion="15"
                       MinorVersion="0"
                       MajorBuildNumber="918"
                       MinorBuildNumber="07"
                       Version="V2_10"
                       xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetAppManifestsResponse ResponseClass="Error"
                             xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <MessageText>The apiVersionSupported parameter is invalid. 
                   It should be in the form of major version, minor 
                   version, separated by '.', for example '2.34'.</MessageText>
      <ResponseCode>ErrorInvalidRequest</ResponseCode>
      <DescriptiveLinkKey>0</DescriptiveLinkKey>
    </GetAppManifestsResponse>
  </s:Body>
</s:Envelope>

```

## <a name="see-also"></a><span data-ttu-id="f79c8-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f79c8-144">See also</span></span>

- [<span data-ttu-id="f79c8-145">EWS-Operationen in Exchange</span><span class="sxs-lookup"><span data-stu-id="f79c8-145">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="f79c8-146">DisableApp-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f79c8-146">DisableApp operation</span></span>](disableapp-operation.md)
    
- [<span data-ttu-id="f79c8-147">InstallApp-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f79c8-147">InstallApp operation</span></span>](installapp-operation.md)
    
- [<span data-ttu-id="f79c8-148">UninstallApp-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f79c8-148">UninstallApp operation</span></span>](uninstallapp-operation.md)
    
- [<span data-ttu-id="f79c8-149">GetAppMarketplaceUrl-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f79c8-149">GetAppMarketplaceUrl operation</span></span>](getappmarketplaceurl-operation.md)
    

