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
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460960"
---
# <a name="getdomainsettingsrequest-soap"></a><span data-ttu-id="8aa37-103">GetDomainSettingsRequest (SOAP)</span><span class="sxs-lookup"><span data-stu-id="8aa37-103">GetDomainSettingsRequest (SOAP)</span></span>

<span data-ttu-id="8aa37-104">Das **GetDomainSettingsRequest** -Element stellt eine [GetDomainSettings Operation (SOAP)-](getdomainsettings-operation-soap.md) Vorgangsanforderung dar.</span><span class="sxs-lookup"><span data-stu-id="8aa37-104">The **GetDomainSettingsRequest** element represents a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) operation request.</span></span> 
  
```XML
<GetDomainSettingsRequest>
   <Domains/>
   <RequestedSettings/>
   <RequestedVersion/>
</GetDomainSettingsRequest>
```

 <span data-ttu-id="8aa37-105">**GetDomainSettingsRequest**</span><span class="sxs-lookup"><span data-stu-id="8aa37-105">**GetDomainSettingsRequest**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8aa37-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="8aa37-106">Attributes and elements</span></span>

<span data-ttu-id="8aa37-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="8aa37-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8aa37-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="8aa37-108">Attributes</span></span>

<span data-ttu-id="8aa37-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="8aa37-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8aa37-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8aa37-110">Child elements</span></span>

|<span data-ttu-id="8aa37-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="8aa37-111">**Element**</span></span>|<span data-ttu-id="8aa37-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8aa37-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8aa37-113">Domänen (SOAP)</span><span class="sxs-lookup"><span data-stu-id="8aa37-113">Domains (SOAP)</span></span>](domains-soap.md) <br/> |<span data-ttu-id="8aa37-114">Stellt eine Auflistung von Domänen-IDs dar.</span><span class="sxs-lookup"><span data-stu-id="8aa37-114">Represents a collection of domain identifiers.</span></span>  <br/> |
|[<span data-ttu-id="8aa37-115">RequestedSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="8aa37-115">RequestedSettings (SOAP)</span></span>](requestedsettings-soap.md) <br/> |<span data-ttu-id="8aa37-116">Enthält die Namen der angeforderten Domänen Konfigurationseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="8aa37-116">Contains the names of the requested domain configuration settings.</span></span>  <br/> |
|[<span data-ttu-id="8aa37-117">RequestedVersion (SOAP)</span><span class="sxs-lookup"><span data-stu-id="8aa37-117">RequestedVersion (SOAP)</span></span>](requestedversion-soap.md) <br/> |<span data-ttu-id="8aa37-118">Gibt die Server Version an, die vom Anbieter verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8aa37-118">Specifies the server version that the provider will use.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8aa37-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8aa37-119">Parent elements</span></span>

<span data-ttu-id="8aa37-120">Keine.</span><span class="sxs-lookup"><span data-stu-id="8aa37-120">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="8aa37-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="8aa37-121">Text value</span></span>

<span data-ttu-id="8aa37-122">Keine.</span><span class="sxs-lookup"><span data-stu-id="8aa37-122">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8aa37-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="8aa37-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8aa37-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="8aa37-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="8aa37-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="8aa37-125">Schema Name</span></span>  <br/> |<span data-ttu-id="8aa37-126">Auto Ermittlungs Schema</span><span class="sxs-lookup"><span data-stu-id="8aa37-126">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="8aa37-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="8aa37-127">Validation File</span></span>  <br/> |<span data-ttu-id="8aa37-128">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="8aa37-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="8aa37-129">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="8aa37-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="8aa37-130">True</span><span class="sxs-lookup"><span data-stu-id="8aa37-130">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8aa37-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8aa37-131">See also</span></span>



[<span data-ttu-id="8aa37-132">GetDomainSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="8aa37-132">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

