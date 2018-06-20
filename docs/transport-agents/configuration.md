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
description: 'Zuletzt geändert: 17 September 2015'
ms.openlocfilehash: 342e52e879534b6a130d286d358138c6095e4563
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757171"
---
# <a name="configuration"></a><span data-ttu-id="1b893-103">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="1b893-103">configuration</span></span>
  
<span data-ttu-id="1b893-104">**Gilt für:** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="1b893-104">**Applies to:** Exchange Server 2013</span></span>
  
<span data-ttu-id="1b893-105">**Configuration** -Elements ist das Stammelement für die Konfigurationsdatei Agents.</span><span class="sxs-lookup"><span data-stu-id="1b893-105">The **configuration** element is the root element for the agents configuration file.</span></span> 
  
- [<span data-ttu-id="1b893-106">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="1b893-106">configuration</span></span>](configuration.md) 
- [<span data-ttu-id="1b893-107">mexRuntime</span><span class="sxs-lookup"><span data-stu-id="1b893-107">mexRuntime</span></span>](mexruntime.md)
  
```XML
<configuration>
      <mexRuntime/>
</configuration>
```

<span data-ttu-id="1b893-108">**ConfigurationType (ComplexType)**</span><span class="sxs-lookup"><span data-stu-id="1b893-108">**configurationType (complexType)**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="1b893-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1b893-109">Attributes and elements</span></span>

<span data-ttu-id="1b893-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1b893-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1b893-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="1b893-111">Attributes</span></span>

<span data-ttu-id="1b893-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="1b893-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1b893-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1b893-113">Child elements</span></span>

|<span data-ttu-id="1b893-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="1b893-114">**Element**</span></span>|<span data-ttu-id="1b893-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1b893-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1b893-116">mexRuntime</span><span class="sxs-lookup"><span data-stu-id="1b893-116">mexRuntime</span></span>](mexruntime.md) <br/> |<span data-ttu-id="1b893-117">Enthält Elemente, die definieren, Konfigurationsinformationen für die Überwachung durch den Agenten und Konfigurationsinformationen für SMTP und routing-Agents, die installiert werden.</span><span class="sxs-lookup"><span data-stu-id="1b893-117">Contains elements that define configuration information for agent monitoring and configuration information for SMTP and routing agents that are installed.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1b893-118">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1b893-118">Parent elements</span></span>

<span data-ttu-id="1b893-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="1b893-119">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1b893-120">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="1b893-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1b893-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="1b893-121">Namespace</span></span>  <br/> |<span data-ttu-id="1b893-122">Diese Datei ist nicht auf einen Namespace definieren.</span><span class="sxs-lookup"><span data-stu-id="1b893-122">This file does not define a namespace.</span></span>  <br/> |
|<span data-ttu-id="1b893-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="1b893-123">Schema Name</span></span>  <br/> |<span data-ttu-id="1b893-124">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1b893-124">Not available.</span></span>  <br/> |
|<span data-ttu-id="1b893-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="1b893-125">Validation File</span></span>  <br/> |<span data-ttu-id="1b893-126">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1b893-126">Not available.</span></span>  <br/> |
|<span data-ttu-id="1b893-127">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="1b893-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="1b893-128">Falsch.</span><span class="sxs-lookup"><span data-stu-id="1b893-128">False.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1b893-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1b893-129">See also</span></span>

- [<span data-ttu-id="1b893-130">Agents Datei Konfigurationselemente für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="1b893-130">Agents configuration file elements for Exchange 2013</span></span>](agents-configuration-file-elements-for-exchange-2013.md)

