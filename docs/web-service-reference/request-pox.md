---
title: Anforderung (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: da54eb32-7ce5-4384-9893-255a2243a959
description: Das angeforderte Element enthält die Anforderung an den AutoErmittlungsdienst.
ms.openlocfilehash: 3f5d5258a92840fe79c4936370323b78aa4715b3
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2018
ms.locfileid: "21354428"
---
# <a name="request-pox"></a><span data-ttu-id="65073-103">Anforderung (POX)</span><span class="sxs-lookup"><span data-stu-id="65073-103">Request (POX)</span></span>

<span data-ttu-id="65073-104">Das **angeforderte** Element enthält die Anforderung an den AutoErmittlungsdienst.</span><span class="sxs-lookup"><span data-stu-id="65073-104">The **Request** element contains the request to the Autodiscover service.</span></span> 
  
- [<span data-ttu-id="65073-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="65073-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md) 
- [<span data-ttu-id="65073-106">Anforderung (POX)</span><span class="sxs-lookup"><span data-stu-id="65073-106">Request (POX)</span></span>](request-pox.md)
  
```xml
<Request>
   <AcceptableResponseSchema/>
   <EMailAddress/>
</Request>
```

```xml
<Request>
   <AcceptableResponseSchema/> 
   <LegacyDN/>
</Request>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="65073-107">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="65073-107">Attributes and elements</span></span>

<span data-ttu-id="65073-108">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="65073-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="65073-109">Attribute</span><span class="sxs-lookup"><span data-stu-id="65073-109">Attributes</span></span>

<span data-ttu-id="65073-110">Keine.</span><span class="sxs-lookup"><span data-stu-id="65073-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="65073-111">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="65073-111">Child elements</span></span>

|<span data-ttu-id="65073-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="65073-112">**Element**</span></span>|<span data-ttu-id="65073-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="65073-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="65073-114">AcceptableResponseSchema (POX)</span><span class="sxs-lookup"><span data-stu-id="65073-114">AcceptableResponseSchema (POX)</span></span>](acceptableresponseschema-pox.md) <br/> |<span data-ttu-id="65073-115">Das Schema für eine Antwort der AutoErmittlung identifiziert.</span><span class="sxs-lookup"><span data-stu-id="65073-115">Identifies the schema for an Autodiscover response.</span></span>  <br/> |
|[<span data-ttu-id="65073-116">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="65073-116">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="65073-117">Identifiziert die e-Mail-Adresse des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="65073-117">Identifies the user's e-mail address.</span></span>  <br/> |
|[<span data-ttu-id="65073-118">LegacyDN (POX)</span><span class="sxs-lookup"><span data-stu-id="65073-118">LegacyDN (POX)</span></span>](legacydn-pox.md) <br/> |<span data-ttu-id="65073-119">Postfach eines Benutzers identifiziert anhand der legacy-DN.</span><span class="sxs-lookup"><span data-stu-id="65073-119">Identifies a user's mailbox by legacy distinguished name.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="65073-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="65073-120">Parent elements</span></span>

|<span data-ttu-id="65073-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="65073-121">**Element**</span></span>|<span data-ttu-id="65073-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="65073-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="65073-123">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="65073-123">AutoDiscover (POX)</span></span>](autodiscover-pox.md) <br/> |<span data-ttu-id="65073-124">Das Stammelement in einer autoermittlungsanforderung für die.</span><span class="sxs-lookup"><span data-stu-id="65073-124">The root element in an Autodiscover request.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="65073-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="65073-125">See also</span></span>

- [<span data-ttu-id="65073-126">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="65073-126">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

