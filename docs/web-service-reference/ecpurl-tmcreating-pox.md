---
title: EcpUrl-tmCreating (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c942758e-5ff3-4acb-9080-b8672e56f696
description: Das EcpUrl-tmCreating-Element gibt eine partielle URL an, die mit dem Wert des EcpUrl (POX)-Elements kombiniert werden kann, um eine URL zu generieren, die zum Erstellen eines neuen websitepostfachs verwendet werden kann.
ms.openlocfilehash: 93ea3f5752dab0028c0732e5e79c5690e35bd059
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462059"
---
# <a name="ecpurl-tmcreating-pox"></a><span data-ttu-id="868fc-103">EcpUrl-tmCreating (POX)</span><span class="sxs-lookup"><span data-stu-id="868fc-103">EcpUrl-tmCreating (POX)</span></span>

<span data-ttu-id="868fc-104">Das **EcpUrl-tmCreating-** Element gibt eine partielle URL an, die mit dem Wert des [EcpUrl (POX)](ecpurl-pox.md) -Elements kombiniert werden kann, um eine URL zu generieren, die zum Erstellen eines neuen websitepostfachs verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="868fc-104">The **EcpUrl-tmCreating** element specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to create a new site mailbox.</span></span> 
  
[<span data-ttu-id="868fc-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="868fc-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="868fc-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="868fc-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="868fc-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="868fc-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="868fc-108">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="868fc-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="868fc-109">EcpUrl-tmCreating (POX)</span><span class="sxs-lookup"><span data-stu-id="868fc-109">EcpUrl-tmCreating (POX)</span></span>](ecpurl-tmcreating-pox.md)
  
```XML
<EcpUrl-tmCreating/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="868fc-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="868fc-110">Attributes and elements</span></span>

<span data-ttu-id="868fc-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="868fc-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="868fc-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="868fc-112">Attributes</span></span>

<span data-ttu-id="868fc-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="868fc-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="868fc-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="868fc-114">Child elements</span></span>

<span data-ttu-id="868fc-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="868fc-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="868fc-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="868fc-116">Parent elements</span></span>

|<span data-ttu-id="868fc-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="868fc-117">**Element**</span></span>|<span data-ttu-id="868fc-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="868fc-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="868fc-119">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="868fc-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="868fc-120">Enthält die Spezifikationen für das Verbinden eines Clients mit dem Computer, auf dem Exchange Server ausgeführt wird, auf dem die Clientzugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="868fc-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="868fc-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="868fc-121">Text value</span></span>

<span data-ttu-id="868fc-122">Der Textwert stellt eine partielle URL dar, die mit dem [EcpUrl (POX)](ecpurl-pox.md) -Elementwert kombiniert werden kann, um eine URL zu generieren, die zum Erstellen eines neuen websitepostfachs verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="868fc-122">The text value represents a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to create a new site mailbox.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="868fc-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="868fc-123">Remarks</span></span>

<span data-ttu-id="868fc-124">Das **EcpUrl-tmCreating-** Element ist ein optionales untergeordnetes Element des **Protocol** -Elements.</span><span class="sxs-lookup"><span data-stu-id="868fc-124">The **EcpUrl-tmCreating** element is an optional child element of the **Protocol** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="868fc-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="868fc-125">See also</span></span>



[<span data-ttu-id="868fc-126">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="868fc-126">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

