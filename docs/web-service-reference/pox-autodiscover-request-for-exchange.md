---
title: POX Anforderung der AutoErmittlung für Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 75671b1d-f35b-497b-8d8c-706f3f2535fd
description: Die Anforderung der AutoErmittlung enthält eine Abfrage für Access-Clientkonfiguration eines Benutzers.
ms.openlocfilehash: 48d6c30946e75936ed93a6f4507d8a8d3ae47d40
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830865"
---
# <a name="pox-autodiscover-request-for-exchange"></a><span data-ttu-id="dc12b-103">POX Anforderung der AutoErmittlung für Exchange</span><span class="sxs-lookup"><span data-stu-id="dc12b-103">POX Autodiscover request for Exchange</span></span>

<span data-ttu-id="dc12b-104">Die Anforderung der AutoErmittlung enthält eine Abfrage für Access-Clientkonfiguration eines Benutzers.</span><span class="sxs-lookup"><span data-stu-id="dc12b-104">The Autodiscover request contains a query for a user's client access configuration.</span></span>
  
## <a name="autodiscover-request-example"></a><span data-ttu-id="dc12b-105">AutoErmittlung-anforderungsbeispiel</span><span class="sxs-lookup"><span data-stu-id="dc12b-105">Autodiscover request example</span></span>

### <a name="description"></a><span data-ttu-id="dc12b-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dc12b-106">Description</span></span>

<span data-ttu-id="dc12b-107">Das folgende XML-Beispiel zeigt einen AutoErmittlung-Anforderungstext.</span><span class="sxs-lookup"><span data-stu-id="dc12b-107">The following XML example shows an Autodiscover request body.</span></span>
  
### <a name="code"></a><span data-ttu-id="dc12b-108">Code</span><span class="sxs-lookup"><span data-stu-id="dc12b-108">Code</span></span>

```XML
<Autodiscover xmlns="http://schemas.microsoft.com/exchange/autodiscover/outlook/requestschema/2006">
   <Request>
     <EMailAddress>user@contoso.com</EMailAddress>
     <AcceptableResponseSchema>http://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a</AcceptableResponseSchema>
   </Request>
 </Autodiscover>
```

### <a name="request-headers"></a><span data-ttu-id="dc12b-109">Anforderungsheader</span><span class="sxs-lookup"><span data-stu-id="dc12b-109">Request Headers</span></span>

<span data-ttu-id="dc12b-110">Die folgenden HTTP-Header sind optional, wenn für die AutoErmittlung-Anforderungen senden.</span><span class="sxs-lookup"><span data-stu-id="dc12b-110">The following HTTP headers are optional when sending Autodiscover requests.</span></span>
  
<span data-ttu-id="dc12b-111">**In Tabelle 1. Gemeinsam genutzte HTTP-Anforderung**</span><span class="sxs-lookup"><span data-stu-id="dc12b-111">**Table 1. HTTP request headers**</span></span>

|<span data-ttu-id="dc12b-112">**Header**</span><span class="sxs-lookup"><span data-stu-id="dc12b-112">**Header**</span></span>|<span data-ttu-id="dc12b-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dc12b-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="dc12b-114">X-MapiHttpCapability</span><span class="sxs-lookup"><span data-stu-id="dc12b-114">X-MapiHttpCapability</span></span>  <br/> |<span data-ttu-id="dc12b-115">Wenn vorhanden und auf "1", gibt an, dass der Client Informationen anfordert, die Verbindung mit dem Server mithilfe von MAPI/HTTP-Protokoll verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="dc12b-115">If present and set to "1", indicates that the client is requesting information that can be used to connect to the server by using the MAPI/HTTP protocol.</span></span> <span data-ttu-id="dc12b-116">Diese Kopfzeile gilt für Clients, mit die das MAPI/HTTP-Protokoll implementiert.</span><span class="sxs-lookup"><span data-stu-id="dc12b-116">This header is applicable to clients that implement the MAPI/HTTP protocol.</span></span>  <br/> |
|<span data-ttu-id="dc12b-117">X-ClientCanHandle</span><span class="sxs-lookup"><span data-stu-id="dc12b-117">X-ClientCanHandle</span></span>  <br/> |<span data-ttu-id="dc12b-118">Diese Kopfzeile enthält eine durch Trennzeichen getrennte Liste der Funktionen, die der Client unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dc12b-118">This header contains a comma-delimited list of capabilities that the client supports.</span></span> <span data-ttu-id="dc12b-119">In Tabelle 2 sind die möglichen Werte angegeben.</span><span class="sxs-lookup"><span data-stu-id="dc12b-119">The possible values are specified in Table 2.</span></span>  <br/> |
   
<span data-ttu-id="dc12b-120">**In Tabelle 2. X-ClientCanHandle-Headerwerte**</span><span class="sxs-lookup"><span data-stu-id="dc12b-120">**Table 2. X-ClientCanHandle header values**</span></span>

