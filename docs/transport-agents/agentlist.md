---
title: agentList
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- agentList
api_type:
- schema
ms.assetid: e877b7ef-e303-4270-964d-8d116ff2a865
description: 'Zuletzt geändert: 17 September 2015'
ms.openlocfilehash: 7dd9d48356932c82dbc048a85b9f02437c6366de
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757169"
---
# <a name="agentlist"></a><span data-ttu-id="a9fdf-103">agentList</span><span class="sxs-lookup"><span data-stu-id="a9fdf-103">agentList</span></span>
  
<span data-ttu-id="a9fdf-104">**Gilt für:** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="a9fdf-104">**Applies to:** Exchange Server 2013</span></span>
  
<span data-ttu-id="a9fdf-105">Das **AgentList** -Element enthält ein [Agent](agent.md) -Element für jeden installierten Agent.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-105">The **agentList** element contains an [agent](agent.md) element for each installed agent.</span></span> 
  
- [<span data-ttu-id="a9fdf-106">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="a9fdf-106">configuration</span></span>](configuration.md)
- [<span data-ttu-id="a9fdf-107">mexRuntime</span><span class="sxs-lookup"><span data-stu-id="a9fdf-107">mexRuntime</span></span>](mexruntime.md)
- [<span data-ttu-id="a9fdf-108">agentList</span><span class="sxs-lookup"><span data-stu-id="a9fdf-108">agentList</span></span>](agentlist.md)
  
```XML
<agentList>
      <agent/>
</agentList>
```

<span data-ttu-id="a9fdf-109">**AgentListType (ComplexType)**</span><span class="sxs-lookup"><span data-stu-id="a9fdf-109">**agentListType (complexType)**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="a9fdf-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a9fdf-110">Attributes and elements</span></span>

<span data-ttu-id="a9fdf-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a9fdf-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="a9fdf-112">Attributes</span></span>

<span data-ttu-id="a9fdf-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a9fdf-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a9fdf-114">Child elements</span></span>

|<span data-ttu-id="a9fdf-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="a9fdf-115">**Element**</span></span>|<span data-ttu-id="a9fdf-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a9fdf-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a9fdf-117">Agent</span><span class="sxs-lookup"><span data-stu-id="a9fdf-117">agent</span></span>](agent.md) <br/> |<span data-ttu-id="a9fdf-118">Enthält Informationen zur installierten Agenten Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-118">Contains configuration information about an installed agent.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a9fdf-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a9fdf-119">Parent elements</span></span>

|<span data-ttu-id="a9fdf-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="a9fdf-120">**Element**</span></span>|<span data-ttu-id="a9fdf-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a9fdf-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a9fdf-122">mexRuntime</span><span class="sxs-lookup"><span data-stu-id="a9fdf-122">mexRuntime</span></span>](mexruntime.md) <br/> |<span data-ttu-id="a9fdf-123">Enthält Elemente, die Konfigurationsinformationen für die Überwachung durch den Agenten und Konfigurationsinformationen zu installierten Agents definieren.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-123">Contains elements that define configuration information for agent monitoring and configuration information about installed agents.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="a9fdf-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="a9fdf-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a9fdf-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="a9fdf-125">Namespace</span></span>  <br/> |<span data-ttu-id="a9fdf-126">Diese Datei ist nicht auf einen Namespace definieren.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-126">This file does not define a namespace.</span></span>  <br/> |
|<span data-ttu-id="a9fdf-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a9fdf-127">Schema Name</span></span>  <br/> |<span data-ttu-id="a9fdf-128">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-128">Not available.</span></span>  <br/> |
|<span data-ttu-id="a9fdf-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a9fdf-129">Validation File</span></span>  <br/> |<span data-ttu-id="a9fdf-130">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-130">Not available.</span></span>  <br/> |
|<span data-ttu-id="a9fdf-131">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="a9fdf-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="a9fdf-132">Falsch.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-132">False.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a9fdf-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a9fdf-133">See also</span></span>

- [<span data-ttu-id="a9fdf-134">Agents Datei Konfigurationselemente für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="a9fdf-134">Agents configuration file elements for Exchange 2013</span></span>](agents-configuration-file-elements-for-exchange-2013.md)

