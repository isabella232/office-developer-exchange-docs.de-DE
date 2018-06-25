---
title: GetUserAvailability-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetUserAvailability
api_type:
- schema
ms.assetid: 8da17226-5d3a-4525-9ffa-d83730f47bb1
description: Hier finden Sie Informationen über die GetUserAvailability EWS Vorgang.
ms.openlocfilehash: 41246fe22bfb7444cd4aa7b1d4651d475dd9231c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19829686"
---
# <a name="getuseravailability-operation"></a><span data-ttu-id="d2c9a-103">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d2c9a-103">GetUserAvailability operation</span></span>

<span data-ttu-id="d2c9a-104">Hier finden Sie Informationen zum **GetUserAvailability** EWS-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="d2c9a-104">Find information about the **GetUserAvailability** EWS operation.</span></span> 
  
<span data-ttu-id="d2c9a-105">Der Vorgang **GetUserAvailability** enthält ausführliche Informationen über die Verfügbarkeit einer Gruppe von Benutzern, Räumen und Ressourcen innerhalb eines angegebenen Zeitraums.</span><span class="sxs-lookup"><span data-stu-id="d2c9a-105">The **GetUserAvailability** operation provides detailed information about the availability of a set of users, rooms, and resources within a specified time period.</span></span> 
  
## <a name="using-the-getuseravailability-operation"></a><span data-ttu-id="d2c9a-106">Verwenden des GetUserAvailability-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="d2c9a-106">Using the GetUserAvailability operation</span></span>

<span data-ttu-id="d2c9a-107">Der Vorgang **GetUserAvailability** bietet Verfügbarkeitsinformationen für aktuellen Benutzer auf eine angegebene Detailebene.</span><span class="sxs-lookup"><span data-stu-id="d2c9a-107">The **GetUserAvailability** operation provides current user availability information at a specified level of detail.</span></span> <span data-ttu-id="d2c9a-108">Wie Outlook, Outlook Web Access, Outlook Mobile Access und andere Clientanwendungen verwenden SMTP-Adressen, um die angeforderten Informationen zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="d2c9a-108">Client applications such as Outlook, Outlook Web Access, Outlook Mobile Access, and others use SMTP addresses to identify the requested user information.</span></span> 
  
<span data-ttu-id="d2c9a-109">Der Verfügbarkeitsdienst Verteilerlisten zum Abrufen des Frei/Gebucht-Status für jedes Mitglied der Liste erweitert, wie die Anzahl von Postfächern in die Verteilerliste kleiner als 100 ist, die maximale Anzahl von Identitäten ist, die die **GetUserAvailability **Operation anfordern kann.</span><span class="sxs-lookup"><span data-stu-id="d2c9a-109">The Availability service expands distribution lists to retrieve the free/busy status for each member of the list, as long as the number of mailboxes in the distribution list is less than 100, which is the maximum number of identities that the **GetUserAvailability** operation can request.</span></span> <span data-ttu-id="d2c9a-110">Die Frei/Gebucht-Status, der die Mitglieder der Verteilerliste werden in einer einzelnen Frei/Gebucht-Status für die gesamte Verteilerliste zusammengeführt.</span><span class="sxs-lookup"><span data-stu-id="d2c9a-110">The free/busy statuses of the members of the distribution list are merged into a single free/busy status for the whole distribution list.</span></span> 
  
<span data-ttu-id="d2c9a-111">Clientanforderungen für die Anwendung angeben den Zeitraum der Verfügbarkeit Abfrage.</span><span class="sxs-lookup"><span data-stu-id="d2c9a-111">Client application requests specify the time period of the availability query.</span></span> <span data-ttu-id="d2c9a-112">Der Standardwert ist der Zeitraum für die angeforderten Informationen 42 Tage.</span><span class="sxs-lookup"><span data-stu-id="d2c9a-112">The default time period for the requested information is 42 days.</span></span> <span data-ttu-id="d2c9a-113">Enthält den Kalender des Benutzers, Termine und Besprechungen, die sowohl innerhalb als auch außerhalb der definierte Zeitraum für die Abfrage sind, wird der Termin zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d2c9a-113">If the user's calendar contains appointments or meetings that are both within and outside the defined time period for the query, the appointment is returned.</span></span> 
  
