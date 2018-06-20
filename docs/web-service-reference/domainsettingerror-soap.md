---
title: DomainSettingError (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 48c3f7b5-2ee0-42ce-97a1-a881e2f60327
description: Das DomainSettingError-Element stellt einen Fehler, die beim Abrufen einer domäneneinstellung dar. Dies stellt einen Fehler aus einer Anforderung GetDomainSettings dar.
ms.openlocfilehash: 08b0a47acea8d35ec78efd701168a251771effac
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758100"
---
# <a name="domainsettingerror-soap"></a><span data-ttu-id="33b2d-104">DomainSettingError (SOAP)</span><span class="sxs-lookup"><span data-stu-id="33b2d-104">DomainSettingError (SOAP)</span></span>

<span data-ttu-id="33b2d-105">Das **DomainSettingError** -Element stellt einen Fehler, die beim Abrufen einer domäneneinstellung dar.</span><span class="sxs-lookup"><span data-stu-id="33b2d-105">The **DomainSettingError** element represents an error that occurred while retrieving a domain setting.</span></span> <span data-ttu-id="33b2d-106">Dies stellt einen Fehler aus einer Anforderung **GetDomainSettings** dar.</span><span class="sxs-lookup"><span data-stu-id="33b2d-106">This represents an error from a **GetDomainSettings** request.</span></span> 
  
```XML
<DomainSettingError>
   <ErrorCode/>
   <ErrorMessage/>
   <SettingName/>
</DomainSettingError>
```

 <span data-ttu-id="33b2d-107">**DomainSettingError**</span><span class="sxs-lookup"><span data-stu-id="33b2d-107">**DomainSettingError**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="33b2d-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="33b2d-108">Attributes and elements</span></span>

<span data-ttu-id="33b2d-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="33b2d-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="33b2d-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="33b2d-110">Attributes</span></span>

<span data-ttu-id="33b2d-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="33b2d-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="33b2d-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="33b2d-112">Child elements</span></span>

|<span data-ttu-id="33b2d-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="33b2d-113">**Element**</span></span>|<span data-ttu-id="33b2d-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="33b2d-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="33b2d-115">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="33b2d-115">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="33b2d-116">Identifiziert den Fehlercode, der bestimmte Anforderung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="33b2d-116">Identifies the error code that is associated with the specific request.</span></span>  <br/> |
|[<span data-ttu-id="33b2d-117">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="33b2d-117">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="33b2d-118">Enthält die Fehlermeldung, die die spezifische Anforderung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="33b2d-118">Contains the error message that is associated with the specific request.</span></span>  <br/> |
|[<span data-ttu-id="33b2d-119">SettingName (SOAP)</span><span class="sxs-lookup"><span data-stu-id="33b2d-119">SettingName (SOAP)</span></span>](settingname-soap.md) <br/> |<span data-ttu-id="33b2d-120">Der Name der Einstellung darstellt.</span><span class="sxs-lookup"><span data-stu-id="33b2d-120">Represents the name of the setting.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="33b2d-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="33b2d-121">Parent elements</span></span>

|<span data-ttu-id="33b2d-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="33b2d-122">**Element**</span></span>|<span data-ttu-id="33b2d-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="33b2d-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="33b2d-124">DomainSettingErrors (SOAP)</span><span class="sxs-lookup"><span data-stu-id="33b2d-124">DomainSettingErrors (SOAP)</span></span>](domainsettingerrors-soap.md) <br/> |<span data-ttu-id="33b2d-125">Enthält Informationen für die Einstellungen, die nicht zurückgegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="33b2d-125">Contains error information for settings that could not be returned.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="33b2d-126">Textwert</span><span class="sxs-lookup"><span data-stu-id="33b2d-126">Text value</span></span>

<span data-ttu-id="33b2d-127">Keine.</span><span class="sxs-lookup"><span data-stu-id="33b2d-127">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="33b2d-128">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="33b2d-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="33b2d-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="33b2d-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="33b2d-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="33b2d-130">Schema Name</span></span>  <br/> |<span data-ttu-id="33b2d-131">AutoErmittlung-schema</span><span class="sxs-lookup"><span data-stu-id="33b2d-131">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="33b2d-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="33b2d-132">Validation File</span></span>  <br/> |<span data-ttu-id="33b2d-133">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="33b2d-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="33b2d-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="33b2d-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="33b2d-135">True</span><span class="sxs-lookup"><span data-stu-id="33b2d-135">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="33b2d-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="33b2d-136">See also</span></span>

- [<span data-ttu-id="33b2d-137">GetDomainSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="33b2d-137">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

