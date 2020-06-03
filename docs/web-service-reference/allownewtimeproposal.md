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
description: Das AllowNewTimeProposal-Element gibt an, ob eine neue Besprechungszeit für eine Besprechung von einem Teilnehmer vorgeschlagen werden kann.
ms.openlocfilehash: b3f2c569bced08c66144680a4fddd6e8bac0cecf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464805"
---
# <a name="allownewtimeproposal"></a><span data-ttu-id="592e2-103">AllowNewTimeProposal</span><span class="sxs-lookup"><span data-stu-id="592e2-103">AllowNewTimeProposal</span></span>

<span data-ttu-id="592e2-104">Das **AllowNewTimeProposal** -Element gibt an, ob eine neue Besprechungszeit für eine Besprechung von einem Teilnehmer vorgeschlagen werden kann.</span><span class="sxs-lookup"><span data-stu-id="592e2-104">The **AllowNewTimeProposal** element indicates whether a new meeting time can be proposed for a meeting by an attendee.</span></span> 
  
```xml
<AllowNewTimeProposal/>
```

 <span data-ttu-id="592e2-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="592e2-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="592e2-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="592e2-106">Attributes and elements</span></span>

<span data-ttu-id="592e2-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="592e2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="592e2-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="592e2-108">Attributes</span></span>

<span data-ttu-id="592e2-109">Keine</span><span class="sxs-lookup"><span data-stu-id="592e2-109">None</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="592e2-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="592e2-110">Child elements</span></span>

<span data-ttu-id="592e2-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="592e2-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="592e2-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="592e2-112">Parent elements</span></span>

|<span data-ttu-id="592e2-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="592e2-113">**Element**</span></span>|<span data-ttu-id="592e2-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="592e2-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="592e2-115">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="592e2-115">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="592e2-116">Stellt eine Besprechung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="592e2-116">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="592e2-117">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="592e2-117">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="592e2-118">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="592e2-118">Represents an Exchange calendar item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="592e2-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="592e2-119">Text value</span></span>

<span data-ttu-id="592e2-120">Ein Textwert, der einen booleschen Wert darstellt, ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="592e2-120">A text value that represents a Boolean value is required.</span></span> <span data-ttu-id="592e2-121">Der Wert **true** gibt an, dass ein neuer Vorschlag für die Besprechungszeit erstellt werden kann. der Wert **false** gibt an, dass keine neuen Zeit Vorschläge zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="592e2-121">A value of **true** indicates that a new proposal for the meeting time can be created; a value of **false** indicates that new time proposals are not allowed.</span></span> <span data-ttu-id="592e2-122">Der Organisator legt diesen Wert in der Besprechungsanfrage fest.</span><span class="sxs-lookup"><span data-stu-id="592e2-122">The organizer sets this value in the meeting request.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="592e2-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="592e2-123">Remarks</span></span>

<span data-ttu-id="592e2-124">Die AllowNewTimeProposal-Eigenschaft ist für das Kalenderelement des Organisators schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="592e2-124">The AllowNewTimeProposal property is read-writable for the organizer's calendar item.</span></span> <span data-ttu-id="592e2-125">Er ist schreibgeschützt für Besprechungsanfragen und für die Kalenderelemente von Teilnehmern.</span><span class="sxs-lookup"><span data-stu-id="592e2-125">It is read-only for meeting requests and for attendees' calendar items.</span></span>
  
<span data-ttu-id="592e2-126">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="592e2-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
> [!NOTE]
> <span data-ttu-id="592e2-127">Exchange Webdienste unterstützt keine neuen Zeit Angebots Meldungen.</span><span class="sxs-lookup"><span data-stu-id="592e2-127">Exchange Web Services does not support new time proposal messages.</span></span> <span data-ttu-id="592e2-128">Zum Abrufen von Eigenschaften, die sich auf neue Zeit Vorschlags Meldungen beziehen, verwenden Sie erweiterte Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="592e2-128">To get properties that are related to new time proposal messages, use extended properties.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="592e2-129">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="592e2-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="592e2-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="592e2-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="592e2-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="592e2-131">Schema name</span></span>  <br/> |<span data-ttu-id="592e2-132">Schematypen</span><span class="sxs-lookup"><span data-stu-id="592e2-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="592e2-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="592e2-133">Validation file</span></span>  <br/> |<span data-ttu-id="592e2-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="592e2-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="592e2-135">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="592e2-135">Can be empty</span></span>  <br/> |<span data-ttu-id="592e2-136">False</span><span class="sxs-lookup"><span data-stu-id="592e2-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="592e2-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="592e2-137">See also</span></span>

- [<span data-ttu-id="592e2-138">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="592e2-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

