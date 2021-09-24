---
title: agentList
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- agentList
api_type:
- schema
ms.assetid: e877b7ef-e303-4270-964d-8d116ff2a865
description: 'Last modified: September 17, 2015'
ms.openlocfilehash: eadae2a22e4c844f1f2edce9211100bb9ef2776d
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59529356"
---
# <a name="agentlist"></a>agentList
  
**Gilt für:** Exchange Server 2013
  
Das **agentList-Element** enthält ein [Agent-Element](agent.md) für jeden installierten Agent. 
  
- [Konfiguration](configuration.md)
- [mexRuntime](mexruntime.md)
- [agentList](agentlist.md)
  
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
|[mexRuntime](mexruntime.md) <br/> |Enthält Elemente, die Konfigurationsinformationen für die Agentüberwachung und Konfigurationsinformationen zu installierten Agents definieren.  <br/> |
   
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |Diese Datei definiert keinen Namespace.  <br/> |
|Name des Schemas  <br/> |Nicht verfügbar.  <br/> |
|Überprüfungsdatei  <br/> |Nicht verfügbar.  <br/> |
|Leer kann sein  <br/> |"False".  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Agents-Konfigurationsdateielemente für Exchange 2013](agents-configuration-file-elements-for-exchange-2013.md)

