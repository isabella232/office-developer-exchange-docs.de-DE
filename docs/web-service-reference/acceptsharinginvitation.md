---
title: AcceptSharingInvitation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AcceptSharingInvitation
api_type:
- schema
ms.assetid: 3c2a47d6-490d-425b-8893-089a4f8882cd
description: Das AcceptSharingInvitation-Element wird verwendet, um eine Einladung zu akzeptieren, die den Zugriff auf die Kalender-oder Kontaktdaten eines anderen Benutzers zulässt.
ms.openlocfilehash: c8cdae707bd122e74fa0e284163d1540d857c3de
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461709"
---
# <a name="acceptsharinginvitation"></a>AcceptSharingInvitation

Das **AcceptSharingInvitation** -Element wird verwendet, um eine Einladung zu akzeptieren, die den Zugriff auf die Kalender-oder Kontaktdaten eines anderen Benutzers zulässt. 
  
```xml
<AcceptSharingInvitation>
   <ReferenceItemId/>
</AcceptSharingInvitation>
```

 **AcceptSharingInvitationType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ReferenceItemId](referenceitemid.md) <br/> |Gibt das Element an, auf das das Response-Objekt verweist.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ResponseObjects](responseobjects.md) <br/> |Enthält eine Auflistung aller Response-Objekte, die einem Element in der Exchange-Informationsspeicher zugeordnet sind.  <br/> |
|[Elemente (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md) <br/> |Enthält ein Array von Elementen, die in dem Ordner erstellt werden sollen, der durch das [parentfolderid (TargetFolderIdType)-](parentfolderid-targetfolderidtype.md) Element identifiziert wird.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [CreateItem (AcceptSharingInvitation)](createitem-acceptsharinginvitation.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

