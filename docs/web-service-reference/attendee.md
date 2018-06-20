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
description: Das Attendee-Element darstellt, Teilnehmer und Ressourcen für eine Besprechung.
ms.openlocfilehash: 60cb0839c2f6de69b833c11f4594d40c14cd8887
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757399"
---
# <a name="attendee"></a><span data-ttu-id="4ee65-103">Teilnehmer</span><span class="sxs-lookup"><span data-stu-id="4ee65-103">Attendee</span></span>

<span data-ttu-id="4ee65-104">Das **Attendee** -Element darstellt, Teilnehmer und Ressourcen für eine Besprechung.</span><span class="sxs-lookup"><span data-stu-id="4ee65-104">The **Attendee** element represents attendees and resources for a meeting.</span></span> 
  
```xml
<Attendee>
   <Mailbox/>
   <ResponseType/>
   <LastResponseTime/>
</Attendee>
```

 <span data-ttu-id="4ee65-105">**AttendeeType**</span><span class="sxs-lookup"><span data-stu-id="4ee65-105">**AttendeeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4ee65-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="4ee65-106">Attributes and elements</span></span>

<span data-ttu-id="4ee65-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="4ee65-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4ee65-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="4ee65-108">Attributes</span></span>

<span data-ttu-id="4ee65-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="4ee65-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4ee65-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4ee65-110">Child elements</span></span>

|<span data-ttu-id="4ee65-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="4ee65-111">**Element**</span></span>|<span data-ttu-id="4ee65-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4ee65-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4ee65-113">Postfach</span><span class="sxs-lookup"><span data-stu-id="4ee65-113">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="4ee65-114">Identifiziert eine vollständig aufgelöster E-mail-Adresse.</span><span class="sxs-lookup"><span data-stu-id="4ee65-114">Identifies a fully resolved e-mail address.</span></span>  <br/> |
|[<span data-ttu-id="4ee65-115">ResponseType</span><span class="sxs-lookup"><span data-stu-id="4ee65-115">ResponseType</span></span>](responsetype.md) <br/> |<span data-ttu-id="4ee65-116">Stellt den Typ der Empfänger Antwort, die für eine Besprechung empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="4ee65-116">Represents the type of recipient response that is received for a meeting.</span></span> <span data-ttu-id="4ee65-117">Diese Eigenschaft ist nur relevant, Kalenderelement Organisator einer Besprechung.</span><span class="sxs-lookup"><span data-stu-id="4ee65-117">This property is only relevant to a meeting organizer's calendar item.</span></span>  <br/> |
|[<span data-ttu-id="4ee65-118">LastResponseTime</span><span class="sxs-lookup"><span data-stu-id="4ee65-118">LastResponseTime</span></span>](lastresponsetime.md) <br/> |<span data-ttu-id="4ee65-119">Stellt das Datum und Uhrzeit der neuesten Antwort, die empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="4ee65-119">Represents the date and time of the latest response that is received.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4ee65-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4ee65-120">Parent elements</span></span>

|<span data-ttu-id="4ee65-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="4ee65-121">**Element**</span></span>|<span data-ttu-id="4ee65-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4ee65-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4ee65-123">RequiredAttendees</span><span class="sxs-lookup"><span data-stu-id="4ee65-123">RequiredAttendees</span></span>](requiredattendees.md) <br/> |<span data-ttu-id="4ee65-124">Stellt die Teilnehmer, die erforderlich sind, an einer Besprechung teilnehmen.</span><span class="sxs-lookup"><span data-stu-id="4ee65-124">Represents attendees that are required to attend a meeting.</span></span>  <br/> |
|[<span data-ttu-id="4ee65-125">OptionalAttendees</span><span class="sxs-lookup"><span data-stu-id="4ee65-125">OptionalAttendees</span></span>](optionalattendees.md) <br/> |<span data-ttu-id="4ee65-126">Stellt die Teilnehmer, die nicht erforderlich sind, an einer Besprechung teilnehmen.</span><span class="sxs-lookup"><span data-stu-id="4ee65-126">Represents attendees that are not required to attend a meeting.</span></span>  <br/> |
|[<span data-ttu-id="4ee65-127">Ressourcen </span><span class="sxs-lookup"><span data-stu-id="4ee65-127">Resources</span></span>](resources.md) <br/> |<span data-ttu-id="4ee65-128">Stellt eine geplante Ressource für eine Besprechung.</span><span class="sxs-lookup"><span data-stu-id="4ee65-128">Represents a scheduled resource for a meeting.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4ee65-129">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4ee65-129">Remarks</span></span>

<span data-ttu-id="4ee65-130">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="4ee65-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4ee65-131">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="4ee65-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4ee65-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="4ee65-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4ee65-133">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="4ee65-133">Schema name</span></span>  <br/> |<span data-ttu-id="4ee65-134">Schematypen</span><span class="sxs-lookup"><span data-stu-id="4ee65-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="4ee65-135">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="4ee65-135">Validation file</span></span>  <br/> |<span data-ttu-id="4ee65-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4ee65-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4ee65-137">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="4ee65-137">Can be empty</span></span>  <br/> |<span data-ttu-id="4ee65-138">False</span><span class="sxs-lookup"><span data-stu-id="4ee65-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4ee65-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4ee65-139">See also</span></span>

- [<span data-ttu-id="4ee65-140">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="4ee65-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

