---
title: RecurringMasterItemId (itemidtype)
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 48d831cf-10d8-480b-86d2-f9c0b14b8167
description: Das RecurringMasterItemId (itemidtype)-Element identifiziert ein Serienmasterelement durch Identifizieren der Bezeichner eines seiner Verwandten vorkommen Elemente.
ms.openlocfilehash: c725998ad3a728ef1f47ff6491592b461753b895
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468439"
---
# <a name="recurringmasteritemid-itemidtype"></a>RecurringMasterItemId (itemidtype)

Das **RecurringMasterItemId (itemidtype)-** Element identifiziert ein Serienmasterelement durch Identifizieren der Bezeichner eines seiner Verwandten vorkommen Elemente. 
  
```XML
<RecurringMasterItemId Id="" ChangeKey=""/>
```

 **Itemidtype**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

****

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|Id  <br/> |Gibt ein einzelnes Vorkommen eines wiederkehrenden Hauptelements an. Dieses Attribut ist erforderlich.  <br/> |
|ChangeKey  <br/> |Gibt eine bestimmte Version eines einzelnen Auftretens eines wiederkehrenden Hauptelements an. Darüber hinaus wird das wiederkehrende Hauptelement ebenfalls identifiziert, da es und das einzelne Vorkommen denselben Änderungsschlüssel enthalten werden. Dieses Attribut ist optional.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[Reminder](reminder.md)
  
## <a name="remarks"></a>Bemerkungen

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

