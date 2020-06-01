---
title: Konfiguration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- configuration
api_type:
- schema
ms.assetid: 6fc04e4d-657a-4999-9431-186ccb7832b5
description: 'Letzte Änderung: September 17, 2015'
ms.openlocfilehash: b886851b9a0c17d58428f49281d664930d0e4070
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461562"
---
# <a name="configuration"></a>Konfiguration
  
**Gilt für:** Exchange Server 2013
  
Das **Configuration** -Element ist das Stammelement für die Konfigurationsdatei der Agents. 
  
- [Konfiguration](configuration.md) 
- [mexRuntime](mexruntime.md)
  
```XML
<configuration>
      <mexRuntime/>
</configuration>
```

**ConfigurationType (complexType)**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[mexRuntime](mexruntime.md) <br/> |Enthält Elemente, die Konfigurationsinformationen für die Agent-Überwachung und Konfigurationsinformationen für die installierten SMTP-und Routing-Agents definieren.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |In dieser Datei wird kein Namespace definiert.  <br/> |
|Name des Schemas  <br/> |Nicht verfügbar.  <br/> |
|Überprüfungsdatei  <br/> |Nicht verfügbar.  <br/> |
|Leer kann sein  <br/> |"False".  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Elemente der Konfigurationsdatei der Agents für Exchange 2013](agents-configuration-file-elements-for-exchange-2013.md)

