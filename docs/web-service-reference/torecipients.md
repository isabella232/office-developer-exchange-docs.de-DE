---
title: ToRecipients
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ToRecipients
api_type:
- schema
ms.assetid: 72dc3be8-30bb-4ae1-acf4-fb94ff490631
description: Das ToRecipients -Element enthält ein Array von Empfänger eines Elements. Dies sind die primären Empfänger eines Elements.
ms.openlocfilehash: 1e49a3113328b0573124948056f684de72f27b3f
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59527251"
---
# <a name="torecipients"></a>ToRecipients

Das **ToRecipients** -Element enthält ein Array von Empfänger eines Elements. Dies sind die primären Empfänger eines Elements. 
  
```xml
<ToRecipients>
   <Mailbox/>
</ToRecipients>
```

 **ArrayOfRecipientsType**
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
|[RemoveItem](removeitem.md) <br/> |Entfernt ein Element aus dem Exchange-Informationsspeicher.  <br/> |
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
   
## <a name="remarks"></a>HinwBemerkungeneise

Sie können nicht **ToRecipients** mithilfe einer Anforderung FindItem abrufen. Verwenden Sie eine Anforderung GetItem, um die **ToRecipients** abzurufen.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

