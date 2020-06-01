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
description: Das RequestedConfiguration-Element enthält die angeforderten Dienstkonfigurationen.
ms.openlocfilehash: bbc503e6d6f7c56c785365924106bc2468965d0b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457151"
---
# <a name="requestedconfiguration"></a><span data-ttu-id="0ac54-103">RequestedConfiguration</span><span class="sxs-lookup"><span data-stu-id="0ac54-103">RequestedConfiguration</span></span>

<span data-ttu-id="0ac54-104">Das **RequestedConfiguration** -Element enthält die angeforderten Dienstkonfigurationen.</span><span class="sxs-lookup"><span data-stu-id="0ac54-104">The **RequestedConfiguration** element contains the requested service configurations.</span></span> 
  
```XML
<RequestedConfiguration>
   <ConfigurationName/>
</RequestedConfiguration>
```

 <span data-ttu-id="0ac54-105">**ArrayOfServiceConfigurationType**</span><span class="sxs-lookup"><span data-stu-id="0ac54-105">**ArrayOfServiceConfigurationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0ac54-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="0ac54-106">Attributes and elements</span></span>

<span data-ttu-id="0ac54-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="0ac54-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0ac54-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="0ac54-108">Attributes</span></span>

<span data-ttu-id="0ac54-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="0ac54-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0ac54-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0ac54-110">Child elements</span></span>

|<span data-ttu-id="0ac54-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="0ac54-111">**Element**</span></span>|<span data-ttu-id="0ac54-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0ac54-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0ac54-113">ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="0ac54-113">ConfigurationName</span></span>](configurationname.md) <br/> |<span data-ttu-id="0ac54-114">Gibt die angeforderten Dienstkonfigurationen nach Namen an.</span><span class="sxs-lookup"><span data-stu-id="0ac54-114">Specifies the requested service configurations by name.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0ac54-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0ac54-115">Parent elements</span></span>

|<span data-ttu-id="0ac54-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="0ac54-116">**Element**</span></span>|<span data-ttu-id="0ac54-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0ac54-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0ac54-118">GetServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="0ac54-118">GetServiceConfiguration</span></span>](getserviceconfiguration.md) <br/> |<span data-ttu-id="0ac54-119">Definiert eine GetServiceConfiguration-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="0ac54-119">Defines a GetServiceConfiguration request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0ac54-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="0ac54-120">Text value</span></span>

<span data-ttu-id="0ac54-121">Keine.</span><span class="sxs-lookup"><span data-stu-id="0ac54-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0ac54-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0ac54-122">Remarks</span></span>

<span data-ttu-id="0ac54-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="0ac54-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0ac54-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="0ac54-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0ac54-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="0ac54-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0ac54-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="0ac54-126">Schema Name</span></span>  <br/> |<span data-ttu-id="0ac54-127">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="0ac54-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="0ac54-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="0ac54-128">Validation File</span></span>  <br/> |<span data-ttu-id="0ac54-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="0ac54-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0ac54-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="0ac54-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="0ac54-131">False</span><span class="sxs-lookup"><span data-stu-id="0ac54-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0ac54-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0ac54-132">See also</span></span>



- [<span data-ttu-id="0ac54-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="0ac54-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

