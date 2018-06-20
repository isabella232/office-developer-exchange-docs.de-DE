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
description: Das NetworkRequirements-Element enthält die Kriterien, die verwendet werden, um festzustellen, ob der Clientcomputer in einem Netzwerk, die erfüllt die Anforderungen des Internet-Dienstanbieters (ISP ist), um mit dem Server herstellen.
ms.openlocfilehash: f3abcff04cd4121b8dcc7ceff7658ad389e6d0b0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830529"
---
# <a name="networkrequirements-pox"></a><span data-ttu-id="25284-103">NetworkRequirements (POX)</span><span class="sxs-lookup"><span data-stu-id="25284-103">NetworkRequirements (POX)</span></span>

<span data-ttu-id="25284-104">Das **NetworkRequirements** -Element enthält die Kriterien, die verwendet werden, um festzustellen, ob der Clientcomputer in einem Netzwerk, die erfüllt die Anforderungen des Internet-Dienstanbieters (ISP ist), um mit dem Server herstellen.</span><span class="sxs-lookup"><span data-stu-id="25284-104">The **NetworkRequirements** element contains the criteria that are used to determine whether the client computer is on a network that meets the requirements of the Internet service provider (ISP) to connect to the server.</span></span> 
  
[<span data-ttu-id="25284-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="25284-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="25284-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="25284-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="25284-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="25284-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="25284-108">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="25284-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="25284-109">NetworkRequirements (POX)</span><span class="sxs-lookup"><span data-stu-id="25284-109">NetworkRequirements (POX)</span></span>](networkrequirements-pox.md)
  
```xml
<NetworkRequirements>
   <IPv4Start/>
   <IPv4End/>
   <IPv6Start/>
   <IPv6End/>
</NetworkRequirements>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="25284-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="25284-110">Attributes and elements</span></span>

<span data-ttu-id="25284-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="25284-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="25284-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="25284-112">Attributes</span></span>

<span data-ttu-id="25284-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="25284-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="25284-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="25284-114">Child elements</span></span>

|<span data-ttu-id="25284-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="25284-115">**Element**</span></span>|<span data-ttu-id="25284-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="25284-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="25284-117">IPv4Start (POX)</span><span class="sxs-lookup"><span data-stu-id="25284-117">IPv4Start (POX)</span></span>](ipv4start-pox.md) <br/> |<span data-ttu-id="25284-118">Gibt den Beginn einer Reihe von IP-Version 4 (IPv4)-Adressen, die zur Identifizierung von eines Computers in einem Netzwerk verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="25284-118">Identifies the start of a range of IP version 4 (IPv4) addresses that are used to identify a computer on a network.</span></span>  <br/> |
|[<span data-ttu-id="25284-119">IPv4End (POX)</span><span class="sxs-lookup"><span data-stu-id="25284-119">IPv4End (POX)</span></span>](ipv4end-pox.md) <br/> |<span data-ttu-id="25284-120">Bezeichnet das Ende einer Reihe von IP-Version 4 (IPv4)-Adressen, die verwendet werden, um einen Computer im Netzwerk zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="25284-120">Identifies the end of a range of IP version 4 (IPv4) addresses that are used to identify a computer on the network.</span></span>  <br/> |
|[<span data-ttu-id="25284-121">IPv6Start (POX)</span><span class="sxs-lookup"><span data-stu-id="25284-121">IPv6Start (POX)</span></span>](ipv6start-pox.md) <br/> |<span data-ttu-id="25284-122">Identifiziert den Anfang des einen Bereich von IP Version 6 (IPv6)-Adressen, die zur Identifizierung von eines Computers in einem Netzwerk verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="25284-122">Identifies the start of a range of IP version 6 (IPv6) addresses that are used to identify a computer on a network.</span></span>  <br/> |
|[<span data-ttu-id="25284-123">IPv6End (POX)</span><span class="sxs-lookup"><span data-stu-id="25284-123">IPv6End (POX)</span></span>](ipv6end-pox.md) <br/> |<span data-ttu-id="25284-124">Bezeichnet das Ende einer Reihe von IP-Version 6 (IPv6)-Adressen, die zur Identifizierung von eines Computers in einem Netzwerk verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="25284-124">Identifies the end of a range of IP version 6 (IPv6) addresses that are used to identify a computer on a network.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="25284-125">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="25284-125">Parent elements</span></span>

|<span data-ttu-id="25284-126">**Element**</span><span class="sxs-lookup"><span data-stu-id="25284-126">**Element**</span></span>|<span data-ttu-id="25284-127">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="25284-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="25284-128">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="25284-128">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="25284-129">Enthält die Spezifikationen für die Verbindung eines Clients mit dem Computer, auf der Microsoft Exchange Server 2007 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="25284-129">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="25284-130">Hinweise</span><span class="sxs-lookup"><span data-stu-id="25284-130">Remarks</span></span>

<span data-ttu-id="25284-131">Wenn der e-Mail-Client nicht die netzwerkanforderungen entspricht, sollte es anderen Protokolltypen versuchen.</span><span class="sxs-lookup"><span data-stu-id="25284-131">If the e-mail client does not match the network requirements, it should try other protocol types.</span></span> <span data-ttu-id="25284-132">Internetdienstanbieter vorsehen eine Gruppe von Servern mit [Protocol (POX)](protocol-pox.md) Tags, die erforderlich sind, erfordern keine Authentifizierung ISP-Netzwerk befinden.</span><span class="sxs-lookup"><span data-stu-id="25284-132">ISPs may provide one set of servers with [Protocol (POX)](protocol-pox.md) tags that do not require authentication but are required to be on the ISP network.</span></span> <span data-ttu-id="25284-133">Internetdienstanbieter können einen anderen Satz von Servern aufzulisten, die Authentifizierung erfordern, nicht aber ein bestimmtes Netzwerk befinden.</span><span class="sxs-lookup"><span data-stu-id="25284-133">ISPs may list another set of servers that require authentication but are not required to be on a specific network.</span></span> 
  
<span data-ttu-id="25284-134">Das **NetworkRequirements** -Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="25284-134">The **NetworkRequirements** element is optional.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="25284-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="25284-135">See also</span></span>



[<span data-ttu-id="25284-136">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="25284-136">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