|<span data-ttu-id="dc12b-121">**X-ClientCanHandle Wert (Groß-/Kleinschreibung unterschieden)**</span><span class="sxs-lookup"><span data-stu-id="dc12b-121">**X-ClientCanHandle value (case-insensitive)**</span></span>|<span data-ttu-id="dc12b-122">**Minimale Serverversion**</span><span class="sxs-lookup"><span data-stu-id="dc12b-122">**Minimum server version**</span></span>|<span data-ttu-id="dc12b-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dc12b-123">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="dc12b-124">Verhandeln</span><span class="sxs-lookup"><span data-stu-id="dc12b-124">Negotiate</span></span>  <br/> |<span data-ttu-id="dc12b-125">15.00.0995.014</span><span class="sxs-lookup"><span data-stu-id="dc12b-125">15.00.0995.014</span></span>  <br/> |<span data-ttu-id="dc12b-126">Wenn dieser Wert vorhanden ist, gibt der Server einen Wert "Negotiate" im Element [AuthPackage (POX)](authpackage-pox.md) zurück, wenn der Server für die Annahme Negotiate-Authentifizierung konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="dc12b-126">If this value is present, the server will return a value of "Negotiate" in the [AuthPackage (POX)](authpackage-pox.md) element if the server is configured to accept Negotiate authentication.</span></span> <span data-ttu-id="dc12b-127">Wenn dieser Wert nicht vorhanden ist, gibt der Server einen Wert "Negotiate" nicht im **AuthPackage** -Element zurück.</span><span class="sxs-lookup"><span data-stu-id="dc12b-127">If this value is not present, the server will not return a value of "Negotiate" in the **AuthPackage** element.</span></span>  <br/> |
|<span data-ttu-id="dc12b-128">ExHttpInfo</span><span class="sxs-lookup"><span data-stu-id="dc12b-128">ExHttpInfo</span></span>  <br/> |<span data-ttu-id="dc12b-129">15.00.0995.014</span><span class="sxs-lookup"><span data-stu-id="dc12b-129">15.00.0995.014</span></span>  <br/> |<span data-ttu-id="dc12b-130">Wenn dieser Wert vorhanden ist, gibt der Server zurück, ein [Protokoll (POX)](protocol-pox.md) -Element mit einem [Typ (POX)](type-pox.md) Element auf "EXHTTP" festgelegt, wenn der Server für die Annahme von RPC/HTTP-Verbindungen konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="dc12b-130">If this value is present, the server will return a [Protocol (POX)](protocol-pox.md) element with a [Type (POX)](type-pox.md) element set to "EXHTTP" if the server is configured to accept RPC/HTTP connections.</span></span> <span data-ttu-id="dc12b-131">Wenn dieser Wert nicht vorhanden ist, wird der Server kein **Protokoll** -Element mit einem **Typ** Element auf "EXHTTP" festgelegt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="dc12b-131">If this value is not present, the server will not return a **Protocol** element with a **Type** element set to "EXHTTP".</span></span>  <br/> |
   
### <a name="request-elements"></a><span data-ttu-id="dc12b-132">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="dc12b-132">Request elements</span></span>

<span data-ttu-id="dc12b-133">Die folgenden Elemente werden im Textkörper Anforderung verwendet:</span><span class="sxs-lookup"><span data-stu-id="dc12b-133">The following elements are used in the request body:</span></span>
  
- [<span data-ttu-id="dc12b-134">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="dc12b-134">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
    
- [<span data-ttu-id="dc12b-135">Anforderung (POX)</span><span class="sxs-lookup"><span data-stu-id="dc12b-135">Request (POX)</span></span>](request-pox.md)
    
- [<span data-ttu-id="dc12b-136">AcceptableResponseSchema (POX)</span><span class="sxs-lookup"><span data-stu-id="dc12b-136">AcceptableResponseSchema (POX)</span></span>](acceptableresponseschema-pox.md)
    
- [<span data-ttu-id="dc12b-137">EMailAddress (POX)</span><span class="sxs-lookup"><span data-stu-id="dc12b-137">EMailAddress (POX)</span></span>](emailaddress-pox.md)
    
> [!NOTE]
> <span data-ttu-id="dc12b-138">Das Element [LegacyDN (POX)](legacydn-pox.md) kann anstelle der [EMailAddress (POX)](emailaddress-pox.md) -Elements verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dc12b-138">The [LegacyDN (POX)](legacydn-pox.md) element can be used in place of the [EMailAddress (POX)](emailaddress-pox.md) element.</span></span> 
  
### <a name="version-differences"></a><span data-ttu-id="dc12b-139">Versionsunterschiede</span><span class="sxs-lookup"><span data-stu-id="dc12b-139">Version differences</span></span>

<span data-ttu-id="dc12b-140">Die X-MapiHttpCapability Kopfzeile steht in Office 365 und Exchange Online und lokaler, beginnend mit Exchange-Versionen 15.00.0847.032 (Exchange Server 2013 SP1) erstellen.</span><span class="sxs-lookup"><span data-stu-id="dc12b-140">The X-MapiHttpCapability header is available in Office 365, Exchange Online, and on-premises versions of Exchange starting with build 15.00.0847.032 (Exchange Server 2013 SP1).</span></span>
  
<span data-ttu-id="dc12b-141">Die X-ClientCanHandle Kopfzeile steht in Office 365 und Exchange Online und lokaler, beginnend mit Exchange-Versionen 15.00.0995.014 erstellen.</span><span class="sxs-lookup"><span data-stu-id="dc12b-141">The X-ClientCanHandle header is available in Office 365, Exchange Online, and on-premises versions of Exchange starting with build 15.00.0995.014.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="dc12b-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dc12b-142">See also</span></span>



[<span data-ttu-id="dc12b-143">POX Antwort der AutoErmittlung für Exchange</span><span class="sxs-lookup"><span data-stu-id="dc12b-143">POX Autodiscover response for Exchange</span></span>](pox-autodiscover-response-for-exchange.md)


[<span data-ttu-id="dc12b-144">POX AutoErmittlung Webdienstverweis für Exchange</span><span class="sxs-lookup"><span data-stu-id="dc12b-144">POX Autodiscover web service reference for Exchange</span></span>](pox-autodiscover-web-service-reference-for-exchange.md)
  
[<span data-ttu-id="dc12b-145">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="dc12b-145">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

