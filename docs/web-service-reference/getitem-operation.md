---
title: GetItem Operation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetItem
api_type:
- schema
ms.assetid: e3590b8b-c2a7-4dad-a014-6360197b68e4
description: Hier finden Sie Informationen zu den GetItem-EWS Vorgang.
ms.openlocfilehash: 9b63032b2eaa3bf26027a42e38bfa06bedcbac86
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758718"
---
# <a name="getitem-operation"></a>GetItem Operation

Hier finden Sie Informationen zu den **GetItem** -EWS-Vorgang. 
  
Die **GetItem** Operation ruft Elemente aus dem Exchange-Speicher ab. 
  
## <a name="using-the-getitem-operation"></a>Verwenden des GetItem-Vorgangs

Die **GetItem** Operation gibt viele Elementeigenschaften zurück. Die Eigenschaften, die in einer Antwort **GetItem** zurückgegeben werden hängen die angeforderte Form angeforderte zusätzliche Eigenschaften und den Typ des Elements zurückgegeben wird. 
  
[Nachrichtenelemente](message-ex15websvcsotherref.md) darstellen, e-Mail-Nachrichten und andere Elemente, die vom Exchange-Webdienste (EWS) Schema nicht stark typisiert sind. Elemente wie IPM.Sharing- und IPM.InfoPath-Elemente werden als [Message](message-ex15websvcsotherref.md)-Elemente zurückgegeben. Exchange gibt das [Element](item.md)-Basiselement nicht in Antworten zurück. 
  
Die **GetItem** Operation gibt keine Anlagen zurück. Es gibt Metadaten zu einem angefügte Element oder eine Datei zurück. Wenn eine Anlage zurückgeben möchten, verwenden Sie die [-Vorgangs GetAttachment](getattachment-operation.md).
  
## <a name="getitem-operation-soap-headers"></a>GetItem Operation SOAP-Header

Die **GetItem** Operation können die SOAP-Header, die in der folgenden Tabelle aufgelistet sind. 
  
|Kopfzeile ***|****Element****|****Beschreibung****|
|:-----|:-----|:-----|
|**DateTimePrecision** <br/> |[DateTimePrecision](datetimeprecision.md) <br/> |Gibt die Auflösung der Daten-/Uhrzeitwerte in Antworten vom Server an, entweder in Sekunden oder in Millisekunden.  <br/> |
|**Impersonation** <br/> |["ExchangeImpersonation"](exchangeimpersonation.md) <br/> |Identifiziert den Benutzer, für den die Clientanwendung einen Identitätswechsel durchführt.  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |Bezeichnet die Kultur gemäß Definition in RFC 3066, "Tags for the Identification des Languages", um Zugriff auf das Postfach verwendet werden.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Gibt die Schemaversion für die Vorgangsanforderung an.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Gibt die Version des Servers an, der auf die Anforderung geantwortet hat.  <br/> |
|**TimeZoneContext** <br/> |[TimeZoneContext](timezonecontext.md) <br/> |Gibt die Zeitzone für alle Antworten vom Server an.  <br/> |
   
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

[GetItem-Vorgang (e-Mail-Nachricht)](getitem-operation-email-message.md)
  
[GetItem-Vorgang (Kalenderelement)](getitem-operation-calendar-item.md)
  
[GetItem-Vorgang (Aufgabe)](getitem-operation-task.md)
  
[GetItem-Vorgang (Kontakt)](getitem-operation-contact.md)
  
## <a name="see-also"></a>Siehe auch



[EWS-Referenz für Exchange](ews-reference-for-exchange.md)

