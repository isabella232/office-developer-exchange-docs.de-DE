---
title: Zweck
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- To
api_type:
- schema
ms.assetid: d14e46da-14bd-4a33-a78e-8ee314d9c1d8
description: To-Element gibt das Ziel des Übergangs Zeitzone. Das Ziel ist eine Zeitzone Zeitraum oder eine Gruppe von Zeitzone Übergänge.
ms.openlocfilehash: dc7df8ed3ddd6a9b4222ffab4c2b47b00ee4ba0c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839218"
---
# <a name="to"></a>Zweck

**To** -Element gibt das Ziel des Übergangs Zeitzone. Das Ziel ist eine Zeitzone Zeitraum oder eine Gruppe von Zeitzone Übergänge. 
  
```xml
<To Kind=""/>
```

 **TransitionTargetType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|Art  <br/> |Gibt an, ob das Ziel des Vorgangs Übergang Zeitzone eine Zeitzone läuft oder einer Gruppe von Zeitzone Übergänge.  <br/> |
   
#### <a name="kind-attribute-values"></a>Kind Attributwerte

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Punkt  <br/> |Gibt an, dass die Zeitzone Übergang als Ziel eines Zeitraums Zeitzone fungiert.  <br/> |
|Gruppe  <br/> |Gibt an, dass die Zeitzone Übergang als Ziel einer Gruppe von Zeitzone Übergänge fungiert.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[AbsoluteDateTransition](absolutedatetransition.md) <br/> |Stellt einen Zeitzone Übergang, die einem bestimmten Datum und zu einem bestimmten Zeitpunkt dar.  <br/> |
|[RecurringDayTransition](recurringdaytransition.md) <br/> |Stellt einen Zeitzone Übergang dar, bei dem gleichen Tag pro Jahr auftritt.  <br/> |
|[RecurringDateTransition](recurringdatetransition.md) <br/> |Stellt einen Zeitzone Übergang, der auftritt, an einem angegebenen Tag des Jahres dar.  <br/> |
|[Übergang](transition.md) <br/> |Stellt einen Zeitzone Übergang dar.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert ist eine Zeichenfolge, die gibt die eindeutige ID des [Zeitraums](period.md) oder [TransitionsGroup](transitionsgroup.md) , das das Ziel des Übergangs Zeitzone ist. 
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

