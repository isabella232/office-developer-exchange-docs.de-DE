---
title: FreeBusyViewOptions
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FreeBusyViewOptions
api_type:
- schema
ms.assetid: c07f3ddb-874b-4d30-a60e-7e5c7793bb6f
description: Das FreeBusyViewOptions-Element gibt den Typ der Frei/Gebucht-Informationen in der Antwort zurückgegeben.
ms.openlocfilehash: 703fc6a3625d24cf874a785600e13ee4505b506f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758547"
---
# <a name="freebusyviewoptions"></a><span data-ttu-id="0c04d-103">FreeBusyViewOptions</span><span class="sxs-lookup"><span data-stu-id="0c04d-103">FreeBusyViewOptions</span></span>

<span data-ttu-id="0c04d-104">Das **FreeBusyViewOptions** -Element gibt den Typ der Frei/Gebucht-Informationen in der Antwort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0c04d-104">The **FreeBusyViewOptions** element specifies the type of free/busy information returned in the response.</span></span> 
  
[<span data-ttu-id="0c04d-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="0c04d-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
[<span data-ttu-id="0c04d-106">FreeBusyViewOptions</span><span class="sxs-lookup"><span data-stu-id="0c04d-106">FreeBusyViewOptions</span></span>](freebusyviewoptions.md)
  
```xml
<FreeBusyViewOptions>
   <TimeWindow>...</TimeWindow>
   <MergedFreeBusyIntervalInMinutes>...</MergedFreeBusyIntervalInMinutes>
<RequestedView>...</RequestedView>
</FreeBusyViewOptions>

```

 <span data-ttu-id="0c04d-107">**FreeBusyViewOptionsType**</span><span class="sxs-lookup"><span data-stu-id="0c04d-107">**FreeBusyViewOptionsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0c04d-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="0c04d-108">Attributes and elements</span></span>

<span data-ttu-id="0c04d-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="0c04d-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0c04d-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="0c04d-110">Attributes</span></span>

<span data-ttu-id="0c04d-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="0c04d-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0c04d-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0c04d-112">Child elements</span></span>

|<span data-ttu-id="0c04d-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="0c04d-113">**Element**</span></span>|<span data-ttu-id="0c04d-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0c04d-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0c04d-115">Zeitfenster</span><span class="sxs-lookup"><span data-stu-id="0c04d-115">TimeWindow</span></span>](timewindow.md) <br/> |<span data-ttu-id="0c04d-116">Gibt die Zeitspanne für die Verfügbarkeit Benutzerinformationen abgefragt.</span><span class="sxs-lookup"><span data-stu-id="0c04d-116">Identifies the time span queried for the user availability information.</span></span>  <br/> |
|[<span data-ttu-id="0c04d-117">MergedFreeBusyIntervalInMinutes</span><span class="sxs-lookup"><span data-stu-id="0c04d-117">MergedFreeBusyIntervalInMinutes</span></span>](mergedfreebusyintervalinminutes.md) <br/> |<span data-ttu-id="0c04d-118">Stellt den Zeitunterschied zwischen zwei aufeinanderfolgenden Slots in der Ansicht **FreeBusyMerged** .</span><span class="sxs-lookup"><span data-stu-id="0c04d-118">Represents the time difference between two successive slots in the **FreeBusyMerged** view.</span></span>  <br/> |
|[<span data-ttu-id="0c04d-119">RequestedView</span><span class="sxs-lookup"><span data-stu-id="0c04d-119">RequestedView</span></span>](requestedview.md) <br/> |<span data-ttu-id="0c04d-120">Definiert den Typ von Kalenderinformationen, die ein Client anfordert.</span><span class="sxs-lookup"><span data-stu-id="0c04d-120">Defines the type of calendar information that a client requests.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0c04d-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0c04d-121">Parent elements</span></span>

|<span data-ttu-id="0c04d-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="0c04d-122">**Element**</span></span>|<span data-ttu-id="0c04d-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0c04d-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0c04d-124">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="0c04d-124">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md) <br/> |<span data-ttu-id="0c04d-125">Enthält die Argumente, die zum Abrufen von Informationen zur Verfügbarkeit der Benutzer verwendet.</span><span class="sxs-lookup"><span data-stu-id="0c04d-125">Contains the arguments used to obtain user availability information.</span></span> <span data-ttu-id="0c04d-126">Dies ist eine Stammelements.</span><span class="sxs-lookup"><span data-stu-id="0c04d-126">This is a root element.</span></span>  <br/> <span data-ttu-id="0c04d-127">Es folgt der XPath-Ausdruck für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="0c04d-127">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0c04d-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0c04d-128">Remarks</span></span>

<span data-ttu-id="0c04d-129">Dieses Element ist nicht erforderlich, und kann nur einmal auftreten, wenn verwendet.</span><span class="sxs-lookup"><span data-stu-id="0c04d-129">This element is not required and can only occur once if used.</span></span> <span data-ttu-id="0c04d-130">Dieser Wert kann null sein, wenn der Wert des Elements [SuggestionsViewOptions](suggestionsviewoptions.md) nicht null ist.</span><span class="sxs-lookup"><span data-stu-id="0c04d-130">This value can be null if the value of the [SuggestionsViewOptions](suggestionsviewoptions.md) element is not null.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="0c04d-131">Das Schema, das dieses Element beschreibt befindet sich im Verzeichnis /epi/ des Computers, auf dem Microsoft® Exchange Server 2007 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="0c04d-131">The schema that describes this element is located in the /epi/ directory of the computer that is running Microsoft® Exchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="example"></a><span data-ttu-id="0c04d-132">Beispiel</span><span class="sxs-lookup"><span data-stu-id="0c04d-132">Example</span></span>

<span data-ttu-id="0c04d-133">Das folgende Beispiel ruft eine Liste von Besprechungen und einem Stream Frei/Gebucht-Informationen alle 60 Minuten.</span><span class="sxs-lookup"><span data-stu-id="0c04d-133">The following example obtains a list of meetings and a free/busy stream in 60-minute intervals.</span></span>
  
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
            <Address>someone@ExServer.example.com</Address>
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
          <EndTime>2006-02-25T23:59:59</EndTime>
        </TimeWindow>
        <MergedFreeBusyIntervalInMinutes>60</MergedFreeBusyIntervalInMinutes>
        <RequestedView>FreeBusyMerged</RequestedView>
      </FreeBusyViewOptions>
    </GetUserAvailabilityRequest>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a><span data-ttu-id="0c04d-134">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="0c04d-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0c04d-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="0c04d-135">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0c04d-136">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="0c04d-136">Schema Name</span></span>  <br/> |<span data-ttu-id="0c04d-137">Schematypen</span><span class="sxs-lookup"><span data-stu-id="0c04d-137">Types schema</span></span>  <br/> |
|<span data-ttu-id="0c04d-138">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="0c04d-138">Validation File</span></span>  <br/> |<span data-ttu-id="0c04d-139">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0c04d-139">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0c04d-140">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="0c04d-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="0c04d-141">False</span><span class="sxs-lookup"><span data-stu-id="0c04d-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0c04d-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0c04d-142">See also</span></span>



[<span data-ttu-id="0c04d-143">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="0c04d-143">GetUserAvailability operation</span></span>](getuseravailability-operation.md)


[<span data-ttu-id="0c04d-144">Erste Benutzer Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="0c04d-144">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

