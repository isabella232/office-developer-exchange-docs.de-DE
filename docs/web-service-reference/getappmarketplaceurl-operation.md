---
title: GetAppMarketplaceUrl-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2c016fc3-0e13-4624-9a5b-d3e84577a860
description: Hier finden Sie Informationen über die GetAppMarketplaceUrl EWS Vorgang.
ms.openlocfilehash: 616e7f571ba5283a773e51d611cd18bb37b5bc8b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758573"
---
# <a name="getappmarketplaceurl-operation"></a><span data-ttu-id="3ee67-103">GetAppMarketplaceUrl-Vorgang</span><span class="sxs-lookup"><span data-stu-id="3ee67-103">GetAppMarketplaceUrl operation</span></span>

<span data-ttu-id="3ee67-104">Hier finden Sie Informationen zum **GetAppMarketplaceUrl** EWS-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="3ee67-104">Find information about the **GetAppMarketplaceUrl** EWS operation.</span></span> 
  
<span data-ttu-id="3ee67-105">Der Vorgang **GetAppMarketplaceUrl** Ruft die URL für den app-Marketplace, den ein Client besuchen dürfen, zum Erwerben von apps in einem Postfach zu installieren.</span><span class="sxs-lookup"><span data-stu-id="3ee67-105">The **GetAppMarketplaceUrl** operation retrieves the URL for the app marketplace that a client can visit to acquire apps to install in a mailbox.</span></span> 
  
<span data-ttu-id="3ee67-106">Dieser Vorgang wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="3ee67-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getappmarketplaceurl-operation"></a><span data-ttu-id="3ee67-107">Verwenden des GetAppMarketplaceUrl-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="3ee67-107">Using the GetAppMarketplaceUrl operation</span></span>

<span data-ttu-id="3ee67-108">Der Vorgang **GetAppMarketplaceUrl** ist keine Argumente So fordern Sie die URL für den Marketplace an, von dem ein Client-apps installieren kann.</span><span class="sxs-lookup"><span data-stu-id="3ee67-108">The **GetAppMarketplaceUrl** operation does not take any arguments to request the URL for the marketplace from which a client can install apps.</span></span> <span data-ttu-id="3ee67-109">Die Antwort enthält eine URL zu den app-Marketplace.</span><span class="sxs-lookup"><span data-stu-id="3ee67-109">The response will contain a URL to the app marketplace.</span></span> 
  
### <a name="getappmarketplaceurl-operation-soap-headers"></a><span data-ttu-id="3ee67-110">GetAppMarketplaceUrl Vorgang SOAP-Header</span><span class="sxs-lookup"><span data-stu-id="3ee67-110">GetAppMarketplaceUrl operation SOAP headers</span></span>

<span data-ttu-id="3ee67-111">Der Vorgang **GetAppMarketplaceUrl** können die SOAP-Header, die in der folgenden Tabelle aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="3ee67-111">The **GetAppMarketplaceUrl** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="3ee67-112">**Headername**</span><span class="sxs-lookup"><span data-stu-id="3ee67-112">**Header name**</span></span>|<span data-ttu-id="3ee67-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="3ee67-113">**Element**</span></span>|<span data-ttu-id="3ee67-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3ee67-114">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3ee67-115">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="3ee67-115">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="3ee67-116">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="3ee67-116">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="3ee67-117">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="3ee67-117">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="3ee67-118">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="3ee67-118">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="3ee67-119">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="3ee67-119">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="3ee67-120">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="3ee67-120">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="3ee67-121">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="3ee67-121">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="3ee67-122">Diese Kopfzeile gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="3ee67-122">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getappmarketplaceurl-operation-request-example-get-the-app-marketplace-url-for-a-mailbox"></a><span data-ttu-id="3ee67-123">GetAppMarketplaceUrl Vorgang-anforderungsbeispiel: Abrufen die app Marketplace-URL für ein Postfach</span><span class="sxs-lookup"><span data-stu-id="3ee67-123">GetAppMarketplaceUrl operation request example: Get the app marketplace URL for a mailbox</span></span>

<span data-ttu-id="3ee67-124">Im folgenden Beispiel wird eine **GetAppMarketplaceUrl** Vorgang Anforderung veranschaulicht die app Marketplace-URL für ein Postfach abzurufen.</span><span class="sxs-lookup"><span data-stu-id="3ee67-124">The following example of a **GetAppMarketplaceUrl** operation request shows how to get the app marketplace URL for a mailbox.</span></span> 
  
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
      <m:GetAppMarketplaceUrl>
        <m:ApiVersionSupported>1.0</m:ApiVersionSupported>
        <m:SchemaVersionSupported>1.0</m:SchemaVersionSupported>
      </m:GetAppMarketplaceUrl>
   </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="3ee67-125">Die Anforderung SOAP-Text enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="3ee67-125">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="3ee67-126">GetAppMarketplaceUrl</span><span class="sxs-lookup"><span data-stu-id="3ee67-126">GetAppMarketplaceUrl</span></span>](getappmarketplaceurl.md)
    
- [<span data-ttu-id="3ee67-127">ApiVersionSupported</span><span class="sxs-lookup"><span data-stu-id="3ee67-127">ApiVersionSupported</span></span>](apiversionsupported.md)
    
