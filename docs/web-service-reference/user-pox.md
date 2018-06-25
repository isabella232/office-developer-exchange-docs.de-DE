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
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839432"
---
# <a name="user-pox"></a><span data-ttu-id="0fe30-103">Benutzer (POX)</span><span class="sxs-lookup"><span data-stu-id="0fe30-103">User (POX)</span></span>

<span data-ttu-id="0fe30-104">**Das Element** enthält benutzerspezifische Informationen.</span><span class="sxs-lookup"><span data-stu-id="0fe30-104">The **User** element provides user-specific information.</span></span> 
  
[<span data-ttu-id="0fe30-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="0fe30-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="0fe30-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="0fe30-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="0fe30-107">Benutzer (POX)</span><span class="sxs-lookup"><span data-stu-id="0fe30-107">User (POX)</span></span>](user-pox.md)
  
```xml
<User>
   <DisplayName/>
   <LegacyDN/>
   <DeploymentId/>
   <AutoDiscoverSMTPAddress/>
</User>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="0fe30-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="0fe30-108">Attributes and elements</span></span>

<span data-ttu-id="0fe30-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="0fe30-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0fe30-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="0fe30-110">Attributes</span></span>

<span data-ttu-id="0fe30-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="0fe30-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0fe30-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0fe30-112">Child elements</span></span>

|<span data-ttu-id="0fe30-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="0fe30-113">**Element**</span></span>|<span data-ttu-id="0fe30-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0fe30-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0fe30-115">DisplayName (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="0fe30-115">DisplayName (string)</span></span>](displayname-string.md) <br/> |<span data-ttu-id="0fe30-116">Anzeigenamen des Benutzers darstellt.</span><span class="sxs-lookup"><span data-stu-id="0fe30-116">Represents the user's display name.</span></span>  <br/> |
|[<span data-ttu-id="0fe30-117">LegacyDN (POX)</span><span class="sxs-lookup"><span data-stu-id="0fe30-117">LegacyDN (POX)</span></span>](legacydn-pox.md) <br/> |<span data-ttu-id="0fe30-118">Postfach eines Benutzers identifiziert anhand der legacy-DN.</span><span class="sxs-lookup"><span data-stu-id="0fe30-118">Identifies a user's mailbox by legacy distinguished name.</span></span>  <br/> |
|[<span data-ttu-id="0fe30-119">DeploymentId (POX)</span><span class="sxs-lookup"><span data-stu-id="0fe30-119">DeploymentId (POX)</span></span>](deploymentid-pox.md) <br/> |<span data-ttu-id="0fe30-120">Die Exchange-Gesamtstruktur identifiziert eindeutig.</span><span class="sxs-lookup"><span data-stu-id="0fe30-120">Uniquely identifies the Exchange forest.</span></span>  <br/> |
|[<span data-ttu-id="0fe30-121">AutoDiscoverSMTPAddress (POX)</span><span class="sxs-lookup"><span data-stu-id="0fe30-121">AutoDiscoverSMTPAddress (POX)</span></span>](autodiscoversmtpaddress-pox.md) <br/> |<span data-ttu-id="0fe30-122">Enthält die SMTP-Adresse des Benutzers, die für die AutoErmittlung-Prozesses verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0fe30-122">Contains the user's SMTP address that is used for the Autodiscover process.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0fe30-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0fe30-123">Parent elements</span></span>

|<span data-ttu-id="0fe30-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="0fe30-124">**Element**</span></span>|<span data-ttu-id="0fe30-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0fe30-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0fe30-126">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="0fe30-126">Response (POX)</span></span>](response-pox.md) <br/> |<span data-ttu-id="0fe30-127">Enthält die Antwort vom AutoErmittlungsdienst.</span><span class="sxs-lookup"><span data-stu-id="0fe30-127">Contains the response from the Autodiscover service.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0fe30-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0fe30-128">Remarks</span></span>

<span data-ttu-id="0fe30-129">AutoErmittlung-Anforderungen und-Antworten müssen UTF-8 codiert sein.</span><span class="sxs-lookup"><span data-stu-id="0fe30-129">Autodiscover requests and responses must be UTF-8 encoded.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0fe30-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0fe30-130">See also</span></span>



[<span data-ttu-id="0fe30-131">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="0fe30-131">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

