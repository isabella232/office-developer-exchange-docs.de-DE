---
title: NormalizedBodyType
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c6973aee-ec7b-44c1-b328-f2204d9de5d1
description: Das NormalizedBodyType-Element gibt an, ob die normalisierte Body Text oder HTML-Format zurückgegeben wird.
ms.openlocfilehash: 33575594b22f972a9eb762dfac884fa91459f04a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830554"
---
# <a name="normalizedbodytype"></a>NormalizedBodyType

Das **NormalizedBodyType** -Element gibt an, ob die normalisierte Body Text oder HTML-Format zurückgegeben wird. 
  
```XML
<NormalizedBodyType> Best | HTML | Text </NormalizedBodyType>
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

Der Textwert des **NormalizedBodyType** -Elements gibt an, dass den normalisierten Textkörper Format zurückgegeben wird. Die folgende Tabelle enthält die möglichen Werte für dieses Element. 
  
****

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Am besten  <br/> |Die Antwort wird den inhaltlich verfügbaren Inhalt des Textkörpers zurückzugeben. Dies ist nützlich, wenn nicht bekannt ist, ob der Inhalt Text "oder" HTML ist.  <br/> Der zurückgegebene Text ist Text wird, wenn der gespeicherte Text nur-Text. Andernfalls gibt die Antwort HTML zurück, wenn der gespeicherte Textkörper in HTML oder RTF-Format ist.  <br/> Dies ist der Standardwert.  <br/> |
|HTML  <br/> |Die Antwort wird eine normalisierte Stelle im HTML-Format zurück.  <br/> |
|Text  <br/> |Die Antwort wird ein normalisierte Body als nur-Text zurück.  <br/> |
   
## <a name="remarks"></a>Hinweise

Dieses Element wurde in Exchange Server 2013 Service Pack 1 (SP1) eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch



[ItemShape](itemshape.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

