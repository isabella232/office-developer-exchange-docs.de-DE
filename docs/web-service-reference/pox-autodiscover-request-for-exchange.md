---
title: POX-Anforderung der AutoErmittlung für Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 75671b1d-f35b-497b-8d8c-706f3f2535fd
description: Die Auto Ermittlungsanforderung enthält eine Abfrage für die Clientzugriffs Konfiguration eines Benutzers.
ms.openlocfilehash: b2138f9813c7b75aef9afb90089b9b874aac7532
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461667"
---
# <a name="pox-autodiscover-request-for-exchange"></a><span data-ttu-id="131ee-103">POX-Anforderung der AutoErmittlung für Exchange</span><span class="sxs-lookup"><span data-stu-id="131ee-103">POX Autodiscover request for Exchange</span></span>

<span data-ttu-id="131ee-104">Die Auto Ermittlungsanforderung enthält eine Abfrage für die Clientzugriffs Konfiguration eines Benutzers.</span><span class="sxs-lookup"><span data-stu-id="131ee-104">The Autodiscover request contains a query for a user's client access configuration.</span></span>
  
## <a name="autodiscover-request-example"></a><span data-ttu-id="131ee-105">Beispiel für eine Auto Ermittlungsanforderung</span><span class="sxs-lookup"><span data-stu-id="131ee-105">Autodiscover request example</span></span>

### <a name="description"></a><span data-ttu-id="131ee-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="131ee-106">Description</span></span>

<span data-ttu-id="131ee-107">Das folgende XML-Beispiel zeigt einen Auto Ermittlungs Anforderungstext.</span><span class="sxs-lookup"><span data-stu-id="131ee-107">The following XML example shows an Autodiscover request body.</span></span>
  
### <a name="code"></a><span data-ttu-id="131ee-108">Code</span><span class="sxs-lookup"><span data-stu-id="131ee-108">Code</span></span>

```XML
<Autodiscover xmlns="https://schemas.microsoft.com/exchange/autodiscover/outlook/requestschema/2006">
   <Request>
     <EMailAddress>user@contoso.com</EMailAddress>
     <AcceptableResponseSchema>https://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a</AcceptableResponseSchema>
   </Request>
 </Autodiscover>
```

### <a name="request-headers"></a><span data-ttu-id="131ee-109">Anforderungs Kopfzeilen</span><span class="sxs-lookup"><span data-stu-id="131ee-109">Request Headers</span></span>

<span data-ttu-id="131ee-110">Die folgenden HTTP-Header sind beim Senden von Auto Ermittlungsanforderungen optional.</span><span class="sxs-lookup"><span data-stu-id="131ee-110">The following HTTP headers are optional when sending Autodiscover requests.</span></span>
  
<span data-ttu-id="131ee-111">**Tabelle 1. HTTP-Anforderungsheader**</span><span class="sxs-lookup"><span data-stu-id="131ee-111">**Table 1. HTTP request headers**</span></span>

|<span data-ttu-id="131ee-112">**Header**</span><span class="sxs-lookup"><span data-stu-id="131ee-112">**Header**</span></span>|<span data-ttu-id="131ee-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="131ee-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="131ee-114">X-MapiHttpCapability</span><span class="sxs-lookup"><span data-stu-id="131ee-114">X-MapiHttpCapability</span></span>  <br/> |<span data-ttu-id="131ee-115">Wenn vorhanden und auf "1" festgelegt, wird angegeben, dass der Clientinformationen anfordert, die zum Herstellen einer Verbindung mit dem Server mithilfe des MAPI/http-Protokolls verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="131ee-115">If present and set to "1", indicates that the client is requesting information that can be used to connect to the server by using the MAPI/HTTP protocol.</span></span> <span data-ttu-id="131ee-116">Diese Kopfzeile gilt für Clients, die das MAPI/http-Protokoll implementieren.</span><span class="sxs-lookup"><span data-stu-id="131ee-116">This header is applicable to clients that implement the MAPI/HTTP protocol.</span></span>  <br/> |
|<span data-ttu-id="131ee-117">X-ClientCanHandle</span><span class="sxs-lookup"><span data-stu-id="131ee-117">X-ClientCanHandle</span></span>  <br/> |<span data-ttu-id="131ee-118">Diese Kopfzeile enthält eine durch trennzeichengetrennte Liste von Funktionen, die vom Client unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="131ee-118">This header contains a comma-delimited list of capabilities that the client supports.</span></span> <span data-ttu-id="131ee-119">Die möglichen Werte sind in Tabelle 2 angegeben.</span><span class="sxs-lookup"><span data-stu-id="131ee-119">The possible values are specified in Table 2.</span></span>  <br/> |
   
<span data-ttu-id="131ee-120">**Tabelle 2. X-ClientCanHandle-Headerwerte**</span><span class="sxs-lookup"><span data-stu-id="131ee-120">**Table 2. X-ClientCanHandle header values**</span></span>

