---
title: agentExecution
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- agentExecution
api_type:
- schema
ms.assetid: 600c4690-941c-45af-a906-5528748d09cd
description: 'Letzte Änderung: September 17, 2015'
ms.openlocfilehash: 457257e59fb37659daf2f91b0fa5dfced5c48c03
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44446490"
---
# <a name="agentexecution"></a><span data-ttu-id="b22dc-103">agentExecution</span><span class="sxs-lookup"><span data-stu-id="b22dc-103">agentExecution</span></span>
  
<span data-ttu-id="b22dc-104">**Gilt für:** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="b22dc-104">**Applies to:** Exchange Server 2013</span></span> 
  
<span data-ttu-id="b22dc-105">Das **agentExecution** -Element definiert die Zeit (in Millisekunden), die der Client Zugriffs-oder Postfachserver wartet, bis ein Agent von einem Ereignis zurückkehrt, bevor er in das Ereignisprotokoll schreibt.</span><span class="sxs-lookup"><span data-stu-id="b22dc-105">The **agentExecution** element defines the time, in milliseconds, for the Client Access or Mailbox server to wait for an agent to return from an event before it writes to the event log.</span></span> 
  
- [<span data-ttu-id="b22dc-106">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="b22dc-106">configuration</span></span>](configuration.md)  
- [<span data-ttu-id="b22dc-107">Überwachung</span><span class="sxs-lookup"><span data-stu-id="b22dc-107">monitoring</span></span>](monitoring.md)
- [<span data-ttu-id="b22dc-108">agentExecution</span><span class="sxs-lookup"><span data-stu-id="b22dc-108">agentExecution</span></span>](agentexecution.md)
  
```XML
<agentExecution timeLimitInMilliseconds="" />
```

<span data-ttu-id="b22dc-109">**agentExecutionType (complexType)**</span><span class="sxs-lookup"><span data-stu-id="b22dc-109">**agentExecutionType (complexType)**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="b22dc-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b22dc-110">Attributes and elements</span></span>

<span data-ttu-id="b22dc-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b22dc-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b22dc-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="b22dc-112">Attributes</span></span>

|<span data-ttu-id="b22dc-113">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="b22dc-113">**Attribute**</span></span>|<span data-ttu-id="b22dc-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b22dc-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b22dc-115">**timeLimitInMilliseconds**</span><span class="sxs-lookup"><span data-stu-id="b22dc-115">**timeLimitInMilliseconds**</span></span> <br/> |<span data-ttu-id="b22dc-116">Ein positiver ganzzahliger Wert, der die Zeit in Millisekunden angibt, die der Server wartet, bis ein Agent von einem Ereignis zurückgegeben wird, bevor er eine Warnung in das Ereignisprotokoll schreibt.</span><span class="sxs-lookup"><span data-stu-id="b22dc-116">A positive integer value that specifies the time, in milliseconds, for the server to wait for an agent to return from an event before it writes a warning to the event log.</span></span> <span data-ttu-id="b22dc-117">Die Leistung kann sinken, wenn dieser Wert zu klein ist.</span><span class="sxs-lookup"><span data-stu-id="b22dc-117">Performance can decrease if this value is too small.</span></span> <span data-ttu-id="b22dc-118">Der vorgeschlagene Wert für dieses Attribut ist 300.000, was 5 Minuten entspricht.</span><span class="sxs-lookup"><span data-stu-id="b22dc-118">The suggested value for this attribute is 300,000, which equates to 5 minutes.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b22dc-119">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b22dc-119">Child elements</span></span>

<span data-ttu-id="b22dc-120">Keine.</span><span class="sxs-lookup"><span data-stu-id="b22dc-120">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b22dc-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b22dc-121">Parent elements</span></span>

|<span data-ttu-id="b22dc-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="b22dc-122">**Element**</span></span>|<span data-ttu-id="b22dc-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b22dc-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b22dc-124">Überwachung</span><span class="sxs-lookup"><span data-stu-id="b22dc-124">monitoring</span></span>](monitoring.md) <br/> |<span data-ttu-id="b22dc-125">Enthält Konfigurationsinformationen, die definieren, wie und wann der Front-End-Transport-Dienst oder der Transportdienst Agents überwacht, die installiert sind.</span><span class="sxs-lookup"><span data-stu-id="b22dc-125">Contains configuration information that defines how and when the Front End Transport service or the Transport service monitors agents that are installed.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="b22dc-126">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="b22dc-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b22dc-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="b22dc-127">Namespace</span></span>  <br/> |<span data-ttu-id="b22dc-128">In dieser Datei wird kein Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="b22dc-128">This file does not define a namespace.</span></span>  <br/> |
|<span data-ttu-id="b22dc-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b22dc-129">Schema Name</span></span>  <br/> |<span data-ttu-id="b22dc-130">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b22dc-130">Not available.</span></span>  <br/> |
|<span data-ttu-id="b22dc-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b22dc-131">Validation File</span></span>  <br/> |<span data-ttu-id="b22dc-132">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b22dc-132">Not available.</span></span>  <br/> |
|<span data-ttu-id="b22dc-133">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="b22dc-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="b22dc-134">"False".</span><span class="sxs-lookup"><span data-stu-id="b22dc-134">False.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b22dc-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b22dc-135">See also</span></span>

- [<span data-ttu-id="b22dc-136">Elemente der Konfigurationsdatei der Agents für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="b22dc-136">Agents configuration file elements for Exchange 2013</span></span>](agents-configuration-file-elements-for-exchange-2013.md)

