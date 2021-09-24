---
title: Zeitraum
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Period
api_type:
- schema
ms.assetid: 2f9cf6af-c531-4d7d-90c9-1a1db504d890
description: Das Period-Element definiert den Namen, den Zeitversatz und den eindeutigen Bezeichner für eine bestimmte Phase der Zeitzone.
ms.openlocfilehash: 7fa5bca6547f4e3120c60c2e2b69139f7bb12e93
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59534735"
---
# <a name="period"></a>Zeitraum

Das **Period-Element** definiert den Namen, den Zeitversatz und den eindeutigen Bezeichner für eine bestimmte Phase der Zeitzone. 
  
```xml
<Period Bias="" Name="" Id=""/>
```

 **PeriodType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|Bias  <br/> |Ein xs:duration-Wert, der den Zeitoffset von koordinierter Weltzeit (COORDINATED Universal Time, UTC) für den Zeitraum darstellt.  <br/> |
|Name  <br/> |Ein Zeichenfolgenwert, der den beschreibenden Namen des Punkts darstellt.  <br/> |
|Id  <br/> |Ein Zeichenfolgenwert, der den Bezeichner für den Punkt darstellt.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Zeiten](periods.md) <br/> |Stellt ein Array von Zeiträumen dar, die den Zeitversatz in verschiedenen Phasen der Zeitzone definieren.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

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

