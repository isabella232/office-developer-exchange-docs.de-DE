---
title: Monat (Zeitzonenübergang)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Month
api_type:
- schema
ms.assetid: 5e6aac75-366d-43d0-8ccb-956285474662
description: Das Month-Element stellt den Monat dar, in dem der Zeitzonenübergang erfolgt.
ms.openlocfilehash: 36cf19dc8bf0953e8b198d2626bdfda4febbbb95
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520409"
---
# <a name="month-time-zone-transition"></a>Monat (Zeitzonenübergang)

Das **Month-Element** stellt den Monat dar, in dem der Zeitzonenübergang erfolgt. 
  
```xml
<Month/>
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
|[RecurringDateTransition](recurringdatetransition.md) <br/> |Stellt einen Zeitzonenübergang dar, der jedes Jahr an einem bestimmten Datum stattfindet.  <br/> |
|[RecurringDayTransition](recurringdaytransition.md) <br/> |Stellt einen Zeitzonenübergang dar, der jedes Jahr am selben Tag erfolgt.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert ist eine ganze Zahl, die den Monat darstellt, in dem der Zeitzonenübergang erfolgt.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server ausgeführt wird, auf dem die Clientzugriffsserverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

