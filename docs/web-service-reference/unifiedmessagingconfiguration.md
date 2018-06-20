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
description: Das UnifiedMessagingConfiguration-Element enthält Webdienst-Konfigurationsinformationen für die Unified Messaging-Dienst.
ms.openlocfilehash: 3ad8f66ecdf21062c00c2a6ac6f65fac875da38c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839293"
---
# <a name="unifiedmessagingconfiguration"></a><span data-ttu-id="02887-103">UnifiedMessagingConfiguration</span><span class="sxs-lookup"><span data-stu-id="02887-103">UnifiedMessagingConfiguration</span></span>

<span data-ttu-id="02887-104">Das **UnifiedMessagingConfiguration** -Element enthält Webdienst-Konfigurationsinformationen für die Unified Messaging-Dienst.</span><span class="sxs-lookup"><span data-stu-id="02887-104">The **UnifiedMessagingConfiguration** element contains service configuration information for the Unified Messaging service.</span></span> 
  
```XML
<UnifiedMessagingConfiguration>
   <UmEnabled/>
   <PlayOnPhoneDialString/>
   <PlayOnPhoneEnabled/>
</UnifiedMessagingConfiguration>
```

 <span data-ttu-id="02887-105">**UnifiedMessageServiceConfiguration**</span><span class="sxs-lookup"><span data-stu-id="02887-105">**UnifiedMessageServiceConfiguration**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="02887-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="02887-106">Attributes and elements</span></span>

<span data-ttu-id="02887-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="02887-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="02887-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="02887-108">Attributes</span></span>

<span data-ttu-id="02887-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="02887-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="02887-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="02887-110">Child elements</span></span>

|<span data-ttu-id="02887-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="02887-111">**Element**</span></span>|<span data-ttu-id="02887-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="02887-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="02887-113">UmEnabled</span><span class="sxs-lookup"><span data-stu-id="02887-113">UmEnabled</span></span>](umenabled.md) <br/> |<span data-ttu-id="02887-114">Gibt an, ob für ein Konto Unified Messaging aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="02887-114">Indicates whether Unified Messaging is enabled for an account.</span></span> <span data-ttu-id="02887-115">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="02887-115">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="02887-116">PlayOnPhoneDialString (Exchange Web Services)</span><span class="sxs-lookup"><span data-stu-id="02887-116">PlayOnPhoneDialString (Exchange Web Services)</span></span>](playonphonedialstring-exchange-web-services.md) <br/> |<span data-ttu-id="02887-117">Gibt die Wiedergabe über Telefon DFÜ-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="02887-117">Identifies the Play-on-Phone dial string.</span></span> <span data-ttu-id="02887-118">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="02887-118">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="02887-119">PlayOnPhoneEnabled</span><span class="sxs-lookup"><span data-stu-id="02887-119">PlayOnPhoneEnabled</span></span>](playonphoneenabled.md) <br/> |<span data-ttu-id="02887-120">Gibt an, ob das Wiedergabe über Telefon-Feature aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="02887-120">Indicates whether the Play-on-Phone feature is enabled.</span></span> <span data-ttu-id="02887-121">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="02887-121">This element is required.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="02887-122">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="02887-122">Parent elements</span></span>

|<span data-ttu-id="02887-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="02887-123">**Element**</span></span>|<span data-ttu-id="02887-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="02887-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="02887-125">ServiceConfigurationResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="02887-125">ServiceConfigurationResponseMessageType</span></span>](serviceconfigurationresponsemessagetype.md) <br/> |<span data-ttu-id="02887-126">Konfigurationseinstellungen für enthält.</span><span class="sxs-lookup"><span data-stu-id="02887-126">Contains service configuration settings.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="02887-127">Textwert</span><span class="sxs-lookup"><span data-stu-id="02887-127">Text value</span></span>

<span data-ttu-id="02887-128">Keine.</span><span class="sxs-lookup"><span data-stu-id="02887-128">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="02887-129">Hinweise</span><span class="sxs-lookup"><span data-stu-id="02887-129">Remarks</span></span>

<span data-ttu-id="02887-130">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="02887-130">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="02887-131">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="02887-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="02887-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="02887-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="02887-133">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="02887-133">Schema Name</span></span>  <br/> |<span data-ttu-id="02887-134">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="02887-134">Messages schema</span></span>  <br/> |
|<span data-ttu-id="02887-135">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="02887-135">Validation File</span></span>  <br/> |<span data-ttu-id="02887-136">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="02887-136">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="02887-137">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="02887-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="02887-138">False</span><span class="sxs-lookup"><span data-stu-id="02887-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="02887-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="02887-139">See also</span></span>



- [<span data-ttu-id="02887-140">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="02887-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

