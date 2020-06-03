---
title: Spa (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: fba018d5-0c65-4e1b-9767-d1ce8b356278
description: Das Spa-Element gibt an, ob die sichere Kennwortauthentifizierung (Spa) erforderlich ist.
ms.openlocfilehash: cf57b3a6046b1b9b030b7cae81381189eee92c1c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467641"
---
# <a name="spa-pox"></a><span data-ttu-id="3dd13-103">Spa (POX)</span><span class="sxs-lookup"><span data-stu-id="3dd13-103">SPA (POX)</span></span>

<span data-ttu-id="3dd13-104">Das **Spa** -Element gibt an, ob die sichere Kennwortauthentifizierung (Spa) erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="3dd13-104">The **SPA** element indicates whether Secure Password Authentication (SPA) is required.</span></span> 
  
[<span data-ttu-id="3dd13-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="3dd13-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="3dd13-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="3dd13-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="3dd13-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="3dd13-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="3dd13-108">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="3dd13-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="3dd13-109">Spa (POX)</span><span class="sxs-lookup"><span data-stu-id="3dd13-109">SPA (POX)</span></span>](spa-pox.md)
  
```xml
<SPA/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="3dd13-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3dd13-110">Attributes and elements</span></span>

<span data-ttu-id="3dd13-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="3dd13-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3dd13-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="3dd13-112">Attributes</span></span>

<span data-ttu-id="3dd13-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="3dd13-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3dd13-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3dd13-114">Child elements</span></span>

<span data-ttu-id="3dd13-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="3dd13-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3dd13-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3dd13-116">Parent elements</span></span>

|<span data-ttu-id="3dd13-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="3dd13-117">**Element**</span></span>|<span data-ttu-id="3dd13-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3dd13-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3dd13-119">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="3dd13-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="3dd13-120">Enthält die Spezifikationen für das Verbinden eines Clients mit dem Computer, auf dem Microsoft Exchange Server 2007 ausgeführt wird, auf dem die Clientzugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="3dd13-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3dd13-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="3dd13-121">Text value</span></span>

<span data-ttu-id="3dd13-122">Der Textwert gibt an, ob Spa erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="3dd13-122">The text value indicates whether SPA is required.</span></span> <span data-ttu-id="3dd13-123">Wenn der Textwert **on**ist, ist Spa erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3dd13-123">If the text value is **on**, SPA is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3dd13-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3dd13-124">Remarks</span></span>

<span data-ttu-id="3dd13-125">Wenn dieses Element nicht vorhanden ist, wird der Standardwert **auf ein**festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3dd13-125">If this element is not present, the default value is set to **on**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3dd13-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3dd13-126">See also</span></span>



[<span data-ttu-id="3dd13-127">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="3dd13-127">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

