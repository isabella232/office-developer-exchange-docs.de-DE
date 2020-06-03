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
description: Das User-Element enthält benutzerspezifische Informationen.
ms.openlocfilehash: 8f53319bcf34595305748adafc9aa1e25283611e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530218"
---
# <a name="user-pox"></a><span data-ttu-id="da6e7-103">Benutzer (POX)</span><span class="sxs-lookup"><span data-stu-id="da6e7-103">User (POX)</span></span>

<span data-ttu-id="da6e7-104">Das **User** -Element enthält benutzerspezifische Informationen.</span><span class="sxs-lookup"><span data-stu-id="da6e7-104">The **User** element provides user-specific information.</span></span> 
  
[<span data-ttu-id="da6e7-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="da6e7-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="da6e7-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="da6e7-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="da6e7-107">Benutzer (POX)</span><span class="sxs-lookup"><span data-stu-id="da6e7-107">User (POX)</span></span>](user-pox.md)
  
```xml
<User>
   <DisplayName/>
   <LegacyDN/>
   <DeploymentId/>
   <AutoDiscoverSMTPAddress/>
</User>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="da6e7-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="da6e7-108">Attributes and elements</span></span>

<span data-ttu-id="da6e7-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="da6e7-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="da6e7-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="da6e7-110">Attributes</span></span>

<span data-ttu-id="da6e7-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="da6e7-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="da6e7-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="da6e7-112">Child elements</span></span>

|<span data-ttu-id="da6e7-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="da6e7-113">**Element**</span></span>|<span data-ttu-id="da6e7-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="da6e7-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="da6e7-115">DisplayName (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="da6e7-115">DisplayName (string)</span></span>](displayname-string.md) <br/> |<span data-ttu-id="da6e7-116">Stellt den Anzeigenamen des Benutzers dar.</span><span class="sxs-lookup"><span data-stu-id="da6e7-116">Represents the user's display name.</span></span>  <br/> |
|[<span data-ttu-id="da6e7-117">LegacyDN (POX)</span><span class="sxs-lookup"><span data-stu-id="da6e7-117">LegacyDN (POX)</span></span>](legacydn-pox.md) <br/> |<span data-ttu-id="da6e7-118">Identifiziert das Postfach eines Benutzers anhand des Distinguished Name-Legacy namens.</span><span class="sxs-lookup"><span data-stu-id="da6e7-118">Identifies a user's mailbox by legacy distinguished name.</span></span>  <br/> |
|[<span data-ttu-id="da6e7-119">DeploymentId (POX)</span><span class="sxs-lookup"><span data-stu-id="da6e7-119">DeploymentId (POX)</span></span>](deploymentid-pox.md) <br/> |<span data-ttu-id="da6e7-120">Identifiziert die Exchange-Gesamtstruktur eindeutig.</span><span class="sxs-lookup"><span data-stu-id="da6e7-120">Uniquely identifies the Exchange forest.</span></span>  <br/> |
|[<span data-ttu-id="da6e7-121">AutoDiscoverSMTPAddress (POX)</span><span class="sxs-lookup"><span data-stu-id="da6e7-121">AutoDiscoverSMTPAddress (POX)</span></span>](autodiscoversmtpaddress-pox.md) <br/> |<span data-ttu-id="da6e7-122">Enthält die SMTP-Adresse des Benutzers, die für den Auto Ermittlungsprozess verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="da6e7-122">Contains the user's SMTP address that is used for the Autodiscover process.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="da6e7-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="da6e7-123">Parent elements</span></span>

|<span data-ttu-id="da6e7-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="da6e7-124">**Element**</span></span>|<span data-ttu-id="da6e7-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="da6e7-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="da6e7-126">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="da6e7-126">Response (POX)</span></span>](response-pox.md) <br/> |<span data-ttu-id="da6e7-127">Enthält die Antwort des AutoErmittlungsdiensts.</span><span class="sxs-lookup"><span data-stu-id="da6e7-127">Contains the response from the Autodiscover service.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="da6e7-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="da6e7-128">Remarks</span></span>

<span data-ttu-id="da6e7-129">AutoErmittlung-Anforderungen und-Antworten müssen UTF-8-codiert sein.</span><span class="sxs-lookup"><span data-stu-id="da6e7-129">Autodiscover requests and responses must be UTF-8 encoded.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="da6e7-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="da6e7-130">See also</span></span>



[<span data-ttu-id="da6e7-131">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="da6e7-131">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

