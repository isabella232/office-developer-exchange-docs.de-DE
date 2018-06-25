---
title: mexRuntime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- mexRuntime
api_type:
- schema
ms.assetid: eabb2f12-10a7-4ce2-ae4b-9c04010c765f
description: 'Zuletzt geändert: 17 September 2015'
ms.openlocfilehash: 4a34eedfc16d64cbfa67003ed23cf6eba2bb4bad
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757201"
---
# <a name="mexruntime"></a>mexRuntime
  
**Gilt für:** Exchange Server 2013
  
Das **MexRuntime** -Element enthält Elemente, die definieren, Konfigurationsinformationen für die Überwachung durch den Agenten und Konfigurationsinformationen für SMTP und routing-Agents, die installiert werden. 
  
- [Konfiguration](configuration.md)  
- [mexRuntime](mexruntime.md)
  
```XML
<mexRuntime>
   <monitoring/>
   <agentList/>
</mexRuntime>
```

**MexRuntimeType (ComplexType)**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Überwachung](monitoring.md) <br/> |Enthält Konfigurationsinformationen, die definiert, wie und wann mit Transport Agents überwacht wird, die installiert werden.  <br/> |
|[agentList](agentlist.md) <br/> |Enthält ein [Agent](agent.md) -Element für jeden Agent, installiert ist.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Konfiguration](configuration.md) <br/> |Das Stammelement für die Konfigurationsdatei Agents.  <br/> |
   
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |Diese Datei ist nicht auf einen Namespace definieren.  <br/> |
|Name des Schemas  <br/> |Nicht verfügbar.  <br/> |
|Überprüfungsdatei  <br/> |Nicht verfügbar.  <br/> |
|Leer kann sein  <br/> |Falsch.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Agents Datei Konfigurationselemente für Exchange 2013](agents-configuration-file-elements-for-exchange-2013.md)

