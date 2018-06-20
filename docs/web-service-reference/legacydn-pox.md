---
title: LegacyDN (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 9fb9529f-52c5-4907-a84b-935b78de16c3
description: Das Element LegacyDN identifiziert Postfach eines Benutzers von legacy-DN.
ms.openlocfilehash: f7ec1dea29a7d3ad6d470ef7812390d179fe1d2a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830243"
---
# <a name="legacydn-pox"></a><span data-ttu-id="cd8eb-103">LegacyDN (POX)</span><span class="sxs-lookup"><span data-stu-id="cd8eb-103">LegacyDN (POX)</span></span>

<span data-ttu-id="cd8eb-104">Das Element **LegacyDN** identifiziert Postfach eines Benutzers von legacy-DN.</span><span class="sxs-lookup"><span data-stu-id="cd8eb-104">The **LegacyDN** element identifies a user's mailbox by legacy distinguished name.</span></span> 
  
```xml
<LegacyDN/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="cd8eb-105">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="cd8eb-105">Attributes and elements</span></span>

<span data-ttu-id="cd8eb-106">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="cd8eb-106">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cd8eb-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="cd8eb-107">Attributes</span></span>

<span data-ttu-id="cd8eb-108">Keine.</span><span class="sxs-lookup"><span data-stu-id="cd8eb-108">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cd8eb-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cd8eb-109">Child elements</span></span>

<span data-ttu-id="cd8eb-110">Keine.</span><span class="sxs-lookup"><span data-stu-id="cd8eb-110">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="cd8eb-111">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cd8eb-111">Parent elements</span></span>

|<span data-ttu-id="cd8eb-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="cd8eb-112">**Element**</span></span>|<span data-ttu-id="cd8eb-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cd8eb-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cd8eb-114">Anforderung (POX)</span><span class="sxs-lookup"><span data-stu-id="cd8eb-114">Request (POX)</span></span>](request-pox.md) <br/> |<span data-ttu-id="cd8eb-115">Enthält die Anforderung an den AutoErmittlungsdienst.</span><span class="sxs-lookup"><span data-stu-id="cd8eb-115">Contains the request to the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="cd8eb-116">Benutzer (POX)</span><span class="sxs-lookup"><span data-stu-id="cd8eb-116">User (POX)</span></span>](user-pox.md) <br/> |<span data-ttu-id="cd8eb-117">Benutzerspezifische Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="cd8eb-117">Provides user-specific information.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="cd8eb-118">Textwert</span><span class="sxs-lookup"><span data-stu-id="cd8eb-118">Text value</span></span>

<span data-ttu-id="cd8eb-119">Der Textwert stellt die ältere e-Mail-Adresse eines Benutzers.</span><span class="sxs-lookup"><span data-stu-id="cd8eb-119">The text value represents a user's legacy e-mail address.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cd8eb-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="cd8eb-120">Remarks</span></span>

<span data-ttu-id="cd8eb-121">Das Element ["EmailAddress" (NonEmptyStringType)](emailaddress-nonemptystringtype.md) ist ein alternativer Element für eine Anforderung der AutoErmittlung.</span><span class="sxs-lookup"><span data-stu-id="cd8eb-121">The [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) element is an alternative element for an Autodiscover request.</span></span> <span data-ttu-id="cd8eb-122">Es wird verwendet, wenn ein Postfach auf einem Computer vorhanden ist, auf dem Microsoft Exchange Server 2007 ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cd8eb-122">It is used when a mailbox exists on a computer that is running Microsoft Exchange Server 2007.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cd8eb-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cd8eb-123">See also</span></span>

- [<span data-ttu-id="cd8eb-124">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="cd8eb-124">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

