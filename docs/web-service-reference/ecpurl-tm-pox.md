---
title: EcpUrl-TM (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f35d5ac-55be-4d3a-ad03-7d6e9349d923
description: Das EcpUrl-TM-Element gibt eine partielle URL an, die mit dem Wert des EcpUrl (POX)-Elements kombiniert werden kann, um eine URL zu generieren, die für den Zugriff auf eine Liste aller Website Postfächer verwendet werden kann, in denen ein e-Mail-aktivierter Benutzer derzeit Mitglied ist.
ms.openlocfilehash: 8d4c787e2eeae5300cd0496f199ea71baace98ba
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463545"
---
# <a name="ecpurl-tm-pox"></a><span data-ttu-id="d412f-103">EcpUrl-TM (POX)</span><span class="sxs-lookup"><span data-stu-id="d412f-103">EcpUrl-tm (POX)</span></span>

<span data-ttu-id="d412f-104">Das **EcpUrl-TM-** Element gibt eine partielle URL an, die mit dem Wert des [EcpUrl (POX)](ecpurl-pox.md) -Elements kombiniert werden kann, um eine URL zu generieren, die für den Zugriff auf eine Liste aller Website Postfächer verwendet werden kann, in denen ein e-Mail-aktivierter Benutzer derzeit Mitglied ist.</span><span class="sxs-lookup"><span data-stu-id="d412f-104">The **EcpUrl-tm** element specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access a list of all site mailboxes of which a mail-enabled user is currently a member.</span></span> 
  
[<span data-ttu-id="d412f-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="d412f-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="d412f-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="d412f-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="d412f-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="d412f-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="d412f-108">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="d412f-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="d412f-109">EcpUrl-TM (POX)</span><span class="sxs-lookup"><span data-stu-id="d412f-109">EcpUrl-tm (POX)</span></span>](ecpurl-tm-pox.md)
  
```XML
<EcpUrl-tm/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="d412f-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d412f-110">Attributes and elements</span></span>

<span data-ttu-id="d412f-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d412f-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d412f-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="d412f-112">Attributes</span></span>

<span data-ttu-id="d412f-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="d412f-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d412f-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d412f-114">Child elements</span></span>

<span data-ttu-id="d412f-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="d412f-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d412f-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d412f-116">Parent elements</span></span>

|<span data-ttu-id="d412f-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="d412f-117">**Element**</span></span>|<span data-ttu-id="d412f-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d412f-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d412f-119">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="d412f-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="d412f-120">Enthält die Spezifikationen für das Verbinden eines Clients mit dem Computer, auf dem Exchange Server ausgeführt wird, auf dem die Clientzugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="d412f-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d412f-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="d412f-121">Text value</span></span>

<span data-ttu-id="d412f-122">Der Textwert stellt eine partielle URL dar, die mit dem [EcpUrl (POX)](ecpurl-pox.md) -Elementwert kombiniert werden kann, um eine URL zu generieren, die für den Zugriff auf eine Liste von Website Postfächern für den Benutzer verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="d412f-122">The text value represents a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to access a list of site mailboxes for the user.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d412f-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d412f-123">Remarks</span></span>

<span data-ttu-id="d412f-124">Das **EcpUrl-TM-** Element ist ein optionales untergeordnetes Element des **Protocol** -Elements.</span><span class="sxs-lookup"><span data-stu-id="d412f-124">The **EcpUrl-tm** element is an optional child element of the **Protocol** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d412f-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d412f-125">See also</span></span>



[<span data-ttu-id="d412f-126">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="d412f-126">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

