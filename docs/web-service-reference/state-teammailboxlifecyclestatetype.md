---
title: State (TeamMailboxLifecycleStateType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3b1bc531-6988-41c3-9aad-3f5ad5b732a9
description: Das State-Element enthält den Lebenszyklusstatus, der für ein websitepostfach festgelegt wird.
ms.openlocfilehash: 597946b48649d997f8dd57823b4e0fcc091a6f84
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465163"
---
# <a name="state-teammailboxlifecyclestatetype"></a>State (TeamMailboxLifecycleStateType)

Das **State** -Element enthält den Lebenszyklusstatus, der für ein websitepostfach festgelegt wird. 
  
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

Der Textwert des **State** -Elements ist der Lebenszyklusstatus, der für ein websitepostfach festgelegt wird. Der Textwert **aktiv** gibt an, dass ein websitepostfach aktiv verwendet wird. Der Textwert **Closed** gibt an, dass ein websitepostfach geschlossen wurde und nicht aktiv verwendet wird. Ein Textwert von **unlinked** gibt an, dass ein websitepostfach nicht mit einer webbasierten Zusammenarbeitsumgebung verknüpft ist. Die Werte " **aktiv**", " **Closed**" und " **" PendingDelete "** " schließen sich gegenseitig aus, aber der nicht **verlinkte** Wert schließt sich nicht gegenseitig aus den anderen Werten aus. Der Textwert **"PendingDelete"** gibt an, dass ein websitepostfach aussteht, das gelöscht wird. Ein websitepostfach muss geschlossen werden, bevor es als **"PendingDelete"** festgelegt werden kann.
  
## <a name="remarks"></a>Bemerkungen

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Kann leer sein  <br/> ||
   

