---
title: UninstallApp-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7707aa6a-381d-43f7-a454-54f6343ed127
description: Hier finden Sie Informationen zum UninstallApp-EWS-Vorgang.
ms.openlocfilehash: 27931636ee13a251fb03fe804987d7b01a325230
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467151"
---
# <a name="uninstallapp-operation"></a><span data-ttu-id="d80ad-103">UninstallApp-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d80ad-103">UninstallApp operation</span></span>

<span data-ttu-id="d80ad-104">Hier finden Sie Informationen zum **UninstallApp** -EWS-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="d80ad-104">Find information about the **UninstallApp** EWS operation.</span></span> 
  
<span data-ttu-id="d80ad-105">Der **UninstallApp** -Vorgang deinstalliert eine Mail-App für Outlook.</span><span class="sxs-lookup"><span data-stu-id="d80ad-105">The **UninstallApp** operation uninstalls a mail app for Outlook.</span></span> 
  
<span data-ttu-id="d80ad-106">Dieser Vorgang wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d80ad-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-uninstallapp-operation"></a><span data-ttu-id="d80ad-107">Verwenden des UninstallApp-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="d80ad-107">Using the UninstallApp operation</span></span>

<span data-ttu-id="d80ad-108">Der **UninstallApp** -Vorgang verwendet ein Argument in der Anforderung, das die zu deinstallierende Mail-App identifiziert.</span><span class="sxs-lookup"><span data-stu-id="d80ad-108">The **UninstallApp** operation takes one argument in the request that identifies the mail app to uninstall.</span></span> 
  
### <a name="uninstallapp-operation-soap-headers"></a><span data-ttu-id="d80ad-109">SOAP-Header des UninstallApp-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="d80ad-109">UninstallApp operation SOAP headers</span></span>

<span data-ttu-id="d80ad-110">Der **UninstallApp** -Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="d80ad-110">The **UninstallApp** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="d80ad-111">**Headername**</span><span class="sxs-lookup"><span data-stu-id="d80ad-111">**Header name**</span></span>|<span data-ttu-id="d80ad-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="d80ad-112">**Element**</span></span>|<span data-ttu-id="d80ad-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d80ad-113">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d80ad-114">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="d80ad-114">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="d80ad-115">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="d80ad-115">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="d80ad-116">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="d80ad-116">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="d80ad-117">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="d80ad-117">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="d80ad-118">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="d80ad-118">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="d80ad-119">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="d80ad-119">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="d80ad-120">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="d80ad-120">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="d80ad-121">Diese Kopfzeile gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="d80ad-121">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="uninstallapp-operation-request-example-uninstall-a-mail-app-in-a-mailbox"></a><span data-ttu-id="d80ad-122">UninstallApp-Vorgangs Anforderungs Beispiel: Deinstallieren einer Mail-app in einem Postfach</span><span class="sxs-lookup"><span data-stu-id="d80ad-122">UninstallApp operation request example: Uninstall a mail app in a mailbox</span></span>

<span data-ttu-id="d80ad-123">Im folgenden Beispiel einer **UninstallApp** -Vorgangsanforderung wird gezeigt, wie eine Mail-App mithilfe der APP-ID deinstalliert werden kann.</span><span class="sxs-lookup"><span data-stu-id="d80ad-123">The following example of an **UninstallApp** operation request shows how to a uninstall a mail app by using the app identifier.</span></span> <span data-ttu-id="d80ad-124">Der APP-Bezeichner befindet sich im App-Manifest, das von der [GetAppManifests-Operation](getappmanifests-operation.md)zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d80ad-124">The app identifier can be found in the app manifest that is returned by the [GetAppManifests operation](getappmanifests-operation.md).</span></span>
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:UninstallApp>
         <m:ID>1C50226D-04B5-4AB2-9FCD-42E236B59E4B</m:ID>
      </m:UninstallApp>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="d80ad-125">Der SOAP-Anforderungstext Körper enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="d80ad-125">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="d80ad-126">UninstallApp</span><span class="sxs-lookup"><span data-stu-id="d80ad-126">UninstallApp</span></span>](uninstallapp.md)
    
