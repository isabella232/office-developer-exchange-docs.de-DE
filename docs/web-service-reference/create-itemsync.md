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
description: Das Create-Element identifiziert ein einzelnes Element in der lokalen Client-Speicher zu erstellen.
ms.openlocfilehash: 39056bcaab3577b1b729421118a45571910922fc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757737"
---
# <a name="create-itemsync"></a>Erstellen (ItemSync)

Das **Create** -Element identifiziert ein einzelnes Element in der lokalen Client-Speicher zu erstellen. 
  
[SyncFolderItemsResponse](syncfolderitemsresponse.md)
  
[ResponseMessages](responsemessages.md)
  
[SyncFolderItemsResponseMessage](syncfolderitemsresponsemessage.md)
  
[Änderungen (Elemente)](changes-items.md)
  
[Erstellen (ItemSync)](create-itemsync.md)
  
```xml
<Create>
   <Item/>
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
|[Item](item.md) <br/> |So erstellen Sie ein generisches Exchange-Element darstellt.  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |So erstellen Sie eine Exchange E-mail-Nachricht darstellt.  <br/> |
|[CalendarItem](calendaritem.md) <br/> |So erstellen Sie ein Exchange-Kalender-Element darstellt.  <br/> |
|[Contact](contact.md) <br/> |So erstellen Sie ein Exchange-Kontaktelement darstellt.  <br/> |
|[DistributionList](distributionlist.md) <br/> |So erstellen Sie eine Verteilerliste darstellt.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Stellt eine Besprechungsnachricht zu erstellen.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |So erstellen Sie eine Besprechungsanfrage darstellt.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |So erstellen Sie eine Antwort auf Besprechungsanfrage darstellt.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |So erstellen Sie einen Besprechungsabsage darstellt.  <br/> |
|[Aufgabe](task.md) <br/> |So erstellen Sie eine Aufgabe darstellt.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Änderungen (Elemente)](changes-items.md) <br/> |Enthält ein Array Sequenz von Dateitypen ändern, die die Typen der Unterschiede zwischen den Elementen auf dem Client und der Elemente auf dem Exchange-Server darstellen.  <br/> |
   
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



[SyncFolderItems-Vorgang](syncfolderitems-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

