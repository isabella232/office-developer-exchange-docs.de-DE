---
title: NetworkRequirements (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 1555fd2e-05b6-4b94-907b-dae9174049d9
description: Das NetworkRequirements-Element enthält die Kriterien, die verwendet werden, um zu bestimmen, ob sich der Clientcomputer in einem Netzwerk befindet, das die Anforderungen des Internetdienstanbieters erfüllt, um eine Verbindung mit dem Server herzustellen.
ms.openlocfilehash: d588f7eb12a445fba9c997c4b9db0a6842105b4e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462724"
---
# <a name="networkrequirements-pox"></a><span data-ttu-id="bfc2e-103">NetworkRequirements (POX)</span><span class="sxs-lookup"><span data-stu-id="bfc2e-103">NetworkRequirements (POX)</span></span>

<span data-ttu-id="bfc2e-104">Das **NetworkRequirements** -Element enthält die Kriterien, die verwendet werden, um zu bestimmen, ob sich der Clientcomputer in einem Netzwerk befindet, das die Anforderungen des Internetdienstanbieters erfüllt, um eine Verbindung mit dem Server herzustellen.</span><span class="sxs-lookup"><span data-stu-id="bfc2e-104">The **NetworkRequirements** element contains the criteria that are used to determine whether the client computer is on a network that meets the requirements of the Internet service provider (ISP) to connect to the server.</span></span> 
  
[<span data-ttu-id="bfc2e-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="bfc2e-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="bfc2e-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="bfc2e-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="bfc2e-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="bfc2e-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="bfc2e-108">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="bfc2e-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="bfc2e-109">NetworkRequirements (POX)</span><span class="sxs-lookup"><span data-stu-id="bfc2e-109">NetworkRequirements (POX)</span></span>](networkrequirements-pox.md)
  
```xml
<NetworkRequirements>
   <IPv4Start/>
   <IPv4End/>
   <IPv6Start/>
   <IPv6End/>
</NetworkRequirements>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="bfc2e-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="bfc2e-110">Attributes and elements</span></span>

<span data-ttu-id="bfc2e-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="bfc2e-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bfc2e-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="bfc2e-112">Attributes</span></span>

<span data-ttu-id="bfc2e-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="bfc2e-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bfc2e-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bfc2e-114">Child elements</span></span>

|<span data-ttu-id="bfc2e-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="bfc2e-115">**Element**</span></span>|<span data-ttu-id="bfc2e-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bfc2e-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bfc2e-117">IPv4Start (POX)</span><span class="sxs-lookup"><span data-stu-id="bfc2e-117">IPv4Start (POX)</span></span>](ipv4start-pox.md) <br/> |<span data-ttu-id="bfc2e-118">Gibt den Anfang eines Bereichs von IPv4-Adressen (IP Version 4) an, die zum Identifizieren eines Computers in einem Netzwerk verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bfc2e-118">Identifies the start of a range of IP version 4 (IPv4) addresses that are used to identify a computer on a network.</span></span>  <br/> |
|[<span data-ttu-id="bfc2e-119">IPv4End (POX)</span><span class="sxs-lookup"><span data-stu-id="bfc2e-119">IPv4End (POX)</span></span>](ipv4end-pox.md) <br/> |<span data-ttu-id="bfc2e-120">Identifiziert das Ende eines Bereichs von IPv4-Adressen (IP Version 4), die zum Identifizieren eines Computers im Netzwerk verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bfc2e-120">Identifies the end of a range of IP version 4 (IPv4) addresses that are used to identify a computer on the network.</span></span>  <br/> |
|[<span data-ttu-id="bfc2e-121">IPv6Start (POX)</span><span class="sxs-lookup"><span data-stu-id="bfc2e-121">IPv6Start (POX)</span></span>](ipv6start-pox.md) <br/> |<span data-ttu-id="bfc2e-122">Gibt den Anfang eines Bereichs von IPv6-Adressen (IP Version 6) an, die zum Identifizieren eines Computers in einem Netzwerk verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bfc2e-122">Identifies the start of a range of IP version 6 (IPv6) addresses that are used to identify a computer on a network.</span></span>  <br/> |
|[<span data-ttu-id="bfc2e-123">IPv6End (POX)</span><span class="sxs-lookup"><span data-stu-id="bfc2e-123">IPv6End (POX)</span></span>](ipv6end-pox.md) <br/> |<span data-ttu-id="bfc2e-124">Identifiziert das Ende eines Bereichs von IPv6-Adressen (IP Version 6), die verwendet werden, um einen Computer in einem Netzwerk zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="bfc2e-124">Identifies the end of a range of IP version 6 (IPv6) addresses that are used to identify a computer on a network.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="bfc2e-125">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bfc2e-125">Parent elements</span></span>

|<span data-ttu-id="bfc2e-126">**Element**</span><span class="sxs-lookup"><span data-stu-id="bfc2e-126">**Element**</span></span>|<span data-ttu-id="bfc2e-127">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bfc2e-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bfc2e-128">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="bfc2e-128">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="bfc2e-129">Enthält die Spezifikationen für das Verbinden eines Clients mit dem Computer, auf dem Microsoft Exchange Server 2007 ausgeführt wird, auf dem die Clientzugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="bfc2e-129">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bfc2e-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bfc2e-130">Remarks</span></span>

<span data-ttu-id="bfc2e-131">Wenn der e-Mail-Client nicht den Netzwerkanforderungen entspricht, sollte er andere Protokolltypen ausprobieren.</span><span class="sxs-lookup"><span data-stu-id="bfc2e-131">If the e-mail client does not match the network requirements, it should try other protocol types.</span></span> <span data-ttu-id="bfc2e-132">ISPs können eine Gruppe von Servern mit [Protokoll-Tags (POX)](protocol-pox.md) bereitstellen, die keine Authentifizierung erfordern, aber sich im ISP-Netzwerk befinden müssen.</span><span class="sxs-lookup"><span data-stu-id="bfc2e-132">ISPs may provide one set of servers with [Protocol (POX)](protocol-pox.md) tags that do not require authentication but are required to be on the ISP network.</span></span> <span data-ttu-id="bfc2e-133">ISPs können eine andere Gruppe von Servern auflisten, die eine Authentifizierung erfordern, sich jedoch nicht in einem bestimmten Netzwerk befinden müssen.</span><span class="sxs-lookup"><span data-stu-id="bfc2e-133">ISPs may list another set of servers that require authentication but are not required to be on a specific network.</span></span> 
  
<span data-ttu-id="bfc2e-134">Das **NetworkRequirements** -Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="bfc2e-134">The **NetworkRequirements** element is optional.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bfc2e-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bfc2e-135">See also</span></span>



[<span data-ttu-id="bfc2e-136">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="bfc2e-136">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

