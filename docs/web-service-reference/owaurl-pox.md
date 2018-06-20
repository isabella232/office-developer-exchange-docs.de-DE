---
title: OWAUrl (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 450b86a1-1722-49f5-b541-16c1edc3db7a
description: Das OWAUrl-Element beschreibt die URL und Authentifizierung Schema, das verwendet wird, auf einen bestimmten Computer zugreifen, der Microsoft Exchange Server 2007 ausgeführt wird, hat die Clientzugriffs-Serverrolle installiert, die Outlook Web Access gehostet wird.
ms.openlocfilehash: 93d03506e2a74aa1b4ef6d2a49ccbda01cfc1f9a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830673"
---
# <a name="owaurl-pox"></a><span data-ttu-id="ba90f-103">OWAUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="ba90f-103">OWAUrl (POX)</span></span>

<span data-ttu-id="ba90f-104">Das **OWAUrl** -Element beschreibt die URL und Authentifizierung Schema, das verwendet wird, auf einen bestimmten Computer zugreifen, der Microsoft Exchange Server 2007 ausgeführt wird, hat die Clientzugriffs-Serverrolle installiert, die Outlook Web Access gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="ba90f-104">The **OWAUrl** element describes the URL and authentication schema that is used to access a particular computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed that hosts Outlook Web Access.</span></span> 
  
[<span data-ttu-id="ba90f-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="ba90f-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="ba90f-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="ba90f-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="ba90f-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="ba90f-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="ba90f-108">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="ba90f-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="ba90f-109">Interne (POX)</span><span class="sxs-lookup"><span data-stu-id="ba90f-109">Internal (POX)</span></span>](internal-pox.md)
  
[<span data-ttu-id="ba90f-110">OWAUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="ba90f-110">OWAUrl (POX)</span></span>](owaurl-pox.md)
  
```xml
<OWAUrl AuthenticationMethod=""/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="ba90f-111">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ba90f-111">Attributes and elements</span></span>

<span data-ttu-id="ba90f-112">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ba90f-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ba90f-113">Attribute</span><span class="sxs-lookup"><span data-stu-id="ba90f-113">Attributes</span></span>

|<span data-ttu-id="ba90f-114">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="ba90f-114">**Attribute**</span></span>|<span data-ttu-id="ba90f-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ba90f-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ba90f-116">**AuthenticationMethod**</span><span class="sxs-lookup"><span data-stu-id="ba90f-116">**AuthenticationMethod**</span></span> <br/> |<span data-ttu-id="ba90f-117">Beschreibt die Authentifizierungsmethoden für den Zugriff auf Outlook Web Access.</span><span class="sxs-lookup"><span data-stu-id="ba90f-117">Describes the authentication methods for accessing Outlook Web Access.</span></span>  <br/> |
   
#### <a name="authenticationmethod-attribute"></a><span data-ttu-id="ba90f-118">AuthenticationMethod--Attribut</span><span class="sxs-lookup"><span data-stu-id="ba90f-118">AuthenticationMethod Attribute</span></span>

|<span data-ttu-id="ba90f-119">**Wert**</span><span class="sxs-lookup"><span data-stu-id="ba90f-119">**Value**</span></span>|<span data-ttu-id="ba90f-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ba90f-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ba90f-121">WindowsIntegrated</span><span class="sxs-lookup"><span data-stu-id="ba90f-121">WindowsIntegrated</span></span>  <br/> |<span data-ttu-id="ba90f-122">Integrierte Windows-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="ba90f-122">Integrated Windows authentication.</span></span>  <br/> |
|<span data-ttu-id="ba90f-123">FBA</span><span class="sxs-lookup"><span data-stu-id="ba90f-123">FBA</span></span>  <br/> |<span data-ttu-id="ba90f-124">Formularbasierte Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="ba90f-124">Forms-based authentication.</span></span>  <br/> |
|<span data-ttu-id="ba90f-125">NTLM</span><span class="sxs-lookup"><span data-stu-id="ba90f-125">NTLM</span></span>  <br/> |<span data-ttu-id="ba90f-126">NTLM-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="ba90f-126">NTLM authentication.</span></span>  <br/> |
|<span data-ttu-id="ba90f-127">Digest</span><span class="sxs-lookup"><span data-stu-id="ba90f-127">Digest</span></span>  <br/> |<span data-ttu-id="ba90f-128">Digest-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="ba90f-128">Digest authentication.</span></span>  <br/> |
|<span data-ttu-id="ba90f-129">Standard</span><span class="sxs-lookup"><span data-stu-id="ba90f-129">Basic</span></span>  <br/> |<span data-ttu-id="ba90f-130">Standardauthentifizierung.</span><span class="sxs-lookup"><span data-stu-id="ba90f-130">Basic authentication.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ba90f-131">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ba90f-131">Child elements</span></span>

<span data-ttu-id="ba90f-132">Keine.</span><span class="sxs-lookup"><span data-stu-id="ba90f-132">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ba90f-133">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ba90f-133">Parent elements</span></span>

|<span data-ttu-id="ba90f-134">**Element**</span><span class="sxs-lookup"><span data-stu-id="ba90f-134">**Element**</span></span>|<span data-ttu-id="ba90f-135">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ba90f-135">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ba90f-136">Interne (POX)</span><span class="sxs-lookup"><span data-stu-id="ba90f-136">Internal (POX)</span></span>](internal-pox.md) <br/> |<span data-ttu-id="ba90f-137">Enthält die Auflistung von Outlook Web Access-URLs, die ein Client herstellen kann, wenn es innerhalb der Firewall ist.</span><span class="sxs-lookup"><span data-stu-id="ba90f-137">Contains the collection of Outlook Web Access URLs that a client can connect to when it is inside the firewall.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ba90f-138">Textwert</span><span class="sxs-lookup"><span data-stu-id="ba90f-138">Text value</span></span>

<span data-ttu-id="ba90f-139">Der Textwert stellt die URL für die Outlook Web Access-Dienst auf einem Clientzugriffsserver.</span><span class="sxs-lookup"><span data-stu-id="ba90f-139">The text value represents the URL for the Outlook Web Access service on a Client Access server.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ba90f-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ba90f-140">See also</span></span>



[<span data-ttu-id="ba90f-141">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="ba90f-141">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

