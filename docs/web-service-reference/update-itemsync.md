---
title: Update (ItemSync)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Update
api_type:
- schema
ms.assetid: 4e204446-1c80-44f9-b93b-77ce630a01a5
description: Das Update-Element identifiziert ein einzelnes Element, das im lokalen Clientspeicher aktualisiert werden soll.
ms.openlocfilehash: 12248cbbd5d47a19e36d49fcebe6d4753a2e162f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468887"
---
# <a name="update-itemsync"></a>Update (ItemSync)

Das **Update** -Element identifiziert ein einzelnes Element, das im lokalen Clientspeicher aktualisiert werden soll. 
  
- [SyncFolderItemsResponse](syncfolderitemsresponse.md) 
- [ResponseMessages](responsemessages.md)  
- [SyncFolderItemsResponseMessage](syncfolderitemsresponsemessage.md)  
- [Änderungen (Elemente)](changes-items.md)  
- [Update (ItemSync)](update-itemsync.md)
  
```xml
<Update>
   <Item/>
</Update>
```

```xml
<Update>
   <MeetingRequest/>
</Update>
```

```xml
<Update>
   <MeetingCancellation/>
</Update>
```

```xml
<Update>
   <Task/>
</Update>
```

```xml
<Update>
   <CalendarItem/>
</Update>
```

```xml
<Update>
   <MeetingResponse/>
</Update>
```

```xml
<Update>
   <Message/>
</Update>
```

```xml
<Update>
   <DistributionList/>
</Update>
```

```xml
<Update>
   <MeetingMessage/>
</Update>
```

```xml
<Update>
   <Contact/> 
</Update>
```

**SyncFolderItemsCreateOrUpdateType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Item](item.md) <br/> |Stellt ein generisches Exchange-Element dar, das aktualisiert werden soll.  <br/> |
|[Meldung](message-ex15websvcsotherref.md) <br/> |Stellt eine zu aktualisierenden Exchange-e-Mail-Nachricht dar.  <br/> |
|[CalendarItem](calendaritem.md) <br/> |Stellt ein zu aktualisieres Exchange-Kalenderelement dar.  <br/> |
|[Contact](contact.md) <br/> |Stellt ein zu aktualisieres Exchange-Kontaktelement dar.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Stellt eine zu aktualisierende Verteilerliste dar.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Stellt eine zu aktualisierende Besprechungs Meldung dar.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Stellt eine Besprechungsanfrage zum Aktualisieren dar.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Stellt eine Besprechungsantwort dar, die aktualisiert werden soll.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Stellt einen Besprechungs Abbruch dar, der aktualisiert werden soll.  <br/> |
|[Task](task.md) <br/> |Stellt eine Aufgabe dar, die aktualisiert werden soll.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Änderungen (Elemente)](changes-items.md) <br/> |Enthält ein Sequenz Array von Änderungstypen, die die Art der Unterschiede zwischen den Elementen auf dem Client und den Elementen auf dem Exchange-Server darstellen.  <br/> |
   
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

