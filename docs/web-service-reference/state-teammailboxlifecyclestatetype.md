---
title: Status (TeamMailboxLifecycleStateType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 3b1bc531-6988-41c3-9aad-3f5ad5b732a9
description: Das State-Element enthält den Lebenszyklusstatus, der für ein Websitepostfach festgelegt ist.
ms.openlocfilehash: 5189ee8573fd33d2265fd60c47bb40d17b16b8fe
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59538968"
---
# <a name="state-teammailboxlifecyclestatetype"></a>Status (TeamMailboxLifecycleStateType)

Das **State-Element** enthält den Lebenszyklusstatus, der für ein Websitepostfach festgelegt ist. 
  
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

Der Textwert des **State-Elements** ist der Lebenszyklusstatus, der für ein Websitepostfach festgelegt ist. Der Textwert **"Active"** gibt an, dass ein Websitepostfach aktiv verwendet wird. Der Textwert **"Closed"** gibt an, dass ein Websitepostfach geschlossen wurde und nicht aktiv verwendet wird. Der Textwert **"Nicht verknüpft"** gibt an, dass ein Websitepostfach nicht mit einer webbasierten Umgebung für die Zusammenarbeit verknüpft ist. Die Werte **"Active",** **"Closed"** und **"PendingDelete"** schließen sich gegenseitig aus, aber der Wert **"Nicht verknüpft"** schließt sich nicht gegenseitig von den anderen Werten aus. Der Textwert **"PendingDelete"** gibt an, dass ein Websitepostfach gelöscht werden muss. Ein Websitepostfach muss geschlossen werden, bevor es als **"PendingDelete"** festgelegt werden kann.
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Kann leer sein  <br/> ||
   

