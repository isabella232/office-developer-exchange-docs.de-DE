---
title: DeploymentId (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: b879c134-307e-4645-bb53-55d8ba4fad9c
description: Das Bereitstellungs-Kennungs Element identifiziert die Microsoft Exchange Server 2007 Gesamtstruktur eindeutig.
ms.openlocfilehash: 4986a3404763e88fb3e84d52a5d30d54c810f93a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467921"
---
# <a name="deploymentid-pox"></a><span data-ttu-id="bc850-103">DeploymentId (POX)</span><span class="sxs-lookup"><span data-stu-id="bc850-103">DeploymentId (POX)</span></span>

<span data-ttu-id="bc850-104">Das **Bereitstellungs** -Kennungs Element identifiziert die Microsoft Exchange Server 2007 Gesamtstruktur eindeutig.</span><span class="sxs-lookup"><span data-stu-id="bc850-104">The **DeploymentId** element uniquely identifies the Microsoft Exchange Server 2007 forest.</span></span> 
  
- [<span data-ttu-id="bc850-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="bc850-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)  
- [<span data-ttu-id="bc850-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="bc850-106">Response (POX)</span></span>](response-pox.md) 
- [<span data-ttu-id="bc850-107">Benutzer (POX)</span><span class="sxs-lookup"><span data-stu-id="bc850-107">User (POX)</span></span>](user-pox.md)  
- [<span data-ttu-id="bc850-108">DeploymentId (POX)</span><span class="sxs-lookup"><span data-stu-id="bc850-108">DeploymentId (POX)</span></span>](deploymentid-pox.md)
  
```xml
<DeploymentId/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="bc850-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="bc850-109">Attributes and elements</span></span>

<span data-ttu-id="bc850-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="bc850-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bc850-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="bc850-111">Attributes</span></span>

<span data-ttu-id="bc850-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="bc850-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bc850-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bc850-113">Child elements</span></span>

<span data-ttu-id="bc850-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="bc850-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="bc850-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bc850-115">Parent elements</span></span>

|<span data-ttu-id="bc850-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="bc850-116">**Element**</span></span>|<span data-ttu-id="bc850-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bc850-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bc850-118">Benutzer (POX)</span><span class="sxs-lookup"><span data-stu-id="bc850-118">User (POX)</span></span>](user-pox.md) <br/> |<span data-ttu-id="bc850-119">Enthält benutzerspezifische Informationen.</span><span class="sxs-lookup"><span data-stu-id="bc850-119">Provides user-specific information.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="bc850-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="bc850-120">Text value</span></span>

<span data-ttu-id="bc850-121">Der Textwert identifiziert die Exchange 2007 Gesamtstruktur im GUID-Format eindeutig.</span><span class="sxs-lookup"><span data-stu-id="bc850-121">The text value uniquely identifies the Exchange 2007 forest in GUID format.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bc850-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bc850-122">Remarks</span></span>

<span data-ttu-id="bc850-123">Wenn Sie Exchange 2007 deinstallieren und anschließend neu installieren und denselben Servernamen verwenden, ändert sich der Wert der **Bereitstellungs** -Nr.</span><span class="sxs-lookup"><span data-stu-id="bc850-123">If you uninstall and then reinstall Exchange 2007 and you use the same server name, the **DeploymentId** value changes.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bc850-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bc850-124">See also</span></span>

- [<span data-ttu-id="bc850-125">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="bc850-125">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

