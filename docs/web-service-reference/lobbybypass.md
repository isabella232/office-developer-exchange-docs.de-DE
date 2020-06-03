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
# <a name="lobbybypass"></a><span data-ttu-id="6a96d-103">LobbyBypass</span><span class="sxs-lookup"><span data-stu-id="6a96d-103">LobbyBypass</span></span>

<span data-ttu-id="6a96d-104">Das **LobbyBypass** -Element gibt die Online Besprechungs Einstellung an, um die virtuelle Lobby zu umgehen.</span><span class="sxs-lookup"><span data-stu-id="6a96d-104">The **LobbyBypass** element specifies the online meeting setting to bypass the virtual lobby.</span></span> 
  
```XML
<LobbyBypass> Disabled | EnabledForGatewayParticipants </LobbyBypass>
```

 <span data-ttu-id="6a96d-105">**LobbyBypassType**</span><span class="sxs-lookup"><span data-stu-id="6a96d-105">**LobbyBypassType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6a96d-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="6a96d-106">Attributes and elements</span></span>

<span data-ttu-id="6a96d-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="6a96d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6a96d-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="6a96d-108">Attributes</span></span>

<span data-ttu-id="6a96d-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="6a96d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6a96d-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6a96d-110">Child elements</span></span>

<span data-ttu-id="6a96d-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="6a96d-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6a96d-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6a96d-112">Parent elements</span></span>

[<span data-ttu-id="6a96d-113">OnlineMeetingSettings</span><span class="sxs-lookup"><span data-stu-id="6a96d-113">OnlineMeetingSettings</span></span>](onlinemeetingsettings.md)
  
## <a name="text-value"></a><span data-ttu-id="6a96d-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="6a96d-114">Text value</span></span>

<span data-ttu-id="6a96d-115">Der Textwert des **LobbyBypass** -Elements kann entweder **deaktiviert** oder **EnabledForGatewayParticipants**sein.</span><span class="sxs-lookup"><span data-stu-id="6a96d-115">The text value of the **LobbyBypass** element can be either **Disabled** or **EnabledForGatewayParticipants**.</span></span> <span data-ttu-id="6a96d-116">Der **Deaktivierte** Wert gibt an, dass die Lobby Umgehung deaktiviert ist, damit alle Besprechungsteilnehmer über die virtuelle Lobby zugreifen müssen.</span><span class="sxs-lookup"><span data-stu-id="6a96d-116">The **Disabled** value indicates that the lobby bypass is disabled so all meeting attendees must access through the virtual lobby.</span></span> <span data-ttu-id="6a96d-117">Der Wert **EnabledForGatewayParticipants** gibt an, dass die Lobby Umgehung für Telefonteilnehmer aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="6a96d-117">The **EnabledForGatewayParticipants** value indicates that the lobby bypass is enabled for telephone participants.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="6a96d-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6a96d-118">Remarks</span></span>

<span data-ttu-id="6a96d-119">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="6a96d-119">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="6a96d-120">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="6a96d-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  

