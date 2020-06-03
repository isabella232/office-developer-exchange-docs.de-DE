---
title: GetServerTimeZones-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetServerTimeZones
api_type:
- schema
ms.assetid: 680173e1-e916-466b-b573-5a3182316345
description: Der GetServerTimeZones-Vorgang gibt Informationen aus den Zeitzonendefinitionen zurück, die auf einem Exchange-Server verfügbar sind.
ms.openlocfilehash: 1afe7fe13501af4a14f72c731703fe41e1f33049
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460540"
---
# <a name="getservertimezones-operation"></a><span data-ttu-id="ad67f-103">GetServerTimeZones-Vorgang</span><span class="sxs-lookup"><span data-stu-id="ad67f-103">GetServerTimeZones operation</span></span>

<span data-ttu-id="ad67f-104">Der **GetServerTimeZones** -Vorgang gibt Informationen aus den Zeitzonendefinitionen zurück, die auf einem Exchange-Server verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="ad67f-104">The **GetServerTimeZones** operation returns information from time zone definitions that are available on an Exchange server.</span></span> 
  
## <a name="soap-headers"></a><span data-ttu-id="ad67f-105">SOAP-Header</span><span class="sxs-lookup"><span data-stu-id="ad67f-105">SOAP Headers</span></span>

<span data-ttu-id="ad67f-106">Der **GetServerTimeZones** -Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt und beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="ad67f-106">The **GetServerTimeZones** operation can use the SOAP headers that are listed and described in the following table.</span></span> 
  
