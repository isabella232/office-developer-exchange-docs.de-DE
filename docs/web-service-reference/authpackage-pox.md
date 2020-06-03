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
description: Das AuthPackage-Element gibt das Authentifizierungsschema an, das bei der Authentifizierung mit dem Exchange-Server verwendet wird, auf dem die Postfachserverrolle installiert ist.
ms.openlocfilehash: 5317cf49d354a558417829e1d1b5b67cd6874309
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459104"
---
# <a name="authpackage-pox"></a><span data-ttu-id="9a143-103">AuthPackage (POX)</span><span class="sxs-lookup"><span data-stu-id="9a143-103">AuthPackage (POX)</span></span>

<span data-ttu-id="9a143-104">Das **AuthPackage** -Element gibt das Authentifizierungsschema an, das bei der Authentifizierung mit dem Exchange-Server verwendet wird, auf dem die Postfachserverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="9a143-104">The **AuthPackage** element specifies the authentication scheme that is used when authenticating against the Exchange server that has the Mailbox server role installed.</span></span> 
  
- [<span data-ttu-id="9a143-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="9a143-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
- [<span data-ttu-id="9a143-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="9a143-106">Response (POX)</span></span>](response-pox.md)
  
- [<span data-ttu-id="9a143-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="9a143-107">Account (POX)</span></span>](account-pox.md)
  
- [<span data-ttu-id="9a143-108">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="9a143-108">Protocol (POX)</span></span>](protocol-pox.md)
  
- [<span data-ttu-id="9a143-109">AuthPackage (POX)</span><span class="sxs-lookup"><span data-stu-id="9a143-109">AuthPackage (POX)</span></span>](authpackage-pox.md)
  
```xml
<AuthPackage>basic or kerb or kerbntlm or ntlm or certificate or negotiate or nego2</AuthPackage>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="9a143-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="9a143-110">Attributes and elements</span></span>

<span data-ttu-id="9a143-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="9a143-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9a143-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="9a143-112">Attributes</span></span>

<span data-ttu-id="9a143-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="9a143-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9a143-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9a143-114">Child elements</span></span>

<span data-ttu-id="9a143-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="9a143-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9a143-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9a143-116">Parent elements</span></span>

|<span data-ttu-id="9a143-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="9a143-117">**Element**</span></span>|<span data-ttu-id="9a143-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9a143-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9a143-119">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="9a143-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="9a143-120">Enthält die Spezifikationen für die Verbindung eines Clients mit dem Clientzugriffsserver.</span><span class="sxs-lookup"><span data-stu-id="9a143-120">Contains the specifications for connecting a client to the Client Access server.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="9a143-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="9a143-121">Text value</span></span>

<span data-ttu-id="9a143-122">Der Wert Text gibt das Authentifizierungsschema an, das bei der Authentifizierung mit dem Postfachserver verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9a143-122">The text value specifies the authentication scheme that is used when authenticating against the Mailbox server.</span></span> <span data-ttu-id="9a143-123">Im Folgenden sind die möglichen Werte aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="9a143-123">The following are the possible values:</span></span>
  
- <span data-ttu-id="9a143-124">Basic</span><span class="sxs-lookup"><span data-stu-id="9a143-124">basic</span></span>
- <span data-ttu-id="9a143-125">Kerbtray</span><span class="sxs-lookup"><span data-stu-id="9a143-125">kerb</span></span>
- <span data-ttu-id="9a143-126">kerbntlm</span><span class="sxs-lookup"><span data-stu-id="9a143-126">kerbntlm</span></span>
- <span data-ttu-id="9a143-127">NTLM</span><span class="sxs-lookup"><span data-stu-id="9a143-127">ntlm</span></span>
- <span data-ttu-id="9a143-128">certificate</span><span class="sxs-lookup"><span data-stu-id="9a143-128">certificate</span></span>
- <span data-ttu-id="9a143-129">aushandeln</span><span class="sxs-lookup"><span data-stu-id="9a143-129">negotiate</span></span>
- <span data-ttu-id="9a143-130">nego2</span><span class="sxs-lookup"><span data-stu-id="9a143-130">nego2</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9a143-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9a143-131">Remarks</span></span>

<span data-ttu-id="9a143-132">Das **AuthPackage** -Element wird nur verwendet, wenn der [Typ (POX)-](type-pox.md) Element den Textwert von "$" oder "expr" aufweist.</span><span class="sxs-lookup"><span data-stu-id="9a143-132">The **AuthPackage** element is only used when the [Type (POX)](type-pox.md) element has a text value of EXCH or EXPR.</span></span> 
  
### <a name="version-differences"></a><span data-ttu-id="9a143-133">Versionsunterschiede</span><span class="sxs-lookup"><span data-stu-id="9a143-133">Version differences</span></span>

<span data-ttu-id="9a143-134">Office 365, Exchange Online und lokale Versionen von Exchange, beginnend mit Build 15.00.0995.014, geben nur dann den Wert "Negotiate" zurück, wenn der Server für die Verwendung der Negotiate-Authentifizierung konfiguriert ist und der Client einen [X-ClientCanHandle-](pox-autodiscover-request-for-exchange.md) Header mit "Negotiate" enthält.</span><span class="sxs-lookup"><span data-stu-id="9a143-134">Office 365, Exchange Online, and on-premises versions of Exchange starting with build 15.00.0995.014 return a value of "negotiate" only if the server is configured to use Negotiate authentication and the client includes a [X-ClientCanHandle](pox-autodiscover-request-for-exchange.md) header that contains "Negotiate".</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9a143-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9a143-135">See also</span></span>

- [<span data-ttu-id="9a143-136">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="9a143-136">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

