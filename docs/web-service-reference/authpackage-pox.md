---
title: AuthPackage (POX)
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 709dbe53-6141-41f8-a2b9-a399bae47991
description: Das AuthPackage-Element gibt das Authentifizierungsschema, das verwendet wird, wenn der Exchange-Server authentifiziert, die die Postfach-Serverrolle installiert ist.
ms.openlocfilehash: 120ec00ac82166ae2002a8fbac0edf9a1e23afc7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757410"
---
# <a name="authpackage-pox"></a><span data-ttu-id="2d0f9-103">AuthPackage (POX)</span><span class="sxs-lookup"><span data-stu-id="2d0f9-103">AuthPackage (POX)</span></span>

<span data-ttu-id="2d0f9-104">Das **AuthPackage** -Element gibt das Authentifizierungsschema, das verwendet wird, wenn der Exchange-Server authentifiziert, die die Postfach-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="2d0f9-104">The **AuthPackage** element specifies the authentication scheme that is used when authenticating against the Exchange server that has the Mailbox server role installed.</span></span> 
  
- [<span data-ttu-id="2d0f9-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="2d0f9-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
- [<span data-ttu-id="2d0f9-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="2d0f9-106">Response (POX)</span></span>](response-pox.md)
  
- [<span data-ttu-id="2d0f9-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="2d0f9-107">Account (POX)</span></span>](account-pox.md)
  
- [<span data-ttu-id="2d0f9-108">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="2d0f9-108">Protocol (POX)</span></span>](protocol-pox.md)
  
- [<span data-ttu-id="2d0f9-109">AuthPackage (POX)</span><span class="sxs-lookup"><span data-stu-id="2d0f9-109">AuthPackage (POX)</span></span>](authpackage-pox.md)
  
```xml
<AuthPackage>basic or kerb or kerbntlm or ntlm or certificate or negotiate or nego2</AuthPackage>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="2d0f9-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="2d0f9-110">Attributes and elements</span></span>

<span data-ttu-id="2d0f9-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="2d0f9-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2d0f9-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="2d0f9-112">Attributes</span></span>

<span data-ttu-id="2d0f9-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="2d0f9-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2d0f9-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2d0f9-114">Child elements</span></span>

<span data-ttu-id="2d0f9-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="2d0f9-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2d0f9-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2d0f9-116">Parent elements</span></span>

|<span data-ttu-id="2d0f9-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="2d0f9-117">**Element**</span></span>|<span data-ttu-id="2d0f9-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2d0f9-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2d0f9-119">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="2d0f9-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="2d0f9-120">Enthält die Spezifikationen für die Verbindung eines Clients mit dem Clientzugriffsserver an.</span><span class="sxs-lookup"><span data-stu-id="2d0f9-120">Contains the specifications for connecting a client to the Client Access server.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2d0f9-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="2d0f9-121">Text value</span></span>

<span data-ttu-id="2d0f9-122">Der Textwert gibt das Authentifizierungsschema, das verwendet wird, wenn auf dem Postfachserver zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="2d0f9-122">The text value specifies the authentication scheme that is used when authenticating against the Mailbox server.</span></span> <span data-ttu-id="2d0f9-123">Im Folgenden sind die möglichen Werte aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="2d0f9-123">The following are the possible values:</span></span>
  
- <span data-ttu-id="2d0f9-124">grundlegende</span><span class="sxs-lookup"><span data-stu-id="2d0f9-124">basic</span></span>
- <span data-ttu-id="2d0f9-125">Kerbtray</span><span class="sxs-lookup"><span data-stu-id="2d0f9-125">kerb</span></span>
- <span data-ttu-id="2d0f9-126">kerbntlm</span><span class="sxs-lookup"><span data-stu-id="2d0f9-126">kerbntlm</span></span>
- <span data-ttu-id="2d0f9-127">NTLM</span><span class="sxs-lookup"><span data-stu-id="2d0f9-127">ntlm</span></span>
- <span data-ttu-id="2d0f9-128">certificate</span><span class="sxs-lookup"><span data-stu-id="2d0f9-128">certificate</span></span>
- <span data-ttu-id="2d0f9-129">Verhandeln</span><span class="sxs-lookup"><span data-stu-id="2d0f9-129">negotiate</span></span>
- <span data-ttu-id="2d0f9-130">nego2</span><span class="sxs-lookup"><span data-stu-id="2d0f9-130">nego2</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2d0f9-131">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2d0f9-131">Remarks</span></span>

<span data-ttu-id="2d0f9-132">Das **AuthPackage** -Element wird nur verwendet, wenn das Element [Typ (POX)](type-pox.md) ein Textwerts EXCH oder AUSDR vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="2d0f9-132">The **AuthPackage** element is only used when the [Type (POX)](type-pox.md) element has a text value of EXCH or EXPR.</span></span> 
  
### <a name="version-differences"></a><span data-ttu-id="2d0f9-133">Versionsunterschiede</span><span class="sxs-lookup"><span data-stu-id="2d0f9-133">Version differences</span></span>

<span data-ttu-id="2d0f9-134">Office 365, Exchange Online und lokale Versionen von Exchange beginnend mit erstellen 15.00.0995.014 zurück Wert "aushandeln" nur, wenn der Server so konfiguriert ist, dass aushandeln-Authentifizierung verwenden und der Client einen [X-ClientCanHandle](pox-autodiscover-request-for-exchange.md) -Header enthält, "Aushandeln" enthält.</span><span class="sxs-lookup"><span data-stu-id="2d0f9-134">Office 365, Exchange Online, and on-premises versions of Exchange starting with build 15.00.0995.014 return a value of "negotiate" only if the server is configured to use Negotiate authentication and the client includes a [X-ClientCanHandle](pox-autodiscover-request-for-exchange.md) header that contains "Negotiate".</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2d0f9-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2d0f9-135">See also</span></span>

- [<span data-ttu-id="2d0f9-136">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="2d0f9-136">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

