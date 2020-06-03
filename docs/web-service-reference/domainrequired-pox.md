---
title: DomainRequired (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 1f26b691-7331-4c7f-a92b-dfcc66c26963
description: Das DomainRequired-Element gibt an, ob die Domäne für die Authentifizierung erforderlich ist.
ms.openlocfilehash: 97d602c40b247f9a6650cc4440b53bf23c18482e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461324"
---
# <a name="domainrequired-pox"></a><span data-ttu-id="2dc1a-103">DomainRequired (POX)</span><span class="sxs-lookup"><span data-stu-id="2dc1a-103">DomainRequired (POX)</span></span>

<span data-ttu-id="2dc1a-104">Das **DomainRequired** -Element gibt an, ob die Domäne für die Authentifizierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="2dc1a-104">The **DomainRequired** element indicates whether the domain is required for authentication.</span></span> 
  
- [<span data-ttu-id="2dc1a-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="2dc1a-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)  
- [<span data-ttu-id="2dc1a-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="2dc1a-106">Response (POX)</span></span>](response-pox.md) 
- [<span data-ttu-id="2dc1a-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="2dc1a-107">Account (POX)</span></span>](account-pox.md)  
- [<span data-ttu-id="2dc1a-108">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="2dc1a-108">Protocol (POX)</span></span>](protocol-pox.md)  
- [<span data-ttu-id="2dc1a-109">DomainRequired (POX)</span><span class="sxs-lookup"><span data-stu-id="2dc1a-109">DomainRequired (POX)</span></span>](domainrequired-pox.md)
  
```xml
<DomainRequired>on or off</DomainRequired>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="2dc1a-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="2dc1a-110">Attributes and elements</span></span>

<span data-ttu-id="2dc1a-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="2dc1a-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2dc1a-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="2dc1a-112">Attributes</span></span>

<span data-ttu-id="2dc1a-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="2dc1a-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2dc1a-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2dc1a-114">Child elements</span></span>

<span data-ttu-id="2dc1a-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="2dc1a-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2dc1a-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2dc1a-116">Parent elements</span></span>

|<span data-ttu-id="2dc1a-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="2dc1a-117">**Element**</span></span>|<span data-ttu-id="2dc1a-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2dc1a-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2dc1a-119">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="2dc1a-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="2dc1a-120">Enthält die Spezifikationen für das Verbinden eines Clients mit dem Computer, auf dem Microsoft Exchange Server 2007 ausgeführt wird, auf dem die Clientzugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="2dc1a-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2dc1a-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="2dc1a-121">Text value</span></span>

<span data-ttu-id="2dc1a-122">Der Wert Text gibt an, ob die Domäne für die Authentifizierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="2dc1a-122">The text value indicates whether the domain is required for authentication.</span></span> <span data-ttu-id="2dc1a-123">Die möglichen Werte sind **ein** -und **ausgeschaltet**.</span><span class="sxs-lookup"><span data-stu-id="2dc1a-123">The possible values are **on** and **off**.</span></span> <span data-ttu-id="2dc1a-124">Wenn der Wert **auf "on**" festgelegt ist, muss die nachfolgende Anforderung die Domäne des Benutzerkontos enthalten.</span><span class="sxs-lookup"><span data-stu-id="2dc1a-124">If the value is **on**, the subsequent request must contain the domain of the user's account.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2dc1a-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2dc1a-125">Remarks</span></span>

<span data-ttu-id="2dc1a-126">Wenn die Domäne nicht im [LoginName-](loginname-pox.md) Element angegeben ist oder das **LoginName** -Element nicht angegeben wurde, muss der Benutzer die Domäne eingeben, bevor die Authentifizierung erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2dc1a-126">If the domain is not specified in the [LoginName (POX)](loginname-pox.md) element, or the **LoginName** element was not specified, the user must enter the domain before authentication will succeed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2dc1a-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2dc1a-127">See also</span></span>

- [<span data-ttu-id="2dc1a-128">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="2dc1a-128">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

