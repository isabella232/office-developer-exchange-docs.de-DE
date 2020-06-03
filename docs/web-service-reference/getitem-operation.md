---
title: GetItem-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
api_name:
- GetItem
api_type:
- schema
ms.assetid: e3590b8b-c2a7-4dad-a014-6360197b68e4
description: Hier finden Sie Informationen zum GetItem-EWS-Vorgang.
localization_priority: Priority
ms.openlocfilehash: 8871dde183974454fc27dbddda489e6b0a70f3aa
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463328"
---
# <a name="getitem-operation"></a>GetItem-Vorgang

Hier finden Sie Informationen zum **GetItem** -EWS-Vorgang. 
  
Der **GetItem** -Vorgang ruft Elemente aus dem Exchange-Informationsspeicher ab. 
  
## <a name="using-the-getitem-operation"></a>Verwenden des GetItem-Vorgangs

Der **GetItem** -Vorgang gibt viele Elementeigenschaften zurück. Die Eigenschaften, die in einer **GetItem** -Antwort zurückgegeben werden, variieren basierend auf der angeforderten Form, den angeforderten zusätzlichen Eigenschaften und dem Typ des zurückgegebenen Elements. 
  
[Nachrichten](message-ex15websvcsotherref.md) Elemente stellen e-Mail-Nachrichten und alle anderen Elemente dar, die nicht stark vom Exchange-Webdienste Schema eingegeben werden. Elemente wie IPM.Sharing- und IPM.InfoPath-Elemente werden als [Message](message-ex15websvcsotherref.md)-Elemente zurückgegeben. Exchange gibt das [Element](item.md)-Basiselement nicht in Antworten zurück. 
  
Der **GetItem** -Vorgang gibt keine Anlagen zurück. Es werden Metadaten zu einem angefügten Element oder einer Datei zurückgegeben. Verwenden Sie den [GetAttachment-Vorgang](getattachment-operation.md), um eine Anlage zurückzugeben.
  
## <a name="getitem-operation-soap-headers"></a>GetItem-Vorgangs-SOAP-Header

Der **GetItem** -Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind. 
  
|Kopfzeile * * * *|****Element****|****Beschreibung****|
|:-----|:-----|:-----|
|**DateTimePrecision** <br/> |[DateTimePrecision](datetimeprecision.md) <br/> |Gibt die Auflösung der Daten-/Uhrzeitwerte in Antworten vom Server an, entweder in Sekunden oder in Millisekunden.  <br/> |
|**Impersonation** <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt.  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |Identifiziert die Kultur gemäß der Definition in RFC 3066, "Tags für die Identifizierung von Sprachen", die für den Zugriff auf das Postfach verwendet werden sollen.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Gibt die Schemaversion für die Vorgangsanforderung an.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.  <br/> |
|**TimeZoneContext** <br/> |[TimeZoneContext](timezonecontext.md) <br/> |Gibt die Zeitzone für alle Antworten vom Server an.  <br/> |
   
## <a name="in-this-section"></a>In diesem Abschnitt

[GetItem-Vorgang (e-Mail-Nachricht)](getitem-operation-email-message.md)
  
[GetItem-Vorgang (Kalenderelement)](getitem-operation-calendar-item.md)
  
[GetItem-Vorgang (Aufgabe)](getitem-operation-task.md)
  
[GetItem-Vorgang (Kontakt)](getitem-operation-contact.md)
  
## <a name="see-also"></a>Siehe auch



[EWS-Referenz für Exchange](ews-reference-for-exchange.md)

