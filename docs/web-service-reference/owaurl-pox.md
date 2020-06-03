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
description: Das OWAUrl-Element beschreibt die URL und das Authentifizierungsschema, das verwendet wird, um auf einen bestimmten Computer zuzugreifen, auf dem Microsoft Exchange Server 2007 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist, die Outlook Web Access hostet.
ms.openlocfilehash: c0728af063cfbf1353eb7d3b81f5fcfe8b398f7d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457263"
---
# <a name="owaurl-pox"></a><span data-ttu-id="c1f50-103">OWAUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="c1f50-103">OWAUrl (POX)</span></span>

<span data-ttu-id="c1f50-104">Das **OWAUrl** -Element beschreibt die URL und das Authentifizierungsschema, das verwendet wird, um auf einen bestimmten Computer zuzugreifen, auf dem Microsoft Exchange Server 2007 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist, die Outlook Web Access hostet.</span><span class="sxs-lookup"><span data-stu-id="c1f50-104">The **OWAUrl** element describes the URL and authentication schema that is used to access a particular computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed that hosts Outlook Web Access.</span></span> 
  
[<span data-ttu-id="c1f50-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="c1f50-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="c1f50-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="c1f50-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="c1f50-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="c1f50-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="c1f50-108">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="c1f50-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="c1f50-109">Interne (POX)</span><span class="sxs-lookup"><span data-stu-id="c1f50-109">Internal (POX)</span></span>](internal-pox.md)
  
[<span data-ttu-id="c1f50-110">OWAUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="c1f50-110">OWAUrl (POX)</span></span>](owaurl-pox.md)
  
```xml
<OWAUrl AuthenticationMethod=""/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="c1f50-111">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c1f50-111">Attributes and elements</span></span>

<span data-ttu-id="c1f50-112">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c1f50-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c1f50-113">Attribute</span><span class="sxs-lookup"><span data-stu-id="c1f50-113">Attributes</span></span>

|<span data-ttu-id="c1f50-114">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="c1f50-114">**Attribute**</span></span>|<span data-ttu-id="c1f50-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c1f50-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c1f50-116">**AuthenticationMethod**</span><span class="sxs-lookup"><span data-stu-id="c1f50-116">**AuthenticationMethod**</span></span> <br/> |<span data-ttu-id="c1f50-117">Beschreibt die Authentifizierungsmethoden für den Zugriff auf Outlook Web Access.</span><span class="sxs-lookup"><span data-stu-id="c1f50-117">Describes the authentication methods for accessing Outlook Web Access.</span></span>  <br/> |
   
#### <a name="authenticationmethod-attribute"></a><span data-ttu-id="c1f50-118">AuthenticationMethod-Attribut</span><span class="sxs-lookup"><span data-stu-id="c1f50-118">AuthenticationMethod Attribute</span></span>

|<span data-ttu-id="c1f50-119">**Wert**</span><span class="sxs-lookup"><span data-stu-id="c1f50-119">**Value**</span></span>|<span data-ttu-id="c1f50-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c1f50-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c1f50-121">WindowsIntegrated</span><span class="sxs-lookup"><span data-stu-id="c1f50-121">WindowsIntegrated</span></span>  <br/> |<span data-ttu-id="c1f50-122">Integrierte Windows-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="c1f50-122">Integrated Windows authentication.</span></span>  <br/> |
|<span data-ttu-id="c1f50-123">FBA</span><span class="sxs-lookup"><span data-stu-id="c1f50-123">FBA</span></span>  <br/> |<span data-ttu-id="c1f50-124">Formularbasierte Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="c1f50-124">Forms-based authentication.</span></span>  <br/> |
|<span data-ttu-id="c1f50-125">NTLM</span><span class="sxs-lookup"><span data-stu-id="c1f50-125">NTLM</span></span>  <br/> |<span data-ttu-id="c1f50-126">NTLM-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="c1f50-126">NTLM authentication.</span></span>  <br/> |
|<span data-ttu-id="c1f50-127">Digest</span><span class="sxs-lookup"><span data-stu-id="c1f50-127">Digest</span></span>  <br/> |<span data-ttu-id="c1f50-128">Digest-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="c1f50-128">Digest authentication.</span></span>  <br/> |
|<span data-ttu-id="c1f50-129">Basic</span><span class="sxs-lookup"><span data-stu-id="c1f50-129">Basic</span></span>  <br/> |<span data-ttu-id="c1f50-130">Standardauthentifizierung.</span><span class="sxs-lookup"><span data-stu-id="c1f50-130">Basic authentication.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c1f50-131">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c1f50-131">Child elements</span></span>

<span data-ttu-id="c1f50-132">Keine.</span><span class="sxs-lookup"><span data-stu-id="c1f50-132">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c1f50-133">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c1f50-133">Parent elements</span></span>

|<span data-ttu-id="c1f50-134">**Element**</span><span class="sxs-lookup"><span data-stu-id="c1f50-134">**Element**</span></span>|<span data-ttu-id="c1f50-135">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c1f50-135">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c1f50-136">Interne (POX)</span><span class="sxs-lookup"><span data-stu-id="c1f50-136">Internal (POX)</span></span>](internal-pox.md) <br/> |<span data-ttu-id="c1f50-137">Enthält die Sammlung von Outlook Web Access-URLs, mit denen ein Client eine Verbindung herstellen kann, wenn er sich innerhalb der Firewall befindet.</span><span class="sxs-lookup"><span data-stu-id="c1f50-137">Contains the collection of Outlook Web Access URLs that a client can connect to when it is inside the firewall.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c1f50-138">Textwert</span><span class="sxs-lookup"><span data-stu-id="c1f50-138">Text value</span></span>

<span data-ttu-id="c1f50-139">Der Wert Text stellt die URL für den Outlook Web Access Dienst auf einem Client Zugriffsserver dar.</span><span class="sxs-lookup"><span data-stu-id="c1f50-139">The text value represents the URL for the Outlook Web Access service on a Client Access server.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c1f50-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c1f50-140">See also</span></span>



[<span data-ttu-id="c1f50-141">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="c1f50-141">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

