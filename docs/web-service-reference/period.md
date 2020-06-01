---
title: Punkt
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Period
api_type:
- schema
ms.assetid: 2f9cf6af-c531-4d7d-90c9-1a1db504d890
description: Das period-Element definiert den Namen, den Zeit Offset und den eindeutigen Bezeichner für eine bestimmte Phase der Zeitzone.
ms.openlocfilehash: a7c36a9de01fd0484a7df75de3b5525992ef7ee7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459721"
---
# <a name="period"></a>Punkt

Das **Period** -Element definiert den Namen, den Zeit Offset und den eindeutigen Bezeichner für eine bestimmte Phase der Zeitzone. 
  
```xml
<Period Bias="" Name="" Id=""/>
```

 **Periodtype**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|Bias  <br/> |Ein xs: Duration-Wert, der den Zeit Offset der koordinierten Weltzeit (Coordinated Universal Time, UTC) für den Zeitraum darstellt.  <br/> |
|Name  <br/> |Ein String-Wert, der den beschreibenden Namen des Zeitraums darstellt.  <br/> |
|Id  <br/> |Ein String-Wert, der den Bezeichner für den Zeitraum darstellt.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Zeiten](periods.md) <br/> |Stellt ein Array von Punkten dar, die den Zeit Offset in unterschiedlichen Phasen der Zeitzone definieren.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
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

