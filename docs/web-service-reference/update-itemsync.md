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
description: Das Update-Element identifiziert ein einzelnes Element in den Speicher des lokalen Client aktualisieren.
ms.openlocfilehash: bf560f18184151a3f17d7016d05cdb725db934ae
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353630"
---
# <a name="update-itemsync"></a>Update (ItemSync)

**Update** -Elements gibt ein einzelnes Element in den Speicher des lokalen Client aktualisieren. 
  
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
|[Item](item.md) <br/> |Stellt ein generisches Exchange-Element zu aktualisieren.  <br/> |
|[Meldung](message-ex15websvcsotherref.md) <br/> |Stellt eine E-mail-Nachricht Exchange zu aktualisieren.  <br/> |
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
|[Änderungen (Elemente)](changes-items.md) <br/> |Enthält ein Array Sequenz von Dateitypen ändern, die den Typ der Unterschiede zwischen den Elementen auf dem Client und der Elemente auf dem Exchange-Server darstellen.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [SyncFolderItems-Vorgang](syncfolderitems-operation.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

