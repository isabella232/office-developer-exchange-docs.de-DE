---
title: ServerDN (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 2ef73d13-e8bb-43f6-96c7-3ee157fed739
description: Das ServerDN-Element gibt den distinguished Name des Computers, auf dem Microsoft Exchange Server 2007 ausgeführt wird.
ms.openlocfilehash: d2b9ce663d8245a78acd088b0622406c0dfcb4da
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831374"
---
# <a name="serverdn-pox"></a><span data-ttu-id="179ba-103">ServerDN (POX)</span><span class="sxs-lookup"><span data-stu-id="179ba-103">ServerDN (POX)</span></span>

<span data-ttu-id="179ba-104">Das **ServerDN** -Element gibt den distinguished Name des Computers, auf dem Microsoft Exchange Server 2007 ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="179ba-104">The **ServerDN** element specifies the distinguished name of the computer that is running Microsoft Exchange Server 2007.</span></span> 
  
[<span data-ttu-id="179ba-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="179ba-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="179ba-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="179ba-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="179ba-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="179ba-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="179ba-108">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="179ba-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="179ba-109">ServerDN (POX)</span><span class="sxs-lookup"><span data-stu-id="179ba-109">ServerDN (POX)</span></span>](serverdn-pox.md)
  
```xml
<ServerDN/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="179ba-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="179ba-110">Attributes and elements</span></span>

<span data-ttu-id="179ba-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="179ba-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="179ba-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="179ba-112">Attributes</span></span>

<span data-ttu-id="179ba-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="179ba-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="179ba-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="179ba-114">Child elements</span></span>

<span data-ttu-id="179ba-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="179ba-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="179ba-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="179ba-116">Parent elements</span></span>

|<span data-ttu-id="179ba-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="179ba-117">**Element**</span></span>|<span data-ttu-id="179ba-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="179ba-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="179ba-119">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="179ba-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="179ba-120">Enthält die Spezifikationen für die Verbindung eines Clients mit dem Computer, auf der Microsoft Exchange Server 2007 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="179ba-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="179ba-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="179ba-121">Text value</span></span>

<span data-ttu-id="179ba-122">Der Textwert stellt den distinguished Name des Exchange-Servers.</span><span class="sxs-lookup"><span data-stu-id="179ba-122">The text value represents the distinguished name of the Exchange server.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="179ba-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="179ba-123">Remarks</span></span>

<span data-ttu-id="179ba-124">Der Wert **ServerDN** wird nur verwendet, wenn [Type (POX)](type-pox.md) Wechselkurs entspricht</span><span class="sxs-lookup"><span data-stu-id="179ba-124">The **ServerDN** value is only used when [Type (POX)](type-pox.md) is equal to EXCH.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="179ba-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="179ba-125">See also</span></span>



[<span data-ttu-id="179ba-126">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="179ba-126">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

