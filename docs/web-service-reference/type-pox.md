---
title: Typ (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 9a627244-554f-4223-b9d8-a601b81a4a1a
description: Das Type-Element identifiziert den Typ des konfigurierten e-Mail-Kontos.
ms.openlocfilehash: 6e1349769c6a5349304f576419e0c609d3edd9a0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839271"
---
# <a name="type-pox"></a><span data-ttu-id="3251e-103">Typ (POX)</span><span class="sxs-lookup"><span data-stu-id="3251e-103">Type (POX)</span></span>

<span data-ttu-id="3251e-104">Das **Type** -Element identifiziert den Typ des konfigurierten e-Mail-Kontos.</span><span class="sxs-lookup"><span data-stu-id="3251e-104">The **Type** element identifies the type of the configured mail account.</span></span> 
  
[<span data-ttu-id="3251e-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="3251e-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="3251e-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="3251e-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="3251e-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="3251e-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="3251e-108">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="3251e-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="3251e-109">Typ (POX)</span><span class="sxs-lookup"><span data-stu-id="3251e-109">Type (POX)</span></span>](type-pox.md)
  
```XML
<Type>WEB or EXCH or EXPR or EXHTTP</Type>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="3251e-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3251e-110">Attributes and elements</span></span>

<span data-ttu-id="3251e-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="3251e-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3251e-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="3251e-112">Attributes</span></span>

<span data-ttu-id="3251e-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="3251e-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3251e-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3251e-114">Child elements</span></span>

<span data-ttu-id="3251e-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="3251e-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3251e-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3251e-116">Parent elements</span></span>

|<span data-ttu-id="3251e-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="3251e-117">**Element**</span></span>|<span data-ttu-id="3251e-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3251e-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3251e-119">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="3251e-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="3251e-120">Enthält die Spezifikationen für die Verbindung eines Clients mit dem Exchange-Server.</span><span class="sxs-lookup"><span data-stu-id="3251e-120">Contains the specifications for connecting a client to the Exchange server.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3251e-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="3251e-121">Text value</span></span>

<span data-ttu-id="3251e-122">Der Textwert stellt den Typ des e-Mail-Konto.</span><span class="sxs-lookup"><span data-stu-id="3251e-122">The text value represents the type of mail account.</span></span> <span data-ttu-id="3251e-123">In der folgenden Tabelle sind die möglichen Werte aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="3251e-123">The following table lists the possible values.</span></span>
  
|<span data-ttu-id="3251e-124">**Wert**</span><span class="sxs-lookup"><span data-stu-id="3251e-124">**Value**</span></span>|<span data-ttu-id="3251e-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3251e-125">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3251e-126">EXCH</span><span class="sxs-lookup"><span data-stu-id="3251e-126">EXCH</span></span>  <br/> |<span data-ttu-id="3251e-127">Das Protokoll, das für die Verbindung mit dem Server verwendet wird, ist Exchange RPC.</span><span class="sxs-lookup"><span data-stu-id="3251e-127">The protocol that is used to connect to the server is Exchange RPC.</span></span>  <br/> |
|<span data-ttu-id="3251e-128">EXHTTP</span><span class="sxs-lookup"><span data-stu-id="3251e-128">EXHTTP</span></span>  <br/> |<span data-ttu-id="3251e-129">Das Protokoll, das zum Herstellen einer Verbindung der Server RPC/HTTP-Verbindungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3251e-129">The protocol that is used to connect to the server RPC/HTTP connections.</span></span>  <br/> |
|<span data-ttu-id="3251e-130">AUSDR</span><span class="sxs-lookup"><span data-stu-id="3251e-130">EXPR</span></span>  <br/> |<span data-ttu-id="3251e-131">Das Protokoll, das verwendet wird, um mit dem Server herstellen ist Exchange – RPC über HTTP mit RPC-Proxyserver.</span><span class="sxs-lookup"><span data-stu-id="3251e-131">The protocol that is used to connect to the server is Exchange RPC over HTTP, using an RPC proxy server.</span></span>  <br/> <span data-ttu-id="3251e-132">Dies gilt nur, wenn das Element [AccountType (POX)](accounttype-pox.md) auf e-Mails festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="3251e-132">This is only applicable when the [AccountType (POX)](accounttype-pox.md) element is set to email.</span></span>  <br/> |
|<span data-ttu-id="3251e-133">WEB</span><span class="sxs-lookup"><span data-stu-id="3251e-133">WEB</span></span>  <br/> |<span data-ttu-id="3251e-134">E-Mail ist über einen Webbrowser zugegriffen, über die URL, die im [Server (POX)](server-pox.md) -Element angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="3251e-134">E-mail is accessed from a Web browser by using the URL that is specified in the [Server (POX)](server-pox.md) element.</span></span>  <br/> <span data-ttu-id="3251e-135">Dies gilt nur, wenn das Element [AccountType (POX)](accounttype-pox.md) auf e-Mails festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="3251e-135">This is only applicable when the [AccountType (POX)](accounttype-pox.md) element is set to email.</span></span>  <br/> |
   
### <a name="version-differences"></a><span data-ttu-id="3251e-136">Versionsunterschiede</span><span class="sxs-lookup"><span data-stu-id="3251e-136">Version differences</span></span>

<span data-ttu-id="3251e-137">Office 365, Exchange Online und lokale Versionen von Exchange beginnend mit erstellen 15.00.0995.014 return Wert "EXHTTP" nur, wenn der Server so konfiguriert ist, dass um RPC/HTTP-Verbindungen zu übernehmen und der Client eine [X-ClientCanHandle](pox-autodiscover-request-for-exchange.md) -Kopfzeile enthält, "ExHttpInfo" enthält.</span><span class="sxs-lookup"><span data-stu-id="3251e-137">Office 365, Exchange Online, and on-premises versions of Exchange starting with build 15.00.0995.014 return a value of "EXHTTP" only if the server is configured to accept RPC/HTTP connections and the client includes an [X-ClientCanHandle](pox-autodiscover-request-for-exchange.md) header that contains "ExHttpInfo".</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3251e-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3251e-138">See also</span></span>



[<span data-ttu-id="3251e-139">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="3251e-139">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

