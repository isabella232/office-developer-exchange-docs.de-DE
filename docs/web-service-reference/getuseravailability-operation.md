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
description: Hier finden Sie Informationen zum GetUserAvailability-EWS-Vorgang.
ms.openlocfilehash: b6d03c7da65e3f30f093b7e41448abcca2330a84
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458222"
---
# <a name="getuseravailability-operation"></a><span data-ttu-id="e7b18-103">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="e7b18-103">GetUserAvailability operation</span></span>

<span data-ttu-id="e7b18-104">Hier finden Sie Informationen zum **GetUserAvailability** -EWS-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="e7b18-104">Find information about the **GetUserAvailability** EWS operation.</span></span> 
  
<span data-ttu-id="e7b18-105">Der **GetUserAvailability** -Vorgang enthält detaillierte Informationen zur Verfügbarkeit einer Gruppe von Benutzern, Räumen und Ressourcen innerhalb eines bestimmten Zeitraums.</span><span class="sxs-lookup"><span data-stu-id="e7b18-105">The **GetUserAvailability** operation provides detailed information about the availability of a set of users, rooms, and resources within a specified time period.</span></span> 
  
## <a name="using-the-getuseravailability-operation"></a><span data-ttu-id="e7b18-106">Verwenden des GetUserAvailability-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="e7b18-106">Using the GetUserAvailability operation</span></span>

<span data-ttu-id="e7b18-107">Der **GetUserAvailability** -Vorgang stellt aktuelle Informationen zur Verfügbarkeit von Benutzern mit einer bestimmten Detailebene bereit.</span><span class="sxs-lookup"><span data-stu-id="e7b18-107">The **GetUserAvailability** operation provides current user availability information at a specified level of detail.</span></span> <span data-ttu-id="e7b18-108">Client Anwendungen wie Outlook, Outlook Web Access, Outlook Mobile Access und andere verwenden SMTP-Adressen, um die angeforderten Benutzerinformationen zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="e7b18-108">Client applications such as Outlook, Outlook Web Access, Outlook Mobile Access, and others use SMTP addresses to identify the requested user information.</span></span> 
  
<span data-ttu-id="e7b18-109">Der Verfügbarkeitsdienst erweitert Verteilerlisten, um den Frei/Gebucht-Status für jedes Mitglied der Liste abzurufen, solange die Anzahl der Postfächer in der Verteilerliste kleiner als 100 ist, was die maximale Anzahl von Identitäten ist, die der **GetUserAvailability** -Vorgang anfordern kann.</span><span class="sxs-lookup"><span data-stu-id="e7b18-109">The Availability service expands distribution lists to retrieve the free/busy status for each member of the list, as long as the number of mailboxes in the distribution list is less than 100, which is the maximum number of identities that the **GetUserAvailability** operation can request.</span></span> <span data-ttu-id="e7b18-110">Die Frei/Gebucht-Status der Mitglieder der Verteilerliste werden mit einem einzelnen Frei/Gebucht-Status für die gesamte Verteilerliste zusammengeführt.</span><span class="sxs-lookup"><span data-stu-id="e7b18-110">The free/busy statuses of the members of the distribution list are merged into a single free/busy status for the whole distribution list.</span></span> 
  
<span data-ttu-id="e7b18-111">Client Anwendungsanforderungen geben den Zeitraum der Verfügbarkeitsabfrage an.</span><span class="sxs-lookup"><span data-stu-id="e7b18-111">Client application requests specify the time period of the availability query.</span></span> <span data-ttu-id="e7b18-112">Der Standardzeitraum für die angeforderten Informationen beträgt 42 Tage.</span><span class="sxs-lookup"><span data-stu-id="e7b18-112">The default time period for the requested information is 42 days.</span></span> <span data-ttu-id="e7b18-113">Wenn der Kalender des Benutzers Termine oder Besprechungen enthält, die innerhalb und außerhalb des definierten Zeitraums für die Abfrage liegen, wird der Termin zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e7b18-113">If the user's calendar contains appointments or meetings that are both within and outside the defined time period for the query, the appointment is returned.</span></span> 
  
