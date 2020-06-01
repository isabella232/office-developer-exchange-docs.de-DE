---
title: messageSnapshot
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- messageSnapshot
api_type:
- schema
ms.assetid: f157e44c-b950-463f-b086-31d5da94b7ff
description: 'Letzte Änderung: September 17, 2015'
ms.openlocfilehash: 8a58444580c803efb7312df95d75d697bc42e8e0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461842"
---
# <a name="messagesnapshot"></a>messageSnapshot

**Gilt für:** Exchange Server 2013
  
Das **messageSnapshot** -Element enthält ein Attribut, das angibt, ob das Feature für die Pipelineablaufverfolgung für den Exchange-Server aktiviert ist, auf dem die Client Zugriffs-oder Postfachserverrolle installiert ist. 
  
- [Konfiguration](configuration.md)  
- [mexRuntime](mexruntime.md) 
- [Überwachung](monitoring.md) 
- [messageSnapshot](messagesnapshot.md)
  
```XML
<messageSnapshot enabled="" />
```

**messageSnapshotType (Boolean)**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**enabled** <br/> |Ein boolescher Wert, der angibt, ob das Feature für die Pipelineablaufverfolgung für den Client Zugriff oder den Postfachserver aktiviert ist. Der Wert ist **true** , wenn die Pipelineablaufverfolgung aktiviert ist; Andernfalls ist der Wert **false** , oder das Element ist nicht vorhanden.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Überwachung](monitoring.md) <br/> |Enthält Konfigurationsinformationen, die definieren, wie und wann der Transportdienst Agents überwacht, die installiert sind.  <br/> |
   
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |In dieser Datei wird kein Namespace definiert.  <br/> |
|Name des Schemas  <br/> |Nicht verfügbar.  <br/> |
|Überprüfungsdatei  <br/> |Nicht verfügbar.  <br/> |
|Leer kann sein  <br/> |"False".  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Elemente der Konfigurationsdatei der Agents für Exchange 2013](agents-configuration-file-elements-for-exchange-2013.md)

