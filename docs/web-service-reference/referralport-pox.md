---
title: ReferralPort (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: cd693f1e-fed4-4eb9-8297-178906f47050
description: Das ReferralPort-Element gibt den Port an, der verwendet wird, um einen Verweis auf ein Verzeichnis zu erhalten.
ms.openlocfilehash: 6b3968d7b2f252439d2dfbc647bd8337668cf818
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456794"
---
# <a name="referralport-pox"></a><span data-ttu-id="f7529-103">ReferralPort (POX)</span><span class="sxs-lookup"><span data-stu-id="f7529-103">ReferralPort (POX)</span></span>

<span data-ttu-id="f7529-104">Das **ReferralPort** -Element gibt den Port an, der verwendet wird, um einen Verweis auf ein Verzeichnis zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f7529-104">The **ReferralPort** element specifies the port that is used to get a referral to a directory.</span></span> 
  
[<span data-ttu-id="f7529-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="f7529-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="f7529-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="f7529-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="f7529-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="f7529-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="f7529-108">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="f7529-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="f7529-109">ReferralPort (POX)</span><span class="sxs-lookup"><span data-stu-id="f7529-109">ReferralPort (POX)</span></span>](referralport-pox.md)
  
```xml
<ReferralPort/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="f7529-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f7529-110">Attributes and elements</span></span>

<span data-ttu-id="f7529-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f7529-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f7529-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="f7529-112">Attributes</span></span>

<span data-ttu-id="f7529-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="f7529-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f7529-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f7529-114">Child elements</span></span>

<span data-ttu-id="f7529-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="f7529-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f7529-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f7529-116">Parent elements</span></span>

|<span data-ttu-id="f7529-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="f7529-117">**Element**</span></span>|<span data-ttu-id="f7529-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f7529-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f7529-119">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="f7529-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="f7529-120">Enthält die Spezifikationen für das Verbinden eines Clients mit dem Computer, auf dem Microsoft Exchange Server 2007 ausgeführt wird, auf dem die Clientzugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="f7529-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f7529-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="f7529-121">Text value</span></span>

<span data-ttu-id="f7529-122">Der Wert Text stellt den Port dar, der für den Zugriff auf den Exchange-Server verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f7529-122">The text value represents the port that is used to access the Exchange server.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f7529-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f7529-123">Remarks</span></span>

<span data-ttu-id="f7529-124">Das **ReferralPort** -Element wird nur verwendet, wenn der [Typ (POX)-](type-pox.md) Element mit dem Wert "$" oder "expr" identisch ist.</span><span class="sxs-lookup"><span data-stu-id="f7529-124">The **ReferralPort** element is only used when the [Type (POX)](type-pox.md) element equals EXCH or EXPR.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f7529-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f7529-125">See also</span></span>



[<span data-ttu-id="f7529-126">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="f7529-126">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

