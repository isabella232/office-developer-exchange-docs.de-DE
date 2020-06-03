---
title: MailStore (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: af338f99-9e62-4124-9bff-8d7cc2008161
description: Das MailStore-Element enthält die Spezifikationen für die Verbindung eines Clients mit dem Postfach des Benutzers mithilfe des MAPI/http-Protokolls.
ms.openlocfilehash: 635228fcfeb3ad791c845050b82666a6e060b229
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459791"
---
# <a name="mailstore-pox"></a><span data-ttu-id="76a8a-103">MailStore (POX)</span><span class="sxs-lookup"><span data-stu-id="76a8a-103">MailStore (POX)</span></span>

<span data-ttu-id="76a8a-104">Das **MailStore** -Element enthält die Spezifikationen für die Verbindung eines Clients mit dem Postfach des Benutzers mithilfe des MAPI/http-Protokolls.</span><span class="sxs-lookup"><span data-stu-id="76a8a-104">The **MailStore** element contains the specifications for connecting a client to the user's mailbox by using the MAPI/HTTP protocol.</span></span> 
  
[<span data-ttu-id="76a8a-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="76a8a-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="76a8a-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="76a8a-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="76a8a-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="76a8a-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="76a8a-108">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="76a8a-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="76a8a-109">MailStore (POX)</span><span class="sxs-lookup"><span data-stu-id="76a8a-109">MailStore (POX)</span></span>](mailstore-pox.md)
  
```XML
<MailStore>
   <ExternalUrl/>
   <InternalUrl/>
</MailStore>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="76a8a-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="76a8a-110">Attributes and elements</span></span>

<span data-ttu-id="76a8a-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="76a8a-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="76a8a-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="76a8a-112">Attributes</span></span>

<span data-ttu-id="76a8a-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="76a8a-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="76a8a-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="76a8a-114">Child elements</span></span>

|<span data-ttu-id="76a8a-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="76a8a-115">**Element**</span></span>|<span data-ttu-id="76a8a-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="76a8a-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="76a8a-117">ExternalURL (POX)</span><span class="sxs-lookup"><span data-stu-id="76a8a-117">ExternalUrl (POX)</span></span>](externalurl-pox.md) <br/> |<span data-ttu-id="76a8a-118">Enthält die URL, die verwendet werden sollte, um über das MAPI/http-Protokoll von außerhalb des Netzwerks des Unternehmens auf das Postfach des Benutzers zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="76a8a-118">Contains the URL that should be used to access the user's mailbox from outside the organization's network by means of the MAPI/HTTP protocol.</span></span>  <br/> |
|[<span data-ttu-id="76a8a-119">InternalURL (POX)</span><span class="sxs-lookup"><span data-stu-id="76a8a-119">InternalUrl (POX)</span></span>](internalurl-pox.md) <br/> |<span data-ttu-id="76a8a-120">Enthält die URL, die für den Zugriff auf das Postfach des Benutzers im Netzwerk des Unternehmens über das MAPI/http-Protokoll verwendet werden sollte.</span><span class="sxs-lookup"><span data-stu-id="76a8a-120">Contains the URL that should be used to access the user's mailbox from inside the organization's network by means of the MAPI/HTTP protocol.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="76a8a-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="76a8a-121">Parent elements</span></span>

|<span data-ttu-id="76a8a-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="76a8a-122">**Element**</span></span>|<span data-ttu-id="76a8a-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="76a8a-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="76a8a-124">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="76a8a-124">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="76a8a-125">Enthält die Spezifikationen für die Verbindung eines Clients mit dem Clientzugriffsserver.</span><span class="sxs-lookup"><span data-stu-id="76a8a-125">Contains the specifications for connecting a client to the Client Access server.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="76a8a-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="76a8a-126">Remarks</span></span>

<span data-ttu-id="76a8a-127">Das **MailStore** -Element ist in einer Antwort vorhanden, die ein [Protocol (POX)-](protocol-pox.md) Element mit dem **Type** -Attributwert "mapiHttp" aufweist.</span><span class="sxs-lookup"><span data-stu-id="76a8a-127">The **MailStore** element is present in a response that has a [Protocol (POX)](protocol-pox.md) element with a **Type** attribute value of "mapiHttp".</span></span> 
  
<span data-ttu-id="76a8a-128">Das **MailStore** -Element steht für Clients zur Verfügung, die das MAPI/http-Protokoll und die Ziel Exchange Online implementieren, Exchange Online im Rahmen von Office 365 und lokalen Versionen von Exchange, beginnend mit Build 15.00.0847.032 (Exchange Server 2013 SP1).</span><span class="sxs-lookup"><span data-stu-id="76a8a-128">The **MailStore** element is available to clients that implement the MAPI/HTTP protocol and target Exchange Online, Exchange Online as part of Office 365, and on-premises versions of Exchange starting with build 15.00.0847.032 (Exchange Server 2013 SP1).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="76a8a-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="76a8a-129">See also</span></span>



[<span data-ttu-id="76a8a-130">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="76a8a-130">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

