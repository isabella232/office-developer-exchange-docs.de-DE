---
title: GetAppMarketplaceUrl-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2c016fc3-0e13-4624-9a5b-d3e84577a860
description: Hier finden Sie Informationen zum GetAppMarketplaceUrl-EWS-Vorgang.
ms.openlocfilehash: 6797af44c3aaa6653c440b3d53a282d8c90a4381
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459525"
---
# <a name="getappmarketplaceurl-operation"></a><span data-ttu-id="abed0-103">GetAppMarketplaceUrl-Vorgang</span><span class="sxs-lookup"><span data-stu-id="abed0-103">GetAppMarketplaceUrl operation</span></span>

<span data-ttu-id="abed0-104">Hier finden Sie Informationen zum **GetAppMarketplaceUrl** -EWS-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="abed0-104">Find information about the **GetAppMarketplaceUrl** EWS operation.</span></span> 
  
<span data-ttu-id="abed0-105">Der **GetAppMarketplaceUrl** -Vorgang ruft die URL für den App-Marketplace ab, den ein Client besuchen kann, um apps zu erwerben, die in einem Postfach installiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="abed0-105">The **GetAppMarketplaceUrl** operation retrieves the URL for the app marketplace that a client can visit to acquire apps to install in a mailbox.</span></span> 
  
<span data-ttu-id="abed0-106">Dieser Vorgang wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="abed0-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getappmarketplaceurl-operation"></a><span data-ttu-id="abed0-107">Verwenden des GetAppMarketplaceUrl-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="abed0-107">Using the GetAppMarketplaceUrl operation</span></span>

<span data-ttu-id="abed0-108">Für den **GetAppMarketplaceUrl** -Vorgang werden keine Argumente benötigt, um die URL für den Marketplace anzufordern, von dem ein Client apps installieren kann.</span><span class="sxs-lookup"><span data-stu-id="abed0-108">The **GetAppMarketplaceUrl** operation does not take any arguments to request the URL for the marketplace from which a client can install apps.</span></span> <span data-ttu-id="abed0-109">Die Antwort wird eine URL zum App-Marketplace enthalten.</span><span class="sxs-lookup"><span data-stu-id="abed0-109">The response will contain a URL to the app marketplace.</span></span> 
  
### <a name="getappmarketplaceurl-operation-soap-headers"></a><span data-ttu-id="abed0-110">SOAP-Header des GetAppMarketplaceUrl-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="abed0-110">GetAppMarketplaceUrl operation SOAP headers</span></span>

<span data-ttu-id="abed0-111">Der **GetAppMarketplaceUrl** -Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="abed0-111">The **GetAppMarketplaceUrl** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="abed0-112">**Headername**</span><span class="sxs-lookup"><span data-stu-id="abed0-112">**Header name**</span></span>|<span data-ttu-id="abed0-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="abed0-113">**Element**</span></span>|<span data-ttu-id="abed0-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="abed0-114">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="abed0-115">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="abed0-115">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="abed0-116">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="abed0-116">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="abed0-117">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="abed0-117">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="abed0-118">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="abed0-118">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="abed0-119">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="abed0-119">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="abed0-120">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="abed0-120">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="abed0-121">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="abed0-121">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="abed0-122">Diese Kopfzeile gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="abed0-122">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getappmarketplaceurl-operation-request-example-get-the-app-marketplace-url-for-a-mailbox"></a><span data-ttu-id="abed0-123">GetAppMarketplaceUrl-Vorgangs Anforderungs Beispiel: Abrufen der URL des App-Marketplace für ein Postfach</span><span class="sxs-lookup"><span data-stu-id="abed0-123">GetAppMarketplaceUrl operation request example: Get the app marketplace URL for a mailbox</span></span>

<span data-ttu-id="abed0-124">Im folgenden Beispiel einer **GetAppMarketplaceUrl** -Vorgangsanforderung wird gezeigt, wie die APP Marketplace-URL für ein Postfach abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="abed0-124">The following example of a **GetAppMarketplaceUrl** operation request shows how to get the app marketplace URL for a mailbox.</span></span> 
  
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
      <m:GetAppMarketplaceUrl>
        <m:ApiVersionSupported>1.0</m:ApiVersionSupported>
        <m:SchemaVersionSupported>1.0</m:SchemaVersionSupported>
      </m:GetAppMarketplaceUrl>
   </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="abed0-125">Der SOAP-Anforderungstext Körper enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="abed0-125">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="abed0-126">GetAppMarketplaceUrl</span><span class="sxs-lookup"><span data-stu-id="abed0-126">GetAppMarketplaceUrl</span></span>](getappmarketplaceurl.md)
    
- [<span data-ttu-id="abed0-127">ApiVersionSupported</span><span class="sxs-lookup"><span data-stu-id="abed0-127">ApiVersionSupported</span></span>](apiversionsupported.md)
    
