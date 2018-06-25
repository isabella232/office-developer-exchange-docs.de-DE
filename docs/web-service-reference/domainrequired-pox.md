---
title: Erforderlicher (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 1f26b691-7331-4c7f-a92b-dfcc66c26963
description: Erforderlicher-Element gibt an, ob die Domäne für die Authentifizierung erforderlich ist.
ms.openlocfilehash: f314b9d27d1b4ee472d249ec49af1a785ff9ac25
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758088"
---
# <a name="domainrequired-pox"></a><span data-ttu-id="309e7-103">Erforderlicher (POX)</span><span class="sxs-lookup"><span data-stu-id="309e7-103">DomainRequired (POX)</span></span>

<span data-ttu-id="309e7-104">**Erforderlicher** -Element gibt an, ob die Domäne für die Authentifizierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="309e7-104">The **DomainRequired** element indicates whether the domain is required for authentication.</span></span> 
  
- [<span data-ttu-id="309e7-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="309e7-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)  
- [<span data-ttu-id="309e7-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="309e7-106">Response (POX)</span></span>](response-pox.md) 
- [<span data-ttu-id="309e7-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="309e7-107">Account (POX)</span></span>](account-pox.md)  
- [<span data-ttu-id="309e7-108">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="309e7-108">Protocol (POX)</span></span>](protocol-pox.md)  
- [<span data-ttu-id="309e7-109">Erforderlicher (POX)</span><span class="sxs-lookup"><span data-stu-id="309e7-109">DomainRequired (POX)</span></span>](domainrequired-pox.md)
  
```xml
<DomainRequired>on or off</DomainRequired>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="309e7-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="309e7-110">Attributes and elements</span></span>

<span data-ttu-id="309e7-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="309e7-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="309e7-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="309e7-112">Attributes</span></span>

<span data-ttu-id="309e7-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="309e7-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="309e7-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="309e7-114">Child elements</span></span>

<span data-ttu-id="309e7-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="309e7-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="309e7-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="309e7-116">Parent elements</span></span>

|<span data-ttu-id="309e7-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="309e7-117">**Element**</span></span>|<span data-ttu-id="309e7-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="309e7-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="309e7-119">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="309e7-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="309e7-120">Enthält die Spezifikationen für die Verbindung eines Clients mit dem Computer, auf der Microsoft Exchange Server 2007 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="309e7-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="309e7-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="309e7-121">Text value</span></span>

<span data-ttu-id="309e7-122">Der Textwert gibt an, ob die Domäne für die Authentifizierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="309e7-122">The text value indicates whether the domain is required for authentication.</span></span> <span data-ttu-id="309e7-123">Die möglichen Werte sind **aktiviert** und **deaktiviert**.</span><span class="sxs-lookup"><span data-stu-id="309e7-123">The possible values are **on** and **off**.</span></span> <span data-ttu-id="309e7-124">Ist der Wert **auf**, muss die nachfolgende Anforderung die Domäne für das Konto des Benutzers enthalten.</span><span class="sxs-lookup"><span data-stu-id="309e7-124">If the value is **on**, the subsequent request must contain the domain of the user's account.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="309e7-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="309e7-125">Remarks</span></span>

<span data-ttu-id="309e7-126">Wenn die Domäne in die [LoginName (POX)](loginname-pox.md) Element nicht angegeben ist oder das **LoginName** -Element nicht angegeben wurde, muss der Benutzer die Domäne eingeben, bevor die Authentifizierung erfolgreich ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="309e7-126">If the domain is not specified in the [LoginName (POX)](loginname-pox.md) element, or the **LoginName** element was not specified, the user must enter the domain before authentication will succeed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="309e7-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="309e7-127">See also</span></span>

- [<span data-ttu-id="309e7-128">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="309e7-128">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

