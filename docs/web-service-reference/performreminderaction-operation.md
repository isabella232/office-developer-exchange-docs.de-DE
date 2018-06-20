---
title: PerformReminderAction-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c597bb0e-13b0-422e-9c23-970463e2a5c3
description: Hier finden Sie Informationen über die PerformReminderAction EWS Vorgang.
ms.openlocfilehash: 778fbb508413721f58cfcf9143a5296874e6cd1c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830722"
---
# <a name="performreminderaction-operation"></a>PerformReminderAction-Vorgang

Hier finden Sie Informationen zum **PerformReminderAction** EWS-Vorgang. 
  
Der Vorgang des **PerformReminderAction** Exchange-Webdienste (EWS) initiiert eine Aktion schließen oder erneut erinnern auf eine Erinnerung. 
  
Dieser Vorgang wurde in Exchange Server 2013 eingeführt.
  
## <a name="using-the-performreminderaction-operation"></a>Verwenden des PerformReminderAction-Vorgangs

Den Vorgang **PerformReminderAction** können Sie schließen oder erneut erinnern (Verzögerung) Erinnerungen durch den Vorgang [GetReminders](getreminders-operation.md) zurückgegeben. Um eine Erinnerung snooze, die [ActionType](actiontype-reminderactiontype.md) auf **erneut erinnern**, und legen Sie den [NewReminderTime](newremindertime.md) Wert auf einen Zeitpunkt höher als die aktuelle [ReminderTime](remindertime.md)andernfalls die **NewReminderTime** wird vom Server ignoriert. Wenn die Erinnerung für ein Vorkommen einer Besprechungsserie wird und der **erneut erinnern** Aktionen auf die Erinnerung mit einer **NewReminderTime** , die die Erinnerung an das nächste Vorkommen überschreitet, wird die Erinnerung effektiv geschlossen. 
  
Um eine Erinnerung zu schließen, legen Sie die **ActionType** auf **Schließen**. Wenn der Server die Anforderung verarbeitet, ändert der Server den [IsReminderSet](isreminderset.md) Wert für das Element von **True** auf **false festgelegt**.
  
### <a name="performreminderaction-operation-soap-headers"></a>PerformReminderAction Vorgang SOAP-Header

Der Vorgang **PerformReminderAction** können die SOAP-Header, die in der folgenden Tabelle aufgelistet sind. 
  
|**Headername**|**Element**|**Beschreibung**|
|:-----|:-----|:-----|
|**Impersonation** <br/> |["ExchangeImpersonation"](exchangeimpersonation.md) <br/> |Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt. Diese Kopfzeile gilt für eine Anforderung.  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |Bezeichnet die Kultur gemäß Definition in RFC 3066, "Tags for the Identification des Languages", um Zugriff auf das Postfach verwendet werden. Diese Kopfzeile gilt für eine Anforderung.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Gibt die Schemaversion für die Vorgangsanforderung an. Diese Kopfzeile gilt für eine Anforderung.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Gibt die Version des Servers an, der auf die Anforderung geantwortet hat. Diese Kopfzeile gilt für eine Antwort.  <br/> |
   
## <a name="performreminderaction-operation-request-example"></a>PerformReminderAction Vorgang anforderungsbeispiel

Im folgenden Beispiel wird eine **PerformReminderAction** Vorgang Anforderung veranschaulicht eine aktuelle Erinnerung snooze, und legen Sie eine neue Erinnerungszeit. Beachten Sie, dass Sie die **ChangeKey** für die [ItemId](itemid.md) schließen müssen und die **NewReminderTime** auf einen Zeitpunkt höher als die durch den Vorgang [GetReminders](getreminders-operation.md) zurückgegebenen **ReminderTime** festgelegt werden muss. 
  
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
> Der **ItemId** -Wert wurde gekürzt, um die Lesbarkeit zu erhalten. 
  
Die Anforderung SOAP-Text enthält die folgenden Elemente:
  
- [PerformReminderAction](performreminderaction.md)
    
- [ReminderItemActions](reminderitemactions.md)
    
- [ReminderItemAction](reminderitemaction.md)
    
- [ActionType](actiontype-reminderactiontype.md)
    
- [ItemId](itemid.md)
    
- [NewReminderTime](newremindertime.md)
    
## <a name="successful-performreminderaction-operation-response"></a>Erfolgreiche PerformReminderAction Vorgangsantwort

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine **PerformReminderAction** Vorgang an. Das **UpdatedItemIds** -Element enthält die **Artikelnummern ein.** des aktualisierten Kalenderelements. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <ServerVersionInfo MajorVersion="15"
                       MinorVersion="0"
                       MajorBuildNumber="921"
                       MinorBuildNumber="20"
                       Version="V2_10"
                       xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <PerformReminderActionResponse ResponseClass="Success"
                                   xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <UpdatedItemIds>
        <ItemId Id="vwAAAA=="
                ChangeKey="DwAAABYAAAB4to43JyybTYwHLBM1k8MxAAAJKP+S"/>
      </UpdatedItemIds>
    </PerformReminderActionResponse>
  </s:Body>
</s:Envelope>
```

Die Antwort SOAP-Text enthält die folgenden Elemente:
  
- [PerformReminderActionResponse](performreminderactionresponse.md)
    
- [ResponseCode](responsecode.md)
    
- [UpdatedItemIds](updateditemids.md)
    
- [ItemId](itemid.md)
    
## <a name="performreminderaction-operation-error-response-example"></a>PerformReminderAction Vorgang Fehler antwortbeispiel

Das folgende Beispiel zeigt eine Antwort auf eine **PerformReminderAction** Vorgang an, wenn auf dem Server keine Änderung vorgenommen wurde. Dies ist eine Antwort, in denen eine Anforderung gesendet wurde, aber keine **UpdatedItemIds** wurden zurückgegeben, was bedeutet, dass keine Erinnerungen geändert wurden. 
  
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
    <PerformReminderActionResponse ResponseClass="Success"
                                   xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <UpdatedItemIds />
    </PerformReminderActionResponse>
  </s:Body>
</s:Envelope>
```

Die SOAP-Body-Fehlerantwort enthält die folgenden Elemente:
  
- [PerformReminderActionResponse](performreminderactionresponse.md)
    
- [ResponseCode](responsecode.md)
    
- [UpdatedItemIds](updateditemids.md)
    
Zusätzliche Fehlercodes, die für EWS generisch sind, finden Sie unter [ResponseCode](responsecode.md).
  
## <a name="see-also"></a>Siehe auch


- [GetReminders-Vorgang](getreminders-operation.md)
    

