---
title: ProtectionRulesConfiguration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ProtectionRulesConfiguration
api_type:
- schema
ms.assetid: e5b4699a-476e-4053-bb52-873eb921c046
description: Das ProtectionRulesConfiguration-Element enthält Konfigurationsinformationen für den Schutz Regeln Dienst Service.
ms.openlocfilehash: 9c286fcf9752d591d53323f45a264f4bdd078c1c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830912"
---
# <a name="protectionrulesconfiguration"></a><span data-ttu-id="7fdd2-103">ProtectionRulesConfiguration</span><span class="sxs-lookup"><span data-stu-id="7fdd2-103">ProtectionRulesConfiguration</span></span>

<span data-ttu-id="7fdd2-104">Das **ProtectionRulesConfiguration** -Element enthält Konfigurationsinformationen für den Schutz Regeln Dienst Service.</span><span class="sxs-lookup"><span data-stu-id="7fdd2-104">The **ProtectionRulesConfiguration** element contains service configuration information for the protection rules service.</span></span> 
  
```XML
<ProtectionRulesConfiguration RefreshInterval="">
   <Rules/>
   <InternalDomains/>
</ProtectionRulesConfiguration>
```

 <span data-ttu-id="7fdd2-105">**ProtectionRulesServiceConfiguration**</span><span class="sxs-lookup"><span data-stu-id="7fdd2-105">**ProtectionRulesServiceConfiguration**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7fdd2-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="7fdd2-106">Attributes and elements</span></span>

<span data-ttu-id="7fdd2-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="7fdd2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7fdd2-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="7fdd2-108">Attributes</span></span>

|<span data-ttu-id="7fdd2-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="7fdd2-109">**Attribute**</span></span>|<span data-ttu-id="7fdd2-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7fdd2-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7fdd2-111">**RefreshInterval**</span><span class="sxs-lookup"><span data-stu-id="7fdd2-111">**RefreshInterval**</span></span> <br/> |<span data-ttu-id="7fdd2-112">Gibt an, wie oft in ganzen Stunden der Client-Schutzregeln vom Server anfordern soll.</span><span class="sxs-lookup"><span data-stu-id="7fdd2-112">Specifies how often, in whole hours, the client should request protection rules from the server.</span></span> <span data-ttu-id="7fdd2-113">Dieses Attribut ist erforderlich, und der Wert muss eine ganze Zahl, die gleich oder größer als 1 ist.</span><span class="sxs-lookup"><span data-stu-id="7fdd2-113">This attribute is required and its value must be an integer that is equal to or greater than 1.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7fdd2-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7fdd2-114">Child elements</span></span>

|<span data-ttu-id="7fdd2-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="7fdd2-115">**Element**</span></span>|<span data-ttu-id="7fdd2-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7fdd2-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7fdd2-117">Regeln</span><span class="sxs-lookup"><span data-stu-id="7fdd2-117">Rules </span></span>](rules-ex15websvcsotherref.md) <br/> |<span data-ttu-id="7fdd2-118">Ein Array von Regeln für den Schutz.</span><span class="sxs-lookup"><span data-stu-id="7fdd2-118">An array of protection rules.</span></span> <span data-ttu-id="7fdd2-119">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7fdd2-119">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="7fdd2-120">InternalDomains (SmtpDomainList)</span><span class="sxs-lookup"><span data-stu-id="7fdd2-120">InternalDomains (SmtpDomainList)</span></span>](internaldomains-smtpdomainlist.md) <br/> |<span data-ttu-id="7fdd2-121">Gibt die Liste der internen SMTP-Domänen der Organisation.</span><span class="sxs-lookup"><span data-stu-id="7fdd2-121">Identifies the list of internal SMTP domains of the organization.</span></span> <span data-ttu-id="7fdd2-122">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7fdd2-122">This element is required.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7fdd2-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7fdd2-123">Parent elements</span></span>

|<span data-ttu-id="7fdd2-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="7fdd2-124">**Element**</span></span>|<span data-ttu-id="7fdd2-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7fdd2-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7fdd2-126">ServiceConfigurationResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="7fdd2-126">ServiceConfigurationResponseMessageType</span></span>](serviceconfigurationresponsemessagetype.md) <br/> |<span data-ttu-id="7fdd2-127">Konfigurationseinstellungen für enthält.</span><span class="sxs-lookup"><span data-stu-id="7fdd2-127">Contains service configuration settings.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7fdd2-128">Textwert</span><span class="sxs-lookup"><span data-stu-id="7fdd2-128">Text value</span></span>

<span data-ttu-id="7fdd2-129">Keine.</span><span class="sxs-lookup"><span data-stu-id="7fdd2-129">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7fdd2-130">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7fdd2-130">Remarks</span></span>

<span data-ttu-id="7fdd2-131">Eine Liste der Regeln, interne Domänen und ein Aktualisierungsintervall besteht die Konfiguration für den Schutz-Regeln.</span><span class="sxs-lookup"><span data-stu-id="7fdd2-131">The protection rules service configuration is comprised of a list of rules, internal domains, and a refresh interval.</span></span>
  
<span data-ttu-id="7fdd2-132">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="7fdd2-132">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7fdd2-133">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="7fdd2-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7fdd2-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="7fdd2-134">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="7fdd2-135">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="7fdd2-135">Schema Name</span></span>  <br/> |<span data-ttu-id="7fdd2-136">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="7fdd2-136">Messages schema</span></span>  <br/> |
|<span data-ttu-id="7fdd2-137">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="7fdd2-137">Validation File</span></span>  <br/> |<span data-ttu-id="7fdd2-138">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="7fdd2-138">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7fdd2-139">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="7fdd2-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="7fdd2-140">False</span><span class="sxs-lookup"><span data-stu-id="7fdd2-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7fdd2-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7fdd2-141">See also</span></span>



- [<span data-ttu-id="7fdd2-142">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="7fdd2-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

