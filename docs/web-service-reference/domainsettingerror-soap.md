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
description: Das DomainSettingError-Element stellt einen Fehler dar, der beim Abrufen einer Domäneneinstellung aufgetreten ist. Dies stellt einen Fehler aus einer GetDomainSettings-Anforderung dar.
ms.openlocfilehash: 189a614e7629033c8db2f60b8fd3679835a696ed
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530712"
---
# <a name="domainsettingerror-soap"></a><span data-ttu-id="4f9a7-104">DomainSettingError (SOAP)</span><span class="sxs-lookup"><span data-stu-id="4f9a7-104">DomainSettingError (SOAP)</span></span>

<span data-ttu-id="4f9a7-105">Das **DomainSettingError** -Element stellt einen Fehler dar, der beim Abrufen einer Domäneneinstellung aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="4f9a7-105">The **DomainSettingError** element represents an error that occurred while retrieving a domain setting.</span></span> <span data-ttu-id="4f9a7-106">Dies stellt einen Fehler aus einer **GetDomainSettings** -Anforderung dar.</span><span class="sxs-lookup"><span data-stu-id="4f9a7-106">This represents an error from a **GetDomainSettings** request.</span></span> 
  
```XML
<DomainSettingError>
   <ErrorCode/>
   <ErrorMessage/>
   <SettingName/>
</DomainSettingError>
```

 <span data-ttu-id="4f9a7-107">**DomainSettingError**</span><span class="sxs-lookup"><span data-stu-id="4f9a7-107">**DomainSettingError**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4f9a7-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="4f9a7-108">Attributes and elements</span></span>

<span data-ttu-id="4f9a7-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="4f9a7-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4f9a7-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="4f9a7-110">Attributes</span></span>

<span data-ttu-id="4f9a7-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="4f9a7-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4f9a7-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4f9a7-112">Child elements</span></span>

|<span data-ttu-id="4f9a7-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="4f9a7-113">**Element**</span></span>|<span data-ttu-id="4f9a7-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4f9a7-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4f9a7-115">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="4f9a7-115">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="4f9a7-116">Gibt den Fehlercode an, der der spezifischen Anforderung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="4f9a7-116">Identifies the error code that is associated with the specific request.</span></span>  <br/> |
|[<span data-ttu-id="4f9a7-117">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="4f9a7-117">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="4f9a7-118">Enthält die Fehlermeldung, die der spezifischen Anforderung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="4f9a7-118">Contains the error message that is associated with the specific request.</span></span>  <br/> |
|[<span data-ttu-id="4f9a7-119">SettingName (SOAP)</span><span class="sxs-lookup"><span data-stu-id="4f9a7-119">SettingName (SOAP)</span></span>](settingname-soap.md) <br/> |<span data-ttu-id="4f9a7-120">Stellt den Namen der Einstellung dar.</span><span class="sxs-lookup"><span data-stu-id="4f9a7-120">Represents the name of the setting.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4f9a7-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4f9a7-121">Parent elements</span></span>

|<span data-ttu-id="4f9a7-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="4f9a7-122">**Element**</span></span>|<span data-ttu-id="4f9a7-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4f9a7-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4f9a7-124">DomainSettingErrors (SOAP)</span><span class="sxs-lookup"><span data-stu-id="4f9a7-124">DomainSettingErrors (SOAP)</span></span>](domainsettingerrors-soap.md) <br/> |<span data-ttu-id="4f9a7-125">Enthält Fehlerinformationen für Einstellungen, die nicht zurückgegeben werden konnten.</span><span class="sxs-lookup"><span data-stu-id="4f9a7-125">Contains error information for settings that could not be returned.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4f9a7-126">Textwert</span><span class="sxs-lookup"><span data-stu-id="4f9a7-126">Text value</span></span>

<span data-ttu-id="4f9a7-127">Keine.</span><span class="sxs-lookup"><span data-stu-id="4f9a7-127">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4f9a7-128">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="4f9a7-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4f9a7-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="4f9a7-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="4f9a7-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="4f9a7-130">Schema Name</span></span>  <br/> |<span data-ttu-id="4f9a7-131">Auto Ermittlungs Schema</span><span class="sxs-lookup"><span data-stu-id="4f9a7-131">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="4f9a7-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="4f9a7-132">Validation File</span></span>  <br/> |<span data-ttu-id="4f9a7-133">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="4f9a7-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="4f9a7-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="4f9a7-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="4f9a7-135">True</span><span class="sxs-lookup"><span data-stu-id="4f9a7-135">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4f9a7-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4f9a7-136">See also</span></span>

- [<span data-ttu-id="4f9a7-137">GetDomainSettings-Vorgang (SOAP)</span><span class="sxs-lookup"><span data-stu-id="4f9a7-137">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

