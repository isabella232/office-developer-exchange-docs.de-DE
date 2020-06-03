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
description: Das RemoveItem-Element stellt ein Response-Objekt dar, das zum Entfernen eines Besprechungselements verwendet wird, wenn eine MeetingCancellation-Nachricht empfangen wird.
ms.openlocfilehash: c0cd5c1f9894287ee78c2f7a65b8f4d3b943414e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467690"
---
# <a name="removeitem"></a>RemoveItem

Das **RemoveItem** -Element stellt ein Response-Objekt dar, das zum Entfernen eines Besprechungselements verwendet wird, wenn eine MeetingCancellation-Nachricht empfangen wird. 
  
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
|**ObjectName** <br/> |Stellt den Namen der RemoveItem-Antwortobjekt Klasse als englische Zeichenfolge dar.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ReferenceItemId](referenceitemid.md) <br/> |Gibt das Element an, auf das das RemoveItem-Antwortobjekt verweist.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Elemente (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md) <br/> |Enthält ein Array von Elementen, die in dem Ordner erstellt werden sollen, der durch das [parentfolderid (TargetFolderIdType)-](parentfolderid-targetfolderidtype.md) Element identifiziert wird.  <br/> |
|[ResponseObjects](responseobjects.md) <br/> |Enthält eine Auflistung aller Response-Objekte, die einem Element in der Exchange-Informationsspeicher zugeordnet sind.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

 **RemoveItem** ist nur für eine [MeetingCancellation](meetingcancellation.md)gültig. Andernfalls wird ein Fehler ausgelöst.
  
> [!NOTE]
> Das [ItemClass](itemclass.md) für eine Besprechungsabsage ist IPM. Schedule. Meeting. Canceled. 
  
Verwenden Sie zum Entfernen einer [MeetingRequest](meetingrequest.md) und der zugeordneten [CalendarItem](calendaritem.md)das [DeclineItem](declineitem.md) -Antwortobjekt anstelle von **RemoveItem**.
  
 **RemoveItem** wird für den Stellvertretungszugriff nicht unterstützt. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

