---
title: DayOfMonth
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DayOfMonth
api_type:
- schema
ms.assetid: 09b7504e-08d8-42f9-88cc-a2a37a2e2b8b
description: Das DAYOFMONTH-Element beschreibt den Tag in einem Monat, an dem ein wiederkehrendes Element auftritt.
ms.openlocfilehash: dc333a46283d5e8eba3a79f62f8c22c22f56e190
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44442829"
---
# <a name="dayofmonth"></a>DayOfMonth

Das **DAYOFMONTH** -Element beschreibt den Tag in einem Monat, an dem ein wiederkehrendes Element auftritt. 
  
```xml
<DayOfMonth/>
```

**int**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[AbsoluteYearlyRecurrence](absoluteyearlyrecurrence.md) <br/> |Stellt ein jährliches Serienmuster dar.  <br/> |
|[AbsoluteMonthlyRecurrence](absolutemonthlyrecurrence.md) <br/> |Stellt ein monatliches Serienmuster dar.  <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert, der eine ganze Zahl im Bereich von 1 bis 31 darstellt, ist erforderlich. Wenn dieser Wert für einen bestimmten Monat größer ist als die Anzahl der Tage im Monat, wird der letzte Tag des Monats angenommen.
  
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

