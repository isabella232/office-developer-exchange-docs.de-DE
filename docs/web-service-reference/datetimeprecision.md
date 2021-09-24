---
title: DateTimePrecision
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 822dc5a6-2d57-474b-8a7d-da150898e5b6
description: Das DateTimePrecision-Element gibt die Genauigkeit für zurückgegebene Datums-/Uhrzeitwerte an.
ms.openlocfilehash: 075e37bfdd2c61f56352e000ef6cc5810dd81bbb
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59535710"
---
# <a name="datetimeprecision"></a>DateTimePrecision

Das **DateTimePrecision-Element** gibt die Genauigkeit für zurückgegebene Datums-/Uhrzeitwerte an. 
  
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

Das **DateTimePrecision-Element** befindet sich im SOAP-Header. 
  
## <a name="text-value"></a>Textwert

Ein Textwert ist erforderlich. Im Folgenden sind die möglichen Werte aufgeführt:
  
- Sekunden
    
- Millisekunden
    
## <a name="remarks"></a>HinwBemerkungeneise

Wenn ein SOAP-Header verwendet wird, für den das **DateTimePrecision-Element** auf "Seconds" festgelegt ist, werden Datums-/Uhrzeitwerte an die nächsten Sekunden (00:00:00) zurückgegeben. Wenn "Millisekunden" verwendet wird, werden Datums-/Uhrzeitwerte an die nächste Millisekunden (00:00:00,0000) zurückgegeben. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
Dieses Element wurde in Exchange Server 2010 Service Pack 2 (SP2) eingeführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   

