---
title: RequestType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RequestType
api_type:
- schema
ms.assetid: 4e657e57-528f-4250-a99c-f9850bbbcec5
description: Das RequestType-Element angibt, ob eine Proxyanforderung einer Cross-Site oder einer gesamtstrukturübergreifenden Anforderung ist.
ms.openlocfilehash: 96a4d57432b15aa54fff2618df458fc75cb227f3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831139"
---
# <a name="requesttype"></a>RequestType

Das **RequestType** -Element angibt, ob eine Proxyanforderung einer Cross-Site oder einer gesamtstrukturübergreifenden Anforderung ist. 
  
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

Dieses Element muss ein übergeordnetes Element nicht im Schema. Dieses Element wird in den SOAP-Header verwendet. Weitere Informationen zur Verwendung dieses Elements finden Sie unter der WSDL-Datei.
  
## <a name="text-value"></a>Textwert

Es wird ein Textwert für dieses Element erforderlich. Im Folgenden sind die möglichen Werte aufgeführt:
  
- CrossSite
    
- CrossForest
    
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

