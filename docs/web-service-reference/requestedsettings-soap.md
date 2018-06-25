---
title: RequestedSettings (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 8d713d22-580c-49a5-99f5-ee532443e89a
description: Das RequestedSettings-Element enthält die Namen der angeforderten Konfigurationseinstellungen für die.
ms.openlocfilehash: 025f86d417ea2041a3247ac67b065d75c8f75599
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831136"
---
# <a name="requestedsettings-soap"></a><span data-ttu-id="36920-103">RequestedSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="36920-103">RequestedSettings (SOAP)</span></span>

<span data-ttu-id="36920-104">Das **RequestedSettings** -Element enthält die Namen der angeforderten Konfigurationseinstellungen für die.</span><span class="sxs-lookup"><span data-stu-id="36920-104">The **RequestedSettings** element contains the names of the requested configuration settings.</span></span> 
  
```XML
<RequestedSettings>
   <Setting/>
</RequestedSettings>
```

 <span data-ttu-id="36920-105">**RequestedSettings**</span><span class="sxs-lookup"><span data-stu-id="36920-105">**RequestedSettings**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="36920-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="36920-106">Attributes and elements</span></span>

<span data-ttu-id="36920-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="36920-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="36920-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="36920-108">Attributes</span></span>

<span data-ttu-id="36920-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="36920-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="36920-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="36920-110">Child elements</span></span>

|<span data-ttu-id="36920-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="36920-111">**Element**</span></span>|<span data-ttu-id="36920-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="36920-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="36920-113">Einstellung (SOAP)</span><span class="sxs-lookup"><span data-stu-id="36920-113">Setting (SOAP)</span></span>](setting-soap.md) <br/> |<span data-ttu-id="36920-114">Stellt eine Konfigurationseinstellung zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="36920-114">Represents a configuration setting to be returned.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="36920-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="36920-115">Parent elements</span></span>

|<span data-ttu-id="36920-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="36920-116">**Element**</span></span>|<span data-ttu-id="36920-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="36920-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="36920-118">GetUserSettingsRequest (SOAP)</span><span class="sxs-lookup"><span data-stu-id="36920-118">GetUserSettingsRequest (SOAP)</span></span>](getusersettingsrequest-soap.md) <br/> |<span data-ttu-id="36920-119">Stellt eine Anforderung an die angegebene Einstellungen für einen oder mehrere Benutzer abzurufen.</span><span class="sxs-lookup"><span data-stu-id="36920-119">Represents a request to retrieve specified settings for one or more users.</span></span>  <br/> |
|[<span data-ttu-id="36920-120">Anforderung (SOAP)</span><span class="sxs-lookup"><span data-stu-id="36920-120">Request (SOAP)</span></span>](request-soap.md) <br/> |<span data-ttu-id="36920-121">Enthält die angeforderten Konfigurationseinstellungen und die Zielbenutzer.</span><span class="sxs-lookup"><span data-stu-id="36920-121">Contains the requested configuration settings and the target users.</span></span>  <br/> |
|[<span data-ttu-id="36920-122">GetDomainSettingsRequest (SOAP)</span><span class="sxs-lookup"><span data-stu-id="36920-122">GetDomainSettingsRequest (SOAP)</span></span>](getdomainsettingsrequest-soap.md) <br/> |<span data-ttu-id="36920-123">Stellt eine Anforderung [GetDomainSettings-Vorgang (SOAP)](getdomainsettings-operation-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="36920-123">Represents a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) request.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="36920-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="36920-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="36920-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="36920-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="36920-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="36920-126">Schema Name</span></span>  <br/> |<span data-ttu-id="36920-127">AutoErmittlung-schema</span><span class="sxs-lookup"><span data-stu-id="36920-127">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="36920-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="36920-128">Validation File</span></span>  <br/> |<span data-ttu-id="36920-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="36920-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="36920-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="36920-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="36920-131">True</span><span class="sxs-lookup"><span data-stu-id="36920-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="36920-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="36920-132">See also</span></span>



[<span data-ttu-id="36920-133">GetUserSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="36920-133">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
  
[<span data-ttu-id="36920-134">GetDomainSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="36920-134">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

