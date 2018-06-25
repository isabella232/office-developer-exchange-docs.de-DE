---
title: LobbyBypass
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e05ed6eb-00ae-49c8-8341-43f6e0d728ff
description: Das LobbyBypass-Element gibt die onlinebesprechung teilnehmen, umgehen den Wartebereich für eine virtuellen festlegen.
ms.openlocfilehash: 9ecc920acd9e1aea3476ad1194d6c7d0529b21c7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830246"
---
# <a name="lobbybypass"></a>LobbyBypass

Das **LobbyBypass** -Element gibt die onlinebesprechung teilnehmen, umgehen den Wartebereich für eine virtuellen festlegen. 
  
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

Der Textwert des **LobbyBypass** -Elements kann entweder **deaktiviert** oder **EnabledForGatewayParticipants**sein. Der Wert **deaktiviert** gibt an, dass die Umgehung der Lobby deaktiviert ist, sodass alle Besprechungsteilnehmer über den Wartebereich für eine virtuelle zugreifen müssen. Der Wert **EnabledForGatewayParticipants** gibt an, dass die Lobby Umgehung für Teilnehmer per Telefon aktiviert ist. 
  
## <a name="remarks"></a>Hinweise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  

