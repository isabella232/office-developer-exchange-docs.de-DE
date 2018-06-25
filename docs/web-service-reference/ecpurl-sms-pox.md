---
title: EcpUrl-Sms (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5e5e589-ee16-42a8-9cd4-ae3909fc869b
description: Das EcpUrl-Sms-Element gibt eine partielle URL, die mit dem EcpUrl (POX) Elementwert generiert eine URL, die verwendet werden können, auf Short Message Service (SMS) die Einstellungen für einen e-Mail-aktivierten Benutzer zugreifen kombiniert werden kann.
ms.openlocfilehash: 38471db7b7e046e43425b132b1716033c1c96afd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758126"
---
# <a name="ecpurl-sms-pox"></a><span data-ttu-id="722aa-103">EcpUrl-Sms (POX)</span><span class="sxs-lookup"><span data-stu-id="722aa-103">EcpUrl-sms (POX)</span></span>

<span data-ttu-id="722aa-104">Das **EcpUrl-Sms** -Element gibt eine partielle URL, die mit dem [EcpUrl (POX)](ecpurl-pox.md) Elementwert generiert eine URL, die verwendet werden können, auf Short Message Service (SMS) die Einstellungen für einen e-Mail-aktivierten Benutzer zugreifen kombiniert werden kann.</span><span class="sxs-lookup"><span data-stu-id="722aa-104">The **EcpUrl-sms** element specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access Short Message Service (SMS) settings for a mail-enabled user.</span></span> 
  
[<span data-ttu-id="722aa-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="722aa-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="722aa-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="722aa-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="722aa-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="722aa-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="722aa-108">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="722aa-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="722aa-109">EcpUrl-Sms (POX)</span><span class="sxs-lookup"><span data-stu-id="722aa-109">EcpUrl-sms (POX)</span></span>](ecpurl-sms-pox.md)
  
```XML
<EcpUrl-sms/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="722aa-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="722aa-110">Attributes and elements</span></span>

<span data-ttu-id="722aa-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="722aa-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="722aa-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="722aa-112">Attributes</span></span>

<span data-ttu-id="722aa-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="722aa-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="722aa-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="722aa-114">Child elements</span></span>

<span data-ttu-id="722aa-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="722aa-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="722aa-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="722aa-116">Parent elements</span></span>

|<span data-ttu-id="722aa-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="722aa-117">**Element**</span></span>|<span data-ttu-id="722aa-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="722aa-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="722aa-119">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="722aa-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="722aa-120">Enthält die Spezifikationen für die Verbindung eines Clients mit dem Computer, auf der Microsoft Exchange Server ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="722aa-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="722aa-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="722aa-121">Text value</span></span>

<span data-ttu-id="722aa-122">Der Textwert stellt eine partielle URL, die mit dem [EcpUrl (POX)](ecpurl-pox.md) Elementwert generiert eine URL, die verwendet werden können, für den SMS-Einstellungen für den Benutzer Zugriff auf kombiniert werden kann.</span><span class="sxs-lookup"><span data-stu-id="722aa-122">The text value represents a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access SMS settings for the user.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="722aa-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="722aa-123">Remarks</span></span>

<span data-ttu-id="722aa-124">Das **EcpUrl-Sms** -Element ist ein optionales untergeordnetes Element des **Protokoll** -Elements.</span><span class="sxs-lookup"><span data-stu-id="722aa-124">The **EcpUrl-sms** element is an optional child element of the **Protocol** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="722aa-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="722aa-125">See also</span></span>



[<span data-ttu-id="722aa-126">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="722aa-126">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

