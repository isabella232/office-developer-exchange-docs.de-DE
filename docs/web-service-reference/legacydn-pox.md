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
description: Das LegacyDN-Element identifiziert das Postfach eines Benutzers anhand des Legacy Distinguished Name.
ms.openlocfilehash: b9af4278a5421dc932573396c3563a64a78de41e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526382"
---
# <a name="legacydn-pox"></a><span data-ttu-id="c7e54-103">LegacyDN (POX)</span><span class="sxs-lookup"><span data-stu-id="c7e54-103">LegacyDN (POX)</span></span>

<span data-ttu-id="c7e54-104">Das **LegacyDN** -Element identifiziert das Postfach eines Benutzers anhand des Legacy Distinguished Name.</span><span class="sxs-lookup"><span data-stu-id="c7e54-104">The **LegacyDN** element identifies a user's mailbox by legacy distinguished name.</span></span> 
  
```xml
<LegacyDN/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="c7e54-105">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c7e54-105">Attributes and elements</span></span>

<span data-ttu-id="c7e54-106">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c7e54-106">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c7e54-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="c7e54-107">Attributes</span></span>

<span data-ttu-id="c7e54-108">Keine.</span><span class="sxs-lookup"><span data-stu-id="c7e54-108">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c7e54-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c7e54-109">Child elements</span></span>

<span data-ttu-id="c7e54-110">Keine.</span><span class="sxs-lookup"><span data-stu-id="c7e54-110">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c7e54-111">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c7e54-111">Parent elements</span></span>

|<span data-ttu-id="c7e54-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="c7e54-112">**Element**</span></span>|<span data-ttu-id="c7e54-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c7e54-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c7e54-114">Anforderung (POX)</span><span class="sxs-lookup"><span data-stu-id="c7e54-114">Request (POX)</span></span>](request-pox.md) <br/> |<span data-ttu-id="c7e54-115">Enthält die Anforderung an den AutoErmittlungsdienst.</span><span class="sxs-lookup"><span data-stu-id="c7e54-115">Contains the request to the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="c7e54-116">Benutzer (POX)</span><span class="sxs-lookup"><span data-stu-id="c7e54-116">User (POX)</span></span>](user-pox.md) <br/> |<span data-ttu-id="c7e54-117">Enthält benutzerspezifische Informationen.</span><span class="sxs-lookup"><span data-stu-id="c7e54-117">Provides user-specific information.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c7e54-118">Textwert</span><span class="sxs-lookup"><span data-stu-id="c7e54-118">Text value</span></span>

<span data-ttu-id="c7e54-119">Der Textwert stellt die ältere e-Mail-Adresse eines Benutzers dar.</span><span class="sxs-lookup"><span data-stu-id="c7e54-119">The text value represents a user's legacy e-mail address.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c7e54-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c7e54-120">Remarks</span></span>

<span data-ttu-id="c7e54-121">Das [NonEmptyStringType-Element (Email)](emailaddress-nonemptystringtype.md) ist ein alternatives Element für eine Auto Ermittlungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="c7e54-121">The [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) element is an alternative element for an Autodiscover request.</span></span> <span data-ttu-id="c7e54-122">Sie wird verwendet, wenn ein Postfach auf einem Computer mit Microsoft Exchange Server 2007 vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c7e54-122">It is used when a mailbox exists on a computer that is running Microsoft Exchange Server 2007.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c7e54-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c7e54-123">See also</span></span>

- [<span data-ttu-id="c7e54-124">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="c7e54-124">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

