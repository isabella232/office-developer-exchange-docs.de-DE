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
description: Das GetDomainSettingsResponse-Element stellt die Antwort auf einen GetDomainSettings-Vorgang (SOAP) dar, der die Domäneneinstellungen zurückgibt.
ms.openlocfilehash: 94cb202948e6a0d5a34f5547132c052d1d1b6a40
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461877"
---
# <a name="getdomainsettingsresponse-soap"></a><span data-ttu-id="69de2-103">GetDomainSettingsResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="69de2-103">GetDomainSettingsResponse (SOAP)</span></span>

<span data-ttu-id="69de2-104">Das **GetDomainSettingsResponse** -Element stellt die Antwort auf einen [GetDomainSettings-Vorgang (SOAP)](getdomainsettings-operation-soap.md)dar, der die Domäneneinstellungen zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="69de2-104">The **GetDomainSettingsResponse** element represents the response to a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md), which returns the domain settings.</span></span>
  
```XML
<GetDomainSettingsResponse>
   <DomainResponses/>
   <ErrorCode/>
   <ErrorMessage/>
</GetDomainSettingsResponse>
```

 <span data-ttu-id="69de2-105">**GetDomainSettingsResponse**</span><span class="sxs-lookup"><span data-stu-id="69de2-105">**GetDomainSettingsResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="69de2-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="69de2-106">Attributes and elements</span></span>

<span data-ttu-id="69de2-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="69de2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="69de2-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="69de2-108">Attributes</span></span>

<span data-ttu-id="69de2-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="69de2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="69de2-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="69de2-110">Child elements</span></span>

|<span data-ttu-id="69de2-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="69de2-111">**Element**</span></span>|<span data-ttu-id="69de2-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="69de2-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="69de2-113">DomainResponses (SOAP)</span><span class="sxs-lookup"><span data-stu-id="69de2-113">DomainResponses (SOAP)</span></span>](domainresponses-soap.md) <br/> |<span data-ttu-id="69de2-114">Enthält ein Array von Antworten für die Einstellungen jeder angeforderten Domäne.</span><span class="sxs-lookup"><span data-stu-id="69de2-114">Contains an array of responses for each requested domain's settings.</span></span>  <br/> |
|[<span data-ttu-id="69de2-115">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="69de2-115">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="69de2-116">Stellt einen Fehlercode dar, der vom AutoErmittlungsdienst zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="69de2-116">Represents an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="69de2-117">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="69de2-117">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="69de2-118">Stellt eine Meldung dar, die einem Fehlercode zugeordnet ist, der vom AutoErmittlungsdienst zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="69de2-118">Represents a message that is associated with an error code that is returned by the Autodiscover service.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="69de2-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="69de2-119">Parent elements</span></span>

<span data-ttu-id="69de2-120">Keine.</span><span class="sxs-lookup"><span data-stu-id="69de2-120">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="69de2-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="69de2-121">Text value</span></span>

<span data-ttu-id="69de2-122">Keine.</span><span class="sxs-lookup"><span data-stu-id="69de2-122">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="69de2-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="69de2-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="69de2-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="69de2-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="69de2-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="69de2-125">Schema Name</span></span>  <br/> |<span data-ttu-id="69de2-126">Auto Ermittlungs Schema</span><span class="sxs-lookup"><span data-stu-id="69de2-126">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="69de2-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="69de2-127">Validation File</span></span>  <br/> |<span data-ttu-id="69de2-128">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="69de2-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="69de2-129">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="69de2-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="69de2-130">True</span><span class="sxs-lookup"><span data-stu-id="69de2-130">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="69de2-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="69de2-131">See also</span></span>



[<span data-ttu-id="69de2-132">GetDomainSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="69de2-132">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

