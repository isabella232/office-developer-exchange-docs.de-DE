---
title: UniqueBodyType
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 8f7276aa-e354-40e4-b9cb-950fad46ac93
description: Das UniqueBodyType-Element gibt an, ob der eindeutige Textkörper im Text- oder HTML-Format zurückgegeben wird.
ms.openlocfilehash: a0149e41da24646fdf38a465434bfad3557ece22
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520269"
---
# <a name="uniquebodytype"></a>UniqueBodyType

Das **UniqueBodyType-Element** gibt an, ob der eindeutige Textkörper im Text- oder HTML-Format zurückgegeben wird. 
  
```XML
<UniqueBodyType> Best | HTML | Text </UniqueBodyType>
```

 **BodyTypeResponseType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[ItemShape](itemshape.md)
  
## <a name="text-value"></a>Textwert

Der Textwert des **UniqueBodyType-Elements** gibt das Format an, in dem der eindeutige Textkörper zurückgegeben wird. In der folgenden Tabelle sind die möglichen Werte für dieses Element aufgeführt. 
  
****

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Optimal  <br/> |Die Antwort gibt den umfangreichsten verfügbaren Inhalt des Textkörpers zurück. Dies ist nützlich, wenn nicht bekannt ist, ob es sich bei dem Inhalt um Text oder HTML handelt.  <br/> Der zurückgegebene Textkörper ist Text, wenn der gespeicherte Text nur Text ist. Andernfalls gibt die Antwort HTML zurück, wenn der gespeicherte Textkörper im HTML- oder RTF-Format vorliegt.  <br/> Dies ist der Standardwert.  <br/> |
|HTML  <br/> |Die Antwort gibt einen eindeutigen Textkörper als HTML zurück.  <br/> |
|Text  <br/> |Die Antwort gibt einen eindeutigen Textkörper als Nur-Text zurück.  <br/> |
   
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



[ItemShape](itemshape.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

