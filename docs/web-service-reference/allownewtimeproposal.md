---
title: AllowNewTimeProposal
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AllowNewTimeProposal
api_type:
- schema
ms.assetid: afdb4ec9-2daf-48a1-a0bb-a7f647f212f2
description: Das AllowNewTimeProposal-Element gibt an, ob für eine Besprechung durch ein Teilnehmer eine neue Besprechungszeit vorgeschlagen werden kann.
ms.openlocfilehash: d5deed5044769c477ffe54cc533d5261ba2e1932
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757253"
---
# <a name="allownewtimeproposal"></a><span data-ttu-id="19dce-103">AllowNewTimeProposal</span><span class="sxs-lookup"><span data-stu-id="19dce-103">AllowNewTimeProposal</span></span>

<span data-ttu-id="19dce-104">Das **AllowNewTimeProposal** -Element gibt an, ob für eine Besprechung durch ein Teilnehmer eine neue Besprechungszeit vorgeschlagen werden kann.</span><span class="sxs-lookup"><span data-stu-id="19dce-104">The **AllowNewTimeProposal** element indicates whether a new meeting time can be proposed for a meeting by an attendee.</span></span> 
  
```xml
<AllowNewTimeProposal/>
```

 <span data-ttu-id="19dce-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="19dce-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="19dce-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="19dce-106">Attributes and elements</span></span>

<span data-ttu-id="19dce-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="19dce-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="19dce-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="19dce-108">Attributes</span></span>

<span data-ttu-id="19dce-109">Keine</span><span class="sxs-lookup"><span data-stu-id="19dce-109">None</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="19dce-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="19dce-110">Child elements</span></span>

<span data-ttu-id="19dce-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="19dce-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="19dce-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="19dce-112">Parent elements</span></span>

|<span data-ttu-id="19dce-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="19dce-113">**Element**</span></span>|<span data-ttu-id="19dce-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="19dce-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="19dce-115">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="19dce-115">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="19dce-116">Stellt eine Besprechung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="19dce-116">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="19dce-117">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="19dce-117">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="19dce-118">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="19dce-118">Represents an Exchange calendar item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="19dce-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="19dce-119">Text value</span></span>

<span data-ttu-id="19dce-120">Ein Textwert, der einen booleschen Wert darstellt, ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="19dce-120">A text value that represents a Boolean value is required.</span></span> <span data-ttu-id="19dce-121">Der Wert **true** gibt an, dass für die Besprechungszeit ein neues Vorschlags erstellt werden kann; der Wert **false** gibt an, dass neue Zeit Vorschläge nicht zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="19dce-121">A value of **true** indicates that a new proposal for the meeting time can be created; a value of **false** indicates that new time proposals are not allowed.</span></span> <span data-ttu-id="19dce-122">Der Organisator Festlegen dieses Werts in der Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="19dce-122">The organizer sets this value in the meeting request.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="19dce-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="19dce-123">Remarks</span></span>

<span data-ttu-id="19dce-124">Die AllowNewTimeProposal-Eigenschaft kann für den Organisator Kalenderelement lesen geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="19dce-124">The AllowNewTimeProposal property is read-writable for the organizer's calendar item.</span></span> <span data-ttu-id="19dce-125">Es ist schreibgeschützt, für Besprechungsanfragen und Kalenderelemente Teilnehmer.</span><span class="sxs-lookup"><span data-stu-id="19dce-125">It is read-only for meeting requests and for attendees' calendar items.</span></span>
  
<span data-ttu-id="19dce-126">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="19dce-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
> [!NOTE]
> <span data-ttu-id="19dce-127">Exchange-Webdienste unterstützt keine neue Zeit Vorschlag Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="19dce-127">Exchange Web Services does not support new time proposal messages.</span></span> <span data-ttu-id="19dce-128">Um die Eigenschaften, die im Zusammenhang mit neuen Uhrzeit Vorschlag Nachrichten erhalten möchten, verwenden Sie erweiterte Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="19dce-128">To get properties that are related to new time proposal messages, use extended properties.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="19dce-129">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="19dce-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="19dce-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="19dce-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="19dce-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="19dce-131">Schema name</span></span>  <br/> |<span data-ttu-id="19dce-132">Schematypen</span><span class="sxs-lookup"><span data-stu-id="19dce-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="19dce-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="19dce-133">Validation file</span></span>  <br/> |<span data-ttu-id="19dce-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="19dce-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="19dce-135">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="19dce-135">Can be empty</span></span>  <br/> |<span data-ttu-id="19dce-136">False</span><span class="sxs-lookup"><span data-stu-id="19dce-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="19dce-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="19dce-137">See also</span></span>

- [<span data-ttu-id="19dce-138">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="19dce-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

