---
title: Name (Nachrichtenverfolgung)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Name
api_type:
- schema
ms.assetid: a1669f6d-53f3-4849-9b30-56909aaeac82
description: Das Name-Element stellt den Eigenschaftennamen für einen Nachrichtenverfolgungsbericht dar.
ms.openlocfilehash: b57c109cfbcb2744ae6854e0afce52e240d22b30
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59515453"
---
# <a name="name-message-tracking"></a>Name (Nachrichtenverfolgung)

Das **Name-Element** stellt den Eigenschaftennamen für einen Nachrichtenverfolgungsbericht dar. 
  
```xml
<Name/>
```

**String**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[TrackingPropertyType](trackingpropertytype.md) <br/> |Stellt ein Name-Wert-Zeichenfolgenpaar dar, das zum Erstellen von Eigenschaften für Nachrichtenverfolgungsberichte verwendet wird.  <br/> |
   
## <a name="text-value"></a>Textwert

Wenn dieses Element verwendet wird, ist ein Textwert erforderlich.
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element kann höchstens einmal im [TrackingPropertyType-Element](trackingpropertytype.md) auftreten. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

