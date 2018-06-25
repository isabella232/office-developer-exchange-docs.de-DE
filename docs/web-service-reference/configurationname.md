---
title: ConfigurationName
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConfigurationName
api_type:
- schema
ms.assetid: 3b524a2f-9c6b-4550-9f3d-f78d176b0f7b
description: Das ConfigurationName-Element gibt den Namen der angeforderten Dienstkonfigurationen an.
ms.openlocfilehash: a03a0bc0ab7ecbc1c2aec31f864503ee0f560908
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757593"
---
# <a name="configurationname"></a><span data-ttu-id="b6966-103">ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="b6966-103">ConfigurationName</span></span>

<span data-ttu-id="b6966-104">Das **ConfigurationName** -Element gibt den Namen der angeforderten Dienstkonfigurationen an.</span><span class="sxs-lookup"><span data-stu-id="b6966-104">The **ConfigurationName** element specifies the requested service configurations by name.</span></span> 
  
```xml
<ConfigurationName>MailTips or UnifiedMessagingConfiguration or ProtectionRules</ConfigurationName>
```

 <span data-ttu-id="b6966-105">**ServiceConfigurationType**</span><span class="sxs-lookup"><span data-stu-id="b6966-105">**ServiceConfigurationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b6966-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b6966-106">Attributes and elements</span></span>

<span data-ttu-id="b6966-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b6966-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b6966-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="b6966-108">Attributes</span></span>

<span data-ttu-id="b6966-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="b6966-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b6966-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b6966-110">Child elements</span></span>

<span data-ttu-id="b6966-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="b6966-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b6966-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b6966-112">Parent elements</span></span>

|<span data-ttu-id="b6966-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="b6966-113">**Element**</span></span>|<span data-ttu-id="b6966-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b6966-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b6966-115">RequestedConfiguration</span><span class="sxs-lookup"><span data-stu-id="b6966-115">RequestedConfiguration</span></span>](requestedconfiguration.md) <br/> |<span data-ttu-id="b6966-116">Enthält die Konfigurationen für den angeforderten Dienst.</span><span class="sxs-lookup"><span data-stu-id="b6966-116">Contains the requested service configurations.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b6966-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="b6966-117">Text value</span></span>

<span data-ttu-id="b6966-118">Die folgende Tabelle enthält die möglichen Werte für das Element **ConfigurationName** .</span><span class="sxs-lookup"><span data-stu-id="b6966-118">The following table lists the possible values for the **ConfigurationName** element.</span></span> 
  
<span data-ttu-id="b6966-119">**ConfigurationName-Elementwerte**</span><span class="sxs-lookup"><span data-stu-id="b6966-119">**ConfigurationName element values**</span></span>

|<span data-ttu-id="b6966-120">**Wert**</span><span class="sxs-lookup"><span data-stu-id="b6966-120">**Value**</span></span>|<span data-ttu-id="b6966-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b6966-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b6966-122">E-Mail-Infos</span><span class="sxs-lookup"><span data-stu-id="b6966-122">MailTips</span></span>  <br/> |<span data-ttu-id="b6966-123">Identifiziert die e-Mail-Infos-Dienstkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="b6966-123">Identifies the MailTips service configuration.</span></span>  <br/> |
|<span data-ttu-id="b6966-124">UnifiedMessagingConfiguration</span><span class="sxs-lookup"><span data-stu-id="b6966-124">UnifiedMessagingConfiguration</span></span>  <br/> |<span data-ttu-id="b6966-125">Identifiziert die Unified Messaging-Dienstkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="b6966-125">Identifies the Unified Messaging service configuration.</span></span>  <br/> |
|<span data-ttu-id="b6966-126">ProtectionRules</span><span class="sxs-lookup"><span data-stu-id="b6966-126">ProtectionRules</span></span>  <br/> |<span data-ttu-id="b6966-127">Identifiziert die Dienstkonfiguration Protection Rules.</span><span class="sxs-lookup"><span data-stu-id="b6966-127">Identifies the Protection Rules service configuration.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b6966-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b6966-128">Remarks</span></span>

<span data-ttu-id="b6966-129">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="b6966-129">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b6966-130">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="b6966-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b6966-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="b6966-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b6966-132">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b6966-132">Schema Name</span></span>  <br/> |<span data-ttu-id="b6966-133">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="b6966-133">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b6966-134">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b6966-134">Validation File</span></span>  <br/> |<span data-ttu-id="b6966-135">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="b6966-135">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b6966-136">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="b6966-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="b6966-137">False</span><span class="sxs-lookup"><span data-stu-id="b6966-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b6966-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b6966-138">See also</span></span>



- [<span data-ttu-id="b6966-139">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="b6966-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

