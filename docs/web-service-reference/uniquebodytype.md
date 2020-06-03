---
title: UniqueBodyType
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8f7276aa-e354-40e4-b9cb-950fad46ac93
description: Das UniqueBodyType-Element gibt an, ob der eindeutige Text im Text-oder HTML-Format zurückgegeben wird.
ms.openlocfilehash: 7e6c4631ef589555ce4d5da747c200ffe956f3a1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459440"
---
# <a name="uniquebodytype"></a>UniqueBodyType

Das **UniqueBodyType** -Element gibt an, ob der eindeutige Text im Text-oder HTML-Format zurückgegeben wird. 
  
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

Der Textwert des **UniqueBodyType** -Elements gibt an, in welchem Format der eindeutige Textkörper zurückgegeben wird. In der folgenden Tabelle sind die möglichen Werte für dieses Element aufgeführt. 
  
****

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Optimal  <br/> |Die Antwort gibt den reichsten verfügbaren Inhalt des Textkörpers zurück. Dies ist hilfreich, wenn unbekannt ist, ob es sich bei dem Inhalt um Text oder HTML handelt.  <br/> Der zurückgegebene Text ist Text, wenn der gespeicherte Text nur-Text ist. Andernfalls gibt die Antwort HTML zurück, wenn der gespeicherte Text im HTML-oder RTF-Format vorliegt.  <br/> Dies ist der Standardwert.  <br/> |
|HTML  <br/> |Die Antwort gibt einen eindeutigen Text im HTML-Format zurück.  <br/> |
|Text  <br/> |Die Antwort gibt einen eindeutigen Text im Klartext zurück.  <br/> |
   
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



[ItemShape](itemshape.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

