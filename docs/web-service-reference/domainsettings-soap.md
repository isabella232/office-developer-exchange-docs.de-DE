---
title: DomainSettings (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: f3d37f5a-c9ea-4ed9-a011-94d33bda64d1
description: Das Element DomainSettings stellt die domäneneinstellungen, die in einer autoermittlungsanforderung für die gesendet oder von einer Antwort der AutoErmittlung zurückgegeben wurden.
ms.openlocfilehash: 961051399dc8babd8cba6eeaf43456071d0f40a6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758108"
---
# <a name="domainsettings-soap"></a><span data-ttu-id="cdd1d-103">DomainSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="cdd1d-103">DomainSettings (SOAP)</span></span>

<span data-ttu-id="cdd1d-104">Das Element **DomainSettings** stellt die domäneneinstellungen, die in einer autoermittlungsanforderung für die gesendet oder von einer Antwort der AutoErmittlung zurückgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="cdd1d-104">The **DomainSettings** element represents the domain settings that were submitted in an Autodiscover request or returned by an Autodiscover response.</span></span> 
  
```XML
<DomainSettings>
   <DomainSetting/>
</DomainSettings>
```

 <span data-ttu-id="cdd1d-105">**DomainSettings**</span><span class="sxs-lookup"><span data-stu-id="cdd1d-105">**DomainSettings**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cdd1d-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="cdd1d-106">Attributes and elements</span></span>

<span data-ttu-id="cdd1d-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="cdd1d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cdd1d-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="cdd1d-108">Attributes</span></span>

<span data-ttu-id="cdd1d-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="cdd1d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cdd1d-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cdd1d-110">Child elements</span></span>

|<span data-ttu-id="cdd1d-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="cdd1d-111">**Element**</span></span>|<span data-ttu-id="cdd1d-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cdd1d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cdd1d-113">DomainSetting (SOAP)</span><span class="sxs-lookup"><span data-stu-id="cdd1d-113">DomainSetting (SOAP)</span></span>](domainsetting-soap.md) <br/> |<span data-ttu-id="cdd1d-114">Enthält domäneneinstellungen für die, die durch eine Anforderung [(SOAP) GetDomainSettings-Vorgang](getdomainsettings-operation-soap.md) zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="cdd1d-114">Contains domain settings that are returned by a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="cdd1d-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cdd1d-115">Parent elements</span></span>

|<span data-ttu-id="cdd1d-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="cdd1d-116">**Element**</span></span>|<span data-ttu-id="cdd1d-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cdd1d-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cdd1d-118">DomainResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="cdd1d-118">DomainResponse (SOAP)</span></span>](domainresponse-soap.md) <br/> |<span data-ttu-id="cdd1d-119">Enthält die angeforderten Einstellungen für die angegebene Domäne.</span><span class="sxs-lookup"><span data-stu-id="cdd1d-119">Contains the requested settings for the specified domain.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="cdd1d-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="cdd1d-120">Text value</span></span>

<span data-ttu-id="cdd1d-121">Keine.</span><span class="sxs-lookup"><span data-stu-id="cdd1d-121">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cdd1d-122">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="cdd1d-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cdd1d-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="cdd1d-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="cdd1d-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="cdd1d-124">Schema Name</span></span>  <br/> |<span data-ttu-id="cdd1d-125">AutoErmittlung-schema</span><span class="sxs-lookup"><span data-stu-id="cdd1d-125">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="cdd1d-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="cdd1d-126">Validation File</span></span>  <br/> |<span data-ttu-id="cdd1d-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="cdd1d-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="cdd1d-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="cdd1d-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="cdd1d-129">True</span><span class="sxs-lookup"><span data-stu-id="cdd1d-129">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cdd1d-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cdd1d-130">See also</span></span>

- [<span data-ttu-id="cdd1d-131">GetDomainSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="cdd1d-131">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

