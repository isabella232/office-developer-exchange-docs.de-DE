---
title: Überwachung
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- monitoring
api_type:
- schema
ms.assetid: 350d7b46-9260-41a7-8613-3cb8cc1b29a5
description: 'Letzte Änderung: September 17, 2015'
ms.openlocfilehash: 5614ac2c6428da9b6845769a9335486d3ded5754
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455828"
---
# <a name="monitoring"></a>Überwachung
  
**Gilt für:** Exchange Server 2013
  
Das **Monitoring** -Element enthält Konfigurationsinformationen, die definieren, wie und wann der Front-End-Transport-Dienst oder der Transportdienst Agents überwacht, die installiert sind. 
  
- [Konfiguration](configuration.md)  
- [mexRuntime](mexruntime.md)  
- [Überwachung](monitoring.md)
  
```XML
<monitoring>
   <agentExecution/>
   <messageSnapshot/>
</monitoring>
```

**monitoringtype (complexType)**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[agentExecution](agentexecution.md) <br/> |Definiert die Zeit (in Millisekunden) für den Client Zugriff oder den Postfachserver, um zu warten, bis ein Agent von einem Ereignis zurückkehrt, bevor er in das Ereignisprotokoll schreibt.  <br/> |
|[messageSnapshot](messagesnapshot.md) <br/> |Enthält ein Attribut, das angibt, ob das Feature für die Pipelineablaufverfolgung für den Client Zugriffs-oder den Postfachserver aktiviert ist.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[mexRuntime](mexruntime.md) <br/> |Enthält Elemente, die Konfigurationsinformationen für die Agent-Überwachung und Konfigurationsinformationen für die installierten SMTP-und Routing-Agents definieren.  <br/> |
   
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |In dieser Datei wird kein Namespace definiert.  <br/> |
|Name des Schemas  <br/> |Nicht verfügbar.  <br/> |
|Überprüfungsdatei  <br/> |Nicht verfügbar.  <br/> |
|Leer kann sein  <br/> |"False".  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Elemente der Konfigurationsdatei der Agents für Exchange 2013](agents-configuration-file-elements-for-exchange-2013.md)

