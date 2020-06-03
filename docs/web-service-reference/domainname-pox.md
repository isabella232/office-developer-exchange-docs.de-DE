---
title: Domänenname (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 2b4af2b2-58b5-4f28-9cb3-c07a11377747
description: Das Domain Name-Element gibt die Domäne des Benutzers an.
ms.openlocfilehash: ff38d6a876e396317dedece0a81a9f9f0db0f587
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458425"
---
# <a name="domainname-pox"></a><span data-ttu-id="82cce-103">Domänenname (POX)</span><span class="sxs-lookup"><span data-stu-id="82cce-103">DomainName (POX)</span></span>

<span data-ttu-id="82cce-104">Das **Domain Name** -Element gibt die Domäne des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="82cce-104">The **DomainName** element specifies the user's domain.</span></span> 
  
- [<span data-ttu-id="82cce-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="82cce-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)  
- [<span data-ttu-id="82cce-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="82cce-106">Response (POX)</span></span>](response-pox.md)  
- [<span data-ttu-id="82cce-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="82cce-107">Account (POX)</span></span>](account-pox.md) 
- [<span data-ttu-id="82cce-108">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="82cce-108">Protocol (POX)</span></span>](protocol-pox.md) 
- [<span data-ttu-id="82cce-109">Domänenname (POX)</span><span class="sxs-lookup"><span data-stu-id="82cce-109">DomainName (POX)</span></span>](domainname-pox.md)
  
```xml
<DomainName/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="82cce-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="82cce-110">Attributes and elements</span></span>

<span data-ttu-id="82cce-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="82cce-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="82cce-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="82cce-112">Attributes</span></span>

<span data-ttu-id="82cce-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="82cce-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="82cce-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="82cce-114">Child elements</span></span>

<span data-ttu-id="82cce-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="82cce-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="82cce-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="82cce-116">Parent elements</span></span>

|<span data-ttu-id="82cce-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="82cce-117">**Element**</span></span>|<span data-ttu-id="82cce-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="82cce-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="82cce-119">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="82cce-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="82cce-120">Enthält die Spezifikationen für das Verbinden eines Clients mit dem Computer, auf dem Microsoft Exchange Server 2007 ausgeführt wird, auf dem die Clientzugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="82cce-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="82cce-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="82cce-121">Text value</span></span>

<span data-ttu-id="82cce-122">Der Wert Text gibt die Domäne des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="82cce-122">The text value specifies the user's domain.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="82cce-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="82cce-123">Remarks</span></span>

<span data-ttu-id="82cce-124">Wenn kein Wert angegeben ist, wird die Standardauthentifizierung verwendet, um die e-Mail-Adresse als Benutzerprinzipalnamen-Format (User Principal Name, UPN) zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="82cce-124">If no value is specified, the default authentication is to use the e-mail address as a user principal name (UPN) format.</span></span> <span data-ttu-id="82cce-125">Beispiel: \<Username\> @ \<Domain\> .</span><span class="sxs-lookup"><span data-stu-id="82cce-125">For example: \<Username\>@\<Domain\>.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="82cce-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="82cce-126">See also</span></span>

- [<span data-ttu-id="82cce-127">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="82cce-127">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

