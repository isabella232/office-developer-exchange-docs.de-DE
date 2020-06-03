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
ms.openlocfilehash: 43821db58457ffce22be918a7ba6427f57230010
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466570"
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
|**ConflictResolution** <br/> |Gibt den Typ der Konfliktlösung an, die während einer Aktualisierung versucht werden soll. Der Standardwert ist autoresolve.  <br/> |
|**MessageDisposition** <br/> |Beschreibt, wie das Element nach seiner Aktualisierung behandelt wird. Das **MessageDisposition** -Attribut ist für Nachrichtenelemente erforderlich, einschließlich Besprechungsnachrichten wie Besprechungsabsagen, Besprechungsanfragen und Besprechungsantworten.  <br/> |
|**SendMeetingInvitationsOrCancellations** <br/> |Beschreibt, wie Besprechungsaktualisierungen mitgeteilt werden, nachdem ein Kalenderelement aktualisiert wurde. Dieses Attribut ist für Kalenderelemente und Kalenderelement vorkommen erforderlich.  <br/> |
|**SuppressReadReceipts** <br/> |Gibt an, ob Lesebestätigungen für das aktualisierte Element unterdrückt werden sollen. Der Textwert **true** gibt an, dass Lesebestätigungen unterdrückt werden sollen. Der Wert **false** gibt an, dass die Lesebestätigungen an den Absender gesendet werden. Dieses Attribut ist optional.  <br/> Dieses Attribut wurde in Exchange Server 2013 SP1 eingeführt.  <br/> |
   
#### <a name="conflictresolution-attribute"></a>ConflictResolution-Attribut

|**Wert**|**Beschreibung**|
|:-----|:-----|
|NeverOverwrite  <br/> |Wenn ein Konflikt vorliegt, schlägt der Aktualisierungsvorgang fehl, und es wird ein Fehler zurückgegeben.  <br/> |
|Alle automatisch auflösen  <br/> |Der Aktualisierungsvorgang löst alle Konflikte automatisch auf.  <br/> |
|AlwaysOverwrite  <br/> |Wenn ein Konflikt vorliegt, werden Informationen vom Aktualisierungsvorgang überschrieben.  <br/> |
   
#### <a name="messagedisposition-attribute"></a>MessageDisposition-Attribut

|**Wert**|**Beschreibung**|
|:-----|:-----|
|SaveOnly  <br/> |Das Element wird aktualisiert und in seinem aktuellen Ordner zurückgespeichert.  <br/> |
|SendOnly  <br/> |Das Element wird aktualisiert und gesendet, aber es wird keine Kopie gespeichert.  <br/> |
|SendAndSaveCopy  <br/> |Das Element wird aktualisiert, und eine Kopie wird in dem durch das [SavedItemFolderId](saveditemfolderid.md) -Element identifizierten Ordner gespeichert.  <br/> |
   
#### <a name="sendmeetinginvitationsorcancellations-attribute"></a>SendMeetingInvitationsOrCancellations-Attribut

|**Wert**|**Beschreibung**|
|:-----|:-----|
|SendToNone  <br/> |Das Kalenderelement wird aktualisiert, aber Updates werden nicht an die Teilnehmer gesendet.  <br/> |
|SendOnlyToAll  <br/> |Das Kalenderelement wird aktualisiert, und das Besprechungs Update wird an alle Teilnehmer gesendet, aber nicht im Ordner "Gesendete Elemente" gespeichert.  <br/> |
|SendOnlyToChanged  <br/> |Das Kalenderelement wird aktualisiert, und das Besprechungs Update wird nur an Teilnehmer gesendet, die von der Änderung in der Besprechung betroffen sind.  <br/> |
|SendToAllAndSaveCopy  <br/> |Das Kalenderelement wird aktualisiert, das Besprechungs Update wird an alle Teilnehmer gesendet, und eine Kopie wird im Ordner "Gesendete Elemente" gespeichert.  <br/> |
|SendToChangedAndSaveCopy  <br/> |Das Kalenderelement wird aktualisiert, das Besprechungs Update wird an alle Teilnehmer gesendet, die von der Änderung in der Besprechung betroffen sind, und eine Kopie wird im Ordner "Gesendete Elemente" gespeichert.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[SavedItemFolderId](saveditemfolderid.md) <br/> |Identifiziert den Zielordner für Vorgänge, die Elemente im Exchange-Informationsspeicher aktualisieren, senden und erstellen.  <br/> |
|[ItemChanges](itemchanges.md) <br/> |Enthält ein Array von [ItemChange](itemchange.md) -Elementen, mit denen Elemente identifiziert werden, und die Updates, die auf die Elemente angewendet werden sollen.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[UpdateItem-Vorgang](updateitem-operation.md)