- [<span data-ttu-id="3ee67-128">SchemaVersionSupported</span><span class="sxs-lookup"><span data-stu-id="3ee67-128">SchemaVersionSupported</span></span>](schemaversionsupported.md)
    
## <a name="successful-getappmarketplaceurl-operation-response"></a><span data-ttu-id="3ee67-129">Erfolgreiche GetAppMarketplaceUrl Vorgangsantwort</span><span class="sxs-lookup"><span data-stu-id="3ee67-129">Successful GetAppMarketplaceUrl operation response</span></span>

<span data-ttu-id="3ee67-130">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine Anforderung **GetAppMarketplaceUrl** Vorgang, um die app Marketplace-URL für ein Postfach abzurufen.</span><span class="sxs-lookup"><span data-stu-id="3ee67-130">The following example shows a successful response to a **GetAppMarketplaceUrl** operation request to get the app marketplace URL for a mailbox.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="3ee67-131">Die URL der app-Marketplace wurde geändert, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="3ee67-131">The app marketplace URL has been altered to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="918" 
                           MinorBuildNumber="7" 
                           Version="V2_10" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetAppMarketplaceUrlResponse ResponseClass="Success" 
                                    xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <AppMarketplaceUrl>http://marketplace.contoso.com</AppMarketplaceUrl>
      </GetAppMarketplaceUrlResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="3ee67-132">Die Antwort SOAP-Text enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="3ee67-132">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="3ee67-133">GetAppMarketplaceUrlResponse</span><span class="sxs-lookup"><span data-stu-id="3ee67-133">GetAppMarketplaceUrlResponse</span></span>](getappmarketplaceurlresponse.md)
    
- [<span data-ttu-id="3ee67-134">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="3ee67-134">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="3ee67-135">AppMarketplaceUrl</span><span class="sxs-lookup"><span data-stu-id="3ee67-135">AppMarketplaceUrl</span></span>](appmarketplaceurl.md)
    
## <a name="getappmarketplaceurl-operation-error-response"></a><span data-ttu-id="3ee67-136">GetAppMarketPlaceUrl Vorgang Fehlerantwort</span><span class="sxs-lookup"><span data-stu-id="3ee67-136">GetAppMarketPlaceUrl operation error response</span></span>

<span data-ttu-id="3ee67-137">Fehler, die für diesen Vorgang zurückgegeben werden entweder im Zusammenhang mit der eine falsche Konfiguration oder generische EWS-Fehler sind.</span><span class="sxs-lookup"><span data-stu-id="3ee67-137">Errors returned for this operation are either related to an incorrect service configuration or are generic EWS errors.</span></span> <span data-ttu-id="3ee67-138">Fehlercodes, die für EWS generisch und für diese Operation spezifisch sind, finden Sie unter [ResponseCode](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="3ee67-138">For error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span> 
  
<span data-ttu-id="3ee67-139">Das folgende Beispiel zeigt eine Fehlerantwort an, die zurückgegeben wird, wenn externe Exchange Steuerelement Systemsteuerung nicht konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="3ee67-139">The following example shows an error response that is returned when external Exchange Control Panel (ECP) is not configured.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="918" 
                           MinorBuildNumber="7" 
                           Version="V2_10" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetAppMarketplaceUrlResponse ResponseClass="Error" 
                                    xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>Cannot get external ECP URL. This might happen if external ECP URL isn't configured.</MessageText>
         <ResponseCode>ErrorCannotGetExternalEcpUrl</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </GetAppMarketplaceUrlResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="3ee67-140">Die SOAP-Body-Fehlerantwort enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="3ee67-140">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="3ee67-141">GetAppMarketplaceUrlResponse</span><span class="sxs-lookup"><span data-stu-id="3ee67-141">GetAppMarketplaceUrlResponse</span></span>](getappmarketplaceurlresponse.md)
    
- [<span data-ttu-id="3ee67-142">MessageText</span><span class="sxs-lookup"><span data-stu-id="3ee67-142">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="3ee67-143">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="3ee67-143">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="3ee67-144">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="3ee67-144">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="3ee67-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3ee67-145">See also</span></span>

- [<span data-ttu-id="3ee67-146">EWS-Operationen in Exchange</span><span class="sxs-lookup"><span data-stu-id="3ee67-146">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="3ee67-147">DisableApp-Vorgang</span><span class="sxs-lookup"><span data-stu-id="3ee67-147">DisableApp operation</span></span>](disableapp-operation.md)
    
- [<span data-ttu-id="3ee67-148">InstallApp-Vorgang</span><span class="sxs-lookup"><span data-stu-id="3ee67-148">InstallApp operation</span></span>](installapp-operation.md)
    
- [<span data-ttu-id="3ee67-149">UninstallApp-Vorgang</span><span class="sxs-lookup"><span data-stu-id="3ee67-149">UninstallApp operation</span></span>](uninstallapp-operation.md)
    
- [<span data-ttu-id="3ee67-150">GetAppManifests-Vorgang</span><span class="sxs-lookup"><span data-stu-id="3ee67-150">GetAppManifests operation</span></span>](getappmanifests-operation.md)
    

