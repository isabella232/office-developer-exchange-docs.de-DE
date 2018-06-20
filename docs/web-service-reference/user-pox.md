---
title: Benutzer (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 7c42b516-77f6-4aee-99d8-b866d82d793a
description: Das Element enthält benutzerspezifische Informationen.
ms.openlocfilehash: 3f90ff0cc00170170c7304f2a19fe1d7abd9d1bc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839432"
---
# <a name="user-pox"></a><span data-ttu-id="b3165-103">Benutzer (POX)</span><span class="sxs-lookup"><span data-stu-id="b3165-103">User (POX)</span></span>

<span data-ttu-id="b3165-104">**Das Element** enthält benutzerspezifische Informationen.</span><span class="sxs-lookup"><span data-stu-id="b3165-104">The **User** element provides user-specific information.</span></span> 
  
[<span data-ttu-id="b3165-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="b3165-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="b3165-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="b3165-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="b3165-107">Benutzer (POX)</span><span class="sxs-lookup"><span data-stu-id="b3165-107">User (POX)</span></span>](user-pox.md)
  
```xml
<User>
   <DisplayName/>
   <LegacyDN/>
   <DeploymentId/>
   <AutoDiscoverSMTPAddress/>
</User>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="b3165-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b3165-108">Attributes and elements</span></span>

<span data-ttu-id="b3165-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b3165-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b3165-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="b3165-110">Attributes</span></span>

<span data-ttu-id="b3165-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="b3165-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b3165-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b3165-112">Child elements</span></span>

|<span data-ttu-id="b3165-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="b3165-113">**Element**</span></span>|<span data-ttu-id="b3165-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b3165-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b3165-115">DisplayName (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="b3165-115">DisplayName (string)</span></span>](displayname-string.md) <br/> |<span data-ttu-id="b3165-116">Anzeigenamen des Benutzers darstellt.</span><span class="sxs-lookup"><span data-stu-id="b3165-116">Represents the user's display name.</span></span>  <br/> |
|[<span data-ttu-id="b3165-117">LegacyDN (POX)</span><span class="sxs-lookup"><span data-stu-id="b3165-117">LegacyDN (POX)</span></span>](legacydn-pox.md) <br/> |<span data-ttu-id="b3165-118">Postfach eines Benutzers identifiziert anhand der legacy-DN.</span><span class="sxs-lookup"><span data-stu-id="b3165-118">Identifies a user's mailbox by legacy distinguished name.</span></span>  <br/> |
|[<span data-ttu-id="b3165-119">DeploymentId (POX)</span><span class="sxs-lookup"><span data-stu-id="b3165-119">DeploymentId (POX)</span></span>](deploymentid-pox.md) <br/> |<span data-ttu-id="b3165-120">Die Exchange-Gesamtstruktur identifiziert eindeutig.</span><span class="sxs-lookup"><span data-stu-id="b3165-120">Uniquely identifies the Exchange forest.</span></span>  <br/> |
|[<span data-ttu-id="b3165-121">AutoDiscoverSMTPAddress (POX)</span><span class="sxs-lookup"><span data-stu-id="b3165-121">AutoDiscoverSMTPAddress (POX)</span></span>](autodiscoversmtpaddress-pox.md) <br/> |<span data-ttu-id="b3165-122">Enthält die SMTP-Adresse des Benutzers, die für die AutoErmittlung-Prozesses verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b3165-122">Contains the user's SMTP address that is used for the Autodiscover process.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b3165-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b3165-123">Parent elements</span></span>

|<span data-ttu-id="b3165-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="b3165-124">**Element**</span></span>|<span data-ttu-id="b3165-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b3165-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b3165-126">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="b3165-126">Response (POX)</span></span>](response-pox.md) <br/> |<span data-ttu-id="b3165-127">Enthält die Antwort vom AutoErmittlungsdienst.</span><span class="sxs-lookup"><span data-stu-id="b3165-127">Contains the response from the Autodiscover service.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b3165-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b3165-128">Remarks</span></span>

<span data-ttu-id="b3165-129">AutoErmittlung-Anforderungen und-Antworten müssen UTF-8 codiert sein.</span><span class="sxs-lookup"><span data-stu-id="b3165-129">Autodiscover requests and responses must be UTF-8 encoded.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b3165-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b3165-130">See also</span></span>



[<span data-ttu-id="b3165-131">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="b3165-131">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

