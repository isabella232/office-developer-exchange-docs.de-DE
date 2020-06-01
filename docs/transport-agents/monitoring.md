---
title: Überwachung
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- monitoring
api_type:
- schema
ms.assetid: 350d7b46-9260-41a7-8613-3cb8cc1b29a5
description: 'Letzte Änderung: September 17, 2015'
ms.openlocfilehash: 5614ac2c6428da9b6845769a9335486d3ded5754
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455828"
---
# <a name="monitoring"></a><span data-ttu-id="dbf81-103">Überwachung</span><span class="sxs-lookup"><span data-stu-id="dbf81-103">monitoring</span></span>
  
<span data-ttu-id="dbf81-104">**Gilt für:** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="dbf81-104">**Applies to:** Exchange Server 2013</span></span>
  
<span data-ttu-id="dbf81-105">Das **Monitoring** -Element enthält Konfigurationsinformationen, die definieren, wie und wann der Front-End-Transport-Dienst oder der Transportdienst Agents überwacht, die installiert sind.</span><span class="sxs-lookup"><span data-stu-id="dbf81-105">The **monitoring** element contains configuration information that defines how and when the Front End transport service or the Transport service monitors agents that are installed.</span></span> 
  
- [<span data-ttu-id="dbf81-106">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="dbf81-106">configuration</span></span>](configuration.md)  
- [<span data-ttu-id="dbf81-107">mexRuntime</span><span class="sxs-lookup"><span data-stu-id="dbf81-107">mexRuntime</span></span>](mexruntime.md)  
- [<span data-ttu-id="dbf81-108">Überwachung</span><span class="sxs-lookup"><span data-stu-id="dbf81-108">monitoring</span></span>](monitoring.md)
  
```XML
<monitoring>
   <agentExecution/>
   <messageSnapshot/>
</monitoring>
```

<span data-ttu-id="dbf81-109">**monitoringtype (complexType)**</span><span class="sxs-lookup"><span data-stu-id="dbf81-109">**monitoringType (complexType)**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="dbf81-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="dbf81-110">Attributes and elements</span></span>

<span data-ttu-id="dbf81-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="dbf81-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dbf81-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="dbf81-112">Attributes</span></span>

<span data-ttu-id="dbf81-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="dbf81-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dbf81-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dbf81-114">Child elements</span></span>

|<span data-ttu-id="dbf81-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="dbf81-115">**Element**</span></span>|<span data-ttu-id="dbf81-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dbf81-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dbf81-117">agentExecution</span><span class="sxs-lookup"><span data-stu-id="dbf81-117">agentExecution</span></span>](agentexecution.md) <br/> |<span data-ttu-id="dbf81-118">Definiert die Zeit (in Millisekunden) für den Client Zugriff oder den Postfachserver, um zu warten, bis ein Agent von einem Ereignis zurückkehrt, bevor er in das Ereignisprotokoll schreibt.</span><span class="sxs-lookup"><span data-stu-id="dbf81-118">Defines the time, in milliseconds, for the Client Access or the Mailbox server to wait for an agent to return from an event before it writes to the event log.</span></span>  <br/> |
|[<span data-ttu-id="dbf81-119">messageSnapshot</span><span class="sxs-lookup"><span data-stu-id="dbf81-119">messageSnapshot</span></span>](messagesnapshot.md) <br/> |<span data-ttu-id="dbf81-120">Enthält ein Attribut, das angibt, ob das Feature für die Pipelineablaufverfolgung für den Client Zugriffs-oder den Postfachserver aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="dbf81-120">Contains an attribute that specifies whether the pipeline tracing feature is enabled for the Client Access or the Mailbox server.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="dbf81-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dbf81-121">Parent elements</span></span>

|<span data-ttu-id="dbf81-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="dbf81-122">**Element**</span></span>|<span data-ttu-id="dbf81-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dbf81-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dbf81-124">mexRuntime</span><span class="sxs-lookup"><span data-stu-id="dbf81-124">mexRuntime</span></span>](mexruntime.md) <br/> |<span data-ttu-id="dbf81-125">Enthält Elemente, die Konfigurationsinformationen für die Agent-Überwachung und Konfigurationsinformationen für die installierten SMTP-und Routing-Agents definieren.</span><span class="sxs-lookup"><span data-stu-id="dbf81-125">Contains elements that define configuration information for agent monitoring and configuration information for SMTP and routing agents that are installed.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="dbf81-126">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="dbf81-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dbf81-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="dbf81-127">Namespace</span></span>  <br/> |<span data-ttu-id="dbf81-128">In dieser Datei wird kein Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="dbf81-128">This file does not define a namespace.</span></span>  <br/> |
|<span data-ttu-id="dbf81-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="dbf81-129">Schema Name</span></span>  <br/> |<span data-ttu-id="dbf81-130">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="dbf81-130">Not available.</span></span>  <br/> |
|<span data-ttu-id="dbf81-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="dbf81-131">Validation File</span></span>  <br/> |<span data-ttu-id="dbf81-132">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="dbf81-132">Not available.</span></span>  <br/> |
|<span data-ttu-id="dbf81-133">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="dbf81-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="dbf81-134">"False".</span><span class="sxs-lookup"><span data-stu-id="dbf81-134">False.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dbf81-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dbf81-135">See also</span></span>

- [<span data-ttu-id="dbf81-136">Elemente der Konfigurationsdatei der Agents für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="dbf81-136">Agents configuration file elements for Exchange 2013</span></span>](agents-configuration-file-elements-for-exchange-2013.md)

