---
title: EwsPartnerUrl (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2ebae21c-3efa-4239-9b49-4a3a8871449b
description: Das EwsPartnerUrl-Element gibt die URL der besten Endpunktinstanz für die Exchange-Webdienste (EWS) für einen e-Mail-aktivierten Benutzer.
ms.openlocfilehash: 97c33e1fed4adc8a9e8542d85e67c942118f6096
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758298"
---
# <a name="ewspartnerurl-pox"></a><span data-ttu-id="b6bfc-103">EwsPartnerUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="b6bfc-103">EwsPartnerUrl (POX)</span></span>

<span data-ttu-id="b6bfc-104">Das **EwsPartnerUrl** -Element gibt die URL der besten Endpunktinstanz für die Exchange-Webdienste (EWS) für einen e-Mail-aktivierten Benutzer.</span><span class="sxs-lookup"><span data-stu-id="b6bfc-104">The **EwsPartnerUrl** element specifies the URL of the best endpoint instance for Exchange Web Services (EWS) for a mail-enabled user.</span></span> 
  
[<span data-ttu-id="b6bfc-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="b6bfc-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="b6bfc-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="b6bfc-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="b6bfc-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="b6bfc-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="b6bfc-108">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="b6bfc-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="b6bfc-109">EwsPartnerUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="b6bfc-109">EwsPartnerUrl (POX)</span></span>](ewspartnerurl-pox.md)
  
```XML
<EwsPartnerUrl/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="b6bfc-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b6bfc-110">Attributes and elements</span></span>

<span data-ttu-id="b6bfc-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b6bfc-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b6bfc-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="b6bfc-112">Attributes</span></span>

<span data-ttu-id="b6bfc-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="b6bfc-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b6bfc-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b6bfc-114">Child elements</span></span>

<span data-ttu-id="b6bfc-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="b6bfc-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b6bfc-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b6bfc-116">Parent elements</span></span>

|<span data-ttu-id="b6bfc-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="b6bfc-117">**Element**</span></span>|<span data-ttu-id="b6bfc-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b6bfc-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b6bfc-119">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="b6bfc-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="b6bfc-120">Enthält die Spezifikationen für die Verbindung eines Clients mit dem Computer, auf der Microsoft Exchange Server ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="b6bfc-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b6bfc-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="b6bfc-121">Text value</span></span>

<span data-ttu-id="b6bfc-122">Der Textwert stellt die URL des EWS-Endpunkts für den Benutzer.</span><span class="sxs-lookup"><span data-stu-id="b6bfc-122">The text value represents the URL of the EWS endpoint for the user.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b6bfc-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b6bfc-123">Remarks</span></span>

<span data-ttu-id="b6bfc-124">Das **EwsPartnerUrl** -Element ist ein optionales untergeordnetes Element des **Protokoll** -Elements.</span><span class="sxs-lookup"><span data-stu-id="b6bfc-124">The **EwsPartnerUrl** element is an optional child element of the **Protocol** element.</span></span> <span data-ttu-id="b6bfc-125">Dies entspricht dem Element ["Ewsurl" (POX)](ewsurl-pox.md) .</span><span class="sxs-lookup"><span data-stu-id="b6bfc-125">It is equivalent to the [EwsUrl (POX)](ewsurl-pox.md) element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b6bfc-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b6bfc-126">See also</span></span>



[<span data-ttu-id="b6bfc-127">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="b6bfc-127">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

