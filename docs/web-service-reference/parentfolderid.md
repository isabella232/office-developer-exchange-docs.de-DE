---
title: ParentFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ParentFolderId
api_type:
- schema
ms.assetid: 258f4b1f-367e-4c7d-9c29-eb775a2398c7
description: Das ParentFolderId-Element stellt den Bezeichner des übergeordneten Ordners, der das Element oder Ordner enthält.
ms.openlocfilehash: 3f60e8adb62fbf464a58af4169fbcd83910877cc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830687"
---
# <a name="parentfolderid"></a>ParentFolderId

Das **ParentFolderId** -Element stellt den Bezeichner des übergeordneten Ordners, der das Element oder Ordner enthält. 
  
```XML
<ParentFolderId Id="" ChangeKey=""/>
```

**FolderIdType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**Id** <br/> |Enthält eine Zeichenfolge, die einen Ordner im Exchange-Speicher identifiziert. Dieses Attribut ist erforderlich.  <br/> |
|**ChangeKey** <br/> |Enthält eine Zeichenfolge, die eine Version eines Ordners identifiziert, die von dem **Id** -Attribut angegeben ist. Dieses Attribut ist optional. Verwenden Sie dieses Attribut, um sicherzustellen, dass die richtige Version eines Ordners verwendet wird.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[CalendarFolder](calendarfolder.md) <br/> |Stellt einen Kalenderordner in einem Postfach an.  <br/> |
|[CalendarItem](calendaritem.md) <br/> |Stellt ein Kalenderelement in einem Postfach an.  <br/> |
|[Contact](contact.md) <br/> |Stellt ein Kontaktelement in einem Postfach an.  <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |Stellt einen Kontakteordner in einem Postfach an.  <br/> |
|[CopiedEvent](copiedevent.md) <br/> |Stellt ein Ereignis in der eines Elements oder Ordners kopiert wird.  <br/> |
|[CreatedEvent](createdevent.md) <br/> |Stellt ein Ereignis in der eines Elements oder Ordners erstellt wird.  <br/> |
|[DeletedEvent](deletedevent.md) <br/> |Stellt ein Ereignis in der eines Elements oder Ordners gelöscht wird.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Stellt eine private Verteilerliste in einem Postfach an.  <br/> |
|[Folder](folder.md) <br/> |Stellt einen Ordner in einem Postfach an.  <br/> |
|[Element](item.md) <br/> |Stellt ein generisches Exchange-Element.  <br/> |
|[Item (UploadItemType)](item-uploaditemtype.md) <br/> |Stellt ein einzelnes Element in einem Postfach hochladen.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Stellt einen Besprechungsabsage in einem Postfach an.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Stellt eine Besprechungsnachricht in einem Postfach an.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Stellt eine Besprechungsanfrage in einem Postfach an.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Stellt eine Antwort auf Besprechungsanfrage in einem Postfach an.  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |Stellt eine e-Mail-Nachricht in einem Postfach an.  <br/> |
|[ModifiedEvent](modifiedevent.md) <br/> |Stellt ein Ereignis in der eines Elements oder Ordners geändert wird.  <br/> |
|[MovedEvent](movedevent.md) <br/> |Stellt ein Ereignis in der eines Elements oder Ordners von einem übergeordneten Ordner in einer anderen übergeordneten Ordner verschoben wird.  <br/> |
|[NewMailEvent](newmailevent.md) <br/> |Stellt ein Ereignis, das durch eine neue e-Mail-Element in einem Postfach ausgelöst wird.  <br/> |
|[AcceptItem](acceptitem.md) <br/> |Stellt eine Accept-Antwort auf eine Besprechungsanfrage.  <br/> |
|[TentativelyAcceptItem](tentativelyacceptitem.md) <br/> |Stellt eine mit Vorbehalt Antworten auf eine Besprechungsanfrage.  <br/> |
|[DeclineItem](declineitem.md) <br/> |Stellt eine ablehnen Antwort auf eine Besprechungsanfrage.  <br/> |
|[RemoveItem](removeitem.md) <br/> |Entfernt ein Element aus dem Exchange-Informationsspeicher.  <br/> |
|[Aufgabe](task.md) <br/> |Stellt ein Aufgabenelement in einem Postfach an.  <br/> |
|[ReplyToItem](replytoitem.md) <br/> |Enthält eine Antwort an den Ersteller eines Elements in der Exchange-Speicher.  <br/> |
|[ReplyAllToItem](replyalltoitem.md) <br/> |Enthält eine Antwort an alle identifizierten Empfänger eines Elements in der Exchange-Speicher.  <br/> |
|[ForwardItem](forwarditem.md) <br/> |Enthält ein Exchange-Speicher-Element an Empfänger weitergeleitet.  <br/> |
|[CancelCalendarItem](cancelcalendaritem.md) <br/> |Stellt das Antwortobjekt, das Sie eine Besprechung absagen verwendet wird.  <br/> |
|[TasksFolder](tasksfolder.md) <br/> |Stellt einen Ordner in einem Postfach an.  <br/> |
|["SearchFolder"](searchfolder.md) <br/> |Stellt einen Suchordner in einem Postfach an.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

