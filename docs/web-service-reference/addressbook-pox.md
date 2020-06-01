---
title: Adressbuch (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b2d62fd0-741c-4a41-9762-cc7d0ff01c9c
description: Das addressbook-Element enthält die Spezifikationen für die Verbindung eines Clients mit dem Adressbuchserver mithilfe des MAPI/http-Protokolls.
ms.openlocfilehash: 0967ac123cd3bb0086fd004ea0d0d37c08d2e037
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463636"
---
# <a name="addressbook-pox"></a><span data-ttu-id="8c964-103">Adressbuch (POX)</span><span class="sxs-lookup"><span data-stu-id="8c964-103">AddressBook (POX)</span></span>

<span data-ttu-id="8c964-104">Das **addressbook** -Element enthält die Spezifikationen für die Verbindung eines Clients mit dem Adressbuchserver mithilfe des MAPI/http-Protokolls.</span><span class="sxs-lookup"><span data-stu-id="8c964-104">The **AddressBook** element contains the specifications for connecting a client to the address book server by using the MAPI/HTTP protocol.</span></span> 
  
[<span data-ttu-id="8c964-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="8c964-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="8c964-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="8c964-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="8c964-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="8c964-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="8c964-108">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="8c964-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="8c964-109">Adressbuch (POX)</span><span class="sxs-lookup"><span data-stu-id="8c964-109">AddressBook (POX)</span></span>](addressbook-pox.md)
  
```XML
<AddressBook>
   <ExternalUrl/>
   <InternalUrl/>
</AddressBook>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="8c964-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="8c964-110">Attributes and elements</span></span>

<span data-ttu-id="8c964-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="8c964-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8c964-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="8c964-112">Attributes</span></span>

<span data-ttu-id="8c964-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="8c964-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8c964-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8c964-114">Child elements</span></span>

|<span data-ttu-id="8c964-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="8c964-115">**Element**</span></span>|<span data-ttu-id="8c964-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8c964-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8c964-117">ExternalURL (POX)</span><span class="sxs-lookup"><span data-stu-id="8c964-117">ExternalUrl (POX)</span></span>](externalurl-pox.md) <br/> |<span data-ttu-id="8c964-118">Enthält die URL, die verwendet werden sollte, um über das MAPI/http-Protokoll von außerhalb des Netzwerks des Unternehmens auf das Adressbuch zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="8c964-118">Contains the URL that should be used to access the address book from outside the organization's network by using the MAPI/HTTP protocol.</span></span>  <br/> |
|[<span data-ttu-id="8c964-119">InternalURL (POX)</span><span class="sxs-lookup"><span data-stu-id="8c964-119">InternalUrl (POX)</span></span>](internalurl-pox.md) <br/> |<span data-ttu-id="8c964-120">Enthält die URL, die für den Zugriff auf das Adressbuch im Netzwerk des Unternehmens mithilfe des MAPI/http-Protokolls verwendet werden sollte.</span><span class="sxs-lookup"><span data-stu-id="8c964-120">Contains the URL that should be used to access the address book from inside the organization's network by using the MAPI/HTTP protocol.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8c964-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8c964-121">Parent elements</span></span>

|<span data-ttu-id="8c964-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="8c964-122">**Element**</span></span>|<span data-ttu-id="8c964-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8c964-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8c964-124">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="8c964-124">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="8c964-125">Enthält die Spezifikationen für die Verbindung eines Clients mit dem Clientzugriffsserver.</span><span class="sxs-lookup"><span data-stu-id="8c964-125">Contains the specifications for connecting a client to the Client Access server.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8c964-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8c964-126">Remarks</span></span>

<span data-ttu-id="8c964-127">Das **addressbook** -Element ist in einer Antwort vorhanden, die ein [Protocol (POX)-](protocol-pox.md) Element mit dem **Type** -Attributwert "mapiHttp" aufweist.</span><span class="sxs-lookup"><span data-stu-id="8c964-127">The **AddressBook** element is present in a response that has a [Protocol (POX)](protocol-pox.md) element with a **Type** attribute value of "mapiHttp".</span></span> 
  
<span data-ttu-id="8c964-128">Das **addressbook** -Element steht für Clients zur Verfügung, die das MAPI/http-Protokoll und die Ziel Exchange Online implementieren, Exchange Online im Rahmen von Office 365 und lokalen Versionen von Exchange, beginnend mit Build 15.00.0847.032 (Exchange Server 2013 SP1).</span><span class="sxs-lookup"><span data-stu-id="8c964-128">The **AddressBook** element is available to clients that implement the MAPI/HTTP protocol and target Exchange Online, Exchange Online as part of Office 365, and on-premises versions of Exchange starting with build 15.00.0847.032 (Exchange Server 2013 SP1).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8c964-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8c964-129">See also</span></span>

- [<span data-ttu-id="8c964-130">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="8c964-130">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

