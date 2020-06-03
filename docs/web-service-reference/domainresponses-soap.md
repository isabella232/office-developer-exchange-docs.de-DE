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
description: Das DomainResponses-Element enthält ein Array von Antworten für die Einstellungen jeder angeforderten Domäne.
ms.openlocfilehash: 2c76b9691fe88657a65130ef6829e5af64380d95
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526319"
---
# <a name="domainresponses-soap"></a><span data-ttu-id="70769-103">DomainResponses (SOAP)</span><span class="sxs-lookup"><span data-stu-id="70769-103">DomainResponses (SOAP)</span></span>

<span data-ttu-id="70769-104">Das **DomainResponses** -Element enthält ein Array von Antworten für die Einstellungen jeder angeforderten Domäne.</span><span class="sxs-lookup"><span data-stu-id="70769-104">The **DomainResponses** element contains an array of responses for each requested domain's settings.</span></span> 
  
```XML
<DomainResponses>
   <DomainResponse/>
</DomainResponses>
```

 <span data-ttu-id="70769-105">**ArrayOfDomainResponse**</span><span class="sxs-lookup"><span data-stu-id="70769-105">**ArrayOfDomainResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="70769-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="70769-106">Attributes and elements</span></span>

<span data-ttu-id="70769-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="70769-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="70769-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="70769-108">Attributes</span></span>

<span data-ttu-id="70769-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="70769-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="70769-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="70769-110">Child elements</span></span>

|<span data-ttu-id="70769-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="70769-111">**Element**</span></span>|<span data-ttu-id="70769-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="70769-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="70769-113">DomainResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="70769-113">DomainResponse (SOAP)</span></span>](domainresponse-soap.md) <br/> |<span data-ttu-id="70769-114">Enthält die angeforderten Einstellungen für die angegebene Domäne.</span><span class="sxs-lookup"><span data-stu-id="70769-114">Contains the requested settings for the specified domain.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="70769-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="70769-115">Parent elements</span></span>

|<span data-ttu-id="70769-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="70769-116">**Element**</span></span>|<span data-ttu-id="70769-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="70769-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="70769-118">GetDomainSettingsResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="70769-118">GetDomainSettingsResponse (SOAP)</span></span>](getdomainsettingsresponse-soap.md) <br/> |<span data-ttu-id="70769-119">Stellt die Antwort auf eine [GetDomainSettings-Vorgang (SOAP)](getdomainsettings-operation-soap.md) -Anforderung für eine Domäne dar und gibt die Domäneneinstellungen zurück.</span><span class="sxs-lookup"><span data-stu-id="70769-119">Represents the response to a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) request for a domain, and returns the domain settings.</span></span>  <br/> |
|[<span data-ttu-id="70769-120">Antwort (GetDomainSettings) (SOAP)</span><span class="sxs-lookup"><span data-stu-id="70769-120">Response (GetDomainSettings) (SOAP)</span></span>](response-getdomainsettingssoap.md) <br/> |<span data-ttu-id="70769-121">Stellt die Antwort auf einen [GetDomainSettings-Vorgang (SOAP)-](getdomainsettings-operation-soap.md) Aufruf für eine einzelne Domäne dar.</span><span class="sxs-lookup"><span data-stu-id="70769-121">Represents the response to a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) call for an individual domain.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="70769-122">Textwert</span><span class="sxs-lookup"><span data-stu-id="70769-122">Text value</span></span>

<span data-ttu-id="70769-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="70769-123">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="70769-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="70769-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="70769-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="70769-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="70769-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="70769-126">Schema Name</span></span>  <br/> |<span data-ttu-id="70769-127">Auto Ermittlungs Schema</span><span class="sxs-lookup"><span data-stu-id="70769-127">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="70769-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="70769-128">Validation File</span></span>  <br/> |<span data-ttu-id="70769-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="70769-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="70769-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="70769-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="70769-131">True</span><span class="sxs-lookup"><span data-stu-id="70769-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="70769-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="70769-132">See also</span></span>

- [<span data-ttu-id="70769-133">GetDomainSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="70769-133">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

