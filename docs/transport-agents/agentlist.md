---
title: Agentliste
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
description: 'Letzte Änderung: September 17, 2015'
ms.openlocfilehash: 99e4e24c3bca77c7e7d5f2c59bb21cee1317fed2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44446392"
---
# <a name="agentlist"></a><span data-ttu-id="abc04-103">Agentliste</span><span class="sxs-lookup"><span data-stu-id="abc04-103">agentList</span></span>
  
<span data-ttu-id="abc04-104">**Gilt für:** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="abc04-104">**Applies to:** Exchange Server 2013</span></span>
  
<span data-ttu-id="abc04-105">Das **agentlist** -Element enthält ein [Agent](agent.md) -Element für jeden installierten Agent.</span><span class="sxs-lookup"><span data-stu-id="abc04-105">The **agentList** element contains an [agent](agent.md) element for each installed agent.</span></span> 
  
- [<span data-ttu-id="abc04-106">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="abc04-106">configuration</span></span>](configuration.md)
- [<span data-ttu-id="abc04-107">mexRuntime</span><span class="sxs-lookup"><span data-stu-id="abc04-107">mexRuntime</span></span>](mexruntime.md)
- [<span data-ttu-id="abc04-108">Agentliste</span><span class="sxs-lookup"><span data-stu-id="abc04-108">agentList</span></span>](agentlist.md)
  
```XML
<agentList>
      <agent/>
</agentList>
```

<span data-ttu-id="abc04-109">**agentListType (complexType)**</span><span class="sxs-lookup"><span data-stu-id="abc04-109">**agentListType (complexType)**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="abc04-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="abc04-110">Attributes and elements</span></span>

<span data-ttu-id="abc04-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="abc04-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="abc04-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="abc04-112">Attributes</span></span>

<span data-ttu-id="abc04-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="abc04-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="abc04-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="abc04-114">Child elements</span></span>

|<span data-ttu-id="abc04-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="abc04-115">**Element**</span></span>|<span data-ttu-id="abc04-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="abc04-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="abc04-117">Agent</span><span class="sxs-lookup"><span data-stu-id="abc04-117">agent</span></span>](agent.md) <br/> |<span data-ttu-id="abc04-118">Enthält Konfigurationsinformationen zu einem installierten Agent.</span><span class="sxs-lookup"><span data-stu-id="abc04-118">Contains configuration information about an installed agent.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="abc04-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="abc04-119">Parent elements</span></span>

|<span data-ttu-id="abc04-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="abc04-120">**Element**</span></span>|<span data-ttu-id="abc04-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="abc04-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="abc04-122">mexRuntime</span><span class="sxs-lookup"><span data-stu-id="abc04-122">mexRuntime</span></span>](mexruntime.md) <br/> |<span data-ttu-id="abc04-123">Enthält Elemente, die Konfigurationsinformationen für die Agent-Überwachung und Konfigurationsinformationen zu installierten Agents definieren.</span><span class="sxs-lookup"><span data-stu-id="abc04-123">Contains elements that define configuration information for agent monitoring and configuration information about installed agents.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="abc04-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="abc04-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="abc04-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="abc04-125">Namespace</span></span>  <br/> |<span data-ttu-id="abc04-126">In dieser Datei wird kein Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="abc04-126">This file does not define a namespace.</span></span>  <br/> |
|<span data-ttu-id="abc04-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="abc04-127">Schema Name</span></span>  <br/> |<span data-ttu-id="abc04-128">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="abc04-128">Not available.</span></span>  <br/> |
|<span data-ttu-id="abc04-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="abc04-129">Validation File</span></span>  <br/> |<span data-ttu-id="abc04-130">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="abc04-130">Not available.</span></span>  <br/> |
|<span data-ttu-id="abc04-131">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="abc04-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="abc04-132">"False".</span><span class="sxs-lookup"><span data-stu-id="abc04-132">False.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="abc04-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="abc04-133">See also</span></span>

- [<span data-ttu-id="abc04-134">Elemente der Konfigurationsdatei der Agents für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="abc04-134">Agents configuration file elements for Exchange 2013</span></span>](agents-configuration-file-elements-for-exchange-2013.md)

