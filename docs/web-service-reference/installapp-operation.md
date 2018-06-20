---
title: InstallApp-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 596eae95-3e78-489a-8bb2-d2dd4a026405
description: Hier finden Sie Informationen über die InstallApp EWS Vorgang.
ms.openlocfilehash: ccc5d2dde949070bae905ff1ebb182c892f07fcb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19829951"
---
# <a name="installapp-operation"></a><span data-ttu-id="5b7e7-103">InstallApp-Vorgang</span><span class="sxs-lookup"><span data-stu-id="5b7e7-103">InstallApp operation</span></span>

<span data-ttu-id="5b7e7-104">Hier finden Sie Informationen zum **InstallApp** EWS-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="5b7e7-104">Find information about the **InstallApp** EWS operation.</span></span> 
  
<span data-ttu-id="5b7e7-105">Der Vorgang **InstallApp** Installation eine Mail-app für Outlook in einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="5b7e7-105">The **InstallApp** operation installs a mail app for Outlook in a mailbox.</span></span> 
  
<span data-ttu-id="5b7e7-106">Dieser Vorgang wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="5b7e7-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-installapp-operation"></a><span data-ttu-id="5b7e7-107">Verwenden des InstallApp-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="5b7e7-107">Using the InstallApp operation</span></span>

<span data-ttu-id="5b7e7-108">Der Vorgang **InstallApp** erhält ein einzelnes Argument, das zum Installieren eine Mail-app identifiziert.</span><span class="sxs-lookup"><span data-stu-id="5b7e7-108">The **InstallApp** operation takes a single argument that identifies a mail app to install.</span></span> <span data-ttu-id="5b7e7-109">Das Argument enthält das base64-codierten Manifest für eine Mail-app.</span><span class="sxs-lookup"><span data-stu-id="5b7e7-109">The argument contains the base64-encoded manifest for a mail app.</span></span> 
  
### <a name="installapp-operation-soap-headers"></a><span data-ttu-id="5b7e7-110">InstallApp Vorgang SOAP-Header</span><span class="sxs-lookup"><span data-stu-id="5b7e7-110">InstallApp operation SOAP headers</span></span>

<span data-ttu-id="5b7e7-111">Der Vorgang **InstallApp** können die SOAP-Header, die in der folgenden Tabelle aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="5b7e7-111">The **InstallApp** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="5b7e7-112">**Headername**</span><span class="sxs-lookup"><span data-stu-id="5b7e7-112">**Header name**</span></span>|<span data-ttu-id="5b7e7-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="5b7e7-113">**Element**</span></span>|<span data-ttu-id="5b7e7-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5b7e7-114">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5b7e7-115">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="5b7e7-115">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="5b7e7-116">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="5b7e7-116">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="5b7e7-117">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="5b7e7-117">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="5b7e7-118">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="5b7e7-118">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="5b7e7-119">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="5b7e7-119">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="5b7e7-120">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="5b7e7-120">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="5b7e7-121">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="5b7e7-121">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="5b7e7-122">Diese Kopfzeile gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="5b7e7-122">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="installapp-operation-request-example-install-a-mail-app-in-a-mailbox"></a><span data-ttu-id="5b7e7-123">InstallApp Vorgang-anforderungsbeispiel: installieren eine Mail-app in einem Postfach</span><span class="sxs-lookup"><span data-stu-id="5b7e7-123">InstallApp operation request example: Install a mail app in a mailbox</span></span>

<span data-ttu-id="5b7e7-124">Im folgenden Beispiel wird ein **InstallApp** Vorgang Anforderung veranschaulicht, wie eine Mail-app für Outlook zu installieren.</span><span class="sxs-lookup"><span data-stu-id="5b7e7-124">The following example of an **InstallApp** operation request shows how to install a mail app for Outlook.</span></span> <span data-ttu-id="5b7e7-125">App-Manifest kann mit der [GetAppManifests Vorgang](getappmanifests-operation.md)gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="5b7e7-125">The app manifest can be found by using the [GetAppManifests operation](getappmanifests-operation.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="5b7e7-126">Base64-codierten app-Manifest wurde willkürlich um Erhaltung der Lesbarkeit abgeschnitten und ein gültiges Manifest nicht darstellt.</span><span class="sxs-lookup"><span data-stu-id="5b7e7-126">The base64-encoded app manifest has been arbitrarily truncated to preserve readability and does not represent a valid manifest.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:InstallApp>
         <m:Manifest>TUwiIC8+CiAgPC9SdWxlPgo8L09mZmljZUFwcD4=</m:Manifest>
      </m:InstallApp>
   </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="5b7e7-127">Die Anforderung SOAP-Text enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="5b7e7-127">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="5b7e7-128">InstallApp</span><span class="sxs-lookup"><span data-stu-id="5b7e7-128">InstallApp</span></span>](installapp.md)
    
