---
title: DateTimePrecision
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 822dc5a6-2d57-474b-8a7d-da150898e5b6
description: Das DateTimePrecision-Element gibt die Genauigkeit für zurückgegebenen Datums-/Uhrzeitwerte.
ms.openlocfilehash: 4d11598628228b41adf021adbbaa77e6348534bb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757860"
---
# <a name="datetimeprecision"></a>DateTimePrecision

Das **DateTimePrecision** -Element gibt die Genauigkeit für zurückgegebenen Datums-/Uhrzeitwerte. 
  
```XML
<DateTimePrecision />
```

**DateTimePrecisionType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

Das Element **DateTimePrecision** befindet sich die SOAP-Header. 
  
## <a name="text-value"></a>Textwert

Ein Textwert ist erforderlich. Im Folgenden sind die möglichen Werte aufgeführt:
  
- Sekunden
    
- Millisekunden
    
## <a name="remarks"></a>Hinweise

Wenn ein SOAP-Header mit dem **DateTimePrecision** -Element "Sekunden" verwendet wird, Datum/Uhrzeit-Werte werden zurückgegeben, auf die nächsten Sekunden (00: 00:00). Wenn "Millisekunden" verwendet werden, Datum/Uhrzeit-Werte werden auf die nächste Millisekunde (00:00:00.0000) zurückgegeben. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
Dieses Element wurde in Exchange Server 2010 Service Pack 2 (SP2) eingeführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   

