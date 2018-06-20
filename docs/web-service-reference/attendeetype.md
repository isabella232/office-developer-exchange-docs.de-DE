---
title: AttendeeType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AttendeeType
api_type:
- schema
ms.assetid: 048043a8-dbad-45a0-97c8-4cad63d8898b
description: Das Element AttendeeType stellt den Typ des Teilnehmers, der in der E-Mail (EmailAddressType)-Element identifiziert wird. Dieses Element wird in Anforderungen für Besprechungsvorschläge verwendet.
ms.openlocfilehash: a08532ed78296102ee252c1e0c40beee7ca8ea5d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757404"
---
# <a name="attendeetype"></a><span data-ttu-id="44008-104">AttendeeType</span><span class="sxs-lookup"><span data-stu-id="44008-104">AttendeeType</span></span>

<span data-ttu-id="44008-105">Das Element **AttendeeType** stellt den Typ des Teilnehmers, der in der [E-Mail (EmailAddressType)](email-emailaddresstype.md) -Element identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="44008-105">The **AttendeeType** element represents the type of attendee that is identified in the [Email (EmailAddressType)](email-emailaddresstype.md) element.</span></span> <span data-ttu-id="44008-106">Dieses Element wird in Anforderungen für Besprechungsvorschläge verwendet.</span><span class="sxs-lookup"><span data-stu-id="44008-106">This element is used in requests for meeting suggestions.</span></span> 
  
