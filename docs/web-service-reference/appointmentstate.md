---
title: AppointmentState
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AppointmentState
api_type:
- schema
ms.assetid: ab3f5d04-ace1-4a15-9107-cefa6c41abc7
description: Das AppointmentState-Element gibt den Status des Termins.
ms.openlocfilehash: 05e92a3fea10a84518b0680c425011a91bc43d93
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757364"
---
# <a name="appointmentstate"></a><span data-ttu-id="60f45-103">AppointmentState</span><span class="sxs-lookup"><span data-stu-id="60f45-103">AppointmentState</span></span>

<span data-ttu-id="60f45-104">Das **AppointmentState** -Element gibt den Status des Termins.</span><span class="sxs-lookup"><span data-stu-id="60f45-104">The **AppointmentState** element specifies the status of the appointment.</span></span> 
  
```XML
<AppointmentState/>
```

 <span data-ttu-id="60f45-105">**int**</span><span class="sxs-lookup"><span data-stu-id="60f45-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="60f45-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="60f45-106">Attributes and elements</span></span>

<span data-ttu-id="60f45-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="60f45-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="60f45-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="60f45-108">Attributes</span></span>

<span data-ttu-id="60f45-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="60f45-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="60f45-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="60f45-110">Child elements</span></span>

<span data-ttu-id="60f45-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="60f45-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="60f45-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="60f45-112">Parent elements</span></span>

|<span data-ttu-id="60f45-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="60f45-113">**Element**</span></span>|<span data-ttu-id="60f45-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="60f45-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="60f45-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="60f45-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="60f45-116">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="60f45-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="60f45-117">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="60f45-117">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="60f45-118">Stellt eine Besprechung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="60f45-118">Represents a meeting in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="60f45-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="60f45-119">Text value</span></span>

<span data-ttu-id="60f45-120">Dieses Element enthält einen Textwert, dass stellt Bits festgelegt.</span><span class="sxs-lookup"><span data-stu-id="60f45-120">This element contains a text value that represents set bits.</span></span> <span data-ttu-id="60f45-121">Dies ist Integer-Formular.</span><span class="sxs-lookup"><span data-stu-id="60f45-121">This is in integer form.</span></span> <span data-ttu-id="60f45-122">Dieses Element ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="60f45-122">This element is read-only.</span></span> <span data-ttu-id="60f45-123">Es wird nur in einer Antwort zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="60f45-123">It will only be returned in a response.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="60f45-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="60f45-124">Remarks</span></span>

<span data-ttu-id="60f45-125">Der Ganzzahlwert, der zurückgegeben wird, stellt die Termin Zustand Bitmaske dar.</span><span class="sxs-lookup"><span data-stu-id="60f45-125">The integer value that is returned represents the appointment state bitmask.</span></span> <span data-ttu-id="60f45-126">Die folgende Tabelle beschreibt jedes Bit.</span><span class="sxs-lookup"><span data-stu-id="60f45-126">The following table describes each bit.</span></span>
  
|<span data-ttu-id="60f45-127">**Name**</span><span class="sxs-lookup"><span data-stu-id="60f45-127">**Name**</span></span>|<span data-ttu-id="60f45-128">**Bit**</span><span class="sxs-lookup"><span data-stu-id="60f45-128">**Bit**</span></span>|<span data-ttu-id="60f45-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="60f45-129">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="60f45-130">Keine</span><span class="sxs-lookup"><span data-stu-id="60f45-130">None</span></span>  <br/> |<span data-ttu-id="60f45-131">0x0000</span><span class="sxs-lookup"><span data-stu-id="60f45-131">0x0000</span></span>  <br/> |<span data-ttu-id="60f45-132">Keine Flags es wurden festgelegt.</span><span class="sxs-lookup"><span data-stu-id="60f45-132">No flags have been set.</span></span> <span data-ttu-id="60f45-133">Dies ist nur für einen Termin verwendet, die nicht Teilnehmer enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="60f45-133">This is only used for an appointment that does not include attendees.</span></span>  <br/> |
|<span data-ttu-id="60f45-134">Besprechung</span><span class="sxs-lookup"><span data-stu-id="60f45-134">Meeting</span></span>  <br/> |<span data-ttu-id="60f45-135">0x0001</span><span class="sxs-lookup"><span data-stu-id="60f45-135">0x0001</span></span>  <br/> |<span data-ttu-id="60f45-136">Dieser Termin ist eine Besprechung.</span><span class="sxs-lookup"><span data-stu-id="60f45-136">This appointment is a meeting.</span></span>  <br/> |
|<span data-ttu-id="60f45-137">Auszahlung</span><span class="sxs-lookup"><span data-stu-id="60f45-137">Received</span></span>  <br/> |<span data-ttu-id="60f45-138">0x0002</span><span class="sxs-lookup"><span data-stu-id="60f45-138">0x0002</span></span>  <br/> |<span data-ttu-id="60f45-139">Dieser Termin wurde empfangen.</span><span class="sxs-lookup"><span data-stu-id="60f45-139">This appointment has been received.</span></span>  <br/> |
|<span data-ttu-id="60f45-140">Abgebrochen</span><span class="sxs-lookup"><span data-stu-id="60f45-140">Canceled</span></span>  <br/> |<span data-ttu-id="60f45-141">0x0004</span><span class="sxs-lookup"><span data-stu-id="60f45-141">0x0004</span></span>  <br/> |<span data-ttu-id="60f45-142">Dieser Termin wurde abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="60f45-142">This appointment has been canceled.</span></span>  <br/> |
   
<span data-ttu-id="60f45-143">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="60f45-143">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="60f45-144">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="60f45-144">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="60f45-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="60f45-145">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="60f45-146">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="60f45-146">Schema name</span></span>  <br/> |<span data-ttu-id="60f45-147">Schematypen</span><span class="sxs-lookup"><span data-stu-id="60f45-147">Types schema</span></span>  <br/> |
|<span data-ttu-id="60f45-148">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="60f45-148">Validation file</span></span>  <br/> |<span data-ttu-id="60f45-149">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="60f45-149">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="60f45-150">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="60f45-150">Can be empty</span></span>  <br/> |<span data-ttu-id="60f45-151">False</span><span class="sxs-lookup"><span data-stu-id="60f45-151">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="60f45-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="60f45-152">See also</span></span>

- [<span data-ttu-id="60f45-153">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="60f45-153">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

