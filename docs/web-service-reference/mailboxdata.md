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
description: Das MailboxData-Element stellt einen einzelnen Postfachbenutzer und Optionen für den Typ der Daten dar, die über den Postfachbenutzer zurückgegeben werden sollen.
ms.openlocfilehash: bfcb8c01d40af81097c7d9868006fe9b7b5519d4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467249"
---
# <a name="mailboxdata"></a><span data-ttu-id="d3dbe-103">MailboxData</span><span class="sxs-lookup"><span data-stu-id="d3dbe-103">MailboxData</span></span>

<span data-ttu-id="d3dbe-104">Das **MailboxData** -Element stellt einen einzelnen Postfachbenutzer und Optionen für den Typ der Daten dar, die über den Postfachbenutzer zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d3dbe-104">The **MailboxData** element represents an individual mailbox user and options for the type of data to be returned about the mailbox user.</span></span> 
  
- [<span data-ttu-id="d3dbe-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="d3dbe-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
- [<span data-ttu-id="d3dbe-106">MailboxDataArray</span><span class="sxs-lookup"><span data-stu-id="d3dbe-106">MailboxDataArray</span></span>](mailboxdataarray.md)
  
- [<span data-ttu-id="d3dbe-107">MailboxData</span><span class="sxs-lookup"><span data-stu-id="d3dbe-107">MailboxData</span></span>](mailboxdata.md)
  
```xml
<MailboxData>
   <Email>...</Email>
   <AttendeeType>...</AttendeeType>
   <ExcludeConflicts>...</ExcludeConflicts>
<MailboxData>
```

<span data-ttu-id="d3dbe-108">**MailboxData**</span><span class="sxs-lookup"><span data-stu-id="d3dbe-108">**MailboxData**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="d3dbe-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d3dbe-109">Attributes and elements</span></span>

<span data-ttu-id="d3dbe-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d3dbe-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d3dbe-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="d3dbe-111">Attributes</span></span>

<span data-ttu-id="d3dbe-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="d3dbe-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d3dbe-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d3dbe-113">Child elements</span></span>

|<span data-ttu-id="d3dbe-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="d3dbe-114">**Element**</span></span>|<span data-ttu-id="d3dbe-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d3dbe-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d3dbe-116">E-Mail (e-Mail-Adresse)</span><span class="sxs-lookup"><span data-stu-id="d3dbe-116">Email (EmailAddressType)</span></span>](email-emailaddresstype.md) <br/> |<span data-ttu-id="d3dbe-117">Stellt den Postfachbenutzer für eine GetUserAvailability-Abfrage dar.</span><span class="sxs-lookup"><span data-stu-id="d3dbe-117">Represents the mailbox user for a GetUserAvailability query.</span></span>  <br/> |
|[<span data-ttu-id="d3dbe-118">AttendeeType</span><span class="sxs-lookup"><span data-stu-id="d3dbe-118">AttendeeType</span></span>](attendeetype.md) <br/> |<span data-ttu-id="d3dbe-119">Stellt den Typ des Teilnehmers dar, der im [e-Mail-](email-emailaddresstype.md) Element angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="d3dbe-119">Represents the type of attendee identified in the [Email (EmailAddressType)](email-emailaddresstype.md) element.</span></span> <span data-ttu-id="d3dbe-120">Dies wird in Anforderungen für Besprechungsvorschläge verwendet.</span><span class="sxs-lookup"><span data-stu-id="d3dbe-120">This is used in requests for meeting suggestions.</span></span>  <br/> |
|[<span data-ttu-id="d3dbe-121">ExcludeConflicts</span><span class="sxs-lookup"><span data-stu-id="d3dbe-121">ExcludeConflicts</span></span>](excludeconflicts.md) <br/> |<span data-ttu-id="d3dbe-122">Gibt an, ob vorgeschlagene Zeiten für Kalenderzeiten zurückgegeben werden sollen, die in Konflikt zwischen den Teilnehmern liegen.</span><span class="sxs-lookup"><span data-stu-id="d3dbe-122">Specifies whether to return suggested times for calendar times that conflict among the attendees.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d3dbe-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d3dbe-123">Parent elements</span></span>

|<span data-ttu-id="d3dbe-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="d3dbe-124">**Element**</span></span>|<span data-ttu-id="d3dbe-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d3dbe-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d3dbe-126">MailboxDataArray</span><span class="sxs-lookup"><span data-stu-id="d3dbe-126">MailboxDataArray</span></span>](mailboxdataarray.md) <br/> |<span data-ttu-id="d3dbe-127">Enthält eine Liste der Postfächer, die nach Verfügbarkeitsinformationen abgefragt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d3dbe-127">Contains a list of mailboxes to query for availability information.</span></span>  <br/> <span data-ttu-id="d3dbe-128">Es folgt der XPath für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="d3dbe-128">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/MailboxDataArray[i]` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d3dbe-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d3dbe-129">Remarks</span></span>

<span data-ttu-id="d3dbe-130">Eine Clientanwendung kann ein bis viele **MailboxData** -Elemente definieren.</span><span class="sxs-lookup"><span data-stu-id="d3dbe-130">A client application can define one to many **MailboxData** elements.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d3dbe-131">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Exchange Server 2007 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="d3dbe-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="example"></a><span data-ttu-id="d3dbe-132">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d3dbe-132">Example</span></span>

```xml
<MailboxDataArray>
  <MailboxData xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="element-information"></a><span data-ttu-id="d3dbe-133">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="d3dbe-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d3dbe-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="d3dbe-134">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d3dbe-135">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d3dbe-135">Schema Name</span></span>  <br/> |<span data-ttu-id="d3dbe-136">Schematypen</span><span class="sxs-lookup"><span data-stu-id="d3dbe-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="d3dbe-137">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d3dbe-137">Validation File</span></span>  <br/> |<span data-ttu-id="d3dbe-138">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d3dbe-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d3dbe-139">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d3dbe-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="d3dbe-140">False</span><span class="sxs-lookup"><span data-stu-id="d3dbe-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d3dbe-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d3dbe-141">See also</span></span>

- [<span data-ttu-id="d3dbe-142">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d3dbe-142">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="d3dbe-143">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="d3dbe-143">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
- [<span data-ttu-id="d3dbe-144">Verfügbarkeit von Benutzern wird abgerufen</span><span class="sxs-lookup"><span data-stu-id="d3dbe-144">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

