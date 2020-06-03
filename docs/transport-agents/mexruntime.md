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
description: 'Letzte Änderung: September 17, 2015'
ms.openlocfilehash: f192965a8375eb46d1ca5b46d3b768a3299c284d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461835"
---
# <a name="mexruntime"></a><span data-ttu-id="100de-103">mexRuntime</span><span class="sxs-lookup"><span data-stu-id="100de-103">mexRuntime</span></span>
  
<span data-ttu-id="100de-104">**Gilt für:** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="100de-104">**Applies to:** Exchange Server 2013</span></span>
  
<span data-ttu-id="100de-105">Das **mexRuntime** -Element enthält Elemente, die Konfigurationsinformationen für die Agent-Überwachung und Konfigurationsinformationen für die installierten SMTP-und Routing-Agents definieren.</span><span class="sxs-lookup"><span data-stu-id="100de-105">The **mexRuntime** element contains elements that define configuration information for agent monitoring and configuration information for SMTP and routing agents that are installed.</span></span> 
  
- [<span data-ttu-id="100de-106">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="100de-106">configuration</span></span>](configuration.md)  
- [<span data-ttu-id="100de-107">mexRuntime</span><span class="sxs-lookup"><span data-stu-id="100de-107">mexRuntime</span></span>](mexruntime.md)
  
```XML
<mexRuntime>
   <monitoring/>
   <agentList/>
</mexRuntime>
```

<span data-ttu-id="100de-108">**mexRuntimeType (complexType)**</span><span class="sxs-lookup"><span data-stu-id="100de-108">**mexRuntimeType (complexType)**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="100de-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="100de-109">Attributes and elements</span></span>

<span data-ttu-id="100de-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="100de-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="100de-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="100de-111">Attributes</span></span>

<span data-ttu-id="100de-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="100de-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="100de-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="100de-113">Child elements</span></span>

|<span data-ttu-id="100de-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="100de-114">**Element**</span></span>|<span data-ttu-id="100de-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="100de-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="100de-116">Überwachung</span><span class="sxs-lookup"><span data-stu-id="100de-116">monitoring</span></span>](monitoring.md) <br/> |<span data-ttu-id="100de-117">Enthält Konfigurationsinformationen, die definieren, wie und wann der Transport Agents überwacht, die installiert werden.</span><span class="sxs-lookup"><span data-stu-id="100de-117">Contains configuration information that defines how and when transport monitors agents that are installed.</span></span>  <br/> |
|[<span data-ttu-id="100de-118">Agentliste</span><span class="sxs-lookup"><span data-stu-id="100de-118">agentList</span></span>](agentlist.md) <br/> |<span data-ttu-id="100de-119">Enthält ein [Agent](agent.md) -Element für jeden Agent, der installiert ist.</span><span class="sxs-lookup"><span data-stu-id="100de-119">Contains an [agent](agent.md) element for each agent that is installed.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="100de-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="100de-120">Parent elements</span></span>

|<span data-ttu-id="100de-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="100de-121">**Element**</span></span>|<span data-ttu-id="100de-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="100de-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="100de-123">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="100de-123">configuration</span></span>](configuration.md) <br/> |<span data-ttu-id="100de-124">Das Stammelement für die Konfigurationsdatei der Agents.</span><span class="sxs-lookup"><span data-stu-id="100de-124">The root element for the agents configuration file.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="100de-125">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="100de-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="100de-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="100de-126">Namespace</span></span>  <br/> |<span data-ttu-id="100de-127">In dieser Datei wird kein Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="100de-127">This file does not define a namespace.</span></span>  <br/> |
|<span data-ttu-id="100de-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="100de-128">Schema Name</span></span>  <br/> |<span data-ttu-id="100de-129">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="100de-129">Not available.</span></span>  <br/> |
|<span data-ttu-id="100de-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="100de-130">Validation File</span></span>  <br/> |<span data-ttu-id="100de-131">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="100de-131">Not available.</span></span>  <br/> |
|<span data-ttu-id="100de-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="100de-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="100de-133">"False".</span><span class="sxs-lookup"><span data-stu-id="100de-133">False.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="100de-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="100de-134">See also</span></span>

- [<span data-ttu-id="100de-135">Elemente der Konfigurationsdatei der Agents für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="100de-135">Agents configuration file elements for Exchange 2013</span></span>](agents-configuration-file-elements-for-exchange-2013.md)

