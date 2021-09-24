---
title: RemoveItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- RemoveItem
api_type:
- schema
ms.assetid: 766878e3-9007-454f-8501-45139bc5c0e2
description: Das RemoveItem-Element stellt ein Antwortobjekt dar, das verwendet wird, um ein Besprechungselement zu entfernen, wenn eine MeetingCancellation-Nachricht empfangen wird.
ms.openlocfilehash: 4dbe9ede36bf6e3c008a2186cfe617519ecfae1f
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59517959"
---
# <a name="removeitem"></a>RemoveItem

Das **RemoveItem-Element** stellt ein Antwortobjekt dar, das verwendet wird, um ein Besprechungselement zu entfernen, wenn eine MeetingCancellation-Nachricht empfangen wird. 
  
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
|**ObjectName** <br/> |Stellt den Namen der RemoveItem-Antwortobjektklasse als englische Zeichenfolge dar.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ReferenceItemId](referenceitemid.md) <br/> |Gibt das Element an, auf das sich das RemoveItem-Antwortobjekt bezieht.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Items (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md) <br/> |Enthält ein Array von Elementen, die im Ordner erstellt werden sollen, der vom [ParentFolderId (TargetFolderIdType)-Element](parentfolderid-targetfolderidtype.md) identifiziert wird.  <br/> |
|[ResponseObjects](responseobjects.md) <br/> |Enthält eine Auflistung aller Antwortobjekte, die einem Element im Exchange Speicher zugeordnet sind.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

 **RemoveItem** ist nur für eine [MeetingCancellation](meetingcancellation.md)gültig. Andernfalls wird ein Fehler ausgelöst.
  
> [!NOTE]
> Die [ItemClass](itemclass.md) für eine Besprechungsabsage ist IPM. Schedule.Meeting.Canceled. 
  
Verwenden Sie zum Entfernen eines [MeetingRequest-Objekts](meetingrequest.md) und des [zugehörigen CalendarItem-Objekts](calendaritem.md)das [DeclineItem-Antwortobjekt](declineitem.md) anstelle von **RemoveItem**.
  
 **RemoveItem** wird für den Delegatenzugriff nicht unterstützt. 
  
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

