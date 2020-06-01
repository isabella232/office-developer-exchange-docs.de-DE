---
title: ReceivedRepresenting
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ReceivedRepresenting
api_type:
- schema
ms.assetid: 1157b042-6dce-4cdc-9700-e22b749da39f
description: Das ReceivedRepresenting-Element identifiziert den Prinzipal in einem Stellvertretungs-Zugriffs Szenario.
ms.openlocfilehash: f444fb88be9c0df174f0c1490cf7c499cc0c0539
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468222"
---
# <a name="receivedrepresenting"></a>ReceivedRepresenting

Das **ReceivedRepresenting** -Element identifiziert den Prinzipal in einem Stellvertretungs-Zugriffs Szenario. 
  
```xml
<ReceivedRepresenting>
   <Mailbox/>
</ReceivedRepresenting>
```

 **SingleRecipientType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Postfach](mailbox.md) <br/> |Ein e-Mail-aktivierten Active Directory Directory Service-Objekt identifiziert.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Message](message-ex15websvcsotherref.md) <br/> |Stellt eine Exchange-E-Mail-Nachricht dar.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Stellt eine Besprechung im Exchange-Informationsspeicher dar.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Stellt eine Besprechungsantwort im Exchange-Informationsspeicher dar.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Stellt eine Besprechungsabsage im Exchange-Informationsspeicher dar.  <br/> |
|[AcceptItem](acceptitem.md) <br/> |Stellt eine Accept-Antwort auf eine Besprechungsanfrage.  <br/> |
|[TentativelyAcceptItem](tentativelyacceptitem.md) <br/> |Stellt eine mit Vorbehalt Antworten auf eine Besprechungsanfrage.  <br/> |
|[DeclineItem](declineitem.md) <br/> |Stellt eine ablehnen Antwort auf eine Besprechungsanfrage.  <br/> |
|[ReplyToItem](replytoitem.md) <br/> |Enthält eine Antwort an den Ersteller eines Elements in der Exchange-Speicher.  <br/> |
|[ReplyAllToItem](replyalltoitem.md) <br/> |Enthält eine Antwort an alle identifizierten Empfänger eines Elements in der Exchange-Speicher.  <br/> |
|[ForwardItem](forwarditem.md) <br/> |Enthält ein Exchange-Speicher-Element an Empfänger weitergeleitet.  <br/> |
|[CancelCalendarItem](cancelcalendaritem.md) <br/> |Stellt das Antwortobjekt, das Sie eine Besprechung absagen verwendet wird.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Das **ReceivedRepresenting** -Element wird zusammen mit den **from** -und **ReceivedBy** -Elementen in Stellvertretungs-Zugriffsszenarien verwendet. In der folgenden Tabelle sind die Entitäten aufgeführt, die diese Elemente in einem Stellvertretungs-Zugriffs Szenario darstellen. 
  
**Elemente in einem Szenario mit Stellvertretungszugriff**

|**Element**|**Entität, die das Element darstellt**|
|:-----|:-----|
|[From](from.md) <br/> |ThirdParty  <br/> |
|[ReceivedBy](receivedby.md) <br/> |Stellvertretung  <br/> |
|[ReceivedRepresenting](receivedrepresenting.md) <br/> |Principal  <br/> |
   
Wenn ein thirdparty in einem Stellvertretungs-Zugriffs Szenario eine Besprechungsanfrage an einen Prinzipal sendet, der über eine Stellvertretung verfügt, wird der Stellvertretung eine neue Besprechungsanfrage angezeigt. Diese Elemente ermöglichen Delegaten, zwischen Nachrichten zu unterscheiden, die direkt an Sie gesendet werden, und Nachrichten, die aufgrund einer Weiterleitungsregel für Delegaten an Sie gesendet werden.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

