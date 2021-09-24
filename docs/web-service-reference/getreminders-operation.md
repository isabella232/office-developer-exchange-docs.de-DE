---
title: GetReminders-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 1b56f83f-3b87-4b55-8259-fde6692da681
description: Hier finden Sie Informationen zum GetReminders EWS-Vorgang.
ms.openlocfilehash: e47dbb6ffceac3535bb72f93ee27bbb3f3f259e6
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513563"
---
# <a name="getreminders-operation"></a>GetReminders-Vorgang

Hier finden Sie Informationen zum **GetReminders** EWS-Vorgang. 
  
Der EWS-Vorgang **(GetReminders** Exchange Web Services) ruft Erinnerungen für Kalender- und Aufgabenelemente ab. 
  
Dieser Vorgang wurde in Exchange Server 2013 eingeführt.
  
## <a name="using-the-getreminders-operation"></a>Verwenden des GetReminders-Vorgangs

Der **GetReminders-Vorgang** ruft Erinnerungen für aktuelle und zukünftige Kalender- und Aufgabenelemente im Postfach des Benutzers ab, abhängig von den in der Anforderung übergebenen Elementwerten. Der Vorgang kann alle aktuellen und zukünftigen Kalenderelemente sowie Aufgaben abrufen, für die eine Erinnerung festgelegt ist. Private Kalenderelemente sind in Antworten enthalten. Aufgaben ohne Erinnerungen sind weder in Antworten enthalten noch E-Mails mit Erinnerungen oder Nachverfolgungsflags. 
  
Um alle aktuellen Erinnerungen abzurufen, wird empfohlen, [reminderType](remindertype.md) auf **"Alle"** und ["EndTime"](endtime-remindermessagedatatype.md) auf die aktuelle Uhrzeit festzulegen. 
  
Wenn die [Elemente BeginTime](begintime.md) und **EndTime** in der Anforderung enthalten sind, enthält die Antwort Erinnerungen für alle Kalender- und Aufgabenelemente, die dazwischen auftreten, haben eine Erinnerung, die zwischen **"BeginTime"** und **"EndTime"** auftritt.
  
In der folgenden Tabelle wird das Verhalten des **ReminderType-Elements** beschrieben, wenn die **Elemente BeginTime** und **EndTime** enthalten sind. 
  
|ReminderType**-Elementwert**|**Beschreibung**|
|:-----|:-----|
|Alle  <br/> |Erinnerungen, die zwischen **"BeginTime"** und **"EndTime"** auftreten.  <br/> |
|Current  <br/> |Erinnerungen, die von **"Alle"** zurückgegeben werden, plus Erinnerungen, die vor dem angeforderten Zeitfenster liegen, wenn das Ereignis noch läuft, sowie alle Termine unabhängig vom Alter.  <br/> |
|Alt  <br/> |Erinnerungen, die von **"Alle"** zurückgegeben werden, minus Ereignisse, die noch nicht abgeschlossen wurden, abzüglich aller Termine. Die **Elemente "BeginTime"** und **"EndTime"** müssen so festgelegt werden, dass sie den **Wert "Old"** verwenden.  <br/> |
   
### <a name="getreminders-operation-soap-headers"></a>SOAP-Header des GetReminders-Vorgangs

Der **GetReminders-Vorgang** kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind. 
  
|**Headername**|**Element**|**Beschreibung**|
|:-----|:-----|:-----|
|**Impersonation** <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt. Dieser Header gilt für eine Anforderung.  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |Identifiziert die Kultur, wie in RFC 3066 definiert, "Tags für die Identifizierung von Sprachen", die für den Zugriff auf das Postfach verwendet werden soll. Dieser Header gilt für eine Anforderung.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Gibt die Schemaversion für die Vorgangsanforderung an. Dieser Header gilt für eine Anforderung.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Gibt die Version des Servers an, der auf die Anforderung geantwortet hat. Dieser Header gilt für eine Antwort.  <br/> |
   
## <a name="getreminders-operation-request-example"></a>GetReminders-Vorgangsanforderungsbeispiel

Das folgende Beispiel einer **GetReminders-Vorgangsanforderung** zeigt, wie die ersten fünf Kalenderelemente abgerufen werden, die zwischen **BeginTime** und **EndTime** auftreten.
  
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

Der SOAP-Textkörper der Beispielanforderung enthält die folgenden Elemente:
  
- [GetReminders](getreminders.md)
    
- [EndTime](endtime-remindermessagedatatype.md)
    
- [ReminderType](remindertype.md)
    
Der SOAP-Textkörper kann auch die folgenden Elemente enthalten:
  
- [BeginTime](begintime.md)
    
- [MaxItems](maxitems.md)
    
## <a name="successful-getreminders-operation-response"></a>Erfolgreiche GetReminders-Vorgangsantwort

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **GetReminders-Vorgangsanforderung.** Die Antwort enthält eine Erinnerung für das Kalenderelement "Teambesprechung" und eine Erinnerung für die Aufgabe "Aufgabe zum Senden von Besprechungsnotizen". 
  
> [!NOTE]
> Bezeichner wurden gekürzt, um die Lesbarkeit zu gewährleisten. 
  
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

Der SOAP-Antworttext enthält die folgenden Elemente:
  
- [GetRemindersResponse](getremindersresponse.md)
    
- [Reminders](reminders.md)
    
- [Reminder](reminder.md)
    
- [Betreff](subject.md)
    
- [Ort](location-remindermessagedatatype.md)
    
- [ReminderTime](remindertime.md)
    
- [StartDate](startdate.md)
    
- [EndDate](enddate-remindertype.md)
    
- [ItemId](itemid.md)
    
- [RecurringMasterItemId](recurringmasteritemid.md)
    
- [ReminderGroup](remindergroup.md)
    
- [UID](uid-remindertype.md)
    
## <a name="getreminders-operation-error-response-example"></a>Beispiel für eine GetReminders-Vorgangsfehlerantwort

Das folgende Beispiel zeigt eine Fehlerantwort auf eine **GetReminders-Vorgangsanforderung.** Dies ist eine Antwort auf eine Anforderung, bei der das Enddatum vor dem Startdatum lag. 
  
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
    
Weitere Fehlercodes, die für EWS generisch und für diesen Vorgang spezifisch sind, finden Sie unter [ResponseCode](responsecode.md).
  
## <a name="see-also"></a>Siehe auch


- [PerformReminderAction](performreminderaction.md)
    

