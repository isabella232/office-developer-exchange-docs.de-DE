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
description: Das configurationName-Element gibt die angeforderten Dienstkonfigurationen nach Namen an.
ms.openlocfilehash: 5e1216253a633af643dbd276827842dbe2db5d5f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463923"
---
# <a name="configurationname"></a><span data-ttu-id="fada7-103">ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="fada7-103">ConfigurationName</span></span>

<span data-ttu-id="fada7-104">Das **ConfigurationName** -Element gibt die angeforderten Dienstkonfigurationen nach Namen an.</span><span class="sxs-lookup"><span data-stu-id="fada7-104">The **ConfigurationName** element specifies the requested service configurations by name.</span></span> 
  
```xml
<ConfigurationName>MailTips or UnifiedMessagingConfiguration or ProtectionRules</ConfigurationName>
```

 <span data-ttu-id="fada7-105">**ServiceConfigurationType**</span><span class="sxs-lookup"><span data-stu-id="fada7-105">**ServiceConfigurationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fada7-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="fada7-106">Attributes and elements</span></span>

<span data-ttu-id="fada7-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="fada7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fada7-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="fada7-108">Attributes</span></span>

<span data-ttu-id="fada7-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="fada7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fada7-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fada7-110">Child elements</span></span>

<span data-ttu-id="fada7-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="fada7-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="fada7-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fada7-112">Parent elements</span></span>

|<span data-ttu-id="fada7-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="fada7-113">**Element**</span></span>|<span data-ttu-id="fada7-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fada7-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fada7-115">RequestedConfiguration</span><span class="sxs-lookup"><span data-stu-id="fada7-115">RequestedConfiguration</span></span>](requestedconfiguration.md) <br/> |<span data-ttu-id="fada7-116">Enthält die angeforderten Dienstkonfigurationen.</span><span class="sxs-lookup"><span data-stu-id="fada7-116">Contains the requested service configurations.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="fada7-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="fada7-117">Text value</span></span>

<span data-ttu-id="fada7-118">In der folgenden Tabelle sind die möglichen Werte für das **ConfigurationName** -Element aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="fada7-118">The following table lists the possible values for the **ConfigurationName** element.</span></span> 
  
<span data-ttu-id="fada7-119">**Werte des ConfigurationName-Elements**</span><span class="sxs-lookup"><span data-stu-id="fada7-119">**ConfigurationName element values**</span></span>

|<span data-ttu-id="fada7-120">**Wert**</span><span class="sxs-lookup"><span data-stu-id="fada7-120">**Value**</span></span>|<span data-ttu-id="fada7-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fada7-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fada7-122">MailTips</span><span class="sxs-lookup"><span data-stu-id="fada7-122">MailTips</span></span>  <br/> |<span data-ttu-id="fada7-123">Identifiziert die e-Mail-Infos-Dienstkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="fada7-123">Identifies the MailTips service configuration.</span></span>  <br/> |
|<span data-ttu-id="fada7-124">UnifiedMessagingConfiguration</span><span class="sxs-lookup"><span data-stu-id="fada7-124">UnifiedMessagingConfiguration</span></span>  <br/> |<span data-ttu-id="fada7-125">Gibt die Konfiguration des Unified Messaging-Diensts an.</span><span class="sxs-lookup"><span data-stu-id="fada7-125">Identifies the Unified Messaging service configuration.</span></span>  <br/> |
|<span data-ttu-id="fada7-126">ProtectionRules</span><span class="sxs-lookup"><span data-stu-id="fada7-126">ProtectionRules</span></span>  <br/> |<span data-ttu-id="fada7-127">Identifiziert die Dienstkonfiguration des Schutz Regel Diensts.</span><span class="sxs-lookup"><span data-stu-id="fada7-127">Identifies the Protection Rules service configuration.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fada7-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fada7-128">Remarks</span></span>

<span data-ttu-id="fada7-129">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="fada7-129">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fada7-130">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="fada7-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fada7-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="fada7-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="fada7-132">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="fada7-132">Schema Name</span></span>  <br/> |<span data-ttu-id="fada7-133">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="fada7-133">Messages schema</span></span>  <br/> |
|<span data-ttu-id="fada7-134">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="fada7-134">Validation File</span></span>  <br/> |<span data-ttu-id="fada7-135">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="fada7-135">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="fada7-136">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="fada7-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="fada7-137">False</span><span class="sxs-lookup"><span data-stu-id="fada7-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fada7-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fada7-138">See also</span></span>



- [<span data-ttu-id="fada7-139">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="fada7-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

