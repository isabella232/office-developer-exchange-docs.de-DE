---
title: RecurringMasterItemId (ItemIdType)
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 48d831cf-10d8-480b-86d2-f9c0b14b8167
description: Das RecurringMasterItemId (ItemIdType)-Element identifiziert ein Serienmasterelement, indem die Bezeichner eines der zugehörigen Vorkommenselemente identifiziert werden.
ms.openlocfilehash: 491bb6686ad6cc9ee8169144b659d828e3920e45
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522740"
---
# <a name="recurringmasteritemid-itemidtype"></a>RecurringMasterItemId (ItemIdType)

Das **RecurringMasterItemId (ItemIdType)-Element** identifiziert ein Serienmasterelement, indem die Bezeichner eines der zugehörigen Vorkommenselemente identifiziert werden. 
  
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
|Id  <br/> |Identifiziert ein einzelnes Vorkommen eines wiederkehrenden Masterelements. Dieses Attribut ist erforderlich.  <br/> |
|ChangeKey  <br/> |Identifiziert eine bestimmte Version eines einzelnen Vorkommens eines wiederkehrenden Masterelements. Darüber hinaus wird das wiederkehrende Masterelement auch identifiziert, da es und das einzelne Vorkommen denselben Änderungsschlüssel enthalten. Dieses Attribut ist optional.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[Reminder](reminder.md)
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 Service Pack 1 (SP1) eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Reminder](reminder.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

