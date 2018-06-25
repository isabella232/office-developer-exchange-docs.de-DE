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
description: Das DeleteItem-Element definiert eine Anforderung zum Löschen eines Elements aus einem Postfach im Exchange-Speicher.
ms.openlocfilehash: de64787750c88c8a47bb69daddc0a1d2ebe8bde9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757932"
---
# <a name="deleteitem"></a>DeleteItem

Das **DeleteItem** -Element definiert eine Anforderung zum Löschen eines Elements aus einem Postfach im Exchange-Speicher. 
  
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
|**"SendMeetingCancellations"** <br/> |Beschreibt, ob eine Kalender Element Löschung an die Teilnehmer weitergeleitet wird. Dieses Attribut ist erforderlich, wenn die Elemente im Kalender gelöscht werden. Dieses Attribut ist optional, wenn nichtkalenderelemente gelöscht werden.  <br/> |
|**"AffectedTaskOccurrences"** <br/> |Beschreibt, ob eine Aufgabeninstanz oder ein Master-Shape Aufgabe durch eine [DeleteItem Vorgang](deleteitem-operation.md)gelöscht wird. Dieses Attribut ist erforderlich, wenn Vorgänge gelöscht werden. Dieses Attribut ist optional, wenn nicht Aufgabenelementen gelöscht werden.  <br/> |
|**SuppressReadReceipts** <br/> |Gibt an, ob lesebestätigungen für das gelöschte Element unterdrückt werden. Der Textwert **true**, gibt an, dass die lesebestätigungen unterdrückt werden. Der Wert **false** gibt an, dass die lesebestätigungen an den Absender gesendet werden. Dieses Attribut ist optional.  <br/> |
   
#### <a name="deletetype-attribute"></a>DeleteType-Attribut

|**Wert**|**Beschreibung**|
|:-----|:-----|
|HardDelete  <br/> |Ein Element wird dauerhaft aus dem Speicher entfernt.  <br/> |
|SoftDelete  <br/> |Ein Element wird verschoben, um die Dumpster Wenn die Dumpster ist aktiviert.  <br/> |
|MoveToDeletedItems  <br/> |Ein Element wird in den Ordner Gelöschte Objekte verschoben.  <br/> |
   
#### <a name="sendmeetingcancellations-attribute"></a>Attribut "SendMeetingCancellations"

|**Wert**|**Beschreibung**|
|:-----|:-----|
|SendToNone  <br/> |Ein Kalenderelement wird gelöscht, ohne eine Absage senden.  <br/> |
|SendOnlyToAll  <br/> |Ein Kalenderelement wird gelöscht und eine Absage an alle Teilnehmer gesendet.  <br/> |
|SendToAllAndSaveCopy  <br/> |Ein Kalenderelement wird gelöscht und eine Absage an alle Teilnehmer gesendet. Eine Kopie der Nachricht Abbruch wird im Ordner "Gesendete Elemente" gespeichert.  <br/> |
   
#### <a name="affectedtaskoccurrences-attribute"></a>Attribut "AffectedTaskOccurrences"

|**Wert**|**Beschreibung**|
|:-----|:-----|
|AllOccurrences  <br/> |Anforderung für das Element löschen Löscht die Aufgabe Master-Shape, und daher alle Aufgabenserien, sind der master Aufgabe zugeordnet.  <br/> |
|SpecifiedOccurrenceOnly  <br/> |Anforderung für das Element löschen Löscht nur bestimmte Vorkommen eines Vorgangs.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Artikelnummern ein.](itemids.md) <br/> |Enthält ein Array von Elementen, Vorkommen Elemente und master Terminserien aus einem Postfach im Exchange-Speicher zu löschen. Die [DeleteItem Vorgang](deleteitem-operation.md) kann auf einem beliebigen Element ausgeführt werden.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>Hinweise

Die Optionen **MoveToDeletedItems** und **HardDelete** sind transaktional, was bedeutet, dass jeweils ein Webdienstaufruf abgeschlossen ist, die Datenbank hat das Element in den Ordner Gelöschte Objekte verschoben oder dauerhaft entfernt das Element aus der Exchange-Datenbank. Dieses Verhalten gilt für MicrosoftExchange Server 2007 und Exchange Server 2010. 
  
Die Option **SoftDelete** funktioniert anders für andere Versionen von Exchange. **SoftDelete** für Exchange 2007 legt etwas auf das Element, das in der Exchange-Datenbank angibt, die das Element verschoben werden die Dumpster Ordner zu einem unbestimmten Zeitpunkt in der Zukunft. **SoftDelete** für Exchange 2010 sofort verschoben wird das Element, das die Dumpster. **SoftDelete** ist keine Option zum Ordner löschen. **SoftDelete** durchqueren Suchvorgänge für Elemente und Ordner werden keine Ergebnisse zurückgegeben. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [DeleteItemResponse](deleteitemresponse.md)  
- [DeleteItem-Operation](deleteitem-operation.md)

