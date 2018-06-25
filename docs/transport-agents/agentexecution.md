---
title: agentExecution
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- agentExecution
api_type:
- schema
ms.assetid: 600c4690-941c-45af-a906-5528748d09cd
description: 'Zuletzt geändert: 17 September 2015'
ms.openlocfilehash: 5848d52a68c8c3f747614015e49becb34bc4cfd8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757167"
---
# <a name="agentexecution"></a>agentExecution
  
**Gilt für:** Exchange Server 2013 
  
Das **AgentExecution** -Element definiert die Zeit in Millisekunden an, für den Clientzugriff "oder" Postfach-Server zu warten, bis ein Agent zurückgeben, ein Ereignis, bevor in das Ereignisprotokoll geschrieben. 
  
- [Konfiguration](configuration.md)  
- [Überwachung](monitoring.md)
- [agentExecution](agentexecution.md)
  
```XML
<agentExecution timeLimitInMilliseconds="" />
```

**AgentExecutionType (ComplexType)**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**timeLimitInMilliseconds** <br/> |Eine positive ganze Zahl, die gibt die Zeit in Millisekunden an, für den Server zu warten, bis ein Agent zurückgeben, ein Ereignis, bevor eine Warnung in das Ereignisprotokoll geschrieben. Wenn dieser Wert zu klein ist, kann die Leistung verringern. Der vorgeschlagene Wert für dieses Attribut ist 300.000, die auf 5 Minuten entspricht.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Überwachung](monitoring.md) <br/> |Enthält Konfigurationsinformationen, die definiert, wann und wie der Front-End-Transport-Dienst oder den Transportdienst Agents überwacht, die installiert werden.  <br/> |
   
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |Diese Datei ist nicht auf einen Namespace definieren.  <br/> |
|Name des Schemas  <br/> |Nicht verfügbar.  <br/> |
|Überprüfungsdatei  <br/> |Nicht verfügbar.  <br/> |
|Leer kann sein  <br/> |Falsch.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Agents Datei Konfigurationselemente für Exchange 2013](agents-configuration-file-elements-for-exchange-2013.md)