- [<span data-ttu-id="abed0-128">SchemaVersionSupported</span><span class="sxs-lookup"><span data-stu-id="abed0-128">SchemaVersionSupported</span></span>](schemaversionsupported.md)
    
## <a name="successful-getappmarketplaceurl-operation-response"></a><span data-ttu-id="abed0-129">Erfolgreiche Reaktion des GetAppMarketplaceUrl-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="abed0-129">Successful GetAppMarketplaceUrl operation response</span></span>

<span data-ttu-id="abed0-130">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **GetAppMarketplaceUrl** -Vorgangsanforderung, um die APP Marketplace-URL für ein Postfach abzurufen.</span><span class="sxs-lookup"><span data-stu-id="abed0-130">The following example shows a successful response to a **GetAppMarketplaceUrl** operation request to get the app marketplace URL for a mailbox.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="abed0-131">Die URL des App-Marktplatzes wurde geändert, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="abed0-131">The app marketplace URL has been altered to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="918" 
                           MinorBuildNumber="7" 
                           Version="V2_10" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetAppMarketplaceUrlResponse ResponseClass="Success" 
                                    xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <AppMarketplaceUrl>http://marketplace.contoso.com</AppMarketplaceUrl>
      </GetAppMarketplaceUrlResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="abed0-132">Der SOAP-Antworttext Körper enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="abed0-132">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="abed0-133">GetAppMarketplaceUrlResponse</span><span class="sxs-lookup"><span data-stu-id="abed0-133">GetAppMarketplaceUrlResponse</span></span>](getappmarketplaceurlresponse.md)
    
- [<span data-ttu-id="abed0-134">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="abed0-134">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="abed0-135">AppMarketplaceUrl</span><span class="sxs-lookup"><span data-stu-id="abed0-135">AppMarketplaceUrl</span></span>](appmarketplaceurl.md)
    
## <a name="getappmarketplaceurl-operation-error-response"></a><span data-ttu-id="abed0-136">Fehlerantwort des GetAppMarketPlaceUrl-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="abed0-136">GetAppMarketPlaceUrl operation error response</span></span>

<span data-ttu-id="abed0-137">Fehler, die für diesen Vorgang zurückgegeben werden, beziehen sich entweder auf eine falsche Dienstkonfiguration oder sind generische EWS-Fehler.</span><span class="sxs-lookup"><span data-stu-id="abed0-137">Errors returned for this operation are either related to an incorrect service configuration or are generic EWS errors.</span></span> <span data-ttu-id="abed0-138">Informationen zu Fehlercodes, die für EWS allgemein und spezifisch für diesen Vorgang sind, finden Sie unter [Response Code](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="abed0-138">For error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span> 
  
<span data-ttu-id="abed0-139">Das folgende Beispiel zeigt eine Fehlerantwort, die zurückgegeben wird, wenn die externe Exchange-Systemsteuerung (ECP) nicht konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="abed0-139">The following example shows an error response that is returned when external Exchange Control Panel (ECP) is not configured.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="918" 
                           MinorBuildNumber="7" 
                           Version="V2_10" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetAppMarketplaceUrlResponse ResponseClass="Error" 
                                    xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>Cannot get external ECP URL. This might happen if external ECP URL isn't configured.</MessageText>
         <ResponseCode>ErrorCannotGetExternalEcpUrl</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </GetAppMarketplaceUrlResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="abed0-140">Der SOAP-Textkörper der Fehlerantwort enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="abed0-140">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="abed0-141">GetAppMarketplaceUrlResponse</span><span class="sxs-lookup"><span data-stu-id="abed0-141">GetAppMarketplaceUrlResponse</span></span>](getappmarketplaceurlresponse.md)
    
- [<span data-ttu-id="abed0-142">MessageText</span><span class="sxs-lookup"><span data-stu-id="abed0-142">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="abed0-143">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="abed0-143">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="abed0-144">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="abed0-144">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="abed0-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="abed0-145">See also</span></span>

- [<span data-ttu-id="abed0-146">EWS-Operationen in Exchange</span><span class="sxs-lookup"><span data-stu-id="abed0-146">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="abed0-147">DisableApp-Vorgang</span><span class="sxs-lookup"><span data-stu-id="abed0-147">DisableApp operation</span></span>](disableapp-operation.md)
    
- [<span data-ttu-id="abed0-148">InstallApp-Vorgang</span><span class="sxs-lookup"><span data-stu-id="abed0-148">InstallApp operation</span></span>](installapp-operation.md)
    
- [<span data-ttu-id="abed0-149">UninstallApp-Vorgang</span><span class="sxs-lookup"><span data-stu-id="abed0-149">UninstallApp operation</span></span>](uninstallapp-operation.md)
    
- [<span data-ttu-id="abed0-150">GetAppManifests-Vorgang</span><span class="sxs-lookup"><span data-stu-id="abed0-150">GetAppManifests operation</span></span>](getappmanifests-operation.md)
    

