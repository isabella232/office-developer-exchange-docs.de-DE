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
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831134"
---
# <a name="requestedversion-soap"></a><span data-ttu-id="e3f43-103">RequestedVersion (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e3f43-103">RequestedVersion (SOAP)</span></span>

<span data-ttu-id="e3f43-104">Das **RequestedVersion** -Element gibt die minimale Service-Version, die der Client die Anforderung auf verarbeitet werden möchte.</span><span class="sxs-lookup"><span data-stu-id="e3f43-104">The **RequestedVersion** element specifies the minimum service version that the client wants the request to be processed on.</span></span> 
  
```XML
<RequestedVersion/>
```

 <span data-ttu-id="e3f43-105">**ExchangeVersion**</span><span class="sxs-lookup"><span data-stu-id="e3f43-105">**ExchangeVersion**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e3f43-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e3f43-106">Attributes and elements</span></span>

<span data-ttu-id="e3f43-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e3f43-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e3f43-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="e3f43-108">Attributes</span></span>

<span data-ttu-id="e3f43-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="e3f43-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e3f43-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e3f43-110">Child elements</span></span>

<span data-ttu-id="e3f43-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="e3f43-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e3f43-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e3f43-112">Parent elements</span></span>

|<span data-ttu-id="e3f43-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="e3f43-113">**Element**</span></span>|<span data-ttu-id="e3f43-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e3f43-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e3f43-115">Anforderung (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e3f43-115">Request (SOAP)</span></span>](request-soap.md) <br/> |<span data-ttu-id="e3f43-116">Enthält die angeforderten Konfigurationseinstellungen und die Zielbenutzer.</span><span class="sxs-lookup"><span data-stu-id="e3f43-116">Contains the requested configuration settings and the target users.</span></span>  <br/> |
|[<span data-ttu-id="e3f43-117">Anforderung (GetDomainSettings) (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e3f43-117">Request (GetDomainSettings) (SOAP)</span></span>](request-getdomainsettingssoap.md) <br/> |<span data-ttu-id="e3f43-118">Stellt eine Anforderung an die domäneneinstellungen abrufen.</span><span class="sxs-lookup"><span data-stu-id="e3f43-118">Represents a request to get domain settings.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e3f43-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="e3f43-119">Text value</span></span>

<span data-ttu-id="e3f43-120">Der Textwert für das **RequestedVersion** -Element kann Exchange2010, Exchange2010_SP1, Exchange2010_SP2 oder Exchange2013 sein.</span><span class="sxs-lookup"><span data-stu-id="e3f43-120">The text value for the **RequestedVersion** element can be Exchange2010, Exchange2010_SP1, Exchange2010_SP2, or Exchange2013.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e3f43-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e3f43-121">Remarks</span></span>

<span data-ttu-id="e3f43-122">Wenn dieses Element nicht vorhanden ist, wird die neueste Service Version verwendet.</span><span class="sxs-lookup"><span data-stu-id="e3f43-122">If this element is not present, the latest service version is used.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e3f43-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="e3f43-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e3f43-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="e3f43-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="e3f43-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e3f43-125">Schema Name</span></span>  <br/> |<span data-ttu-id="e3f43-126">AutoErmittlung-schema</span><span class="sxs-lookup"><span data-stu-id="e3f43-126">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="e3f43-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e3f43-127">Validation File</span></span>  <br/> |<span data-ttu-id="e3f43-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="e3f43-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e3f43-129">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="e3f43-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="e3f43-130">False</span><span class="sxs-lookup"><span data-stu-id="e3f43-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e3f43-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e3f43-131">See also</span></span>



[<span data-ttu-id="e3f43-132">GetUserSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e3f43-132">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
  
[<span data-ttu-id="e3f43-133">GetDomainSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e3f43-133">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

