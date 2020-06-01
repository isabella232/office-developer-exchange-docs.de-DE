---
title: RefreshSharingFolder-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RefreshSharingFolder
api_type:
- schema
ms.assetid: 1b047e34-40f0-459f-ac9e-e9f8e7349479
description: Der RefreshSharingFolder-Vorgang aktualisiert den angegebenen lokalen Ordner mit den neuesten Daten aus dem Ordner, der freigegeben wird.
ms.openlocfilehash: dd7136ae82353841db09497d23eabe450c1c8b13
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456753"
---
# <a name="refreshsharingfolder-operation"></a><span data-ttu-id="4890e-103">RefreshSharingFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="4890e-103">RefreshSharingFolder operation</span></span>

<span data-ttu-id="4890e-104">Der **RefreshSharingFolder** -Vorgang aktualisiert den angegebenen lokalen Ordner mit den neuesten Daten aus dem Ordner, der freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4890e-104">The **RefreshSharingFolder** operation refreshes the specified local folder with the latest data from the folder that is being shared.</span></span> 
  
## <a name="soap-headers"></a><span data-ttu-id="4890e-105">SOAP-Header</span><span class="sxs-lookup"><span data-stu-id="4890e-105">SOAP Headers</span></span>

<span data-ttu-id="4890e-106">Der **RefreshSharingFolder** -Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt und beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="4890e-106">The **RefreshSharingFolder** operation can use the SOAP headers that are listed and described in the following table.</span></span> 
  
|<span data-ttu-id="4890e-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="4890e-107">**Header**</span></span>|<span data-ttu-id="4890e-108">**Element**</span><span class="sxs-lookup"><span data-stu-id="4890e-108">**Element**</span></span>|<span data-ttu-id="4890e-109">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4890e-109">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4890e-110">RequestVersion</span><span class="sxs-lookup"><span data-stu-id="4890e-110">RequestVersion</span></span>  <br/> |[<span data-ttu-id="4890e-111">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="4890e-111">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="4890e-112">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="4890e-112">Identifies the schema version for the operation request.</span></span>  <br/> |
|<span data-ttu-id="4890e-113">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="4890e-113">ServerVersion</span></span>  <br/> |[<span data-ttu-id="4890e-114">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="4890e-114">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="4890e-115">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="4890e-115">Identifies the version of the server that responded to the request.</span></span>  <br/> |
   
## <a name="refreshsharingfolder-request-example"></a><span data-ttu-id="4890e-116">RefreshSharingFolder-Anforderungs Beispiel</span><span class="sxs-lookup"><span data-stu-id="4890e-116">RefreshSharingFolder request example</span></span>

### <a name="description"></a><span data-ttu-id="4890e-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4890e-117">Description</span></span>

<span data-ttu-id="4890e-118">Das folgende Beispiel zeigt, wie Sie eine Anforderung zum Aktualisieren des angegebenen lokalen Ordners mit den neuesten Daten aus dem freigegebenen Ordner bilden.</span><span class="sxs-lookup"><span data-stu-id="4890e-118">The following example shows how to form a request to refresh the specified local folder with the latest data from the folder that is being shared.</span></span> <span data-ttu-id="4890e-119">Das [SharingFolderId](sharingfolderid.md) -Element gibt den Bezeichner des lokalen Ordners an, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="4890e-119">The [SharingFolderId](sharingfolderid.md) element specifies the identifier of the local folder to be refreshed.</span></span> 
  
### <a name="code"></a><span data-ttu-id="4890e-120">Code</span><span class="sxs-lookup"><span data-stu-id="4890e-120">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010"/>
  </soap:Header>
  <soap:Body>
    <RefreshSharingFolder xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:SharingFolderId Id="AAMkAD=" ChangeKey="AwAAA=" />
    </RefreshSharingFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a><span data-ttu-id="4890e-121">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="4890e-121">Request elements</span></span>

<span data-ttu-id="4890e-122">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="4890e-122">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="4890e-123">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="4890e-123">RequestServerVersion</span></span>](requestserverversion.md)
    
- [<span data-ttu-id="4890e-124">RefreshSharingFolder</span><span class="sxs-lookup"><span data-stu-id="4890e-124">RefreshSharingFolder</span></span>](refreshsharingfolder.md)
    
- [<span data-ttu-id="4890e-125">SharingFolderId</span><span class="sxs-lookup"><span data-stu-id="4890e-125">SharingFolderId</span></span>](sharingfolderid.md)
    
## <a name="successful-refreshsharingfolder-response"></a><span data-ttu-id="4890e-126">Erfolgreiche RefreshSharingFolder-Antwort</span><span class="sxs-lookup"><span data-stu-id="4890e-126">Successful RefreshSharingFolder Response</span></span>

### <a name="description"></a><span data-ttu-id="4890e-127">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4890e-127">Description</span></span>

