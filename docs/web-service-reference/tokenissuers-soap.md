---
title: TokenIssuers (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 26c55228-184e-4340-bd80-f86be56f3e7a
description: Die TokenIssuers-Elemente stellt die TokenIssuer (SOAP)-Auflistung dar.
ms.openlocfilehash: 352487ad3fd9c1ee7de756a109fb98a49d0cdcd7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457074"
---
# <a name="tokenissuers-soap"></a><span data-ttu-id="419c4-103">TokenIssuers (SOAP)</span><span class="sxs-lookup"><span data-stu-id="419c4-103">TokenIssuers (SOAP)</span></span>

<span data-ttu-id="419c4-104">Die **TokenIssuers** -Elemente stellt die [TokenIssuer (SOAP)](tokenissuer-soap.md) -Auflistung dar.</span><span class="sxs-lookup"><span data-stu-id="419c4-104">The **TokenIssuers** elements represents the [TokenIssuer (SOAP)](tokenissuer-soap.md) collection.</span></span> 
  
```XML
<TokenIssuers>
    <TokenIssuer/>
</TokenIssuers>
```

 <span data-ttu-id="419c4-105">**TokenIssuers**</span><span class="sxs-lookup"><span data-stu-id="419c4-105">**TokenIssuers**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="419c4-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="419c4-106">Attributes and elements</span></span>

<span data-ttu-id="419c4-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="419c4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="419c4-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="419c4-108">Attributes</span></span>

<span data-ttu-id="419c4-109">Keine</span><span class="sxs-lookup"><span data-stu-id="419c4-109">None</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="419c4-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="419c4-110">Child elements</span></span>

|<span data-ttu-id="419c4-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="419c4-111">**Element**</span></span>|<span data-ttu-id="419c4-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="419c4-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="419c4-113">TokenIssuer (SOAP)</span><span class="sxs-lookup"><span data-stu-id="419c4-113">TokenIssuer (SOAP)</span></span>](tokenissuer-soap.md) <br/> |<span data-ttu-id="419c4-114">Gibt den [URI (SOAP)](uri-soap.md) und den [Endpunkt (SOAP)](endpoint-soap.md) für den Sicherheitstokendienst an.</span><span class="sxs-lookup"><span data-stu-id="419c4-114">Specifies the [Uri (SOAP)](uri-soap.md) and [Endpoint (SOAP)](endpoint-soap.md) for the security token service.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="419c4-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="419c4-115">Parent elements</span></span>

|<span data-ttu-id="419c4-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="419c4-116">**Element**</span></span>|<span data-ttu-id="419c4-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="419c4-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="419c4-118">GetFederationInformationResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="419c4-118">GetFederationInformationResponse (SOAP)</span></span>](getfederationinformationresponse-soap.md) <br/> |<span data-ttu-id="419c4-119">Enthält die [SOAP-Antwort (GetFederationInformation Operation)](getfederationinformation-operation-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="419c4-119">Contains the [GetFederationInformation operation (SOAP)](getfederationinformation-operation-soap.md) response.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="419c4-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="419c4-120">Remarks</span></span>

<span data-ttu-id="419c4-121">Das **TokenIssuers** stellt eine Auflistung von [TokenIssuer (SOAP)-](tokenissuer-soap.md) Elementen dar, die in der AutoDiscovery verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="419c4-121">The **TokenIssuers** represents a collection of [TokenIssuer (SOAP)](tokenissuer-soap.md) elements to be used in the Autodiscovery.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="419c4-122">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="419c4-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="419c4-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="419c4-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="419c4-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="419c4-124">Schema Name</span></span>  <br/> |<span data-ttu-id="419c4-125">Auto Ermittlungs Schema</span><span class="sxs-lookup"><span data-stu-id="419c4-125">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="419c4-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="419c4-126">Validation File</span></span>  <br/> |<span data-ttu-id="419c4-127">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="419c4-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="419c4-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="419c4-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="419c4-129">True</span><span class="sxs-lookup"><span data-stu-id="419c4-129">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="419c4-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="419c4-130">See also</span></span>



[<span data-ttu-id="419c4-131">AutoErmittlung Webdienstverweis für Exchange</span><span class="sxs-lookup"><span data-stu-id="419c4-131">Autodiscover web service reference for Exchange</span></span>](autodiscover-web-service-reference-for-exchange.md)
  
[<span data-ttu-id="419c4-132">XML-Elemente der SOAP-AutoErmittlung für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="419c4-132">SOAP Autodiscover XML elements for Exchange 2013</span></span>](soap-autodiscover-xml-elements-for-exchange-2013.md)

