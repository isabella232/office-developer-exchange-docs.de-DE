---
title: DomainResponse (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 6aa319be-3a01-4044-8dfc-8fa1318524c3
description: Das DomainResponse-Element enthält die angeforderten Einstellungen für die angegebene Domäne.
ms.openlocfilehash: c40f33a278b5032913329a7cd64346b572f5df2f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758091"
---
# <a name="domainresponse-soap"></a><span data-ttu-id="7fd76-103">DomainResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7fd76-103">DomainResponse (SOAP)</span></span>

<span data-ttu-id="7fd76-104">Das **DomainResponse** -Element enthält die angeforderten Einstellungen für die angegebene Domäne.</span><span class="sxs-lookup"><span data-stu-id="7fd76-104">The **DomainResponse** element contains the requested settings for the specified domain.</span></span> 
  
```XML
<DomainResponse>
   <DomainSettingErrors/>
   <DomainSettings/>
   <RedirectTarget/>
   <ErrorCode/>
   <ErrorMessage/>
</DomainResponse>
```

 <span data-ttu-id="7fd76-105">**DomainResponse**</span><span class="sxs-lookup"><span data-stu-id="7fd76-105">**DomainResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7fd76-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="7fd76-106">Attributes and elements</span></span>

<span data-ttu-id="7fd76-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="7fd76-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7fd76-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="7fd76-108">Attributes</span></span>

<span data-ttu-id="7fd76-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="7fd76-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7fd76-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7fd76-110">Child elements</span></span>

|<span data-ttu-id="7fd76-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="7fd76-111">**Element**</span></span>|<span data-ttu-id="7fd76-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7fd76-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7fd76-113">DomainSettingErrors (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7fd76-113">DomainSettingErrors (SOAP)</span></span>](domainsettingerrors-soap.md) <br/> |<span data-ttu-id="7fd76-114">Enthält Informationen für die Einstellungen, die nicht zurückgegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="7fd76-114">Contains error information for settings that could not be returned.</span></span>  <br/> |
|[<span data-ttu-id="7fd76-115">DomainSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7fd76-115">DomainSettings (SOAP)</span></span>](domainsettings-soap.md) <br/> |<span data-ttu-id="7fd76-116">Stellt die domäneneinstellungen, die in einer autoermittlungsanforderung für die gesendet oder von einer Antwort der AutoErmittlung zurückgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="7fd76-116">Represents the domain settings that were submitted in an Autodiscover request or returned by an Autodiscover response.</span></span>  <br/> |
|[<span data-ttu-id="7fd76-117">RedirectTarget (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7fd76-117">RedirectTarget (SOAP)</span></span>](redirecttarget-soap.md) <br/> |<span data-ttu-id="7fd76-118">Identifiziert die als Ziel für die Umleitung an.</span><span class="sxs-lookup"><span data-stu-id="7fd76-118">Identifies the target of the redirection.</span></span> <span data-ttu-id="7fd76-119">Das Ziel kann eine URL oder eine e-Mail-Adresse sein.</span><span class="sxs-lookup"><span data-stu-id="7fd76-119">The target can be either a URL or an e-mail address.</span></span>  <br/> |
|[<span data-ttu-id="7fd76-120">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7fd76-120">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="7fd76-121">Gibt den Fehlercode, der bestimmte Anforderung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="7fd76-121">Specifies the error code that is associated with the specific request.</span></span>  <br/> |
|[<span data-ttu-id="7fd76-122">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7fd76-122">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="7fd76-123">Gibt die Fehlermeldung, die die spezifische Anforderung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="7fd76-123">Specifies the error message that is associated with the specific request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7fd76-124">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7fd76-124">Parent elements</span></span>

|<span data-ttu-id="7fd76-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="7fd76-125">**Element**</span></span>|<span data-ttu-id="7fd76-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7fd76-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7fd76-127">ArrayOfDomainResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7fd76-127">ArrayOfDomainResponse (SOAP)</span></span>](arrayofdomainresponse-soap.md) <br/> |<span data-ttu-id="7fd76-128">Enthält ein Array von **DomainResponse** -Elementen.</span><span class="sxs-lookup"><span data-stu-id="7fd76-128">Contains an array of **DomainResponse** elements.</span></span> <span data-ttu-id="7fd76-129">Jedes Element **DomainResponse** enthält die angeforderten Einstellungen für den angegebenen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="7fd76-129">Each **DomainResponse** element contains the requested settings for the specified user.</span></span>  <br/> |
|[<span data-ttu-id="7fd76-130">DomainResponses (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7fd76-130">DomainResponses (SOAP)</span></span>](domainresponses-soap.md) <br/> |<span data-ttu-id="7fd76-131">Enthält die Antworten für jede Domäne.</span><span class="sxs-lookup"><span data-stu-id="7fd76-131">Contains the responses for each domain.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7fd76-132">Textwert</span><span class="sxs-lookup"><span data-stu-id="7fd76-132">Text value</span></span>

<span data-ttu-id="7fd76-133">Keine.</span><span class="sxs-lookup"><span data-stu-id="7fd76-133">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7fd76-134">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="7fd76-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7fd76-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="7fd76-135">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="7fd76-136">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="7fd76-136">Schema Name</span></span>  <br/> |<span data-ttu-id="7fd76-137">AutoErmittlung-schema</span><span class="sxs-lookup"><span data-stu-id="7fd76-137">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="7fd76-138">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="7fd76-138">Validation File</span></span>  <br/> |<span data-ttu-id="7fd76-139">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="7fd76-139">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7fd76-140">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="7fd76-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="7fd76-141">True</span><span class="sxs-lookup"><span data-stu-id="7fd76-141">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7fd76-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7fd76-142">See also</span></span>

- [<span data-ttu-id="7fd76-143">GetDomainSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7fd76-143">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

