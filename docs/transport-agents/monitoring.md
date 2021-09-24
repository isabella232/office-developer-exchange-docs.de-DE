---
title: Überwachen
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- monitoring
api_type:
- schema
ms.assetid: 350d7b46-9260-41a7-8613-3cb8cc1b29a5
description: 'Last modified: September 17, 2015'
ms.openlocfilehash: 215737fb43e1dbef9b7dd11baea1d3f922df7d34
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59540366"
---
# <a name="monitoring"></a>Überwachen
  
**Gilt für:** Exchange Server 2013
  
Das **Überwachungselement** enthält Konfigurationsinformationen, die definieren, wie und wann der Front-End-Transportdienst oder der Transportdienst die installierten Agents überwacht. 
  
- [Konfiguration](configuration.md)  
- [mexRuntime](mexruntime.md)  
- [Überwachung](monitoring.md)
  
```XML
<monitoring>
   <agentExecution/>
   <messageSnapshot/>
</monitoring>
```

**monitoringType (complexType)**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[agentExecution](agentexecution.md) <br/> |Definiert die Zeit in Millisekunden, bis der Clientzugriff oder der Postfachserver wartet, bis ein Agent von einem Ereignis zurückkehrt, bevor er in das Ereignisprotokoll schreibt.  <br/> |
|[messageSnapshot](messagesnapshot.md) <br/> |Enthält ein Attribut, das angibt, ob das Pipelineablaufverfolgungsfeature für den Clientzugriff oder den Postfachserver aktiviert ist.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[mexRuntime](mexruntime.md) <br/> |Enthält Elemente, die Konfigurationsinformationen für die Agentüberwachung und Konfigurationsinformationen für installierte SMTP- und Routing-Agents definieren.  <br/> |
   
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |Diese Datei definiert keinen Namespace.  <br/> |
|Name des Schemas  <br/> |Nicht verfügbar.  <br/> |
|Überprüfungsdatei  <br/> |Nicht verfügbar.  <br/> |
|Leer kann sein  <br/> |"False".  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Agents-Konfigurationsdateielemente für Exchange 2013](agents-configuration-file-elements-for-exchange-2013.md)

