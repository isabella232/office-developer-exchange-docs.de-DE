---
title: EwsPartnerUrl (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2ebae21c-3efa-4239-9b49-4a3a8871449b
description: Das EwsPartnerUrl-Element gibt die URL der besten Endpunkt Instanz für Exchange-Webdienste für einen e-Mail-aktivierten Benutzer an.
ms.openlocfilehash: a67eb17bb3db67a922c53ba5e37900ee0a9b956b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526109"
---
# <a name="ewspartnerurl-pox"></a><span data-ttu-id="4c0b8-103">EwsPartnerUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="4c0b8-103">EwsPartnerUrl (POX)</span></span>

<span data-ttu-id="4c0b8-104">Das **EwsPartnerUrl** -Element gibt die URL der besten Endpunkt Instanz für Exchange-Webdienste für einen e-Mail-aktivierten Benutzer an.</span><span class="sxs-lookup"><span data-stu-id="4c0b8-104">The **EwsPartnerUrl** element specifies the URL of the best endpoint instance for Exchange Web Services (EWS) for a mail-enabled user.</span></span> 
  
[<span data-ttu-id="4c0b8-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="4c0b8-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="4c0b8-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="4c0b8-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="4c0b8-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="4c0b8-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="4c0b8-108">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="4c0b8-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="4c0b8-109">EwsPartnerUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="4c0b8-109">EwsPartnerUrl (POX)</span></span>](ewspartnerurl-pox.md)
  
```XML
<EwsPartnerUrl/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="4c0b8-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="4c0b8-110">Attributes and elements</span></span>

<span data-ttu-id="4c0b8-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="4c0b8-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4c0b8-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="4c0b8-112">Attributes</span></span>

<span data-ttu-id="4c0b8-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="4c0b8-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4c0b8-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4c0b8-114">Child elements</span></span>

<span data-ttu-id="4c0b8-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="4c0b8-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4c0b8-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4c0b8-116">Parent elements</span></span>

|<span data-ttu-id="4c0b8-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="4c0b8-117">**Element**</span></span>|<span data-ttu-id="4c0b8-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4c0b8-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4c0b8-119">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="4c0b8-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="4c0b8-120">Enthält die Spezifikationen für das Verbinden eines Clients mit dem Computer, auf dem Exchange Server ausgeführt wird, auf dem die Clientzugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="4c0b8-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4c0b8-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="4c0b8-121">Text value</span></span>

<span data-ttu-id="4c0b8-122">Der Wert Text stellt die URL des EWS-Endpunkts für den Benutzer dar.</span><span class="sxs-lookup"><span data-stu-id="4c0b8-122">The text value represents the URL of the EWS endpoint for the user.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4c0b8-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4c0b8-123">Remarks</span></span>

<span data-ttu-id="4c0b8-124">Das **EwsPartnerUrl** -Element ist ein optionales untergeordnetes Element des **Protocol** -Elements.</span><span class="sxs-lookup"><span data-stu-id="4c0b8-124">The **EwsPartnerUrl** element is an optional child element of the **Protocol** element.</span></span> <span data-ttu-id="4c0b8-125">Es entspricht dem [EwsUrl (POX)-](ewsurl-pox.md) Element.</span><span class="sxs-lookup"><span data-stu-id="4c0b8-125">It is equivalent to the [EwsUrl (POX)](ewsurl-pox.md) element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4c0b8-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4c0b8-126">See also</span></span>



[<span data-ttu-id="4c0b8-127">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="4c0b8-127">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