<span data-ttu-id="e7b18-114">Die zurückgegebenen Termin-und Besprechungszeiten befinden sich in der gleichen Zeitzone wie die Clientanwendung, die die Besprechung anfordert.</span><span class="sxs-lookup"><span data-stu-id="e7b18-114">The appointment and meeting times that are returned are in the same time zone as the client application that is requesting the meeting.</span></span>
  
<span data-ttu-id="e7b18-115">Der Verfügbarkeitsdienst verarbeitet die Anforderung für jeden Client.</span><span class="sxs-lookup"><span data-stu-id="e7b18-115">The Availability service processes the request for each client.</span></span> <span data-ttu-id="e7b18-116">Der Dienst erweitert alle Terminserien und gibt die maximale Anzahl von Kalenderdetails zurück, die der anfordernde Client über die Berechtigung zum empfangen verfügt.</span><span class="sxs-lookup"><span data-stu-id="e7b18-116">The service expands all the recurring appointments and returns the maximum number of calendar details that the requesting client has permission to receive.</span></span>
  
> [!NOTE]
> <span data-ttu-id="e7b18-117">Wenn das Zielpostfach nicht verfügbar ist oder nicht gefunden werden kann, wird eine **MailRecipientNotFoundException** -Ausnahme ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="e7b18-117">If the target mailbox is unavailable or cannot be found, a **MailRecipientNotFoundException** exception is thrown.</span></span> <span data-ttu-id="e7b18-118">Der Client erhält eine Fehlermeldung, die besagt, dass der e-Mail-Empfänger nicht im Active Directory Verzeichnisdienst oder Active Directory-Domänendienste (AD DS) gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="e7b18-118">The client receives an error message that states that the mail recipient is not found in the Active Directory directory service or Active Directory Domain Services (AD DS).</span></span> 
  
### <a name="getuseravailability-operation-soap-headers"></a><span data-ttu-id="e7b18-119">SOAP-Header des GetUserAvailability-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="e7b18-119">GetUserAvailability operation SOAP headers</span></span>

