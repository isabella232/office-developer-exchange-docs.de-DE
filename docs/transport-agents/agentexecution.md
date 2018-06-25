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
description: 'Zuletzt geändert: 17 September 2015'
ms.openlocfilehash: 5848d52a68c8c3f747614015e49becb34bc4cfd8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757167"
---
# <a name="agentexecution"></a><span data-ttu-id="9cc3c-103">agentExecution</span><span class="sxs-lookup"><span data-stu-id="9cc3c-103">agentExecution</span></span>
  
<span data-ttu-id="9cc3c-104">**Gilt für:** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="9cc3c-104">**Applies to:** Exchange Server 2013</span></span> 
  
<span data-ttu-id="9cc3c-105">Das **AgentExecution** -Element definiert die Zeit in Millisekunden an, für den Clientzugriff "oder" Postfach-Server zu warten, bis ein Agent zurückgeben, ein Ereignis, bevor in das Ereignisprotokoll geschrieben.</span><span class="sxs-lookup"><span data-stu-id="9cc3c-105">The **agentExecution** element defines the time, in milliseconds, for the Client Access or Mailbox server to wait for an agent to return from an event before it writes to the event log.</span></span> 
  
- [<span data-ttu-id="9cc3c-106">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="9cc3c-106">configuration</span></span>](configuration.md)  
- [<span data-ttu-id="9cc3c-107">Überwachung</span><span class="sxs-lookup"><span data-stu-id="9cc3c-107">monitoring</span></span>](monitoring.md)
- [<span data-ttu-id="9cc3c-108">agentExecution</span><span class="sxs-lookup"><span data-stu-id="9cc3c-108">agentExecution</span></span>](agentexecution.md)
  
```XML
<agentExecution timeLimitInMilliseconds="" />
```

<span data-ttu-id="9cc3c-109">**AgentExecutionType (ComplexType)**</span><span class="sxs-lookup"><span data-stu-id="9cc3c-109">**agentExecutionType (complexType)**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="9cc3c-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="9cc3c-110">Attributes and elements</span></span>

<span data-ttu-id="9cc3c-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="9cc3c-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9cc3c-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="9cc3c-112">Attributes</span></span>

|<span data-ttu-id="9cc3c-113">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="9cc3c-113">**Attribute**</span></span>|<span data-ttu-id="9cc3c-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9cc3c-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9cc3c-115">**timeLimitInMilliseconds**</span><span class="sxs-lookup"><span data-stu-id="9cc3c-115">**timeLimitInMilliseconds**</span></span> <br/> |<span data-ttu-id="9cc3c-116">Eine positive ganze Zahl, die gibt die Zeit in Millisekunden an, für den Server zu warten, bis ein Agent zurückgeben, ein Ereignis, bevor eine Warnung in das Ereignisprotokoll geschrieben.</span><span class="sxs-lookup"><span data-stu-id="9cc3c-116">A positive integer value that specifies the time, in milliseconds, for the server to wait for an agent to return from an event before it writes a warning to the event log.</span></span> <span data-ttu-id="9cc3c-117">Wenn dieser Wert zu klein ist, kann die Leistung verringern.</span><span class="sxs-lookup"><span data-stu-id="9cc3c-117">Performance can decrease if this value is too small.</span></span> <span data-ttu-id="9cc3c-118">Der vorgeschlagene Wert für dieses Attribut ist 300.000, die auf 5 Minuten entspricht.</span><span class="sxs-lookup"><span data-stu-id="9cc3c-118">The suggested value for this attribute is 300,000, which equates to 5 minutes.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9cc3c-119">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9cc3c-119">Child elements</span></span>

<span data-ttu-id="9cc3c-120">Keine.</span><span class="sxs-lookup"><span data-stu-id="9cc3c-120">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9cc3c-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9cc3c-121">Parent elements</span></span>

|<span data-ttu-id="9cc3c-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="9cc3c-122">**Element**</span></span>|<span data-ttu-id="9cc3c-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9cc3c-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9cc3c-124">Überwachung</span><span class="sxs-lookup"><span data-stu-id="9cc3c-124">monitoring</span></span>](monitoring.md) <br/> |<span data-ttu-id="9cc3c-125">Enthält Konfigurationsinformationen, die definiert, wann und wie der Front-End-Transport-Dienst oder den Transportdienst Agents überwacht, die installiert werden.</span><span class="sxs-lookup"><span data-stu-id="9cc3c-125">Contains configuration information that defines how and when the Front End Transport service or the Transport service monitors agents that are installed.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="9cc3c-126">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="9cc3c-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9cc3c-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="9cc3c-127">Namespace</span></span>  <br/> |<span data-ttu-id="9cc3c-128">Diese Datei ist nicht auf einen Namespace definieren.</span><span class="sxs-lookup"><span data-stu-id="9cc3c-128">This file does not define a namespace.</span></span>  <br/> |
|<span data-ttu-id="9cc3c-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="9cc3c-129">Schema Name</span></span>  <br/> |<span data-ttu-id="9cc3c-130">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9cc3c-130">Not available.</span></span>  <br/> |
|<span data-ttu-id="9cc3c-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="9cc3c-131">Validation File</span></span>  <br/> |<span data-ttu-id="9cc3c-132">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9cc3c-132">Not available.</span></span>  <br/> |
|<span data-ttu-id="9cc3c-133">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="9cc3c-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="9cc3c-134">Falsch.</span><span class="sxs-lookup"><span data-stu-id="9cc3c-134">False.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9cc3c-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9cc3c-135">See also</span></span>

- [<span data-ttu-id="9cc3c-136">Agents Datei Konfigurationselemente für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="9cc3c-136">Agents configuration file elements for Exchange 2013</span></span>](agents-configuration-file-elements-for-exchange-2013.md)

