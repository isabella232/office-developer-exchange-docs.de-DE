---
title: LobbyBypass
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: e05ed6eb-00ae-49c8-8341-43f6e0d728ff
description: Das LobbyBypass-Element gibt die Onlinebesprechungseinstellung an, um den virtuellen Wartebereich zu umgehen.
ms.openlocfilehash: 41ab9c3f846112d2b679bbb477a0de355a477ffa
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59540783"
---
# <a name="lobbybypass"></a>LobbyBypass

Das **LobbyBypass-Element** gibt die Onlinebesprechungseinstellung an, um den virtuellen Wartebereich zu umgehen. 
  
```XML
<LobbyBypass> Disabled | EnabledForGatewayParticipants </LobbyBypass>
```

 **LobbyBypassType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[OnlineMeetingSettings](onlinemeetingsettings.md)
  
## <a name="text-value"></a>Textwert

Der Textwert des **LobbyBypass** -Elements kann entweder **Disabled** oder **EnabledForGatewayParticipants** sein. Der Wert **"Disabled"** gibt an, dass die Wartebereichsumgehung deaktiviert ist, sodass alle Besprechungsteilnehmer über den virtuellen Wartebereich zugreifen müssen. Der **Wert EnabledForGatewayParticipants** gibt an, dass die Wartebereichsumgehung für Telefonteilnehmer aktiviert ist. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  

