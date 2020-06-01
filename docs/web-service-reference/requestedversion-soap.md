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
description: Das RequestedVersion-Element gibt die minimale Dienstversion an, für die der Client die Anforderung verarbeiten möchte.
ms.openlocfilehash: ded276b3eb2c70b6edd39ca12289098de2b3faea
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459167"
---
# <a name="requestedversion-soap"></a><span data-ttu-id="384e2-103">RequestedVersion (SOAP)</span><span class="sxs-lookup"><span data-stu-id="384e2-103">RequestedVersion (SOAP)</span></span>

<span data-ttu-id="384e2-104">Das **RequestedVersion** -Element gibt die minimale Dienstversion an, für die der Client die Anforderung verarbeiten möchte.</span><span class="sxs-lookup"><span data-stu-id="384e2-104">The **RequestedVersion** element specifies the minimum service version that the client wants the request to be processed on.</span></span> 
  
```XML
<RequestedVersion/>
```

 <span data-ttu-id="384e2-105">**ExchangeVersion**</span><span class="sxs-lookup"><span data-stu-id="384e2-105">**ExchangeVersion**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="384e2-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="384e2-106">Attributes and elements</span></span>

<span data-ttu-id="384e2-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="384e2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="384e2-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="384e2-108">Attributes</span></span>

<span data-ttu-id="384e2-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="384e2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="384e2-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="384e2-110">Child elements</span></span>

<span data-ttu-id="384e2-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="384e2-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="384e2-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="384e2-112">Parent elements</span></span>

|<span data-ttu-id="384e2-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="384e2-113">**Element**</span></span>|<span data-ttu-id="384e2-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="384e2-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="384e2-115">Request (SOAP)</span><span class="sxs-lookup"><span data-stu-id="384e2-115">Request (SOAP)</span></span>](request-soap.md) <br/> |<span data-ttu-id="384e2-116">Enthält die angeforderten Konfigurationseinstellungen und die Zielbenutzer.</span><span class="sxs-lookup"><span data-stu-id="384e2-116">Contains the requested configuration settings and the target users.</span></span>  <br/> |
|[<span data-ttu-id="384e2-117">Request (GetDomainSettings) (SOAP)</span><span class="sxs-lookup"><span data-stu-id="384e2-117">Request (GetDomainSettings) (SOAP)</span></span>](request-getdomainsettingssoap.md) <br/> |<span data-ttu-id="384e2-118">Stellt eine Anforderung zum Abrufen von Domäneneinstellungen dar.</span><span class="sxs-lookup"><span data-stu-id="384e2-118">Represents a request to get domain settings.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="384e2-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="384e2-119">Text value</span></span>

<span data-ttu-id="384e2-120">Der Textwert für das **RequestedVersion** -Element kann Exchange2010, Exchange2010_SP1, Exchange2010_SP2 oder Exchange2013 sein.</span><span class="sxs-lookup"><span data-stu-id="384e2-120">The text value for the **RequestedVersion** element can be Exchange2010, Exchange2010_SP1, Exchange2010_SP2, or Exchange2013.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="384e2-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="384e2-121">Remarks</span></span>

<span data-ttu-id="384e2-122">Wenn dieses Element nicht vorhanden ist, wird die neueste Dienstversion verwendet.</span><span class="sxs-lookup"><span data-stu-id="384e2-122">If this element is not present, the latest service version is used.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="384e2-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="384e2-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="384e2-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="384e2-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="384e2-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="384e2-125">Schema Name</span></span>  <br/> |<span data-ttu-id="384e2-126">Auto Ermittlungs Schema</span><span class="sxs-lookup"><span data-stu-id="384e2-126">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="384e2-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="384e2-127">Validation File</span></span>  <br/> |<span data-ttu-id="384e2-128">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="384e2-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="384e2-129">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="384e2-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="384e2-130">False</span><span class="sxs-lookup"><span data-stu-id="384e2-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="384e2-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="384e2-131">See also</span></span>



[<span data-ttu-id="384e2-132">GetUserSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="384e2-132">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
  
[<span data-ttu-id="384e2-133">GetDomainSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="384e2-133">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

