---
title: GetStreamingEvents-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetStreamingEvents
api_type:
- schema
ms.assetid: 8da95423-72bc-4034-90a8-162eedcd059b
description: Hier finden Sie Informationen zum GetStreamingEvents-EWS-Vorgang.
ms.openlocfilehash: 27744ec40d7c7cb551f35ed5f6fcb726f23d4865
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530169"
---
# <a name="getstreamingevents-operation"></a>GetStreamingEvents-Vorgang

Hier finden Sie Informationen zum **GetStreamingEvents** -EWS-Vorgang. 
  
Der **GetStreamingEvents** -Vorgang wird von Streaming-Abonnementclients verwendet, um Benachrichtigungen vom Client Zugriffsserver anzufordern. Die **GetStreamingEvents** -Antwort gibt ein Array von Elementen und Ereignissen zurück, die seit der letzten Benachrichtigung in einem Postfach aufgetreten sind. 
  
## <a name="getstreamingevents-request-example"></a>GetStreamingEvents-Anforderungs Beispiel

### <a name="description"></a>Beschreibung

Im folgenden Beispiel eines **GetStreamingEvents** -Vorgangs wird gezeigt, wie die Ereignisse und Elemente angefordert werden, die einem Abonnement zugeordnet sind, das durch die Abonnement-ID identifiziert wird. 
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
  xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Body>
    <GetStreamingEvents xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <SubscriptionId>f6bc657d-dde1-4f94-952d-143b95d6483d</SubscriptionId>
      <ConnectionTimeout>30</ConnectionTimeout>
    </GetStreamingEvents>
  </soap:Body>
</soap:Envelope>
```

### <a name="getstreamingevents-request-elements"></a>GetStreamingEvents-anforderungselemente

In der Anforderung werden folgende Elemente verwendet:
  
- [GetStreamingEvents](getstreamingevents.md)
    
- [Abonnement-GetStreamingEvents](subscriptionid-getstreamingevents.md)
    
- [ConnectionTimeout](connectiontimeout.md)
    
## <a name="successful-getstreamingevents-response-example"></a>Erfolgreiches GetStreamingEvents-Antwortbeispiel

### <a name="description"></a>Beschreibung

Im folgenden Beispiel einer **GetStreamingEvents** -Antwort werden die Benachrichtigungen angezeigt, die an den Client gesendet werden, wenn eine neue e-Mail-Nachricht empfangen wird. Es enthält Benachrichtigungen für die folgenden Ereignisse: CreatedEvent, newmail und ModifiedEvent. 
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Header xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <ServerVersionInfo xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" MajorVersion="15" MinorVersion="0" MajorBuildNumber="775" MinorBuildNumber="7" Version="V2_4" xmlns="https://schemas.microsoft.com/exchange/services/2006/types" />
</soap:Header>
<soap:Body xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <m:GetStreamingEventsResponse xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
    <m:ResponseMessages>
      <m:GetStreamingEventsResponseMessage ResponseClass="Success">
        <m:ResponseCode>NoError</m:ResponseCode>
        <m:Notifications>
          <m:Notification>
            <t:SubscriptionId>f6bc657d-dde1-4f94-952d-143b95d6483d</t:SubscriptionId>
            <t:CreatedEvent>
              <t:TimeStamp>2013-09-16T04:31:29Z</t:TimeStamp>
              <t:ItemId Id="AAMkADkzNjJjODUzLWZhMDMtNDVkMS05ZDdjLWVmMDlkYjQ1Zjc4MwBGAAAAAABSSWVKrmGUTJE+MVIvofglBwDZGACZQpSgSpyNkexYe2b7AAAAAAENAADZGACZQpSgSpyNkexYe2b7AAANGFYwAAA=" ChangeKey="CQAAAA==" />
              <t:ParentFolderId Id="AQMkADkzNjJjODUzLWZhMDMtNDVkMS05ZDdjLWVmMDlkYjQ1Zjc4MwAuAAADUkllSq5hlEyRPjFSL6H4JQEA2RgAmUKUoEqcjZHsWHtm+wAAAgENAAAA" ChangeKey="AQAAAA==" />
            </t:CreatedEvent>
            <t:NewMailEvent>
              <t:TimeStamp>2013-09-16T04:31:29Z</t:TimeStamp>
              <t:ItemId Id="AAMkADkzNjJjODUzLWZhMDMtNDVkMS05ZDdjLWVmMDlkYjQ1Zjc4MwBGAAAAAABSSWVKrmGUTJE+MVIvofglBwDZGACZQpSgSpyNkexYe2b7AAAAAAENAADZGACZQpSgSpyNkexYe2b7AAANGFYwAAA=" ChangeKey="CQAAAA==" />
              <t:ParentFolderId Id="AQMkADkzNjJjODUzLWZhMDMtNDVkMS05ZDdjLWVmMDlkYjQ1Zjc4MwAuAAADUkllSq5hlEyRPjFSL6H4JQEA2RgAmUKUoEqcjZHsWHtm+wAAAgENAAAA" ChangeKey="AQAAAA==" />
            </t:NewMailEvent>
            <t:ModifiedEvent>
              <t:TimeStamp>2013-09-16T04:31:29Z</t:TimeStamp>
              <t:FolderId Id="AQMkADkzNjJjODUzLWZhMDMtNDVkMS05ZDdjLWVmMDlkYjQ1Zjc4MwAuAAADUkllSq5hlEyRPjFSL6H4JQEA2RgAmUKUoEqcjZHsWHtm+wAAAgENAAAA" ChangeKey="AQAAAA==" />
              <t:ParentFolderId Id="AQMkADkzNjJjODUzLWZhMDMtNDVkMS05ZDdjLWVmMDlkYjQ1Zjc4MwAuAAADUkllSq5hlEyRPjFSL6H4JQEA2RgAmUKUoEqcjZHsWHtm+wAAAgEJAAAA" ChangeKey="AQAAAA==" />
              <t:UnreadCount>1</t:UnreadCount>
            </t:ModifiedEvent>
          </m:Notification>
        </m:Notifications>
      </m:GetStreamingEventsResponseMessage>
    </m:ResponseMessages>
  </m:GetStreamingEventsResponse>
</soap:Body>
```

