---
title: DisableApp-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 211731a3-2470-49af-bda3-1ddfc15a8e46
description: Hier finden Sie Informationen zum DisableApp-EWS-Vorgang.
ms.openlocfilehash: 8e1f3a257a70c042a01ed70da97cfa0573a2d454
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462066"
---
# <a name="disableapp-operation"></a><span data-ttu-id="210ed-103">DisableApp-Vorgang</span><span class="sxs-lookup"><span data-stu-id="210ed-103">DisableApp operation</span></span>

<span data-ttu-id="210ed-104">Hier finden Sie Informationen zum **DisableApp** -EWS-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="210ed-104">Find information about the **DisableApp** EWS operation.</span></span> 
  
<span data-ttu-id="210ed-105">Der **DisableApp** -Vorgang deaktiviert eine Mail-App für Outlook.</span><span class="sxs-lookup"><span data-stu-id="210ed-105">The **DisableApp** operation disables a mail app for Outlook.</span></span> 
  
<span data-ttu-id="210ed-106">Dieser Vorgang wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="210ed-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-disableapp-operation"></a><span data-ttu-id="210ed-107">Verwenden des DisableApp-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="210ed-107">Using the DisableApp operation</span></span>

<span data-ttu-id="210ed-108">Der **DisableApp** -Vorgang benötigt zwei Argumente in der Anforderung, die die zu deaktivierende Mail-APP und den Grund für die Deaktivierung identifizieren.</span><span class="sxs-lookup"><span data-stu-id="210ed-108">The **DisableApp** operation takes two arguments in the request that identify the mail app to disable and the reason why it was disabled.</span></span> 
  
### <a name="disableapp-operation-soap-headers"></a><span data-ttu-id="210ed-109">SOAP-Header des DisableApp-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="210ed-109">DisableApp operation SOAP headers</span></span>

<span data-ttu-id="210ed-110">Der **DisableApp** -Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="210ed-110">The **DisableApp** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="210ed-111">**Headername**</span><span class="sxs-lookup"><span data-stu-id="210ed-111">**Header name**</span></span>|<span data-ttu-id="210ed-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="210ed-112">**Element**</span></span>|<span data-ttu-id="210ed-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="210ed-113">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="210ed-114">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="210ed-114">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="210ed-115">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="210ed-115">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="210ed-116">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="210ed-116">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="210ed-117">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="210ed-117">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="210ed-118">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="210ed-118">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="210ed-119">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="210ed-119">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="210ed-120">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="210ed-120">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="210ed-121">Diese Kopfzeile gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="210ed-121">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="disableapp-operation-request-example-disable-a-mail-app-installed-in-a-mailbox"></a><span data-ttu-id="210ed-122">DisableApp-Vorgangs Anforderungs Beispiel: Deaktivieren einer in einem Postfach installierten Mail-App</span><span class="sxs-lookup"><span data-stu-id="210ed-122">DisableApp operation request example: Disable a mail app installed in a mailbox</span></span>

<span data-ttu-id="210ed-123">Im folgenden Beispiel einer **DisableApp** -Vorgangsanforderung wird gezeigt, wie eine Mail-App deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="210ed-123">The following example of a **DisableApp** operation request shows how to a disable a mail app.</span></span> <span data-ttu-id="210ed-124">Der APP-Bezeichner befindet sich im App-Manifest, das in einer [GetAppManifests-Vorgangs](getappmanifests-operation.md) Antwort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="210ed-124">The app identifier can be found in the app manifest that is returned in a [GetAppManifests operation](getappmanifests-operation.md) response.</span></span> 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
      <t:MailboxCulture>en-US</t:MailboxCulture>
      <t:TimeZoneContext>
         <t:TimeZoneDefinition Id="GMT Standard Time"/>
      </t:TimeZoneContext>
   </soap:Header>
   <soap:Body >
      <m:DisableApp>
         <m:ID>1C50226D-04B5-4AB2-9FCD-42E236B59E4B</m:ID>
         <m:DisableReason>NoReason</m:DisableReason>
      </m:DisableApp>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="210ed-125">Der SOAP-Anforderungstext Körper enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="210ed-125">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="210ed-126">DisableApp</span><span class="sxs-lookup"><span data-stu-id="210ed-126">DisableApp</span></span>](disableapp.md)
    
