---
title: RequestedVersion (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 962036c9-9b13-4669-bed2-2502c0f5aabe
description: Das RequestedVersion-Element gibt die minimale Service-Version, die der Client die Anforderung auf verarbeitet werden möchte.
ms.openlocfilehash: 0d8682c33790d2d26001512ad9e2191ae52074d0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831134"
---
# <a name="requestedversion-soap"></a><span data-ttu-id="b85b7-103">RequestedVersion (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b85b7-103">RequestedVersion (SOAP)</span></span>

<span data-ttu-id="b85b7-104">Das **RequestedVersion** -Element gibt die minimale Service-Version, die der Client die Anforderung auf verarbeitet werden möchte.</span><span class="sxs-lookup"><span data-stu-id="b85b7-104">The **RequestedVersion** element specifies the minimum service version that the client wants the request to be processed on.</span></span> 
  
```XML
<RequestedVersion/>
```

 <span data-ttu-id="b85b7-105">**ExchangeVersion**</span><span class="sxs-lookup"><span data-stu-id="b85b7-105">**ExchangeVersion**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b85b7-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b85b7-106">Attributes and elements</span></span>

<span data-ttu-id="b85b7-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b85b7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b85b7-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="b85b7-108">Attributes</span></span>

<span data-ttu-id="b85b7-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="b85b7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b85b7-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b85b7-110">Child elements</span></span>

<span data-ttu-id="b85b7-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="b85b7-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b85b7-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b85b7-112">Parent elements</span></span>

|<span data-ttu-id="b85b7-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="b85b7-113">**Element**</span></span>|<span data-ttu-id="b85b7-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b85b7-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b85b7-115">Anforderung (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b85b7-115">Request (SOAP)</span></span>](request-soap.md) <br/> |<span data-ttu-id="b85b7-116">Enthält die angeforderten Konfigurationseinstellungen und die Zielbenutzer.</span><span class="sxs-lookup"><span data-stu-id="b85b7-116">Contains the requested configuration settings and the target users.</span></span>  <br/> |
|[<span data-ttu-id="b85b7-117">Anforderung (GetDomainSettings) (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b85b7-117">Request (GetDomainSettings) (SOAP)</span></span>](request-getdomainsettingssoap.md) <br/> |<span data-ttu-id="b85b7-118">Stellt eine Anforderung an die domäneneinstellungen abrufen.</span><span class="sxs-lookup"><span data-stu-id="b85b7-118">Represents a request to get domain settings.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b85b7-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="b85b7-119">Text value</span></span>

<span data-ttu-id="b85b7-120">Der Textwert für das **RequestedVersion** -Element kann Exchange2010, Exchange2010_SP1, Exchange2010_SP2 oder Exchange2013 sein.</span><span class="sxs-lookup"><span data-stu-id="b85b7-120">The text value for the **RequestedVersion** element can be Exchange2010, Exchange2010_SP1, Exchange2010_SP2, or Exchange2013.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b85b7-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b85b7-121">Remarks</span></span>

<span data-ttu-id="b85b7-122">Wenn dieses Element nicht vorhanden ist, wird die neueste Service Version verwendet.</span><span class="sxs-lookup"><span data-stu-id="b85b7-122">If this element is not present, the latest service version is used.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b85b7-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="b85b7-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b85b7-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="b85b7-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="b85b7-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b85b7-125">Schema Name</span></span>  <br/> |<span data-ttu-id="b85b7-126">AutoErmittlung-schema</span><span class="sxs-lookup"><span data-stu-id="b85b7-126">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="b85b7-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b85b7-127">Validation File</span></span>  <br/> |<span data-ttu-id="b85b7-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="b85b7-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b85b7-129">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="b85b7-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="b85b7-130">False</span><span class="sxs-lookup"><span data-stu-id="b85b7-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b85b7-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b85b7-131">See also</span></span>



[<span data-ttu-id="b85b7-132">GetUserSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b85b7-132">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
  
[<span data-ttu-id="b85b7-133">GetDomainSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b85b7-133">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

