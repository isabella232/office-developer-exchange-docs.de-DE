---
title: GetUserAvailabilityRequest
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetUserAvailabilityRequest
api_type:
- schema
ms.assetid: 7906711b-80a1-42ae-8b33-26eeac036a5a
description: Das GetUserAvailabilityRequest-Element enthält die Argumente, die zum Abrufen von Informationen zur Verfügbarkeit der Benutzer verwendet. Dies ist eine Stammelements.
ms.openlocfilehash: 5440f739b09bfbe27ad97cba99c08756686594f7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19829683"
---
# <a name="getuseravailabilityrequest"></a><span data-ttu-id="2406c-104">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="2406c-104">GetUserAvailabilityRequest</span></span>

<span data-ttu-id="2406c-105">Das **GetUserAvailabilityRequest** -Element enthält die Argumente, die zum Abrufen von Informationen zur Verfügbarkeit der Benutzer verwendet.</span><span class="sxs-lookup"><span data-stu-id="2406c-105">The **GetUserAvailabilityRequest** element contains the arguments used to obtain user availability information.</span></span> <span data-ttu-id="2406c-106">Dies ist eine Stammelements.</span><span class="sxs-lookup"><span data-stu-id="2406c-106">This is a root element.</span></span> 
  
```xml
<GetUserAvailabilityRequest>
   <TimeZone>...</TimeZone>
   <MailboxDataArray>...</MailboxDataArray>
   <FreeBusyViewOptions>...</FreeBusyViewOptions>
   <SuggestionsViewOptions>...</SuggestionsViewOptions>
</GetUserAvailabilityRequest>
```

 <span data-ttu-id="2406c-107">**GetUserAvailabilityRequestType**</span><span class="sxs-lookup"><span data-stu-id="2406c-107">**GetUserAvailabilityRequestType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2406c-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="2406c-108">Attributes and elements</span></span>

<span data-ttu-id="2406c-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="2406c-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2406c-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="2406c-110">Attributes</span></span>

<span data-ttu-id="2406c-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="2406c-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2406c-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2406c-112">Child elements</span></span>

|<span data-ttu-id="2406c-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="2406c-113">**Element**</span></span>|<span data-ttu-id="2406c-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2406c-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2406c-115">TimeZone (Verfügbarkeit)</span><span class="sxs-lookup"><span data-stu-id="2406c-115">TimeZone (Availability)</span></span>](timezone-availability.md) <br/> |<span data-ttu-id="2406c-116">Enthält Elemente, die Informationen zur Zeitzone zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="2406c-116">Contains elements that identify time zone information.</span></span> <span data-ttu-id="2406c-117">Dieses Element enthält auch Informationen über den Wechsel zwischen Standardzeit und Sommerzeit.</span><span class="sxs-lookup"><span data-stu-id="2406c-117">This element also contains information about the transition between standard time and daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="2406c-118">MailboxDataArray</span><span class="sxs-lookup"><span data-stu-id="2406c-118">MailboxDataArray</span></span>](mailboxdataarray.md) <br/> |<span data-ttu-id="2406c-119">Enthält eine Liste der Postfächer, um Informationen zur Verfügbarkeit abzufragen.</span><span class="sxs-lookup"><span data-stu-id="2406c-119">Contains a list of mailboxes to query for availability information.</span></span>  <br/> |
|[<span data-ttu-id="2406c-120">FreeBusyViewOptions</span><span class="sxs-lookup"><span data-stu-id="2406c-120">FreeBusyViewOptions</span></span>](freebusyviewoptions.md) <br/> |<span data-ttu-id="2406c-121">Gibt den Typ des Frei/Gebucht-Informationen in der Antwort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2406c-121">Specifies the type of free/busy information returned in the response.</span></span>  <br/> |
|[<span data-ttu-id="2406c-122">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="2406c-122">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md) <br/> |<span data-ttu-id="2406c-123">Enthält die Optionen zum Abrufen von Besprechungsinformationen Vorschlag.</span><span class="sxs-lookup"><span data-stu-id="2406c-123">Contains the options for obtaining meeting suggestion information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2406c-124">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2406c-124">Parent elements</span></span>

<span data-ttu-id="2406c-125">Keine.</span><span class="sxs-lookup"><span data-stu-id="2406c-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2406c-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2406c-126">Remarks</span></span>

<span data-ttu-id="2406c-127">Das Schema, das dieses Element beschreibt befindet sich im Verzeichnis /EWS/ des Computers, auf dem Microsoft Exchange Server 2007 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="2406c-127">The schema that describes this element is located in the /EWS/ directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="2406c-128">Beispiel</span><span class="sxs-lookup"><span data-stu-id="2406c-128">Example</span></span>

<span data-ttu-id="2406c-129">Das folgende Beispiel zeigt eine Anforderung für Frei/Gebucht-Informationen.</span><span class="sxs-lookup"><span data-stu-id="2406c-129">The following example shows a request for free/busy information.</span></span>
  
```
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetUserAvailabilityRequest xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <TimeZone xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
        <Bias>480</Bias>
        <StandardTime>
          <Bias>0</Bias>
          <Time>02:00:00</Time>
          <DayOrder>5</DayOrder>
          <Month>10</Month>
          <DayOfWeek>Sunday</DayOfWeek>
        </StandardTime>
        <DaylightTime>
          <Bias>-60</Bias>
          <Time>02:00:00</Time>
          <DayOrder>1</DayOrder>
          <Month>4</Month>
          <DayOfWeek>Sunday</DayOfWeek>
        </DaylightTime>
      </TimeZone>
      <MailboxDataArray>
        <MailboxData xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
          <Email>
            <Name></Name>
            <Address>someone@exchangeserver.example.com</Address>
            <RoutingType>SMTP</RoutingType>
          </Email>
          <AttendeeType>Organizer</AttendeeType>
          <ExcludeConflicts>false</ExcludeConflicts>
          <ExcludeNonWorkingHours>false</ExcludeNonWorkingHours>
        </MailboxData>
      </MailboxDataArray>
      <FreeBusyViewOptions xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
        <TimeWindow>
          <StartTime>2006-02-06T00:00:00</StartTime>
          <EndTime>2006-02-30T23:59:59</EndTime>
        </TimeWindow>
        <MergedFreeBusyIntervalInMinutes>60</MergedFreeBusyIntervalInMinutes>
        <RequestedView>FreeBusyMerged</RequestedView>
      </FreeBusyViewOptions>
    </GetUserAvailabilityRequest>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a><span data-ttu-id="2406c-130">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="2406c-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2406c-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="2406c-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2406c-132">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="2406c-132">Schema Name</span></span>  <br/> |<span data-ttu-id="2406c-133">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="2406c-133">Messages schema</span></span>  <br/> |
|<span data-ttu-id="2406c-134">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="2406c-134">Validation File</span></span>  <br/> |<span data-ttu-id="2406c-135">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="2406c-135">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2406c-136">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="2406c-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="2406c-137">False</span><span class="sxs-lookup"><span data-stu-id="2406c-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2406c-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2406c-138">See also</span></span>



[<span data-ttu-id="2406c-139">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="2406c-139">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="2406c-140">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="2406c-140">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="2406c-141">Erste Benutzer Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="2406c-141">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

