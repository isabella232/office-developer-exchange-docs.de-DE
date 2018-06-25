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
description: 'Zuletzt geändert: 17 September 2015'
ms.openlocfilehash: 4b814def8eef8fb452d2e754c5f6787d644055f7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757198"
---
# <a name="messagesnapshot"></a>messageSnapshot

**Gilt für:** Exchange Server 2013
  
Das **MessageSnapshot** -Element enthält ein Attribut, das angibt, ob das Pipeline Tracing-Feature für den Exchange-Server aktiviert ist, die Access-Client oder die Serverrolle Mailbox installiert hat. 
  
- [Konfiguration](configuration.md)  
- [mexRuntime](mexruntime.md) 
- [Überwachung](monitoring.md) 
- [messageSnapshot](messagesnapshot.md)
  
```XML
<messageSnapshot enabled="" />
```

**MessageSnapshotType (boolesch)**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**aktiviert** <br/> |Ein boolescher Wert, der angibt, ob das Pipeline Tracing-Feature für den Clientzugriff oder dem Postfachserver aktiviert ist. Der Wert ist **true** , wenn die pipelineablaufverfolgung aktiviert ist. Andernfalls ist des Werts **false** oder das Element ist nicht vorhanden.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Überwachung](monitoring.md) <br/> |Enthält Konfigurationsinformationen, die definiert, wie und wann Transportdienst mit Agents überwacht, die installiert werden.  <br/> |
   
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |Diese Datei ist nicht auf einen Namespace definieren.  <br/> |
|Name des Schemas  <br/> |Nicht verfügbar.  <br/> |
|Überprüfungsdatei  <br/> |Nicht verfügbar.  <br/> |
|Leer kann sein  <br/> |Falsch.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Agents Datei Konfigurationselemente für Exchange 2013](agents-configuration-file-elements-for-exchange-2013.md)

