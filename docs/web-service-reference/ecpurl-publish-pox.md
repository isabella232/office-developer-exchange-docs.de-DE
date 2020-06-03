---
title: EcpUrl-Publish (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a51189db-f6e5-428d-833d-65a209204a5b
description: Das EcpUrl-Publish-Element gibt eine partielle URL an, die mit dem Wert des EcpUrl (POX)-Elements kombiniert werden kann, um eine URL zu generieren, die für den Zugriff auf die Kalender Veröffentlichungseinstellungen für einen e-Mail-aktivierten Benutzer verwendet werden kann.
ms.openlocfilehash: 98cac9132c1ba6e368be6337fbf3b522a02cb47a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458005"
---
# <a name="ecpurl-publish-pox"></a><span data-ttu-id="60a01-103">EcpUrl-Publish (POX)</span><span class="sxs-lookup"><span data-stu-id="60a01-103">EcpUrl-publish (POX)</span></span>

<span data-ttu-id="60a01-104">Das **EcpUrl-Publish-** Element gibt eine partielle URL an, die mit dem Wert des [EcpUrl (POX)](ecpurl-pox.md) -Elements kombiniert werden kann, um eine URL zu generieren, die für den Zugriff auf die Kalender Veröffentlichungseinstellungen für einen e-Mail-aktivierten Benutzer verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="60a01-104">The **EcpUrl-publish** element specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access calendar publishing settings for a mail-enabled user.</span></span> 
  
[<span data-ttu-id="60a01-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="60a01-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="60a01-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="60a01-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="60a01-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="60a01-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="60a01-108">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="60a01-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="60a01-109">EcpUrl-Publish (POX)</span><span class="sxs-lookup"><span data-stu-id="60a01-109">EcpUrl-publish (POX)</span></span>](ecpurl-publish-pox.md)
  
```XML
<EcpUrl-publish/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="60a01-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="60a01-110">Attributes and elements</span></span>

<span data-ttu-id="60a01-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="60a01-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="60a01-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="60a01-112">Attributes</span></span>

<span data-ttu-id="60a01-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="60a01-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="60a01-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="60a01-114">Child elements</span></span>

<span data-ttu-id="60a01-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="60a01-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="60a01-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="60a01-116">Parent elements</span></span>

|<span data-ttu-id="60a01-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="60a01-117">**Element**</span></span>|<span data-ttu-id="60a01-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="60a01-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="60a01-119">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="60a01-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="60a01-120">Enthält die Spezifikationen für das Verbinden eines Clients mit dem Computer, auf dem Exchange Server ausgeführt wird, auf dem die Clientzugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="60a01-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="60a01-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="60a01-121">Text value</span></span>

<span data-ttu-id="60a01-122">Der Textwert stellt eine partielle URL dar, die mit dem [EcpUrl (POX)](ecpurl-pox.md) -Elementwert kombiniert werden kann, um eine URL zu generieren, die für den Zugriff auf die Kalender Veröffentlichungseinstellungen für den Benutzer verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="60a01-122">The text value represents a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access calendar publishing settings for the user.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="60a01-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="60a01-123">Remarks</span></span>

<span data-ttu-id="60a01-124">Das **EcpUrl-Publish-** Element ist ein optionales untergeordnetes Element des **Protocol** -Elements.</span><span class="sxs-lookup"><span data-stu-id="60a01-124">The **EcpUrl-publish** element is an optional child element of the **Protocol** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="60a01-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="60a01-125">See also</span></span>



[<span data-ttu-id="60a01-126">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="60a01-126">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

