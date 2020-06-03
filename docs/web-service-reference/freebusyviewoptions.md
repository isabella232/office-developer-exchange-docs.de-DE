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
description: Das FreeBusyViewOptions-Element gibt den Typ der Frei/Gebucht-Informationen an, die in der Antwort zurückgegeben werden.
ms.openlocfilehash: b67d3f461e0edaa82f074f75b0c1c54efc8af4d0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459574"
---
# <a name="freebusyviewoptions"></a><span data-ttu-id="b945e-103">FreeBusyViewOptions</span><span class="sxs-lookup"><span data-stu-id="b945e-103">FreeBusyViewOptions</span></span>

<span data-ttu-id="b945e-104">Das **FreeBusyViewOptions** -Element gibt den Typ der Frei/Gebucht-Informationen an, die in der Antwort zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b945e-104">The **FreeBusyViewOptions** element specifies the type of free/busy information returned in the response.</span></span> 
  
[<span data-ttu-id="b945e-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="b945e-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
[<span data-ttu-id="b945e-106">FreeBusyViewOptions</span><span class="sxs-lookup"><span data-stu-id="b945e-106">FreeBusyViewOptions</span></span>](freebusyviewoptions.md)
  
```xml
<FreeBusyViewOptions>
   <TimeWindow>...</TimeWindow>
   <MergedFreeBusyIntervalInMinutes>...</MergedFreeBusyIntervalInMinutes>
<RequestedView>...</RequestedView>
</FreeBusyViewOptions>

```

 <span data-ttu-id="b945e-107">**FreeBusyViewOptionsType**</span><span class="sxs-lookup"><span data-stu-id="b945e-107">**FreeBusyViewOptionsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b945e-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b945e-108">Attributes and elements</span></span>

<span data-ttu-id="b945e-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b945e-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b945e-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="b945e-110">Attributes</span></span>

<span data-ttu-id="b945e-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="b945e-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b945e-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b945e-112">Child elements</span></span>

|<span data-ttu-id="b945e-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="b945e-113">**Element**</span></span>|<span data-ttu-id="b945e-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b945e-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b945e-115">TimeWindow</span><span class="sxs-lookup"><span data-stu-id="b945e-115">TimeWindow</span></span>](timewindow.md) <br/> |<span data-ttu-id="b945e-116">Gibt den Zeitraum an, der für die Informationen zur Benutzerverfügbarkeit abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="b945e-116">Identifies the time span queried for the user availability information.</span></span>  <br/> |
|[<span data-ttu-id="b945e-117">MergedFreeBusyIntervalInMinutes</span><span class="sxs-lookup"><span data-stu-id="b945e-117">MergedFreeBusyIntervalInMinutes</span></span>](mergedfreebusyintervalinminutes.md) <br/> |<span data-ttu-id="b945e-118">Stellt den Zeitunterschied zwischen zwei aufeinanderfolgenden Slots in der **FreeBusyMerged** -Ansicht dar.</span><span class="sxs-lookup"><span data-stu-id="b945e-118">Represents the time difference between two successive slots in the **FreeBusyMerged** view.</span></span>  <br/> |
|[<span data-ttu-id="b945e-119">RequestedView</span><span class="sxs-lookup"><span data-stu-id="b945e-119">RequestedView</span></span>](requestedview.md) <br/> |<span data-ttu-id="b945e-120">Definiert den Typ von Kalenderinformationen, die von einem Client angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="b945e-120">Defines the type of calendar information that a client requests.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b945e-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b945e-121">Parent elements</span></span>

|<span data-ttu-id="b945e-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="b945e-122">**Element**</span></span>|<span data-ttu-id="b945e-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b945e-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b945e-124">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="b945e-124">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md) <br/> |<span data-ttu-id="b945e-125">Enthält die Argumente, die zum Abrufen von Informationen zur Benutzerverfügbarkeit verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b945e-125">Contains the arguments used to obtain user availability information.</span></span> <span data-ttu-id="b945e-126">Dies ist ein Stammelement.</span><span class="sxs-lookup"><span data-stu-id="b945e-126">This is a root element.</span></span>  <br/> <span data-ttu-id="b945e-127">Es folgt der XPath für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="b945e-127">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b945e-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b945e-128">Remarks</span></span>

<span data-ttu-id="b945e-129">Dieses Element ist nicht erforderlich und kann nur einmal auftreten, wenn es verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b945e-129">This element is not required and can only occur once if used.</span></span> <span data-ttu-id="b945e-130">Dieser Wert kann NULL sein, wenn der Wert des [SuggestionsViewOptions](suggestionsviewoptions.md) -Elements nicht NULL ist.</span><span class="sxs-lookup"><span data-stu-id="b945e-130">This value can be null if the value of the [SuggestionsViewOptions](suggestionsviewoptions.md) element is not null.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="b945e-131">Das Schema, das dieses Element beschreibt, befindet sich im/EPI/-Verzeichnis des Computers, auf dem Microsoft® Exchange Server 2007 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="b945e-131">The schema that describes this element is located in the /epi/ directory of the computer that is running Microsoft® Exchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="example"></a><span data-ttu-id="b945e-132">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b945e-132">Example</span></span>

<span data-ttu-id="b945e-133">Im folgenden Beispiel wird eine Liste der Besprechungen und eines frei/gebucht-Streams in 60-Minuten-Intervallen abgerufen.</span><span class="sxs-lookup"><span data-stu-id="b945e-133">The following example obtains a list of meetings and a free/busy stream in 60-minute intervals.</span></span>
  
```
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetUserAvailabilityRequest xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <TimeZone xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
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
        <MailboxData xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
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
      <FreeBusyViewOptions xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="element-information"></a><span data-ttu-id="b945e-134">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="b945e-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b945e-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="b945e-135">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b945e-136">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b945e-136">Schema Name</span></span>  <br/> |<span data-ttu-id="b945e-137">Schematypen</span><span class="sxs-lookup"><span data-stu-id="b945e-137">Types schema</span></span>  <br/> |
|<span data-ttu-id="b945e-138">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b945e-138">Validation File</span></span>  <br/> |<span data-ttu-id="b945e-139">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b945e-139">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b945e-140">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="b945e-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="b945e-141">False</span><span class="sxs-lookup"><span data-stu-id="b945e-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b945e-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b945e-142">See also</span></span>



[<span data-ttu-id="b945e-143">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="b945e-143">GetUserAvailability operation</span></span>](getuseravailability-operation.md)


[<span data-ttu-id="b945e-144">Verfügbarkeit von Benutzern wird abgerufen</span><span class="sxs-lookup"><span data-stu-id="b945e-144">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

