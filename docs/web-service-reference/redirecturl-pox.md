---
title: RedirectUrl (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: c54f310f-8c99-4c37-8e73-ac87722b6229
description: Das RedirectUrl-Element enthält die URL der Computer, auf dem Microsoft Exchange Server 2007 ausgeführt wird, dem die Clientzugriffs-Serverrolle installiert ist, die zum Abrufen der für die AutoErmittlung verwendet werden soll.
ms.openlocfilehash: 3b634f1a3a3d44b6aae1a826a005149200641dcb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831027"
---
# <a name="redirecturl-pox"></a><span data-ttu-id="5eea1-103">RedirectUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="5eea1-103">RedirectUrl (POX)</span></span>

<span data-ttu-id="5eea1-104">Das **RedirectUrl** -Element enthält die URL der Computer, auf dem Microsoft Exchange Server 2007 ausgeführt wird, dem die Clientzugriffs-Serverrolle installiert ist, die zum Abrufen der für die AutoErmittlung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5eea1-104">The **RedirectUrl** element contains the URL of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed that should be used to obtain Autodiscover settings.</span></span> 
  
[<span data-ttu-id="5eea1-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="5eea1-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="5eea1-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="5eea1-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="5eea1-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="5eea1-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="5eea1-108">RedirectUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="5eea1-108">RedirectUrl (POX)</span></span>](redirecturl-pox.md)
  
```xml
<RedirectUrl/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="5eea1-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="5eea1-109">Attributes and elements</span></span>

<span data-ttu-id="5eea1-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="5eea1-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5eea1-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="5eea1-111">Attributes</span></span>

<span data-ttu-id="5eea1-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="5eea1-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5eea1-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5eea1-113">Child elements</span></span>

<span data-ttu-id="5eea1-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="5eea1-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5eea1-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5eea1-115">Parent elements</span></span>

|<span data-ttu-id="5eea1-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="5eea1-116">**Element**</span></span>|<span data-ttu-id="5eea1-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5eea1-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5eea1-118">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="5eea1-118">Account (POX)</span></span>](account-pox.md) <br/> |<span data-ttu-id="5eea1-119">Gibt die kontoeinstellungen für den Benutzer an.</span><span class="sxs-lookup"><span data-stu-id="5eea1-119">Specifies account settings for the user.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5eea1-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="5eea1-120">Text value</span></span>

<span data-ttu-id="5eea1-121">Der Textwert stellt die URL des Clientzugriffsservers, die zum Abrufen der für die AutoErmittlung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5eea1-121">The text value represents the URL of the Client Access server that should be used to obtain Autodiscover settings.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5eea1-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5eea1-122">Remarks</span></span>

<span data-ttu-id="5eea1-123">Die Clientanwendung sollte beenden umleiten nach 10 umleitungen zulässig.</span><span class="sxs-lookup"><span data-stu-id="5eea1-123">The client application should stop redirecting after 10 redirects.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5eea1-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5eea1-124">See also</span></span>



[<span data-ttu-id="5eea1-125">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="5eea1-125">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

