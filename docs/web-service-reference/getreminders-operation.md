---
title: GetReminders-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1b56f83f-3b87-4b55-8259-fde6692da681
description: Hier finden Sie Informationen zum reerinnerungs-EWS-Vorgang.
ms.openlocfilehash: dcbe20c674d7524a7776d374fa6964899abf472f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458306"
---
# <a name="getreminders-operation"></a>GetReminders-Vorgang

Hier finden Sie Informationen zum **reerinnerungs** -EWS-Vorgang. 
  
Mit **dem** Reminder-Exchange-Webdienste Vorgang werden Erinnerungen für Kalender-und Aufgabenelemente abgerufen. 
  
Dieser Vorgang wurde in Exchange Server 2013 eingeführt.
  
## <a name="using-the-getreminders-operation"></a>Verwenden der reerinnerungs-Operation

Der **geterinnerungs** -Vorgang ruft Erinnerungen für aktuelle und zukünftige Kalender-und Aufgabenelemente im Postfach des Benutzers ab, abhängig von den in der Anforderung übergebenen Elementwerten. Mit dem Vorgang können alle aktuellen und zukünftigen Kalenderelemente sowie Aufgaben abgerufen werden, für die eine Erinnerung festgelegt wurde. Private Kalenderelemente werden in den Antworten eingeschlossen. Aufgaben ohne Erinnerungen werden in den Antworten nicht berücksichtigt, und es handelt sich auch nicht um e-Mails mit Erinnerungen oder Nachverfolgungskennzeichen. 
  
Zum Abrufen aller aktuellen Erinnerungen empfiehlt es sich, den [Reminder](remindertype.md) auf " **all** " und " [EndTime](endtime-remindermessagedatatype.md) " auf die aktuelle Uhrzeit festzulegen. 
  
Wenn die [BeginTime](begintime.md) -und **EndTime** -Elemente in der Anforderung enthalten sind, enthält die Antwort Erinnerungen für alle Kalender-und Aufgabenelemente, die zwischen einer Erinnerung zwischen dem **BeginTime** und **EndTime**stattfinden.
  
In der folgenden Tabelle wird das Verhalten des **Reminder** -Elements beschrieben, wenn die Elemente **BeginTime** und **EndTime** enthalten sind. 
  
|Reminder * *-Elementwert * *|**Beschreibung**|
|:-----|:-----|
|Alle  <br/> |Erinnerungen, die zwischen **BeginTime** und **EndTime**auftreten.  <br/> |
|Current  <br/> |Erinnerungen, die von **allen**zurückgegeben werden, sowie Erinnerungen, die vor dem angeforderten Zeitfenster liegen, wenn das Ereignis noch nicht abgeschlossen ist, sowie alle Termine unabhängig vom Alter.  <br/> |
|Alten  <br/> |Erinnerungen, die von **allen**zurückgegeben werden, minus Ereignisse, die noch nicht abgeschlossen wurden, abzüglich aller Termine. Die **BeginTime** -und **EndTime** -Elemente müssen festgelegt werden, um den **alten** Wert zu verwenden.  <br/> |
   
### <a name="getreminders-operation-soap-headers"></a>Reerinnerungs-Operation SOAP-Header

Der **reerinnerungs** -Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind. 
  
|**Headername**|**Element**|**Beschreibung**|
|:-----|:-----|:-----|
|**Impersonation** <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt. Diese Kopfzeile gilt für eine Anforderung.  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |Identifiziert die Kultur gemäß der Definition in RFC 3066, "Tags für die Identifizierung von Sprachen", die für den Zugriff auf das Postfach verwendet werden sollen. Diese Kopfzeile gilt für eine Anforderung.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Gibt die Schemaversion für die Vorgangsanforderung an. Diese Kopfzeile gilt für eine Anforderung.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Gibt die Version des Servers an, der auf die Anforderung geantwortet hat. Diese Kopfzeile gilt für eine Antwort.  <br/> |
   
## <a name="getreminders-operation-request-example"></a>Reerinnerungs-Vorgangsanforderung (Beispiel)

Das folgende Beispiel einer **reerinnerungs** -Vorgangsanforderung zeigt, wie die ersten fünf Kalenderelemente abgerufen werden, die zwischen **BeginTime** und **EndTime**auftreten.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
  <soap:Body>
    <m:GetReminders>
      <m:EndTime>2014-04-16T21:00:00Z</m:EndTime>
      <m:ReminderType>All</m:ReminderType>
    </m:GetReminders>
  </soap:Body>
