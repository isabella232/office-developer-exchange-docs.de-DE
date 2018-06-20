---
title: GetReminders-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1b56f83f-3b87-4b55-8259-fde6692da681
description: Hier finden Sie Informationen über die GetReminders EWS Vorgang.
ms.openlocfilehash: 803dabf51b94dbd8fb01f2709a42ff59a597bfd1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758785"
---
# <a name="getreminders-operation"></a>GetReminders-Vorgang

Hier finden Sie Informationen zum **GetReminders** EWS-Vorgang. 
  
Der Vorgang des **GetReminders** Exchange-Webdienste (EWS) werden für Kalender und Erinnerungen abgerufen. 
  
Dieser Vorgang wurde in Exchange Server 2013 eingeführt.
  
## <a name="using-the-getreminders-operation"></a>Verwenden des GetReminders-Vorgangs

Der Vorgang **GetReminders** ruft Erinnerungen für aktuellen und zukünftigen Kalender und Aufgabenelementen im Postfach des Benutzers, je nach der Elementwerte in der Anforderung übergeben. Alle aktuellen und zukünftigen Kalenderelemente sowie Aufgaben, bei die eine Erinnerung festgelegt haben, kann die Operation abrufen. Privaten Kalenderelementen sind in Antworten enthalten. Aufgaben ohne Erinnerungen sind nicht in Antworten, noch werden e-Mails mit Erinnerungen oder Flags nachverfolgen. 
  
Rufen Sie alle aktuelle Erinnerungen wird empfohlen, die [ReminderType](remindertype.md) an **Alle** und die [EndTime](endtime-remindermessagedatatype.md) auf die aktuelle Zeit festlegen. 
  
Wenn die [BeginTime](begintime.md) und **EndTime für** Elemente in der Anforderung enthalten sind, die Antwort enthält Erinnerungen für alle Kalender und Aufgabenelementen, die zwischen auftreten haben eine Erinnerung, die zwischen den **BeginTime** und **EndTime**liegt.
  
In der folgenden Tabelle wird das Verhalten des **ReminderType** -Elements beschrieben, wenn die Elemente **BeginTime** und **EndTime** enthalten sind. 
  
|ReminderType ** Element Wert **|**Beschreibung**|
|:-----|:-----|
|Alle  <br/> |Erinnerungen, die zwischen dem **BeginTime** und **EndTime**auftreten.  <br/> |
|Aktuelle  <br/> |Erinnerungen zurückgegebene **Alle**, plus Erinnerungen, die älter als die angeforderte Zeitfenster sind Wenn das Ereignis noch laufende plus alle Termine unabhängig von Alter.  <br/> |
|Alte  <br/> |Erinnerungen zurückgegebene **Alle**, minus Ereignisse, die noch nicht minus alle Termine abgeschlossen haben. Die Elemente **BeginTime** und **EndTime** müssen den **alten** Wert verwenden, festgelegt werden.  <br/> |
   
### <a name="getreminders-operation-soap-headers"></a>GetReminders Vorgang SOAP-Header

Der Vorgang **GetReminders** können die SOAP-Header, die in der folgenden Tabelle aufgelistet sind. 
  
|**Headername**|**Element**|**Beschreibung**|
|:-----|:-----|:-----|
|**Impersonation** <br/> |["ExchangeImpersonation"](exchangeimpersonation.md) <br/> |Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt. Diese Kopfzeile gilt für eine Anforderung.  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |Bezeichnet die Kultur gemäß Definition in RFC 3066, "Tags for the Identification des Languages", um Zugriff auf das Postfach verwendet werden. Diese Kopfzeile gilt für eine Anforderung.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Gibt die Schemaversion für die Vorgangsanforderung an. Diese Kopfzeile gilt für eine Anforderung.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Gibt die Version des Servers an, der auf die Anforderung geantwortet hat. Diese Kopfzeile gilt für eine Antwort.  <br/> |
   
## <a name="getreminders-operation-request-example"></a>GetReminders Vorgang anforderungsbeispiel

Im folgenden Beispiel wird eine **GetReminders** Vorgang Anforderung veranschaulicht, wie die ersten fünf Kalenderelemente abgerufen, die zwischen dem **BeginTime** und **EndTime**auftreten.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
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

Die Beispiel für eine Anforderung SOAP-Text enthält die folgenden Elemente:
  
- [GetReminders](getreminders.md)
    
- [EndTime](endtime-remindermessagedatatype.md)
    
- [ReminderType](remindertype.md)
    
Der SOAP-Text kann auch die folgenden Elemente enthalten:
  
- [BeginTime](begintime.md)
    
- [MaxItems wird](maxitems.md)
    
## <a name="successful-getreminders-operation-response"></a>Erfolgreiche GetReminders Vorgangsantwort

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **GetReminders** Vorgang an. Die Antwort enthält eine Erinnerung für das Kalenderelement "Team-Meeting" und eine Erinnerung für die Aufgabe "Vorgang zum Senden von Besprechungsnotizen". 
  
> [!NOTE]
> Bezeichner wurden gekürzt, um die Lesbarkeit zu erhalten. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <ServerVersionInfo MajorVersion="15"
                       MinorVersion="0"
                       MajorBuildNumber="918"
                       MinorBuildNumber="7"
                       Version="V2_10"
                       xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetRemindersResponse ResponseClass="Success"
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <Reminders>
        <Reminder xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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
        <Reminder xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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

Die Antwort SOAP-Text enthält die folgenden Elemente:
  
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
    
## <a name="getreminders-operation-error-response-example"></a>GetReminders Vorgang Fehler antwortbeispiel

Das folgende Beispiel zeigt eine Fehlerantwort an eine **GetReminders** Vorgang Anforderung. Dies ist eine Antwort auf eine Anforderung, in der das Enddatum einer älteren Version als der Anfangstermin war. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <ServerVersionInfo MajorVersion="15"
                       MinorVersion="0"
                       MajorBuildNumber="918"
                       MinorBuildNumber="7"
                       Version="V2_10"
                       xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetRemindersResponse ResponseClass="Error"
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <MessageText>EndDate is earlier than StartDate</MessageText>
      <ResponseCode>ErrorInvalidOperation</ResponseCode>
      <DescriptiveLinkKey>0</DescriptiveLinkKey>
    </GetRemindersResponse>
  </s:Body>
</s:Envelope>
```

Die SOAP-Body-Fehlerantwort enthält die folgenden Elemente:
  
- [GetRemindersResponse](getremindersresponse.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
Zusätzliche Fehlercodes, die für EWS generisch und für diese Operation spezifisch sind, finden Sie unter [ResponseCode](responsecode.md).
  
## <a name="see-also"></a>Siehe auch


- [PerformReminderAction](performreminderaction.md)
    

