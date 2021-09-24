---
title: Items (NonEmptyArrayOfAllItemsType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Items
api_type:
- schema
ms.assetid: d61ef1cc-ddfc-480a-9625-7b436cb33ae0
description: Das Items-Element enthält eine Gruppe von Elementen, die erstellt werden sollen.
ms.openlocfilehash: a511fa9e81cdfb4d5c84705edb0d37f75eb76049
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59524994"
---
# <a name="items-nonemptyarrayofallitemstype"></a>Items (NonEmptyArrayOfAllItemsType)

Das **Items-Element** enthält eine Gruppe von Elementen, die erstellt werden sollen. 
  
```XML
<Items>
   <Item/>
   <Message/>
   <CalendarItem/>
   <Contact/>
   <DistributionList/>
   <MeetingMessage/>
   <MeetingRequest/>
   <MeetingResponse/>
   <MeetingCancellation/>
   <Task/>
   <ReplyToItem/>
   <ForwardItem/>
   <ReplyAllToItem/>
   <AcceptItem/>
   <TentativelyAcceptItem/>
   <DeclineItem/>
   <CancelCalendarItem/>
   <RemoveItem/>
   <PostReplyItem/>
   <SuppressReadReceipt/>
   <AcceptSharingInvitation/>
</Items>
```

 **NonEmptyArrayOfAllItemsType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Element](item.md) <br/> |Stellt ein Element im Exchange-Informationsspeicher dar.  <br/> |
|[Meldung](message-ex15websvcsotherref.md) <br/> |Stellt eine Exchange E-Mail-Nachricht dar.  <br/> |
|[CalendarItem](calendaritem.md) <br/> |Stellt ein Element im Exchange-Kalender dar.  <br/> |
|[Kontaktperson](contact.md) <br/> |Stellt ein Exchange-Kontaktelement dar.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Stellt eine Verteilerliste dar.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Stellt eine Besprechungsnachricht im Exchange Store dar.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Stellt eine Besprechungsantwort im Exchange-Informationsspeicher dar.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Stellt eine Besprechungsabsage im Exchange-Informationsspeicher dar.  <br/> |
|[Aufgabe](task.md) <br/> |Stellt eine Aufgabe im Exchange-Informationsspeicher dar.  <br/> |
|[ReplyToItem](replytoitem.md) <br/> |Enthält eine Antwort an den Absender eines Elements im Exchange Speicher.  <br/> |
|[ForwardItem](forwarditem.md) <br/> |Enthält ein Exchange-Speicher-Element an Empfänger weitergeleitet.  <br/> |
|[ReplyAllToItem](replyalltoitem.md) <br/> |Enthält eine Antwort an den Absender und alle identifizierten Empfänger eines Elements im Exchange Speicher.  <br/> |
|[AcceptItem](acceptitem.md) <br/> |Stellt eine Accept-Antwort auf eine Besprechungsanfrage.  <br/> |
|[TentativelyAcceptItem](tentativelyacceptitem.md) <br/> |Stellt eine mit Vorbehalt Antworten auf eine Besprechungsanfrage.  <br/> |
|[DeclineItem](declineitem.md) <br/> |Stellt eine ablehnen Antwort auf eine Besprechungsanfrage.  <br/> |
|[CancelCalendarItem](cancelcalendaritem.md) <br/> |Stellt das Antwortobjekt, das Sie eine Besprechung absagen verwendet wird.  <br/> |
|[RemoveItem](removeitem.md) <br/> |Stellt ein Antwortobjekt dar, das verwendet wird, um ein Besprechungselement zu entfernen, wenn eine MeetingCancellation-Nachricht empfangen wird.  <br/> |
|[PostReplyItem](postreplyitem.md) <br/> |Enthält eine Antwort auf ein Beitragselement.  <br/> |
|[SuppressReadReceipt](suppressreadreceipt.md) <br/> |Wird verwendet, um Lesebestätigungen zu unterdrücken.  <br/> |
|[AcceptSharingInvitation](acceptsharinginvitation.md) <br/> |Wird verwendet, um eine Einladung zu akzeptieren, die den Zugriff auf den Kalender oder die Kontaktdaten eines anderen Benutzers ermöglicht.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[CreateItem](createitem.md) <br/> |Definiert die Anforderung zum Erstellen eines Elements im Exchange Speicher.  <br/> Es folgt der XPath-Ausdruck für dieses Element:  `/CreateItem` <br/> |
|[ConversationNode](conversationnode.md) <br/> |Identifiziert einen einzelnen Knoten in einer Unterhaltung.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[CreateFolder-Vorgang](createfolder-operation.md)
  
[CreateItem-Vorgang](createitem-operation.md)


[Erstellen von Ordnern (Exchange Webdienste)](https://msdn.microsoft.com/library/3b15b0ec-8691-45ed-9a24-a91ff732d6cf%28Office.15%29.aspx)