<span data-ttu-id="d2c9a-114">Die Termin und Besprechung Zeiten, die zurückgegeben werden befinden sich in der gleichen Zeitzone als Clientanwendung, die die Besprechung aufgefordert wird.</span><span class="sxs-lookup"><span data-stu-id="d2c9a-114">The appointment and meeting times that are returned are in the same time zone as the client application that is requesting the meeting.</span></span>
  
<span data-ttu-id="d2c9a-115">Der Verfügbarkeitsdienst verarbeitet die Anforderung für jeden Client.</span><span class="sxs-lookup"><span data-stu-id="d2c9a-115">The Availability service processes the request for each client.</span></span> <span data-ttu-id="d2c9a-116">Der Dienst wird erweitert und zeigt alle wiederkehrender Termine und gibt die maximale Anzahl von Kalenderdetails, die der anfordernde Client über die Berechtigung zum empfangen hat.</span><span class="sxs-lookup"><span data-stu-id="d2c9a-116">The service expands all the recurring appointments and returns the maximum number of calendar details that the requesting client has permission to receive.</span></span>
  
> [!NOTE]
> <span data-ttu-id="d2c9a-117">Wenn das Zielpostfach nicht verfügbar ist oder kann nicht gefunden werden, wird eine **MailRecipientNotFoundException** -Ausnahme ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="d2c9a-117">If the target mailbox is unavailable or cannot be found, a **MailRecipientNotFoundException** exception is thrown.</span></span> <span data-ttu-id="d2c9a-118">Der Client erhält eine Fehlermeldung, die besagt, dass der Empfänger in der Active Directory-Verzeichnisdienst oder Active Directory-Domänendienste (AD DS) nicht gefunden werden kann.</span><span class="sxs-lookup"><span data-stu-id="d2c9a-118">The client receives an error message that states that the mail recipient is not found in the Active Directory directory service or Active Directory Domain Services (AD DS).</span></span> 
  
### <a name="getuseravailability-operation-soap-headers"></a><span data-ttu-id="d2c9a-119">GetUserAvailability Vorgang SOAP-Header</span><span class="sxs-lookup"><span data-stu-id="d2c9a-119">GetUserAvailability operation SOAP headers</span></span>

