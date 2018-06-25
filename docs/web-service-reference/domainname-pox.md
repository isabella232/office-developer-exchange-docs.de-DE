---
title: DomainName (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 2b4af2b2-58b5-4f28-9cb3-c07a11377747
description: Das DomainName-Element gibt die Domäne des Benutzers an.
ms.openlocfilehash: c38d2e470bd174ab6dd7e5e1dd3eee23daea5e69
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758092"
---
# <a name="domainname-pox"></a><span data-ttu-id="5804c-103">DomainName (POX)</span><span class="sxs-lookup"><span data-stu-id="5804c-103">DomainName (POX)</span></span>

<span data-ttu-id="5804c-104">Das **DomainName** -Element gibt die Domäne des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="5804c-104">The **DomainName** element specifies the user's domain.</span></span> 
  
- [<span data-ttu-id="5804c-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="5804c-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)  
- [<span data-ttu-id="5804c-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="5804c-106">Response (POX)</span></span>](response-pox.md)  
- [<span data-ttu-id="5804c-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="5804c-107">Account (POX)</span></span>](account-pox.md) 
- [<span data-ttu-id="5804c-108">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="5804c-108">Protocol (POX)</span></span>](protocol-pox.md) 
- [<span data-ttu-id="5804c-109">DomainName (POX)</span><span class="sxs-lookup"><span data-stu-id="5804c-109">DomainName (POX)</span></span>](domainname-pox.md)
  
```xml
<DomainName/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="5804c-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="5804c-110">Attributes and elements</span></span>

<span data-ttu-id="5804c-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="5804c-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5804c-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="5804c-112">Attributes</span></span>

<span data-ttu-id="5804c-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="5804c-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5804c-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5804c-114">Child elements</span></span>

<span data-ttu-id="5804c-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="5804c-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5804c-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5804c-116">Parent elements</span></span>

|<span data-ttu-id="5804c-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="5804c-117">**Element**</span></span>|<span data-ttu-id="5804c-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5804c-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5804c-119">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="5804c-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="5804c-120">Enthält die Spezifikationen für die Verbindung eines Clients mit dem Computer, auf der Microsoft Exchange Server 2007 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="5804c-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5804c-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="5804c-121">Text value</span></span>

<span data-ttu-id="5804c-122">Der Textwert gibt die Domäne des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="5804c-122">The text value specifies the user's domain.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5804c-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5804c-123">Remarks</span></span>

<span data-ttu-id="5804c-124">Wenn kein Wert angegeben ist, wird die Standardauthentifizierung die E-mail-Adresse als ein Benutzer Benutzerprinzipalnamens (UPN) Format verwenden.</span><span class="sxs-lookup"><span data-stu-id="5804c-124">If no value is specified, the default authentication is to use the e-mail address as a user principal name (UPN) format.</span></span> <span data-ttu-id="5804c-125">Beispiel: \<Username\>@\<Domäne\>.</span><span class="sxs-lookup"><span data-stu-id="5804c-125">For example: \<Username\>@\<Domain\>.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5804c-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5804c-126">See also</span></span>

- [<span data-ttu-id="5804c-127">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="5804c-127">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