- [<span data-ttu-id="44008-107">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="44008-107">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
- [<span data-ttu-id="44008-108">MailboxDataArray</span><span class="sxs-lookup"><span data-stu-id="44008-108">MailboxDataArray</span></span>](mailboxdataarray.md)
  
- [<span data-ttu-id="44008-109">MailboxData</span><span class="sxs-lookup"><span data-stu-id="44008-109">MailboxData</span></span>](mailboxdata.md)
  
- [<span data-ttu-id="44008-110">AttendeeType</span><span class="sxs-lookup"><span data-stu-id="44008-110">AttendeeType</span></span>](attendeetype.md)
  
```xml
<AttendeeType>Organizer or Required or Optional or Room or Resource</AttendeeType>
```

 <span data-ttu-id="44008-111">**MeetingAttendeeType**</span><span class="sxs-lookup"><span data-stu-id="44008-111">**MeetingAttendeeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="44008-112">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="44008-112">Attributes and elements</span></span>

<span data-ttu-id="44008-113">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="44008-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="44008-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="44008-114">Attributes</span></span>

<span data-ttu-id="44008-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="44008-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="44008-116">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="44008-116">Child elements</span></span>

<span data-ttu-id="44008-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="44008-117">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="44008-118">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="44008-118">Parent elements</span></span>

|<span data-ttu-id="44008-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="44008-119">**Element**</span></span>|<span data-ttu-id="44008-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="44008-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="44008-121">MailboxData</span><span class="sxs-lookup"><span data-stu-id="44008-121">MailboxData</span></span>](mailboxdata.md) <br/> |<span data-ttu-id="44008-122">Stellt eine einzelne Postfachbenutzer und Optionen für den Typ der Daten zu den Postfachbenutzer zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="44008-122">Represents an individual mailbox user and options for the type of data to be returned about the mailbox user.</span></span>  <br/> <span data-ttu-id="44008-123">Es folgt der XPath-Ausdruck für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="44008-123">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/MailboxDataArray[i]/MailboxData` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="44008-124">Textwert</span><span class="sxs-lookup"><span data-stu-id="44008-124">Text value</span></span>

<span data-ttu-id="44008-125">Es wird ein Textwert für dieses Element erforderlich.</span><span class="sxs-lookup"><span data-stu-id="44008-125">A text value is required for this element.</span></span> <span data-ttu-id="44008-126">Die folgende Tabelle enthält die möglichen Werte für dieses Element.</span><span class="sxs-lookup"><span data-stu-id="44008-126">The following table lists the possible values for this element.</span></span>
  
|<span data-ttu-id="44008-127">**Wert**</span><span class="sxs-lookup"><span data-stu-id="44008-127">**Value**</span></span>|<span data-ttu-id="44008-128">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="44008-128">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="44008-129">Organisator</span><span class="sxs-lookup"><span data-stu-id="44008-129">Organizer</span></span>  <br/> |<span data-ttu-id="44008-130">Die Postfachbenutzer und Teilnehmer, die das Kalenderelement erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="44008-130">The mailbox user and attendee who created the calendar item.</span></span>  <br/> |
|<span data-ttu-id="44008-131">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="44008-131">Required</span></span>  <br/> |<span data-ttu-id="44008-132">Einen Postfachbenutzer an, der ein Erforderlicher Teilnehmer der Besprechung ist.</span><span class="sxs-lookup"><span data-stu-id="44008-132">A mailbox user who is a required attendee to the meeting.</span></span>  <br/> |
|<span data-ttu-id="44008-133">Optional</span><span class="sxs-lookup"><span data-stu-id="44008-133">Optional</span></span>  <br/> |<span data-ttu-id="44008-134">Einen Postfachbenutzer an, der einem optionalen Teilnehmer der Besprechung ist.</span><span class="sxs-lookup"><span data-stu-id="44008-134">A mailbox user who is an optional attendee to the meeting.</span></span>  <br/> |
|<span data-ttu-id="44008-135">Raum</span><span class="sxs-lookup"><span data-stu-id="44008-135">Room</span></span>  <br/> |<span data-ttu-id="44008-136">Ein Postfach-Entität, die eine Raum Ressource für die Besprechung verwendet darstellt.</span><span class="sxs-lookup"><span data-stu-id="44008-136">A mailbox entity that represents a room resource used for the meeting.</span></span>  <br/> |
|<span data-ttu-id="44008-137">Ressource</span><span class="sxs-lookup"><span data-stu-id="44008-137">Resource</span></span>  <br/> |<span data-ttu-id="44008-138">Eine Ressource wie TV oder für die Verwendung in der Besprechung geplant ist Projektor.</span><span class="sxs-lookup"><span data-stu-id="44008-138">A resource such as a TV or projector that is scheduled for use in the meeting.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="44008-139">Hinweise</span><span class="sxs-lookup"><span data-stu-id="44008-139">Remarks</span></span>

<span data-ttu-id="44008-140">Dieses Element ist ein erforderliches untergeordnetes Element des Elements [MailboxData](mailboxdata.md) .</span><span class="sxs-lookup"><span data-stu-id="44008-140">This element is a required child element of the [MailboxData](mailboxdata.md) element.</span></span> <span data-ttu-id="44008-141">Dieses Element kann nur einmal im Element [MailboxData](mailboxdata.md) auftreten.</span><span class="sxs-lookup"><span data-stu-id="44008-141">This element can only occur once in the [MailboxData](mailboxdata.md) element.</span></span> <span data-ttu-id="44008-142">Das Schema, das dieses Element beschreibt befindet sich im Verzeichnis /EWS/ des Computers, auf dem MicrosoftExchange Server 2007 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="44008-142">The schema that describes this element is located in the /EWS/ directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="44008-143">Der Typ des AttendeeType-Schema wird verwendet, um Teilnehmer für ein Kalenderelement darstellen.</span><span class="sxs-lookup"><span data-stu-id="44008-143">The AttendeeType schema type is used to represent attendees to a calendar item.</span></span> <span data-ttu-id="44008-144">Verwechseln Sie nicht dieses Element mit Elementen des Typs AttendeeType Schema.</span><span class="sxs-lookup"><span data-stu-id="44008-144">Do not confuse this element with elements of the AttendeeType schema type.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="44008-145">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="44008-145">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="44008-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="44008-146">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="44008-147">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="44008-147">Schema Name</span></span>  <br/> |<span data-ttu-id="44008-148">Schematypen</span><span class="sxs-lookup"><span data-stu-id="44008-148">Types schema</span></span>  <br/> |
|<span data-ttu-id="44008-149">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="44008-149">Validation File</span></span>  <br/> |<span data-ttu-id="44008-150">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="44008-150">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="44008-151">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="44008-151">Can be Empty</span></span>  <br/> |<span data-ttu-id="44008-152">False</span><span class="sxs-lookup"><span data-stu-id="44008-152">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="44008-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="44008-153">See also</span></span>

- [<span data-ttu-id="44008-154">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="44008-154">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="44008-155">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="44008-155">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
- [<span data-ttu-id="44008-156">Erste Benutzer Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="44008-156">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

