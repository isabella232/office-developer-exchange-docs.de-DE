---
title: RetentionAction
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3bdf5955-1212-48a1-b3b5-743086866c91
description: Das Retention Action-Element gibt die Aktion an, die für Elemente mit dem Aufbewahrungs Tag ausgeführt wird.
ms.openlocfilehash: c16988413e732ddc3cd6ebc355cb73c4d96550c7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465233"
---
# <a name="retentionaction"></a>RetentionAction

Das **Retention** Action-Element gibt die Aktion an, die für Elemente mit dem Aufbewahrungs Tag ausgeführt wird. 
  
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

Der Textwert des Elements **Retention** Action ist die für Elemente ausgeführte Aktion. Die folgende Liste enthält die Textwerte für das **Retention** -Element. 
  
> **None** : für das Element wird keine Aktion ausgeführt. 
    
> **MoveToDeletedItems** – das Element wird in den Standardordner "Gelöschte Elemente" verschoben. 
    
> **MoveToFolder** – das Element wird in einen angegebenen Ordner verschoben. 
    
> **DeleteAndAllowRecovery mit** – das Element wird gelöscht und in den Papierkorb verschoben. 
    
> **PermanentlyDelete** – das Element wird endgültig aus dem Postfach gelöscht. 
    
> **MarkAsPastRetentionLimit** – das Element wird als das Beibehaltungs Zeitlimit überschritten markiert. 
    
> **MoveToArchive mit** – das Element wird in das Archivpostfach verschoben. 
    
## <a name="remarks"></a>Bemerkungen

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> ||
   