- [<span data-ttu-id="d80ad-127">ID (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="d80ad-127">ID (String)</span></span>](id-string.md)
    
## <a name="successful-uninstallapp-operation-response"></a><span data-ttu-id="d80ad-128">Erfolgreiche Reaktion des UninstallApp-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="d80ad-128">Successful UninstallApp operation response</span></span>

<span data-ttu-id="d80ad-129">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **UninstallApp** -Vorgangsanforderung zum Deinstallieren einer Mail-app.</span><span class="sxs-lookup"><span data-stu-id="d80ad-129">The following example shows a successful response to an **UninstallApp** operation request to uninstall a mail app.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="14" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <UninstallAppResponse ResponseClass="Success" 
                            xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
      </UninstallAppResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="d80ad-130">Der SOAP-Antworttext Körper enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="d80ad-130">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="d80ad-131">UninstallAppResponse</span><span class="sxs-lookup"><span data-stu-id="d80ad-131">UninstallAppResponse</span></span>](uninstallappresponse.md)
    
- [<span data-ttu-id="d80ad-132">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="d80ad-132">ResponseCode</span></span>](responsecode.md)
    
## <a name="uninstallapp-operation-error-response"></a><span data-ttu-id="d80ad-133">Fehlerantwort des UninstallApp-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="d80ad-133">UninstallApp operation error response</span></span>

<span data-ttu-id="d80ad-134">Das folgende Beispiel zeigt eine Fehlerantwort auf eine **UninstallApp** -Vorgangsanforderung.</span><span class="sxs-lookup"><span data-stu-id="d80ad-134">The following example shows an error response to an **UninstallApp** operation request.</span></span> <span data-ttu-id="d80ad-135">Dies ist eine Antwort auf eine Anforderung zum Deinstallieren einer Mail-APP, die bereits deinstalliert wurde.</span><span class="sxs-lookup"><span data-stu-id="d80ad-135">This is a response to a request to uninstall a mail app that has already been uninstalled.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="14" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <UninstallAppResponse ResponseClass="Error" 
                            xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>Extension ID 1c50226d-04b5-4ab2-9fcd-42e236b59e4b can't be found.</MessageText>
         <ResponseCode>ErrorInternalServerError</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </UninstallAppResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="d80ad-136">Der SOAP-Textkörper der Fehlerantwort enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="d80ad-136">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="d80ad-137">UninstallAppResponse</span><span class="sxs-lookup"><span data-stu-id="d80ad-137">UninstallAppResponse</span></span>](uninstallappresponse.md)
    
- [<span data-ttu-id="d80ad-138">MessageText</span><span class="sxs-lookup"><span data-stu-id="d80ad-138">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="d80ad-139">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="d80ad-139">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="d80ad-140">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="d80ad-140">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="d80ad-141">Weitere Fehlercodes, die für EWS allgemein und spezifisch für diesen Vorgang sind, finden Sie unter [Response Code](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="d80ad-141">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d80ad-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d80ad-142">See also</span></span>

- [<span data-ttu-id="d80ad-143">EWS-Operationen in Exchange</span><span class="sxs-lookup"><span data-stu-id="d80ad-143">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="d80ad-144">InstallApp-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d80ad-144">InstallApp operation</span></span>](installapp-operation.md)
    
- [<span data-ttu-id="d80ad-145">DisableApp-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d80ad-145">DisableApp operation</span></span>](disableapp-operation.md)
    
- [<span data-ttu-id="d80ad-146">GetAppManifests</span><span class="sxs-lookup"><span data-stu-id="d80ad-146">GetAppManifests</span></span>](getappmanifests.md)
    
- [<span data-ttu-id="d80ad-147">GetAppMarketplaceUrl-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d80ad-147">GetAppMarketplaceUrl operation</span></span>](getappmarketplaceurl-operation.md)
    