### <a name="getstreamingevents-response-elements"></a>GetStreamingEvents-Antwortelemente

In der Antwort werden folgende Elemente verwendet:
  
- [GetStreamingEventsResponse](getstreamingeventsresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [GetStreamingEventsResponseMessage](getstreamingeventsresponsemessage.md)
    
- [NotesFolderPermissionLevel](notesfolderpermissionlevel.md)
    
- [Benachrichtigung](notification-ex15websvcsotherref.md)
    
- [Abonnement-GetStreamingEvents](subscriptionid-getstreamingevents.md)
    
Um andere Optionen für die Antwortnachricht des **GetStreamingEvents** -Vorgangs zu finden, erkunden Sie die Schemahierarchie. Beginnen Sie mit dem [Benachrichtigungs](notification-ex15websvcsotherref.md) Element. 
  
## <a name="getstreamingevents-error-response-example"></a>GetStreamingEvents-Fehlerantwort Beispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine Fehlerantwort auf eine **GetStreamingEvents** -Anforderung. 
  
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
    <GetStreamingEventsResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                       xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:GetStreamingEventsResponseMessage ResponseClass="Error">
        <m:MessageText></m:MessageText>
        <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        <m:ResponseCode>ErrorInvalidSubscription</m:ResponseCode>
        <m:ConnectionStatus>Closed</m:ConnectionStatus>
      </m:ResponseMessages>
    </GetStreamingEventsResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="remarks"></a>Bemerkungen

Bei der Verarbeitung einer **GetStreamingEvents** -Anforderung führt der Client Zugriffsserver die folgenden Schritte aus: 
  
1. Die [Abonnement-GetStreamingEvents](subscriptionid-getstreamingevents.md) der Anforderung wird als gültiges Abonnement bestätigt, das auf dem Client Zugriffsserver gehostet wird. Wenn dies nicht der Fall ist, schlägt der **GetStreamingEvents** -Aufruf fehl. 
    
2. Die SMTP-Adresse des authentifizierten Benutzers für die Anforderung wird überprüft, um Identitätswechsel Rechte zu besitzen. Wenn dies nicht der Fall ist, schlägt die **GetStreamingEvents** -Anforderung fehl. 
    
3. Die Abonnement Warteschlange wird für Ereignisse abgefragt, die darauf warten, an den Client gesendet zu werden. Wenn die Warteschlange nicht leer ist, werden die ersten 50-Ereignisse aus der Warteschlange aus der Warteschlange gezogen und in eine Benachrichtigung codiert.
    
4. Wenn in der Warteschlange keine Ereignisse gefunden werden, wird ein [StatusEvent](statusevent.md) generiert und in einer Benachrichtigungsantwort codiert. 
    
5. Die Benachrichtigungsantwort wird an den Client zurückgegeben.
    
6. Die Ereignisse, die in der Benachrichtigung enthalten sind, werden aus der Abonnement Warteschlange entfernt, und der Client Zugriffsserver-lokales letzte Wasserzeichen für das Abonnement wird auf das Wasserzeichen des letzten zurückgegebenen Ereignisses festgelegt.
    
7. Der Timeout-Zeitgeber für das Abonnement wird zurückgesetzt.
    
## <a name="see-also"></a>Siehe auch



[Vorgang abonnieren](subscribe-operation.md)
  
[Vorgang des Kündigens von Abonnements](unsubscribe-operation.md)

