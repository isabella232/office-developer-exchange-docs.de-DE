---
title: Agentliste
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- agentList
api_type:
- schema
ms.assetid: e877b7ef-e303-4270-964d-8d116ff2a865
description: 'Letzte Änderung: September 17, 2015'
ms.openlocfilehash: 99e4e24c3bca77c7e7d5f2c59bb21cee1317fed2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44446392"
---
# <a name="agentlist"></a>Agentliste
  
**Gilt für:** Exchange Server 2013
  
Das **agentlist** -Element enthält ein [Agent](agent.md) -Element für jeden installierten Agent. 
  
- [Konfiguration](configuration.md)
- [mexRuntime](mexruntime.md)
- [Agentliste](agentlist.md)
  
```XML
<agentList>
      <agent/>
</agentList>
```

**agentListType (complexType)**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Agent](agent.md) <br/> |Enthält Konfigurationsinformationen zu einem installierten Agent.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[mexRuntime](mexruntime.md) <br/> |Enthält Elemente, die Konfigurationsinformationen für die Agent-Überwachung und Konfigurationsinformationen zu installierten Agents definieren.  <br/> |
   
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |In dieser Datei wird kein Namespace definiert.  <br/> |
|Name des Schemas  <br/> |Nicht verfügbar.  <br/> |
|Überprüfungsdatei  <br/> |Nicht verfügbar.  <br/> |
|Leer kann sein  <br/> |"False".  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Elemente der Konfigurationsdatei der Agents für Exchange 2013](agents-configuration-file-elements-for-exchange-2013.md)

