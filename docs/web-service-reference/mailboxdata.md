---
title: MailboxData
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MailboxData
api_type:
- schema
ms.assetid: e9e3f50c-5a7b-49c7-a9ea-117959c08352
description: Das MailboxData-Element stellt ein einzelnes Postfachbenutzer und Optionen für den Typ der Daten zu den Postfachbenutzer zurückgegeben werden soll.
ms.openlocfilehash: df60294e7d83b1459e5cca7d75c2b6b4bb9d931d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830281"
---
# <a name="mailboxdata"></a><span data-ttu-id="f61e5-103">MailboxData</span><span class="sxs-lookup"><span data-stu-id="f61e5-103">MailboxData</span></span>

<span data-ttu-id="f61e5-104">Das **MailboxData** -Element stellt ein einzelnes Postfachbenutzer und Optionen für den Typ der Daten zu den Postfachbenutzer zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="f61e5-104">The **MailboxData** element represents an individual mailbox user and options for the type of data to be returned about the mailbox user.</span></span> 
  
- [<span data-ttu-id="f61e5-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="f61e5-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
- [<span data-ttu-id="f61e5-106">MailboxDataArray</span><span class="sxs-lookup"><span data-stu-id="f61e5-106">MailboxDataArray</span></span>](mailboxdataarray.md)
  
- [<span data-ttu-id="f61e5-107">MailboxData</span><span class="sxs-lookup"><span data-stu-id="f61e5-107">MailboxData</span></span>](mailboxdata.md)
  
```xml
<MailboxData>
   <Email>...</Email>
   <AttendeeType>...</AttendeeType>
   <ExcludeConflicts>...</ExcludeConflicts>
<MailboxData>
```

<span data-ttu-id="f61e5-108">**MailboxData**</span><span class="sxs-lookup"><span data-stu-id="f61e5-108">**MailboxData**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="f61e5-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f61e5-109">Attributes and elements</span></span>

<span data-ttu-id="f61e5-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f61e5-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f61e5-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="f61e5-111">Attributes</span></span>

<span data-ttu-id="f61e5-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="f61e5-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f61e5-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f61e5-113">Child elements</span></span>

|<span data-ttu-id="f61e5-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="f61e5-114">**Element**</span></span>|<span data-ttu-id="f61e5-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f61e5-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f61e5-116">E-Mail (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="f61e5-116">Email (EmailAddressType)</span></span>](email-emailaddresstype.md) <br/> |<span data-ttu-id="f61e5-117">Stellt den Postfachbenutzer für eine GetUserAvailability-Abfrage dar.</span><span class="sxs-lookup"><span data-stu-id="f61e5-117">Represents the mailbox user for a GetUserAvailability query.</span></span>  <br/> |
|[<span data-ttu-id="f61e5-118">AttendeeType</span><span class="sxs-lookup"><span data-stu-id="f61e5-118">AttendeeType</span></span>](attendeetype.md) <br/> |<span data-ttu-id="f61e5-119">Stellt den Typ des Teilnehmers [(EmailAddressType) E-Mail](email-emailaddresstype.md) -Element identifiziert.</span><span class="sxs-lookup"><span data-stu-id="f61e5-119">Represents the type of attendee identified in the [Email (EmailAddressType)](email-emailaddresstype.md) element.</span></span> <span data-ttu-id="f61e5-120">Dies wird in Anforderungen für Besprechungsvorschläge verwendet.</span><span class="sxs-lookup"><span data-stu-id="f61e5-120">This is used in requests for meeting suggestions.</span></span>  <br/> |
|[<span data-ttu-id="f61e5-121">ExcludeConflicts</span><span class="sxs-lookup"><span data-stu-id="f61e5-121">ExcludeConflicts</span></span>](excludeconflicts.md) <br/> |<span data-ttu-id="f61e5-122">Gibt an, ob zurückzugebenden vorgeschlagenen Zeiten für Kalender Versuche, die auf der Teilnehmerliste in Konflikt stehen.</span><span class="sxs-lookup"><span data-stu-id="f61e5-122">Specifies whether to return suggested times for calendar times that conflict among the attendees.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f61e5-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f61e5-123">Parent elements</span></span>

|<span data-ttu-id="f61e5-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="f61e5-124">**Element**</span></span>|<span data-ttu-id="f61e5-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f61e5-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f61e5-126">MailboxDataArray</span><span class="sxs-lookup"><span data-stu-id="f61e5-126">MailboxDataArray</span></span>](mailboxdataarray.md) <br/> |<span data-ttu-id="f61e5-127">Enthält eine Liste der Postfächer, um Informationen zur Verfügbarkeit abzufragen.</span><span class="sxs-lookup"><span data-stu-id="f61e5-127">Contains a list of mailboxes to query for availability information.</span></span>  <br/> <span data-ttu-id="f61e5-128">Es folgt der XPath-Ausdruck für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="f61e5-128">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/MailboxDataArray[i]` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f61e5-129">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f61e5-129">Remarks</span></span>

<span data-ttu-id="f61e5-130">Eine Clientanwendung kann auf viele **MailboxData** -Elemente definieren.</span><span class="sxs-lookup"><span data-stu-id="f61e5-130">A client application can define one to many **MailboxData** elements.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f61e5-131">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Exchange Server 2007 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="f61e5-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="example"></a><span data-ttu-id="f61e5-132">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f61e5-132">Example</span></span>

```xml
<MailboxDataArray>
  <MailboxData xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
    <Email>
      <Name></Name>
      <Address>someone@ExServer.example.com</Address>
      <RoutingType>SMTP</RoutingType>
    </Email>
    <AttendeeType>Organizer</AttendeeType>
    <ExcludeConflicts>false</ExcludeConflicts>
  </MailboxData>
</MailboxDataArray>
```

## <a name="element-information"></a><span data-ttu-id="f61e5-133">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="f61e5-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f61e5-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="f61e5-134">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f61e5-135">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f61e5-135">Schema Name</span></span>  <br/> |<span data-ttu-id="f61e5-136">Schematypen</span><span class="sxs-lookup"><span data-stu-id="f61e5-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="f61e5-137">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f61e5-137">Validation File</span></span>  <br/> |<span data-ttu-id="f61e5-138">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f61e5-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f61e5-139">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="f61e5-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="f61e5-140">False</span><span class="sxs-lookup"><span data-stu-id="f61e5-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f61e5-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f61e5-141">See also</span></span>

- [<span data-ttu-id="f61e5-142">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f61e5-142">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="f61e5-143">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="f61e5-143">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
- [<span data-ttu-id="f61e5-144">Erste Benutzer Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="f61e5-144">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

