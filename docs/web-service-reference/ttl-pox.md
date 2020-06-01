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
description: Das TTL-Element gibt die Zeit in Stunden an, in der die Einstellungen gültig bleiben.
ms.openlocfilehash: 9a17cbe4e669d1afe9f3ef4a24f2a9a2889a7d52
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467382"
---
# <a name="ttl-pox"></a><span data-ttu-id="a4aa8-103">TTL (POX)</span><span class="sxs-lookup"><span data-stu-id="a4aa8-103">TTL (POX)</span></span>

<span data-ttu-id="a4aa8-104">Das **TTL** -Element gibt die Zeit in Stunden an, in der die Einstellungen gültig bleiben.</span><span class="sxs-lookup"><span data-stu-id="a4aa8-104">The **TTL** element specifies the Time to Live, in hours, during which the settings remain valid.</span></span> 
  
[<span data-ttu-id="a4aa8-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="a4aa8-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="a4aa8-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="a4aa8-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="a4aa8-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="a4aa8-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="a4aa8-108">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="a4aa8-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="a4aa8-109">TTL (POX)</span><span class="sxs-lookup"><span data-stu-id="a4aa8-109">TTL (POX)</span></span>](ttl-pox.md)
  
```xml
<TTL/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="a4aa8-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a4aa8-110">Attributes and elements</span></span>

<span data-ttu-id="a4aa8-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a4aa8-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a4aa8-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="a4aa8-112">Attributes</span></span>

<span data-ttu-id="a4aa8-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="a4aa8-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a4aa8-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a4aa8-114">Child elements</span></span>

<span data-ttu-id="a4aa8-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="a4aa8-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a4aa8-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a4aa8-116">Parent elements</span></span>

|<span data-ttu-id="a4aa8-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="a4aa8-117">**Element**</span></span>|<span data-ttu-id="a4aa8-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a4aa8-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a4aa8-119">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="a4aa8-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="a4aa8-120">Enthält die Spezifikationen für das Verbinden eines Clients mit dem Exchange Server 2007 Computer, auf dem die Clientzugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="a4aa8-120">Contains the specifications for connecting a client to the Exchange Server 2007 computer on which the Client Access server role is installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a4aa8-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="a4aa8-121">Text value</span></span>

<span data-ttu-id="a4aa8-122">Der Textwert stellt die Zeit zu leben, in Stunden, während der die Einstellungen gültig bleiben.</span><span class="sxs-lookup"><span data-stu-id="a4aa8-122">The text value represents the Time to Live, in hours, during which the settings remain valid.</span></span> <span data-ttu-id="a4aa8-123">Der Wert NULL gibt an, dass die Wiedererkennung nicht erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="a4aa8-123">A value of zero indicates that rediscovery is not required.</span></span> <span data-ttu-id="a4aa8-124">Wenn kein Wert angegeben ist, ist der Standardwert für dieses Element 1 Stunde.</span><span class="sxs-lookup"><span data-stu-id="a4aa8-124">If no value is specified, the default value for this element is 1 hour.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a4aa8-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a4aa8-125">Remarks</span></span>

<span data-ttu-id="a4aa8-126">Nachdem die vom **TTL** -Element dargestellte Zeit verstrichen ist, sollten die Einstellungen mithilfe einer AutoErmittlungs-Anforderung erneut ermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="a4aa8-126">After the time that is represented by the **TTL** element has elapsed, the settings should be rediscovered by using an Autodiscover request.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a4aa8-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a4aa8-127">See also</span></span>



[<span data-ttu-id="a4aa8-128">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="a4aa8-128">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

