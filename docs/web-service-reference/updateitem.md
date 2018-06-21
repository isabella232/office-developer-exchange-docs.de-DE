---
title: UpdateItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateItem
api_type:
- schema
ms.assetid: 34643d58-2743-45b0-a08d-bff6dc1da61d
description: Das UpdateItem-Element definiert eine Anforderung zum Aktualisieren eines Elements in einem Postfach.
ms.openlocfilehash: 7b9b5f1dcffb95eb127572cb91f92d961c05a77e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/21/2018
ms.locfileid: "19839381"
---
# <a name="updateitem"></a>UpdateItem

Das **UpdateItem** -Element definiert eine Anforderung zum Aktualisieren eines Elements in einem Postfach. 
  
```XML
<UpdateItem ConflictResolution="" MessageDisposition="" SendMeetingInvitationsOrCancellations="" SuppressReadReceipts="">
   <SavedItemFolderId/>
   <ItemChanges/>
</UpdateItem>
```

 **UpdateItemType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**ConflictResolution** <br/> |Identifiziert den Typ des Konfliktbehebung während einer Aktualisierung versuchen. Der Standardwert ist auflösen.  <br/> |
|**"MessageDisposition"** <br/> |Beschreibt, wie das Element nach der Aktualisierung behandelt werden sollen. Das Attribut **"MessageDisposition"** ist für Nachrichtenelemente, einschließlich der Besprechungsnachrichten wie Besprechungsabsagen, Besprechungsanfragen und Antworten auf Besprechungsanfragen erforderlich.  <br/> |
|**"SendMeetingInvitationsOrCancellations"** <br/> |Beschreibt, wie Besprechung aktualisiert übermittelt werden, nachdem ein Kalenderelement aktualisiert wurde. Dieses Attribut ist für Kalenderelemente und Kalendertermine Element erforderlich.  <br/> |
|**SuppressReadReceipts** <br/> |Gibt an, ob lesebestätigungen für das aktualisierte Element unterdrückt werden soll. Der Textwert **true** gibt an, dass das Read, Empfangsbestätigungen unterdrückt werden soll. Der Wert **false** gibt an, dass die lesebestätigungen an den Absender gesendet werden. Dieses Attribut ist optional.  <br/> Dieses Attribut wurde in Exchange Server 2013 SP1 eingeführt.  <br/> |
   
#### <a name="conflictresolution-attribute"></a>ConflictResolution-Attribut

|**Wert**|**Beschreibung**|
|:-----|:-----|
|NeverOverwrite  <br/> |Wenn ein Konflikt vorliegt, die Aktualisierung fehl und ein Fehler zurückgegeben.  <br/> |
|Auflösen  <br/> |Der Aktualisierungsvorgang aufgelöst wird automatisch ein Konflikt.  <br/> |
|AlwaysOverwrite  <br/> |Wenn ein Konflikt vorliegt, wird der Aktualisierungsvorgang Informationen überschrieben.  <br/> |
   
#### <a name="messagedisposition-attribute"></a>Attribut "MessageDisposition"

|**Wert**|**Beschreibung**|
|:-----|:-----|
|SaveOnly  <br/> |Das Element wird aktualisiert und wieder in seinem aktuellen Ordner gespeichert.  <br/> |
|SendOnly  <br/> |Das Element wird aktualisiert und gesendet, aber keine Kopie gespeichert wird.  <br/> |
|SendAndSaveCopy  <br/> |Das Element wird aktualisiert, und eine Kopie im durch das Element [des SavedItemFolderId](saveditemfolderid.md) identifizierten Ordner gespeichert ist.  <br/> |
   
#### <a name="sendmeetinginvitationsorcancellations-attribute"></a>Attribut "SendMeetingInvitationsOrCancellations"

|**Wert**|**Beschreibung**|
|:-----|:-----|
|SendToNone  <br/> |Das Kalenderelement wurde aktualisiert, jedoch Updates werden nicht an die Teilnehmer gesendet.  <br/> |
|SendOnlyToAll  <br/> |Das Kalenderelement wird aktualisiert und die Besprechungsanfrage wird an alle Teilnehmer gesendet, aber nicht im Ordner "Gesendete Elemente" gespeichert.  <br/> |
|SendOnlyToChanged  <br/> |Das Kalenderelement wird aktualisiert, und die besprechungsaktualisierung wird nur für Teilnehmer, die von der Änderung in der Besprechung betroffen sind gesendet.  <br/> |
|SendToAllAndSaveCopy  <br/> |Das Kalenderelement wird aktualisiert, die besprechungsaktualisierung wird an alle Teilnehmer gesendet und eine Kopie im Ordner "Gesendete Elemente" gespeichert ist.  <br/> |
|SendToChangedAndSaveCopy  <br/> |Das Kalenderelement wird aktualisiert, die besprechungsaktualisierung wird an alle Teilnehmer, die von der Änderung in der Besprechung betroffen sind gesendet, und eine Kopie im Ordner "Gesendete Elemente" gespeichert ist.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Des SavedItemFolderId](saveditemfolderid.md) <br/> |Identifiziert den Zielordner für Vorgänge, die zu aktualisieren, senden und Elemente im Exchange-Speicher zu erstellen.  <br/> |
|[ItemChanges](itemchanges.md) <br/> |Enthält ein Array von [ItemChange](itemchange.md) -Elementen, die Elemente und die Updates auf Elemente anwenden zu identifizieren.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[UpdateItem Operation](updateitem-operation.md)

