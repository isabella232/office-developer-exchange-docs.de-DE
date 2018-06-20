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
description: Das ReferralPort-Element gibt den Port, der zum Abrufen eines Verweises auf ein Verzeichnis verwendet wird.
ms.openlocfilehash: 5045c0c5a9f15d5a31ac2e884b942e00dfb1f520
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831037"
---
# <a name="referralport-pox"></a><span data-ttu-id="1f559-103">ReferralPort (POX)</span><span class="sxs-lookup"><span data-stu-id="1f559-103">ReferralPort (POX)</span></span>

<span data-ttu-id="1f559-104">Das **ReferralPort** -Element gibt den Port, der zum Abrufen eines Verweises auf ein Verzeichnis verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1f559-104">The **ReferralPort** element specifies the port that is used to get a referral to a directory.</span></span> 
  
[<span data-ttu-id="1f559-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="1f559-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="1f559-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="1f559-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="1f559-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="1f559-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="1f559-108">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="1f559-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="1f559-109">ReferralPort (POX)</span><span class="sxs-lookup"><span data-stu-id="1f559-109">ReferralPort (POX)</span></span>](referralport-pox.md)
  
```xml
<ReferralPort/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="1f559-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1f559-110">Attributes and elements</span></span>

<span data-ttu-id="1f559-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1f559-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1f559-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="1f559-112">Attributes</span></span>

<span data-ttu-id="1f559-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="1f559-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1f559-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1f559-114">Child elements</span></span>

<span data-ttu-id="1f559-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="1f559-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1f559-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1f559-116">Parent elements</span></span>

|<span data-ttu-id="1f559-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="1f559-117">**Element**</span></span>|<span data-ttu-id="1f559-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1f559-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1f559-119">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="1f559-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="1f559-120">Enthält die Spezifikationen für die Verbindung eines Clients mit dem Computer, auf der Microsoft Exchange Server 2007 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="1f559-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1f559-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="1f559-121">Text value</span></span>

<span data-ttu-id="1f559-122">Der Textwert stellt den Port, der Zugriff auf den Exchange-Server verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1f559-122">The text value represents the port that is used to access the Exchange server.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1f559-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1f559-123">Remarks</span></span>

<span data-ttu-id="1f559-124">Das **ReferralPort** -Element wird nur verwendet, wenn das Element [Typ (POX)](type-pox.md) EXCH oder Ausdruck gleich ist.</span><span class="sxs-lookup"><span data-stu-id="1f559-124">The **ReferralPort** element is only used when the [Type (POX)](type-pox.md) element equals EXCH or EXPR.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1f559-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1f559-125">See also</span></span>



[<span data-ttu-id="1f559-126">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="1f559-126">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

