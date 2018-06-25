---
title: TTL (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 178eefa1-995c-4bea-930b-e51293961191
description: Das Element TTL gibt die Zeitspanne an Live, in Stunden, in denen die Einstellungen gültig.
ms.openlocfilehash: 5fecf3103553a82ed2aeeecfc1e4e1b9fe38583c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839269"
---
# <a name="ttl-pox"></a><span data-ttu-id="5f943-103">TTL (POX)</span><span class="sxs-lookup"><span data-stu-id="5f943-103">TTL (POX)</span></span>

<span data-ttu-id="5f943-104">Das Element **TTL** gibt die Zeitspanne an Live, in Stunden, in denen die Einstellungen gültig.</span><span class="sxs-lookup"><span data-stu-id="5f943-104">The **TTL** element specifies the Time to Live, in hours, during which the settings remain valid.</span></span> 
  
[<span data-ttu-id="5f943-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="5f943-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="5f943-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="5f943-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="5f943-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="5f943-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="5f943-108">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="5f943-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="5f943-109">TTL (POX)</span><span class="sxs-lookup"><span data-stu-id="5f943-109">TTL (POX)</span></span>](ttl-pox.md)
  
```xml
<TTL/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="5f943-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="5f943-110">Attributes and elements</span></span>

<span data-ttu-id="5f943-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="5f943-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5f943-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="5f943-112">Attributes</span></span>

<span data-ttu-id="5f943-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="5f943-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5f943-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5f943-114">Child elements</span></span>

<span data-ttu-id="5f943-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="5f943-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5f943-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5f943-116">Parent elements</span></span>

|<span data-ttu-id="5f943-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="5f943-117">**Element**</span></span>|<span data-ttu-id="5f943-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5f943-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5f943-119">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="5f943-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="5f943-120">Enthält die Spezifikationen für die Verbindung eines Clients mit dem Exchange Server 2007-Computer, auf dem die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="5f943-120">Contains the specifications for connecting a client to the Exchange Server 2007 computer on which the Client Access server role is installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5f943-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="5f943-121">Text value</span></span>

<span data-ttu-id="5f943-122">Der Textwert stellt Gültigkeitsdauer, in Stunden, in denen die Einstellungen gültig.</span><span class="sxs-lookup"><span data-stu-id="5f943-122">The text value represents the Time to Live, in hours, during which the settings remain valid.</span></span> <span data-ttu-id="5f943-123">Der Wert 0 gibt an, dass diese neue Suche nicht erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="5f943-123">A value of zero indicates that rediscovery is not required.</span></span> <span data-ttu-id="5f943-124">Wenn kein Wert angegeben ist, ist der Standardwert für dieses Element 1 Stunde.</span><span class="sxs-lookup"><span data-stu-id="5f943-124">If no value is specified, the default value for this element is 1 hour.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5f943-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5f943-125">Remarks</span></span>

<span data-ttu-id="5f943-126">Nach Ablauf dieses Zeitraums, der durch das **TTL** -Element dargestellt wird, sollte die Einstellungen mithilfe einer Anforderung der AutoErmittlung erneut gefunden.</span><span class="sxs-lookup"><span data-stu-id="5f943-126">After the time that is represented by the **TTL** element has elapsed, the settings should be rediscovered by using an Autodiscover request.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5f943-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5f943-127">See also</span></span>



[<span data-ttu-id="5f943-128">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="5f943-128">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

