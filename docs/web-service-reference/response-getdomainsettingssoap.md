---
title: Antwort (GetDomainSettings) (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: a5b052df-93bd-4fe1-ac30-83de9a3dfcd7
description: Das Response-Element stellt die Antwort auf einen GetDomainSettings-Aufruf für eine einzelne Domäne dar.
ms.openlocfilehash: 67fe7aea4533058fa0df972e49a2069749dc258b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455583"
---
# <a name="response-getdomainsettings-soap"></a><span data-ttu-id="ed905-103">Antwort (GetDomainSettings) (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ed905-103">Response (GetDomainSettings) (SOAP)</span></span>

<span data-ttu-id="ed905-104">Das **Response** -Element stellt die Antwort auf einen **GetDomainSettings** -Aufruf für eine einzelne Domäne dar.</span><span class="sxs-lookup"><span data-stu-id="ed905-104">The **Response** element represents the response to a **GetDomainSettings** call for an individual domain.</span></span> 
  
```XML
<Response>
   <DomainResponses/>
   <ErrorCode/>
   <ErrorMessage/>
</Response>
```

 <span data-ttu-id="ed905-105">**GetDomainSettingsResponse**</span><span class="sxs-lookup"><span data-stu-id="ed905-105">**GetDomainSettingsResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ed905-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ed905-106">Attributes and elements</span></span>

<span data-ttu-id="ed905-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ed905-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ed905-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="ed905-108">Attributes</span></span>

<span data-ttu-id="ed905-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="ed905-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ed905-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ed905-110">Child elements</span></span>

|<span data-ttu-id="ed905-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="ed905-111">**Element**</span></span>|<span data-ttu-id="ed905-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ed905-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ed905-113">DomainResponses (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ed905-113">DomainResponses (SOAP)</span></span>](domainresponses-soap.md) <br/> |<span data-ttu-id="ed905-114">Enthält die Antwort für jede in einer **GetDomainSettings** -Anforderung angeforderte Domäne.</span><span class="sxs-lookup"><span data-stu-id="ed905-114">Contains the response for each domain requested in a **GetDomainSettings** request.</span></span>  <br/> |
|[<span data-ttu-id="ed905-115">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ed905-115">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="ed905-116">Enthält den Fehlercode, der der Antwort zugeordnet ist (falls zutreffend).</span><span class="sxs-lookup"><span data-stu-id="ed905-116">Contains the error code that is associated with the response, if applicable.</span></span>  <br/> |
|[<span data-ttu-id="ed905-117">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ed905-117">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="ed905-118">Enthält die Fehlermeldung, die der Antwort zugeordnet ist (falls zutreffend).</span><span class="sxs-lookup"><span data-stu-id="ed905-118">Contains the error message that is associated with the response, if applicable.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ed905-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ed905-119">Parent elements</span></span>

|<span data-ttu-id="ed905-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="ed905-120">**Element**</span></span>|<span data-ttu-id="ed905-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ed905-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ed905-122">GetDomainSettingsResponseMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ed905-122">GetDomainSettingsResponseMessage (SOAP)</span></span>](getdomainsettingsresponsemessage-soap.md) <br/> |<span data-ttu-id="ed905-123">Gibt die Domänen Konfigurationseinstellungen an den Aufrufer zurück.</span><span class="sxs-lookup"><span data-stu-id="ed905-123">Returns to the caller the domain configuration settings.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ed905-124">Textwert</span><span class="sxs-lookup"><span data-stu-id="ed905-124">Text value</span></span>

<span data-ttu-id="ed905-125">Keine.</span><span class="sxs-lookup"><span data-stu-id="ed905-125">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ed905-126">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="ed905-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ed905-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="ed905-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="ed905-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ed905-128">Schema Name</span></span>  <br/> |<span data-ttu-id="ed905-129">Auto Ermittlungs Schema</span><span class="sxs-lookup"><span data-stu-id="ed905-129">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="ed905-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ed905-130">Validation File</span></span>  <br/> |<span data-ttu-id="ed905-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="ed905-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ed905-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="ed905-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="ed905-133">True</span><span class="sxs-lookup"><span data-stu-id="ed905-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ed905-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed905-134">See also</span></span>



[<span data-ttu-id="ed905-135">GetDomainSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ed905-135">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

