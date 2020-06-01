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
description: 'Letzte Änderung: September 17, 2015'
ms.openlocfilehash: 457257e59fb37659daf2f91b0fa5dfced5c48c03
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44446490"
---
# <a name="agentexecution"></a>agentExecution
  
**Gilt für:** Exchange Server 2013 
  
Das **agentExecution** -Element definiert die Zeit (in Millisekunden), die der Client Zugriffs-oder Postfachserver wartet, bis ein Agent von einem Ereignis zurückkehrt, bevor er in das Ereignisprotokoll schreibt. 
  
- [Konfiguration](configuration.md)  
- [Überwachung](monitoring.md)
- [agentExecution](agentexecution.md)
  
```XML
<agentExecution timeLimitInMilliseconds="" />
```

**agentExecutionType (complexType)**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**timeLimitInMilliseconds** <br/> |Ein positiver ganzzahliger Wert, der die Zeit in Millisekunden angibt, die der Server wartet, bis ein Agent von einem Ereignis zurückgegeben wird, bevor er eine Warnung in das Ereignisprotokoll schreibt. Die Leistung kann sinken, wenn dieser Wert zu klein ist. Der vorgeschlagene Wert für dieses Attribut ist 300.000, was 5 Minuten entspricht.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Überwachung](monitoring.md) <br/> |Enthält Konfigurationsinformationen, die definieren, wie und wann der Front-End-Transport-Dienst oder der Transportdienst Agents überwacht, die installiert sind.  <br/> |
   
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |In dieser Datei wird kein Namespace definiert.  <br/> |
|Name des Schemas  <br/> |Nicht verfügbar.  <br/> |
|Überprüfungsdatei  <br/> |Nicht verfügbar.  <br/> |
|Leer kann sein  <br/> |"False".  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Elemente der Konfigurationsdatei der Agents für Exchange 2013](agents-configuration-file-elements-for-exchange-2013.md)

