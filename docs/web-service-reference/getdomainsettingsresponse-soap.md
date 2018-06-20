---
title: GetDomainSettingsResponse (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 43ebd17b-3a70-4878-9254-97a4c2c87b77
description: Das GetDomainSettingsResponse-Element darstellt, die Antwort auf eine Operation GetDomainSettings (SOAP), die die domäneneinstellungen zurückgibt.
ms.openlocfilehash: c4984c2c6c532fcbd45c1a75733e578f6d9491fa
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758642"
---
# <a name="getdomainsettingsresponse-soap"></a><span data-ttu-id="9579b-103">GetDomainSettingsResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="9579b-103">GetDomainSettingsResponse (SOAP)</span></span>

<span data-ttu-id="9579b-104">Das **GetDomainSettingsResponse** -Element darstellt, die Antwort auf eine [GetDomainSettings-Vorgang (SOAP)](getdomainsettings-operation-soap.md), die die domäneneinstellungen zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="9579b-104">The **GetDomainSettingsResponse** element represents the response to a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md), which returns the domain settings.</span></span>
  
```XML
<GetDomainSettingsResponse>
   <DomainResponses/>
   <ErrorCode/>
   <ErrorMessage/>
</GetDomainSettingsResponse>
```

 <span data-ttu-id="9579b-105">**GetDomainSettingsResponse**</span><span class="sxs-lookup"><span data-stu-id="9579b-105">**GetDomainSettingsResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9579b-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="9579b-106">Attributes and elements</span></span>

<span data-ttu-id="9579b-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="9579b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9579b-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="9579b-108">Attributes</span></span>

<span data-ttu-id="9579b-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="9579b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9579b-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9579b-110">Child elements</span></span>

|<span data-ttu-id="9579b-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="9579b-111">**Element**</span></span>|<span data-ttu-id="9579b-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9579b-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9579b-113">DomainResponses (SOAP)</span><span class="sxs-lookup"><span data-stu-id="9579b-113">DomainResponses (SOAP)</span></span>](domainresponses-soap.md) <br/> |<span data-ttu-id="9579b-114">Enthält ein Array von Antworten für jede angeforderte Domäne Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="9579b-114">Contains an array of responses for each requested domain's settings.</span></span>  <br/> |
|[<span data-ttu-id="9579b-115">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="9579b-115">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="9579b-116">Stellt einen Fehlercode, der von den AutoErmittlungsdienst zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9579b-116">Represents an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="9579b-117">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="9579b-117">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="9579b-118">Stellt eine Nachricht, die ein Fehlercode zugeordnet ist, die von den AutoErmittlungsdienst zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9579b-118">Represents a message that is associated with an error code that is returned by the Autodiscover service.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9579b-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9579b-119">Parent elements</span></span>

<span data-ttu-id="9579b-120">Keine.</span><span class="sxs-lookup"><span data-stu-id="9579b-120">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="9579b-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="9579b-121">Text value</span></span>

<span data-ttu-id="9579b-122">Keine.</span><span class="sxs-lookup"><span data-stu-id="9579b-122">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9579b-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="9579b-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9579b-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="9579b-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="9579b-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="9579b-125">Schema Name</span></span>  <br/> |<span data-ttu-id="9579b-126">AutoErmittlung-schema</span><span class="sxs-lookup"><span data-stu-id="9579b-126">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="9579b-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="9579b-127">Validation File</span></span>  <br/> |<span data-ttu-id="9579b-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="9579b-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9579b-129">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="9579b-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="9579b-130">True</span><span class="sxs-lookup"><span data-stu-id="9579b-130">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9579b-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9579b-131">See also</span></span>



[<span data-ttu-id="9579b-132">GetDomainSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="9579b-132">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

