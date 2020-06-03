---
title: InstallApp-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 596eae95-3e78-489a-8bb2-d2dd4a026405
description: Hier finden Sie Informationen zum InstallApp-EWS-Vorgang.
ms.openlocfilehash: ae6aab7f7176aa827bafa9abf1aa67d458d309d2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465688"
---
# <a name="installapp-operation"></a><span data-ttu-id="2a0ca-103">InstallApp-Vorgang</span><span class="sxs-lookup"><span data-stu-id="2a0ca-103">InstallApp operation</span></span>

<span data-ttu-id="2a0ca-104">Hier finden Sie Informationen zum **InstallApp** -EWS-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="2a0ca-104">Find information about the **InstallApp** EWS operation.</span></span> 
  
<span data-ttu-id="2a0ca-105">Mit dem **InstallApp** -Vorgang wird eine Mail-App für Outlook in einem Postfach installiert.</span><span class="sxs-lookup"><span data-stu-id="2a0ca-105">The **InstallApp** operation installs a mail app for Outlook in a mailbox.</span></span> 
  
<span data-ttu-id="2a0ca-106">Dieser Vorgang wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="2a0ca-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-installapp-operation"></a><span data-ttu-id="2a0ca-107">Verwenden des InstallApp-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="2a0ca-107">Using the InstallApp operation</span></span>

<span data-ttu-id="2a0ca-108">Der **InstallApp** -Vorgang verwendet ein einzelnes Argument, das eine zu installierende Mail-App identifiziert.</span><span class="sxs-lookup"><span data-stu-id="2a0ca-108">The **InstallApp** operation takes a single argument that identifies a mail app to install.</span></span> <span data-ttu-id="2a0ca-109">Das Argument enthält das Base64-codierte Manifest für eine Mail-app.</span><span class="sxs-lookup"><span data-stu-id="2a0ca-109">The argument contains the base64-encoded manifest for a mail app.</span></span> 
  
### <a name="installapp-operation-soap-headers"></a><span data-ttu-id="2a0ca-110">SOAP-Header des InstallApp-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="2a0ca-110">InstallApp operation SOAP headers</span></span>

<span data-ttu-id="2a0ca-111">Der **InstallApp** -Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="2a0ca-111">The **InstallApp** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="2a0ca-112">**Headername**</span><span class="sxs-lookup"><span data-stu-id="2a0ca-112">**Header name**</span></span>|<span data-ttu-id="2a0ca-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="2a0ca-113">**Element**</span></span>|<span data-ttu-id="2a0ca-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2a0ca-114">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2a0ca-115">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="2a0ca-115">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="2a0ca-116">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="2a0ca-116">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="2a0ca-117">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="2a0ca-117">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="2a0ca-118">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="2a0ca-118">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="2a0ca-119">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="2a0ca-119">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="2a0ca-120">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="2a0ca-120">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="2a0ca-121">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="2a0ca-121">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="2a0ca-122">Diese Kopfzeile gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="2a0ca-122">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="installapp-operation-request-example-install-a-mail-app-in-a-mailbox"></a><span data-ttu-id="2a0ca-123">InstallApp-Vorgangs Anforderungs Beispiel: Installieren einer Mail-app in einem Postfach</span><span class="sxs-lookup"><span data-stu-id="2a0ca-123">InstallApp operation request example: Install a mail app in a mailbox</span></span>

<span data-ttu-id="2a0ca-124">Im folgenden Beispiel einer **InstallApp** -Vorgangsanforderung wird gezeigt, wie eine Mail-App für Outlook installiert wird.</span><span class="sxs-lookup"><span data-stu-id="2a0ca-124">The following example of an **InstallApp** operation request shows how to install a mail app for Outlook.</span></span> <span data-ttu-id="2a0ca-125">Das App-Manifest kann mithilfe des GetAppManifests- [Vorgangs](getappmanifests-operation.md)gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="2a0ca-125">The app manifest can be found by using the [GetAppManifests operation](getappmanifests-operation.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="2a0ca-126">Das Base64-codierte App-Manifest wurde willkürlich abgeschnitten, um die Lesbarkeit zu erhalten, und stellt kein gültiges Manifest dar.</span><span class="sxs-lookup"><span data-stu-id="2a0ca-126">The base64-encoded app manifest has been arbitrarily truncated to preserve readability and does not represent a valid manifest.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
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

<span data-ttu-id="2a0ca-127">Der SOAP-Anforderungstext Körper enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="2a0ca-127">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="2a0ca-128">InstallApp</span><span class="sxs-lookup"><span data-stu-id="2a0ca-128">InstallApp</span></span>](installapp.md)
    
