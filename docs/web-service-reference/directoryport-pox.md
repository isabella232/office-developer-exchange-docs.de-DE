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
description: Das DirectoryPort-Element gibt den Port an, der zum Herstellen einer Verbindung mit dem Verzeichnis verwendet wird, wenn das NSPI-Protokoll (Name Service Provider Interface) verwendet wird.
ms.openlocfilehash: 2ba0a15cea0b4eb9b6069fab384edb3d9747a360
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462087"
---
# <a name="directoryport-pox"></a><span data-ttu-id="7133e-103">DirectoryPort (POX)</span><span class="sxs-lookup"><span data-stu-id="7133e-103">DirectoryPort (POX)</span></span>

<span data-ttu-id="7133e-104">Das **DirectoryPort** -Element gibt den Port an, der zum Herstellen einer Verbindung mit dem Verzeichnis verwendet wird, wenn das NSPI-Protokoll (Name Service Provider Interface) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7133e-104">The **DirectoryPort** element specifies the port that is used to connect to the directory when the Name Service Provider Interface (NSPI) protocol is used.</span></span> 
  
- [<span data-ttu-id="7133e-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="7133e-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md) 
- [<span data-ttu-id="7133e-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="7133e-106">Response (POX)</span></span>](response-pox.md)  
- [<span data-ttu-id="7133e-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="7133e-107">Account (POX)</span></span>](account-pox.md)  
- [<span data-ttu-id="7133e-108">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="7133e-108">Protocol (POX)</span></span>](protocol-pox.md)  
- [<span data-ttu-id="7133e-109">DirectoryPort (POX)</span><span class="sxs-lookup"><span data-stu-id="7133e-109">DirectoryPort (POX)</span></span>](directoryport-pox.md)
  
```xml
<DirectoryPort/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="7133e-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="7133e-110">Attributes and elements</span></span>

<span data-ttu-id="7133e-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="7133e-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7133e-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="7133e-112">Attributes</span></span>

<span data-ttu-id="7133e-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="7133e-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7133e-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7133e-114">Child elements</span></span>

<span data-ttu-id="7133e-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="7133e-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7133e-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7133e-116">Parent elements</span></span>

|<span data-ttu-id="7133e-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="7133e-117">**Element**</span></span>|<span data-ttu-id="7133e-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7133e-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7133e-119">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="7133e-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="7133e-120">Enthält die Spezifikationen für das Verbinden eines Clients mit dem Computer, auf dem Microsoft Exchange Server 2007 ausgeführt wird, auf dem die Clientzugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="7133e-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7133e-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="7133e-121">Text value</span></span>

<span data-ttu-id="7133e-122">Der Wert Text stellt den Port dar, der für den Zugriff auf den Exchange-Server verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7133e-122">The text value represents the port that is used to access the Exchange server.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7133e-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7133e-123">Remarks</span></span>

<span data-ttu-id="7133e-124">Das **DirectoryPort** -Element wird nur verwendet, wenn der [Typ (POX)-](type-pox.md) Element mit dem Wert "$" oder "expr" identisch ist.</span><span class="sxs-lookup"><span data-stu-id="7133e-124">The **DirectoryPort** element is only used when the [Type (POX)](type-pox.md) element equals EXCH or EXPR.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7133e-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7133e-125">See also</span></span>

- [<span data-ttu-id="7133e-126">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="7133e-126">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

