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
# <a name="lobbybypass"></a><span data-ttu-id="54734-103">LobbyBypass</span><span class="sxs-lookup"><span data-stu-id="54734-103">LobbyBypass</span></span>

<span data-ttu-id="54734-104">Das **LobbyBypass** -Element gibt die onlinebesprechung teilnehmen, umgehen den Wartebereich für eine virtuellen festlegen.</span><span class="sxs-lookup"><span data-stu-id="54734-104">The **LobbyBypass** element specifies the online meeting setting to bypass the virtual lobby.</span></span> 
  
```XML
<LobbyBypass> Disabled | EnabledForGatewayParticipants </LobbyBypass>
```

 <span data-ttu-id="54734-105">**LobbyBypassType**</span><span class="sxs-lookup"><span data-stu-id="54734-105">**LobbyBypassType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="54734-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="54734-106">Attributes and elements</span></span>

<span data-ttu-id="54734-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="54734-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="54734-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="54734-108">Attributes</span></span>

<span data-ttu-id="54734-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="54734-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="54734-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="54734-110">Child elements</span></span>

<span data-ttu-id="54734-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="54734-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="54734-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="54734-112">Parent elements</span></span>

[<span data-ttu-id="54734-113">OnlineMeetingSettings</span><span class="sxs-lookup"><span data-stu-id="54734-113">OnlineMeetingSettings</span></span>](onlinemeetingsettings.md)
  
## <a name="text-value"></a><span data-ttu-id="54734-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="54734-114">Text value</span></span>

<span data-ttu-id="54734-115">Der Textwert des **LobbyBypass** -Elements kann entweder **deaktiviert** oder **EnabledForGatewayParticipants**sein.</span><span class="sxs-lookup"><span data-stu-id="54734-115">The text value of the **LobbyBypass** element can be either **Disabled** or **EnabledForGatewayParticipants**.</span></span> <span data-ttu-id="54734-116">Der Wert **deaktiviert** gibt an, dass die Umgehung der Lobby deaktiviert ist, sodass alle Besprechungsteilnehmer über den Wartebereich für eine virtuelle zugreifen müssen.</span><span class="sxs-lookup"><span data-stu-id="54734-116">The **Disabled** value indicates that the lobby bypass is disabled so all meeting attendees must access through the virtual lobby.</span></span> <span data-ttu-id="54734-117">Der Wert **EnabledForGatewayParticipants** gibt an, dass die Lobby Umgehung für Teilnehmer per Telefon aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="54734-117">The **EnabledForGatewayParticipants** value indicates that the lobby bypass is enabled for telephone participants.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="54734-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="54734-118">Remarks</span></span>

<span data-ttu-id="54734-119">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="54734-119">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="54734-120">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="54734-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  

