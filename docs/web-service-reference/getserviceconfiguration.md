---
title: GetServiceConfiguration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetServiceConfiguration
api_type:
- schema
ms.assetid: acbb29e4-d853-4302-8e32-7018775d54e4
description: Das GetServiceConfiguration-Element definiert eine GetServiceConfiguration-Anforderung.
ms.openlocfilehash: 7ff7124ff062f21a02fc69b86b7cc7367ba3fcb6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19829666"
---
# <a name="getserviceconfiguration"></a><span data-ttu-id="53e4f-103">GetServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="53e4f-103">GetServiceConfiguration</span></span>

<span data-ttu-id="53e4f-104">Das **GetServiceConfiguration** -Element definiert eine GetServiceConfiguration-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="53e4f-104">The **GetServiceConfiguration** element defines a GetServiceConfiguration request.</span></span> 
  
```XML
<GetServiceConfiguration>
   <ActingAs/>
   <RequestedConfiguration/>
</GetServiceConfiguration>
```

 <span data-ttu-id="53e4f-105">**GetServiceConfigurationType**</span><span class="sxs-lookup"><span data-stu-id="53e4f-105">**GetServiceConfigurationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="53e4f-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="53e4f-106">Attributes and elements</span></span>

<span data-ttu-id="53e4f-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="53e4f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="53e4f-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="53e4f-108">Attributes</span></span>

<span data-ttu-id="53e4f-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="53e4f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="53e4f-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="53e4f-110">Child elements</span></span>

|<span data-ttu-id="53e4f-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="53e4f-111">**Element**</span></span>|<span data-ttu-id="53e4f-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="53e4f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="53e4f-113">ActingAs</span><span class="sxs-lookup"><span data-stu-id="53e4f-113">ActingAs</span></span>](actingas.md) <br/> |<span data-ttu-id="53e4f-114">Identifiziert, die der Anrufer als sendet.</span><span class="sxs-lookup"><span data-stu-id="53e4f-114">Identifies who the caller is sending as.</span></span> <span data-ttu-id="53e4f-115">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="53e4f-115">This element is optional.</span></span> <span data-ttu-id="53e4f-116">Wenn dieses Element nicht vorhanden ist, wird davon ausgegangen, dass der authentifizierte Benutzer die Absender werden.</span><span class="sxs-lookup"><span data-stu-id="53e4f-116">If this element is not present, the authenticated user is assumed to be the sender.</span></span> <span data-ttu-id="53e4f-117">Das **ActingAs** -Element muss für die Anforderung des Absenders Hinweise eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="53e4f-117">The **ActingAs** element must be included for requesting sender hints.</span></span> <span data-ttu-id="53e4f-118">Fehler ErrorInvalidArgument kann in einer Antwort zurückgegeben werden soll, wenn das **ActingAs** -Element nicht vorhanden ist, enthält keine Routingtyp, eine e-Mail-Adresse nicht umfasst, eine ungültige e-Mail-Adresse enthält, nicht an einen Benutzer in Active Directory-Domäne löst Services (AD DS), oder auf mehrere Benutzer in AD DS aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="53e4f-118">An ErrorInvalidArgument error can be returned in a response if the **ActingAs** element is missing, does not include a routing type, does not include an e-mail address, contains an invalid e-mail address, does not resolve to a user in Active Directory Domain Services (AD DS), or resolves to multiple users in AD DS.</span></span>  <br/> |
|[<span data-ttu-id="53e4f-119">RequestedConfiguration</span><span class="sxs-lookup"><span data-stu-id="53e4f-119">RequestedConfiguration</span></span>](requestedconfiguration.md) <br/> |<span data-ttu-id="53e4f-120">Enthält die Konfigurationen für den angeforderten Dienst.</span><span class="sxs-lookup"><span data-stu-id="53e4f-120">Contains the requested service configurations.</span></span> <span data-ttu-id="53e4f-121">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="53e4f-121">This element is required.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="53e4f-122">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="53e4f-122">Parent elements</span></span>

<span data-ttu-id="53e4f-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="53e4f-123">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="53e4f-124">Textwert</span><span class="sxs-lookup"><span data-stu-id="53e4f-124">Text value</span></span>

<span data-ttu-id="53e4f-125">Keine.</span><span class="sxs-lookup"><span data-stu-id="53e4f-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="53e4f-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="53e4f-126">Remarks</span></span>

<span data-ttu-id="53e4f-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="53e4f-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="53e4f-128">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="53e4f-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="53e4f-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="53e4f-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="53e4f-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="53e4f-130">Schema Name</span></span>  <br/> |<span data-ttu-id="53e4f-131">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="53e4f-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="53e4f-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="53e4f-132">Validation File</span></span>  <br/> |<span data-ttu-id="53e4f-133">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="53e4f-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="53e4f-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="53e4f-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="53e4f-135">False</span><span class="sxs-lookup"><span data-stu-id="53e4f-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="53e4f-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="53e4f-136">See also</span></span>



- [<span data-ttu-id="53e4f-137">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="53e4f-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

