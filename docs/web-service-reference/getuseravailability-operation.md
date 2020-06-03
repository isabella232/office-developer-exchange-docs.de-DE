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
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458222"
---
# <a name="getuseravailability-operation"></a>GetUserAvailability-Vorgang

Hier finden Sie Informationen zum **GetUserAvailability** -EWS-Vorgang. 
  
Der **GetUserAvailability** -Vorgang enthält detaillierte Informationen zur Verfügbarkeit einer Gruppe von Benutzern, Räumen und Ressourcen innerhalb eines bestimmten Zeitraums. 
  
## <a name="using-the-getuseravailability-operation"></a>Verwenden des GetUserAvailability-Vorgangs

Der **GetUserAvailability** -Vorgang stellt aktuelle Informationen zur Verfügbarkeit von Benutzern mit einer bestimmten Detailebene bereit. Client Anwendungen wie Outlook, Outlook Web Access, Outlook Mobile Access und andere verwenden SMTP-Adressen, um die angeforderten Benutzerinformationen zu identifizieren. 
  
Der Verfügbarkeitsdienst erweitert Verteilerlisten, um den Frei/Gebucht-Status für jedes Mitglied der Liste abzurufen, solange die Anzahl der Postfächer in der Verteilerliste kleiner als 100 ist, was die maximale Anzahl von Identitäten ist, die der **GetUserAvailability** -Vorgang anfordern kann. Die Frei/Gebucht-Status der Mitglieder der Verteilerliste werden mit einem einzelnen Frei/Gebucht-Status für die gesamte Verteilerliste zusammengeführt. 
  
Client Anwendungsanforderungen geben den Zeitraum der Verfügbarkeitsabfrage an. Der Standardzeitraum für die angeforderten Informationen beträgt 42 Tage. Wenn der Kalender des Benutzers Termine oder Besprechungen enthält, die innerhalb und außerhalb des definierten Zeitraums für die Abfrage liegen, wird der Termin zurückgegeben. 
  
Die zurückgegebenen Termin-und Besprechungszeiten befinden sich in der gleichen Zeitzone wie die Clientanwendung, die die Besprechung anfordert.
  
Der Verfügbarkeitsdienst verarbeitet die Anforderung für jeden Client. Der Dienst erweitert alle Terminserien und gibt die maximale Anzahl von Kalenderdetails zurück, die der anfordernde Client über die Berechtigung zum empfangen verfügt.
  
> [!NOTE]
> Wenn das Zielpostfach nicht verfügbar ist oder nicht gefunden werden kann, wird eine **MailRecipientNotFoundException** -Ausnahme ausgelöst. Der Client erhält eine Fehlermeldung, die besagt, dass der e-Mail-Empfänger nicht im Active Directory Verzeichnisdienst oder Active Directory-Domänendienste (AD DS) gefunden wird. 
  
### <a name="getuseravailability-operation-soap-headers"></a>SOAP-Header des GetUserAvailability-Vorgangs

Der **GetUserAvailability** -Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind. 
  
|**Header**|**Element**|**Beschreibung**|
|:-----|:-----|:-----|
|**Impersonation** <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Gibt den Benutzer an, den der Client imitiert. Diese Kopfzeile gilt für eine Anforderung.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Gibt die Schemaversion für die Vorgangsanforderung an. Diese Kopfzeile gilt für eine Anforderung.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Gibt die Version des Servers an, der auf die Anforderung geantwortet hat. Diese Kopfzeile gilt für eine Antwort.  <br/> |
|**TimeZoneContext** <br/> |[TimeZoneContext](timezonecontext.md) <br/> |Gibt einen SOAP-Header an, der die Zeitzone angibt, die für alle Antworten vom Server verwendet werden soll. Alle vom Server zurückgegebenen Zeiten werden in die angegebene Zeitzone konvertiert. Diese Kopfzeile gilt für eine Antwort.  <br/> |
   
## <a name="getuseravailability-request-example-get-availability-information"></a>GetUserAvailability-Anforderungs Beispiel: Abrufen von Verfügbarkeitsinformationen

Im folgenden Beispiel einer **GetUserAvailability** -Vorgangsanforderung wird gezeigt, wie detaillierte Verfügbarkeitsinformationen für zwei Benutzer in der Pacific Time-Zeitzone abgerufen werden. 
  
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

Weitere Informationen zum Abrufen von vorgeschlagenen Besprechungen mithilfe des [SuggestionsViewOptions](suggestionsviewoptions.md) -Elements finden Sie unter dem Schema im virtuellen EWS-Verzeichnis. 
  
Der SOAP-Anforderungstext Körper enthält die folgenden Elemente:
  
