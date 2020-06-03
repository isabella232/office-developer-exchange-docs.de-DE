---
title: TokenIssuer (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2d7be675-626c-4173-89e9-e32beef81ad5
description: Das TokenIssuer-Element gibt den URI (SOAP) und den Endpunkt (SOAP) für den Sicherheitstokendienst an.
ms.openlocfilehash: e9c0b4140de26c7ff05daf4e863b3e8a17fedc62
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526326"
---
# <a name="tokenissuer-soap"></a><span data-ttu-id="50d23-103">TokenIssuer (SOAP)</span><span class="sxs-lookup"><span data-stu-id="50d23-103">TokenIssuer (SOAP)</span></span>

<span data-ttu-id="50d23-104">Das **TokenIssuer** -Element gibt den [URI (SOAP)](uri-soap.md) und den [Endpunkt (SOAP)](endpoint-soap.md) für den Sicherheitstokendienst an.</span><span class="sxs-lookup"><span data-stu-id="50d23-104">The **TokenIssuer** element specifies the [Uri (SOAP)](uri-soap.md) and [Endpoint (SOAP)](endpoint-soap.md) for the security token service.</span></span> 
  
```XML
<TokenIssuer>
   <Uri/>
   <Endpoint/>
</TokenIssuer>
```

 <span data-ttu-id="50d23-105">**TokenIssuer**</span><span class="sxs-lookup"><span data-stu-id="50d23-105">**TokenIssuer**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="50d23-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="50d23-106">Attributes and elements</span></span>

<span data-ttu-id="50d23-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="50d23-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="50d23-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="50d23-108">Attributes</span></span>

<span data-ttu-id="50d23-109">Keine</span><span class="sxs-lookup"><span data-stu-id="50d23-109">None</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="50d23-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="50d23-110">Child elements</span></span>

|<span data-ttu-id="50d23-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="50d23-111">**Element**</span></span>|<span data-ttu-id="50d23-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="50d23-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="50d23-113">URI (SOAP)</span><span class="sxs-lookup"><span data-stu-id="50d23-113">Uri (SOAP)</span></span>](uri-soap.md) <br/> |<span data-ttu-id="50d23-114">Der URI des Sicherheitstokendienst, der den Sicherheitstoken ausgestellt hat.</span><span class="sxs-lookup"><span data-stu-id="50d23-114">The URI of the security token service that issued the security token.</span></span>  <br/> |
|[<span data-ttu-id="50d23-115">Endpunkt (SOAP)</span><span class="sxs-lookup"><span data-stu-id="50d23-115">Endpoint (SOAP)</span></span>](endpoint-soap.md) <br/> |<span data-ttu-id="50d23-116">Der Endpunkt-URI des Webdiensts.</span><span class="sxs-lookup"><span data-stu-id="50d23-116">The web service Endpoint URI.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="50d23-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="50d23-117">Parent elements</span></span>

|<span data-ttu-id="50d23-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="50d23-118">**Element**</span></span>|<span data-ttu-id="50d23-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="50d23-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="50d23-120">TokenIssuers (SOAP)</span><span class="sxs-lookup"><span data-stu-id="50d23-120">TokenIssuers (SOAP)</span></span>](tokenissuers-soap.md) <br/> |<span data-ttu-id="50d23-121">Stellt eine Auflistung von Security Token Service [URI (SOAP)](uri-soap.md) und [EndPoint (SOAP)](endpoint-soap.md)dar.</span><span class="sxs-lookup"><span data-stu-id="50d23-121">Represents a collection of security token service [Uri (SOAP)](uri-soap.md) and [Endpoint (SOAP)](endpoint-soap.md).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="50d23-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="50d23-122">Remarks</span></span>

<span data-ttu-id="50d23-123">Verwenden Sie das **TokenIssuer** -Element, um den Sicherheitstokendienst Bei Verwendung von Sicherheitstoken anzugeben.</span><span class="sxs-lookup"><span data-stu-id="50d23-123">Use the **TokenIssuer** element to specify the security token service when using security tokens.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="50d23-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="50d23-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="50d23-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="50d23-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="50d23-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="50d23-126">Schema Name</span></span>  <br/> |<span data-ttu-id="50d23-127">Auto Ermittlungs Schema</span><span class="sxs-lookup"><span data-stu-id="50d23-127">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="50d23-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="50d23-128">Validation File</span></span>  <br/> |<span data-ttu-id="50d23-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="50d23-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="50d23-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="50d23-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="50d23-131">True</span><span class="sxs-lookup"><span data-stu-id="50d23-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="50d23-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="50d23-132">See also</span></span>



[<span data-ttu-id="50d23-133">AutoErmittlung Webdienstverweis für Exchange</span><span class="sxs-lookup"><span data-stu-id="50d23-133">Autodiscover web service reference for Exchange</span></span>](autodiscover-web-service-reference-for-exchange.md)
  
[<span data-ttu-id="50d23-134">XML-Elemente der SOAP-AutoErmittlung für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="50d23-134">SOAP Autodiscover XML elements for Exchange 2013</span></span>](soap-autodiscover-xml-elements-for-exchange-2013.md)

