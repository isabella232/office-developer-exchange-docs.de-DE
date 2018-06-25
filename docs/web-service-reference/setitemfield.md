---
title: SetItemField
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SetItemField
api_type:
- schema
ms.assetid: 85284fcb-bd1e-4fda-9dab-cb4cd637cd5b
description: Das SetItemField-Element stellt eine Aktualisierung auf eine einzelne Eigenschaft eines Elements in einem UpdateItem Vorgang dar.
ms.openlocfilehash: 012e6ae21af653b4bf12588e5a97334a62884059
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831439"
---
# <a name="setitemfield"></a>SetItemField

Das Element **SetItemField** stellt eine Aktualisierung auf eine einzelne Eigenschaft eines Elements in einem [UpdateItem Vorgang](updateitem-operation.md)dar.
  
```xml
<SetItemField>
   <FieldURI/>
   <Item/>
</SetItemField>
```

 **SetItemFieldType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FieldURI](fielduri.md) <br/> |Identifiziert die Eigenschaften von URI häufig verwiesen wird.  <br/> |
|[IndexedFieldURI](indexedfielduri.md) <br/> |Einzelne Elemente eines Wörterbuchs identifiziert.  <br/> |
|[ExtendedFieldURI](extendedfielduri.md) <br/> |Bezeichnet die extended MAPI-Eigenschaften festlegen.  <br/> |
|[Element](item.md) <br/> |Stellt ein Element im Exchange-Informationsspeicher dar.  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |Stellt eine E-mail-Nachricht Exchange zu aktualisieren.  <br/> |
|[CalendarItem](calendaritem.md) <br/> |Stellt ein Element des Exchange-Kalender zu aktualisieren.  <br/> |
|[Contact](contact.md) <br/> |Stellt ein Exchange-Kontaktelement zu aktualisieren.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Stellt eine Verteilerliste aktualisieren.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Stellt eine Besprechungsnachricht zu aktualisieren.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |So aktualisieren Sie eine Besprechungsanfrage darstellt.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Stellt eine Antwort auf Besprechungsanfrage aktualisieren.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Aktualisieren einen Besprechungsabsage darstellt.  <br/> |
|[Aufgabe](task.md) <br/> |Stellt eine Aufgabe zu aktualisieren.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Updates (Element)](updates-item.md) <br/> |Enthält eine Reihe von Elementen, definieren anfügen, festlegen und Löschen von Änderungen an Elementeigenschaften.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[UpdateItem Operation](updateitem-operation.md)