- [<span data-ttu-id="2a0ca-129">Manifest</span><span class="sxs-lookup"><span data-stu-id="2a0ca-129">Manifest</span></span>](manifest.md)
    
## <a name="successful-installapp-operation-response"></a><span data-ttu-id="2a0ca-130">Erfolgreiche Reaktion des InstallApp-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="2a0ca-130">Successful InstallApp operation response</span></span>

<span data-ttu-id="2a0ca-131">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **InstallApp** -Vorgangsanforderung zum Installieren einer Mail-app.</span><span class="sxs-lookup"><span data-stu-id="2a0ca-131">The following example shows a successful response to an **InstallApp** operation request to install a mail app.</span></span> 
  
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
      <InstallAppResponse ResponseClass="Success" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
      </InstallAppResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="2a0ca-132">Der SOAP-Antworttext Körper enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="2a0ca-132">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="2a0ca-133">InstallAppResponse</span><span class="sxs-lookup"><span data-stu-id="2a0ca-133">InstallAppResponse</span></span>](installappresponse.md)
    
- [<span data-ttu-id="2a0ca-134">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="2a0ca-134">ResponseCode</span></span>](responsecode.md)
    
## <a name="installapp-operation-error-response"></a><span data-ttu-id="2a0ca-135">Fehlerantwort des InstallApp-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="2a0ca-135">InstallApp operation error response</span></span>

<span data-ttu-id="2a0ca-136">Das folgende Beispiel zeigt eine Fehlerantwort auf eine **InstallApp** -Vorgangsanforderung.</span><span class="sxs-lookup"><span data-stu-id="2a0ca-136">The following example shows an error response to an **InstallApp** operation request.</span></span> <span data-ttu-id="2a0ca-137">Dies ist eine Antwort auf eine Anforderung, die ein ungültiges Manifest enthält.</span><span class="sxs-lookup"><span data-stu-id="2a0ca-137">This is a response to a request that contains an invalid manifest.</span></span> 
  
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
      <InstallAppResponse ResponseClass="Error" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>This app can't be installed. Missing OfficeApp element.</MessageText>
         <ResponseCode>ErrorInternalServerError</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </InstallAppResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="2a0ca-138">Der SOAP-Textkörper der Fehlerantwort enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="2a0ca-138">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="2a0ca-139">InstallAppResponse</span><span class="sxs-lookup"><span data-stu-id="2a0ca-139">InstallAppResponse</span></span>](installappresponse.md)
    
- [<span data-ttu-id="2a0ca-140">MessageText</span><span class="sxs-lookup"><span data-stu-id="2a0ca-140">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="2a0ca-141">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="2a0ca-141">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="2a0ca-142">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="2a0ca-142">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
## <a name="see-also"></a><span data-ttu-id="2a0ca-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2a0ca-143">See also</span></span>

- [<span data-ttu-id="2a0ca-144">EWS-Operationen in Exchange</span><span class="sxs-lookup"><span data-stu-id="2a0ca-144">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="2a0ca-145">DisableApp-Vorgang</span><span class="sxs-lookup"><span data-stu-id="2a0ca-145">DisableApp operation</span></span>](disableapp-operation.md)
    
- [<span data-ttu-id="2a0ca-146">UninstallApp-Vorgang</span><span class="sxs-lookup"><span data-stu-id="2a0ca-146">UninstallApp operation</span></span>](uninstallapp-operation.md)
    
- [<span data-ttu-id="2a0ca-147">GetAppManifests</span><span class="sxs-lookup"><span data-stu-id="2a0ca-147">GetAppManifests</span></span>](getappmanifests.md)
    
- [<span data-ttu-id="2a0ca-148">GetAppMarketplaceUrl-Vorgang</span><span class="sxs-lookup"><span data-stu-id="2a0ca-148">GetAppMarketplaceUrl operation</span></span>](getappmarketplaceurl-operation.md)
    

