---
title: GetEvents-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetEvents
api_type:
- schema
ms.assetid: f268efe5-9a1a-41a2-b6a6-51fcde7720a1
description: Der Vorgang GetEvents wird von Pull-Abonnement-Clients auf Anforderung-Benachrichtigungen vom Client Access-Server verwendet. Die Antwort auf einen Vorgang GetEvents gibt ein Array von Elementen und Ereignisse, die in einem Postfach seit dem letzten die Benachrichtigung aufgetreten sind.
ms.openlocfilehash: 1a23a9d570a4554e54becb7927f25dff89888c74
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758647"
---
# <a name="getevents-operation"></a>GetEvents-Vorgang

Der Vorgang **GetEvents** wird von Pull-Abonnement-Clients auf Anforderung-Benachrichtigungen vom Client Access-Server verwendet. Die Antwort auf einen Vorgang **GetEvents** gibt ein Array von Elementen und Ereignisse, die in einem Postfach seit dem letzten die Benachrichtigung aufgetreten sind. 
  
> [!IMPORTANT]
> Der Vorgang **DeleteUserConfiguration** wird ein Ereignis für das Ereignis Benachrichtigungssystem ausgelöst. Das Benutzerobjekt Konfiguration wird verschoben werden, um die Dumpster. 
  
## <a name="remarks"></a>Hinweise

Änderungen an Kalenderelemente möglicherweise die Generierung von mehreren Ereignisse. Diese Ereignisse sind das Ergebnis der temporäre Objekte, die zu erstellenden in das Postfach Frei/Gebucht-Daten Speicher Elemente als Teil des und/oder den normalen Betrieb Kalender geändert wird. Ereignisse für Element class "IPM. SchedulePlus.FreeBusy.BinaryData"sollte mithilfe Webdienstclients ignoriert werden. Diese temporäre Elemente werden gelöscht, nachdem sie erstellt wurden. aus diesem Grund, wenn versucht wird, diese Elemente abzurufen, wird ein Fehler zurückgegeben werden, dass die, die besagt, dass das Element nicht gefunden wurde.
  
## <a name="getevents-request-example"></a>GetEvents anforderungsbeispiel

### <a name="description"></a>Beschreibung

Im folgenden Beispiel wird gezeigt, wie zum Anfordern der Ereignisse und Elemente, die mit einem Abonnement verknüpft sind, die durch die Abonnement-ID und Wasserzeichen identifiziert wird.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetEvents xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <SubscriptionId>f6bc657d-dde1-4f94-952d-143b95d6483d</SubscriptionId>
      <Watermark>AAAAAMAGAAAAAAAAAQ==</Watermark>
    </GetEvents>
  </soap:Body>