<span data-ttu-id="e7b18-120">Der **GetUserAvailability** -Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="e7b18-120">The **GetUserAvailability** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="e7b18-121">**Header**</span><span class="sxs-lookup"><span data-stu-id="e7b18-121">**Header**</span></span>|<span data-ttu-id="e7b18-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="e7b18-122">**Element**</span></span>|<span data-ttu-id="e7b18-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e7b18-123">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e7b18-124">**Impersonation**</span><span class="sxs-lookup"><span data-stu-id="e7b18-124">**Impersonation**</span></span> <br/> |[<span data-ttu-id="e7b18-125">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="e7b18-125">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="e7b18-126">Gibt den Benutzer an, den der Client imitiert.</span><span class="sxs-lookup"><span data-stu-id="e7b18-126">Identifies the user whom the client is impersonating.</span></span> <span data-ttu-id="e7b18-127">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="e7b18-127">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="e7b18-128">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="e7b18-128">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="e7b18-129">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="e7b18-129">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="e7b18-130">Gibt die Schemaversion für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="e7b18-130">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="e7b18-131">Diese Kopfzeile gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="e7b18-131">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="e7b18-132">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="e7b18-132">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="e7b18-133">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="e7b18-133">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="e7b18-134">Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="e7b18-134">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="e7b18-135">Diese Kopfzeile gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="e7b18-135">This header is applicable to a response.</span></span>  <br/> |
|<span data-ttu-id="e7b18-136">**TimeZoneContext**</span><span class="sxs-lookup"><span data-stu-id="e7b18-136">**TimeZoneContext**</span></span> <br/> |[<span data-ttu-id="e7b18-137">TimeZoneContext</span><span class="sxs-lookup"><span data-stu-id="e7b18-137">TimeZoneContext</span></span>](timezonecontext.md) <br/> |<span data-ttu-id="e7b18-138">Gibt einen SOAP-Header an, der die Zeitzone angibt, die für alle Antworten vom Server verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e7b18-138">Specifies a SOAP header that identifies the time zone to be used for all responses from the server.</span></span> <span data-ttu-id="e7b18-139">Alle vom Server zurückgegebenen Zeiten werden in die angegebene Zeitzone konvertiert.</span><span class="sxs-lookup"><span data-stu-id="e7b18-139">All times that are returned from the server will be converted to the specified time zone.</span></span> <span data-ttu-id="e7b18-140">Diese Kopfzeile gilt für eine Antwort.</span><span class="sxs-lookup"><span data-stu-id="e7b18-140">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getuseravailability-request-example-get-availability-information"></a><span data-ttu-id="e7b18-141">GetUserAvailability-Anforderungs Beispiel: Abrufen von Verfügbarkeitsinformationen</span><span class="sxs-lookup"><span data-stu-id="e7b18-141">GetUserAvailability request example: Get availability information</span></span>

<span data-ttu-id="e7b18-142">Im folgenden Beispiel einer **GetUserAvailability** -Vorgangsanforderung wird gezeigt, wie detaillierte Verfügbarkeitsinformationen für zwei Benutzer in der Pacific Time-Zeitzone abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="e7b18-142">The following example of a **GetUserAvailability** operation request shows how to get detailed availability information for two users in the Pacific Time time zone.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetUserAvailabilityRequest xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <t:TimeZone xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="e7b18-143">Weitere Informationen zum Abrufen von vorgeschlagenen Besprechungen mithilfe des [SuggestionsViewOptions](suggestionsviewoptions.md) -Elements finden Sie unter dem Schema im virtuellen EWS-Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="e7b18-143">For more information about retrieving suggested meetings by using the [SuggestionsViewOptions](suggestionsviewoptions.md) element, see the schema in the EWS virtual directory.</span></span> 
  
<span data-ttu-id="e7b18-144">Der SOAP-Anforderungstext Körper enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="e7b18-144">The request SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="e7b18-145">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="e7b18-145">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
    
- [<span data-ttu-id="e7b18-146">Zeitzone (Verfügbarkeit)</span><span class="sxs-lookup"><span data-stu-id="e7b18-146">TimeZone (Availability)</span></span>](timezone-availability.md)
    
- [<span data-ttu-id="e7b18-147">Bias (UTC)</span><span class="sxs-lookup"><span data-stu-id="e7b18-147">Bias (UTC)</span></span>](bias-utc.md)
    
- [<span data-ttu-id="e7b18-148">Standard Time</span><span class="sxs-lookup"><span data-stu-id="e7b18-148">StandardTime</span></span>](standardtime.md)
    
- [<span data-ttu-id="e7b18-149">Bias</span><span class="sxs-lookup"><span data-stu-id="e7b18-149">Bias</span></span>](bias.md)
    
- [<span data-ttu-id="e7b18-150">Time</span><span class="sxs-lookup"><span data-stu-id="e7b18-150">Time</span></span>](time.md)
    
- [<span data-ttu-id="e7b18-151">DayOrder</span><span class="sxs-lookup"><span data-stu-id="e7b18-151">DayOrder</span></span>](dayorder.md)
    
- [<span data-ttu-id="e7b18-152">Month</span><span class="sxs-lookup"><span data-stu-id="e7b18-152">Month</span></span>](month.md)
    
- [<span data-ttu-id="e7b18-153">DayOfWeek (Zeitzone)</span><span class="sxs-lookup"><span data-stu-id="e7b18-153">DayOfWeek (TimeZone)</span></span>](dayofweek-timezone.md)
    
- [<span data-ttu-id="e7b18-154">DaylightTime</span><span class="sxs-lookup"><span data-stu-id="e7b18-154">DaylightTime</span></span>](daylighttime.md)
    
- [<span data-ttu-id="e7b18-155">MailboxDataArray</span><span class="sxs-lookup"><span data-stu-id="e7b18-155">MailboxDataArray</span></span>](mailboxdataarray.md)
    
- [<span data-ttu-id="e7b18-156">MailboxData</span><span class="sxs-lookup"><span data-stu-id="e7b18-156">MailboxData</span></span>](mailboxdata.md)
    
- [<span data-ttu-id="e7b18-157">E-Mail (e-Mail-Adresse)</span><span class="sxs-lookup"><span data-stu-id="e7b18-157">Email (EmailAddressType)</span></span>](email-emailaddresstype.md)
    
- [<span data-ttu-id="e7b18-158">Address (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="e7b18-158">Address (string)</span></span>](address-string.md)
    
- [<span data-ttu-id="e7b18-159">AttendeeType</span><span class="sxs-lookup"><span data-stu-id="e7b18-159">AttendeeType</span></span>](attendeetype.md)
    
- [<span data-ttu-id="e7b18-160">ExcludeConflicts</span><span class="sxs-lookup"><span data-stu-id="e7b18-160">ExcludeConflicts</span></span>](excludeconflicts.md)
    
- [<span data-ttu-id="e7b18-161">FreeBusyViewOptions</span><span class="sxs-lookup"><span data-stu-id="e7b18-161">FreeBusyViewOptions</span></span>](freebusyviewoptions.md)
    
- [<span data-ttu-id="e7b18-162">TimeWindow</span><span class="sxs-lookup"><span data-stu-id="e7b18-162">TimeWindow</span></span>](timewindow.md)
    
- [<span data-ttu-id="e7b18-163">StartTime</span><span class="sxs-lookup"><span data-stu-id="e7b18-163">StartTime</span></span>](starttime.md)
    
- [<span data-ttu-id="e7b18-164">EndTime</span><span class="sxs-lookup"><span data-stu-id="e7b18-164">EndTime</span></span>](endtime.md)
    
## <a name="successful-getuseravailability-operation-response"></a><span data-ttu-id="e7b18-165">Erfolgreiche Reaktion des GetUserAvailability-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="e7b18-165">Successful GetUserAvailability operation response</span></span>

<span data-ttu-id="e7b18-166">Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die **GetUserAvailability** -Vorgangsanforderung.</span><span class="sxs-lookup"><span data-stu-id="e7b18-166">The following example shows a successful response to the **GetUserAvailability** operation request.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="e7b18-167">Die Kalenderereignis Bezeichner wurden verkürzt, um die Lesbarkeit beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="e7b18-167">The calendar event identifiers have been shortened to preserve readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="665" MinorBuildNumber="7" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetUserAvailabilityResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <FreeBusyResponseArray>
        <FreeBusyResponse>
          <ResponseMessage ResponseClass="Success">
            <ResponseCode>NoError</ResponseCode>
          </ResponseMessage>
          <FreeBusyView>
            <FreeBusyViewType xmlns="https://schemas.microsoft.com/exchange/services/2006/types">DetailedMerged</FreeBusyViewType>
            <MergedFreeBusy xmlns="https://schemas.microsoft.com/exchange/services/2006/types">000002220220000000000000</MergedFreeBusy>
            <CalendarEventArray xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
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
            <WorkingHours xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
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
            <FreeBusyViewType xmlns="https://schemas.microsoft.com/exchange/services/2006/types">FreeBusyMerged</FreeBusyViewType>
            <MergedFreeBusy xmlns="https://schemas.microsoft.com/exchange/services/2006/types">000000001100000000000000</MergedFreeBusy>
            <CalendarEventArray xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
              <CalendarEvent>
                <StartTime>2006-10-16T09:00:00-07:00</StartTime>
                <EndTime>2006-10-16T10:00:00-07:00</EndTime>
                <BusyType>Tentative</BusyType>
              </CalendarEvent>
            </CalendarEventArray>
            <WorkingHours xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="e7b18-168">Die Verfügbarkeitsinformationen für jeden Benutzer werden in einem eindeutigen [FreeBusyResponse](freebusyresponse.md) -Element angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e7b18-168">The availability information for each user appears in a unique [FreeBusyResponse](freebusyresponse.md) element.</span></span> <span data-ttu-id="e7b18-169">Die Reihenfolge der Benutzer in der **GetUserAvailability** -Vorgangsanforderung bestimmt die Reihenfolge der Verfügbarkeitsdaten für jeden Benutzer in der Antwort.</span><span class="sxs-lookup"><span data-stu-id="e7b18-169">The order of users in the **GetUserAvailability** operation request determines the order of availability data for each user in the response.</span></span> 
  
<span data-ttu-id="e7b18-170">Wenn die Anzahl der Termine in dem in der Abfrage definierten Zeitraum größer ist als die vom Administrator festgelegte maximale Zahl, wird ein Fehler an den Client zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e7b18-170">An error will be returned to the client if the number of appointments in the time period that is defined in the query is greater than the administrator-specified maximum number.</span></span> <span data-ttu-id="e7b18-171">Die standardmäßige maximale Anzahl von Terminen ist 10.000 einzelne Instanzen und erweiterte Serienelemente.</span><span class="sxs-lookup"><span data-stu-id="e7b18-171">The default maximum number of appointments is 10,000 single instances and expanded recurrence items.</span></span> <span data-ttu-id="e7b18-172">Diese Eigenschaft kann nur von einem Administrator konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="e7b18-172">This property can be configured only by an administrator.</span></span>
  
<span data-ttu-id="e7b18-173">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="e7b18-173">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="e7b18-174">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="e7b18-174">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="e7b18-175">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="e7b18-175">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
    
- [<span data-ttu-id="e7b18-176">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="e7b18-176">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
    
- [<span data-ttu-id="e7b18-177">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="e7b18-177">FreeBusyResponse</span></span>](freebusyresponse.md)
    
- [<span data-ttu-id="e7b18-178">ResponseMessage</span><span class="sxs-lookup"><span data-stu-id="e7b18-178">ResponseMessage</span></span>](responsemessage.md)
    
- [<span data-ttu-id="e7b18-179">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="e7b18-179">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="e7b18-180">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="e7b18-180">FreeBusyView</span></span>](freebusyview.md)
    
- [<span data-ttu-id="e7b18-181">FreeBusyViewType</span><span class="sxs-lookup"><span data-stu-id="e7b18-181">FreeBusyViewType</span></span>](freebusyviewtype.md)
    
- [<span data-ttu-id="e7b18-182">MergedFreeBusy</span><span class="sxs-lookup"><span data-stu-id="e7b18-182">MergedFreeBusy</span></span>](mergedfreebusy.md)
    
- [<span data-ttu-id="e7b18-183">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="e7b18-183">CalendarEventArray</span></span>](calendareventarray.md)
    
- [<span data-ttu-id="e7b18-184">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="e7b18-184">CalendarEvent</span></span>](calendarevent.md)
    
- [<span data-ttu-id="e7b18-185">StartTime</span><span class="sxs-lookup"><span data-stu-id="e7b18-185">StartTime</span></span>](starttime.md)
    
- [<span data-ttu-id="e7b18-186">EndTime</span><span class="sxs-lookup"><span data-stu-id="e7b18-186">EndTime</span></span>](endtime.md)
    
- [<span data-ttu-id="e7b18-187">Busytype</span><span class="sxs-lookup"><span data-stu-id="e7b18-187">BusyType</span></span>](busytype.md)
    
- [<span data-ttu-id="e7b18-188">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="e7b18-188">CalendarEventDetails</span></span>](calendareventdetails.md)
    
- [<span data-ttu-id="e7b18-189">ID</span><span class="sxs-lookup"><span data-stu-id="e7b18-189">ID</span></span>](id.md)
    
- [<span data-ttu-id="e7b18-190">Betreff (CalendarEventDetails)</span><span class="sxs-lookup"><span data-stu-id="e7b18-190">Subject (CalendarEventDetails)</span></span>](subject-calendareventdetails.md)
    
- [<span data-ttu-id="e7b18-191">Speicherort (CalendarEventDetails)</span><span class="sxs-lookup"><span data-stu-id="e7b18-191">Location (CalendarEventDetails)</span></span>](location-calendareventdetails.md)
    
- [<span data-ttu-id="e7b18-192">Ismeeting (CalendarEventDetails)</span><span class="sxs-lookup"><span data-stu-id="e7b18-192">IsMeeting (CalendarEventDetails)</span></span>](ismeeting-calendareventdetails.md)
    
- [<span data-ttu-id="e7b18-193">Iswiederkehr (CalendarEventDetails)</span><span class="sxs-lookup"><span data-stu-id="e7b18-193">IsRecurring (CalendarEventDetails)</span></span>](isrecurring-calendareventdetails.md)
    
- [<span data-ttu-id="e7b18-194">Isexception</span><span class="sxs-lookup"><span data-stu-id="e7b18-194">IsException</span></span>](isexception.md)
    
- [<span data-ttu-id="e7b18-195">Reminder</span><span class="sxs-lookup"><span data-stu-id="e7b18-195">IsReminderSet</span></span>](isreminderset.md)
    
- [<span data-ttu-id="e7b18-196">IsPrivate</span><span class="sxs-lookup"><span data-stu-id="e7b18-196">IsPrivate</span></span>](isprivate.md)
    
- [<span data-ttu-id="e7b18-197">WorkingHours</span><span class="sxs-lookup"><span data-stu-id="e7b18-197">WorkingHours</span></span>](workinghours-ex15websvcsotherref.md)
    
- [<span data-ttu-id="e7b18-198">Zeitzone (Verfügbarkeit)</span><span class="sxs-lookup"><span data-stu-id="e7b18-198">TimeZone (Availability)</span></span>](timezone-availability.md)
    
- [<span data-ttu-id="e7b18-199">Bias (UTC)</span><span class="sxs-lookup"><span data-stu-id="e7b18-199">Bias (UTC)</span></span>](bias-utc.md)
    
- [<span data-ttu-id="e7b18-200">Standard Time</span><span class="sxs-lookup"><span data-stu-id="e7b18-200">StandardTime</span></span>](standardtime.md)
    
- [<span data-ttu-id="e7b18-201">Bias</span><span class="sxs-lookup"><span data-stu-id="e7b18-201">Bias</span></span>](bias.md)
    
- [<span data-ttu-id="e7b18-202">Time</span><span class="sxs-lookup"><span data-stu-id="e7b18-202">Time</span></span>](time.md)
    
- [<span data-ttu-id="e7b18-203">DayOrder</span><span class="sxs-lookup"><span data-stu-id="e7b18-203">DayOrder</span></span>](dayorder.md)
    
- [<span data-ttu-id="e7b18-204">Month</span><span class="sxs-lookup"><span data-stu-id="e7b18-204">Month</span></span>](month.md)
    
- [<span data-ttu-id="e7b18-205">DayOfWeek (Zeitzone)</span><span class="sxs-lookup"><span data-stu-id="e7b18-205">DayOfWeek (TimeZone)</span></span>](dayofweek-timezone.md)
    
- [<span data-ttu-id="e7b18-206">DaylightTime</span><span class="sxs-lookup"><span data-stu-id="e7b18-206">DaylightTime</span></span>](daylighttime.md)
    
- [<span data-ttu-id="e7b18-207">WorkingPeriodArray</span><span class="sxs-lookup"><span data-stu-id="e7b18-207">WorkingPeriodArray</span></span>](workingperiodarray.md)
    
- [<span data-ttu-id="e7b18-208">WorkingPeriod</span><span class="sxs-lookup"><span data-stu-id="e7b18-208">WorkingPeriod</span></span>](workingperiod.md)
    
- [<span data-ttu-id="e7b18-209">DayOfWeek (WorkingPeriod)</span><span class="sxs-lookup"><span data-stu-id="e7b18-209">DayOfWeek (WorkingPeriod)</span></span>](dayofweek-workingperiod.md)
    
- [<span data-ttu-id="e7b18-210">StartTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="e7b18-210">StartTimeInMinutes</span></span>](starttimeinminutes.md)
    
- [<span data-ttu-id="e7b18-211">EndTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="e7b18-211">EndTimeInMinutes</span></span>](endtimeinminutes.md)
    
## <a name="see-also"></a><span data-ttu-id="e7b18-212">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e7b18-212">See also</span></span>

- [<span data-ttu-id="e7b18-213">EWS-Operationen in Exchange</span><span class="sxs-lookup"><span data-stu-id="e7b18-213">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
    
- [<span data-ttu-id="e7b18-214">Verfügbarkeit von Benutzern wird abgerufen</span><span class="sxs-lookup"><span data-stu-id="e7b18-214">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)
    

