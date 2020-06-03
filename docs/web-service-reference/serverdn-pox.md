---
title: ServerDN (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 2ef73d13-e8bb-43f6-96c7-3ee157fed739
description: Das ServerDN-Element gibt den DN (Distinguished Name) des Computers an, auf dem Microsoft Exchange Server 2007 ausführt.
ms.openlocfilehash: 16c6e7368e221b7e54c8d7d63532bb29464a7e54
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461996"
---
# <a name="serverdn-pox"></a><span data-ttu-id="e9f2b-103">ServerDN (POX)</span><span class="sxs-lookup"><span data-stu-id="e9f2b-103">ServerDN (POX)</span></span>

<span data-ttu-id="e9f2b-104">Das **ServerDN** -Element gibt den DN (Distinguished Name) des Computers an, auf dem Microsoft Exchange Server 2007 ausführt.</span><span class="sxs-lookup"><span data-stu-id="e9f2b-104">The **ServerDN** element specifies the distinguished name of the computer that is running Microsoft Exchange Server 2007.</span></span> 
  
[<span data-ttu-id="e9f2b-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="e9f2b-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="e9f2b-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="e9f2b-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="e9f2b-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="e9f2b-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="e9f2b-108">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="e9f2b-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="e9f2b-109">ServerDN (POX)</span><span class="sxs-lookup"><span data-stu-id="e9f2b-109">ServerDN (POX)</span></span>](serverdn-pox.md)
  
```xml
<ServerDN/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="e9f2b-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e9f2b-110">Attributes and elements</span></span>

<span data-ttu-id="e9f2b-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e9f2b-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e9f2b-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="e9f2b-112">Attributes</span></span>

<span data-ttu-id="e9f2b-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="e9f2b-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e9f2b-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e9f2b-114">Child elements</span></span>

<span data-ttu-id="e9f2b-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="e9f2b-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e9f2b-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e9f2b-116">Parent elements</span></span>

|<span data-ttu-id="e9f2b-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="e9f2b-117">**Element**</span></span>|<span data-ttu-id="e9f2b-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e9f2b-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e9f2b-119">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="e9f2b-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="e9f2b-120">Enthält die Spezifikationen für das Verbinden eines Clients mit dem Computer, auf dem Microsoft Exchange Server 2007 ausgeführt wird, auf dem die Clientzugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="e9f2b-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e9f2b-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="e9f2b-121">Text value</span></span>

<span data-ttu-id="e9f2b-122">Der Wert Text stellt den Distinguished Name des Exchange-Servers dar.</span><span class="sxs-lookup"><span data-stu-id="e9f2b-122">The text value represents the distinguished name of the Exchange server.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e9f2b-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e9f2b-123">Remarks</span></span>

<span data-ttu-id="e9f2b-124">Der **ServerDN** -Wert wird nur verwendet, wenn [Type (POX)](type-pox.md) gleich dem-Typ ist.</span><span class="sxs-lookup"><span data-stu-id="e9f2b-124">The **ServerDN** value is only used when [Type (POX)](type-pox.md) is equal to EXCH.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e9f2b-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e9f2b-125">See also</span></span>



[<span data-ttu-id="e9f2b-126">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="e9f2b-126">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

