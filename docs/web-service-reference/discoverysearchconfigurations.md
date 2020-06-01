---
title: DiscoverySearchConfigurations
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f04b14c9-384c-4016-b113-52a49e15e73b
description: Das DiscoverySearchConfigurations-Element gibt ein Array von DiscoverySearchConfiguration-Elementen an.
ms.openlocfilehash: 6af4c8198f2ad73f8b39f9718e11b88aa8075c39
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461380"
---
# <a name="discoverysearchconfigurations"></a><span data-ttu-id="17acb-103">DiscoverySearchConfigurations</span><span class="sxs-lookup"><span data-stu-id="17acb-103">DiscoverySearchConfigurations</span></span>

<span data-ttu-id="17acb-104">Das **DiscoverySearchConfigurations** -Element gibt ein Array von **DiscoverySearchConfiguration** -Elementen an.</span><span class="sxs-lookup"><span data-stu-id="17acb-104">The **DiscoverySearchConfigurations** element specifies an array of **DiscoverySearchConfiguration** elements.</span></span> 
  
```XML
<DiscoverySearchConfigurations>
    <DiscoverySearchConfiguration></DiscoverySearchConfiguration>
</DiscoverySearchConfigurations>
```

 <span data-ttu-id="17acb-105">**ArrayOfDiscoverySearchConfigurationType**</span><span class="sxs-lookup"><span data-stu-id="17acb-105">**ArrayOfDiscoverySearchConfigurationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="17acb-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="17acb-106">Attributes and elements</span></span>

<span data-ttu-id="17acb-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="17acb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="17acb-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="17acb-108">Attributes</span></span>

<span data-ttu-id="17acb-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="17acb-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="17acb-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="17acb-110">Child elements</span></span>

|<span data-ttu-id="17acb-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="17acb-111">**Element**</span></span>|<span data-ttu-id="17acb-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="17acb-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="17acb-113">DiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="17acb-113">DiscoverySearchConfiguration</span></span>](discoverysearchconfiguration.md) <br/> |<span data-ttu-id="17acb-114">Gibt die Konfiguration für die eDiscovery-Suche an.</span><span class="sxs-lookup"><span data-stu-id="17acb-114">Specifies the configuration for eDiscovery search.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="17acb-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="17acb-115">Parent elements</span></span>

|<span data-ttu-id="17acb-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="17acb-116">**Element**</span></span>|<span data-ttu-id="17acb-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="17acb-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="17acb-118">GetDiscoverySearchConfigurationResponseMessage</span><span class="sxs-lookup"><span data-stu-id="17acb-118">GetDiscoverySearchConfigurationResponseMessage</span></span>](getdiscoverysearchconfigurationresponsemessage.md) <br/> |<span data-ttu-id="17acb-119">Gibt die Antwortnachricht für eine **GetDiscoverySearchConfiguration** -Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="17acb-119">Specifies the response message for a **GetDiscoverySearchConfiguration** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="17acb-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="17acb-120">Remarks</span></span>

<span data-ttu-id="17acb-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="17acb-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="17acb-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="17acb-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="17acb-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="17acb-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="17acb-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="17acb-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="17acb-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="17acb-125">Schema Name</span></span>  <br/> |<span data-ttu-id="17acb-126">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="17acb-126">Message schema</span></span>  <br/> |
|<span data-ttu-id="17acb-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="17acb-127">Validation File</span></span>  <br/> |<span data-ttu-id="17acb-128">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="17acb-128">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="17acb-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="17acb-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="17acb-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="17acb-130">See also</span></span>

- [<span data-ttu-id="17acb-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="17acb-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

