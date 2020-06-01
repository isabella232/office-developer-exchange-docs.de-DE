---
title: UsePOPAuth (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 28f552d8-6bb8-49b4-a45c-b2053670f1cc
description: Das UsePOPAuth-Element gibt an, ob die Authentifizierungsinformationen, die für einen POP3-Kontotyp bereitgestellt werden, auch für Simple Mail Transfer Protocol (SMTP) verwendet werden.
ms.openlocfilehash: 8d5bfffaab31c382ad43915e18b8a7a2b2737c21
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466507"
---
# <a name="usepopauth-pox"></a><span data-ttu-id="1a162-103">UsePOPAuth (POX)</span><span class="sxs-lookup"><span data-stu-id="1a162-103">UsePOPAuth (POX)</span></span>

<span data-ttu-id="1a162-104">Das **UsePOPAuth** -Element gibt an, ob die Authentifizierungsinformationen, die für einen POP3-Kontotyp bereitgestellt werden, auch für Simple Mail Transfer Protocol (SMTP) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1a162-104">The **UsePOPAuth** element indicates whether the authentication information that is provided for a POP3 type of account is also used for Simple Mail Transfer Protocol (SMTP).</span></span> 
  
[<span data-ttu-id="1a162-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="1a162-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="1a162-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="1a162-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="1a162-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="1a162-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="1a162-108">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="1a162-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="1a162-109">UsePOPAuth (POX)</span><span class="sxs-lookup"><span data-stu-id="1a162-109">UsePOPAuth (POX)</span></span>](usepopauth-pox.md)
  
```xml
<UsePOPAuth>on or off</UsePOPAuth>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="1a162-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1a162-110">Attributes and elements</span></span>

<span data-ttu-id="1a162-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1a162-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1a162-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="1a162-112">Attributes</span></span>

<span data-ttu-id="1a162-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="1a162-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1a162-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1a162-114">Child elements</span></span>

<span data-ttu-id="1a162-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="1a162-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1a162-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1a162-116">Parent elements</span></span>

|<span data-ttu-id="1a162-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="1a162-117">**Element**</span></span>|<span data-ttu-id="1a162-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1a162-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1a162-119">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="1a162-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="1a162-120">Enthält die Spezifikationen für das Verbinden eines Clients mit dem Computer, auf dem Microsoft Exchange Server 2007 ausgeführt wird, auf dem die Clientzugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="1a162-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1a162-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="1a162-121">Text value</span></span>

<span data-ttu-id="1a162-122">Der Textwert gibt an, ob die Authentifizierungsinformationen, die für einen POP3-Kontotyp angegeben werden, auch für SMTP verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1a162-122">The text value indicates whether the authentication information that is provided for a POP3 type of account is also used for SMTP.</span></span> <span data-ttu-id="1a162-123">Die möglichen Werte sind **ein** -und **ausgeschaltet**.</span><span class="sxs-lookup"><span data-stu-id="1a162-123">The possible values are **on** and **off**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1a162-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1a162-124">Remarks</span></span>

<span data-ttu-id="1a162-125">Das **UsePOPAuth** -Element wird nur verwendet, wenn der [Typ (POX)](type-pox.md) SMTP lautet.</span><span class="sxs-lookup"><span data-stu-id="1a162-125">The **UsePOPAuth** element is only used when [Type (POX)](type-pox.md) is SMTP.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1a162-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1a162-126">See also</span></span>



[<span data-ttu-id="1a162-127">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="1a162-127">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

