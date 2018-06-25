---
title: DirectoryPort (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: ab436b54-ceba-4cd9-aeb4-134f9b93986d
description: Das DirectoryPort-Element gibt den Port, mit der Netzwerkfirewall auf das Verzeichnis, wenn das Protokoll (NSPI = Name Service Provider Interface) verwendet wird.
ms.openlocfilehash: 1b73b9cd1d21c73f4e897684371993312f741322
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757993"
---
# <a name="directoryport-pox"></a><span data-ttu-id="bd9f4-103">DirectoryPort (POX)</span><span class="sxs-lookup"><span data-stu-id="bd9f4-103">DirectoryPort (POX)</span></span>

<span data-ttu-id="bd9f4-104">Das **DirectoryPort** -Element gibt den Port, mit der Netzwerkfirewall auf das Verzeichnis, wenn das Protokoll (NSPI = Name Service Provider Interface) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bd9f4-104">The **DirectoryPort** element specifies the port that is used to connect to the directory when the Name Service Provider Interface (NSPI) protocol is used.</span></span> 
  
- [<span data-ttu-id="bd9f4-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="bd9f4-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md) 
- [<span data-ttu-id="bd9f4-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="bd9f4-106">Response (POX)</span></span>](response-pox.md)  
- [<span data-ttu-id="bd9f4-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="bd9f4-107">Account (POX)</span></span>](account-pox.md)  
- [<span data-ttu-id="bd9f4-108">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="bd9f4-108">Protocol (POX)</span></span>](protocol-pox.md)  
- [<span data-ttu-id="bd9f4-109">DirectoryPort (POX)</span><span class="sxs-lookup"><span data-stu-id="bd9f4-109">DirectoryPort (POX)</span></span>](directoryport-pox.md)
  
```xml
<DirectoryPort/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="bd9f4-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="bd9f4-110">Attributes and elements</span></span>

<span data-ttu-id="bd9f4-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="bd9f4-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bd9f4-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="bd9f4-112">Attributes</span></span>

<span data-ttu-id="bd9f4-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="bd9f4-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bd9f4-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bd9f4-114">Child elements</span></span>

<span data-ttu-id="bd9f4-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="bd9f4-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="bd9f4-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bd9f4-116">Parent elements</span></span>

|<span data-ttu-id="bd9f4-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="bd9f4-117">**Element**</span></span>|<span data-ttu-id="bd9f4-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bd9f4-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bd9f4-119">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="bd9f4-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="bd9f4-120">Enthält die Spezifikationen für die Verbindung eines Clients mit dem Computer, auf der Microsoft Exchange Server 2007 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="bd9f4-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="bd9f4-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="bd9f4-121">Text value</span></span>

<span data-ttu-id="bd9f4-122">Der Textwert stellt den Port, der Zugriff auf den Exchange-Server verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bd9f4-122">The text value represents the port that is used to access the Exchange server.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bd9f4-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bd9f4-123">Remarks</span></span>

<span data-ttu-id="bd9f4-124">Das **DirectoryPort** -Element wird nur verwendet, wenn das Element [Typ (POX)](type-pox.md) EXCH oder Ausdruck gleich ist.</span><span class="sxs-lookup"><span data-stu-id="bd9f4-124">The **DirectoryPort** element is only used when the [Type (POX)](type-pox.md) element equals EXCH or EXPR.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bd9f4-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bd9f4-125">See also</span></span>

- [<span data-ttu-id="bd9f4-126">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="bd9f4-126">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

