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
ms.openlocfilehash: dea6e36c51ceea53201b668cfba616c03a44df86
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456962"
---
# <a name="domainresponse-soap"></a><span data-ttu-id="10a99-103">DomainResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="10a99-103">DomainResponse (SOAP)</span></span>

<span data-ttu-id="10a99-104">Das **DomainResponse** -Element enthält die angeforderten Einstellungen für die angegebene Domäne.</span><span class="sxs-lookup"><span data-stu-id="10a99-104">The **DomainResponse** element contains the requested settings for the specified domain.</span></span> 
  
```XML
<DomainResponse>
   <DomainSettingErrors/>
   <DomainSettings/>
   <RedirectTarget/>
   <ErrorCode/>
   <ErrorMessage/>
</DomainResponse>
```

 <span data-ttu-id="10a99-105">**DomainResponse**</span><span class="sxs-lookup"><span data-stu-id="10a99-105">**DomainResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="10a99-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="10a99-106">Attributes and elements</span></span>

<span data-ttu-id="10a99-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="10a99-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="10a99-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="10a99-108">Attributes</span></span>

<span data-ttu-id="10a99-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="10a99-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="10a99-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="10a99-110">Child elements</span></span>

|<span data-ttu-id="10a99-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="10a99-111">**Element**</span></span>|<span data-ttu-id="10a99-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="10a99-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="10a99-113">DomainSettingErrors (SOAP)</span><span class="sxs-lookup"><span data-stu-id="10a99-113">DomainSettingErrors (SOAP)</span></span>](domainsettingerrors-soap.md) <br/> |<span data-ttu-id="10a99-114">Enthält Fehlerinformationen für Einstellungen, die nicht zurückgegeben werden konnten.</span><span class="sxs-lookup"><span data-stu-id="10a99-114">Contains error information for settings that could not be returned.</span></span>  <br/> |
|[<span data-ttu-id="10a99-115">DomainSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="10a99-115">DomainSettings (SOAP)</span></span>](domainsettings-soap.md) <br/> |<span data-ttu-id="10a99-116">Stellt die Domäneneinstellungen dar, die in einer Auto Ermittlungsanforderung übermittelt oder von einer Auto Ermittlungs Antwort zurückgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="10a99-116">Represents the domain settings that were submitted in an Autodiscover request or returned by an Autodiscover response.</span></span>  <br/> |
|[<span data-ttu-id="10a99-117">RedirectTarget (SOAP)</span><span class="sxs-lookup"><span data-stu-id="10a99-117">RedirectTarget (SOAP)</span></span>](redirecttarget-soap.md) <br/> |<span data-ttu-id="10a99-118">Gibt das Ziel der Umleitung an.</span><span class="sxs-lookup"><span data-stu-id="10a99-118">Identifies the target of the redirection.</span></span> <span data-ttu-id="10a99-119">Das Ziel kann entweder eine URL oder eine e-Mail-Adresse sein.</span><span class="sxs-lookup"><span data-stu-id="10a99-119">The target can be either a URL or an e-mail address.</span></span>  <br/> |
|[<span data-ttu-id="10a99-120">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="10a99-120">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="10a99-121">Gibt den Fehlercode an, der der spezifischen Anforderung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="10a99-121">Specifies the error code that is associated with the specific request.</span></span>  <br/> |
|[<span data-ttu-id="10a99-122">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="10a99-122">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="10a99-123">Gibt die Fehlermeldung an, die der spezifischen Anforderung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="10a99-123">Specifies the error message that is associated with the specific request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="10a99-124">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="10a99-124">Parent elements</span></span>

|<span data-ttu-id="10a99-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="10a99-125">**Element**</span></span>|<span data-ttu-id="10a99-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="10a99-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="10a99-127">ArrayOfDomainResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="10a99-127">ArrayOfDomainResponse (SOAP)</span></span>](arrayofdomainresponse-soap.md) <br/> |<span data-ttu-id="10a99-128">Enthält ein Array von **DomainResponse** -Elementen.</span><span class="sxs-lookup"><span data-stu-id="10a99-128">Contains an array of **DomainResponse** elements.</span></span> <span data-ttu-id="10a99-129">Jedes **DomainResponse** -Element enthält die angeforderten Einstellungen für den angegebenen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="10a99-129">Each **DomainResponse** element contains the requested settings for the specified user.</span></span>  <br/> |
|[<span data-ttu-id="10a99-130">DomainResponses (SOAP)</span><span class="sxs-lookup"><span data-stu-id="10a99-130">DomainResponses (SOAP)</span></span>](domainresponses-soap.md) <br/> |<span data-ttu-id="10a99-131">Enthält die Antworten für jede Domäne.</span><span class="sxs-lookup"><span data-stu-id="10a99-131">Contains the responses for each domain.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="10a99-132">Textwert</span><span class="sxs-lookup"><span data-stu-id="10a99-132">Text value</span></span>

<span data-ttu-id="10a99-133">Keine.</span><span class="sxs-lookup"><span data-stu-id="10a99-133">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="10a99-134">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="10a99-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="10a99-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="10a99-135">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="10a99-136">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="10a99-136">Schema Name</span></span>  <br/> |<span data-ttu-id="10a99-137">Auto Ermittlungs Schema</span><span class="sxs-lookup"><span data-stu-id="10a99-137">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="10a99-138">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="10a99-138">Validation File</span></span>  <br/> |<span data-ttu-id="10a99-139">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="10a99-139">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="10a99-140">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="10a99-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="10a99-141">True</span><span class="sxs-lookup"><span data-stu-id="10a99-141">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="10a99-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="10a99-142">See also</span></span>

- [<span data-ttu-id="10a99-143">GetDomainSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="10a99-143">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