|<span data-ttu-id="131ee-121">**X-ClientCanHandle-Wert (Groß-/Kleinschreibung wird nicht berücksichtigt)**</span><span class="sxs-lookup"><span data-stu-id="131ee-121">**X-ClientCanHandle value (case-insensitive)**</span></span>|<span data-ttu-id="131ee-122">**Minimale Server Version**</span><span class="sxs-lookup"><span data-stu-id="131ee-122">**Minimum server version**</span></span>|<span data-ttu-id="131ee-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="131ee-123">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="131ee-124">Aushandeln</span><span class="sxs-lookup"><span data-stu-id="131ee-124">Negotiate</span></span>  <br/> |<span data-ttu-id="131ee-125">15.00.0995.014</span><span class="sxs-lookup"><span data-stu-id="131ee-125">15.00.0995.014</span></span>  <br/> |<span data-ttu-id="131ee-126">Wenn dieser Wert vorhanden ist, gibt der Server den Wert "Negotiate" im [AuthPackage (POX)-](authpackage-pox.md) Element zurück, wenn der Server so konfiguriert ist, dass die Negotiate-Authentifizierung akzeptiert wird.</span><span class="sxs-lookup"><span data-stu-id="131ee-126">If this value is present, the server will return a value of "Negotiate" in the [AuthPackage (POX)](authpackage-pox.md) element if the server is configured to accept Negotiate authentication.</span></span> <span data-ttu-id="131ee-127">Wenn dieser Wert nicht vorhanden ist, gibt der Server den Wert "Negotiate" im **AuthPackage** -Element nicht zurück.</span><span class="sxs-lookup"><span data-stu-id="131ee-127">If this value is not present, the server will not return a value of "Negotiate" in the **AuthPackage** element.</span></span>  <br/> |
|<span data-ttu-id="131ee-128">ExHttpInfo</span><span class="sxs-lookup"><span data-stu-id="131ee-128">ExHttpInfo</span></span>  <br/> |<span data-ttu-id="131ee-129">15.00.0995.014</span><span class="sxs-lookup"><span data-stu-id="131ee-129">15.00.0995.014</span></span>  <br/> |<span data-ttu-id="131ee-130">Wenn dieser Wert vorhanden ist, gibt der Server ein [Pocken-Element (POX](protocol-pox.md) ) mit einem [Typ (POX)](type-pox.md) -Element auf "http" zurück, wenn der Server für die Annahme von RPC/HTTP-Verbindungen konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="131ee-130">If this value is present, the server will return a [Protocol (POX)](protocol-pox.md) element with a [Type (POX)](type-pox.md) element set to "EXHTTP" if the server is configured to accept RPC/HTTP connections.</span></span> <span data-ttu-id="131ee-131">Wenn dieser Wert nicht vorhanden ist, gibt der Server kein **Protocol** -Element zurück, dessen **Type** -Element auf "http" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="131ee-131">If this value is not present, the server will not return a **Protocol** element with a **Type** element set to "EXHTTP".</span></span>  <br/> |
   
### <a name="request-elements"></a><span data-ttu-id="131ee-132">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="131ee-132">Request elements</span></span>

<span data-ttu-id="131ee-133">Die folgenden Elemente werden im Anforderungstext verwendet:</span><span class="sxs-lookup"><span data-stu-id="131ee-133">The following elements are used in the request body:</span></span>
  
- [<span data-ttu-id="131ee-134">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="131ee-134">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
    
- [<span data-ttu-id="131ee-135">Anforderung (POX)</span><span class="sxs-lookup"><span data-stu-id="131ee-135">Request (POX)</span></span>](request-pox.md)
    
- [<span data-ttu-id="131ee-136">AcceptableResponseSchema (POX)</span><span class="sxs-lookup"><span data-stu-id="131ee-136">AcceptableResponseSchema (POX)</span></span>](acceptableresponseschema-pox.md)
    
- [<span data-ttu-id="131ee-137">E-mailemail (POX)</span><span class="sxs-lookup"><span data-stu-id="131ee-137">EMailAddress (POX)</span></span>](emailaddress-pox.md)
    
> [!NOTE]
> <span data-ttu-id="131ee-138">Das [LegacyDN (POX)-](legacydn-pox.md) Element kann anstelle des Elements [Email (POX)](emailaddress-pox.md) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="131ee-138">The [LegacyDN (POX)](legacydn-pox.md) element can be used in place of the [EMailAddress (POX)](emailaddress-pox.md) element.</span></span> 
  
### <a name="version-differences"></a><span data-ttu-id="131ee-139">Versionsunterschiede</span><span class="sxs-lookup"><span data-stu-id="131ee-139">Version differences</span></span>

<span data-ttu-id="131ee-140">Der X-MapiHttpCapability-Header ist in Office 365-, Exchange Online-und lokalen Versionen von Exchange verfügbar, beginnend mit Build 15.00.0847.032 (Exchange Server 2013 SP1).</span><span class="sxs-lookup"><span data-stu-id="131ee-140">The X-MapiHttpCapability header is available in Office 365, Exchange Online, and on-premises versions of Exchange starting with build 15.00.0847.032 (Exchange Server 2013 SP1).</span></span>
  
<span data-ttu-id="131ee-141">Der X-ClientCanHandle-Header ist in Office 365, Exchange Online und lokalen Versionen von Exchange verfügbar, beginnend mit Build 15.00.0995.014.</span><span class="sxs-lookup"><span data-stu-id="131ee-141">The X-ClientCanHandle header is available in Office 365, Exchange Online, and on-premises versions of Exchange starting with build 15.00.0995.014.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="131ee-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="131ee-142">See also</span></span>



[<span data-ttu-id="131ee-143">POX-Auto Ermittlungs Antwort für Exchange</span><span class="sxs-lookup"><span data-stu-id="131ee-143">POX Autodiscover response for Exchange</span></span>](pox-autodiscover-response-for-exchange.md)


[<span data-ttu-id="131ee-144">POX AutoErmittlung Webdienstverweis für Exchange</span><span class="sxs-lookup"><span data-stu-id="131ee-144">POX Autodiscover web service reference for Exchange</span></span>](pox-autodiscover-web-service-reference-for-exchange.md)
  
[<span data-ttu-id="131ee-145">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="131ee-145">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