</soap:Envelope>
```

Der SOAP-Beispiel Anforderungstext enthält die folgenden Elemente:
  
- [GetReminders](getreminders.md)
    
- [EndTime](endtime-remindermessagedatatype.md)
    
- [Reminder](remindertype.md)
    
Der SOAP-Textkörper kann auch die folgenden Elemente enthalten:
  
- [BeginTime](begintime.md)
    
- [MaxItems wird](maxitems.md)
    
## <a name="successful-getreminders-operation-response"></a>Erfolgreiche reerinnerungs-Vorgangs Antwort

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine Vorgangsanforderung von **reerinnerter** . Die Antwort enthält eine Erinnerung für das Kalenderelement "Team Besprechung" und eine Erinnerung an die Aufgabe "Besprechungsnotizen senden". 
  
> [!NOTE]
> Die Bezeichner wurden verkürzt, um die Lesbarkeit zu erhalten. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <ServerVersionInfo MajorVersion="15"
                       MinorVersion="0"
                       MajorBuildNumber="918"
                       MinorBuildNumber="7"
                       Version="V2_10"
                       xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetRemindersResponse ResponseClass="Success"
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <Reminders>
        <Reminder xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <Subject>Team meeting</Subject>
          <Location />
          <ReminderTime>2014-04-15T21:00:00Z</ReminderTime>
          <StartDate>2014-04-15T21:00:00Z</StartDate>
          <EndDate>2014-04-15T21:30:00Z</EndDate>
          <ItemId Id="vQAAAA=="
                  ChangeKey="DwAAABYAAAB4to43JyybTYwHLBM1k8MxAAACRoV4" />
          <RecurringMasterItemId Id="K7u5AAA=" ChangeKey="DwAAABYAAAB4to43JyybTYwHLBM1k8MxAAACRoV0" />
          <ReminderGroup>Calendar</ReminderGroup>
          <UID>6CF2FA62</UID>
        </Reminder>
        <Reminder xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <Subject>Task to send meeting notes</Subject>
          <Location />
          <ReminderTime>2014-04-16T14:00:00Z</ReminderTime>
          <StartDate>0001-01-02T00:00:00Z</StartDate>
          <EndDate>0001-01-02T00:00:00Z</EndDate>
          <ItemId Id="vAAAAA=="
                  ChangeKey="EwAAABQAAACOs0HEMq1WTKpI7sNu5qXNAAAIDg==" />
          <ReminderGroup>Task</ReminderGroup>
          <UID>vAAAAA==</UID>
        </Reminder>
      </Reminders>
    </GetRemindersResponse>
  </s:Body>
</s:Envelope>
```

Der SOAP-Antworttext Körper enthält die folgenden Elemente:
  
- [GetRemindersResponse](getremindersresponse.md)
    
- [Reminders](reminders.md)
    
- [Reminder](reminder.md)
    
- [Betreff](subject.md)
    
- [Standort](location-remindermessagedatatype.md)
    
- [ReminderTime](remindertime.md)
    
- [StartDate](startdate.md)
    
- [EndDate](enddate-remindertype.md)
    
- [ItemId](itemid.md)
    
- [RecurringMasterItemId](recurringmasteritemid.md)
    
- [Reminder](remindergroup.md)
    
- [UID](uid-remindertype.md)
    
## <a name="getreminders-operation-error-response-example"></a>Reerinnerungs Operation-Fehlerantwort (Beispiel)

Das folgende Beispiel zeigt eine Fehlerantwort auf eine **reerinnerungs** -Vorgangsanforderung. Dies ist eine Antwort auf eine Anforderung, bei der das Enddatum vor dem Startdatum lag. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <ServerVersionInfo MajorVersion="15"
                       MinorVersion="0"
                       MajorBuildNumber="918"
                       MinorBuildNumber="7"
                       Version="V2_10"
                       xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetRemindersResponse ResponseClass="Error"
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <MessageText>EndDate is earlier than StartDate</MessageText>
      <ResponseCode>ErrorInvalidOperation</ResponseCode>
      <DescriptiveLinkKey>0</DescriptiveLinkKey>
    </GetRemindersResponse>
  </s:Body>
</s:Envelope>
```

Der SOAP-Textkörper der Fehlerantwort enthält die folgenden Elemente:
  
- [GetRemindersResponse](getremindersresponse.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
Weitere Fehlercodes, die für EWS allgemein und spezifisch für diesen Vorgang sind, finden Sie unter [Response Code](responsecode.md).
  
## <a name="see-also"></a>Siehe auch


- [PerformReminderAction](performreminderaction.md)
    

