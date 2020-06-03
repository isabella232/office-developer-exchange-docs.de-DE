---
title: LobbyBypass
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e05ed6eb-00ae-49c8-8341-43f6e0d728ff
description: Das LobbyBypass-Element gibt die Online Besprechungs Einstellung an, um die virtuelle Lobby zu umgehen.
ms.openlocfilehash: 6940428c944b9d4d64acc6dbbf3993576e1932eb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458096"
---
# <a name="lobbybypass"></a>LobbyBypass

Das **LobbyBypass** -Element gibt die Online Besprechungs Einstellung an, um die virtuelle Lobby zu umgehen. 
  
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

Der Textwert des **LobbyBypass** -Elements kann entweder **deaktiviert** oder **EnabledForGatewayParticipants**sein. Der **Deaktivierte** Wert gibt an, dass die Lobby Umgehung deaktiviert ist, damit alle Besprechungsteilnehmer über die virtuelle Lobby zugreifen müssen. Der Wert **EnabledForGatewayParticipants** gibt an, dass die Lobby Umgehung für Telefonteilnehmer aktiviert ist. 
  
## <a name="remarks"></a>Bemerkungen

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  

