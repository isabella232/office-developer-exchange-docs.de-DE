---
title: DateTimePrecision
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 822dc5a6-2d57-474b-8a7d-da150898e5b6
description: Das DateTimePrecision-Element gibt die Genauigkeit für zurückgegebene Datum/Uhrzeit-Werte an.
ms.openlocfilehash: 9d245dfb0123daae42ba9b9b4e98aff872b67d80
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529224"
---
# <a name="datetimeprecision"></a>DateTimePrecision

Das **DateTimePrecision** -Element gibt die Genauigkeit für zurückgegebene Datum/Uhrzeit-Werte an. 
  
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

Das **DateTimePrecision** -Element befindet sich im SOAP-Header. 
  
## <a name="text-value"></a>Textwert

Ein Textwert ist erforderlich. Im Folgenden sind die möglichen Werte aufgeführt:
  
- Sekunden
    
- Millisekunden
    
## <a name="remarks"></a>Bemerkungen

Wenn ein SOAP-Header mit dem **DateTimePrecision** -Element auf "seconds" festgelegt wird, werden Datum/Uhrzeit-Werte an die nächsten Sekunden zurückgegeben (00:00:00). Wenn "Millisekunden" verwendet wird, werden die Werte für Datum/Uhrzeit an die nächste Millisekunde zurückgegeben (00:00:00.0000). 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
Dieses Element wurde in Exchange Server 2010 Service Pack 2 (SP2) eingeführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   

