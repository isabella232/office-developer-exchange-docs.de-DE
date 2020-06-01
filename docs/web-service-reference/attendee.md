---
title: Teilnehmer
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Attendee
api_type:
- schema
ms.assetid: 393c3d7e-7416-458a-b976-270b88eaaa03
description: Das Attendee-Element stellt Teilnehmer und Ressourcen für eine Besprechung dar.
ms.openlocfilehash: f376e59b27017e0a9d27692cb1a4ae759cd1af0e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457648"
---
# <a name="attendee"></a><span data-ttu-id="f2114-103">Teilnehmer</span><span class="sxs-lookup"><span data-stu-id="f2114-103">Attendee</span></span>

<span data-ttu-id="f2114-104">Das **Attendee** -Element stellt Teilnehmer und Ressourcen für eine Besprechung dar.</span><span class="sxs-lookup"><span data-stu-id="f2114-104">The **Attendee** element represents attendees and resources for a meeting.</span></span> 
  
```xml
<Attendee>
   <Mailbox/>
   <ResponseType/>
   <LastResponseTime/>
</Attendee>
```

 <span data-ttu-id="f2114-105">**AttendeeType**</span><span class="sxs-lookup"><span data-stu-id="f2114-105">**AttendeeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f2114-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f2114-106">Attributes and elements</span></span>

<span data-ttu-id="f2114-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f2114-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f2114-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="f2114-108">Attributes</span></span>

<span data-ttu-id="f2114-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="f2114-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f2114-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f2114-110">Child elements</span></span>

|<span data-ttu-id="f2114-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="f2114-111">**Element**</span></span>|<span data-ttu-id="f2114-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f2114-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f2114-113">Postfach</span><span class="sxs-lookup"><span data-stu-id="f2114-113">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="f2114-114">Identifiziert eine vollständig aufgelöste e-Mail-Adresse.</span><span class="sxs-lookup"><span data-stu-id="f2114-114">Identifies a fully resolved e-mail address.</span></span>  <br/> |
|[<span data-ttu-id="f2114-115">ResponseType</span><span class="sxs-lookup"><span data-stu-id="f2114-115">ResponseType</span></span>](responsetype.md) <br/> |<span data-ttu-id="f2114-116">Stellt den Typ der Empfängerantwort dar, die für eine Besprechung empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="f2114-116">Represents the type of recipient response that is received for a meeting.</span></span> <span data-ttu-id="f2114-117">Diese Eigenschaft ist nur für das Kalenderelement eines Besprechungsorganisators relevant.</span><span class="sxs-lookup"><span data-stu-id="f2114-117">This property is only relevant to a meeting organizer's calendar item.</span></span>  <br/> |
|[<span data-ttu-id="f2114-118">LastResponseTime</span><span class="sxs-lookup"><span data-stu-id="f2114-118">LastResponseTime</span></span>](lastresponsetime.md) <br/> |<span data-ttu-id="f2114-119">Stellt das Datum und die Uhrzeit der letzten empfangenen Antwort dar.</span><span class="sxs-lookup"><span data-stu-id="f2114-119">Represents the date and time of the latest response that is received.</span></span>  <br/> |
|[<span data-ttu-id="f2114-120">ProposedStart</span><span class="sxs-lookup"><span data-stu-id="f2114-120">ProposedStart</span></span>](proposedstart-attendeetype.md) <br/> |<span data-ttu-id="f2114-121">Stellt die vorgeschlagene Startzeit eines Teilnehmers für eine Besprechung dar.</span><span class="sxs-lookup"><span data-stu-id="f2114-121">Represents an attendee's proposed start time for a meeting.</span></span> <br/> |
|[<span data-ttu-id="f2114-122">ProposedEnd</span><span class="sxs-lookup"><span data-stu-id="f2114-122">ProposedEnd</span></span>](proposedend-attendeetype.md) <br/> |<span data-ttu-id="f2114-123">Stellt die vorgeschlagene Endzeit eines Teilnehmers für eine Besprechung dar.</span><span class="sxs-lookup"><span data-stu-id="f2114-123">Represents an attendee's proposed end time for a meeting.</span></span> <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f2114-124">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f2114-124">Parent elements</span></span>

|<span data-ttu-id="f2114-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="f2114-125">**Element**</span></span>|<span data-ttu-id="f2114-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f2114-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f2114-127">RequiredAttendees</span><span class="sxs-lookup"><span data-stu-id="f2114-127">RequiredAttendees</span></span>](requiredattendees.md) <br/> |<span data-ttu-id="f2114-128">Stellt Teilnehmer dar, die für die Teilnahme an einer Besprechung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="f2114-128">Represents attendees that are required to attend a meeting.</span></span>  <br/> |
|[<span data-ttu-id="f2114-129">OptionalAttendees</span><span class="sxs-lookup"><span data-stu-id="f2114-129">OptionalAttendees</span></span>](optionalattendees.md) <br/> |<span data-ttu-id="f2114-130">Stellt Teilnehmer dar, die für die Teilnahme an einer Besprechung nicht erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="f2114-130">Represents attendees that are not required to attend a meeting.</span></span>  <br/> |
|[<span data-ttu-id="f2114-131">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f2114-131">Resources</span></span>](resources.md) <br/> |<span data-ttu-id="f2114-132">Stellt eine geplante Ressource für eine Besprechung dar.</span><span class="sxs-lookup"><span data-stu-id="f2114-132">Represents a scheduled resource for a meeting.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f2114-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f2114-133">Remarks</span></span>

<span data-ttu-id="f2114-134">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="f2114-134">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f2114-135">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="f2114-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f2114-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="f2114-136">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f2114-137">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f2114-137">Schema name</span></span>  <br/> |<span data-ttu-id="f2114-138">Schematypen</span><span class="sxs-lookup"><span data-stu-id="f2114-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="f2114-139">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f2114-139">Validation file</span></span>  <br/> |<span data-ttu-id="f2114-140">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f2114-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f2114-141">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="f2114-141">Can be empty</span></span>  <br/> |<span data-ttu-id="f2114-142">False</span><span class="sxs-lookup"><span data-stu-id="f2114-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f2114-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f2114-143">See also</span></span>

- [<span data-ttu-id="f2114-144">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="f2114-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

