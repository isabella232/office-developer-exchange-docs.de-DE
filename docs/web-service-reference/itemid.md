---
title: ItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
api_name:
- ItemId
api_type:
- schema
ms.assetid: 3350b597-57a0-4961-8f44-8624946719b4
description: Das Itemid-Element enthält den eindeutigen Bezeichner und den Änderungsschlüssel eines Elements in der Exchange-Informationsspeicher.
localization_priority: Priority
ms.openlocfilehash: d5931702225c6864b1ca60a6f0753b65f65aca30
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44441562"
---
# <a name="itemid"></a>ItemId

Das **ItemID** -Element enthält den eindeutigen Bezeichner und den Änderungsschlüssel eines Elements in der Exchange-Informationsspeicher. 
  
```XML
<ItemId Id="" ChangeKey="" />
```

 **Itemidtype**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**Id** <br/> |Identifiziert ein bestimmtes Element in der Exchange-Informationsspeicher. Bei der **ID** wird die Groß-/Kleinschreibung beachtet; Daher muss bei Vergleichen zwischen **IDs** die Groß-/Kleinschreibung beachtet oder binär sein.  <br/> |
|**ChangeKey** <br/> | Gibt eine bestimmte Version eines Elements an. <br/><br/>Für die folgenden Szenarien ist ein **ChangeKey** erforderlich: <br/> <br/>-Das [UpdateItem](updateitem.md) -Element erfordert ein **ChangeKey** , wenn das **ConflictResolution** -Attribut auf autoresolve festgelegt ist. Autoresolve ist ein Standardwert. Wenn das **ChangeKey** -Attribut nicht enthalten ist, gibt die Antwort einen [Response Code](responsecode.md) -Wert zurück, der **ErrorChangeKeyRequired**entspricht.  <br/><br/>-Das [SendItem](senditem.md) -Element erfordert ein **ChangeKey** , um zu testen, ob der versuchte Vorgang auf die neueste Version eines Elements angewendet wird. Wenn das **ChangeKey** -Attribut nicht in der **ItemID** -Eigenschaft enthalten ist oder wenn das **ChangeKey** -Objekt leer ist, gibt die Antwort einen [Response Code](responsecode.md) -Wert zurück, der **ErrorStaleObject**entspricht.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[CalendarItem](calendaritem.md) <br/> |Stellt ein Element im Exchange-Kalender dar.  <br/> |
|[Kontaktperson](contact.md) <br/> |Stellt ein Exchange-Kontaktelement dar.  <br/> |
|[CopiedEvent](copiedevent.md) <br/> |Stellt ein Ereignis dar, wenn ein Element oder ein Ordner kopiert wird.  <br/> |
|[CreatedEvent](createdevent.md) <br/> |Stellt ein Ereignis dar, wenn ein Element oder ein Ordner erstellt wird.  <br/> |
|[Delete (ItemSync)](delete-itemsync.md) <br/> |Identifiziert ein einzelnes Element, das im lokalen Clientspeicher gelöscht werden soll.  <br/> |
|[DeletedEvent](deletedevent.md) <br/> |Stellt ein Ereignis dar, wenn ein Element oder ein Ordner gelöscht wird.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Stellt eine Verteilerliste dar.  <br/> |
|[ExportItemsResponseMessage](exportitemsresponsemessage.md) <br/> |Enthält den Status und die Ergebnisse einer Anforderung zum Exportieren eines einzelnen Post Fach Elements.  <br/> |
|[FirstOccurrence](firstoccurrence.md) <br/> |Stellt das erste Vorkommen eines wiederkehrenden Kalenderelements dar.  <br/> |
|[GlobalItemIds](globalitemids.md) <br/> |Enthält die Auflistung von Element-IDs für alle Unterhaltungselemente in einem Postfach.  <br/> |
|[Ignore](ignore.md) <br/> |Identifiziert Elemente, die während der Synchronisierung übersprungen werden sollen.  <br/> |
|[Element](item.md) <br/> |Stellt ein generisches Exchange-Element dar.  <br/> |
|[Element (UploadItemType)](item-uploaditemtype.md) <br/> |Stellt ein einzelnes Element dar, das in ein Postfach hochgeladen werden soll.  <br/> |
|[ItemChange](itemchange.md) <br/> |Enthält eine Element-ID und die Updates, die auf das Element angewendet werden sollen.  <br/><br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:  <br/> <br/>  `/UpdateItem/ItemChanges/ItemChange[i]` <br/> |
|[ItemIds](itemids.md) <br/> | Enthält die eindeutigen Identitäten von Elementen, Element Elementen und wiederkehrenden Master Elementen, die zum Löschen, senden, abrufen, verlagern oder Kopieren von Elementen in der Exchange-Informationsspeicher verwendet werden. <br/> <br/>  Folgende XPath-Ausdrücke werden für dieses Element verwendet: <br/> <br/>  `/DeleteItem/ItemIds` <br/>  `/SendItem/ItemIds` <br/>  `/GetItem/ItemIds` <br/>  `/MoveItem/ItemIds` <br/>  `/CopyItem//ItemIds` <br/> |
|[Itemids (NonEmptyArrayOfItemIdsType)](itemids-nonemptyarrayofitemidstype.md) <br/> |Enthält ein Array von Element-IDs, mit denen die Elemente identifiziert werden, die aus einem Postfach exportiert werden sollen.  <br/> |
|[LastOccurrence](lastoccurrence.md) <br/> |Stellt das letzte Vorkommen eines wiederkehrenden Kalenderelements dar.  <br/> |
|[Postfach](mailbox.md) <br/> |Ein e-Mail-aktivierten Active Directory Directory Service-Objekt identifiziert.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Stellt eine Besprechungsabsage im Exchange-Informationsspeicher dar.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Stellt eine Besprechung im Exchange-Informationsspeicher dar.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Stellt eine Besprechungsantwort im Exchange-Informationsspeicher dar.  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |Stellt eine Exchange-E-Mail-Nachricht dar.  <br/> |
|[ModifiedEvent](modifiedevent.md) <br/> |Stellt ein Ereignis dar, das auftritt, wenn ein Element geändert wird.  <br/> |
|[MovedEvent](movedevent.md) <br/> |Stellt ein Ereignis dar, das auftritt, wenn ein Element von einem übergeordneten Ordner in einen anderen übergeordneten Ordner verschoben wird.  <br/> |
|[NewMailEvent](newmailevent.md) <br/> |Stellt ein Ereignis dar, das durch ein neues e-Mail-Element in einem Postfach ausgelöst wird.  <br/> |
|[Vorkommen](occurrence.md) <br/> |Stellt ein einzelnes geändertes Vorkommen eines wiederkehrenden Kalenderelements dar.  <br/> |
|[PlayOnPhone (Exchange Webdienste)](playonphone-exchange-web-services.md) <br/> |Stellt eine Anforderung zum Lesen eines Elements auf einem Telefon dar.  <br/> |
|[RemoveItem](removeitem.md) <br/> |Entfernt ein Element aus dem Exchange-Informationsspeicher.  <br/> |
|[RoomList](roomlist.md) <br/> |Stellt eine e-Mail-Adresse dar, die eine Liste von Besprechungsräumen identifiziert.  <br/> |
|[Aufgabe](task.md) <br/> |Stellt eine Aufgabe im Exchange-Informationsspeicher dar.  <br/> |
|[UploadItemsResponseMessage](uploaditemsresponsemessage.md) <br/> |Enthält den Status und die Ergebnisse einer Anforderung zum Hochladen eines einzelnen Post Fach Elements.  <br/> |
|[UserConfiguration](userconfiguration.md) <br/> |Definiert ein einzelnes Benutzer Konfigurationsobjekt.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [ExportItems-Vorgang](exportitems-operation.md)
- [UploadItems-Vorgang](uploaditems-operation.md) 
- [FindConversation-Vorgang](findconversation-operation.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

