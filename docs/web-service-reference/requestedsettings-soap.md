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
description: Das RequestedSettings-Element enthält die Namen der angeforderten Konfigurationseinstellungen.
ms.openlocfilehash: e94c02d8f92d7aaac619c58f093c536cc1a098bf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465296"
---
# <a name="requestedsettings-soap"></a><span data-ttu-id="32ca0-103">RequestedSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="32ca0-103">RequestedSettings (SOAP)</span></span>

<span data-ttu-id="32ca0-104">Das **RequestedSettings** -Element enthält die Namen der angeforderten Konfigurationseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="32ca0-104">The **RequestedSettings** element contains the names of the requested configuration settings.</span></span> 
  
```XML
<RequestedSettings>
   <Setting/>
</RequestedSettings>
```

 <span data-ttu-id="32ca0-105">**RequestedSettings**</span><span class="sxs-lookup"><span data-stu-id="32ca0-105">**RequestedSettings**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="32ca0-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="32ca0-106">Attributes and elements</span></span>

<span data-ttu-id="32ca0-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="32ca0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="32ca0-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="32ca0-108">Attributes</span></span>

<span data-ttu-id="32ca0-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="32ca0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="32ca0-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="32ca0-110">Child elements</span></span>

|<span data-ttu-id="32ca0-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="32ca0-111">**Element**</span></span>|<span data-ttu-id="32ca0-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="32ca0-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="32ca0-113">Einstellung (SOAP)</span><span class="sxs-lookup"><span data-stu-id="32ca0-113">Setting (SOAP)</span></span>](setting-soap.md) <br/> |<span data-ttu-id="32ca0-114">Stellt eine zurückzugebende Konfigurationseinstellung dar.</span><span class="sxs-lookup"><span data-stu-id="32ca0-114">Represents a configuration setting to be returned.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="32ca0-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="32ca0-115">Parent elements</span></span>

|<span data-ttu-id="32ca0-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="32ca0-116">**Element**</span></span>|<span data-ttu-id="32ca0-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="32ca0-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="32ca0-118">GetUserSettingsRequest (SOAP)</span><span class="sxs-lookup"><span data-stu-id="32ca0-118">GetUserSettingsRequest (SOAP)</span></span>](getusersettingsrequest-soap.md) <br/> |<span data-ttu-id="32ca0-119">Stellt eine Anforderung zum Abrufen der angegebenen Einstellungen für einen oder mehrere Benutzer dar.</span><span class="sxs-lookup"><span data-stu-id="32ca0-119">Represents a request to retrieve specified settings for one or more users.</span></span>  <br/> |
|[<span data-ttu-id="32ca0-120">Request (SOAP)</span><span class="sxs-lookup"><span data-stu-id="32ca0-120">Request (SOAP)</span></span>](request-soap.md) <br/> |<span data-ttu-id="32ca0-121">Enthält die angeforderten Konfigurationseinstellungen und die Zielbenutzer.</span><span class="sxs-lookup"><span data-stu-id="32ca0-121">Contains the requested configuration settings and the target users.</span></span>  <br/> |
|[<span data-ttu-id="32ca0-122">GetDomainSettingsRequest (SOAP)</span><span class="sxs-lookup"><span data-stu-id="32ca0-122">GetDomainSettingsRequest (SOAP)</span></span>](getdomainsettingsrequest-soap.md) <br/> |<span data-ttu-id="32ca0-123">Stellt eine [SOAP-Anforderung (GetDomainSettings Operation)](getdomainsettings-operation-soap.md) dar.</span><span class="sxs-lookup"><span data-stu-id="32ca0-123">Represents a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) request.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="32ca0-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="32ca0-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="32ca0-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="32ca0-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="32ca0-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="32ca0-126">Schema Name</span></span>  <br/> |<span data-ttu-id="32ca0-127">Auto Ermittlungs Schema</span><span class="sxs-lookup"><span data-stu-id="32ca0-127">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="32ca0-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="32ca0-128">Validation File</span></span>  <br/> |<span data-ttu-id="32ca0-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="32ca0-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="32ca0-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="32ca0-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="32ca0-131">True</span><span class="sxs-lookup"><span data-stu-id="32ca0-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="32ca0-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="32ca0-132">See also</span></span>



[<span data-ttu-id="32ca0-133">GetUserSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="32ca0-133">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
  
[<span data-ttu-id="32ca0-134">GetDomainSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="32ca0-134">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