<span data-ttu-id="d2c9a-120">Der Vorgang **GetUserAvailability** können die SOAP-Header, die in der folgenden Tabelle aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="d2c9a-120">The **GetUserAvailability** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="d2c9a-121">**Header**</span><span class="sxs-lookup"><span data-stu-id="d2c9a-121">**Header**</span></span>|<span data-ttu-id="d2c9a-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="d2c9a-122">**Element**</span></span>|<span data-ttu-id="d2c9a-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d2c9a-123">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d2c9a-124">**Impersonation**</span><span class="sxs-lookup"><span data-stu-id="d2c9a-124">**Impersonation**</span></span> <br/> |[<span data-ttu-id="d2c9a-125">"ExchangeImpersonation"</span><span class="sxs-lookup"><span data-stu-id="d2c9a-125">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="d2c9a-126">Identifiziert den Benutzer, denen Identität des Clients imitiert wird.</span><span class="sxs-lookup"><span data-stu-id="d2c9a-126">Identifies the user whom the client is impersonating.</span></span> <span data-ttu-id="d2c9a-127">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="d2c9a-127">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="d2c9a-128">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="d2c9a-128">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="d2c9a-129">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="d2c9a-129">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="d2c9a-130">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="d2c9a-130">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="d2c9a-131">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="d2c9a-131">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="d2c9a-132">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="d2c9a-132">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="d2c9a-133">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="d2c9a-133">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="d2c9a-134">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="d2c9a-134">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="d2c9a-135">Diese Kopfzeile gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="d2c9a-135">This header is applicable to a response.</span></span>  <br/> |
|<span data-ttu-id="d2c9a-136">**TimeZoneContext**</span><span class="sxs-lookup"><span data-stu-id="d2c9a-136">**TimeZoneContext**</span></span> <br/> |[<span data-ttu-id="d2c9a-137">TimeZoneContext</span><span class="sxs-lookup"><span data-stu-id="d2c9a-137">TimeZoneContext</span></span>](timezonecontext.md) <br/> |<span data-ttu-id="d2c9a-138">Gibt einen SOAP-Header, der identifiziert die Zeitzone für alle Antworten vom Server verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d2c9a-138">Specifies a SOAP header that identifies the time zone to be used for all responses from the server.</span></span> <span data-ttu-id="d2c9a-139">Alle Versuche, die vom Server zurückgegeben werden werden in der angegebenen Zeitzone konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d2c9a-139">All times that are returned from the server will be converted to the specified time zone.</span></span> <span data-ttu-id="d2c9a-140">Diese Kopfzeile gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="d2c9a-140">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getuseravailability-request-example-get-availability-information"></a><span data-ttu-id="d2c9a-141">GetUserAvailability-anforderungsbeispiel: Abrufen von Verfügbarkeitsinformationen</span><span class="sxs-lookup"><span data-stu-id="d2c9a-141">GetUserAvailability request example: Get availability information</span></span>

<span data-ttu-id="d2c9a-142">Im folgenden Beispiel wird eine **GetUserAvailability** -Vorgang-Anforderung erhalten Sie detaillierte Verfügbarkeitsinformationen für zwei Benutzer in der Pacific Standard Time-Zeitzone veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="d2c9a-142">The following example of a **GetUserAvailability** operation request shows how to get detailed availability information for two users in the Pacific Time time zone.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetUserAvailabilityRequest xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
                xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <t:TimeZone xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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
      </t:TimeZone>
      <MailboxDataArray>
        <t:MailboxData>
          <t:Email>
            <t:Address>user1@example.com</t:Address>
          </t:Email>
          <t:AttendeeType>Required</t:AttendeeType>
          <t:ExcludeConflicts>false</t:ExcludeConflicts>
        </t:MailboxData>
        <t:MailboxData>
          <t:Email>
            <t:Address>user2@example.com</t:Address>
          </t:Email>
          <t:AttendeeType>Required</t:AttendeeType>
          <t:ExcludeConflicts>false</t:ExcludeConflicts>
        </t:MailboxData>
      </MailboxDataArray>
      <t:FreeBusyViewOptions>
        <t:TimeWindow>
          <t:StartTime>2006-10-16T00:00:00</t:StartTime>
          <t:EndTime>2006-10-16T23:59:59</t:EndTime>
        </t:TimeWindow>
        <t:MergedFreeBusyIntervalInMinutes>60</t:MergedFreeBusyIntervalInMinutes>
        <t:RequestedView>DetailedMerged</t:RequestedView>
      </t:FreeBusyViewOptions>
    </GetUserAvailabilityRequest>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="d2c9a-143">Weitere Informationen zum vorgeschlagene Besprechungen mit dem [SuggestionsViewOptions](suggestionsviewoptions.md) Element abrufen finden Sie unter dem Schema in das virtuelle Verzeichnis EWS.</span><span class="sxs-lookup"><span data-stu-id="d2c9a-143">For more information about retrieving suggested meetings by using the [SuggestionsViewOptions](suggestionsviewoptions.md) element, see the schema in the EWS virtual directory.</span></span> 
  
<span data-ttu-id="d2c9a-144">Die Anforderung SOAP-Text enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="d2c9a-144">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="d2c9a-145">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="d2c9a-145">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
    
- [<span data-ttu-id="d2c9a-146">TimeZone (Verfügbarkeit)</span><span class="sxs-lookup"><span data-stu-id="d2c9a-146">TimeZone (Availability)</span></span>](timezone-availability.md)
    
- [<span data-ttu-id="d2c9a-147">Bias (UTC)</span><span class="sxs-lookup"><span data-stu-id="d2c9a-147">Bias (UTC)</span></span>](bias-utc.md)
    
- [<span data-ttu-id="d2c9a-148">StandardTime</span><span class="sxs-lookup"><span data-stu-id="d2c9a-148">StandardTime</span></span>](standardtime.md)
    
- [<span data-ttu-id="d2c9a-149">Bias</span><span class="sxs-lookup"><span data-stu-id="d2c9a-149">Bias</span></span>](bias.md)
    
- [<span data-ttu-id="d2c9a-150">Time</span><span class="sxs-lookup"><span data-stu-id="d2c9a-150">Time</span></span>](time.md)
    
- [<span data-ttu-id="d2c9a-151">DayOrder</span><span class="sxs-lookup"><span data-stu-id="d2c9a-151">DayOrder</span></span>](dayorder.md)
    
- [<span data-ttu-id="d2c9a-152">Month</span><span class="sxs-lookup"><span data-stu-id="d2c9a-152">Month</span></span>](month.md)
    
- [<span data-ttu-id="d2c9a-153">DayOfWeek (TimeZone)</span><span class="sxs-lookup"><span data-stu-id="d2c9a-153">DayOfWeek (TimeZone)</span></span>](dayofweek-timezone.md)
    
- [<span data-ttu-id="d2c9a-154">DaylightTime</span><span class="sxs-lookup"><span data-stu-id="d2c9a-154">DaylightTime</span></span>](daylighttime.md)
    
- [<span data-ttu-id="d2c9a-155">MailboxDataArray</span><span class="sxs-lookup"><span data-stu-id="d2c9a-155">MailboxDataArray</span></span>](mailboxdataarray.md)
    
- [<span data-ttu-id="d2c9a-156">MailboxData</span><span class="sxs-lookup"><span data-stu-id="d2c9a-156">MailboxData</span></span>](mailboxdata.md)
    
- [<span data-ttu-id="d2c9a-157">E-Mail (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="d2c9a-157">Email (EmailAddressType)</span></span>](email-emailaddresstype.md)
    
- [<span data-ttu-id="d2c9a-158">Adresse (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="d2c9a-158">Address (string)</span></span>](address-string.md)
    
- [<span data-ttu-id="d2c9a-159">AttendeeType</span><span class="sxs-lookup"><span data-stu-id="d2c9a-159">AttendeeType</span></span>](attendeetype.md)
    
- [<span data-ttu-id="d2c9a-160">ExcludeConflicts</span><span class="sxs-lookup"><span data-stu-id="d2c9a-160">ExcludeConflicts</span></span>](excludeconflicts.md)
    
- [<span data-ttu-id="d2c9a-161">FreeBusyViewOptions</span><span class="sxs-lookup"><span data-stu-id="d2c9a-161">FreeBusyViewOptions</span></span>](freebusyviewoptions.md)
    
- [<span data-ttu-id="d2c9a-162">Zeitfenster</span><span class="sxs-lookup"><span data-stu-id="d2c9a-162">TimeWindow</span></span>](timewindow.md)
    
- [<span data-ttu-id="d2c9a-163">StartTime</span><span class="sxs-lookup"><span data-stu-id="d2c9a-163">StartTime</span></span>](starttime.md)
    
- [<span data-ttu-id="d2c9a-164">EndTime</span><span class="sxs-lookup"><span data-stu-id="d2c9a-164">EndTime</span></span>](endtime.md)
    
## <a name="successful-getuseravailability-operation-response"></a><span data-ttu-id="d2c9a-165">Erfolgreiche Antwort von GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d2c9a-165">Successful GetUserAvailability operation response</span></span>

<span data-ttu-id="d2c9a-166">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die Anforderung des **GetUserAvailability** -Vorgang.</span><span class="sxs-lookup"><span data-stu-id="d2c9a-166">The following example shows a successful response to the **GetUserAvailability** operation request.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d2c9a-167">Der Kalender-Ereignis-IDs wurden gekürzt, um die Lesbarkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d2c9a-167">The calendar event identifiers have been shortened to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="665" MinorBuildNumber="7" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetUserAvailabilityResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <FreeBusyResponseArray>
        <FreeBusyResponse>
          <ResponseMessage ResponseClass="Success">
            <ResponseCode>NoError</ResponseCode>
          </ResponseMessage>
          <FreeBusyView>
            <FreeBusyViewType xmlns="http://schemas.microsoft.com/exchange/services/2006/types">DetailedMerged</FreeBusyViewType>
            <MergedFreeBusy xmlns="http://schemas.microsoft.com/exchange/services/2006/types">000002220220000000000000</MergedFreeBusy>
            <CalendarEventArray xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
              <CalendarEvent>
                <StartTime>2006-10-16T06:00:00-07:00</StartTime>
                <EndTime>2006-10-16T06:30:00-07:00</EndTime>
                <BusyType>Busy</BusyType>
                <CalendarEventDetails>
                  <ID>14B6414B0</ID>
                  <Subject>Meet with Contoso Account Executives</Subject>
                  <Location />
                  <IsMeeting>false</IsMeeting>
                  <IsRecurring>false</IsRecurring>
                  <IsException>false</IsException>
                  <IsReminderSet>false</IsReminderSet>
                  <IsPrivate>false</IsPrivate>
                </CalendarEventDetails>
              </CalendarEvent>
              <CalendarEvent>
                <StartTime>2006-10-16T07:00:00-07:00</StartTime>
                <EndTime>2006-10-16T08:00:00-07:00</EndTime>
                <BusyType>Busy</BusyType>
                <CalendarEventDetails>
                  <ID>E14B6414B0B</ID>
                  <Subject>Pick up my groceries</Subject>
                  <Location />
                  <IsMeeting>false</IsMeeting>
                  <IsRecurring>false</IsRecurring>
                  <IsException>false</IsException>
                  <IsReminderSet>false</IsReminderSet>
                  <IsPrivate>false</IsPrivate>
                </CalendarEventDetails>
              </CalendarEvent>
              <CalendarEvent>
                <StartTime>2006-10-16T09:40:00-07:00</StartTime>
                <EndTime>2006-10-16T10:10:00-07:00</EndTime>
                <BusyType>Busy</BusyType>
                <CalendarEventDetails>
                  <ID>14B6414B0B1</ID>
                  <Subject>Meet with doctor</Subject>
                  <Location>Kirkland</Location>
                  <IsMeeting>false</IsMeeting>
                  <IsRecurring>false</IsRecurring>
                  <IsException>false</IsException>
                  <IsReminderSet>false</IsReminderSet>
                  <IsPrivate>false</IsPrivate>
                </CalendarEventDetails>
              </CalendarEvent>
            </CalendarEventArray>
            <WorkingHours xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
              <TimeZone>
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
              <WorkingPeriodArray>
                <WorkingPeriod>
                  <DayOfWeek>Monday Tuesday Wednesday Thursday Friday</DayOfWeek>
                  <StartTimeInMinutes>480</StartTimeInMinutes>
                  <EndTimeInMinutes>1020</EndTimeInMinutes>
                </WorkingPeriod>
              </WorkingPeriodArray>
            </WorkingHours>
          </FreeBusyView>
        </FreeBusyResponse>
        <FreeBusyResponse>
          <ResponseMessage ResponseClass="Success">
            <ResponseCode>NoError</ResponseCode>
          </ResponseMessage>
          <FreeBusyView>
            <FreeBusyViewType xmlns="http://schemas.microsoft.com/exchange/services/2006/types">FreeBusyMerged</FreeBusyViewType>
            <MergedFreeBusy xmlns="http://schemas.microsoft.com/exchange/services/2006/types">000000001100000000000000</MergedFreeBusy>
            <CalendarEventArray xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
              <CalendarEvent>
                <StartTime>2006-10-16T09:00:00-07:00</StartTime>
                <EndTime>2006-10-16T10:00:00-07:00</EndTime>
                <BusyType>Tentative</BusyType>
              </CalendarEvent>
            </CalendarEventArray>
            <WorkingHours xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
              <TimeZone>
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
              <WorkingPeriodArray>
                <WorkingPeriod>
                  <DayOfWeek>Monday Tuesday Wednesday Thursday Friday</DayOfWeek>
                  <StartTimeInMinutes>480</StartTimeInMinutes>
                  <EndTimeInMinutes>1020</EndTimeInMinutes>
                </WorkingPeriod>
              </WorkingPeriodArray>
            </WorkingHours>
          </FreeBusyView>
        </FreeBusyResponse>
      </FreeBusyResponseArray>
    </GetUserAvailabilityResponse>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="d2c9a-168">Die Verfügbarkeitsinformationen für jeden Benutzer in einem eindeutigen [FreeBusyResponse](freebusyresponse.md) -Element wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d2c9a-168">The availability information for each user appears in a unique [FreeBusyResponse](freebusyresponse.md) element.</span></span> <span data-ttu-id="d2c9a-169">Die Reihenfolge der Benutzer in der **GetUserAvailability** -Vorgang Anforderung bestimmt die Reihenfolge der Daten zur Verfügbarkeit für jeden Benutzer in der Antwort.</span><span class="sxs-lookup"><span data-stu-id="d2c9a-169">The order of users in the **GetUserAvailability** operation request determines the order of availability data for each user in the response.</span></span> 
  
<span data-ttu-id="d2c9a-170">Ein Fehler wird an den Client zurückgegeben werden soll, wenn die Anzahl der Termine in den Zeitraum an, der in der Abfrage definiert ist größer als die maximale Anzahl von vom Administrator angegebene ist.</span><span class="sxs-lookup"><span data-stu-id="d2c9a-170">An error will be returned to the client if the number of appointments in the time period that is defined in the query is greater than the administrator-specified maximum number.</span></span> <span data-ttu-id="d2c9a-171">Die Standardeinstellung für die maximale Anzahl von Terminen ist 10.000 einzelne Instanzen und Serienelemente erweitert.</span><span class="sxs-lookup"><span data-stu-id="d2c9a-171">The default maximum number of appointments is 10,000 single instances and expanded recurrence items.</span></span> <span data-ttu-id="d2c9a-172">Diese Eigenschaft kann nur von einem Administrator konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="d2c9a-172">This property can be configured only by an administrator.</span></span>
  
<span data-ttu-id="d2c9a-173">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="d2c9a-173">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="d2c9a-174">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="d2c9a-174">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="d2c9a-175">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="d2c9a-175">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
    
- [<span data-ttu-id="d2c9a-176">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="d2c9a-176">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
    
- [<span data-ttu-id="d2c9a-177">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="d2c9a-177">FreeBusyResponse</span></span>](freebusyresponse.md)
    
- [<span data-ttu-id="d2c9a-178">ResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d2c9a-178">ResponseMessage</span></span>](responsemessage.md)
    
- [<span data-ttu-id="d2c9a-179">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="d2c9a-179">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="d2c9a-180">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="d2c9a-180">FreeBusyView</span></span>](freebusyview.md)
    
- [<span data-ttu-id="d2c9a-181">FreeBusyViewType</span><span class="sxs-lookup"><span data-stu-id="d2c9a-181">FreeBusyViewType</span></span>](freebusyviewtype.md)
    
- [<span data-ttu-id="d2c9a-182">MergedFreeBusy</span><span class="sxs-lookup"><span data-stu-id="d2c9a-182">MergedFreeBusy</span></span>](mergedfreebusy.md)
    
- [<span data-ttu-id="d2c9a-183">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="d2c9a-183">CalendarEventArray</span></span>](calendareventarray.md)
    
- [<span data-ttu-id="d2c9a-184">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="d2c9a-184">CalendarEvent</span></span>](calendarevent.md)
    
- [<span data-ttu-id="d2c9a-185">StartTime</span><span class="sxs-lookup"><span data-stu-id="d2c9a-185">StartTime</span></span>](starttime.md)
    
- [<span data-ttu-id="d2c9a-186">EndTime</span><span class="sxs-lookup"><span data-stu-id="d2c9a-186">EndTime</span></span>](endtime.md)
    
- [<span data-ttu-id="d2c9a-187">BusyType</span><span class="sxs-lookup"><span data-stu-id="d2c9a-187">BusyType</span></span>](busytype.md)
    
- [<span data-ttu-id="d2c9a-188">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="d2c9a-188">CalendarEventDetails</span></span>](calendareventdetails.md)
    
- [<span data-ttu-id="d2c9a-189">ID</span><span class="sxs-lookup"><span data-stu-id="d2c9a-189">ID</span></span>](id.md)
    
- [<span data-ttu-id="d2c9a-190">Betreff (CalendarEventDetails)</span><span class="sxs-lookup"><span data-stu-id="d2c9a-190">Subject (CalendarEventDetails)</span></span>](subject-calendareventdetails.md)
    
- [<span data-ttu-id="d2c9a-191">Speicherort (CalendarEventDetails)</span><span class="sxs-lookup"><span data-stu-id="d2c9a-191">Location (CalendarEventDetails)</span></span>](location-calendareventdetails.md)
    
- [<span data-ttu-id="d2c9a-192">IsMeeting (CalendarEventDetails)</span><span class="sxs-lookup"><span data-stu-id="d2c9a-192">IsMeeting (CalendarEventDetails)</span></span>](ismeeting-calendareventdetails.md)
    
- [<span data-ttu-id="d2c9a-193">IsRecurring (CalendarEventDetails)</span><span class="sxs-lookup"><span data-stu-id="d2c9a-193">IsRecurring (CalendarEventDetails)</span></span>](isrecurring-calendareventdetails.md)
    
- [<span data-ttu-id="d2c9a-194">IsException</span><span class="sxs-lookup"><span data-stu-id="d2c9a-194">IsException</span></span>](isexception.md)
    
- [<span data-ttu-id="d2c9a-195">IsReminderSet</span><span class="sxs-lookup"><span data-stu-id="d2c9a-195">IsReminderSet</span></span>](isreminderset.md)
    
- [<span data-ttu-id="d2c9a-196">IsPrivate</span><span class="sxs-lookup"><span data-stu-id="d2c9a-196">IsPrivate</span></span>](isprivate.md)
    
- [<span data-ttu-id="d2c9a-197">WorkingHours</span><span class="sxs-lookup"><span data-stu-id="d2c9a-197">WorkingHours</span></span>](workinghours-ex15websvcsotherref.md)
    
- [<span data-ttu-id="d2c9a-198">TimeZone (Verfügbarkeit)</span><span class="sxs-lookup"><span data-stu-id="d2c9a-198">TimeZone (Availability)</span></span>](timezone-availability.md)
    
- [<span data-ttu-id="d2c9a-199">Bias (UTC)</span><span class="sxs-lookup"><span data-stu-id="d2c9a-199">Bias (UTC)</span></span>](bias-utc.md)
    
- [<span data-ttu-id="d2c9a-200">StandardTime</span><span class="sxs-lookup"><span data-stu-id="d2c9a-200">StandardTime</span></span>](standardtime.md)
    
- [<span data-ttu-id="d2c9a-201">Bias</span><span class="sxs-lookup"><span data-stu-id="d2c9a-201">Bias</span></span>](bias.md)
    
- [<span data-ttu-id="d2c9a-202">Time</span><span class="sxs-lookup"><span data-stu-id="d2c9a-202">Time</span></span>](time.md)
    
- [<span data-ttu-id="d2c9a-203">DayOrder</span><span class="sxs-lookup"><span data-stu-id="d2c9a-203">DayOrder</span></span>](dayorder.md)
    
- [<span data-ttu-id="d2c9a-204">Month</span><span class="sxs-lookup"><span data-stu-id="d2c9a-204">Month</span></span>](month.md)
    
- [<span data-ttu-id="d2c9a-205">DayOfWeek (TimeZone)</span><span class="sxs-lookup"><span data-stu-id="d2c9a-205">DayOfWeek (TimeZone)</span></span>](dayofweek-timezone.md)
    
- [<span data-ttu-id="d2c9a-206">DaylightTime</span><span class="sxs-lookup"><span data-stu-id="d2c9a-206">DaylightTime</span></span>](daylighttime.md)
    
- [<span data-ttu-id="d2c9a-207">WorkingPeriodArray</span><span class="sxs-lookup"><span data-stu-id="d2c9a-207">WorkingPeriodArray</span></span>](workingperiodarray.md)
    
- [<span data-ttu-id="d2c9a-208">WorkingPeriod</span><span class="sxs-lookup"><span data-stu-id="d2c9a-208">WorkingPeriod</span></span>](workingperiod.md)
    
- [<span data-ttu-id="d2c9a-209">DayOfWeek (WorkingPeriod)</span><span class="sxs-lookup"><span data-stu-id="d2c9a-209">DayOfWeek (WorkingPeriod)</span></span>](dayofweek-workingperiod.md)
    
- [<span data-ttu-id="d2c9a-210">StartTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="d2c9a-210">StartTimeInMinutes</span></span>](starttimeinminutes.md)
    
- [<span data-ttu-id="d2c9a-211">EndTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="d2c9a-211">EndTimeInMinutes</span></span>](endtimeinminutes.md)
    
## <a name="see-also"></a><span data-ttu-id="d2c9a-212">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d2c9a-212">See also</span></span>

- [<span data-ttu-id="d2c9a-213">EWS-Operationen in Exchange</span><span class="sxs-lookup"><span data-stu-id="d2c9a-213">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="d2c9a-214">Erste Benutzer Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="d2c9a-214">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)
    

