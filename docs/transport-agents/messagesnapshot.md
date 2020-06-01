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
description: 'Letzte Änderung: September 17, 2015'
ms.openlocfilehash: 8a58444580c803efb7312df95d75d697bc42e8e0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461842"
---
# <a name="messagesnapshot"></a><span data-ttu-id="68fcb-103">messageSnapshot</span><span class="sxs-lookup"><span data-stu-id="68fcb-103">messageSnapshot</span></span>

<span data-ttu-id="68fcb-104">**Gilt für:** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="68fcb-104">**Applies to:** Exchange Server 2013</span></span>
  
<span data-ttu-id="68fcb-105">Das **messageSnapshot** -Element enthält ein Attribut, das angibt, ob das Feature für die Pipelineablaufverfolgung für den Exchange-Server aktiviert ist, auf dem die Client Zugriffs-oder Postfachserverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="68fcb-105">The **messageSnapshot** element contains an attribute that specifies whether the pipeline tracing feature is enabled for the Exchange server that has the Client Access or the Mailbox server role installed.</span></span> 
  
- [<span data-ttu-id="68fcb-106">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="68fcb-106">configuration</span></span>](configuration.md)  
- [<span data-ttu-id="68fcb-107">mexRuntime</span><span class="sxs-lookup"><span data-stu-id="68fcb-107">mexRuntime</span></span>](mexruntime.md) 
- [<span data-ttu-id="68fcb-108">Überwachung</span><span class="sxs-lookup"><span data-stu-id="68fcb-108">monitoring</span></span>](monitoring.md) 
- [<span data-ttu-id="68fcb-109">messageSnapshot</span><span class="sxs-lookup"><span data-stu-id="68fcb-109">messageSnapshot</span></span>](messagesnapshot.md)
  
```XML
<messageSnapshot enabled="" />
```

<span data-ttu-id="68fcb-110">**messageSnapshotType (Boolean)**</span><span class="sxs-lookup"><span data-stu-id="68fcb-110">**messageSnapshotType (Boolean)**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="68fcb-111">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="68fcb-111">Attributes and elements</span></span>

<span data-ttu-id="68fcb-112">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="68fcb-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="68fcb-113">Attribute</span><span class="sxs-lookup"><span data-stu-id="68fcb-113">Attributes</span></span>

|<span data-ttu-id="68fcb-114">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="68fcb-114">**Attribute**</span></span>|<span data-ttu-id="68fcb-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="68fcb-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="68fcb-116">**enabled**</span><span class="sxs-lookup"><span data-stu-id="68fcb-116">**enabled**</span></span> <br/> |<span data-ttu-id="68fcb-117">Ein boolescher Wert, der angibt, ob das Feature für die Pipelineablaufverfolgung für den Client Zugriff oder den Postfachserver aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="68fcb-117">A Boolean value that indicates whether the pipeline tracing feature is enabled for the Client Access or the Mailbox server.</span></span> <span data-ttu-id="68fcb-118">Der Wert ist **true** , wenn die Pipelineablaufverfolgung aktiviert ist; Andernfalls ist der Wert **false** , oder das Element ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="68fcb-118">The value is **true** if pipeline tracing is enabled; otherwise, the value is **false** or the element is not present.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="68fcb-119">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="68fcb-119">Child elements</span></span>

<span data-ttu-id="68fcb-120">Keine.</span><span class="sxs-lookup"><span data-stu-id="68fcb-120">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="68fcb-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="68fcb-121">Parent elements</span></span>

|<span data-ttu-id="68fcb-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="68fcb-122">**Element**</span></span>|<span data-ttu-id="68fcb-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="68fcb-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="68fcb-124">Überwachung</span><span class="sxs-lookup"><span data-stu-id="68fcb-124">monitoring</span></span>](monitoring.md) <br/> |<span data-ttu-id="68fcb-125">Enthält Konfigurationsinformationen, die definieren, wie und wann der Transportdienst Agents überwacht, die installiert sind.</span><span class="sxs-lookup"><span data-stu-id="68fcb-125">Contains configuration information that defines how and when the transport service monitors agents that are installed.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="68fcb-126">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="68fcb-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="68fcb-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="68fcb-127">Namespace</span></span>  <br/> |<span data-ttu-id="68fcb-128">In dieser Datei wird kein Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="68fcb-128">This file does not define a namespace.</span></span>  <br/> |
|<span data-ttu-id="68fcb-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="68fcb-129">Schema Name</span></span>  <br/> |<span data-ttu-id="68fcb-130">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="68fcb-130">Not available.</span></span>  <br/> |
|<span data-ttu-id="68fcb-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="68fcb-131">Validation File</span></span>  <br/> |<span data-ttu-id="68fcb-132">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="68fcb-132">Not available.</span></span>  <br/> |
|<span data-ttu-id="68fcb-133">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="68fcb-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="68fcb-134">"False".</span><span class="sxs-lookup"><span data-stu-id="68fcb-134">False.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="68fcb-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="68fcb-135">See also</span></span>

- [<span data-ttu-id="68fcb-136">Elemente der Konfigurationsdatei der Agents für Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="68fcb-136">Agents configuration file elements for Exchange 2013</span></span>](agents-configuration-file-elements-for-exchange-2013.md)

