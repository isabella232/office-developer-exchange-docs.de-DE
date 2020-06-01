---
title: PerformReminderAction-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c597bb0e-13b0-422e-9c23-970463e2a5c3
description: Hier finden Sie Informationen zum PerformReminderAction-EWS-Vorgang.
ms.openlocfilehash: 4c069d541e9a42167c447a50c405399958d3608d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462290"
---
# <a name="performreminderaction-operation"></a>PerformReminderAction-Vorgang

Hier finden Sie Informationen zum **PerformReminderAction** -EWS-Vorgang. 
  
Die **PerformReminderAction** -Exchange-Webdienste Operation initiiert eine Kündigungs-oder Snooze-Aktion für eine Erinnerung. 
  
Dieser Vorgang wurde in Exchange Server 2013 eingeführt.
  
## <a name="using-the-performreminderaction-operation"></a>Verwenden des PerformReminderAction-Vorgangs

Sie können den **PerformReminderAction** -Vorgang verwenden, um Erinnerungen, die von der [geterinnerungs](getreminders-operation.md) -Operation zurückgegeben werden, zu schließen oder zu Snooze (Delay). Um eine Erinnerung zu snoozen, legen Sie den [Action](actiontype-reminderactiontype.md) Type auf **Snooze**fest, und legen Sie den Wert für die [neumahnung](newremindertime.md) auf einen Zeitpunkt nach der aktuellen [Erinnerungs](remindertime.md)Zeit fest, andernfalls wird die **neuerinnerung** vom Server ignoriert. Wenn es sich bei der Erinnerung um ein Auftreten einer Besprechungsserie handelt und die **Snooze** -Aktion in der Erinnerung mit einer Erinnerungszeit angezeigt **wird, die** über die Erinnerung an das nächste Vorkommen verfügt, wird die Erinnerung effektiv zurückgewiesen. 
  
Um eine Erinnerung zu schließen, legen Sie den **Action** Type auf **entlassen**fest. Wenn der Server die Anforderung verarbeitet, ändert der Server den [Reminder](isreminderset.md) -Wert für das Element von **true** in **false**.
  
### <a name="performreminderaction-operation-soap-headers"></a>SOAP-Header des PerformReminderAction-Vorgangs

Der **PerformReminderAction** -Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind. 
  
|**Headername**|**Element**|**Beschreibung**|
|:-----|:-----|:-----|
|**Impersonation** <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt. Diese Kopfzeile gilt für eine Anforderung.  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |Identifiziert die Kultur gemäß der Definition in RFC 3066, "Tags für die Identifizierung von Sprachen", die für den Zugriff auf das Postfach verwendet werden sollen. Diese Kopfzeile gilt für eine Anforderung.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Gibt die Schemaversion für die Vorgangsanforderung an. Diese Kopfzeile gilt für eine Anforderung.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Gibt die Version des Servers an, der auf die Anforderung geantwortet hat. Diese Kopfzeile gilt für eine Antwort.  <br/> |
   
## <a name="performreminderaction-operation-request-example"></a>PerformReminderAction-Vorgangsanforderung (Beispiel)

Im folgenden Beispiel einer **PerformReminderAction** -Vorgangsanforderung wird gezeigt, wie eine aktuelle Erinnerung eingeschlummert und eine neue Erinnerungszeit festgelegt wird. Beachten Sie, dass Sie das **ChangeKey** -Objekt für [das Itemid](itemid.md) -Objekt einschließen müssen und die **Reminder** -Uhrzeit auf eine Zeitspanne festgelegt sein muss, die von der **Reminders** [-Operation zurück](getreminders-operation.md) gegeben wird. 
  
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
    <m:PerformReminderAction>
      <m:ReminderItemActions>
        <t:ReminderItemAction>
          <t:ActionType>Snooze</t:ActionType>
          <t:ItemId Id="vwAAAA=="
           ChangeKey="DwAAABQAAACOs0HEMq1WTKpI7sNu5qXNAAAUDA=="/>
          <t:NewReminderTime>2014-04-16T17:00:00Z</t:NewReminderTime>
        </t:ReminderItemAction>
      </m:ReminderItemActions>
    </m:PerformReminderAction>
  </soap:Body>
</soap:Envelope>
```

> [!NOTE]
> Der **ItemID** -Wert wurde verkürzt, um die Lesbarkeit beizubehalten. 
  
Der SOAP-Anforderungstext Körper enthält die folgenden Elemente:
  
- [PerformReminderAction](performreminderaction.md)
    
- [ReminderItemActions](reminderitemactions.md)
    
- [ReminderItemAction](reminderitemaction.md)
    
- [ActionType](actiontype-reminderactiontype.md)
    
- [ItemId](itemid.md)
    
- [Neuerinnerung](newremindertime.md)
    
## <a name="successful-performreminderaction-operation-response"></a>Erfolgreiche Reaktion des PerformReminderAction-Vorgangs

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **PerformReminderAction** -Vorgangsanforderung. Das **UpdatedItemIds** -Element enthält die **itemids** des aktualisierten Kalenderelements. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <ServerVersionInfo MajorVersion="15"
                       MinorVersion="0"
                       MajorBuildNumber="921"
                       MinorBuildNumber="20"
                       Version="V2_10"
                       xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <PerformReminderActionResponse ResponseClass="Success"
                                   xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <UpdatedItemIds>
        <ItemId Id="vwAAAA=="
                ChangeKey="DwAAABYAAAB4to43JyybTYwHLBM1k8MxAAAJKP+S"/>
      </UpdatedItemIds>
    </PerformReminderActionResponse>
  </s:Body>
</s:Envelope>
```

Der SOAP-Antworttext Körper enthält die folgenden Elemente:
  
- [PerformReminderActionResponse](performreminderactionresponse.md)
    
- [ResponseCode](responsecode.md)
    
- [UpdatedItemIds](updateditemids.md)
    
- [ItemId](itemid.md)
    
## <a name="performreminderaction-operation-error-response-example"></a>PerformReminderAction-Operation-Fehlerantwort (Beispiel)

Das folgende Beispiel zeigt eine Antwort auf eine **PerformReminderAction** -Vorgangsanforderung, wenn keine Änderung auf dem Server vorgenommen wurde. Dies ist eine Antwort, bei der eine Anforderung gesendet wurde, aber keine **UpdatedItemIds** zurückgegeben wurden, was bedeutet, dass keine Erinnerungen geändert wurden. 
  
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
    <PerformReminderActionResponse ResponseClass="Success"
                                   xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <UpdatedItemIds />
    </PerformReminderActionResponse>
  </s:Body>
</s:Envelope>
```

Der SOAP-Textkörper der Fehlerantwort enthält die folgenden Elemente:
  
- [PerformReminderActionResponse](performreminderactionresponse.md)
    
- [ResponseCode](responsecode.md)
    
- [UpdatedItemIds](updateditemids.md)
    
Weitere Fehlercodes, die für EWS allgemein sind, finden Sie unter [Response Code](responsecode.md).
  
## <a name="see-also"></a>Siehe auch


- [GetReminders-Vorgang](getreminders-operation.md)
    

