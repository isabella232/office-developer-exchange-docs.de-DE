---
title: RetentionAction
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3bdf5955-1212-48a1-b3b5-743086866c91
description: Das Element RetentionAction gibt die Aktion für Elemente mit dem Aufbewahrungsrichtlinien-Tag an.
ms.openlocfilehash: 54a1038f2e56aad66f89522423ccfbd69dc44a80
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831215"
---
# <a name="retentionaction"></a>RetentionAction

Das Element **RetentionAction** gibt die Aktion für Elemente mit dem Aufbewahrungsrichtlinien-Tag an. 
  
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

Der Textwert des **RetentionAction** -Elements ist die Aktion für Elemente. Die folgende Liste enthält die Textwerte für das **RetentionAction** -Element. 
  
> **Keine** - keine Aktion wird für das Element ausgeführt. 
    
> **MoveToDeletedItems** - das Element wird in den Standardordner für gelöschte Objekte verschoben. 
    
> **MoveToFolder** - das Element wird in einem angegebenen Ordner verschoben. 
    
> **DeleteAndAllowRecovery** - das Element wird gelöscht und in die Dumpster platzieren. 
    
> **PermanentlyDelete** - das Element wird dauerhaft aus dem Postfach gelöscht. 
    
> **MarkAsPastRetentionLimit** - Elements wird als wurde das Zeitlimit für die Aufbewahrung überschritten gekennzeichnet. 
    
> **MoveToArchive** - das Element wird in das Archivpostfach verschoben. 
    
## <a name="remarks"></a>Hinweise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> ||
   

