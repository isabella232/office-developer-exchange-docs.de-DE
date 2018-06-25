---
title: GetDomainSettingsRequest (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 5ac0ff6d-9e02-4e4c-973d-cd9e076661d5
description: Das GetDomainSettingsRequest-Element stellt eine Anforderung GetDomainSettings-Vorgang (SOAP)-Operation dar.
ms.openlocfilehash: 4de525a9ba47a0d9afb0d6db9200fe32845f31d0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758639"
---
# <a name="getdomainsettingsrequest-soap"></a><span data-ttu-id="e8146-103">GetDomainSettingsRequest (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e8146-103">GetDomainSettingsRequest (SOAP)</span></span>

<span data-ttu-id="e8146-104">Das **GetDomainSettingsRequest** -Element stellt die Anforderung einer [GetDomainSettings-Vorgang (SOAP)](getdomainsettings-operation-soap.md) -Operation dar.</span><span class="sxs-lookup"><span data-stu-id="e8146-104">The **GetDomainSettingsRequest** element represents a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) operation request.</span></span> 
  
```XML
<GetDomainSettingsRequest>
   <Domains/>
   <RequestedSettings/>
   <RequestedVersion/>
</GetDomainSettingsRequest>
```

 <span data-ttu-id="e8146-105">**GetDomainSettingsRequest**</span><span class="sxs-lookup"><span data-stu-id="e8146-105">**GetDomainSettingsRequest**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e8146-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e8146-106">Attributes and elements</span></span>

<span data-ttu-id="e8146-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e8146-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e8146-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="e8146-108">Attributes</span></span>

<span data-ttu-id="e8146-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="e8146-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e8146-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e8146-110">Child elements</span></span>

|<span data-ttu-id="e8146-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="e8146-111">**Element**</span></span>|<span data-ttu-id="e8146-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e8146-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e8146-113">Domänen (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e8146-113">Domains (SOAP)</span></span>](domains-soap.md) <br/> |<span data-ttu-id="e8146-114">Stellt eine Sammlung von Bezeichnern Domäne dar.</span><span class="sxs-lookup"><span data-stu-id="e8146-114">Represents a collection of domain identifiers.</span></span>  <br/> |
|[<span data-ttu-id="e8146-115">RequestedSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e8146-115">RequestedSettings (SOAP)</span></span>](requestedsettings-soap.md) <br/> |<span data-ttu-id="e8146-116">Enthält die Namen der Konfigurationseinstellungen für die angeforderte Domäne.</span><span class="sxs-lookup"><span data-stu-id="e8146-116">Contains the names of the requested domain configuration settings.</span></span>  <br/> |
|[<span data-ttu-id="e8146-117">RequestedVersion (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e8146-117">RequestedVersion (SOAP)</span></span>](requestedversion-soap.md) <br/> |<span data-ttu-id="e8146-118">Gibt die Serverversion, die der Anbieter verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e8146-118">Specifies the server version that the provider will use.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e8146-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e8146-119">Parent elements</span></span>

<span data-ttu-id="e8146-120">Keine.</span><span class="sxs-lookup"><span data-stu-id="e8146-120">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="e8146-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="e8146-121">Text value</span></span>

<span data-ttu-id="e8146-122">Keine.</span><span class="sxs-lookup"><span data-stu-id="e8146-122">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e8146-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="e8146-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e8146-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="e8146-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="e8146-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e8146-125">Schema Name</span></span>  <br/> |<span data-ttu-id="e8146-126">AutoErmittlung-schema</span><span class="sxs-lookup"><span data-stu-id="e8146-126">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="e8146-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e8146-127">Validation File</span></span>  <br/> |<span data-ttu-id="e8146-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="e8146-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e8146-129">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="e8146-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="e8146-130">True</span><span class="sxs-lookup"><span data-stu-id="e8146-130">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e8146-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e8146-131">See also</span></span>



[<span data-ttu-id="e8146-132">GetDomainSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e8146-132">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

