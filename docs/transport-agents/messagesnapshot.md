---
title: messageSnapshot
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- messageSnapshot
api_type:
- schema
ms.assetid: f157e44c-b950-463f-b086-31d5da94b7ff
description: 'Last modified: September 17, 2015'
ms.openlocfilehash: 2ac38dd3f50b5d9d070262f3daffb72b02df5d82
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59525456"
---
# <a name="messagesnapshot"></a>messageSnapshot

**Gilt für:** Exchange Server 2013
  
Das **messageSnapshot-Element** enthält ein Attribut, das angibt, ob das Pipelineablaufverfolgungsfeature für den Exchange Server aktiviert ist, auf dem der Clientzugriff oder die Postfachserverrolle installiert ist. 
  
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
|**enabled** <br/> |Ein boolescher Wert, der angibt, ob das Pipelineablaufverfolgungsfeature für den Clientzugriff oder den Postfachserver aktiviert ist. Der Wert ist **"true",** wenn die Pipelineablaufverfolgung aktiviert ist. andernfalls ist der Wert **"false"** oder das Element nicht vorhanden.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Überwachung](monitoring.md) <br/> |Enthält Konfigurationsinformationen, die definieren, wie und wann der Transportdienst die installierten Agents überwacht.  <br/> |
   
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |Diese Datei definiert keinen Namespace.  <br/> |
|Name des Schemas  <br/> |Nicht verfügbar.  <br/> |
|Überprüfungsdatei  <br/> |Nicht verfügbar.  <br/> |
|Leer kann sein  <br/> |"False".  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Agents-Konfigurationsdateielemente für Exchange 2013](agents-configuration-file-elements-for-exchange-2013.md)

