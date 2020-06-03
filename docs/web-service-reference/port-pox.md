---
title: Port (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 4046821a-d6f3-4764-82be-4011221ce7a3
description: Das Port-Element gibt den Port an, der zum Herstellen einer Verbindung mit dem Speicher verwendet wird.
ms.openlocfilehash: 2da59e03a57b44fb12d14368d1b585ba845eacfe
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464014"
---
# <a name="port-pox"></a><span data-ttu-id="8fca9-103">Port (POX)</span><span class="sxs-lookup"><span data-stu-id="8fca9-103">Port (POX)</span></span>

<span data-ttu-id="8fca9-104">Das **Port** -Element gibt den Port an, der zum Herstellen einer Verbindung mit dem Speicher verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8fca9-104">The **Port** element specifies the port that is used to connect to the store.</span></span> 
  
[<span data-ttu-id="8fca9-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="8fca9-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="8fca9-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="8fca9-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="8fca9-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="8fca9-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="8fca9-108">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="8fca9-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="8fca9-109">Port (POX)</span><span class="sxs-lookup"><span data-stu-id="8fca9-109">Port (POX)</span></span>](port-pox.md)
  
```xml
<Port/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="8fca9-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="8fca9-110">Attributes and elements</span></span>

<span data-ttu-id="8fca9-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="8fca9-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8fca9-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="8fca9-112">Attributes</span></span>

<span data-ttu-id="8fca9-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="8fca9-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8fca9-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8fca9-114">Child elements</span></span>

<span data-ttu-id="8fca9-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="8fca9-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8fca9-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8fca9-116">Parent elements</span></span>

|<span data-ttu-id="8fca9-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="8fca9-117">**Element**</span></span>|<span data-ttu-id="8fca9-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8fca9-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8fca9-119">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="8fca9-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="8fca9-120">Enthält die Spezifikationen für das Verbinden eines Clients mit dem Computer, auf dem Microsoft Exchange Server 2007 ausgeführt wird, auf dem die Clientzugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="8fca9-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="8fca9-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="8fca9-121">Text value</span></span>

<span data-ttu-id="8fca9-122">Der Wert Text stellt den Port dar, der für den Zugriff auf den Exchange-Server verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8fca9-122">The text value represents the port that is used to access the Exchange server.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8fca9-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8fca9-123">Remarks</span></span>

<span data-ttu-id="8fca9-124">Der **Portwert** wird nicht verwendet, wenn das [Server (POX)-](server-pox.md) Element eine URL enthält.</span><span class="sxs-lookup"><span data-stu-id="8fca9-124">The **Port** value is not used if the [Server (POX)](server-pox.md) element contains a URL.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8fca9-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8fca9-125">See also</span></span>



[<span data-ttu-id="8fca9-126">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="8fca9-126">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

