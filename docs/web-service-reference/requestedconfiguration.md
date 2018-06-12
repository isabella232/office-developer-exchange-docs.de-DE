---
title: RequestedConfiguration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RequestedConfiguration
api_type:
- schema
ms.assetid: 24921387-f676-49e6-8d7a-ef3115024866
description: Das RequestedConfiguration-Element enthält die Konfigurationen für den angeforderten Dienst.
ms.openlocfilehash: 1edc6394360250c9a9810fe614c975cb48eba3f0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831130"
---
# <a name="requestedconfiguration"></a><span data-ttu-id="81bdf-103">RequestedConfiguration</span><span class="sxs-lookup"><span data-stu-id="81bdf-103">RequestedConfiguration</span></span>

<span data-ttu-id="81bdf-104">Das **RequestedConfiguration** -Element enthält die Konfigurationen für den angeforderten Dienst.</span><span class="sxs-lookup"><span data-stu-id="81bdf-104">The **RequestedConfiguration** element contains the requested service configurations.</span></span> 
  
```XML
<RequestedConfiguration>
   <ConfigurationName/>
</RequestedConfiguration>
```

 <span data-ttu-id="81bdf-105">**ArrayOfServiceConfigurationType**</span><span class="sxs-lookup"><span data-stu-id="81bdf-105">**ArrayOfServiceConfigurationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="81bdf-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="81bdf-106">Attributes and elements</span></span>

<span data-ttu-id="81bdf-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="81bdf-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="81bdf-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="81bdf-108">Attributes</span></span>

<span data-ttu-id="81bdf-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="81bdf-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="81bdf-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="81bdf-110">Child elements</span></span>

|<span data-ttu-id="81bdf-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="81bdf-111">**Element**</span></span>|<span data-ttu-id="81bdf-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="81bdf-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="81bdf-113">ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="81bdf-113">ConfigurationName</span></span>](configurationname.md) <br/> |<span data-ttu-id="81bdf-114">Gibt den Namen der angeforderten Dienstkonfigurationen an.</span><span class="sxs-lookup"><span data-stu-id="81bdf-114">Specifies the requested service configurations by name.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="81bdf-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="81bdf-115">Parent elements</span></span>

|<span data-ttu-id="81bdf-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="81bdf-116">**Element**</span></span>|<span data-ttu-id="81bdf-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="81bdf-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="81bdf-118">GetServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="81bdf-118">GetServiceConfiguration</span></span>](getserviceconfiguration.md) <br/> |<span data-ttu-id="81bdf-119">Definiert eine GetServiceConfiguration-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="81bdf-119">Defines a GetServiceConfiguration request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="81bdf-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="81bdf-120">Text value</span></span>

<span data-ttu-id="81bdf-121">Keine.</span><span class="sxs-lookup"><span data-stu-id="81bdf-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="81bdf-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="81bdf-122">Remarks</span></span>

<span data-ttu-id="81bdf-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="81bdf-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="81bdf-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="81bdf-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="81bdf-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="81bdf-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="81bdf-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="81bdf-126">Schema Name</span></span>  <br/> |<span data-ttu-id="81bdf-127">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="81bdf-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="81bdf-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="81bdf-128">Validation File</span></span>  <br/> |<span data-ttu-id="81bdf-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="81bdf-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="81bdf-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="81bdf-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="81bdf-131">False</span><span class="sxs-lookup"><span data-stu-id="81bdf-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="81bdf-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="81bdf-132">See also</span></span>



- [<span data-ttu-id="81bdf-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="81bdf-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

