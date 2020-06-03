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
description: Das Type-Element gibt den Typ des konfigurierten e-Mail-Kontos an.
ms.openlocfilehash: ad3570094ebe28498dfdc375cf7fc255434ba20d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465100"
---
# <a name="type-pox"></a><span data-ttu-id="7aced-103">Typ (POX)</span><span class="sxs-lookup"><span data-stu-id="7aced-103">Type (POX)</span></span>

<span data-ttu-id="7aced-104">Das **Type** -Element gibt den Typ des konfigurierten e-Mail-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="7aced-104">The **Type** element identifies the type of the configured mail account.</span></span> 
  
[<span data-ttu-id="7aced-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="7aced-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="7aced-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="7aced-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="7aced-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="7aced-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="7aced-108">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="7aced-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="7aced-109">Typ (POX)</span><span class="sxs-lookup"><span data-stu-id="7aced-109">Type (POX)</span></span>](type-pox.md)
  
```XML
<Type>WEB or EXCH or EXPR or EXHTTP</Type>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="7aced-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="7aced-110">Attributes and elements</span></span>

<span data-ttu-id="7aced-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="7aced-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7aced-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="7aced-112">Attributes</span></span>

<span data-ttu-id="7aced-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="7aced-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7aced-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7aced-114">Child elements</span></span>

<span data-ttu-id="7aced-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="7aced-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7aced-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7aced-116">Parent elements</span></span>

|<span data-ttu-id="7aced-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="7aced-117">**Element**</span></span>|<span data-ttu-id="7aced-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7aced-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7aced-119">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="7aced-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="7aced-120">Enthält die Spezifikationen für die Verbindung eines Clients mit dem Exchange-Server.</span><span class="sxs-lookup"><span data-stu-id="7aced-120">Contains the specifications for connecting a client to the Exchange server.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7aced-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="7aced-121">Text value</span></span>

<span data-ttu-id="7aced-122">Der Wert Text stellt den Typ des e-Mail-Kontos dar.</span><span class="sxs-lookup"><span data-stu-id="7aced-122">The text value represents the type of mail account.</span></span> <span data-ttu-id="7aced-123">In der folgenden Tabelle sind die möglichen Werte aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="7aced-123">The following table lists the possible values.</span></span>
  
|<span data-ttu-id="7aced-124">**Wert**</span><span class="sxs-lookup"><span data-stu-id="7aced-124">**Value**</span></span>|<span data-ttu-id="7aced-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7aced-125">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7aced-126">Exch</span><span class="sxs-lookup"><span data-stu-id="7aced-126">EXCH</span></span>  <br/> |<span data-ttu-id="7aced-127">Das Protokoll, das zum Herstellen einer Verbindung mit dem Server verwendet wird, ist Exchange RPC.</span><span class="sxs-lookup"><span data-stu-id="7aced-127">The protocol that is used to connect to the server is Exchange RPC.</span></span>  <br/> |
|<span data-ttu-id="7aced-128">Http</span><span class="sxs-lookup"><span data-stu-id="7aced-128">EXHTTP</span></span>  <br/> |<span data-ttu-id="7aced-129">Das Protokoll, das zum Herstellen einer Verbindung mit den Server-RPC/HTTP-Verbindungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7aced-129">The protocol that is used to connect to the server RPC/HTTP connections.</span></span>  <br/> |
|<span data-ttu-id="7aced-130">EXPR</span><span class="sxs-lookup"><span data-stu-id="7aced-130">EXPR</span></span>  <br/> |<span data-ttu-id="7aced-131">Das Protokoll, das zum Herstellen einer Verbindung mit dem Server verwendet wird, ist Exchange-RPC-über-HTTP mit einem RPC-Proxy Server.</span><span class="sxs-lookup"><span data-stu-id="7aced-131">The protocol that is used to connect to the server is Exchange RPC over HTTP, using an RPC proxy server.</span></span>  <br/> <span data-ttu-id="7aced-132">Dies gilt nur, wenn das [POX-Element (AccountType)](accounttype-pox.md) auf e-Mail festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7aced-132">This is only applicable when the [AccountType (POX)](accounttype-pox.md) element is set to email.</span></span>  <br/> |
|<span data-ttu-id="7aced-133">Web</span><span class="sxs-lookup"><span data-stu-id="7aced-133">WEB</span></span>  <br/> |<span data-ttu-id="7aced-134">Der Zugriff auf E-Mail erfolgt über einen Webbrowser mithilfe der URL, die im [Server (POX)](server-pox.md) -Element angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="7aced-134">E-mail is accessed from a Web browser by using the URL that is specified in the [Server (POX)](server-pox.md) element.</span></span>  <br/> <span data-ttu-id="7aced-135">Dies gilt nur, wenn das [POX-Element (AccountType)](accounttype-pox.md) auf e-Mail festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7aced-135">This is only applicable when the [AccountType (POX)](accounttype-pox.md) element is set to email.</span></span>  <br/> |
   
### <a name="version-differences"></a><span data-ttu-id="7aced-136">Versionsunterschiede</span><span class="sxs-lookup"><span data-stu-id="7aced-136">Version differences</span></span>

<span data-ttu-id="7aced-137">Office 365, Exchange Online und lokale Versionen von Exchange, die mit Build 15.00.0995.014 beginnen, geben nur dann den Wert "http" zurück, wenn der Server so konfiguriert ist, dass er RPC/HTTP-Verbindungen akzeptiert, und der Client einen [X-ClientCanHandle-](pox-autodiscover-request-for-exchange.md) Header enthält, der "ExHttpInfo" enthält.</span><span class="sxs-lookup"><span data-stu-id="7aced-137">Office 365, Exchange Online, and on-premises versions of Exchange starting with build 15.00.0995.014 return a value of "EXHTTP" only if the server is configured to accept RPC/HTTP connections and the client includes an [X-ClientCanHandle](pox-autodiscover-request-for-exchange.md) header that contains "ExHttpInfo".</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7aced-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7aced-138">See also</span></span>



[<span data-ttu-id="7aced-139">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="7aced-139">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

