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
description: Der GetEvents-Vorgang wird von Pull-Abonnementclients verwendet, um Benachrichtigungen vom Client Zugriffsserver anzufordern. Die GetEvents-Vorgangs Antwort gibt ein Array von Elementen und Ereignissen zurück, die seit der letzten Benachrichtigung in einem Postfach aufgetreten sind.
ms.openlocfilehash: 9258fd003c242911866aa7abbca5eba2b9582223
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462514"
---
# <a name="getevents-operation"></a>GetEvents-Vorgang

Der **GetEvents** -Vorgang wird von Pull-Abonnementclients verwendet, um Benachrichtigungen vom Client Zugriffsserver anzufordern. Die **GetEvents** -Vorgangs Antwort gibt ein Array von Elementen und Ereignissen zurück, die seit der letzten Benachrichtigung in einem Postfach aufgetreten sind. 
  
> [!IMPORTANT]
> Durch den **DeleteUserConfiguration** -Vorgang wird ein Verschiebe Ereignis für das Ereignis Benachrichtigungssystem ausgelöst. Das Benutzer Konfigurationsobjekt wird in den Papierkorb verschoben. 
  
## <a name="remarks"></a>Bemerkungen

Änderungen an Kalenderelementen können zur Generierung von mehreren Ereignissen führen. Diese Ereignisse sind das Ergebnis von temporären Elementen, die im Postfach erstellt werden, und frei/gebucht-Datenspeicherelemente, die im Rahmen normaler Kalender Vorgänge geändert wurden, oder beides. Ereignisse für die Elementklasse "IPM. SchedulePlus. freebusy. BinaryData "sollte von Webdienstclients ignoriert werden. Diese temporären Elemente werden nach ihrer Erstellung gelöscht. Wenn also versucht wird, diese Elemente abzurufen, wird ein Fehler zurückgegeben, der besagt, dass das Element nicht gefunden wurde.
  
## <a name="getevents-request-example"></a>GetEvents-Anforderungs Beispiel

### <a name="description"></a>Beschreibung

Im folgenden Beispiel wird gezeigt, wie die Ereignisse und Elemente angefordert werden, die einem Abonnement zugeordnet sind, das durch die Abonnement-ID und das Wasserzeichen identifiziert wird.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetEvents xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <SubscriptionId>f6bc657d-dde1-4f94-952d-143b95d6483d</SubscriptionId>
      <Watermark>AAAAAMAGAAAAAAAAAQ==</Watermark>
    </GetEvents>
  </soap:Body>
</soap:Envelope>
```

### <a name="getevents-request-elements"></a>GetEvents-anforderungselemente

In der Anforderung werden folgende Elemente verwendet:
  
- [GetEvents](getevents.md)
    
- [Abonnement-Nr (GetEvents)](subscriptionid-getevents.md)
    
- [Watermark](watermark.md)
    
## <a name="successful-getevents-response-example"></a>Erfolgreiches GetEvents-Antwortbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel einer Antwort zeigt eine Benachrichtigung über das vorhanden sein zweier neuer e-Mail-Nachrichten, seit die letzte Benachrichtigungsanforderung an den Server gesendet wurde.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetEventsResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                       xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a>Comments

> [!NOTE]
> Die Element-und Ordner Bezeichner wurden verkürzt, um die Lesbarkeit zu erhalten. 
  
### <a name="getevents-response-elements"></a>GetEvents-Antwortelemente

In der Antwort werden folgende Elemente verwendet:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [GetEventsResponse](geteventsresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [GetEventsResponseMessage](geteventsresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Benachrichtigung](notification-ex15websvcsotherref.md)
    
- [Abonnement-Nr (GetEvents)](subscriptionid-getevents.md)
    
- [PreviousWatermark](previouswatermark.md)
    
- [MoreEvents](moreevents.md)
    
- [NewMailEvent](newmailevent.md)
    
- [Watermark](watermark.md)
    
- [Timestamp](timestamp.md)
    
- [ItemId](itemid.md)
    
- [ParentFolderId](parentfolderid.md)
    
Um andere Optionen für die Antwortnachricht des **GetEvents** -Vorgangs zu finden, erkunden Sie die Schemahierarchie. Beginnen Sie mit dem [Benachrichtigungs](notification-ex15websvcsotherref.md) Element. 
  
## <a name="getevents-error-response-example"></a>GetEvents-Fehlerantwort (Beispiel)

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine Fehlerantwort auf eine **GetEvents** -Anforderung. 
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
                 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                 xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetEventsResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

## <a name="remarks"></a>Bemerkungen

Bei der Verarbeitung einer **GetEvents** -Anforderung führt der Client Zugriffsserver die folgenden Schritte aus: 
  
1. Die Abonnement-Nr der Anforderung wird als gültiges Abonnement bestätigt, das auf dem Client Zugriffsserver gehostet wird. Wenn dies nicht der Fall ist, tritt beim **GetEvents** -Aufruf ein Fehler auf. 
    
2. Die SMTP-Adresse des authentifizierten Benutzers für die Anforderung wird mit der SMTP-Adresse des Benutzers verglichen, der das Abonnement erstellt hat. Wenn Sie nicht übereinstimmen, schlägt die **GetEvents** -Anforderung fehl. 
    
3. Die Abonnement Warteschlange wird für Ereignisse abgefragt, die darauf warten, an den Client gesendet zu werden. Wenn die Warteschlange nicht leer ist, werden die ersten 50-Ereignisse aus der Warteschlange aus der Warteschlange gezogen und in eine Benachrichtigung codiert.
    
4. Wenn in der Warteschlange keine Ereignisse gefunden werden, wird ein StatusEvent generiert und in einer Benachrichtigungsantwort codiert.
    
5. Die Benachrichtigungsantwort wird an den Client zurückgegeben.
    
6. Die Ereignisse, die in der Benachrichtigung enthalten sind, werden aus der Abonnement Warteschlange entfernt, und der lokale Client Zugriffsserver-letzte Wasserzeichen für das Abonnement wird auf das Wasserzeichen des letzten zurückgegebenen Ereignisses festgelegt.
    
7. Der Timeout-Zeitgeber für das Abonnement wird zurückgesetzt.
    
## <a name="see-also"></a>Siehe auch



[Vorgang abonnieren](subscribe-operation.md)
  
[Vorgang des Kündigens von Abonnements](unsubscribe-operation.md)


[Verwenden von Pullabonnements](https://msdn.microsoft.com/library/f956bc0e-2b25-4613-966b-54c65456897c%28Office.15%29.aspx)

