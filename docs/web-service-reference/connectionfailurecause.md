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
description: Das ConnectionFailureCause-Element gibt den Grund für eine Trennung von einem Telefonanruf an.
ms.openlocfilehash: 6385641eaee140a114906703232974d51d5ce344
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529448"
---
# <a name="connectionfailurecause"></a><span data-ttu-id="26087-103">ConnectionFailureCause</span><span class="sxs-lookup"><span data-stu-id="26087-103">ConnectionFailureCause</span></span>

<span data-ttu-id="26087-104">Das **ConnectionFailureCause** -Element gibt den Grund für eine Trennung von einem Telefonanruf an.</span><span class="sxs-lookup"><span data-stu-id="26087-104">The **ConnectionFailureCause** element specifies the reason for a disconnection from a telephone call.</span></span> 
  
```xml
<ConnectionFailureCause>None or UserBusy or NoAnswer or Unavailable or Other</ConnectionFailureCause>
```

 <span data-ttu-id="26087-105">**ConnectionFailureCauseType**</span><span class="sxs-lookup"><span data-stu-id="26087-105">**ConnectionFailureCauseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="26087-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="26087-106">Attributes and elements</span></span>

<span data-ttu-id="26087-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="26087-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="26087-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="26087-108">Attributes</span></span>

<span data-ttu-id="26087-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="26087-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="26087-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="26087-110">Child elements</span></span>

<span data-ttu-id="26087-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="26087-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="26087-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="26087-112">Parent elements</span></span>

|<span data-ttu-id="26087-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="26087-113">**Element**</span></span>|<span data-ttu-id="26087-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="26087-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="26087-115">PhoneCallInformation</span><span class="sxs-lookup"><span data-stu-id="26087-115">PhoneCallInformation</span></span>](phonecallinformation.md) <br/> |<span data-ttu-id="26087-116">Gibt die Statusinformationen für einen Telefonanruf an.</span><span class="sxs-lookup"><span data-stu-id="26087-116">Specifies the state information for a telephone call.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="26087-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="26087-117">Text value</span></span>

<span data-ttu-id="26087-118">In der folgenden Tabelle sind die möglichen Werte für das **ConnectionFailureCause** -Element aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="26087-118">The following table lists the possible values for the **ConnectionFailureCause** element.</span></span> 
  
<span data-ttu-id="26087-119">**ConnectionFailureCause-Elementwerte**</span><span class="sxs-lookup"><span data-stu-id="26087-119">**ConnectionFailureCause element values**</span></span>

|<span data-ttu-id="26087-120">**Wert**</span><span class="sxs-lookup"><span data-stu-id="26087-120">**Value**</span></span>|<span data-ttu-id="26087-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="26087-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="26087-122">Keine</span><span class="sxs-lookup"><span data-stu-id="26087-122">None</span></span>  <br/> |<span data-ttu-id="26087-123">Der Anrufstatus ist nicht getrennt, oder der Verbindungs Grund ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="26087-123">Call state is not disconnected or the disconnect reason is not known.</span></span>  <br/> |
|<span data-ttu-id="26087-124">UserBusy</span><span class="sxs-lookup"><span data-stu-id="26087-124">UserBusy</span></span>  <br/> |<span data-ttu-id="26087-125">Die angerufene Partei war besetzt.</span><span class="sxs-lookup"><span data-stu-id="26087-125">The called party line was busy.</span></span>  <br/> |
|<span data-ttu-id="26087-126">Noanswer</span><span class="sxs-lookup"><span data-stu-id="26087-126">NoAnswer</span></span>  <br/> |<span data-ttu-id="26087-127">Der angerufene Teilnehmer hat nicht geantwortet.</span><span class="sxs-lookup"><span data-stu-id="26087-127">The called party did not answer.</span></span>  <br/> |
|<span data-ttu-id="26087-128">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="26087-128">Unavailable</span></span>  <br/> |<span data-ttu-id="26087-129">Die angerufene Partei Nummer war nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="26087-129">The called party number was not available.</span></span>  <br/> |
|<span data-ttu-id="26087-130">Andere</span><span class="sxs-lookup"><span data-stu-id="26087-130">Other</span></span>  <br/> |<span data-ttu-id="26087-131">Catch-all für andere Gründe für die Trennung.</span><span class="sxs-lookup"><span data-stu-id="26087-131">Catch-all for other disconnect reasons.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="26087-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="26087-132">Remarks</span></span>

<span data-ttu-id="26087-133">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="26087-133">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="26087-134">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="26087-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="26087-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="26087-135">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="26087-136">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="26087-136">Schema Name</span></span>  <br/> |<span data-ttu-id="26087-137">Schematypen</span><span class="sxs-lookup"><span data-stu-id="26087-137">Types schema</span></span>  <br/> |
|<span data-ttu-id="26087-138">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="26087-138">Validation File</span></span>  <br/> |<span data-ttu-id="26087-139">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="26087-139">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="26087-140">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="26087-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="26087-141">False</span><span class="sxs-lookup"><span data-stu-id="26087-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="26087-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="26087-142">See also</span></span>



- [<span data-ttu-id="26087-143">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="26087-143">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

