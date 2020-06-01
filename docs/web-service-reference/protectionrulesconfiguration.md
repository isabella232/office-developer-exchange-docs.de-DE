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
description: Das ProtectionRulesConfiguration-Element enthält Dienstkonfigurationsinformationen für den Schutz Regeldienst.
ms.openlocfilehash: e664fba78f170c9f4c59b49b3a08c0dd2e4ed4cd
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456764"
---
# <a name="protectionrulesconfiguration"></a><span data-ttu-id="3ab16-103">ProtectionRulesConfiguration</span><span class="sxs-lookup"><span data-stu-id="3ab16-103">ProtectionRulesConfiguration</span></span>

<span data-ttu-id="3ab16-104">Das **ProtectionRulesConfiguration** -Element enthält Dienstkonfigurationsinformationen für den Schutz Regeldienst.</span><span class="sxs-lookup"><span data-stu-id="3ab16-104">The **ProtectionRulesConfiguration** element contains service configuration information for the protection rules service.</span></span> 
  
```XML
<ProtectionRulesConfiguration RefreshInterval="">
   <Rules/>
   <InternalDomains/>
</ProtectionRulesConfiguration>
```

 <span data-ttu-id="3ab16-105">**ProtectionRulesServiceConfiguration**</span><span class="sxs-lookup"><span data-stu-id="3ab16-105">**ProtectionRulesServiceConfiguration**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3ab16-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3ab16-106">Attributes and elements</span></span>

<span data-ttu-id="3ab16-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="3ab16-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3ab16-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="3ab16-108">Attributes</span></span>

|<span data-ttu-id="3ab16-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="3ab16-109">**Attribute**</span></span>|<span data-ttu-id="3ab16-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3ab16-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3ab16-111">**RefreshInterval**</span><span class="sxs-lookup"><span data-stu-id="3ab16-111">**RefreshInterval**</span></span> <br/> |<span data-ttu-id="3ab16-112">Gibt an, wie oft der Client in ganzen Stunden Schutzregeln vom Server anfordern soll.</span><span class="sxs-lookup"><span data-stu-id="3ab16-112">Specifies how often, in whole hours, the client should request protection rules from the server.</span></span> <span data-ttu-id="3ab16-113">Dieses Attribut ist erforderlich, und der Wert muss eine ganze Zahl sein, die größer oder gleich 1 ist.</span><span class="sxs-lookup"><span data-stu-id="3ab16-113">This attribute is required and its value must be an integer that is equal to or greater than 1.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="3ab16-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3ab16-114">Child elements</span></span>

|<span data-ttu-id="3ab16-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="3ab16-115">**Element**</span></span>|<span data-ttu-id="3ab16-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3ab16-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3ab16-117">Regeln</span><span class="sxs-lookup"><span data-stu-id="3ab16-117">Rules </span></span>](rules-ex15websvcsotherref.md) <br/> |<span data-ttu-id="3ab16-118">Ein Array von Schutzregeln.</span><span class="sxs-lookup"><span data-stu-id="3ab16-118">An array of protection rules.</span></span> <span data-ttu-id="3ab16-119">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3ab16-119">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="3ab16-120">InternalDomains (SmtpDomainList)</span><span class="sxs-lookup"><span data-stu-id="3ab16-120">InternalDomains (SmtpDomainList)</span></span>](internaldomains-smtpdomainlist.md) <br/> |<span data-ttu-id="3ab16-121">Gibt die Liste der internen SMTP-Domänen der Organisation an.</span><span class="sxs-lookup"><span data-stu-id="3ab16-121">Identifies the list of internal SMTP domains of the organization.</span></span> <span data-ttu-id="3ab16-122">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3ab16-122">This element is required.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3ab16-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3ab16-123">Parent elements</span></span>

|<span data-ttu-id="3ab16-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="3ab16-124">**Element**</span></span>|<span data-ttu-id="3ab16-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3ab16-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3ab16-126">ServiceConfigurationResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="3ab16-126">ServiceConfigurationResponseMessageType</span></span>](serviceconfigurationresponsemessagetype.md) <br/> |<span data-ttu-id="3ab16-127">Enthält Dienst Konfigurationseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="3ab16-127">Contains service configuration settings.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3ab16-128">Textwert</span><span class="sxs-lookup"><span data-stu-id="3ab16-128">Text value</span></span>

<span data-ttu-id="3ab16-129">Keine.</span><span class="sxs-lookup"><span data-stu-id="3ab16-129">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3ab16-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3ab16-130">Remarks</span></span>

<span data-ttu-id="3ab16-131">Die Konfiguration des Schutz Regel Diensts besteht aus einer Liste von Regeln, internen Domänen und einem Aktualisierungsintervall.</span><span class="sxs-lookup"><span data-stu-id="3ab16-131">The protection rules service configuration is comprised of a list of rules, internal domains, and a refresh interval.</span></span>
  
<span data-ttu-id="3ab16-132">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="3ab16-132">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3ab16-133">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="3ab16-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3ab16-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="3ab16-134">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="3ab16-135">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="3ab16-135">Schema Name</span></span>  <br/> |<span data-ttu-id="3ab16-136">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="3ab16-136">Messages schema</span></span>  <br/> |
|<span data-ttu-id="3ab16-137">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="3ab16-137">Validation File</span></span>  <br/> |<span data-ttu-id="3ab16-138">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="3ab16-138">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3ab16-139">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="3ab16-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="3ab16-140">False</span><span class="sxs-lookup"><span data-stu-id="3ab16-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3ab16-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3ab16-141">See also</span></span>



- [<span data-ttu-id="3ab16-142">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="3ab16-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