- [GetUserAvailabilityRequest](getuseravailabilityrequest.md)
    
- [Zeitzone (Verfügbarkeit)](timezone-availability.md)
    
- [Bias (UTC)](bias-utc.md)
    
- [Standard Time](standardtime.md)
    
- [Bias](bias.md)
    
- [Time](time.md)
    
- [DayOrder](dayorder.md)
    
- [Month](month.md)
    
- [DayOfWeek (Zeitzone)](dayofweek-timezone.md)
    
- [DaylightTime](daylighttime.md)
    
- [MailboxDataArray](mailboxdataarray.md)
    
- [MailboxData](mailboxdata.md)
    
- [E-Mail (e-Mail-Adresse)](email-emailaddresstype.md)
    
- [Address (Zeichenfolge)](address-string.md)
    
- [AttendeeType](attendeetype.md)
    
- [ExcludeConflicts](excludeconflicts.md)
    
- [FreeBusyViewOptions](freebusyviewoptions.md)
    
- [TimeWindow](timewindow.md)
    
- [StartTime](starttime.md)
    
- [EndTime](endtime.md)
    
## <a name="successful-getuseravailability-operation-response"></a>Erfolgreiche Reaktion des GetUserAvailability-Vorgangs

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die **GetUserAvailability** -Vorgangsanforderung. 
  
> [!NOTE]
> Die Kalenderereignis Bezeichner wurden verkürzt, um die Lesbarkeit beizubehalten. 
  
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

Die Verfügbarkeitsinformationen für jeden Benutzer werden in einem eindeutigen [FreeBusyResponse](freebusyresponse.md) -Element angezeigt. Die Reihenfolge der Benutzer in der **GetUserAvailability** -Vorgangsanforderung bestimmt die Reihenfolge der Verfügbarkeitsdaten für jeden Benutzer in der Antwort. 
  
Wenn die Anzahl der Termine in dem in der Abfrage definierten Zeitraum größer ist als die vom Administrator festgelegte maximale Zahl, wird ein Fehler an den Client zurückgegeben. Die standardmäßige maximale Anzahl von Terminen ist 10.000 einzelne Instanzen und erweiterte Serienelemente. Diese Eigenschaft kann nur von einem Administrator konfiguriert werden.
  
In der Antwort werden folgende Elemente verwendet:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [GetUserAvailabilityResponse](getuseravailabilityresponse.md)
    
- [FreeBusyResponseArray](freebusyresponsearray.md)
    
- [FreeBusyResponse](freebusyresponse.md)
    
- [ResponseMessage](responsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [FreeBusyView](freebusyview.md)
    
- [FreeBusyViewType](freebusyviewtype.md)
    
- [MergedFreeBusy](mergedfreebusy.md)
    
- [CalendarEventArray](calendareventarray.md)
    
- [CalendarEvent](calendarevent.md)
    
- [StartTime](starttime.md)
    
- [EndTime](endtime.md)
    
- [Busytype](busytype.md)
    
- [CalendarEventDetails](calendareventdetails.md)
    
- [ID](id.md)
    
- [Betreff (CalendarEventDetails)](subject-calendareventdetails.md)
    
- [Speicherort (CalendarEventDetails)](location-calendareventdetails.md)
    
- [Ismeeting (CalendarEventDetails)](ismeeting-calendareventdetails.md)
    
- [Iswiederkehr (CalendarEventDetails)](isrecurring-calendareventdetails.md)
    
- [Isexception](isexception.md)
    
- [Reminder](isreminderset.md)
    
- [IsPrivate](isprivate.md)
    
- [WorkingHours](workinghours-ex15websvcsotherref.md)
    
- [Zeitzone (Verfügbarkeit)](timezone-availability.md)
    
- [Bias (UTC)](bias-utc.md)
    
- [Standard Time](standardtime.md)
    
- [Bias](bias.md)
    
- [Time](time.md)
    
- [DayOrder](dayorder.md)
    
- [Month](month.md)
    
- [DayOfWeek (Zeitzone)](dayofweek-timezone.md)
    
- [DaylightTime](daylighttime.md)
    
- [WorkingPeriodArray](workingperiodarray.md)
    
- [WorkingPeriod](workingperiod.md)
    
- [DayOfWeek (WorkingPeriod)](dayofweek-workingperiod.md)
    
- [StartTimeInMinutes](starttimeinminutes.md)
    
- [EndTimeInMinutes](endtimeinminutes.md)
    
## <a name="see-also"></a>Siehe auch

- [EWS-Operationen in Exchange](ews-operations-in-exchange.md)
    
- [Verfügbarkeit von Benutzern wird abgerufen](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)
    

