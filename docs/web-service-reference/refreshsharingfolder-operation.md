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
description: Der Vorgang RefreshSharingFolder aktualisiert den angegebenen lokalen Ordner mit den neuesten Daten aus dem Ordner, der gemeinsam genutzt wird.
ms.openlocfilehash: 0037de28f0720b97cd51c58a6ee7e3c06e84d642
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831041"
---
# <a name="refreshsharingfolder-operation"></a><span data-ttu-id="99ecf-103">RefreshSharingFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="99ecf-103">RefreshSharingFolder operation</span></span>

<span data-ttu-id="99ecf-104">Der Vorgang **RefreshSharingFolder** aktualisiert den angegebenen lokalen Ordner mit den neuesten Daten aus dem Ordner, der gemeinsam genutzt wird.</span><span class="sxs-lookup"><span data-stu-id="99ecf-104">The **RefreshSharingFolder** operation refreshes the specified local folder with the latest data from the folder that is being shared.</span></span> 
  
## <a name="soap-headers"></a><span data-ttu-id="99ecf-105">SOAP-Header</span><span class="sxs-lookup"><span data-stu-id="99ecf-105">SOAP Headers</span></span>

<span data-ttu-id="99ecf-106">Der Vorgang **RefreshSharingFolder** können die SOAP-Header, die aufgeführt und in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="99ecf-106">The **RefreshSharingFolder** operation can use the SOAP headers that are listed and described in the following table.</span></span> 
  
|<span data-ttu-id="99ecf-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="99ecf-107">**Header**</span></span>|<span data-ttu-id="99ecf-108">**Element**</span><span class="sxs-lookup"><span data-stu-id="99ecf-108">**Element**</span></span>|<span data-ttu-id="99ecf-109">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="99ecf-109">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="99ecf-110">RequestVersion</span><span class="sxs-lookup"><span data-stu-id="99ecf-110">RequestVersion</span></span>  <br/> |[<span data-ttu-id="99ecf-111">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="99ecf-111">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="99ecf-112">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="99ecf-112">Identifies the schema version for the operation request.</span></span>  <br/> |
|<span data-ttu-id="99ecf-113">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="99ecf-113">ServerVersion</span></span>  <br/> |[<span data-ttu-id="99ecf-114">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="99ecf-114">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="99ecf-115">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="99ecf-115">Identifies the version of the server that responded to the request.</span></span>  <br/> |
   
## <a name="refreshsharingfolder-request-example"></a><span data-ttu-id="99ecf-116">Anforderungsbeispiel RefreshSharingFolder</span><span class="sxs-lookup"><span data-stu-id="99ecf-116">RefreshSharingFolder request example</span></span>

### <a name="description"></a><span data-ttu-id="99ecf-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="99ecf-117">Description</span></span>

<span data-ttu-id="99ecf-118">Im folgenden Beispiel wird veranschaulicht, wie auf eine Anforderung an den angegebenen lokalen Ordner mit den neuesten Daten aus dem Ordner zu aktualisieren, die gegenwärtig freigegebenen bilden.</span><span class="sxs-lookup"><span data-stu-id="99ecf-118">The following example shows how to form a request to refresh the specified local folder with the latest data from the folder that is being shared.</span></span> <span data-ttu-id="99ecf-119">Das [SharingFolderId](sharingfolderid.md) -Element gibt den Bezeichner des lokalen Ordners aktualisiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="99ecf-119">The [SharingFolderId](sharingfolderid.md) element specifies the identifier of the local folder to be refreshed.</span></span> 
  
### <a name="code"></a><span data-ttu-id="99ecf-120">Code</span><span class="sxs-lookup"><span data-stu-id="99ecf-120">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010"/>
  </soap:Header>
  <soap:Body>
    <RefreshSharingFolder xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:SharingFolderId Id="AAMkAD=" ChangeKey="AwAAA=" />
    </RefreshSharingFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a><span data-ttu-id="99ecf-121">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="99ecf-121">Request elements</span></span>

<span data-ttu-id="99ecf-122">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="99ecf-122">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="99ecf-123">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="99ecf-123">RequestServerVersion</span></span>](requestserverversion.md)
    
- [<span data-ttu-id="99ecf-124">RefreshSharingFolder</span><span class="sxs-lookup"><span data-stu-id="99ecf-124">RefreshSharingFolder</span></span>](refreshsharingfolder.md)
    
- [<span data-ttu-id="99ecf-125">SharingFolderId</span><span class="sxs-lookup"><span data-stu-id="99ecf-125">SharingFolderId</span></span>](sharingfolderid.md)
    
## <a name="successful-refreshsharingfolder-response"></a><span data-ttu-id="99ecf-126">Erfolgreiche RefreshSharingFolder Antwort</span><span class="sxs-lookup"><span data-stu-id="99ecf-126">Successful RefreshSharingFolder Response</span></span>

### <a name="description"></a><span data-ttu-id="99ecf-127">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="99ecf-127">Description</span></span>

