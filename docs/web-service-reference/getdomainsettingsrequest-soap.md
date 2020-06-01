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
description: Das GetDomainSettingsRequest-Element stellt eine GetDomainSettings Operation (SOAP)-Vorgangsanforderung dar.
ms.openlocfilehash: 400016d0817131fb70ec7ff3db7fbfdc1b51f8f9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460960"
---
# <a name="getdomainsettingsrequest-soap"></a><span data-ttu-id="570dc-103">GetDomainSettingsRequest (SOAP)</span><span class="sxs-lookup"><span data-stu-id="570dc-103">GetDomainSettingsRequest (SOAP)</span></span>

<span data-ttu-id="570dc-104">Das **GetDomainSettingsRequest** -Element stellt eine [GetDomainSettings Operation (SOAP)-](getdomainsettings-operation-soap.md) Vorgangsanforderung dar.</span><span class="sxs-lookup"><span data-stu-id="570dc-104">The **GetDomainSettingsRequest** element represents a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) operation request.</span></span> 
  
```XML
<GetDomainSettingsRequest>
   <Domains/>
   <RequestedSettings/>
   <RequestedVersion/>
</GetDomainSettingsRequest>
```

 <span data-ttu-id="570dc-105">**GetDomainSettingsRequest**</span><span class="sxs-lookup"><span data-stu-id="570dc-105">**GetDomainSettingsRequest**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="570dc-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="570dc-106">Attributes and elements</span></span>

<span data-ttu-id="570dc-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="570dc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="570dc-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="570dc-108">Attributes</span></span>

<span data-ttu-id="570dc-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="570dc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="570dc-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="570dc-110">Child elements</span></span>

|<span data-ttu-id="570dc-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="570dc-111">**Element**</span></span>|<span data-ttu-id="570dc-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="570dc-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="570dc-113">Domänen (SOAP)</span><span class="sxs-lookup"><span data-stu-id="570dc-113">Domains (SOAP)</span></span>](domains-soap.md) <br/> |<span data-ttu-id="570dc-114">Stellt eine Auflistung von Domänen-IDs dar.</span><span class="sxs-lookup"><span data-stu-id="570dc-114">Represents a collection of domain identifiers.</span></span>  <br/> |
|[<span data-ttu-id="570dc-115">RequestedSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="570dc-115">RequestedSettings (SOAP)</span></span>](requestedsettings-soap.md) <br/> |<span data-ttu-id="570dc-116">Enthält die Namen der angeforderten Domänen Konfigurationseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="570dc-116">Contains the names of the requested domain configuration settings.</span></span>  <br/> |
|[<span data-ttu-id="570dc-117">RequestedVersion (SOAP)</span><span class="sxs-lookup"><span data-stu-id="570dc-117">RequestedVersion (SOAP)</span></span>](requestedversion-soap.md) <br/> |<span data-ttu-id="570dc-118">Gibt die Server Version an, die vom Anbieter verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="570dc-118">Specifies the server version that the provider will use.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="570dc-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="570dc-119">Parent elements</span></span>

<span data-ttu-id="570dc-120">Keine.</span><span class="sxs-lookup"><span data-stu-id="570dc-120">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="570dc-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="570dc-121">Text value</span></span>

<span data-ttu-id="570dc-122">Keine.</span><span class="sxs-lookup"><span data-stu-id="570dc-122">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="570dc-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="570dc-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="570dc-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="570dc-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="570dc-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="570dc-125">Schema Name</span></span>  <br/> |<span data-ttu-id="570dc-126">Auto Ermittlungs Schema</span><span class="sxs-lookup"><span data-stu-id="570dc-126">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="570dc-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="570dc-127">Validation File</span></span>  <br/> |<span data-ttu-id="570dc-128">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="570dc-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="570dc-129">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="570dc-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="570dc-130">True</span><span class="sxs-lookup"><span data-stu-id="570dc-130">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="570dc-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="570dc-131">See also</span></span>



[<span data-ttu-id="570dc-132">GetDomainSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="570dc-132">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

