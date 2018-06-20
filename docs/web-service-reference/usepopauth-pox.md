---
title: UsePOPAuth (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 28f552d8-6bb8-49b4-a45c-b2053670f1cc
description: Das UsePOPAuth-Element gibt an, ob die Authentifizierungsinformationen angeben, die für einen POP3-Konto bereitgestellt wird auch für Simple Mail Transfer Protocol (SMTP) verwendet wird.
ms.openlocfilehash: be03568d697b1f5461d49dba388a1d3f1008a67e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839428"
---
# <a name="usepopauth-pox"></a><span data-ttu-id="66de8-103">UsePOPAuth (POX)</span><span class="sxs-lookup"><span data-stu-id="66de8-103">UsePOPAuth (POX)</span></span>

<span data-ttu-id="66de8-104">Das **UsePOPAuth** -Element gibt an, ob die Authentifizierungsinformationen angeben, die für einen POP3-Konto bereitgestellt wird auch für Simple Mail Transfer Protocol (SMTP) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="66de8-104">The **UsePOPAuth** element indicates whether the authentication information that is provided for a POP3 type of account is also used for Simple Mail Transfer Protocol (SMTP).</span></span> 
  
[<span data-ttu-id="66de8-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="66de8-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="66de8-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="66de8-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="66de8-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="66de8-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="66de8-108">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="66de8-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="66de8-109">UsePOPAuth (POX)</span><span class="sxs-lookup"><span data-stu-id="66de8-109">UsePOPAuth (POX)</span></span>](usepopauth-pox.md)
  
```xml
<UsePOPAuth>on or off</UsePOPAuth>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="66de8-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="66de8-110">Attributes and elements</span></span>

<span data-ttu-id="66de8-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="66de8-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="66de8-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="66de8-112">Attributes</span></span>

<span data-ttu-id="66de8-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="66de8-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="66de8-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="66de8-114">Child elements</span></span>

<span data-ttu-id="66de8-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="66de8-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="66de8-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="66de8-116">Parent elements</span></span>

|<span data-ttu-id="66de8-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="66de8-117">**Element**</span></span>|<span data-ttu-id="66de8-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="66de8-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="66de8-119">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="66de8-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="66de8-120">Enthält die Spezifikationen für die Verbindung eines Clients mit dem Computer, auf der Microsoft Exchange Server 2007 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="66de8-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="66de8-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="66de8-121">Text value</span></span>

<span data-ttu-id="66de8-122">Der Textwert gibt an, ob die Authentifizierungsinformationen angeben, die für einen POP3-Konto bereitgestellt wird auch für SMTP verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="66de8-122">The text value indicates whether the authentication information that is provided for a POP3 type of account is also used for SMTP.</span></span> <span data-ttu-id="66de8-123">Die möglichen Werte sind **aktiviert** und **deaktiviert**.</span><span class="sxs-lookup"><span data-stu-id="66de8-123">The possible values are **on** and **off**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="66de8-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="66de8-124">Remarks</span></span>

<span data-ttu-id="66de8-125">Das **UsePOPAuth** -Element wird nur verwendet, wenn [Type (POX)](type-pox.md) SMTP ist.</span><span class="sxs-lookup"><span data-stu-id="66de8-125">The **UsePOPAuth** element is only used when [Type (POX)](type-pox.md) is SMTP.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="66de8-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="66de8-126">See also</span></span>



[<span data-ttu-id="66de8-127">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="66de8-127">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

