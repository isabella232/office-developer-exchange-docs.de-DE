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
description: Das DomainSettings-Element stellt die Domäneneinstellungen dar, die in einer Auto Ermittlungsanforderung übermittelt oder von einer Auto Ermittlungs Antwort zurückgegeben wurden.
ms.openlocfilehash: 67e3753b0cf5c7c653664ff087f697ce7ae2b7a4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530698"
---
# <a name="domainsettings-soap"></a><span data-ttu-id="37e89-103">DomainSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="37e89-103">DomainSettings (SOAP)</span></span>

<span data-ttu-id="37e89-104">Das **DomainSettings** -Element stellt die Domäneneinstellungen dar, die in einer Auto Ermittlungsanforderung übermittelt oder von einer Auto Ermittlungs Antwort zurückgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="37e89-104">The **DomainSettings** element represents the domain settings that were submitted in an Autodiscover request or returned by an Autodiscover response.</span></span> 
  
```XML
<DomainSettings>
   <DomainSetting/>
</DomainSettings>
```

 <span data-ttu-id="37e89-105">**DomainSettings**</span><span class="sxs-lookup"><span data-stu-id="37e89-105">**DomainSettings**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="37e89-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="37e89-106">Attributes and elements</span></span>

<span data-ttu-id="37e89-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="37e89-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="37e89-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="37e89-108">Attributes</span></span>

<span data-ttu-id="37e89-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="37e89-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="37e89-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="37e89-110">Child elements</span></span>

|<span data-ttu-id="37e89-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="37e89-111">**Element**</span></span>|<span data-ttu-id="37e89-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="37e89-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="37e89-113">DomainSetting (SOAP)</span><span class="sxs-lookup"><span data-stu-id="37e89-113">DomainSetting (SOAP)</span></span>](domainsetting-soap.md) <br/> |<span data-ttu-id="37e89-114">Enthält Domäneneinstellungen, die von einer [GetDomainSettings-Vorgang (SOAP)-](getdomainsettings-operation-soap.md) Anforderung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="37e89-114">Contains domain settings that are returned by a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="37e89-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="37e89-115">Parent elements</span></span>

|<span data-ttu-id="37e89-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="37e89-116">**Element**</span></span>|<span data-ttu-id="37e89-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="37e89-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="37e89-118">DomainResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="37e89-118">DomainResponse (SOAP)</span></span>](domainresponse-soap.md) <br/> |<span data-ttu-id="37e89-119">Enthält die angeforderten Einstellungen für die angegebene Domäne.</span><span class="sxs-lookup"><span data-stu-id="37e89-119">Contains the requested settings for the specified domain.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="37e89-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="37e89-120">Text value</span></span>

<span data-ttu-id="37e89-121">Keine.</span><span class="sxs-lookup"><span data-stu-id="37e89-121">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="37e89-122">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="37e89-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="37e89-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="37e89-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="37e89-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="37e89-124">Schema Name</span></span>  <br/> |<span data-ttu-id="37e89-125">Auto Ermittlungs Schema</span><span class="sxs-lookup"><span data-stu-id="37e89-125">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="37e89-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="37e89-126">Validation File</span></span>  <br/> |<span data-ttu-id="37e89-127">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="37e89-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="37e89-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="37e89-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="37e89-129">True</span><span class="sxs-lookup"><span data-stu-id="37e89-129">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="37e89-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="37e89-130">See also</span></span>

- [<span data-ttu-id="37e89-131">GetDomainSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="37e89-131">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

