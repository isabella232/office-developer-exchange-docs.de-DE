---
title: EmwsUrl (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: cad0fa91-8d75-4dde-a484-518c837ae063
description: Das EmwsUrl-Element gibt die URL der besten Endpunktinstanz für die Exchange-Webdienste (EWS) für einen e-Mail-aktivierten Benutzer.
ms.openlocfilehash: d8905d098c9978c3413f67e9a1b2443a52fb0d1f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758212"
---
# <a name="emwsurl-pox"></a><span data-ttu-id="82ec9-103">EmwsUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="82ec9-103">EmwsUrl (POX)</span></span>

<span data-ttu-id="82ec9-104">Das **EmwsUrl** -Element gibt die URL der besten Endpunktinstanz für die Exchange-Webdienste (EWS) für einen e-Mail-aktivierten Benutzer.</span><span class="sxs-lookup"><span data-stu-id="82ec9-104">The **EmwsUrl** element specifies the URL of the best endpoint instance for Exchange Web Services (EWS) for a mail-enabled user.</span></span> 
  
- [<span data-ttu-id="82ec9-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="82ec9-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md) 
- [<span data-ttu-id="82ec9-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="82ec9-106">Response (POX)</span></span>](response-pox.md) 
- [<span data-ttu-id="82ec9-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="82ec9-107">Account (POX)</span></span>](account-pox.md) 
- [<span data-ttu-id="82ec9-108">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="82ec9-108">Protocol (POX)</span></span>](protocol-pox.md) 
- [<span data-ttu-id="82ec9-109">EmwsUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="82ec9-109">EmwsUrl (POX)</span></span>](emwsurl-pox.md)
  
```XML
<EmwsUrl/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="82ec9-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="82ec9-110">Attributes and elements</span></span>

<span data-ttu-id="82ec9-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="82ec9-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="82ec9-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="82ec9-112">Attributes</span></span>

<span data-ttu-id="82ec9-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="82ec9-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="82ec9-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="82ec9-114">Child elements</span></span>

<span data-ttu-id="82ec9-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="82ec9-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="82ec9-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="82ec9-116">Parent elements</span></span>

|<span data-ttu-id="82ec9-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="82ec9-117">**Element**</span></span>|<span data-ttu-id="82ec9-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="82ec9-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="82ec9-119">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="82ec9-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="82ec9-120">Enthält die Spezifikationen für die Verbindung eines Clients mit dem Computer, auf der Microsoft Exchange Server ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="82ec9-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="82ec9-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="82ec9-121">Text value</span></span>

<span data-ttu-id="82ec9-122">Der Textwert stellt die URL des EWS-Endpunkts für den Benutzer.</span><span class="sxs-lookup"><span data-stu-id="82ec9-122">The text value represents the URL of the EWS endpoint for the user.</span></span> <span data-ttu-id="82ec9-123">Dies entspricht dem Element ["Ewsurl" (POX)](ewsurl-pox.md) .</span><span class="sxs-lookup"><span data-stu-id="82ec9-123">It is equivalent to the [EwsUrl (POX)](ewsurl-pox.md) element.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="82ec9-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="82ec9-124">Remarks</span></span>

<span data-ttu-id="82ec9-125">Das **EmwsUrl** -Element ist ein optionales untergeordnetes Element des **Protokoll** -Elements.</span><span class="sxs-lookup"><span data-stu-id="82ec9-125">The **EmwsUrl** element is an optional child element of the **Protocol** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="82ec9-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="82ec9-126">See also</span></span>

- [<span data-ttu-id="82ec9-127">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="82ec9-127">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

