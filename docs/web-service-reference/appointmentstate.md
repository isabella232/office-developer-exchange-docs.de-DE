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
description: Das AppointmentState-Element gibt den Status des Termins an.
ms.openlocfilehash: 8b0e827d02e9051f31d43199503dc286c50e2125
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463475"
---
# <a name="appointmentstate"></a><span data-ttu-id="cb3c2-103">AppointmentState</span><span class="sxs-lookup"><span data-stu-id="cb3c2-103">AppointmentState</span></span>

<span data-ttu-id="cb3c2-104">Das **AppointmentState** -Element gibt den Status des Termins an.</span><span class="sxs-lookup"><span data-stu-id="cb3c2-104">The **AppointmentState** element specifies the status of the appointment.</span></span> 
  
```XML
<AppointmentState/>
```

 <span data-ttu-id="cb3c2-105">**int**</span><span class="sxs-lookup"><span data-stu-id="cb3c2-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cb3c2-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="cb3c2-106">Attributes and elements</span></span>

<span data-ttu-id="cb3c2-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="cb3c2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cb3c2-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="cb3c2-108">Attributes</span></span>

<span data-ttu-id="cb3c2-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="cb3c2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cb3c2-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cb3c2-110">Child elements</span></span>

<span data-ttu-id="cb3c2-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="cb3c2-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="cb3c2-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cb3c2-112">Parent elements</span></span>

|<span data-ttu-id="cb3c2-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="cb3c2-113">**Element**</span></span>|<span data-ttu-id="cb3c2-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cb3c2-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cb3c2-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="cb3c2-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="cb3c2-116">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="cb3c2-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="cb3c2-117">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="cb3c2-117">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="cb3c2-118">Stellt eine Besprechung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="cb3c2-118">Represents a meeting in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="cb3c2-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="cb3c2-119">Text value</span></span>

<span data-ttu-id="cb3c2-120">Dieses Element enthält einen Textwert, der festgelegte Bits darstellt.</span><span class="sxs-lookup"><span data-stu-id="cb3c2-120">This element contains a text value that represents set bits.</span></span> <span data-ttu-id="cb3c2-121">Dies ist eine ganzzahlige Form.</span><span class="sxs-lookup"><span data-stu-id="cb3c2-121">This is in integer form.</span></span> <span data-ttu-id="cb3c2-122">Dieses Element ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="cb3c2-122">This element is read-only.</span></span> <span data-ttu-id="cb3c2-123">Sie wird nur in einer Antwort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cb3c2-123">It will only be returned in a response.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cb3c2-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cb3c2-124">Remarks</span></span>

<span data-ttu-id="cb3c2-125">Der zurückgegebene ganzzahlige Wert stellt die Bitmaske des Terminstatus dar.</span><span class="sxs-lookup"><span data-stu-id="cb3c2-125">The integer value that is returned represents the appointment state bitmask.</span></span> <span data-ttu-id="cb3c2-126">In der folgenden Tabelle werden die einzelnen Bit beschrieben.</span><span class="sxs-lookup"><span data-stu-id="cb3c2-126">The following table describes each bit.</span></span>
  
|<span data-ttu-id="cb3c2-127">**Name**</span><span class="sxs-lookup"><span data-stu-id="cb3c2-127">**Name**</span></span>|<span data-ttu-id="cb3c2-128">**Bit**</span><span class="sxs-lookup"><span data-stu-id="cb3c2-128">**Bit**</span></span>|<span data-ttu-id="cb3c2-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cb3c2-129">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="cb3c2-130">Keine</span><span class="sxs-lookup"><span data-stu-id="cb3c2-130">None</span></span>  <br/> |<span data-ttu-id="cb3c2-131">0x0000</span><span class="sxs-lookup"><span data-stu-id="cb3c2-131">0x0000</span></span>  <br/> |<span data-ttu-id="cb3c2-132">Es wurden keine Flags festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cb3c2-132">No flags have been set.</span></span> <span data-ttu-id="cb3c2-133">Dies wird nur für einen Termin verwendet, der keine Teilnehmer enthält.</span><span class="sxs-lookup"><span data-stu-id="cb3c2-133">This is only used for an appointment that does not include attendees.</span></span>  <br/> |
|<span data-ttu-id="cb3c2-134">Besprechung</span><span class="sxs-lookup"><span data-stu-id="cb3c2-134">Meeting</span></span>  <br/> |<span data-ttu-id="cb3c2-135">0x0001</span><span class="sxs-lookup"><span data-stu-id="cb3c2-135">0x0001</span></span>  <br/> |<span data-ttu-id="cb3c2-136">Dieser Termin ist eine Besprechung.</span><span class="sxs-lookup"><span data-stu-id="cb3c2-136">This appointment is a meeting.</span></span>  <br/> |
|<span data-ttu-id="cb3c2-137">Auszahlung</span><span class="sxs-lookup"><span data-stu-id="cb3c2-137">Received</span></span>  <br/> |<span data-ttu-id="cb3c2-138">0x0002</span><span class="sxs-lookup"><span data-stu-id="cb3c2-138">0x0002</span></span>  <br/> |<span data-ttu-id="cb3c2-139">Dieser Termin wurde empfangen.</span><span class="sxs-lookup"><span data-stu-id="cb3c2-139">This appointment has been received.</span></span>  <br/> |
|<span data-ttu-id="cb3c2-140">Abgebrochen</span><span class="sxs-lookup"><span data-stu-id="cb3c2-140">Canceled</span></span>  <br/> |<span data-ttu-id="cb3c2-141">0x0004</span><span class="sxs-lookup"><span data-stu-id="cb3c2-141">0x0004</span></span>  <br/> |<span data-ttu-id="cb3c2-142">Dieser Termin wurde abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="cb3c2-142">This appointment has been canceled.</span></span>  <br/> |
   
<span data-ttu-id="cb3c2-143">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="cb3c2-143">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cb3c2-144">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="cb3c2-144">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cb3c2-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="cb3c2-145">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="cb3c2-146">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="cb3c2-146">Schema name</span></span>  <br/> |<span data-ttu-id="cb3c2-147">Schematypen</span><span class="sxs-lookup"><span data-stu-id="cb3c2-147">Types schema</span></span>  <br/> |
|<span data-ttu-id="cb3c2-148">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="cb3c2-148">Validation file</span></span>  <br/> |<span data-ttu-id="cb3c2-149">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="cb3c2-149">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="cb3c2-150">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="cb3c2-150">Can be empty</span></span>  <br/> |<span data-ttu-id="cb3c2-151">False</span><span class="sxs-lookup"><span data-stu-id="cb3c2-151">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cb3c2-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cb3c2-152">See also</span></span>

- [<span data-ttu-id="cb3c2-153">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="cb3c2-153">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

