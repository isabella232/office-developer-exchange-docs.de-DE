---
title: ItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ItemId
api_type:
- schema
ms.assetid: 3350b597-57a0-4961-8f44-8624946719b4
description: Das ItemId-Element enthält den eindeutigen Schlüssel-ID und Ändern eines Elements in der Exchange-Speicher.
ms.openlocfilehash: 9c5d71a23e1e4b77d2a50016aa4d765d872d04cc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830157"
---
# <a name="itemid"></a>ItemId

Das **ItemId** -Element enthält den eindeutigen Schlüssel-ID und Ändern eines Elements in der Exchange-Speicher. 
  
```XML
<ItemId Id="" ChangeKey="" />
```

 **ItemIdType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**Id** <br/> |Gibt ein bestimmtes Element in der Exchange-Speicher. **ID** ist die Groß-/Kleinschreibung beachtet. aus diesem Grund muss Vergleiche zwischen **Ids** Groß-und Kleinschreibung berücksichtigt oder binary.  <br/> |
|**ChangeKey** <br/> | Identifiziert eine bestimmte Version eines Elements an. <br/><br/>Eine **ChangeKey** ist erforderlich für die folgenden Szenarien: <br/> <br/>-Das [UpdateItem](updateitem.md) -Element muss ein **ChangeKey** , wenn das Attribut **ConflictResolution** auf auflösen festgelegt ist. Auflösen ist ein Standardwert. Wenn das Attribut **ChangeKey** nicht angegeben ist, gibt die Antwort einen [ResponseCode](responsecode.md) Wert **ErrorChangeKeyRequired**gleich zurück.  <br/><br/>-Das Element [den SendItem](senditem.md) erfordert eine **ChangeKey** zu prüfen, ob der Vorgang die neueste Version eines Elements bestimmt ist. Wenn das Attribut **ChangeKey** nicht in die **ItemId** enthalten ist oder die **ChangeKey** leer ist, wird die Antwort [ResponseCode](responsecode.md) Wert gleich **ErrorStaleObject**zurück.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[CalendarItem](calendaritem.md) <br/> |Stellt ein Element im Exchange-Kalender dar.  <br/> |
|[Kontaktperson](contact.md) <br/> |Stellt ein Exchange-Kontaktelement dar.  <br/> |
|[CopiedEvent](copiedevent.md) <br/> |Stellt ein Ereignis, wenn eines Elements oder Ordners kopiert wird.  <br/> |
|[CreatedEvent](createdevent.md) <br/> |Stellt ein Ereignis, wenn eines Elements oder Ordners erstellt wird.  <br/> |
|[Löschen (ItemSync)](delete-itemsync.md) <br/> |Gibt ein einzelnes Element in der lokalen Client-Speicher zu löschen.  <br/> |
|[DeletedEvent](deletedevent.md) <br/> |Stellt ein Ereignis beim Löschen eines Elements oder Ordners an.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Stellt eine Verteilerliste dar.  <br/> |
|[ExportItemsResponseMessage](exportitemsresponsemessage.md) <br/> |Enthält den Status und die Ergebnisse einer Anforderung für ein einzelnes Postfach-Element zu exportieren.  <br/> |
|[FirstOccurrence](firstoccurrence.md) <br/> |Stellt das erste Vorkommen eines sich wiederholenden Kalenderelements an.  <br/> |
|[GlobalItemIds](globalitemids.md) <br/> |Enthält die Auflistung der Element-IDs für alle Unterhaltungselemente in einem Postfach an.  <br/> |
|[Ignorieren](ignore.md) <br/> |Identifiziert Elemente, während der Synchronisierung zu überspringen.  <br/> |
|[Element](item.md) <br/> |Stellt ein generisches Exchange-Element.  <br/> |
|[Item (UploadItemType)](item-uploaditemtype.md) <br/> |Stellt ein einzelnes Element in einem Postfach hochladen.  <br/> |
|[ItemChange](itemchange.md) <br/> |Enthält eine Element-ID und die Updates auf das Element anwenden.  <br/><br/> Es folgt der XPath-Ausdruck, der dieses Element: <br/> <br/>  `/UpdateItem/ItemChanges/ItemChange[i]` <br/> |
|[Artikelnummern ein.](itemids.md) <br/> | Enthält die eindeutigen Identitäten der Elemente, Vorkommen Elemente und master Terminserien verwendet, um zu löschen, senden, abrufen, verschieben oder Kopieren von Elementen in der Exchange-Speicher. <br/> <br/>  Folgende XPath-Ausdrücke werden für dieses Element verwendet: <br/> <br/>  `/DeleteItem/ItemIds` <br/>  `/SendItem/ItemIds` <br/>  `/GetItem/ItemIds` <br/>  `/MoveItem/ItemIds` <br/>  `/CopyItem//ItemIds` <br/> |
|[Artikelnummern ein (NonEmptyArrayOfItemIdsType).](itemids-nonemptyarrayofitemidstype.md) <br/> |Enthält ein Array der Element-IDs, die die Elemente aus einem Postfach exportieren zu identifizieren.  <br/> |
|[LastOccurrence](lastoccurrence.md) <br/> |Stellt das letzte Vorkommen eines sich wiederholenden Kalenderelements an.  <br/> |
|[Postfach](mailbox.md) <br/> |Ein e-Mail-aktivierten Active Directory Directory Service-Objekt identifiziert.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Stellt eine Besprechungsabsage im Exchange-Informationsspeicher dar.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Stellt eine Besprechung im Exchange-Informationsspeicher dar.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Stellt eine Besprechungsantwort im Exchange-Informationsspeicher dar.  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |Stellt eine Exchange-E-Mail-Nachricht dar.  <br/> |
|[ModifiedEvent](modifiedevent.md) <br/> |Stellt ein Ereignis, das auftritt, wenn ein Element geändert wird.  <br/> |
|[MovedEvent](movedevent.md) <br/> |Stellt ein Ereignis, das auftritt, wenn ein Element aus einem übergeordneten Ordner in einen anderen übergeordneten Ordner verschoben wird.  <br/> |
|[NewMailEvent](newmailevent.md) <br/> |Stellt ein Ereignis, das durch eine neue e-Mail-Element in einem Postfach ausgelöst wird.  <br/> |
|[Vorkommen](occurrence.md) <br/> |Stellt ein einzelnes geändertes Vorkommen des ein wiederkehrendes Kalenderelement.  <br/> |
|[PlayOnPhone (Exchange Web Services)](playonphone-exchange-web-services.md) <br/> |Stellt eine Anforderung an ein Element an einem Telefon gelesen.  <br/> |
|[RemoveItem](removeitem.md) <br/> |Entfernt ein Element aus dem Exchange-Informationsspeicher.  <br/> |
|[RoomList](roomlist.md) <br/> |Stellt eine e-Mail-Adresse, die eine Liste von Besprechungsräumen identifiziert.  <br/> |
|[Aufgabe](task.md) <br/> |Stellt eine Aufgabe im Exchange-Informationsspeicher dar.  <br/> |
|[UploadItemsResponseMessage](uploaditemsresponsemessage.md) <br/> |Enthält den Status und die Ergebnisse einer Anforderung für ein einzelnes Postfach Element hochladen.  <br/> |
|[UserConfiguration](userconfiguration.md) <br/> |Definiert einen einzelnen Benutzer-Konfigurationsobjekt.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [ExportItems-Vorgang](exportitems-operation.md)
- [UploadItems-Vorgang](uploaditems-operation.md) 
- [FindConversation Operation](findconversation-operation.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

