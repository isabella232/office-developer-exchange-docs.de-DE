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
description: Das SMTPLast-Element gibt an, ob für den Simple Mail Transfer Protocol (SMTP) Server die e-Mail-Nachrichten heruntergeladen werden müssen, bevor eine e-Mail mithilfe des SMTP-Servers gesendet wird.
ms.openlocfilehash: 7019da28ffa196a9abc8798aa75aff2756198da3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468432"
---
# <a name="smtplast-pox"></a><span data-ttu-id="2c1d6-103">SMTPLast (POX)</span><span class="sxs-lookup"><span data-stu-id="2c1d6-103">SMTPLast (POX)</span></span>

<span data-ttu-id="2c1d6-104">Das **SMTPLast** -Element gibt an, ob für den Simple Mail Transfer Protocol (SMTP) Server die e-Mail-Nachrichten heruntergeladen werden müssen, bevor eine e-Mail mithilfe des SMTP-Servers gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="2c1d6-104">The **SMTPLast** element specifies whether the Simple Mail Transfer Protocol (SMTP) server requires that e-mail be downloaded before it sends e-mail by using the SMTP server.</span></span> 
  
- [<span data-ttu-id="2c1d6-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="2c1d6-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
- [<span data-ttu-id="2c1d6-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="2c1d6-106">Response (POX)</span></span>](response-pox.md)
  
- [<span data-ttu-id="2c1d6-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="2c1d6-107">Account (POX)</span></span>](account-pox.md)
  
- [<span data-ttu-id="2c1d6-108">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="2c1d6-108">Protocol (POX)</span></span>](protocol-pox.md)
  
- [<span data-ttu-id="2c1d6-109">SMTPLast (POX)</span><span class="sxs-lookup"><span data-stu-id="2c1d6-109">SMTPLast (POX)</span></span>](smtplast-pox.md)
  
```xml
<SMTPLast>on or off</SMTPLast>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="2c1d6-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="2c1d6-110">Attributes and elements</span></span>

<span data-ttu-id="2c1d6-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="2c1d6-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2c1d6-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="2c1d6-112">Attributes</span></span>

<span data-ttu-id="2c1d6-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="2c1d6-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2c1d6-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2c1d6-114">Child elements</span></span>

<span data-ttu-id="2c1d6-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="2c1d6-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2c1d6-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2c1d6-116">Parent elements</span></span>

|<span data-ttu-id="2c1d6-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="2c1d6-117">**Element**</span></span>|<span data-ttu-id="2c1d6-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2c1d6-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2c1d6-119">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="2c1d6-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="2c1d6-120">Enthält die Spezifikationen für das Verbinden eines Clients mit dem Computer, auf dem Microsoft Exchange Server 2007 ausgeführt wird, auf dem die Clientzugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="2c1d6-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2c1d6-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="2c1d6-121">Text value</span></span>

<span data-ttu-id="2c1d6-122">Der Text-Wert gibt an, ob der SMTP-Server die e-Mail-Nachrichten heruntergeladen werden muss, bevor er e-Mails mithilfe des SMTP-Servers sendet.</span><span class="sxs-lookup"><span data-stu-id="2c1d6-122">The text value specifies whether the SMTP server requires that e-mail be downloaded before it sends e-mail by using the SMTP server.</span></span> <span data-ttu-id="2c1d6-123">Die möglichen Werte sind **ein** -und **ausgeschaltet**.</span><span class="sxs-lookup"><span data-stu-id="2c1d6-123">The possible values are **on** and **off**.</span></span> <span data-ttu-id="2c1d6-124">Der Standardwert ist **Off**.</span><span class="sxs-lookup"><span data-stu-id="2c1d6-124">The default value is **off**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2c1d6-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2c1d6-125">See also</span></span>

- [<span data-ttu-id="2c1d6-126">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="2c1d6-126">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

