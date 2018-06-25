---
title: ConnectionFailureCause
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConnectionFailureCause
api_type:
- schema
ms.assetid: d2160c8a-015c-4964-b7f7-93478764a173
description: Das ConnectionFailureCause-Element gibt den Grund für eine Trennung der Verbindung mit einem Anruf.
ms.openlocfilehash: 54b4f5b89efdb42ef82dbef8f1af14a39c0ccc6a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757600"
---
# <a name="connectionfailurecause"></a><span data-ttu-id="f312d-103">ConnectionFailureCause</span><span class="sxs-lookup"><span data-stu-id="f312d-103">ConnectionFailureCause</span></span>

<span data-ttu-id="f312d-104">Das **ConnectionFailureCause** -Element gibt den Grund für eine Trennung der Verbindung mit einem Anruf.</span><span class="sxs-lookup"><span data-stu-id="f312d-104">The **ConnectionFailureCause** element specifies the reason for a disconnection from a telephone call.</span></span> 
  
```xml
<ConnectionFailureCause>None or UserBusy or NoAnswer or Unavailable or Other</ConnectionFailureCause>
```

 <span data-ttu-id="f312d-105">**ConnectionFailureCauseType**</span><span class="sxs-lookup"><span data-stu-id="f312d-105">**ConnectionFailureCauseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f312d-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f312d-106">Attributes and elements</span></span>

<span data-ttu-id="f312d-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f312d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f312d-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="f312d-108">Attributes</span></span>

<span data-ttu-id="f312d-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="f312d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f312d-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f312d-110">Child elements</span></span>

<span data-ttu-id="f312d-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="f312d-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f312d-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f312d-112">Parent elements</span></span>

|<span data-ttu-id="f312d-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="f312d-113">**Element**</span></span>|<span data-ttu-id="f312d-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f312d-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f312d-115">PhoneCallInformation</span><span class="sxs-lookup"><span data-stu-id="f312d-115">PhoneCallInformation</span></span>](phonecallinformation.md) <br/> |<span data-ttu-id="f312d-116">Gibt die Statusinformationen für einen Telefonanruf an.</span><span class="sxs-lookup"><span data-stu-id="f312d-116">Specifies the state information for a telephone call.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f312d-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="f312d-117">Text value</span></span>

<span data-ttu-id="f312d-118">Die folgende Tabelle enthält die möglichen Werte für das **ConnectionFailureCause** -Element.</span><span class="sxs-lookup"><span data-stu-id="f312d-118">The following table lists the possible values for the **ConnectionFailureCause** element.</span></span> 
  
<span data-ttu-id="f312d-119">**ConnectionFailureCause-Elementwerte**</span><span class="sxs-lookup"><span data-stu-id="f312d-119">**ConnectionFailureCause element values**</span></span>

|<span data-ttu-id="f312d-120">**Wert**</span><span class="sxs-lookup"><span data-stu-id="f312d-120">**Value**</span></span>|<span data-ttu-id="f312d-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f312d-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f312d-122">Keine</span><span class="sxs-lookup"><span data-stu-id="f312d-122">None</span></span>  <br/> |<span data-ttu-id="f312d-123">Anrufstatus nicht getrennt ist, oder der Disconnect Grund ist nicht bekannt.</span><span class="sxs-lookup"><span data-stu-id="f312d-123">Call state is not disconnected or the disconnect reason is not known.</span></span>  <br/> |
|<span data-ttu-id="f312d-124">UserBusy</span><span class="sxs-lookup"><span data-stu-id="f312d-124">UserBusy</span></span>  <br/> |<span data-ttu-id="f312d-125">Die gewählte Partei Zeile war ausgelastet.</span><span class="sxs-lookup"><span data-stu-id="f312d-125">The called party line was busy.</span></span>  <br/> |
|<span data-ttu-id="f312d-126">NoAnswer</span><span class="sxs-lookup"><span data-stu-id="f312d-126">NoAnswer</span></span>  <br/> |<span data-ttu-id="f312d-127">Der angerufene hat nicht geantwortet.</span><span class="sxs-lookup"><span data-stu-id="f312d-127">The called party did not answer.</span></span>  <br/> |
|<span data-ttu-id="f312d-128">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f312d-128">Unavailable</span></span>  <br/> |<span data-ttu-id="f312d-129">Die Anzahl der angerufenen war nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f312d-129">The called party number was not available.</span></span>  <br/> |
|<span data-ttu-id="f312d-130">Andere</span><span class="sxs-lookup"><span data-stu-id="f312d-130">Other</span></span>  <br/> |<span data-ttu-id="f312d-131">Catch-All anderen Gründen trennen.</span><span class="sxs-lookup"><span data-stu-id="f312d-131">Catch-all for other disconnect reasons.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f312d-132">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f312d-132">Remarks</span></span>

<span data-ttu-id="f312d-133">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="f312d-133">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f312d-134">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="f312d-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f312d-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="f312d-135">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f312d-136">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f312d-136">Schema Name</span></span>  <br/> |<span data-ttu-id="f312d-137">Schematypen</span><span class="sxs-lookup"><span data-stu-id="f312d-137">Types schema</span></span>  <br/> |
|<span data-ttu-id="f312d-138">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f312d-138">Validation File</span></span>  <br/> |<span data-ttu-id="f312d-139">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f312d-139">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f312d-140">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="f312d-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="f312d-141">False</span><span class="sxs-lookup"><span data-stu-id="f312d-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f312d-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f312d-142">See also</span></span>



- [<span data-ttu-id="f312d-143">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="f312d-143">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

