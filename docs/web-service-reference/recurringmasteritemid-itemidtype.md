---
title: RecurringMasterItemId (ItemIdType)
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 48d831cf-10d8-480b-86d2-f9c0b14b8167
description: Das RecurringMasterItemId (ItemIdType)-Element identifiziert ein Master-Shape Recurrence-Element durch das Identifizieren von Bezeichner eines seiner Elemente verwandte vorkommen.
ms.openlocfilehash: 89089067963e99ac1a6cae6ea6e1e8350d148e82
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831010"
---
# <a name="recurringmasteritemid-itemidtype"></a>RecurringMasterItemId (ItemIdType)

Das **RecurringMasterItemId (ItemIdType)** -Element identifiziert ein Master-Shape Recurrence-Element durch das Identifizieren von Bezeichner eines seiner Elemente verwandte vorkommen. 
  
```XML
<RecurringMasterItemId Id="" ChangeKey=""/>
```

 **ItemIdType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

****

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|Id  <br/> |Gibt ein einzelnes Vorkommen des ein wiederkehrendes master-Objekt. Dieses Attribut ist erforderlich.  <br/> |
|ChangeKey  <br/> |Identifiziert eine bestimmte Version für ein einzelnes Auftreten eines sich wiederholenden master-Elements an. Darüber hinaus wird wiederkehrenden master-Objekts auch identifiziert, da es und die einzelnen Vorkommen der gleichen Änderungsschlüssel enthalten. Dieses Attribut ist optional.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[Reminder](reminder.md)
  
## <a name="remarks"></a>Hinweise

Dieses Element wurde in Exchange Server 2013 Service Pack 1 (SP1) eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Reminder](reminder.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

