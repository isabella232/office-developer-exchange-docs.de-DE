---
title: EcpUrl-um (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 455c77c6-c03f-49a7-a8ca-aa0023b6e73b
description: Das EcpUrl-um-Element gibt eine partielle URL an, die mit dem Wert des EcpUrl (POX)-Elements kombiniert werden kann, um eine URL zu generieren, die für den Zugriff auf Voicemaileinstellungen für e-Mail-aktivierte Benutzer verwendet werden kann.
ms.openlocfilehash: 0fa3d42113d7d9accd6bba3d3b065477baf4d484
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463489"
---
# <a name="ecpurl-um-pox"></a><span data-ttu-id="5183e-103">EcpUrl-um (POX)</span><span class="sxs-lookup"><span data-stu-id="5183e-103">EcpUrl-um (POX)</span></span>

<span data-ttu-id="5183e-104">Das **EcpUrl-um-** Element gibt eine partielle URL an, die mit dem Wert des [EcpUrl (POX)](ecpurl-pox.md) -Elements kombiniert werden kann, um eine URL zu generieren, die für den Zugriff auf Voicemaileinstellungen für e-Mail-aktivierte Benutzer verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="5183e-104">The **EcpUrl-um** element specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access voice mail settings for a mail-enabled user.</span></span> 
  
[<span data-ttu-id="5183e-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="5183e-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="5183e-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="5183e-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="5183e-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="5183e-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="5183e-108">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="5183e-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="5183e-109">EcpUrl-um (POX)</span><span class="sxs-lookup"><span data-stu-id="5183e-109">EcpUrl-um (POX)</span></span>](ecpurl-um-pox.md)
  
```XML
<EcpUrl-um/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="5183e-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="5183e-110">Attributes and elements</span></span>

<span data-ttu-id="5183e-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="5183e-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5183e-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="5183e-112">Attributes</span></span>

<span data-ttu-id="5183e-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="5183e-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5183e-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5183e-114">Child elements</span></span>

<span data-ttu-id="5183e-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="5183e-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5183e-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5183e-116">Parent elements</span></span>

|<span data-ttu-id="5183e-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="5183e-117">**Element**</span></span>|<span data-ttu-id="5183e-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5183e-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5183e-119">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="5183e-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="5183e-120">Enthält die Spezifikationen für das Verbinden eines Clients mit dem Computer, auf dem Exchange Server ausgeführt wird, auf dem die Clientzugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="5183e-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5183e-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="5183e-121">Text value</span></span>

<span data-ttu-id="5183e-122">Der Textwert stellt eine partielle URL dar, die mit dem [EcpUrl (POX)](ecpurl-pox.md) -Elementwert kombiniert werden kann, um eine URL zu generieren, die für den Zugriff auf Voicemaileinstellungen für den Benutzer verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="5183e-122">The text value represents a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access voice mail settings for the user.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5183e-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5183e-123">Remarks</span></span>

<span data-ttu-id="5183e-124">Das **EcpUrl-um-** Element ist ein optionales untergeordnetes Element des **Protocol** -Elements.</span><span class="sxs-lookup"><span data-stu-id="5183e-124">The **EcpUrl-um** element is an optional child element of the **Protocol** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5183e-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5183e-125">See also</span></span>



[<span data-ttu-id="5183e-126">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="5183e-126">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