<span data-ttu-id="99ecf-128">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine Anforderung **RefreshSharingFolder** .</span><span class="sxs-lookup"><span data-stu-id="99ecf-128">The following example shows a successful response to a **RefreshSharingFolder** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="99ecf-129">Code</span><span class="sxs-lookup"><span data-stu-id="99ecf-129">Code</span></span>

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
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <RefreshSharingFolderResponseMessage ResponseClass="Success"
                                xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
                                xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                                xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseCode>NoError</m:ResponseCode>
    </RefreshSharingFolderResponseMessage>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-response-elements"></a><span data-ttu-id="99ecf-130">Elemente einer erfolgreichen Antwort</span><span class="sxs-lookup"><span data-stu-id="99ecf-130">Successful response elements</span></span>

<span data-ttu-id="99ecf-131">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="99ecf-131">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="99ecf-132">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="99ecf-132">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="99ecf-133">RefreshSharingFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="99ecf-133">RefreshSharingFolderResponseMessage</span></span>](refreshsharingfolderresponsemessage.md)
    
- [<span data-ttu-id="99ecf-134">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="99ecf-134">ResponseCode</span></span>](responsecode.md)
    
## <a name="refreshsharingfolder-error-response"></a><span data-ttu-id="99ecf-135">Fehlerantwort RefreshSharingFolder</span><span class="sxs-lookup"><span data-stu-id="99ecf-135">RefreshSharingFolder error response</span></span>

### <a name="description"></a><span data-ttu-id="99ecf-136">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="99ecf-136">Description</span></span>

<span data-ttu-id="99ecf-137">Das folgende Beispiel zeigt eine Fehlerantwort an eine **RefreshSharingFolder** -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="99ecf-137">The following example shows an error response to a **RefreshSharingFolder** request.</span></span> <span data-ttu-id="99ecf-138">In diesem Beispiel wird die Anforderung **RefreshSharingFolder** ist fehlgeschlagen, da ein Abonnement, das den angegebenen lokalen Ordner entspricht, nicht gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="99ecf-138">In this example, the **RefreshSharingFolder** request failed because a subscription that corresponds to the specified local folder was not found.</span></span> 
  
### <a name="code"></a><span data-ttu-id="99ecf-139">Code</span><span class="sxs-lookup"><span data-stu-id="99ecf-139">Code</span></span>

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
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <RefreshSharingFolderResponseMessage ResponseClass="Error"
                                xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
                                xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                                xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="error-response-elements"></a><span data-ttu-id="99ecf-140">Fehler Antwortelemente</span><span class="sxs-lookup"><span data-stu-id="99ecf-140">Error response elements</span></span>

<span data-ttu-id="99ecf-141">Folgende Elemente werden in der Fehlerantwort verwendet:</span><span class="sxs-lookup"><span data-stu-id="99ecf-141">The following elements are used in the error response:</span></span>
  
- [<span data-ttu-id="99ecf-142">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="99ecf-142">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="99ecf-143">RefreshSharingFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="99ecf-143">RefreshSharingFolderResponseMessage</span></span>](refreshsharingfolderresponsemessage.md)
    
- [<span data-ttu-id="99ecf-144">MessageText</span><span class="sxs-lookup"><span data-stu-id="99ecf-144">MessageText</span></span>](messagetext.md)
    
- [<span data-ttu-id="99ecf-145">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="99ecf-145">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="99ecf-146">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="99ecf-146">DescriptiveLinkKey</span></span>](descriptivelinkkey.md)
    
- [<span data-ttu-id="99ecf-147">MessageXml</span><span class="sxs-lookup"><span data-stu-id="99ecf-147">MessageXml</span></span>](messagexml.md)
    
## <a name="see-also"></a><span data-ttu-id="99ecf-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="99ecf-148">See also</span></span>



[<span data-ttu-id="99ecf-149">RefreshSharingFolder</span><span class="sxs-lookup"><span data-stu-id="99ecf-149">RefreshSharingFolder</span></span>](refreshsharingfolder.md)
  
[<span data-ttu-id="99ecf-150">RefreshSharingFolderType</span><span class="sxs-lookup"><span data-stu-id="99ecf-150">RefreshSharingFolderType</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.RefreshSharingFolderType.aspx)
  
[<span data-ttu-id="99ecf-151">RefreshSharingFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="99ecf-151">RefreshSharingFolderResponseMessage</span></span>](refreshsharingfolderresponsemessage.md)
  
[<span data-ttu-id="99ecf-152">RefreshSharingFolderResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="99ecf-152">RefreshSharingFolderResponseMessageType</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.RefreshSharingFolderResponseMessageType.aspx)


[<span data-ttu-id="99ecf-153">EWS-Operationen in Exchange</span><span class="sxs-lookup"><span data-stu-id="99ecf-153">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
  
- [<span data-ttu-id="99ecf-154">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="99ecf-154">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

