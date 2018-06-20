---
title: "\"Ewsurl\" (POX)"
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 73cebc8c-770a-4f1b-b93e-51e7e2f3e342
description: Das Element "ewsurl" gibt die URL der besten Endpunktinstanz für die Exchange-Webdienste (EWS) für einen e-Mail-aktivierten Benutzer.
ms.openlocfilehash: c968b13a069cdc15803c1eb491244b4dc1aa422f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758294"
---
# <a name="ewsurl-pox"></a><span data-ttu-id="c1416-103">"Ewsurl" (POX)</span><span class="sxs-lookup"><span data-stu-id="c1416-103">EwsUrl (POX)</span></span>

<span data-ttu-id="c1416-104">Das Element **"ewsurl"** gibt die URL der besten Endpunktinstanz für die Exchange-Webdienste (EWS) für einen e-Mail-aktivierten Benutzer.</span><span class="sxs-lookup"><span data-stu-id="c1416-104">The **EwsUrl** element specifies the URL of the best endpoint instance for Exchange Web Services (EWS) for a mail-enabled user.</span></span> 
  
[<span data-ttu-id="c1416-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="c1416-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="c1416-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="c1416-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="c1416-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="c1416-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="c1416-108">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="c1416-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="c1416-109">"Ewsurl" (POX)</span><span class="sxs-lookup"><span data-stu-id="c1416-109">EwsUrl (POX)</span></span>](ewsurl-pox.md)
  
```XML
<EwsUrl/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="c1416-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c1416-110">Attributes and elements</span></span>

<span data-ttu-id="c1416-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c1416-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c1416-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="c1416-112">Attributes</span></span>

<span data-ttu-id="c1416-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="c1416-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c1416-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c1416-114">Child elements</span></span>

<span data-ttu-id="c1416-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="c1416-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c1416-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c1416-116">Parent elements</span></span>

|<span data-ttu-id="c1416-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="c1416-117">**Element**</span></span>|<span data-ttu-id="c1416-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c1416-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c1416-119">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="c1416-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="c1416-120">Enthält die Spezifikationen für die Verbindung eines Clients mit dem Computer, auf der Microsoft Exchange Server ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="c1416-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c1416-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="c1416-121">Text value</span></span>

<span data-ttu-id="c1416-122">Der Textwert stellt die URL des EWS-Endpunkts für den Benutzer.</span><span class="sxs-lookup"><span data-stu-id="c1416-122">The text value represents the URL of the EWS endpoint for the user.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c1416-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c1416-123">Remarks</span></span>

<span data-ttu-id="c1416-124">Das Element **"ewsurl"** ist ein optionales untergeordnetes Element des **Protokoll** -Elements.</span><span class="sxs-lookup"><span data-stu-id="c1416-124">The **EwsUrl** element is an optional child element of the **Protocol** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c1416-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c1416-125">See also</span></span>



[<span data-ttu-id="c1416-126">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="c1416-126">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