</soap:Envelope>
```

### <a name="getevents-request-elements"></a>GetEvents Anforderung Elemente

In der Anforderung werden folgende Elemente verwendet:
  
- [GetEvents](getevents.md)
    
- [SubscriptionId (GetEvents)](subscriptionid-getevents.md)
    
- [Wasserzeichen](watermark.md)
    
## <a name="successful-getevents-response-example"></a>Erfolgreiche GetEvents antwortbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel einer Antwort zeigt eine Benachrichtigung über das Vorhandensein von zwei neue e-Mail-Nachrichten, seit die letzte Benachrichtigung-Anforderung an den Server gesendet wurde.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetEventsResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                       xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:GetEventsResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Notification>
            <t:SubscriptionId>f6bc657d-dde1-4f94-952d-143b95d6483d</t:SubscriptionId>
            <t:PreviousWatermark>AAAAAMAGAAAAAAAAAQ==</t:PreviousWatermark>
            <t:MoreEvents>false</t:MoreEvents>
            <t:NewMailEvent>
              <t:Watermark>AAAAAM4GAAAAAAAAAQ==</t:Watermark>
              <t:TimeStamp>2006-08-22T00:36:29Z</t:TimeStamp>
              <t:ItemId Id="AQApAHR" ChangeKey="CQAAAA==" />
              <t:ParentFolderId Id="AQApAH" ChangeKey="AQAAAA==" />
            </t:NewMailEvent>
            <t:NewMailEvent>
              <t:Watermark>AAAAAOQGAAAAAAAAAQ==</t:Watermark>
              <t:TimeStamp>2006-08-22T01:00:50Z</t:TimeStamp>
              <t:ItemId Id="AQApAHRw" ChangeKey="CQAAAA==" />
              <t:ParentFolderId Id="AQApAH" ChangeKey="AQAAAA==" />
            </t:NewMailEvent>
          </m:Notification>
        </m:GetEventsResponseMessage>
      </m:ResponseMessages>
    </GetEventsResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Kommentare

> [!NOTE]
> Der Bezeichner Element und Ordner wurden gekürzt, um die Lesbarkeit zu erhalten. 
  
### <a name="getevents-response-elements"></a>GetEvents Antwortelemente

In der Antwort werden folgende Elemente verwendet:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [GetEventsResponse](geteventsresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [GetEventsResponseMessage](geteventsresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Benachrichtigung](notification-ex15websvcsotherref.md)
    
- [SubscriptionId (GetEvents)](subscriptionid-getevents.md)
    
- [PreviousWatermark](previouswatermark.md)
    
- [MoreEvents](moreevents.md)
    
- [NewMailEvent](newmailevent.md)
    
- [Wasserzeichen](watermark.md)
    
- [Zeitstempel](timestamp.md)
    
- [ItemId](itemid.md)
    
- [ParentFolderId](parentfolderid.md)
    
Wenn andere Optionen für die Antwortnachricht des Vorgangs **GetEvents** suchen möchten, verwenden Sie die Schemahierarchie. Starten Sie die [Benachrichtigung](notification-ex15websvcsotherref.md) -Element. 
  
## <a name="getevents-error-response-example"></a>Antwortbeispiel GetEvents Fehler

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine Fehlerantwort an eine Anforderung **GetEvents** . 
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
                 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                 xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetEventsResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:GetEventsResponseMessage ResponseClass="Error">
          <m:MessageText>Access is denied. Only the subscription owner may access the subscription.</m:MessageText>
          <m:ResponseCode>ErrorSubscriptionAccessDenied</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:GetEventsResponseMessage>
      </m:ResponseMessages>
    </GetEventsResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="remarks"></a>Hinweise

Bei der Verarbeitung einer Anforderung **GetEvents** führt der Clientzugriffs-Server die folgenden Schritte aus: 
  
1. Die SubscriptionID der Anforderung wird bestätigt, um ein gültiges Abonnement sein, das auf dem Client Access Server gehostet wird. Wenn sie nicht der Fall ist, schlägt der **GetEvents** -Aufruf. 
    
2. Die SMTP-Adresse des authentifizierten Benutzers für die Anforderung wird an die SMTP-Adresse des Benutzers verglichen, die das Abonnement erstellt hat. Wenn sie nicht übereinstimmen, schlägt die Anforderung **GetEvents** . 
    
3. Die Abonnement-Warteschlange abgefragt wird für Ereignisse, die darauf warten, an den Client gesendet werden. Wenn die Warteschlange nicht leer ist, werden die ersten 50 Ereignisse aus der Warteschlange aus der Warteschlange abgerufen und in eine Benachrichtigung codiert.
    
4. Wenn keine Ereignisse in der Warteschlange gefunden werden, wird ein StatusEvent generiert und in einer Benachrichtigungsantwort codiert.
    
5. Die Benachrichtigungsantwort wird an den Client zurückgegeben.
    
6. Die Ereignisse, die in der Benachrichtigung enthaltenen werden aus der Warteschlange Abonnement entfernt, und das Client Access Server lokale letzte Wasserzeichen für das Abonnement festgelegt ist, können Sie dem Wasserzeichen des letzten-Ereignisses, das zurückgegeben wird.
    
7. Der Timeout-Zeitgeber für das Abonnement wird zurückgesetzt.
    
## <a name="see-also"></a>Siehe auch



[Vorgang abonnieren](subscribe-operation.md)
  
[Vorgang des Kündigens von Abonnements](unsubscribe-operation.md)


[Mithilfe von Pullabonnements](http://msdn.microsoft.com/library/f956bc0e-2b25-4613-966b-54c65456897c%28Office.15%29.aspx)

