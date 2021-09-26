---
title: UpdateItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- UpdateItem
api_type:
- schema
ms.assetid: 34643d58-2743-45b0-a08d-bff6dc1da61d
description: Das UpdateItem-Element definiert eine Anforderung zum Aktualisieren eines Elements in einem Postfach.
ms.openlocfilehash: 544ccfb8c42b2a4d4f69ae04d383233203c235b8
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59542789"
---
# <a name="updateitem"></a>UpdateItem

Das **UpdateItem-Element** definiert eine Anforderung zum Aktualisieren eines Elements in einem Postfach. 
  
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
|**ConflictResolution** <br/> |Gibt den Typ der Konfliktlösung an, die während einer Aktualisierung versucht werden soll. Der Standardwert ist AutoResolve.  <br/> |
|**MessageDisposition** <br/> |Beschreibt, wie das Element nach der Aktualisierung behandelt wird. Das **MessageDisposition-Attribut** ist für Nachrichtenelemente erforderlich, einschließlich Besprechungsnachrichten wie Besprechungsabsagen, Besprechungsanfragen und Besprechungsantworten.  <br/> |
|**SendMeetingInvitationsOrCancellations** <br/> |Beschreibt, wie Besprechungsupdates nach der Aktualisierung eines Kalenderelements kommuniziert werden. Dieses Attribut ist für Kalenderelemente und Kalenderelementvorkommen erforderlich.  <br/> |
|**SuppressReadReceipts** <br/> |Gibt an, ob Lesebestätigungen für das aktualisierte Element unterdrückt werden sollen. Der Textwert **"true"** gibt an, dass Lesebestätigungen unterdrückt werden sollen. Der Wert **"false"** gibt an, dass die Lesebestätigungen an den Absender gesendet werden. Dieses Attribut ist optional.  <br/> Dieses Attribut wurde in Exchange Server 2013 SP1 eingeführt.  <br/> |
   
#### <a name="conflictresolution-attribute"></a>ConflictResolution-Attribut

|**Wert**|**Beschreibung**|
|:-----|:-----|
|NeverOverwrite  <br/> |Wenn ein Konflikt vorliegt, schlägt der Aktualisierungsvorgang fehl, und es wird ein Fehler zurückgegeben.  <br/> |
|AutoResolve  <br/> |Der Aktualisierungsvorgang löst alle Konflikte automatisch aus.  <br/> |
|AlwaysOverwrite  <br/> |Wenn ein Konflikt vorliegt, überschreibt der Aktualisierungsvorgang Informationen.  <br/> |
   
#### <a name="messagedisposition-attribute"></a>MessageDisposition-Attribut

|**Wert**|**Beschreibung**|
|:-----|:-----|
|SaveOnly  <br/> |Das Element wird aktualisiert und wieder in seinem aktuellen Ordner gespeichert.  <br/> |
|SendOnly  <br/> |Das Element wird aktualisiert und gesendet, aber es wird keine Kopie gespeichert.  <br/> |
|SendAndSaveCopy  <br/> |Das Element wird aktualisiert, und eine Kopie wird in dem Ordner gespeichert, der vom [SavedItemFolderId-Element](saveditemfolderid.md) identifiziert wird.  <br/> |
   
#### <a name="sendmeetinginvitationsorcancellations-attribute"></a>SendMeetingInvitationsOrCancellations-Attribut

|**Wert**|**Beschreibung**|
|:-----|:-----|
|SendToNone  <br/> |Das Kalenderelement wird aktualisiert, updates werden jedoch nicht an die Teilnehmer gesendet.  <br/> |
|SendOnlyToAll  <br/> |Das Kalenderelement wird aktualisiert, und die Besprechungsaktualisierung wird an alle Teilnehmer gesendet, aber nicht im Ordner "Gesendete Elemente" gespeichert.  <br/> |
|SendOnlyToChanged  <br/> |Das Kalenderelement wird aktualisiert, und die Besprechungsaktualisierung wird nur an Teilnehmer gesendet, die von der Änderung in der Besprechung betroffen sind.  <br/> |
|SendToAllAndSaveCopy  <br/> |Das Kalenderelement wird aktualisiert, die Besprechungsaktualisierung wird an alle Teilnehmer gesendet, und eine Kopie wird im Ordner "Gesendete Elemente" gespeichert.  <br/> |
|SendToChangedAndSaveCopy  <br/> |Das Kalenderelement wird aktualisiert, die Besprechungsaktualisierung wird an alle Teilnehmer gesendet, die von der Änderung in der Besprechung betroffen sind, und eine Kopie wird im Ordner "Gesendete Elemente" gespeichert.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[SavedItemFolderId](saveditemfolderid.md) <br/> |Identifiziert den Zielordner für Vorgänge, die Elemente im Exchange Speicher aktualisieren, senden und erstellen.  <br/> |
|[ItemChanges](itemchanges.md) <br/> |Enthält ein Array von [ItemChange-Elementen,](itemchange.md) die Elemente und die Aktualisierungen identifizieren, die auf die Elemente angewendet werden sollen.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
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



[UpdateItem-Vorgang](updateitem-operation.md)

