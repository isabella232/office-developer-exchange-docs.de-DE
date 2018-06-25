---
title: TokenIssuer (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2d7be675-626c-4173-89e9-e32beef81ad5
description: Das TokenIssuer-Element gibt den Uri (SOAP) und Endpunkt (SOAP) für den Sicherheitstokendienst.
ms.openlocfilehash: 1c267fc6cbfdadd471c568473cc9aeeafb43ae2d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839220"
---
# <a name="tokenissuer-soap"></a><span data-ttu-id="d243f-103">TokenIssuer (SOAP)</span><span class="sxs-lookup"><span data-stu-id="d243f-103">TokenIssuer (SOAP)</span></span>

<span data-ttu-id="d243f-104">Das **TokenIssuer** -Element gibt den [Uri (SOAP)](uri-soap.md) und [Endpunkt (SOAP)](endpoint-soap.md) für den Sicherheitstokendienst.</span><span class="sxs-lookup"><span data-stu-id="d243f-104">The **TokenIssuer** element specifies the [Uri (SOAP)](uri-soap.md) and [Endpoint (SOAP)](endpoint-soap.md) for the security token service.</span></span> 
  
```XML
<TokenIssuer>
   <Uri/>
   <Endpoint/>
</TokenIssuer>
```

 <span data-ttu-id="d243f-105">**TokenIssuer**</span><span class="sxs-lookup"><span data-stu-id="d243f-105">**TokenIssuer**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d243f-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d243f-106">Attributes and elements</span></span>

<span data-ttu-id="d243f-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d243f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d243f-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d243f-108">Attributes</span></span>

<span data-ttu-id="d243f-109">Keine</span><span class="sxs-lookup"><span data-stu-id="d243f-109">None</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d243f-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d243f-110">Child elements</span></span>

|<span data-ttu-id="d243f-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="d243f-111">**Element**</span></span>|<span data-ttu-id="d243f-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d243f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d243f-113">Der URI (SOAP)</span><span class="sxs-lookup"><span data-stu-id="d243f-113">Uri (SOAP)</span></span>](uri-soap.md) <br/> |<span data-ttu-id="d243f-114">Der URI des Sicherheitstokendiensts, der das Sicherheitstoken ausgestellt hat.</span><span class="sxs-lookup"><span data-stu-id="d243f-114">The URI of the security token service that issued the security token.</span></span>  <br/> |
|[<span data-ttu-id="d243f-115">Endpunkt (SOAP)</span><span class="sxs-lookup"><span data-stu-id="d243f-115">Endpoint (SOAP)</span></span>](endpoint-soap.md) <br/> |<span data-ttu-id="d243f-116">Der Webdienst-Endpunkt-URI.</span><span class="sxs-lookup"><span data-stu-id="d243f-116">The web service Endpoint URI.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d243f-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d243f-117">Parent elements</span></span>

|<span data-ttu-id="d243f-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="d243f-118">**Element**</span></span>|<span data-ttu-id="d243f-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d243f-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d243f-120">TokenIssuers (SOAP)</span><span class="sxs-lookup"><span data-stu-id="d243f-120">TokenIssuers (SOAP)</span></span>](tokenissuers-soap.md) <br/> |<span data-ttu-id="d243f-121">Stellt eine Auflistung von Sicherheitstokendienst [Uri (SOAP)](uri-soap.md) und [Endpunkt (SOAP)](endpoint-soap.md).</span><span class="sxs-lookup"><span data-stu-id="d243f-121">Represents a collection of security token service [Uri (SOAP)](uri-soap.md) and [Endpoint (SOAP)](endpoint-soap.md).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d243f-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d243f-122">Remarks</span></span>

<span data-ttu-id="d243f-123">Verwenden Sie das **TokenIssuer** -Element des Sicherheitstokendiensts an, wann Sicherheitstoken verwenden.</span><span class="sxs-lookup"><span data-stu-id="d243f-123">Use the **TokenIssuer** element to specify the security token service when using security tokens.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="d243f-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="d243f-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d243f-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="d243f-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="d243f-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d243f-126">Schema Name</span></span>  <br/> |<span data-ttu-id="d243f-127">AutoErmittlung-schema</span><span class="sxs-lookup"><span data-stu-id="d243f-127">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="d243f-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d243f-128">Validation File</span></span>  <br/> |<span data-ttu-id="d243f-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="d243f-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d243f-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d243f-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="d243f-131">True</span><span class="sxs-lookup"><span data-stu-id="d243f-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d243f-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d243f-132">See also</span></span>



[<span data-ttu-id="d243f-133">AutoErmittlung Webdienstverweis für Exchange</span><span class="sxs-lookup"><span data-stu-id="d243f-133">Autodiscover web service reference for Exchange</span></span>](autodiscover-web-service-reference-for-exchange.md)
  
[<span data-ttu-id="d243f-134">SOAP-Autodiscover XML-Elemente für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="d243f-134">SOAP Autodiscover XML elements for Exchange 2013</span></span>](soap-autodiscover-xml-elements-for-exchange-2013.md)

