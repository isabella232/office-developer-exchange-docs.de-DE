---
title: DayOfMonth
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- DayOfMonth
api_type:
- schema
ms.assetid: 09b7504e-08d8-42f9-88cc-a2a37a2e2b8b
description: Das DayOfMonth-Element beschreibt den Tag in einem Monat, an dem ein wiederkehrendes Element auftritt.
ms.openlocfilehash: 73b83b83a6d9522f4a92f8a845bee788fb8dee33
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513002"
---
# <a name="dayofmonth"></a>DayOfMonth

Das **DayOfMonth-Element** beschreibt den Tag in einem Monat, an dem ein wiederkehrendes Element auftritt. 
  
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

Ein Textwert, der eine ganze Zahl im Bereich von 1 bis 31 darstellt, ist erforderlich. Wenn dieser Wert für einen bestimmten Monat größer als die Anzahl der Tage im Monat ist, wird der letzte Tag des Monats angenommen.
  
## <a name="remarks"></a>HinwBemerkungeneise

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

