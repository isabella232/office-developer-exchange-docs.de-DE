---
title: HasEndTimeChanged
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a0eb444d-8e2e-478b-b785-2b9787ffb226
description: Das HasEndTimeChanged-Element gibt an, ob die Endzeit für eine Besprechung geändert wurde.
ms.openlocfilehash: 15ad52c7b7581cce5ca96ba5ff4e8a1c130a02cf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461786"
---
# <a name="hasendtimechanged"></a>HasEndTimeChanged

Das **HasEndTimeChanged** -Element gibt an, ob die Endzeit für eine Besprechung geändert wurde. 
  
```XML
<HasEndTimeChanged>true | false</HasEndTimeChanged>
```

 **Boolescher Wert**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ChangeHighlights](changehighlights.md) <br/> |Gibt an, was zwischen zwei Versionen einer Besprechungsanfrage Nachricht geändert wurde.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert **true** für das **HasEndTimeChanged** -Element gibt an, dass die Endzeit einer Besprechung geändert wurde. Der Wert **false** gibt an, dass die Endzeit einer Besprechung nicht geändert wurde. 
  
## <a name="remarks"></a>Bemerkungen

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Typschema  <br/> |
|Überprüfungsdatei  <br/> |Types. xsd  <br/> |
|Kann leer sein  <br/> ||
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

