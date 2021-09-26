---
title: RequestType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- RequestType
api_type:
- schema
ms.assetid: 4e657e57-528f-4250-a99c-f9850bbbcec5
description: Das RequestType-Element gibt an, ob es sich bei einer Proxyanforderung um eine standortübergreifende oder eine gesamtstrukturübergreifende Anforderung handelt.
ms.openlocfilehash: 3390381b903c7a39a1d2ea6cae80b3fbc07eba43
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59541854"
---
# <a name="requesttype"></a>RequestType

Das **RequestType-Element** gibt an, ob es sich bei einer Proxyanforderung um eine standortübergreifende oder eine gesamtstrukturübergreifende Anforderung handelt. 
  
```xml
<RequestType>CrossSite or CrossForest</RequestType>
```

 **AvailabilityProxyRequestType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

Dieses Element enthält kein übergeordnetes Element im Schema. Dieses Element wird im SOAP-Header verwendet. Weitere Informationen zur Verwendung dieses Elements finden Sie in der WSDL-Datei.
  
## <a name="text-value"></a>Textwert

Für dieses Element ist ein Textwert erforderlich. Im Folgenden sind die möglichen Werte aufgeführt:
  
- CrossSite
    
- CrossForest
    
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