- [<span data-ttu-id="5b7e7-129">Manifest</span><span class="sxs-lookup"><span data-stu-id="5b7e7-129">Manifest</span></span>](manifest.md)
    
## <a name="successful-installapp-operation-response"></a><span data-ttu-id="5b7e7-130">Erfolgreiche InstallApp Vorgangsantwort</span><span class="sxs-lookup"><span data-stu-id="5b7e7-130">Successful InstallApp operation response</span></span>

<span data-ttu-id="5b7e7-131">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine Anforderung **InstallApp** Vorgang, um eine Mail-app zu installieren.</span><span class="sxs-lookup"><span data-stu-id="5b7e7-131">The following example shows a successful response to an **InstallApp** operation request to install a mail app.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="14" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <InstallAppResponse ResponseClass="Success" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
      </InstallAppResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="5b7e7-132">Die Antwort SOAP-Text enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="5b7e7-132">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="5b7e7-133">InstallAppResponse</span><span class="sxs-lookup"><span data-stu-id="5b7e7-133">InstallAppResponse</span></span>](installappresponse.md)
    
- [<span data-ttu-id="5b7e7-134">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="5b7e7-134">ResponseCode</span></span>](responsecode.md)
    
## <a name="installapp-operation-error-response"></a><span data-ttu-id="5b7e7-135">InstallApp Vorgang Fehlerantwort</span><span class="sxs-lookup"><span data-stu-id="5b7e7-135">InstallApp operation error response</span></span>

<span data-ttu-id="5b7e7-136">Das folgende Beispiel zeigt eine Fehlerantwort an eine **InstallApp** Vorgang Anforderung.</span><span class="sxs-lookup"><span data-stu-id="5b7e7-136">The following example shows an error response to an **InstallApp** operation request.</span></span> <span data-ttu-id="5b7e7-137">Dies ist eine Antwort auf eine Anforderung, die eine ungültige Manifestdatei enthält.</span><span class="sxs-lookup"><span data-stu-id="5b7e7-137">This is a response to a request that contains an invalid manifest.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="14" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <InstallAppResponse ResponseClass="Error" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>This app can't be installed. Missing OfficeApp element.</MessageText>
         <ResponseCode>ErrorInternalServerError</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </InstallAppResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="5b7e7-138">Die SOAP-Body-Fehlerantwort enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="5b7e7-138">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="5b7e7-139">InstallAppResponse</span><span class="sxs-lookup"><span data-stu-id="5b7e7-139">InstallAppResponse</span></span>](installappresponse.md)
    
- [<span data-ttu-id="5b7e7-140">MessageText</span><span class="sxs-lookup"><span data-stu-id="5b7e7-140">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="5b7e7-141">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="5b7e7-141">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="5b7e7-142">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="5b7e7-142">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="5b7e7-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5b7e7-143">See also</span></span>

- [<span data-ttu-id="5b7e7-144">EWS-Operationen in Exchange</span><span class="sxs-lookup"><span data-stu-id="5b7e7-144">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="5b7e7-145">DisableApp-Vorgang</span><span class="sxs-lookup"><span data-stu-id="5b7e7-145">DisableApp operation</span></span>](disableapp-operation.md)
    
- [<span data-ttu-id="5b7e7-146">UninstallApp-Vorgang</span><span class="sxs-lookup"><span data-stu-id="5b7e7-146">UninstallApp operation</span></span>](uninstallapp-operation.md)
    
- [<span data-ttu-id="5b7e7-147">GetAppManifests</span><span class="sxs-lookup"><span data-stu-id="5b7e7-147">GetAppManifests</span></span>](getappmanifests.md)
    
- [<span data-ttu-id="5b7e7-148">GetAppMarketplaceUrl-Vorgang</span><span class="sxs-lookup"><span data-stu-id="5b7e7-148">GetAppMarketplaceUrl operation</span></span>](getappmarketplaceurl-operation.md)
    

