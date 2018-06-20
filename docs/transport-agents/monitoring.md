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
description: 'Zuletzt geändert: 17 September 2015'
ms.openlocfilehash: 1b5484467def0bf3d22ba0707357977d5ed461ff
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757197"
---
# <a name="monitoring"></a>Überwachung
  
**Gilt für:** Exchange Server 2013
  
Das **monitoring** -Element enthält Konfigurationsinformationen, die definiert, wie und wann die Front-End-Transport-Dienst oder den Transportdienst Agents überwacht, die installiert werden. 
  
- [Konfiguration](configuration.md)  
- [mexRuntime](mexruntime.md)  
- [Überwachung](monitoring.md)
  
```XML
<monitoring>
   <agentExecution/>
   <messageSnapshot/>
</monitoring>
```

**MonitoringType (ComplexType)**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[agentExecution](agentexecution.md) <br/> |Definiert die Zeit in Millisekunden an, für den Clientzugriff oder dem Postfachserver zu warten, bis ein Agent zurückgeben, ein Ereignis, bevor in das Ereignisprotokoll geschrieben.  <br/> |
|[messageSnapshot](messagesnapshot.md) <br/> |Enthält ein Attribut, das angibt, ob das Pipeline Tracing-Feature für den Clientzugriff oder dem Postfachserver aktiviert ist.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[mexRuntime](mexruntime.md) <br/> |Enthält Elemente, die definieren, Konfigurationsinformationen für die Überwachung durch den Agenten und Konfigurationsinformationen für SMTP und routing-Agents, die installiert werden.  <br/> |
   
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |Diese Datei ist nicht auf einen Namespace definieren.  <br/> |
|Name des Schemas  <br/> |Nicht verfügbar.  <br/> |
|Überprüfungsdatei  <br/> |Nicht verfügbar.  <br/> |
|Leer kann sein  <br/> |Falsch.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Agents Datei Konfigurationselemente für Exchange 2013](agents-configuration-file-elements-for-exchange-2013.md)

