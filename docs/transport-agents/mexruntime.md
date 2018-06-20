---
title: mexRuntime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- mexRuntime
api_type:
- schema
ms.assetid: eabb2f12-10a7-4ce2-ae4b-9c04010c765f
description: 'Zuletzt geändert: 17 September 2015'
ms.openlocfilehash: 4a34eedfc16d64cbfa67003ed23cf6eba2bb4bad
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757201"
---
# <a name="mexruntime"></a><span data-ttu-id="014b5-103">mexRuntime</span><span class="sxs-lookup"><span data-stu-id="014b5-103">mexRuntime</span></span>
  
<span data-ttu-id="014b5-104">**Gilt für:** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="014b5-104">**Applies to:** Exchange Server 2013</span></span>
  
<span data-ttu-id="014b5-105">Das **MexRuntime** -Element enthält Elemente, die definieren, Konfigurationsinformationen für die Überwachung durch den Agenten und Konfigurationsinformationen für SMTP und routing-Agents, die installiert werden.</span><span class="sxs-lookup"><span data-stu-id="014b5-105">The **mexRuntime** element contains elements that define configuration information for agent monitoring and configuration information for SMTP and routing agents that are installed.</span></span> 
  
- [<span data-ttu-id="014b5-106">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="014b5-106">configuration</span></span>](configuration.md)  
- [<span data-ttu-id="014b5-107">mexRuntime</span><span class="sxs-lookup"><span data-stu-id="014b5-107">mexRuntime</span></span>](mexruntime.md)
  
```XML
<mexRuntime>
   <monitoring/>
   <agentList/>
</mexRuntime>
```

<span data-ttu-id="014b5-108">**MexRuntimeType (ComplexType)**</span><span class="sxs-lookup"><span data-stu-id="014b5-108">**mexRuntimeType (complexType)**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="014b5-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="014b5-109">Attributes and elements</span></span>

<span data-ttu-id="014b5-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="014b5-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="014b5-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="014b5-111">Attributes</span></span>

<span data-ttu-id="014b5-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="014b5-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="014b5-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="014b5-113">Child elements</span></span>

|<span data-ttu-id="014b5-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="014b5-114">**Element**</span></span>|<span data-ttu-id="014b5-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="014b5-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="014b5-116">Überwachung</span><span class="sxs-lookup"><span data-stu-id="014b5-116">monitoring</span></span>](monitoring.md) <br/> |<span data-ttu-id="014b5-117">Enthält Konfigurationsinformationen, die definiert, wie und wann mit Transport Agents überwacht wird, die installiert werden.</span><span class="sxs-lookup"><span data-stu-id="014b5-117">Contains configuration information that defines how and when transport monitors agents that are installed.</span></span>  <br/> |
|[<span data-ttu-id="014b5-118">agentList</span><span class="sxs-lookup"><span data-stu-id="014b5-118">agentList</span></span>](agentlist.md) <br/> |<span data-ttu-id="014b5-119">Enthält ein [Agent](agent.md) -Element für jeden Agent, installiert ist.</span><span class="sxs-lookup"><span data-stu-id="014b5-119">Contains an [agent](agent.md) element for each agent that is installed.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="014b5-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="014b5-120">Parent elements</span></span>

|<span data-ttu-id="014b5-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="014b5-121">**Element**</span></span>|<span data-ttu-id="014b5-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="014b5-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="014b5-123">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="014b5-123">configuration</span></span>](configuration.md) <br/> |<span data-ttu-id="014b5-124">Das Stammelement für die Konfigurationsdatei Agents.</span><span class="sxs-lookup"><span data-stu-id="014b5-124">The root element for the agents configuration file.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="014b5-125">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="014b5-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="014b5-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="014b5-126">Namespace</span></span>  <br/> |<span data-ttu-id="014b5-127">Diese Datei ist nicht auf einen Namespace definieren.</span><span class="sxs-lookup"><span data-stu-id="014b5-127">This file does not define a namespace.</span></span>  <br/> |
|<span data-ttu-id="014b5-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="014b5-128">Schema Name</span></span>  <br/> |<span data-ttu-id="014b5-129">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="014b5-129">Not available.</span></span>  <br/> |
|<span data-ttu-id="014b5-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="014b5-130">Validation File</span></span>  <br/> |<span data-ttu-id="014b5-131">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="014b5-131">Not available.</span></span>  <br/> |
|<span data-ttu-id="014b5-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="014b5-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="014b5-133">Falsch.</span><span class="sxs-lookup"><span data-stu-id="014b5-133">False.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="014b5-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="014b5-134">See also</span></span>

- [<span data-ttu-id="014b5-135">Agents Datei Konfigurationselemente für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="014b5-135">Agents configuration file elements for Exchange 2013</span></span>](agents-configuration-file-elements-for-exchange-2013.md)

