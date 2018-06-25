---
title: AppointmentSequenceNumber
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AppointmentSequenceNumber
api_type:
- schema
ms.assetid: eb4c48bd-f905-48dc-ae16-53a080b9b025
description: Das AppointmentSequenceNumber-Element gibt die Sequenznummer des eine Version eines Termins.
ms.openlocfilehash: bc186170ccca06669ea7d20cea06c542f9ce274a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757362"
---
# <a name="appointmentsequencenumber"></a><span data-ttu-id="68cfe-103">AppointmentSequenceNumber</span><span class="sxs-lookup"><span data-stu-id="68cfe-103">AppointmentSequenceNumber</span></span>

<span data-ttu-id="68cfe-104">Das **AppointmentSequenceNumber** -Element gibt die Sequenznummer des eine Version eines Termins.</span><span class="sxs-lookup"><span data-stu-id="68cfe-104">The **AppointmentSequenceNumber** element specifies the sequence number of a version of an appointment.</span></span> 
  
```xml
<AppointmentSequenceNumber/>
```

 <span data-ttu-id="68cfe-105">**int**</span><span class="sxs-lookup"><span data-stu-id="68cfe-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="68cfe-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="68cfe-106">Attributes and elements</span></span>

<span data-ttu-id="68cfe-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="68cfe-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="68cfe-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="68cfe-108">Attributes</span></span>

<span data-ttu-id="68cfe-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="68cfe-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="68cfe-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="68cfe-110">Child elements</span></span>

<span data-ttu-id="68cfe-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="68cfe-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="68cfe-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="68cfe-112">Parent elements</span></span>

|<span data-ttu-id="68cfe-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="68cfe-113">**Element**</span></span>|<span data-ttu-id="68cfe-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="68cfe-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="68cfe-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="68cfe-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="68cfe-116">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="68cfe-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="68cfe-117">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="68cfe-117">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="68cfe-118">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="68cfe-118">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="68cfe-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="68cfe-119">Text value</span></span>

<span data-ttu-id="68cfe-120">Der Textwert stellt eine Versionsnummer.</span><span class="sxs-lookup"><span data-stu-id="68cfe-120">The text value represents a version number.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="68cfe-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="68cfe-121">Remarks</span></span>

<span data-ttu-id="68cfe-122">Dieser Wert wird aktualisiert, wenn der Termin mit neuen Informationen aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="68cfe-122">This value is updated when the appointment is updated with new information.</span></span> 
  
<span data-ttu-id="68cfe-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="68cfe-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="68cfe-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="68cfe-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="68cfe-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="68cfe-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="68cfe-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="68cfe-126">Schema Name</span></span>  <br/> |<span data-ttu-id="68cfe-127">Schematypen</span><span class="sxs-lookup"><span data-stu-id="68cfe-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="68cfe-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="68cfe-128">Validation File</span></span>  <br/> |<span data-ttu-id="68cfe-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="68cfe-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="68cfe-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="68cfe-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="68cfe-131">False</span><span class="sxs-lookup"><span data-stu-id="68cfe-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="68cfe-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="68cfe-132">See also</span></span>

- [<span data-ttu-id="68cfe-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="68cfe-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

