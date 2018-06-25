---
title: messageSnapshot
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- messageSnapshot
api_type:
- schema
ms.assetid: f157e44c-b950-463f-b086-31d5da94b7ff
description: 'Zuletzt geändert: 17 September 2015'
ms.openlocfilehash: 4b814def8eef8fb452d2e754c5f6787d644055f7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757198"
---
# <a name="messagesnapshot"></a><span data-ttu-id="2493e-103">messageSnapshot</span><span class="sxs-lookup"><span data-stu-id="2493e-103">messageSnapshot</span></span>

<span data-ttu-id="2493e-104">**Gilt für:** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="2493e-104">**Applies to:** Exchange Server 2013</span></span>
  
<span data-ttu-id="2493e-105">Das **MessageSnapshot** -Element enthält ein Attribut, das angibt, ob das Pipeline Tracing-Feature für den Exchange-Server aktiviert ist, die Access-Client oder die Serverrolle Mailbox installiert hat.</span><span class="sxs-lookup"><span data-stu-id="2493e-105">The **messageSnapshot** element contains an attribute that specifies whether the pipeline tracing feature is enabled for the Exchange server that has the Client Access or the Mailbox server role installed.</span></span> 
  
- [<span data-ttu-id="2493e-106">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="2493e-106">configuration</span></span>](configuration.md)  
- [<span data-ttu-id="2493e-107">mexRuntime</span><span class="sxs-lookup"><span data-stu-id="2493e-107">mexRuntime</span></span>](mexruntime.md) 
- [<span data-ttu-id="2493e-108">Überwachung</span><span class="sxs-lookup"><span data-stu-id="2493e-108">monitoring</span></span>](monitoring.md) 
- [<span data-ttu-id="2493e-109">messageSnapshot</span><span class="sxs-lookup"><span data-stu-id="2493e-109">messageSnapshot</span></span>](messagesnapshot.md)
  
```XML
<messageSnapshot enabled="" />
```

<span data-ttu-id="2493e-110">**MessageSnapshotType (boolesch)**</span><span class="sxs-lookup"><span data-stu-id="2493e-110">**messageSnapshotType (Boolean)**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="2493e-111">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="2493e-111">Attributes and elements</span></span>

<span data-ttu-id="2493e-112">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="2493e-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2493e-113">Attribute</span><span class="sxs-lookup"><span data-stu-id="2493e-113">Attributes</span></span>

|<span data-ttu-id="2493e-114">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="2493e-114">**Attribute**</span></span>|<span data-ttu-id="2493e-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2493e-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2493e-116">**aktiviert**</span><span class="sxs-lookup"><span data-stu-id="2493e-116">**enabled**</span></span> <br/> |<span data-ttu-id="2493e-117">Ein boolescher Wert, der angibt, ob das Pipeline Tracing-Feature für den Clientzugriff oder dem Postfachserver aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="2493e-117">A Boolean value that indicates whether the pipeline tracing feature is enabled for the Client Access or the Mailbox server.</span></span> <span data-ttu-id="2493e-118">Der Wert ist **true** , wenn die pipelineablaufverfolgung aktiviert ist. Andernfalls ist des Werts **false** oder das Element ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="2493e-118">The value is **true** if pipeline tracing is enabled; otherwise, the value is **false** or the element is not present.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="2493e-119">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2493e-119">Child elements</span></span>

<span data-ttu-id="2493e-120">Keine.</span><span class="sxs-lookup"><span data-stu-id="2493e-120">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2493e-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2493e-121">Parent elements</span></span>

|<span data-ttu-id="2493e-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="2493e-122">**Element**</span></span>|<span data-ttu-id="2493e-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2493e-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2493e-124">Überwachung</span><span class="sxs-lookup"><span data-stu-id="2493e-124">monitoring</span></span>](monitoring.md) <br/> |<span data-ttu-id="2493e-125">Enthält Konfigurationsinformationen, die definiert, wie und wann Transportdienst mit Agents überwacht, die installiert werden.</span><span class="sxs-lookup"><span data-stu-id="2493e-125">Contains configuration information that defines how and when the transport service monitors agents that are installed.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="2493e-126">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="2493e-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2493e-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="2493e-127">Namespace</span></span>  <br/> |<span data-ttu-id="2493e-128">Diese Datei ist nicht auf einen Namespace definieren.</span><span class="sxs-lookup"><span data-stu-id="2493e-128">This file does not define a namespace.</span></span>  <br/> |
|<span data-ttu-id="2493e-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="2493e-129">Schema Name</span></span>  <br/> |<span data-ttu-id="2493e-130">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2493e-130">Not available.</span></span>  <br/> |
|<span data-ttu-id="2493e-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="2493e-131">Validation File</span></span>  <br/> |<span data-ttu-id="2493e-132">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2493e-132">Not available.</span></span>  <br/> |
|<span data-ttu-id="2493e-133">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="2493e-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="2493e-134">Falsch.</span><span class="sxs-lookup"><span data-stu-id="2493e-134">False.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2493e-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2493e-135">See also</span></span>

- [<span data-ttu-id="2493e-136">Agents Datei Konfigurationselemente für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="2493e-136">Agents configuration file elements for Exchange 2013</span></span>](agents-configuration-file-elements-for-exchange-2013.md)

