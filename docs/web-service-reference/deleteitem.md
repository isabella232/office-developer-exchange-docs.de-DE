---
title: DeleteItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteItem
api_type:
- schema
ms.assetid: 055cdee8-3c7d-47db-9f27-740f4a674729
description: Das DeleteItem-Element definiert eine Anforderung zum Löschen eines Elements aus einem Postfach im Exchange-Informationsspeicher.
ms.openlocfilehash: ed13ee32b487f49740aed80e8705257d3e2e6938
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529203"
---
# <a name="deleteitem"></a>DeleteItem

Das **DeleteItem** -Element definiert eine Anforderung zum Löschen eines Elements aus einem Postfach im Exchange-Informationsspeicher. 
  
```XML
<DeleteItem DeleteType="" SendMeetingCancellations="" AffectedTaskOccurrences="" SuppressReadReceipts="">
   <ItemIds/>
</DeleteItem>
```

 **DeleteItemType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**Deletetypeharddelete** <br/> |Beschreibt, wie ein Element gelöscht wird. Dieses Attribut ist erforderlich.  <br/> |
|**SendMeetingCancellations** <br/> |Beschreibt, ob ein Löschen eines Kalenderelements an die Teilnehmer kommuniziert wird. Dieses Attribut ist erforderlich, wenn Kalenderelemente gelöscht werden. Dieses Attribut ist optional, wenn nicht Kalenderelemente gelöscht werden.  <br/> |
|**AffectedTaskOccurrences** <br/> |Beschreibt, ob eine Aufgabeninstanz oder ein Aufgaben Master durch einen [DeleteItem-Vorgang](deleteitem-operation.md)gelöscht wird. Dieses Attribut ist erforderlich, wenn Aufgaben gelöscht werden. Dieses Attribut ist optional, wenn nicht Aufgabenelemente gelöscht werden.  <br/> |
|**SuppressReadReceipts** <br/> |Gibt an, ob Lesebestätigungen für das gelöschte Element unterdrückt werden. Der Textwert **true**, gibt an, dass die Lesebestätigungen unterdrückt werden. Der Wert **false** gibt an, dass die Lesebestätigungen an den Absender gesendet werden. Dieses Attribut ist optional.  <br/> |
   
#### <a name="deletetype-attribute"></a>DeleteType-Attribut

|**Wert**|**Beschreibung**|
|:-----|:-----|
|HardDelete  <br/> |Ein Element wird dauerhaft aus dem Speicher entfernt.  <br/> |
|SoftDelete  <br/> |Ein Element wird in den Papierkorb verschoben, wenn der Papierkorb aktiviert ist.  <br/> |
|MoveToDeletedItems  <br/> |Ein Element wird in den Ordner "Gelöschte Elemente" verschoben.  <br/> |
   
#### <a name="sendmeetingcancellations-attribute"></a>SendMeetingCancellations-Attribut

|**Wert**|**Beschreibung**|
|:-----|:-----|
|SendToNone  <br/> |Ein Kalenderelement wird gelöscht, ohne eine Abbruch Nachricht zu senden.  <br/> |
|SendOnlyToAll  <br/> |Ein Kalenderelement wird gelöscht, und eine Abbruchmeldung wird an alle Teilnehmer gesendet.  <br/> |
|SendToAllAndSaveCopy  <br/> |Ein Kalenderelement wird gelöscht, und eine Abbruchmeldung wird an alle Teilnehmer gesendet. Eine Kopie der Abbruch Nachricht wird im Ordner "Gesendete Elemente" gespeichert.  <br/> |
   
#### <a name="affectedtaskoccurrences-attribute"></a>AffectedTaskOccurrences-Attribut

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Allvorkommen  <br/> |Eine Delete Item-Anforderung löscht den hauptvorgang und somit alle wiederkehrenden Vorgänge, die dem hauptvorgang zugeordnet sind.  <br/> |
|SpecifiedOccurrenceOnly  <br/> |Eine Delete Item-Anforderung löscht nur bestimmte Vorkommen eines Vorgangs.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ItemIds](itemids.md) <br/> |Enthält ein Array von Elementen, vorkommen-Elementen und wiederkehrenden Master Elementen, die aus einem Postfach im Exchange-Informationsspeicher gelöscht werden sollen. Der [DeleteItem-Vorgang](deleteitem-operation.md) kann für beliebige Elementtypen ausgeführt werden.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>Bemerkungen

Die **MoveToDeletedItems** -und **HardDelete** -Optionen sind transaktional, was bedeutet, dass die Datenbank zum Zeitpunkt des Abschlusses eines Webdienstaufrufs das Element in den Ordner "Gelöschte Elemente" verschoben oder das Element endgültig aus der Exchange-Datenbank entfernt hat. Dieses Verhalten ist für Microsoft Exchange Server 2007 und Exchange Server 2010 identisch. 
  
Die Option **SoftDelete** kann für unterschiedliche Zielversionen von Exchange anders verwendet werden. **SoftDelete** für Exchange 2007 legt ein Bit für das Element fest, das der Exchange-Datenbank angibt, dass das Element zu einem bestimmten Zeitpunkt in der Zukunft in den Ordner "Papierkorb" verschoben wird. **SoftDelete** für Exchange 2010 verschiebt das Element sofort in den Papierkorb. **SoftDelete** ist keine Option für das Löschen von Ordnern. **SoftDelete** Traversal sucht nach Elementen und Ordnern werden keine Ergebnisse zurückgegeben. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [DeleteItemResponse](deleteitemresponse.md)  
- [DeleteItem-Operation](deleteitem-operation.md)

