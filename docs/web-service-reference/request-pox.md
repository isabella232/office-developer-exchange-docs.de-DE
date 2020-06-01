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
description: Das Request-Element enthält die Anforderung an den AutoErmittlungsdienst.
ms.openlocfilehash: bc215d614441ed8f12c0f1490f4abdbb7b574ad0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459546"
---
# <a name="request-pox"></a><span data-ttu-id="e0d07-103">Anforderung (POX)</span><span class="sxs-lookup"><span data-stu-id="e0d07-103">Request (POX)</span></span>

<span data-ttu-id="e0d07-104">Das **Request** -Element enthält die Anforderung an den AutoErmittlungsdienst.</span><span class="sxs-lookup"><span data-stu-id="e0d07-104">The **Request** element contains the request to the Autodiscover service.</span></span> 
  
- [<span data-ttu-id="e0d07-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="e0d07-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md) 
- [<span data-ttu-id="e0d07-106">Anforderung (POX)</span><span class="sxs-lookup"><span data-stu-id="e0d07-106">Request (POX)</span></span>](request-pox.md)
  
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

## <a name="attributes-and-elements"></a><span data-ttu-id="e0d07-107">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e0d07-107">Attributes and elements</span></span>

<span data-ttu-id="e0d07-108">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e0d07-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e0d07-109">Attribute</span><span class="sxs-lookup"><span data-stu-id="e0d07-109">Attributes</span></span>

<span data-ttu-id="e0d07-110">Keine.</span><span class="sxs-lookup"><span data-stu-id="e0d07-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e0d07-111">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e0d07-111">Child elements</span></span>

|<span data-ttu-id="e0d07-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="e0d07-112">**Element**</span></span>|<span data-ttu-id="e0d07-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e0d07-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e0d07-114">AcceptableResponseSchema (POX)</span><span class="sxs-lookup"><span data-stu-id="e0d07-114">AcceptableResponseSchema (POX)</span></span>](acceptableresponseschema-pox.md) <br/> |<span data-ttu-id="e0d07-115">Gibt das Schema für eine Auto Ermittlungs Antwort an.</span><span class="sxs-lookup"><span data-stu-id="e0d07-115">Identifies the schema for an Autodiscover response.</span></span>  <br/> |
|[<span data-ttu-id="e0d07-116">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="e0d07-116">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="e0d07-117">Gibt die e-Mail-Adresse des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="e0d07-117">Identifies the user's e-mail address.</span></span>  <br/> |
|[<span data-ttu-id="e0d07-118">LegacyDN (POX)</span><span class="sxs-lookup"><span data-stu-id="e0d07-118">LegacyDN (POX)</span></span>](legacydn-pox.md) <br/> |<span data-ttu-id="e0d07-119">Identifiziert das Postfach eines Benutzers anhand des Distinguished Name-Legacy namens.</span><span class="sxs-lookup"><span data-stu-id="e0d07-119">Identifies a user's mailbox by legacy distinguished name.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e0d07-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e0d07-120">Parent elements</span></span>

|<span data-ttu-id="e0d07-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="e0d07-121">**Element**</span></span>|<span data-ttu-id="e0d07-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e0d07-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e0d07-123">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="e0d07-123">AutoDiscover (POX)</span></span>](autodiscover-pox.md) <br/> |<span data-ttu-id="e0d07-124">Das Stammelement in einer Auto Ermittlungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="e0d07-124">The root element in an Autodiscover request.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e0d07-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e0d07-125">See also</span></span>

- [<span data-ttu-id="e0d07-126">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="e0d07-126">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

