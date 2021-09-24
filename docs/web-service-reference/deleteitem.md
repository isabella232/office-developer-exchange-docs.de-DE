---
title: DeleteItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- DeleteItem
api_type:
- schema
ms.assetid: 055cdee8-3c7d-47db-9f27-740f4a674729
description: Das DeleteItem-Element definiert eine Anforderung zum Löschen eines Elements aus einem Postfach im Exchange Speicher.
ms.openlocfilehash: aa421de447126a22c1f01b3a0dc7498ff5b74a65
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59528887"
---
# <a name="deleteitem"></a>DeleteItem

Das **DeleteItem-Element** definiert eine Anforderung zum Löschen eines Elements aus einem Postfach im Exchange Speicher. 
  
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
|**DeleteType** <br/> |Beschreibt, wie ein Element gelöscht wird. Dieses Attribut ist erforderlich.  <br/> |
|**SendMeetingCancellations** <br/> |Beschreibt, ob den Teilnehmern das Löschen eines Kalenderelements mitgeteilt wird. Dieses Attribut ist erforderlich, wenn Kalenderelemente gelöscht werden. Dieses Attribut ist optional, wenn Nicht-Kalenderelemente gelöscht werden.  <br/> |
|**AffectedTaskOccurrences** <br/> |Beschreibt, ob eine Vorgangsinstanz oder ein Aufgabenmaster durch einen [DeleteItem-Vorgang](deleteitem-operation.md)gelöscht wird. Dieses Attribut ist erforderlich, wenn Aufgaben gelöscht werden. Dieses Attribut ist optional, wenn Nicht-Aufgabenelemente gelöscht werden.  <br/> |
|**SuppressReadReceipts** <br/> |Gibt an, ob Lesebestätigungen für das gelöschte Element unterdrückt werden. Der Textwert **"true"** gibt an, dass die Lesebestätigungen unterdrückt werden. Der Wert **"false"** gibt an, dass die Lesebestätigungen an den Absender gesendet werden. Dieses Attribut ist optional.  <br/> |
   
#### <a name="deletetype-attribute"></a>DeleteType-Attribut

|**Wert**|**Beschreibung**|
|:-----|:-----|
|HardDelete  <br/> |Ein Element wird dauerhaft aus dem Speicher entfernt.  <br/> |
|SoftDelete  <br/> |Ein Element wird in den Dumpster verschoben, wenn der Dumpster aktiviert ist.  <br/> |
|MoveToDeletedItems  <br/> |Ein Element wird in den Ordner "Gelöschte Elemente" verschoben.  <br/> |
   
#### <a name="sendmeetingcancellations-attribute"></a>SendMeetingCancellations-Attribut

|**Wert**|**Beschreibung**|
|:-----|:-----|
|SendToNone  <br/> |Ein Kalenderelement wird gelöscht, ohne eine Abbruchnachricht zu senden.  <br/> |
|SendOnlyToAll  <br/> |Ein Kalenderelement wird gelöscht, und eine Abbruchnachricht wird an alle Teilnehmer gesendet.  <br/> |
|SendToAllAndSaveCopy  <br/> |Ein Kalenderelement wird gelöscht, und eine Abbruchnachricht wird an alle Teilnehmer gesendet. Eine Kopie der Abbruchnachricht wird im Ordner "Gesendete Elemente" gespeichert.  <br/> |
   
#### <a name="affectedtaskoccurrences-attribute"></a>AffectedTaskOccurrences-Attribut

|**Wert**|**Beschreibung**|
|:-----|:-----|
|AllOccurrences  <br/> |Eine Anforderung zum Löschen von Elementen löscht die Hauptaufgabe und damit alle wiederkehrenden Aufgaben, die der Hauptaufgabe zugeordnet sind.  <br/> |
|SpecifiedOccurrenceOnly  <br/> |Eine Löschelementanforderung löscht nur bestimmte Vorkommen einer Aufgabe.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ItemIds](itemids.md) <br/> |Enthält ein Array von Elementen, Vorkommenselementen und wiederkehrenden Masterelementen, die aus einem Postfach im Exchange Speicher gelöscht werden sollen. Der [DeleteItem-Vorgang](deleteitem-operation.md) kann für jeden Elementtyp ausgeführt werden.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Die Optionen **MoveToDeletedItems** und **HardDelete** sind transaktional, d. h., wenn ein Webdienstaufruf abgeschlossen ist, hat die Datenbank das Element in den Ordner "Gelöschte Elemente" verschoben oder das Element dauerhaft aus der Exchange Datenbank entfernt. Dieses Verhalten ist für MicrosoftExchange Server 2007 und Exchange Server 2010 identisch. 
  
Die **Option SoftDelete** funktioniert für unterschiedliche Zielversionen von Exchange unterschiedlich. **SoftDelete** für Exchange 2007 legt ein Bit für das Element fest, das der Exchange-Datenbank angibt, dass das Element zu einem unbestimmten Zeitpunkt in der Zukunft in den Dumpsterordner verschoben wird. **SoftDelete** für Exchange 2010 verschiebt das Element sofort in den Dumpster. **SoftDelete** ist keine Option zum Löschen von Ordnern. **SoftDelete-Traversalsuchen** nach Elementen und Ordnern geben keine Ergebnisse zurück. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [DeleteItemResponse](deleteitemresponse.md)  
- [DeleteItem-Vorgang](deleteitem-operation.md)