- [<span data-ttu-id="210ed-127">ID (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="210ed-127">ID (String)</span></span>](id-string.md)
    
- [<span data-ttu-id="210ed-128">DisableReason</span><span class="sxs-lookup"><span data-stu-id="210ed-128">DisableReason</span></span>](disablereason.md)
    
## <a name="successful-disableapp-operation-response"></a><span data-ttu-id="210ed-129">Erfolgreiche Reaktion des DisableApp-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="210ed-129">Successful DisableApp operation response</span></span>

<span data-ttu-id="210ed-130">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **DisableApp** -Vorgangsanforderung zum Deaktivieren einer Mail-app.</span><span class="sxs-lookup"><span data-stu-id="210ed-130">The following example shows a successful response to a **DisableApp** operation request to disable a mail app.</span></span> 
  
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
      <DisableAppResponse ResponseClass="Success" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
      </DisableAppResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="210ed-131">Der SOAP-Antworttext Körper enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="210ed-131">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="210ed-132">DisableAppResponse</span><span class="sxs-lookup"><span data-stu-id="210ed-132">DisableAppResponse</span></span>](disableappresponse.md)
    
- [<span data-ttu-id="210ed-133">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="210ed-133">ResponseCode</span></span>](responsecode.md)
    
## <a name="disableapp-operation-error-response"></a><span data-ttu-id="210ed-134">Fehlerantwort des DisableApp-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="210ed-134">DisableApp operation error response</span></span>

<span data-ttu-id="210ed-135">Das folgende Beispiel zeigt eine Fehlerantwort auf eine **DisableApp** -Vorgangsanforderung.</span><span class="sxs-lookup"><span data-stu-id="210ed-135">The following example shows an error response to a **DisableApp** operation request.</span></span> <span data-ttu-id="210ed-136">Dies ist eine Antwort auf eine Anforderung zum Deaktivieren einer Mail-APP, die nicht in einem Postfach installiert ist.</span><span class="sxs-lookup"><span data-stu-id="210ed-136">This is a response to a request to disable a mail app that is not installed in a mailbox.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="556" MinorBuildNumber="14" Version="Exchange2013" xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" xmlns="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <DisableAppResponse ResponseClass="Error" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>Extension ID 1C50226D-04B5-4AB2-9FCD-42E236B59E4A can't be found.</MessageText>
         <ResponseCode>ErrorExtensionNotFound</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </DisableAppResponse>
   </s:Body>
</s:Envelope>
```

<span data-ttu-id="210ed-137">Der SOAP-Textkörper der Fehlerantwort enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="210ed-137">The error response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="210ed-138">DisableAppResponse</span><span class="sxs-lookup"><span data-stu-id="210ed-138">DisableAppResponse</span></span>](disableappresponse.md)
    
- [<span data-ttu-id="210ed-139">MessageText</span><span class="sxs-lookup"><span data-stu-id="210ed-139">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="210ed-140">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="210ed-140">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="210ed-141">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="210ed-141">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
<span data-ttu-id="210ed-142">Weitere Fehlercodes, die für EWS allgemein und spezifisch für diesen Vorgang sind, finden Sie unter [Response Code](responsecode.md).</span><span class="sxs-lookup"><span data-stu-id="210ed-142">For additional error codes that are generic to EWS and specific to this operation, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="210ed-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="210ed-143">See also</span></span>

- [<span data-ttu-id="210ed-144">EWS-Operationen in Exchange</span><span class="sxs-lookup"><span data-stu-id="210ed-144">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)   
- [<span data-ttu-id="210ed-145">InstallApp-Vorgang</span><span class="sxs-lookup"><span data-stu-id="210ed-145">InstallApp operation</span></span>](installapp-operation.md)   
- [<span data-ttu-id="210ed-146">UninstallApp-Vorgang</span><span class="sxs-lookup"><span data-stu-id="210ed-146">UninstallApp operation</span></span>](uninstallapp-operation.md)   
- [<span data-ttu-id="210ed-147">GetAppManifests</span><span class="sxs-lookup"><span data-stu-id="210ed-147">GetAppManifests</span></span>](getappmanifests.md)   
- [<span data-ttu-id="210ed-148">GetAppMarketplaceUrl-Vorgang</span><span class="sxs-lookup"><span data-stu-id="210ed-148">GetAppMarketplaceUrl operation</span></span>](getappmarketplaceurl-operation.md)   
- [<span data-ttu-id="210ed-149">Outlook-Add-Ins</span><span class="sxs-lookup"><span data-stu-id="210ed-149">Outlook add-ins</span></span>](https://msdn.microsoft.com/library/71e64bc9-e347-4f5d-8948-0a47b5dd93e6%28Office.15%29.aspx)
    

