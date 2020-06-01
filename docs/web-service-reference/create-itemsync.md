---
title: Erstellen (ItemSync)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Create
api_type:
- schema
ms.assetid: cb5e64a2-66a5-4447-921e-7c13efb8f6bf
description: Das Create-Element identifiziert ein einzelnes Element, das im lokalen Clientspeicher erstellt werden soll.
ms.openlocfilehash: b9c0f28333594a6c17ee9581a227fc4773874fd6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460799"
---
# <a name="create-itemsync"></a>Erstellen (ItemSync)

Das **Create** -Element identifiziert ein einzelnes Element, das im lokalen Clientspeicher erstellt werden soll. 
  
- [SyncFolderItemsResponse](syncfolderitemsresponse.md) 
- [ResponseMessages](responsemessages.md) 
- [SyncFolderItemsResponseMessage](syncfolderitemsresponsemessage.md) 
- [Änderungen (Elemente)](changes-items.md) 
- [Erstellen (ItemSync)](create-itemsync.md)
  
```xml
<Create>
   <Item/>
</Create>
```

```xml
<Create>
   <Task/> 
</Create>
```

```xml
<Create>
   <MeetingResponse/>
</Create>
```

```xml
<Create>
   <CalendarItem/>
</Create>
```

```xml
<Create>
   <MeetingMessage/>
</Create>
```

```xml
<Create>
   <DistributionList/>
</Create>
```

```xml
<Create>
   <MeetingCancellation/>
</Create>
```

```xml
<Create>
   <MeetingRequest/> 
</Create>
```

```xml
<Create>
   <Message/> 
</Create>
```

```xml
<Create>
   <Contact/> 
</Create>
```

**SyncFolderItemsCreateOrUpdateType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Item](item.md) <br/> |Stellt ein generisches Exchange-Element zum Erstellen dar.  <br/> |
|[Nachricht](message-ex15websvcsotherref.md) <br/> |Stellt eine zu erstellenden Exchange-e-Mail-Nachricht dar.  <br/> |
|[CalendarItem](calendaritem.md) <br/> |Stellt ein zu Erstell Exchange-Kalenderelement dar.  <br/> |
|[Kontakt](contact.md) <br/> |Stellt ein zu Erstell Exchange-Kontaktelement dar.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Stellt eine zu erstellende Verteilerliste dar.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Stellt eine zu erstellende Besprechungsnachricht dar.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Stellt eine Besprechungsanfrage zum Erstellen dar.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Stellt eine Besprechungsantwort dar, die erstellt werden soll.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Stellt eine zu Erstell endabbruch Besprechung dar.  <br/> |
|[Aufgabe](task.md) <br/> |Stellt eine Aufgabe dar, die erstellt werden soll.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Änderungen (Elemente)](changes-items.md) <br/> |Enthält ein Sequenz Array von Änderungstypen, die die Arten von Unterschieden zwischen den Elementen auf dem Client und den Elementen auf dem Exchange-Server darstellen.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [SyncFolderItems-Vorgang](syncfolderitems-operation.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

