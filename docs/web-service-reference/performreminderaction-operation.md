---
title: PerformReminderAction-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: c597bb0e-13b0-422e-9c23-970463e2a5c3
description: Hier finden Sie Informationen zum EWS-Vorgang "PerformReminderAction".
ms.openlocfilehash: ca547c401100afdfd9d846ca3bfddf710efd2797
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59515306"
---
# <a name="performreminderaction-operation"></a>PerformReminderAction-Vorgang

Hier finden Sie Informationen zum **EWS-Vorgang "PerformReminderAction".** 
  
Der EWS-Vorgang **(PerformReminderAction** Exchange Web Services) initiiert eine Aktion zum Schließen oder erneuten Erinnern einer Erinnerung. 
  
Dieser Vorgang wurde in Exchange Server 2013 eingeführt.
  
## <a name="using-the-performreminderaction-operation"></a>Verwenden des PerformReminderAction-Vorgangs

Sie können den **PerformReminderAction-Vorgang** verwenden, um Erinnerungen, die vom [GetReminders-Vorgang](getreminders-operation.md) zurückgegeben werden, zu schließen oder erneut zu erinnern (zurückgestellt). Wenn Sie eine Erinnerung erneut erinnern möchten, legen Sie den [ActionType](actiontype-reminderactiontype.md) auf **"Erneut erinnern"** fest, und legen Sie den [NewReminderTime-Wert](newremindertime.md) auf einen späteren Zeitpunkt als die aktuelle [ReminderTime](remindertime.md)fest, **andernfalls wird NewReminderTime** vom Server ignoriert. Wenn es sich bei der Erinnerung um ein Vorkommen einer Besprechungsserie handelt und **die** Erneute Erinnerung mit einer **NewReminderTime** ausgeführt wird, die über die Erinnerung des nächsten Vorkommens hinaus liegt, wird die Erinnerung effektiv geschlossen. 
  
Um eine Erinnerung zu schließen, legen **Sie actionType** auf **"Schließen"** fest. Wenn der Server die Anforderung verarbeitet, ändert der Server den [IsReminderSet-Wert](isreminderset.md) für das Element von **"True"** in **"False".**
  
### <a name="performreminderaction-operation-soap-headers"></a>PerformReminderAction-Vorgang SOAP-Header

Der **PerformReminderAction-Vorgang** kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind. 
  
|**Headername**|**Element**|**Beschreibung**|
|:-----|:-----|:-----|
|**Impersonation** <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt. Dieser Header gilt für eine Anforderung.  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |Identifiziert die Kultur, wie in RFC 3066 definiert, "Tags für die Identifizierung von Sprachen", die für den Zugriff auf das Postfach verwendet werden soll. Dieser Header gilt für eine Anforderung.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Gibt die Schemaversion für die Vorgangsanforderung an. Dieser Header gilt für eine Anforderung.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Gibt die Version des Servers an, der auf die Anforderung geantwortet hat. Dieser Header gilt für eine Antwort.  <br/> |
   
## <a name="performreminderaction-operation-request-example"></a>Beispiel für PerformReminderAction-Vorgangsanforderung

Das folgende Beispiel einer **PerformReminderAction-Vorgangsanforderung** zeigt, wie Sie eine aktuelle Erinnerung erneut erinnern und eine neue Erinnerungszeit festlegen. Beachten Sie, dass Sie den **ChangeKey** für die [ItemId](itemid.md) einschließen müssen, und **newReminderTime** muss auf eine Uhrzeit später als die **reminderTime** festgelegt werden, die vom [GetReminders-Vorgang](getreminders-operation.md) zurückgegeben wird. 
  
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
> Der **ItemId-Wert** wurde gekürzt, um die Lesbarkeit zu gewährleisten. 
  
Der SOAP-Anforderungstext enthält die folgenden Elemente:
  
- [PerformReminderAction](performreminderaction.md)
    
- [ReminderItemActions](reminderitemactions.md)
    
- [ReminderItemAction](reminderitemaction.md)
    
- [ActionType](actiontype-reminderactiontype.md)
    
- [ItemId](itemid.md)
    
- [NewReminderTime](newremindertime.md)
    
## <a name="successful-performreminderaction-operation-response"></a>Erfolgreiche PerformReminderAction-Vorgangsantwort

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **PerformReminderAction-Vorgangsanforderung.** Das **UpdatedItemIds-Element** enthält die **ItemIds des aktualisierten Kalenderelements.** 
  
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

Der SOAP-Antworttext enthält die folgenden Elemente:
  
- [PerformReminderActionResponse](performreminderactionresponse.md)
    
- [ResponseCode](responsecode.md)
    
- [UpdatedItemIds](updateditemids.md)
    
- [ItemId](itemid.md)
    
## <a name="performreminderaction-operation-error-response-example"></a>Beispiel für Die Fehlerantwort des PerformReminderAction-Vorgangs

Das folgende Beispiel zeigt eine Antwort auf eine **PerformReminderAction-Vorgangsanforderung,** wenn keine Änderung auf dem Server vorgenommen wurde. Dies ist eine Antwort, in der eine Anforderung gesendet wurde, aber keine **UpdatedItemIds** zurückgegeben wurden, was bedeutet, dass keine Erinnerungen geändert wurden. 
  
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
    
Weitere Fehlercodes, die für EWS generisch sind, finden Sie unter [ResponseCode](responsecode.md).
  
## <a name="see-also"></a>Siehe auch


- [GetReminders-Vorgang](getreminders-operation.md)
    