<span data-ttu-id="4890e-128">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **RefreshSharingFolder** -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="4890e-128">The following example shows a successful response to a **RefreshSharingFolder** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="4890e-129">Code</span><span class="sxs-lookup"><span data-stu-id="4890e-129">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="0" 
                         MajorBuildNumber="639" 
                         MinorBuildNumber="11" 
                         Version="Exchange2010" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <RefreshSharingFolderResponseMessage ResponseClass="Success"
                                xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                                xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                                xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseCode>NoError</m:ResponseCode>
    </RefreshSharingFolderResponseMessage>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-response-elements"></a><span data-ttu-id="4890e-130">Erfolgreiche Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="4890e-130">Successful response elements</span></span>

<span data-ttu-id="4890e-131">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="4890e-131">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="4890e-132">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="4890e-132">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="4890e-133">RefreshSharingFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="4890e-133">RefreshSharingFolderResponseMessage</span></span>](refreshsharingfolderresponsemessage.md)
    
- [<span data-ttu-id="4890e-134">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="4890e-134">ResponseCode</span></span>](responsecode.md)
    
## <a name="refreshsharingfolder-error-response"></a><span data-ttu-id="4890e-135">RefreshSharingFolder-Fehlerantwort</span><span class="sxs-lookup"><span data-stu-id="4890e-135">RefreshSharingFolder error response</span></span>

### <a name="description"></a><span data-ttu-id="4890e-136">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4890e-136">Description</span></span>

<span data-ttu-id="4890e-137">Das folgende Beispiel zeigt eine Fehlerantwort auf eine **RefreshSharingFolder** -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="4890e-137">The following example shows an error response to a **RefreshSharingFolder** request.</span></span> <span data-ttu-id="4890e-138">In diesem Beispiel ist die **RefreshSharingFolder** -Anforderung fehlgeschlagen, da ein Abonnement, das dem angegebenen lokalen Ordner entspricht, nicht gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="4890e-138">In this example, the **RefreshSharingFolder** request failed because a subscription that corresponds to the specified local folder was not found.</span></span> 
  
### <a name="code"></a><span data-ttu-id="4890e-139">Code</span><span class="sxs-lookup"><span data-stu-id="4890e-139">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="0" 
                         MajorBuildNumber="639" 
                         MinorBuildNumber="11" 
                         Version="Exchange2010" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <RefreshSharingFolderResponseMessage ResponseClass="Error"
                                xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                                xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                                xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:MessageText>Failed to synchronize the sharing folder.</m:MessageText>
      <m:ResponseCode>ErrorSharingSynchronizationFailed</m:ResponseCode>
      <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
      <m:MessageXml>
        <t:Value Name="ErrorDetails">Microsoft.Exchange.InfoWorker.Common.Sharing.SubscriptionNotFoundException: The subscription wasn't found.;</t:Value>
      </m:MessageXml>
    </RefreshSharingFolderResponseMessage>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a><span data-ttu-id="4890e-140">Fehlerantwortelemente</span><span class="sxs-lookup"><span data-stu-id="4890e-140">Error response elements</span></span>

<span data-ttu-id="4890e-141">Folgende Elemente werden in der Fehlerantwort verwendet:</span><span class="sxs-lookup"><span data-stu-id="4890e-141">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="4890e-142">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="4890e-142">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="4890e-143">RefreshSharingFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="4890e-143">RefreshSharingFolderResponseMessage</span></span>](refreshsharingfolderresponsemessage.md)
    
- [<span data-ttu-id="4890e-144">MessageText</span><span class="sxs-lookup"><span data-stu-id="4890e-144">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="4890e-145">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="4890e-145">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="4890e-146">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="4890e-146">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="4890e-147">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="4890e-147">MessageXml</span></span>](messagexml.md)
    
## <a name="see-also"></a><span data-ttu-id="4890e-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4890e-148">See also</span></span>



[<span data-ttu-id="4890e-149">RefreshSharingFolder</span><span class="sxs-lookup"><span data-stu-id="4890e-149">RefreshSharingFolder</span></span>](refreshsharingfolder.md)
  
[<span data-ttu-id="4890e-150">RefreshSharingFolderType</span><span class="sxs-lookup"><span data-stu-id="4890e-150">RefreshSharingFolderType</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.RefreshSharingFolderType.aspx)
  
[<span data-ttu-id="4890e-151">RefreshSharingFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="4890e-151">RefreshSharingFolderResponseMessage</span></span>](refreshsharingfolderresponsemessage.md)
  
[<span data-ttu-id="4890e-152">RefreshSharingFolderResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="4890e-152">RefreshSharingFolderResponseMessageType</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.RefreshSharingFolderResponseMessageType.aspx)


[<span data-ttu-id="4890e-153">EWS-Operationen in Exchange</span><span class="sxs-lookup"><span data-stu-id="4890e-153">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
  
- [<span data-ttu-id="4890e-154">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="4890e-154">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

