---
title: TokenIssuers (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 26c55228-184e-4340-bd80-f86be56f3e7a
description: Die Elemente TokenIssuers stellt die Auflistung TokenIssuer (SOAP) dar.
ms.openlocfilehash: b070d85b32d5bce8461ac4e930329f237885bad7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839232"
---
# <a name="tokenissuers-soap"></a><span data-ttu-id="2b5fd-103">TokenIssuers (SOAP)</span><span class="sxs-lookup"><span data-stu-id="2b5fd-103">TokenIssuers (SOAP)</span></span>

<span data-ttu-id="2b5fd-104">Die Elemente **TokenIssuers** stellt die Auflistung [TokenIssuer (SOAP)](tokenissuer-soap.md) dar.</span><span class="sxs-lookup"><span data-stu-id="2b5fd-104">The **TokenIssuers** elements represents the [TokenIssuer (SOAP)](tokenissuer-soap.md) collection.</span></span> 
  
```XML
<TokenIssuers>
    <TokenIssuer/>
</TokenIssuers>
```

 <span data-ttu-id="2b5fd-105">**TokenIssuers**</span><span class="sxs-lookup"><span data-stu-id="2b5fd-105">**TokenIssuers**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2b5fd-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="2b5fd-106">Attributes and elements</span></span>

<span data-ttu-id="2b5fd-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="2b5fd-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2b5fd-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="2b5fd-108">Attributes</span></span>

<span data-ttu-id="2b5fd-109">Keine</span><span class="sxs-lookup"><span data-stu-id="2b5fd-109">None</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2b5fd-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2b5fd-110">Child elements</span></span>

|<span data-ttu-id="2b5fd-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="2b5fd-111">**Element**</span></span>|<span data-ttu-id="2b5fd-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2b5fd-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2b5fd-113">TokenIssuer (SOAP)</span><span class="sxs-lookup"><span data-stu-id="2b5fd-113">TokenIssuer (SOAP)</span></span>](tokenissuer-soap.md) <br/> |<span data-ttu-id="2b5fd-114">Gibt den [Uri (SOAP)](uri-soap.md) und [Endpunkt (SOAP)](endpoint-soap.md) für den Sicherheitstokendienst an.</span><span class="sxs-lookup"><span data-stu-id="2b5fd-114">Specifies the [Uri (SOAP)](uri-soap.md) and [Endpoint (SOAP)](endpoint-soap.md) for the security token service.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2b5fd-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2b5fd-115">Parent elements</span></span>

|<span data-ttu-id="2b5fd-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="2b5fd-116">**Element**</span></span>|<span data-ttu-id="2b5fd-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2b5fd-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2b5fd-118">GetFederationInformationResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="2b5fd-118">GetFederationInformationResponse (SOAP)</span></span>](getfederationinformationresponse-soap.md) <br/> |<span data-ttu-id="2b5fd-119">Enthält die Antwort [GetFederationInformation-Vorgang (SOAP)](getfederationinformation-operation-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="2b5fd-119">Contains the [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md) response.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2b5fd-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2b5fd-120">Remarks</span></span>

<span data-ttu-id="2b5fd-121">Die **TokenIssuers** stellt eine Sammlung von [TokenIssuer (SOAP)](tokenissuer-soap.md) -Elementen in der AutoErmittlung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2b5fd-121">The **TokenIssuers** represents a collection of [TokenIssuer (SOAP)](tokenissuer-soap.md) elements to be used in the Autodiscovery.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="2b5fd-122">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="2b5fd-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2b5fd-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="2b5fd-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="2b5fd-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="2b5fd-124">Schema Name</span></span>  <br/> |<span data-ttu-id="2b5fd-125">AutoErmittlung-schema</span><span class="sxs-lookup"><span data-stu-id="2b5fd-125">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="2b5fd-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="2b5fd-126">Validation File</span></span>  <br/> |<span data-ttu-id="2b5fd-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="2b5fd-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2b5fd-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="2b5fd-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="2b5fd-129">True</span><span class="sxs-lookup"><span data-stu-id="2b5fd-129">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2b5fd-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2b5fd-130">See also</span></span>



[<span data-ttu-id="2b5fd-131">AutoErmittlung Webdienstverweis für Exchange</span><span class="sxs-lookup"><span data-stu-id="2b5fd-131">Autodiscover web service reference for Exchange</span></span>](autodiscover-web-service-reference-for-exchange.md)
  
[<span data-ttu-id="2b5fd-132">SOAP-Autodiscover XML-Elemente für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="2b5fd-132">SOAP Autodiscover XML elements for Exchange 2013</span></span>](soap-autodiscover-xml-elements-for-exchange-2013.md)

