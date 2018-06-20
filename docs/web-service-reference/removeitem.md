---
title: RemoveItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RemoveItem
api_type:
- schema
ms.assetid: 766878e3-9007-454f-8501-45139bc5c0e2
description: Das RemoveItem-Element stellt ein Response-Objekt, das verwendet wird, um ein Besprechungselement zu entfernen, wenn eine Nachricht MeetingCancellation empfangen wird.
ms.openlocfilehash: 6897363eba602e6a135ad255822197f9296dd44a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831108"
---
# <a name="removeitem"></a>RemoveItem

Das **RemoveItem** -Element stellt ein Response-Objekt, das verwendet wird, um ein Besprechungselement zu entfernen, wenn eine Nachricht MeetingCancellation empfangen wird. 
  
```xml
<RemoveItem ObjectName="">
   <ReferenceItemId/>
</RemoveItem>
```

 **RemoveItemType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**ObjectName** <br/> |Stellt den Namen der RemoveItem Antwort Object-Klasse als eine englische Zeichenfolge dar.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ReferenceItemId](referenceitemid.md) <br/> |Identifiziert das Element auf dem RemoveItem-Response-Objekt verweist.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Elemente (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md) <br/> |Enthält ein Array von Elementen im Ordner zu erstellen, die durch das Element [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) bezeichnet wird.  <br/> |
|[ResponseObjects](responseobjects.md) <br/> |Enthält eine Auflistung aller Antwort-Objekte, die ein Element in der Exchange-Informationsspeicher zugeordnet sind.  <br/> |
   
## <a name="remarks"></a>Hinweise

 **RemoveItem** ist nur für eine [MeetingCancellation](meetingcancellation.md)gültig. Andernfalls wird ein Fehler ausgelöst.
  
> [!NOTE]
> Die [ItemClass](itemclass.md) für einen Besprechungsabsage lautet IPM. Schedule.Meeting.Canceled. 
  
Verwenden Sie zum Entfernen einer [MeetingRequest](meetingrequest.md) und die zugehörigen [CalendarItem](calendaritem.md) [DeclineItem](declineitem.md) -Response-Objekt anstelle von **RemoveItem**.
  
 **RemoveItem** wird für Stellvertretungszugriff nicht unterstützt. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

