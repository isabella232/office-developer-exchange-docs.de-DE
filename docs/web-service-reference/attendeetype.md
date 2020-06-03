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
description: Das AttendeeType-Element stellt den Typ des Teilnehmers dar, der im e-Mail-Element (Epost) identifiziert wird. Dieses Element wird in Anforderungen für Besprechungsvorschläge verwendet.
ms.openlocfilehash: 104b9f38cc891310ecb47c0b47837a912ced6ab7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462297"
---
# <a name="attendeetype"></a><span data-ttu-id="3b539-104">AttendeeType</span><span class="sxs-lookup"><span data-stu-id="3b539-104">AttendeeType</span></span>

<span data-ttu-id="3b539-105">Das **AttendeeType** -Element stellt den Typ des Teilnehmers dar, der im [e-Mail-Element (Epost)](email-emailaddresstype.md) identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="3b539-105">The **AttendeeType** element represents the type of attendee that is identified in the [Email (EmailAddressType)](email-emailaddresstype.md) element.</span></span> <span data-ttu-id="3b539-106">Dieses Element wird in Anforderungen für Besprechungsvorschläge verwendet.</span><span class="sxs-lookup"><span data-stu-id="3b539-106">This element is used in requests for meeting suggestions.</span></span> 
  
- [<span data-ttu-id="3b539-107">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="3b539-107">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
- [<span data-ttu-id="3b539-108">MailboxDataArray</span><span class="sxs-lookup"><span data-stu-id="3b539-108">MailboxDataArray</span></span>](mailboxdataarray.md)
  
- [<span data-ttu-id="3b539-109">MailboxData</span><span class="sxs-lookup"><span data-stu-id="3b539-109">MailboxData</span></span>](mailboxdata.md)
  
- [<span data-ttu-id="3b539-110">AttendeeType</span><span class="sxs-lookup"><span data-stu-id="3b539-110">AttendeeType</span></span>](attendeetype.md)
  
```xml
<AttendeeType>Organizer or Required or Optional or Room or Resource</AttendeeType>
```

 <span data-ttu-id="3b539-111">**MeetingAttendeeType**</span><span class="sxs-lookup"><span data-stu-id="3b539-111">**MeetingAttendeeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3b539-112">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3b539-112">Attributes and elements</span></span>

<span data-ttu-id="3b539-113">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="3b539-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3b539-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="3b539-114">Attributes</span></span>

<span data-ttu-id="3b539-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="3b539-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3b539-116">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3b539-116">Child elements</span></span>

<span data-ttu-id="3b539-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="3b539-117">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3b539-118">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3b539-118">Parent elements</span></span>

|<span data-ttu-id="3b539-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="3b539-119">**Element**</span></span>|<span data-ttu-id="3b539-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3b539-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3b539-121">MailboxData</span><span class="sxs-lookup"><span data-stu-id="3b539-121">MailboxData</span></span>](mailboxdata.md) <br/> |<span data-ttu-id="3b539-122">Stellt einen einzelnen Postfachbenutzer und Optionen für den Typ der Daten dar, die über den Postfachbenutzer zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3b539-122">Represents an individual mailbox user and options for the type of data to be returned about the mailbox user.</span></span>  <br/> <span data-ttu-id="3b539-123">Es folgt der XPath für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="3b539-123">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/MailboxDataArray[i]/MailboxData` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3b539-124">Textwert</span><span class="sxs-lookup"><span data-stu-id="3b539-124">Text value</span></span>

<span data-ttu-id="3b539-125">Für dieses Element ist ein Textwert erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3b539-125">A text value is required for this element.</span></span> <span data-ttu-id="3b539-126">In der folgenden Tabelle sind die möglichen Werte für dieses Element aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="3b539-126">The following table lists the possible values for this element.</span></span>
  
|<span data-ttu-id="3b539-127">**Wert**</span><span class="sxs-lookup"><span data-stu-id="3b539-127">**Value**</span></span>|<span data-ttu-id="3b539-128">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3b539-128">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3b539-129">Organisator</span><span class="sxs-lookup"><span data-stu-id="3b539-129">Organizer</span></span>  <br/> |<span data-ttu-id="3b539-130">Der Postfachbenutzer und der Teilnehmer, der das Kalenderelement erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="3b539-130">The mailbox user and attendee who created the calendar item.</span></span>  <br/> |
|<span data-ttu-id="3b539-131">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="3b539-131">Required</span></span>  <br/> |<span data-ttu-id="3b539-132">Ein Postfachbenutzer, der ein Erforderlicher Teilnehmer für die Besprechung ist.</span><span class="sxs-lookup"><span data-stu-id="3b539-132">A mailbox user who is a required attendee to the meeting.</span></span>  <br/> |
|<span data-ttu-id="3b539-133">Optional</span><span class="sxs-lookup"><span data-stu-id="3b539-133">Optional</span></span>  <br/> |<span data-ttu-id="3b539-134">Ein Postfachbenutzer, der ein optionaler Teilnehmer für die Besprechung ist.</span><span class="sxs-lookup"><span data-stu-id="3b539-134">A mailbox user who is an optional attendee to the meeting.</span></span>  <br/> |
|<span data-ttu-id="3b539-135">Raum</span><span class="sxs-lookup"><span data-stu-id="3b539-135">Room</span></span>  <br/> |<span data-ttu-id="3b539-136">Eine Post Fach Entität, die eine Raum Ressource darstellt, die für die Besprechung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3b539-136">A mailbox entity that represents a room resource used for the meeting.</span></span>  <br/> |
|<span data-ttu-id="3b539-137">Ressource</span><span class="sxs-lookup"><span data-stu-id="3b539-137">Resource</span></span>  <br/> |<span data-ttu-id="3b539-138">Eine Ressource wie ein Fernsehgerät oder Projektor, die für die Besprechung geplant ist.</span><span class="sxs-lookup"><span data-stu-id="3b539-138">A resource such as a TV or projector that is scheduled for use in the meeting.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3b539-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3b539-139">Remarks</span></span>

<span data-ttu-id="3b539-140">Dieses Element ist ein erforderliches untergeordnetes Element des [MailboxData](mailboxdata.md) -Elements.</span><span class="sxs-lookup"><span data-stu-id="3b539-140">This element is a required child element of the [MailboxData](mailboxdata.md) element.</span></span> <span data-ttu-id="3b539-141">Dieses Element kann nur einmal im [MailboxData](mailboxdata.md) -Element vorkommen.</span><span class="sxs-lookup"><span data-stu-id="3b539-141">This element can only occur once in the [MailboxData](mailboxdata.md) element.</span></span> <span data-ttu-id="3b539-142">Das Schema, das dieses Element beschreibt, befindet sich im Verzeichnis/EWS/"aus des Computers mit Microsoft Exchange Server 2007, auf dem die Client Zugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="3b539-142">The schema that describes this element is located in the /EWS/ directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="3b539-143">Der AttendeeType-Schematyp wird zum Darstellen von Teilnehmern eines Kalenderelements verwendet.</span><span class="sxs-lookup"><span data-stu-id="3b539-143">The AttendeeType schema type is used to represent attendees to a calendar item.</span></span> <span data-ttu-id="3b539-144">Verwechseln Sie dieses Element nicht mit Elementen des AttendeeType-Schematyps.</span><span class="sxs-lookup"><span data-stu-id="3b539-144">Do not confuse this element with elements of the AttendeeType schema type.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="3b539-145">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="3b539-145">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3b539-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="3b539-146">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3b539-147">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="3b539-147">Schema Name</span></span>  <br/> |<span data-ttu-id="3b539-148">Schematypen</span><span class="sxs-lookup"><span data-stu-id="3b539-148">Types schema</span></span>  <br/> |
|<span data-ttu-id="3b539-149">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="3b539-149">Validation File</span></span>  <br/> |<span data-ttu-id="3b539-150">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3b539-150">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3b539-151">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="3b539-151">Can be Empty</span></span>  <br/> |<span data-ttu-id="3b539-152">False</span><span class="sxs-lookup"><span data-stu-id="3b539-152">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3b539-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3b539-153">See also</span></span>

- [<span data-ttu-id="3b539-154">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="3b539-154">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="3b539-155">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="3b539-155">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
- [<span data-ttu-id="3b539-156">Verfügbarkeit von Benutzern wird abgerufen</span><span class="sxs-lookup"><span data-stu-id="3b539-156">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

