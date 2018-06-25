---
title: ArrayOfDomainResponse (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 6dbd9221-e019-4981-bcdb-ea370331f407
description: Das ArrayOfDomainResponse-Element enthält ein Array von Antworten für jede angeforderte Domäne Einstellungen.
ms.openlocfilehash: 7dec7f4e3df2fd0d7d1fcd4f08bc74a2b432af1b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757381"
---
# <a name="arrayofdomainresponse-soap"></a><span data-ttu-id="e567d-103">ArrayOfDomainResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e567d-103">ArrayOfDomainResponse (SOAP)</span></span>

<span data-ttu-id="e567d-104">Das **ArrayOfDomainResponse** -Element enthält ein Array von Antworten für jede angeforderte Domäne Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="e567d-104">The **ArrayOfDomainResponse** element contains an array of responses for each requested domain's settings.</span></span> 
  
```XML
<ArrayOfDomainResponse>
   <DomainResponse/>
</ArrayOfDomainResponse>
```

 <span data-ttu-id="e567d-105">**ArrayOfDomainResponse**</span><span class="sxs-lookup"><span data-stu-id="e567d-105">**ArrayOfDomainResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e567d-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e567d-106">Attributes and elements</span></span>

<span data-ttu-id="e567d-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e567d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e567d-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="e567d-108">Attributes</span></span>

<span data-ttu-id="e567d-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="e567d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e567d-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e567d-110">Child elements</span></span>

|<span data-ttu-id="e567d-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="e567d-111">**Element**</span></span>|<span data-ttu-id="e567d-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e567d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e567d-113">DomainResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e567d-113">DomainResponse (SOAP)</span></span>](domainresponse-soap.md) <br/> |<span data-ttu-id="e567d-114">Enthält die angeforderten Einstellungen für die angegebene Domäne.</span><span class="sxs-lookup"><span data-stu-id="e567d-114">Contains the requested settings for the specified domain.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e567d-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e567d-115">Parent elements</span></span>

<span data-ttu-id="e567d-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="e567d-116">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="e567d-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="e567d-117">Text value</span></span>

<span data-ttu-id="e567d-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="e567d-118">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e567d-119">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="e567d-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e567d-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="e567d-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="e567d-121">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e567d-121">Schema Name</span></span>  <br/> |<span data-ttu-id="e567d-122">AutoErmittlung-schema</span><span class="sxs-lookup"><span data-stu-id="e567d-122">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="e567d-123">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e567d-123">Validation File</span></span>  <br/> |<span data-ttu-id="e567d-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="e567d-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e567d-125">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="e567d-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="e567d-126">True</span><span class="sxs-lookup"><span data-stu-id="e567d-126">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e567d-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e567d-127">See also</span></span>

- [<span data-ttu-id="e567d-128">GetDomainSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="e567d-128">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

