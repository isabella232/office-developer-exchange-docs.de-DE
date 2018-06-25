---
title: Postspeicher weitergeleitet (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: af338f99-9e62-4124-9bff-8d7cc2008161
description: Das Postspeicher bezeichnet-Element enthält die Spezifikationen für die Verbindung eines Clients an das Postfach des Benutzers mithilfe des MAPI/HTTP-Protokolls.
ms.openlocfilehash: 4c82c7b61752cf7d91287a3968f6c642f4943855
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830301"
---
# <a name="mailstore-pox"></a><span data-ttu-id="056cd-103">Postspeicher weitergeleitet (POX)</span><span class="sxs-lookup"><span data-stu-id="056cd-103">MailStore (POX)</span></span>

<span data-ttu-id="056cd-104">Das **Postspeicher bezeichnet** -Element enthält die Spezifikationen für die Verbindung eines Clients an das Postfach des Benutzers mithilfe des MAPI/HTTP-Protokolls.</span><span class="sxs-lookup"><span data-stu-id="056cd-104">The **MailStore** element contains the specifications for connecting a client to the user's mailbox by using the MAPI/HTTP protocol.</span></span> 
  
[<span data-ttu-id="056cd-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="056cd-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="056cd-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="056cd-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="056cd-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="056cd-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="056cd-108">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="056cd-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="056cd-109">Postspeicher weitergeleitet (POX)</span><span class="sxs-lookup"><span data-stu-id="056cd-109">MailStore (POX)</span></span>](mailstore-pox.md)
  
```XML
<MailStore>
   <ExternalUrl/>
   <InternalUrl/>
</MailStore>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="056cd-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="056cd-110">Attributes and elements</span></span>

<span data-ttu-id="056cd-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="056cd-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="056cd-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="056cd-112">Attributes</span></span>

<span data-ttu-id="056cd-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="056cd-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="056cd-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="056cd-114">Child elements</span></span>

|<span data-ttu-id="056cd-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="056cd-115">**Element**</span></span>|<span data-ttu-id="056cd-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="056cd-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="056cd-117">ExternalUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="056cd-117">ExternalUrl (POX)</span></span>](externalurl-pox.md) <br/> |<span data-ttu-id="056cd-118">Enthält die URL, die zum Zugriff auf das Postfach des Benutzers von außerhalb des Netzwerks der Organisation über das MAPI/HTTP-Protokoll verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="056cd-118">Contains the URL that should be used to access the user's mailbox from outside the organization's network by means of the MAPI/HTTP protocol.</span></span>  <br/> |
|[<span data-ttu-id="056cd-119">InternalUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="056cd-119">InternalUrl (POX)</span></span>](internalurl-pox.md) <br/> |<span data-ttu-id="056cd-120">Enthält die URL, die zum Zugriff auf das Postfach des Benutzers aus im Netzwerk der Organisation über das MAPI/HTTP-Protokoll verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="056cd-120">Contains the URL that should be used to access the user's mailbox from inside the organization's network by means of the MAPI/HTTP protocol.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="056cd-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="056cd-121">Parent elements</span></span>

|<span data-ttu-id="056cd-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="056cd-122">**Element**</span></span>|<span data-ttu-id="056cd-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="056cd-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="056cd-124">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="056cd-124">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="056cd-125">Enthält die Spezifikationen für die Verbindung eines Clients mit dem Clientzugriffsserver an.</span><span class="sxs-lookup"><span data-stu-id="056cd-125">Contains the specifications for connecting a client to the Client Access server.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="056cd-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="056cd-126">Remarks</span></span>

<span data-ttu-id="056cd-127">Das Element **Postspeicher bezeichnet** ist in eine Antwort, die ein [Protokoll (POX)](protocol-pox.md) -Element mit dem **Type** -Attributwert "MapiHttp" ist vorhanden.</span><span class="sxs-lookup"><span data-stu-id="056cd-127">The **MailStore** element is present in a response that has a [Protocol (POX)](protocol-pox.md) element with a **Type** attribute value of "mapiHttp".</span></span> 
  
<span data-ttu-id="056cd-128">**Postspeicher bezeichnet** -Element wird von Clients, mit die die MAPI/HTTP-Protokoll und das Ziel Exchange Online, Exchange Online als Teil von Office 365, implementiert und lokale Versionen von Exchange, beginnend mit 15.00.0847.032 (Exchange Server 2013 SP1) erstellen.</span><span class="sxs-lookup"><span data-stu-id="056cd-128">The **MailStore** element is available to clients that implement the MAPI/HTTP protocol and target Exchange Online, Exchange Online as part of Office 365, and on-premises versions of Exchange starting with build 15.00.0847.032 (Exchange Server 2013 SP1).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="056cd-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="056cd-129">See also</span></span>



[<span data-ttu-id="056cd-130">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="056cd-130">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

