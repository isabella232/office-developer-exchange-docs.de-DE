---
title: Ismoderiert
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsModerated
api_type:
- schema
ms.assetid: a7562256-feb9-41a1-857e-b5d41cbed680
description: Das ismoded-Element gibt an, ob das Postfach des Empfängers moderiert wird.
ms.openlocfilehash: 930d5a7e09712f35d22850a93462d051a34785a1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44435485"
---
# <a name="ismoderated"></a>Ismoderiert

Das **ismoded** -Element gibt an, ob das Postfach des Empfängers moderiert wird. 
  
```XML
<IsModerated>true | false</IsModerated>
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
|[E-Mail-Info](mailtips.md) <br/> |Stellt Werte für verschiedene Arten von e-Mail-Tipps dar.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert für dieses Element ist **true** , wenn das Postfach des Empfängers moderiert wird. Der Wert ist **false** , wenn das Postfach des Empfängers nicht moderiert wird. 
  
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

