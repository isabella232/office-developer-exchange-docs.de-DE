---
title: DomainSettingErrors (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: a4ce19de-f560-4984-8047-ecbbc86c9b91
description: Das DomainSettingsErrors-Element enthält Fehlerinformationen für Einstellungen, die nicht zurückgegeben werden konnten.
ms.openlocfilehash: 4e7ee29c2bc680a1938b75189c2ac3c214f7d2b5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530705"
---
# <a name="domainsettingerrors-soap"></a><span data-ttu-id="d3656-103">DomainSettingErrors (SOAP)</span><span class="sxs-lookup"><span data-stu-id="d3656-103">DomainSettingErrors (SOAP)</span></span>

<span data-ttu-id="d3656-104">Das **DomainSettingsErrors** -Element enthält Fehlerinformationen für Einstellungen, die nicht zurückgegeben werden konnten.</span><span class="sxs-lookup"><span data-stu-id="d3656-104">The **DomainSettingsErrors** element contains error information for settings that could not be returned.</span></span> 
  
```XML
<DomainSettingsErrors>
   <DomainSettingsError/>
</DomainSettingsErrors>
```

 <span data-ttu-id="d3656-105">**DomainSettingsErrors**</span><span class="sxs-lookup"><span data-stu-id="d3656-105">**DomainSettingsErrors**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d3656-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d3656-106">Attributes and elements</span></span>

<span data-ttu-id="d3656-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d3656-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d3656-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d3656-108">Attributes</span></span>

<span data-ttu-id="d3656-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="d3656-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d3656-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d3656-110">Child elements</span></span>

|<span data-ttu-id="d3656-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="d3656-111">**Element**</span></span>|<span data-ttu-id="d3656-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d3656-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d3656-113">DomainSettingError (SOAP)</span><span class="sxs-lookup"><span data-stu-id="d3656-113">DomainSettingError (SOAP)</span></span>](domainsettingerror-soap.md) <br/> |<span data-ttu-id="d3656-114">Stellt einen Fehler dar, der beim Abrufen einer Domäneneinstellung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="d3656-114">Represents an error that occurred while retrieving a domain setting.</span></span> <span data-ttu-id="d3656-115">Dies stellt einen Fehler aus einer [GetDomainSettings Operation (SOAP)-](getdomainsettings-operation-soap.md) Vorgangsanforderung dar.</span><span class="sxs-lookup"><span data-stu-id="d3656-115">This represents an error from a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) operation request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d3656-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d3656-116">Parent elements</span></span>

|<span data-ttu-id="d3656-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="d3656-117">**Element**</span></span>|<span data-ttu-id="d3656-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d3656-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d3656-119">DomainResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="d3656-119">DomainResponse (SOAP)</span></span>](domainresponse-soap.md) <br/> |<span data-ttu-id="d3656-120">Enthält die angeforderten Einstellungen für die angegebene Domäne.</span><span class="sxs-lookup"><span data-stu-id="d3656-120">Contains the requested settings for the specified domain.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d3656-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="d3656-121">Text value</span></span>

<span data-ttu-id="d3656-122">Keine.</span><span class="sxs-lookup"><span data-stu-id="d3656-122">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d3656-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="d3656-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d3656-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="d3656-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="d3656-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d3656-125">Schema Name</span></span>  <br/> |<span data-ttu-id="d3656-126">Auto Ermittlungs Schema</span><span class="sxs-lookup"><span data-stu-id="d3656-126">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="d3656-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d3656-127">Validation File</span></span>  <br/> |<span data-ttu-id="d3656-128">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="d3656-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d3656-129">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d3656-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="d3656-130">True</span><span class="sxs-lookup"><span data-stu-id="d3656-130">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d3656-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d3656-131">See also</span></span>

- [<span data-ttu-id="d3656-132">GetDomainSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="d3656-132">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

