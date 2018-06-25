---
title: DomainResponses (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: d9c7fd91-22cd-4c72-a841-25cb9d415e0c
description: Das DomainResponses-Element enthält ein Array von Antworten für jede angeforderte Domäne Einstellungen.
ms.openlocfilehash: 77a3efc1605337ab436f6aea2b61a67f22e4f8ce
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758097"
---
# <a name="domainresponses-soap"></a><span data-ttu-id="13037-103">DomainResponses (SOAP)</span><span class="sxs-lookup"><span data-stu-id="13037-103">DomainResponses (SOAP)</span></span>

<span data-ttu-id="13037-104">Das **DomainResponses** -Element enthält ein Array von Antworten für jede angeforderte Domäne Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="13037-104">The **DomainResponses** element contains an array of responses for each requested domain's settings.</span></span> 
  
```XML
<DomainResponses>
   <DomainResponse/>
</DomainResponses>
```

 <span data-ttu-id="13037-105">**ArrayOfDomainResponse**</span><span class="sxs-lookup"><span data-stu-id="13037-105">**ArrayOfDomainResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="13037-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="13037-106">Attributes and elements</span></span>

<span data-ttu-id="13037-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="13037-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="13037-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="13037-108">Attributes</span></span>

<span data-ttu-id="13037-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="13037-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="13037-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="13037-110">Child elements</span></span>

|<span data-ttu-id="13037-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="13037-111">**Element**</span></span>|<span data-ttu-id="13037-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="13037-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="13037-113">DomainResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="13037-113">DomainResponse (SOAP)</span></span>](domainresponse-soap.md) <br/> |<span data-ttu-id="13037-114">Enthält die angeforderten Einstellungen für die angegebene Domäne.</span><span class="sxs-lookup"><span data-stu-id="13037-114">Contains the requested settings for the specified domain.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="13037-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="13037-115">Parent elements</span></span>

|<span data-ttu-id="13037-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="13037-116">**Element**</span></span>|<span data-ttu-id="13037-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="13037-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="13037-118">GetDomainSettingsResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="13037-118">GetDomainSettingsResponse (SOAP)</span></span>](getdomainsettingsresponse-soap.md) <br/> |<span data-ttu-id="13037-119">Stellt die Antwort auf eine Anforderung [(SOAP) GetDomainSettings-Vorgang](getdomainsettings-operation-soap.md) für eine Domäne, und die domäneneinstellungen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="13037-119">Represents the response to a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) request for a domain, and returns the domain settings.</span></span>  <br/> |
|[<span data-ttu-id="13037-120">Antwort (GetDomainSettings) (SOAP)</span><span class="sxs-lookup"><span data-stu-id="13037-120">Response (GetDomainSettings) (SOAP)</span></span>](response-getdomainsettingssoap.md) <br/> |<span data-ttu-id="13037-121">Die Antwort zu einem Anruf [GetDomainSettings-Vorgang (SOAP)](getdomainsettings-operation-soap.md) für eine einzelne Domäne darstellt.</span><span class="sxs-lookup"><span data-stu-id="13037-121">Represents the response to a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) call for an individual domain.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="13037-122">Textwert</span><span class="sxs-lookup"><span data-stu-id="13037-122">Text value</span></span>

<span data-ttu-id="13037-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="13037-123">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="13037-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="13037-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="13037-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="13037-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="13037-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="13037-126">Schema Name</span></span>  <br/> |<span data-ttu-id="13037-127">AutoErmittlung-schema</span><span class="sxs-lookup"><span data-stu-id="13037-127">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="13037-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="13037-128">Validation File</span></span>  <br/> |<span data-ttu-id="13037-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="13037-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="13037-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="13037-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="13037-131">True</span><span class="sxs-lookup"><span data-stu-id="13037-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="13037-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="13037-132">See also</span></span>

- [<span data-ttu-id="13037-133">GetDomainSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="13037-133">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

