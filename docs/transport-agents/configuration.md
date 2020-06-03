---
title: Konfiguration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- configuration
api_type:
- schema
ms.assetid: 6fc04e4d-657a-4999-9431-186ccb7832b5
description: 'Letzte Änderung: September 17, 2015'
ms.openlocfilehash: b886851b9a0c17d58428f49281d664930d0e4070
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461562"
---
# <a name="configuration"></a><span data-ttu-id="04fb5-103">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="04fb5-103">configuration</span></span>
  
<span data-ttu-id="04fb5-104">**Gilt für:** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="04fb5-104">**Applies to:** Exchange Server 2013</span></span>
  
<span data-ttu-id="04fb5-105">Das **Configuration** -Element ist das Stammelement für die Konfigurationsdatei der Agents.</span><span class="sxs-lookup"><span data-stu-id="04fb5-105">The **configuration** element is the root element for the agents configuration file.</span></span> 
  
- [<span data-ttu-id="04fb5-106">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="04fb5-106">configuration</span></span>](configuration.md) 
- [<span data-ttu-id="04fb5-107">mexRuntime</span><span class="sxs-lookup"><span data-stu-id="04fb5-107">mexRuntime</span></span>](mexruntime.md)
  
```XML
<configuration>
      <mexRuntime/>
</configuration>
```

<span data-ttu-id="04fb5-108">**ConfigurationType (complexType)**</span><span class="sxs-lookup"><span data-stu-id="04fb5-108">**configurationType (complexType)**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="04fb5-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="04fb5-109">Attributes and elements</span></span>

<span data-ttu-id="04fb5-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="04fb5-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="04fb5-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="04fb5-111">Attributes</span></span>

<span data-ttu-id="04fb5-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="04fb5-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="04fb5-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="04fb5-113">Child elements</span></span>

|<span data-ttu-id="04fb5-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="04fb5-114">**Element**</span></span>|<span data-ttu-id="04fb5-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="04fb5-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="04fb5-116">mexRuntime</span><span class="sxs-lookup"><span data-stu-id="04fb5-116">mexRuntime</span></span>](mexruntime.md) <br/> |<span data-ttu-id="04fb5-117">Enthält Elemente, die Konfigurationsinformationen für die Agent-Überwachung und Konfigurationsinformationen für die installierten SMTP-und Routing-Agents definieren.</span><span class="sxs-lookup"><span data-stu-id="04fb5-117">Contains elements that define configuration information for agent monitoring and configuration information for SMTP and routing agents that are installed.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="04fb5-118">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="04fb5-118">Parent elements</span></span>

<span data-ttu-id="04fb5-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="04fb5-119">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="04fb5-120">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="04fb5-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="04fb5-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="04fb5-121">Namespace</span></span>  <br/> |<span data-ttu-id="04fb5-122">In dieser Datei wird kein Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="04fb5-122">This file does not define a namespace.</span></span>  <br/> |
|<span data-ttu-id="04fb5-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="04fb5-123">Schema Name</span></span>  <br/> |<span data-ttu-id="04fb5-124">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="04fb5-124">Not available.</span></span>  <br/> |
|<span data-ttu-id="04fb5-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="04fb5-125">Validation File</span></span>  <br/> |<span data-ttu-id="04fb5-126">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="04fb5-126">Not available.</span></span>  <br/> |
|<span data-ttu-id="04fb5-127">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="04fb5-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="04fb5-128">"False".</span><span class="sxs-lookup"><span data-stu-id="04fb5-128">False.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="04fb5-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="04fb5-129">See also</span></span>

- [<span data-ttu-id="04fb5-130">Elemente der Konfigurationsdatei der Agents für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="04fb5-130">Agents configuration file elements for Exchange 2013</span></span>](agents-configuration-file-elements-for-exchange-2013.md)

