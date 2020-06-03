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
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459546"
---
# <a name="request-pox"></a><span data-ttu-id="ca283-103">Anforderung (POX)</span><span class="sxs-lookup"><span data-stu-id="ca283-103">Request (POX)</span></span>

<span data-ttu-id="ca283-104">Das **Request** -Element enthält die Anforderung an den AutoErmittlungsdienst.</span><span class="sxs-lookup"><span data-stu-id="ca283-104">The **Request** element contains the request to the Autodiscover service.</span></span> 
  
- [<span data-ttu-id="ca283-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="ca283-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md) 
- [<span data-ttu-id="ca283-106">Anforderung (POX)</span><span class="sxs-lookup"><span data-stu-id="ca283-106">Request (POX)</span></span>](request-pox.md)
  
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

## <a name="attributes-and-elements"></a><span data-ttu-id="ca283-107">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ca283-107">Attributes and elements</span></span>

<span data-ttu-id="ca283-108">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ca283-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ca283-109">Attribute</span><span class="sxs-lookup"><span data-stu-id="ca283-109">Attributes</span></span>

<span data-ttu-id="ca283-110">Keine.</span><span class="sxs-lookup"><span data-stu-id="ca283-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ca283-111">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ca283-111">Child elements</span></span>

|<span data-ttu-id="ca283-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="ca283-112">**Element**</span></span>|<span data-ttu-id="ca283-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ca283-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ca283-114">AcceptableResponseSchema (POX)</span><span class="sxs-lookup"><span data-stu-id="ca283-114">AcceptableResponseSchema (POX)</span></span>](acceptableresponseschema-pox.md) <br/> |<span data-ttu-id="ca283-115">Gibt das Schema für eine Auto Ermittlungs Antwort an.</span><span class="sxs-lookup"><span data-stu-id="ca283-115">Identifies the schema for an Autodiscover response.</span></span>  <br/> |
|[<span data-ttu-id="ca283-116">EmailAddress (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="ca283-116">EmailAddress (NonEmptyStringType)</span></span>](emailaddress-nonemptystringtype.md) <br/> |<span data-ttu-id="ca283-117">Gibt die e-Mail-Adresse des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="ca283-117">Identifies the user's e-mail address.</span></span>  <br/> |
|[<span data-ttu-id="ca283-118">LegacyDN (POX)</span><span class="sxs-lookup"><span data-stu-id="ca283-118">LegacyDN (POX)</span></span>](legacydn-pox.md) <br/> |<span data-ttu-id="ca283-119">Identifiziert das Postfach eines Benutzers anhand des Distinguished Name-Legacy namens.</span><span class="sxs-lookup"><span data-stu-id="ca283-119">Identifies a user's mailbox by legacy distinguished name.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ca283-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ca283-120">Parent elements</span></span>

|<span data-ttu-id="ca283-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="ca283-121">**Element**</span></span>|<span data-ttu-id="ca283-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ca283-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ca283-123">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="ca283-123">AutoDiscover (POX)</span></span>](autodiscover-pox.md) <br/> |<span data-ttu-id="ca283-124">Das Stammelement in einer Auto Ermittlungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="ca283-124">The root element in an Autodiscover request.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ca283-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ca283-125">See also</span></span>

- [<span data-ttu-id="ca283-126">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="ca283-126">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

