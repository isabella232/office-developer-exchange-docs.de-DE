---
title: RetentionAction
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 3bdf5955-1212-48a1-b3b5-743086866c91
description: Das RetentionAction-Element gibt die Aktion an, die für Elemente mit dem Aufbewahrungstag ausgeführt wird.
ms.openlocfilehash: ecea4326f0e50460635966991cd55badf8946993
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59517945"
---
# <a name="retentionaction"></a>RetentionAction

Das **RetentionAction-Element** gibt die Aktion an, die für Elemente mit dem Aufbewahrungstag ausgeführt wird. 
  
```XML
<RetentionAction> None | MoveToDeletedItems | MoveToFolder | DeleteAndAllowRecovery | PermanentlyDelete | MarkAsPastRetentionLimit | MoveToArchive <RetentionAction>
```

 **RetentionActionType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[RetentionPolicyTag](retentionpolicytag.md)
  
## <a name="text-value"></a>Textwert

Der Textwert des **RetentionAction-Elements** ist die Aktion, die für Elemente ausgeführt wird. Die folgende Liste enthält die Textwerte für das **RetentionAction-Element.** 
  
> **Keine** : Es wird keine Aktion für das Element ausgeführt. 
    
> **MoveToDeletedItems:** Das Element wird in den Standardordner "Gelöschte Elemente" verschoben. 
    
> **MoveToFolder** : Das Element wird in einen angegebenen Ordner verschoben. 
    
> **DeleteAndAllowRecovery** – Das Element wird gelöscht und in den Dumpster eingefügt. 
    
> **PermanentlyDelete** : Das Element wird dauerhaft aus dem Postfach gelöscht. 
    
> **MarkAsPastRetentionLimit** : Das Element wird als das Aufbewahrungszeitlimit überschritten markiert. 
    
> **MoveToArchive** – Das Element wird in das Archivpostfach verschoben. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> ||
   

