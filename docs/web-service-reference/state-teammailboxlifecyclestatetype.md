---
title: Status (TeamMailboxLifecycleStateType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3b1bc531-6988-41c3-9aad-3f5ad5b732a9
description: Das Status-Element enthält den Lebenszyklusstatus, der für ein websitepostfach festgelegt ist.
ms.openlocfilehash: accd70d36cc34e7364387b98a2e94c56b91f012f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831571"
---
# <a name="state-teammailboxlifecyclestatetype"></a>Status (TeamMailboxLifecycleStateType)

Das **Status** -Element enthält den Lebenszyklusstatus, der für ein websitepostfach festgelegt ist. 
  
```XML
<State> Active | Closed | Unlinked | PendingDelete </State>
```

**TeamMailboxLifecycleStateType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[SetTeamMailbox](setteammailbox.md)
  
## <a name="text-value"></a>Textwert

Der Textwert der **State** -Elements ist die Lebenszyklusstatus, der für ein websitepostfach festgelegt ist. Ein Textwert der **aktiven** gibt an, dass ein websitepostfach verwendet wird. Der Textwert **geschlossen** gibt an, dass ein websitepostfach geschlossen wurde und nicht aktiv verwendet. Ein Textwert der **Unverknüpfte** gibt an, dass ein websitepostfach nicht mit einer Umgebung webbasierte Zusammenarbeit verknüpft ist. Die Werte **aktiv**, **geschlossen**und **PendingDelete** schließen sich gegenseitig aus, aber der Wert **Unverknüpfte** schließen sich nicht gegenseitig aus anderen Werte. Der Textwert **PendingDelete** gibt an, dass ein websitepostfach Löschen ausstehend ist. Ein websitepostfach muss geschlossen werden, bevor es als **PendingDelete**festgelegt werden kann.
  
## <a name="remarks"></a>Hinweise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Kann leer sein  <br/> ||
   

