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
description: 'Zuletzt geändert: 17 September 2015'
ms.openlocfilehash: 1b5484467def0bf3d22ba0707357977d5ed461ff
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757197"
---
# <a name="monitoring"></a><span data-ttu-id="2b93f-103">Überwachung</span><span class="sxs-lookup"><span data-stu-id="2b93f-103">monitoring</span></span>
  
<span data-ttu-id="2b93f-104">**Gilt für:** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="2b93f-104">**Applies to:** Exchange Server 2013</span></span>
  
<span data-ttu-id="2b93f-105">Das **monitoring** -Element enthält Konfigurationsinformationen, die definiert, wie und wann die Front-End-Transport-Dienst oder den Transportdienst Agents überwacht, die installiert werden.</span><span class="sxs-lookup"><span data-stu-id="2b93f-105">The **monitoring** element contains configuration information that defines how and when the Front End transport service or the Transport service monitors agents that are installed.</span></span> 
  
- [<span data-ttu-id="2b93f-106">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="2b93f-106">configuration</span></span>](configuration.md)  
- [<span data-ttu-id="2b93f-107">mexRuntime</span><span class="sxs-lookup"><span data-stu-id="2b93f-107">mexRuntime</span></span>](mexruntime.md)  
- [<span data-ttu-id="2b93f-108">Überwachung</span><span class="sxs-lookup"><span data-stu-id="2b93f-108">monitoring</span></span>](monitoring.md)
  
```XML
<monitoring>
   <agentExecution/>
   <messageSnapshot/>
</monitoring>
```

<span data-ttu-id="2b93f-109">**MonitoringType (ComplexType)**</span><span class="sxs-lookup"><span data-stu-id="2b93f-109">**monitoringType (complexType)**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="2b93f-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="2b93f-110">Attributes and elements</span></span>

<span data-ttu-id="2b93f-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="2b93f-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2b93f-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="2b93f-112">Attributes</span></span>

<span data-ttu-id="2b93f-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="2b93f-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2b93f-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2b93f-114">Child elements</span></span>

|<span data-ttu-id="2b93f-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="2b93f-115">**Element**</span></span>|<span data-ttu-id="2b93f-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2b93f-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2b93f-117">agentExecution</span><span class="sxs-lookup"><span data-stu-id="2b93f-117">agentExecution</span></span>](agentexecution.md) <br/> |<span data-ttu-id="2b93f-118">Definiert die Zeit in Millisekunden an, für den Clientzugriff oder dem Postfachserver zu warten, bis ein Agent zurückgeben, ein Ereignis, bevor in das Ereignisprotokoll geschrieben.</span><span class="sxs-lookup"><span data-stu-id="2b93f-118">Defines the time, in milliseconds, for the Client Access or the Mailbox server to wait for an agent to return from an event before it writes to the event log.</span></span>  <br/> |
|[<span data-ttu-id="2b93f-119">messageSnapshot</span><span class="sxs-lookup"><span data-stu-id="2b93f-119">messageSnapshot</span></span>](messagesnapshot.md) <br/> |<span data-ttu-id="2b93f-120">Enthält ein Attribut, das angibt, ob das Pipeline Tracing-Feature für den Clientzugriff oder dem Postfachserver aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="2b93f-120">Contains an attribute that specifies whether the pipeline tracing feature is enabled for the Client Access or the Mailbox server.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2b93f-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2b93f-121">Parent elements</span></span>

|<span data-ttu-id="2b93f-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="2b93f-122">**Element**</span></span>|<span data-ttu-id="2b93f-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2b93f-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2b93f-124">mexRuntime</span><span class="sxs-lookup"><span data-stu-id="2b93f-124">mexRuntime</span></span>](mexruntime.md) <br/> |<span data-ttu-id="2b93f-125">Enthält Elemente, die definieren, Konfigurationsinformationen für die Überwachung durch den Agenten und Konfigurationsinformationen für SMTP und routing-Agents, die installiert werden.</span><span class="sxs-lookup"><span data-stu-id="2b93f-125">Contains elements that define configuration information for agent monitoring and configuration information for SMTP and routing agents that are installed.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="2b93f-126">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="2b93f-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2b93f-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="2b93f-127">Namespace</span></span>  <br/> |<span data-ttu-id="2b93f-128">Diese Datei ist nicht auf einen Namespace definieren.</span><span class="sxs-lookup"><span data-stu-id="2b93f-128">This file does not define a namespace.</span></span>  <br/> |
|<span data-ttu-id="2b93f-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="2b93f-129">Schema Name</span></span>  <br/> |<span data-ttu-id="2b93f-130">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2b93f-130">Not available.</span></span>  <br/> |
|<span data-ttu-id="2b93f-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="2b93f-131">Validation File</span></span>  <br/> |<span data-ttu-id="2b93f-132">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2b93f-132">Not available.</span></span>  <br/> |
|<span data-ttu-id="2b93f-133">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="2b93f-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="2b93f-134">Falsch.</span><span class="sxs-lookup"><span data-stu-id="2b93f-134">False.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2b93f-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2b93f-135">See also</span></span>

- [<span data-ttu-id="2b93f-136">Agents Datei Konfigurationselemente für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="2b93f-136">Agents configuration file elements for Exchange 2013</span></span>](agents-configuration-file-elements-for-exchange-2013.md)