|<span data-ttu-id="ad67f-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="ad67f-107">**Header**</span></span>|<span data-ttu-id="ad67f-108">**Element**</span><span class="sxs-lookup"><span data-stu-id="ad67f-108">**Element**</span></span>|<span data-ttu-id="ad67f-109">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ad67f-109">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ad67f-110">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="ad67f-110">MailboxCulture</span></span>  <br/> |[<span data-ttu-id="ad67f-111">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="ad67f-111">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="ad67f-112">Gibt die RFC3066-Kultur an, die für den Zugriff auf das Postfach verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ad67f-112">Identifies the RFC3066 culture to be used to access the mailbox.</span></span>  <br/> |
|<span data-ttu-id="ad67f-113">RequestVersion</span><span class="sxs-lookup"><span data-stu-id="ad67f-113">RequestVersion</span></span>  <br/> |[<span data-ttu-id="ad67f-114">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="ad67f-114">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="ad67f-115">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="ad67f-115">Identifies the schema version for the operation request.</span></span>  <br/> |
|<span data-ttu-id="ad67f-116">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="ad67f-116">ServerVersion</span></span>  <br/> |[<span data-ttu-id="ad67f-117">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="ad67f-117">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="ad67f-118">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="ad67f-118">Identifies the version of the server that responded to the request.</span></span>  <br/> |
   
## <a name="getservertimezones-request-examples"></a><span data-ttu-id="ad67f-119">GetServerTimeZones-Anforderungs Beispiele</span><span class="sxs-lookup"><span data-stu-id="ad67f-119">GetServerTimeZones request examples</span></span>

### <a name="getting-the-name-and-identifier-of-each-time-zone"></a><span data-ttu-id="ad67f-120">Aufrufen des Namens und der ID jeder Zeitzone</span><span class="sxs-lookup"><span data-stu-id="ad67f-120">Getting the Name and Identifier of Each Time Zone</span></span>

<span data-ttu-id="ad67f-121">Im folgenden Codebeispiel wird gezeigt, wie der Name und der Bezeichner für die Zeit Zonen Eastern Standard Time und Pacific Standard Time abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="ad67f-121">The following code example shows how to retrieve the name and identifier for the Eastern Standard Time and Pacific Standard Time time zones.</span></span>
  
### <a name="code"></a><span data-ttu-id="ad67f-122">Code</span><span class="sxs-lookup"><span data-stu-id="ad67f-122">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010"/>
  </soap:Header>
  <soap:Body>
    <m:GetServerTimeZones ReturnFullTimeZoneData="false">
      <m:Ids>
        <t:Id>Eastern Standard Time</Id>
        <t:Id>Pacific Standard Time</Id>
      </m:Ids>
    </m:GetServerTimeZones>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="ad67f-123">Comments</span><span class="sxs-lookup"><span data-stu-id="ad67f-123">Comments</span></span>

<span data-ttu-id="ad67f-124">Jedes [ID-Element (TimeZone)](id-timezone.md) enthält den Bezeichner einer Zeitzonendefinition, die angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="ad67f-124">Each [Id (TimeZone)](id-timezone.md) element contains the identifier of a time zone definition that is being requested.</span></span> <span data-ttu-id="ad67f-125">Wenn Sie Informationen zu allen Zeitzonen anfordern möchten, lassen Sie das [IDs](ids.md) -Element aus der Anforderung weglassen.</span><span class="sxs-lookup"><span data-stu-id="ad67f-125">To request information for all time zones, omit the [Ids](ids.md) element from the request.</span></span> 
  
### <a name="getting-the-full-definition-of-each-time-zone"></a><span data-ttu-id="ad67f-126">Aufrufen der vollständigen Definition jeder Zeitzone</span><span class="sxs-lookup"><span data-stu-id="ad67f-126">Getting the Full Definition of Each Time Zone</span></span>

<span data-ttu-id="ad67f-127">Im folgenden Codebeispiel wird gezeigt, wie Sie die voll Zeitzonendefinition für die Zeit Zeitzone Eastern Standard Time abrufen.</span><span class="sxs-lookup"><span data-stu-id="ad67f-127">The following code example shows how to retrieve the full time zone definition for the Eastern Standard Time time zone.</span></span>
  
### <a name="code"></a><span data-ttu-id="ad67f-128">Code</span><span class="sxs-lookup"><span data-stu-id="ad67f-128">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010"/>
  </soap:Header>
  <soap:Body>
    <m:GetServerTimeZones ReturnFullTimeZoneData="true">
      <m:Ids>
        <t:Id>Eastern Standard Time</Id>
      </m:Ids>
    </m:GetServerTimeZones>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="ad67f-129">Comments</span><span class="sxs-lookup"><span data-stu-id="ad67f-129">Comments</span></span>

<span data-ttu-id="ad67f-130">Jedes [ID-Element (TimeZone)](id-timezone.md) enthält den Bezeichner einer Zeitzonendefinition, die angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="ad67f-130">Each [Id (TimeZone)](id-timezone.md) element contains the identifier of a time zone definition that is being requested.</span></span> <span data-ttu-id="ad67f-131">Wenn Sie Informationen zu allen Zeitzonen anfordern möchten, lassen Sie das [IDs](ids.md) -Element aus der Anforderung weglassen.</span><span class="sxs-lookup"><span data-stu-id="ad67f-131">To request information for all time zones, omit the [Ids](ids.md) element from the request.</span></span> 
  
## <a name="getservertimezones-response-examples"></a><span data-ttu-id="ad67f-132">GetServerTimeZones-Antwort Beispiele</span><span class="sxs-lookup"><span data-stu-id="ad67f-132">GetServerTimeZones response examples</span></span>

### <a name="receiving-the-time-zone-name-and-identifier-only"></a><span data-ttu-id="ad67f-133">Empfangen des Zeitzonennamens und des Bezeichners</span><span class="sxs-lookup"><span data-stu-id="ad67f-133">Receiving the Time Zone Name and Identifier Only</span></span>

<span data-ttu-id="ad67f-134">Das folgende Beispiel einer **GetServerTimeZones** -Antwort zeigt eine erfolgreiche Antwort auf eine **GetServerTimeZones** -Anforderung, in der das **ReturnFullTimeZoneData** -Attribut auf **false**festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="ad67f-134">The following example of a **GetServerTimeZones** response shows a successful response to a **GetServerTimeZones** request in which the **ReturnFullTimeZoneData** attribute was set to **false**.</span></span> <span data-ttu-id="ad67f-135">Die Antwort enthält den Namen und den Bezeichner für die Zeit Zonen Eastern Standard Time und Pacific Standard Time.</span><span class="sxs-lookup"><span data-stu-id="ad67f-135">The response contains the name and identifier for the Eastern Standard Time and Pacific Standard Time time zones.</span></span>
  
### <a name="code"></a><span data-ttu-id="ad67f-136">Code</span><span class="sxs-lookup"><span data-stu-id="ad67f-136">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="0" 
                         MajorBuildNumber="639" 
                         MinorBuildNumber="11" 
                         Version="Exchange2010" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetServerTimeZonesResponse xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                                xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:GetServerTimeZonesResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</ResponseCode>
          <m:TimeZoneDefinitions>
            <t:TimeZoneDefinition Id="Eastern Standard Time" Name="(GMT-05:00) Eastern Time (US &amp;amp; Canada)" />
            <t:TimeZoneDefinition Id="Pacific Standard Time" Name="(GMT-08:00) Pacific Time (US &amp;amp; Canada)" />
          </m:TimeZoneDefinitions>
        </m:GetServerTimeZonesResponseMessage>
      </m:ResponseMessages>
    </m:GetServerTimeZonesResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="receiving-a-full-time-zone-definition"></a><span data-ttu-id="ad67f-137">Empfangen einer voll Zeit Zonen Definition</span><span class="sxs-lookup"><span data-stu-id="ad67f-137">Receiving a Full Time Zone Definition</span></span>

<span data-ttu-id="ad67f-138">Das folgende Beispiel einer **GetServerTimeZones** -Antwort zeigt eine erfolgreiche Antwort auf eine **GetServerTimeZones** -Anforderung, in der das **ReturnFullTimeZoneData** -Attribut auf **true**festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="ad67f-138">The following example of a **GetServerTimeZones** response shows a successful response to a **GetServerTimeZones** request in which the **ReturnFullTimeZoneData** attribute was set to **true**.</span></span> <span data-ttu-id="ad67f-139">Die Antwort enthält die Definition der vollständigen Zeitzone für die Zeit Zeitzone Eastern Standard Time.</span><span class="sxs-lookup"><span data-stu-id="ad67f-139">The response contains the full time zone definition for the Eastern Standard Time time zone.</span></span>
  
### <a name="code"></a><span data-ttu-id="ad67f-140">Code</span><span class="sxs-lookup"><span data-stu-id="ad67f-140">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="0" 
                         MajorBuildNumber="639" 
                         MinorBuildNumber="11" 
                         Version="Exchange2010" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetServerTimeZonesResponse xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                                xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:GetServerTimeZonesResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</ResponseCode>
          <m:TimeZoneDefinitions>
            <t:TimeZoneDefinition Id="Eastern Standard Time" Name="(GMT-05:00) Eastern Time (US &amp;amp; Canada)">
              <t:Periods>
                <t:Period Bias="PT5H" Name="Standard" Id="trule:Microsoft/Registry/EasternStandardTime/2006-Standard" />
                <t:Period Bias="PT4H" Name="Daylight" Id="trule:Microsoft/Registry/EasternStandardTime/2006-Daylight" />
                <t:Period Bias="PT5H" Name="Standard" Id="trule:Microsoft/Registry/EasternStandardTime/2007-Standard" />
                <t:Period Bias="PT4H" Name="Daylight" Id="trule:Microsoft/Registry/EasternStandardTime/2007-Daylight" />
              </t:Periods>
              <t:TransitionsGroups>
                <t:TransitionsGroup Id="0">
                  <t:RecurringDayTransition>
                    <t:To Kind="Period">trule:Microsoft/Registry/EasternStandardTime/2006-Daylight</t:To>
                    <t:TimeOffset>PT2H</t:TimeOffset>
                    <t:Month>4</t:Month>
                    <t:DayOfWeek>Sunday</t:DayOfWeek>
                    <t:Occurrence>1</t:Occurrence>
                  </t:RecurringDayTransition>
                  <t:RecurringDayTransition>
                    <t:To Kind="Period">trule:Microsoft/Registry/EasternStandardTime/2006-Standard</t:To>
                    <t:TimeOffset>PT2H</t:TimeOffset>
                    <t:Month>10</t:Month>
                    <t:DayOfWeek>Sunday</t:DayOfWeek>
                    <t:Occurrence>-1</t:Occurrence>
                  </t:RecurringDayTransition>
                </t:TransitionsGroup>
                <t:TransitionsGroup Id="1">
                  <t:RecurringDayTransition>
                    <t:To Kind="Period">trule:Microsoft/Registry/EasternStandardTime/2007-Daylight</t:To>
                    <t:TimeOffset>PT2H</t:TimeOffset>
                    <t:Month>3</t:Month>
                    <t:DayOfWeek>Sunday</t:DayOfWeek>
                    <t:Occurrence>2</t:Occurrence>
                  </t:RecurringDayTransition>
                  <t:RecurringDayTransition>
                    <t:To Kind="Period">trule:Microsoft/Registry/EasternStandardTime/2007-Standard</t:To>
                    <t:TimeOffset>PT2H</t:TimeOffset>
                    <t:Month>11</t:Month>
                    <t:DayOfWeek>Sunday</t:DayOfWeek>
                    <t:Occurrence>1</t:Occurrence>
                  </t:RecurringDayTransition>
                </t:TransitionsGroup>
              </t:TransitionsGroups>
              <t:Transitions>
                <t:Transition>
                  <t:To Kind="Group">0</t:To>
                </t:Transition>
                <t:AbsoluteDateTransition>
                  <t:To Kind="Group">1</t:To>
                  <t:DateTime>2007-01-01T00:00:00</t:DateTime>
                </t:AbsoluteDateTransition>
              </t:Transitions>
            </t:TimeZoneDefinition>
          </m:TimeZoneDefinitions>
        </m:GetServerTimeZonesResponseMessage>
      </m:ResponseMessages>
    </m:GetServerTimeZonesResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="ad67f-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ad67f-141">See also</span></span>



[<span data-ttu-id="ad67f-142">GetServerTimeZones</span><span class="sxs-lookup"><span data-stu-id="ad67f-142">GetServerTimeZones</span></span>](getservertimezones.md)
  
[<span data-ttu-id="ad67f-143">GetServerTimeZonesResponse</span><span class="sxs-lookup"><span data-stu-id="ad67f-143">GetServerTimeZonesResponse</span></span>](getservertimezonesresponse.md)
  
 <span data-ttu-id="ad67f-144">**GetServerTimeZonesType**</span><span class="sxs-lookup"><span data-stu-id="ad67f-144">**GetServerTimeZonesType**</span></span>


[<span data-ttu-id="ad67f-145">EWS-Operationen in Exchange</span><span class="sxs-lookup"><span data-stu-id="ad67f-145">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
  
- [<span data-ttu-id="ad67f-146">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="ad67f-146">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

