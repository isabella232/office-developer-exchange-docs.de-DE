---
title: SMTPLast (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: f1aa8bd9-c6ac-41ac-8d2d-56fb20006005
description: Das SMTPLast-Element gibt an, ob der Simple Mail Transfer Protocol (SMTP) Server erfordert, dass E-mail heruntergeladen werden, bevor es e-Mail-Nachrichten mithilfe des SMTP-Servers sendet.
ms.openlocfilehash: 5359f20b33855f4ef48566058bc46bd618e3b2ff
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831505"
---
# <a name="smtplast-pox"></a><span data-ttu-id="9d3f0-103">SMTPLast (POX)</span><span class="sxs-lookup"><span data-stu-id="9d3f0-103">SMTPLast (POX)</span></span>

<span data-ttu-id="9d3f0-104">Das **SMTPLast** -Element gibt an, ob der Simple Mail Transfer Protocol (SMTP) Server erfordert, dass E-mail heruntergeladen werden, bevor es e-Mail-Nachrichten mithilfe des SMTP-Servers sendet.</span><span class="sxs-lookup"><span data-stu-id="9d3f0-104">The **SMTPLast** element specifies whether the Simple Mail Transfer Protocol (SMTP) server requires that e-mail be downloaded before it sends e-mail by using the SMTP server.</span></span> 
  
- [<span data-ttu-id="9d3f0-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="9d3f0-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
- [<span data-ttu-id="9d3f0-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="9d3f0-106">Response (POX)</span></span>](response-pox.md)
  
- [<span data-ttu-id="9d3f0-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="9d3f0-107">Account (POX)</span></span>](account-pox.md)
  
- [<span data-ttu-id="9d3f0-108">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="9d3f0-108">Protocol (POX)</span></span>](protocol-pox.md)
  
- [<span data-ttu-id="9d3f0-109">SMTPLast (POX)</span><span class="sxs-lookup"><span data-stu-id="9d3f0-109">SMTPLast (POX)</span></span>](smtplast-pox.md)
  
```xml
<SMTPLast>on or off</SMTPLast>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="9d3f0-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="9d3f0-110">Attributes and elements</span></span>

<span data-ttu-id="9d3f0-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="9d3f0-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9d3f0-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="9d3f0-112">Attributes</span></span>

<span data-ttu-id="9d3f0-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="9d3f0-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9d3f0-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9d3f0-114">Child elements</span></span>

<span data-ttu-id="9d3f0-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="9d3f0-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9d3f0-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9d3f0-116">Parent elements</span></span>

|<span data-ttu-id="9d3f0-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="9d3f0-117">**Element**</span></span>|<span data-ttu-id="9d3f0-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9d3f0-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9d3f0-119">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="9d3f0-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="9d3f0-120">Enthält die Spezifikationen für die Verbindung eines Clients mit dem Computer, auf der Microsoft Exchange Server 2007 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="9d3f0-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="9d3f0-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="9d3f0-121">Text value</span></span>

<span data-ttu-id="9d3f0-122">Der Textwert gibt an, ob der SMTP-Server erfordert, dass E-mail heruntergeladen werden, bevor es e-Mail-Nachrichten mithilfe des SMTP-Servers sendet.</span><span class="sxs-lookup"><span data-stu-id="9d3f0-122">The text value specifies whether the SMTP server requires that e-mail be downloaded before it sends e-mail by using the SMTP server.</span></span> <span data-ttu-id="9d3f0-123">Die möglichen Werte sind **aktiviert** und **deaktiviert**.</span><span class="sxs-lookup"><span data-stu-id="9d3f0-123">The possible values are **on** and **off**.</span></span> <span data-ttu-id="9d3f0-124">Der Standardwert ist **deaktiviert**.</span><span class="sxs-lookup"><span data-stu-id="9d3f0-124">The default value is **off**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9d3f0-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9d3f0-125">See also</span></span>

- [<span data-ttu-id="9d3f0-126">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="9d3f0-126">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

