---
title: GetEvents-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- GetEvents
api_type:
- schema
ms.assetid: f268efe5-9a1a-41a2-b6a6-51fcde7720a1
description: Der GetEvents-Vorgang wird von Pullabonnementclients verwendet, um Benachrichtigungen vom Clientzugriffsserver anzufordern. Die GetEvents-Vorgangsantwort gibt ein Array von Elementen und Ereignissen zurück, die seit der letzten Benachrichtigung in einem Postfach aufgetreten sind.
ms.openlocfilehash: 72d99a654921794115d56d28327a39a21c9ea378
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59511600"
---
# <a name="getevents-operation"></a>GetEvents-Vorgang

Der **GetEvents-Vorgang** wird von Pullabonnementclients verwendet, um Benachrichtigungen vom Clientzugriffsserver anzufordern. Die **GetEvents-Vorgangsantwort** gibt ein Array von Elementen und Ereignissen zurück, die seit der letzten Benachrichtigung in einem Postfach aufgetreten sind. 
  
> [!IMPORTANT]
> Der **DeleteUserConfiguration-Vorgang** löst ein Verschiebungsereignis für das Ereignisbenachrichtigungssystem aus. Das Benutzerkonfigurationsobjekt wird in den Dumpster verschoben. 
  
## <a name="notes"></a>Notizen

Änderungen an Kalenderelementen können zur Generierung mehrerer Ereignisse führen. Diese Ereignisse sind das Ergebnis der Erstellung temporärer Elemente im Postfach, von Frei/Gebucht-Datenspeicherelementen, die im Rahmen der normalen Kalendervorgänge geändert werden, oder beides. Ereignisse für die Elementklasse "IPM. SchedulePlus.FreeBusy.BinaryData" sollte von Webdienstclients ignoriert werden. Diese temporären Elemente werden gelöscht, nachdem sie erstellt wurden. Wenn daher versucht wird, diese Elemente abzurufen, wird ein Fehler zurückgegeben, der angibt, dass das Element nicht gefunden wurde.
  
## <a name="getevents-request-example"></a>GetEvents-Anforderungsbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt, wie Sie die Ereignisse und Elemente anfordern, die einem Abonnement zugeordnet sind, das durch die Abonnement-ID und das Wasserzeichen identifiziert wird.
  
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

### <a name="getevents-request-elements"></a>GetEvents-Anforderungselemente

In der Anforderung werden folgende Elemente verwendet:
  
- [GetEvents](getevents.md)
    
- [SubscriptionId (GetEvents)](subscriptionid-getevents.md)
    
- [Watermark](watermark.md)
    
## <a name="successful-getevents-response-example"></a>Beispiel für erfolgreiche GetEvents-Antwort

### <a name="description"></a>Beschreibung

Das folgende Beispiel einer Antwort zeigt eine Benachrichtigung über das Vorhandensein von zwei neuen E-Mail-Nachrichten seit dem Senden der letzten Benachrichtigungsanforderung an den Server.
  
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
> Die Element- und Ordnerbezeichner wurden gekürzt, um die Lesbarkeit zu gewährleisten. 
  
### <a name="getevents-response-elements"></a>GetEvents-Antwortelemente

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
    
- [Watermark](watermark.md)
    
- [TimeStamp](timestamp.md)
    
- [ItemId](itemid.md)
    
- [ParentFolderId](parentfolderid.md)
    
Weitere Optionen für die Antwortnachricht des **GetEvents-Vorgangs** finden Sie in der Schemahierarchie. Beginnen Sie mit dem [Notification-Element.](notification-ex15websvcsotherref.md) 
  
## <a name="getevents-error-response-example"></a>GetEvents-Fehlerantwortbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine Fehlerantwort auf eine **GetEvents-Anforderung.** 
  
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

## <a name="remarks"></a>HinwBemerkungeneise

Bei der Verarbeitung einer **GetEvents-Anforderung** führt der Clientzugriffsserver die folgenden Schritte aus: 
  
1. Die SubscriptionID der Anforderung wird als gültiges Abonnement bestätigt, das auf dem Clientzugriffsserver gehostet wird. Ist dies nicht der Typ, schlägt der **GetEvents-Aufruf** fehl. 
    
2. Die SMTP-Adresse des authentifizierten Benutzers für die Anforderung wird mit der SMTP-Adresse des Benutzers verglichen, der das Abonnement erstellt hat. Wenn sie nicht übereinstimmen, schlägt die **GetEvents-Anforderung** fehl. 
    
3. Die Abonnementwarteschlange wird nach Ereignissen abgefragt, die darauf warten, an den Client gesendet zu werden. Wenn die Warteschlange nicht leer ist, werden die ersten 50 Ereignisse aus der Warteschlange aus der Warteschlange abgerufen und in eine Benachrichtigung codiert.
    
4. Wenn in der Warteschlange keine Ereignisse gefunden werden, wird ein StatusEvent generiert und in eine Benachrichtigungsantwort codiert.
    
5. Die Benachrichtigungsantwort wird an den Client zurückgegeben.
    
6. Die Ereignisse, die in der Benachrichtigung enthalten sind, werden aus der Abonnementwarteschlange entfernt, und das lokale letzte Wasserzeichen des Clientzugriffsservers für das Abonnement wird auf das Wasserzeichen des letzten zurückgegebenen Ereignisses festgelegt.
    
7. Der Timeouttimer für das Abonnement wird zurückgesetzt.
    
## <a name="see-also"></a>Siehe auch



[Vorgang abonnieren](subscribe-operation.md)
  
[Vorgang des Kündigens von Abonnements](unsubscribe-operation.md)


[Verwenden von Pullabonnements](https://msdn.microsoft.com/library/f956bc0e-2b25-4613-966b-54c65456897c%28Office.15%29.aspx)

