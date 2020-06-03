---
title: UnifiedMessagingConfiguration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UnifiedMessagingConfiguration
api_type:
- schema
ms.assetid: cbdb4268-077e-44ed-8ec2-9d759c84cc6d
description: Das UnifiedMessagingConfiguration-Element enthält Dienstkonfigurationsinformationen für den Unified Messaging-Dienst.
ms.openlocfilehash: 3f9f4ed65721929c552615c07e2239f48ef837f3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528692"
---
# <a name="unifiedmessagingconfiguration"></a><span data-ttu-id="32f70-103">UnifiedMessagingConfiguration</span><span class="sxs-lookup"><span data-stu-id="32f70-103">UnifiedMessagingConfiguration</span></span>

<span data-ttu-id="32f70-104">Das **UnifiedMessagingConfiguration** -Element enthält Dienstkonfigurationsinformationen für den Unified Messaging-Dienst.</span><span class="sxs-lookup"><span data-stu-id="32f70-104">The **UnifiedMessagingConfiguration** element contains service configuration information for the Unified Messaging service.</span></span> 
  
```XML
<UnifiedMessagingConfiguration>
   <UmEnabled/>
   <PlayOnPhoneDialString/>
   <PlayOnPhoneEnabled/>
</UnifiedMessagingConfiguration>
```

 <span data-ttu-id="32f70-105">**UnifiedMessageServiceConfiguration**</span><span class="sxs-lookup"><span data-stu-id="32f70-105">**UnifiedMessageServiceConfiguration**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="32f70-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="32f70-106">Attributes and elements</span></span>

<span data-ttu-id="32f70-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="32f70-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="32f70-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="32f70-108">Attributes</span></span>

<span data-ttu-id="32f70-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="32f70-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="32f70-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="32f70-110">Child elements</span></span>

|<span data-ttu-id="32f70-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="32f70-111">**Element**</span></span>|<span data-ttu-id="32f70-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="32f70-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="32f70-113">UmEnabled</span><span class="sxs-lookup"><span data-stu-id="32f70-113">UmEnabled</span></span>](umenabled.md) <br/> |<span data-ttu-id="32f70-114">Gibt an, ob Unified Messaging für ein Konto aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="32f70-114">Indicates whether Unified Messaging is enabled for an account.</span></span> <span data-ttu-id="32f70-115">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="32f70-115">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="32f70-116">PlayOnPhoneDialString (Exchange Webdienste)</span><span class="sxs-lookup"><span data-stu-id="32f70-116">PlayOnPhoneDialString (Exchange Web Services)</span></span>](playonphonedialstring-exchange-web-services.md) <br/> |<span data-ttu-id="32f70-117">Identifiziert die Wählzeichenfolge für die Wiedergabe bei anrufen.</span><span class="sxs-lookup"><span data-stu-id="32f70-117">Identifies the Play-on-Phone dial string.</span></span> <span data-ttu-id="32f70-118">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="32f70-118">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="32f70-119">PlayOnPhoneEnabled</span><span class="sxs-lookup"><span data-stu-id="32f70-119">PlayOnPhoneEnabled</span></span>](playonphoneenabled.md) <br/> |<span data-ttu-id="32f70-120">Gibt an, ob die Funktion "Wiedergabe-Telefon" aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="32f70-120">Indicates whether the Play-on-Phone feature is enabled.</span></span> <span data-ttu-id="32f70-121">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="32f70-121">This element is required.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="32f70-122">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="32f70-122">Parent elements</span></span>

|<span data-ttu-id="32f70-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="32f70-123">**Element**</span></span>|<span data-ttu-id="32f70-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="32f70-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="32f70-125">ServiceConfigurationResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="32f70-125">ServiceConfigurationResponseMessageType</span></span>](serviceconfigurationresponsemessagetype.md) <br/> |<span data-ttu-id="32f70-126">Enthält Dienst Konfigurationseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="32f70-126">Contains service configuration settings.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="32f70-127">Textwert</span><span class="sxs-lookup"><span data-stu-id="32f70-127">Text value</span></span>

<span data-ttu-id="32f70-128">Keine.</span><span class="sxs-lookup"><span data-stu-id="32f70-128">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="32f70-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="32f70-129">Remarks</span></span>

<span data-ttu-id="32f70-130">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="32f70-130">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="32f70-131">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="32f70-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="32f70-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="32f70-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="32f70-133">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="32f70-133">Schema Name</span></span>  <br/> |<span data-ttu-id="32f70-134">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="32f70-134">Messages schema</span></span>  <br/> |
|<span data-ttu-id="32f70-135">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="32f70-135">Validation File</span></span>  <br/> |<span data-ttu-id="32f70-136">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="32f70-136">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="32f70-137">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="32f70-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="32f70-138">False</span><span class="sxs-lookup"><span data-stu-id="32f70-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="32f70-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="32f70-139">See also</span></span>



- [<span data-ttu-id="32f70-140">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="32f70-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

