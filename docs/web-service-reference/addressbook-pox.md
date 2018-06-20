---
title: AddressBook (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b2d62fd0-741c-4a41-9762-cc7d0ff01c9c
description: Das AddressBook-Element enthält die Spezifikationen für die Verbindung eines Clients mit der Adressbuchserver mithilfe des MAPI/HTTP-Protokolls.
ms.openlocfilehash: c30f0ee7c36de7e63157d07d003a11187d661fd7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757237"
---
# <a name="addressbook-pox"></a><span data-ttu-id="37421-103">AddressBook (POX)</span><span class="sxs-lookup"><span data-stu-id="37421-103">AddressBook (POX)</span></span>

<span data-ttu-id="37421-104">Das **AddressBook** -Element enthält die Spezifikationen für die Verbindung eines Clients mit der Adressbuchserver mithilfe des MAPI/HTTP-Protokolls.</span><span class="sxs-lookup"><span data-stu-id="37421-104">The **AddressBook** element contains the specifications for connecting a client to the address book server by using the MAPI/HTTP protocol.</span></span> 
  
[<span data-ttu-id="37421-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="37421-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="37421-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="37421-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="37421-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="37421-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="37421-108">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="37421-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="37421-109">AddressBook (POX)</span><span class="sxs-lookup"><span data-stu-id="37421-109">AddressBook (POX)</span></span>](addressbook-pox.md)
  
```XML
<AddressBook>
   <ExternalUrl/>
   <InternalUrl/>
</AddressBook>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="37421-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="37421-110">Attributes and elements</span></span>

<span data-ttu-id="37421-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="37421-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="37421-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="37421-112">Attributes</span></span>

<span data-ttu-id="37421-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="37421-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="37421-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="37421-114">Child elements</span></span>

|<span data-ttu-id="37421-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="37421-115">**Element**</span></span>|<span data-ttu-id="37421-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="37421-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="37421-117">ExternalUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="37421-117">ExternalUrl (POX)</span></span>](externalurl-pox.md) <br/> |<span data-ttu-id="37421-118">Enthält die URL, die zum Adressbuch von außerhalb des Netzwerks der Organisation zugreifen, indem Sie mit dem MAPI/HTTP-Protokoll verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="37421-118">Contains the URL that should be used to access the address book from outside the organization's network by using the MAPI/HTTP protocol.</span></span>  <br/> |
|[<span data-ttu-id="37421-119">InternalUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="37421-119">InternalUrl (POX)</span></span>](internalurl-pox.md) <br/> |<span data-ttu-id="37421-120">Enthält die URL, die zum Adressbuch von innerhalb des Netzwerks der Organisation zugreifen, indem Sie mit dem MAPI/HTTP-Protokoll verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="37421-120">Contains the URL that should be used to access the address book from inside the organization's network by using the MAPI/HTTP protocol.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="37421-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="37421-121">Parent elements</span></span>

|<span data-ttu-id="37421-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="37421-122">**Element**</span></span>|<span data-ttu-id="37421-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="37421-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="37421-124">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="37421-124">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="37421-125">Enthält die Spezifikationen für die Verbindung eines Clients mit dem Clientzugriffsserver an.</span><span class="sxs-lookup"><span data-stu-id="37421-125">Contains the specifications for connecting a client to the Client Access server.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="37421-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="37421-126">Remarks</span></span>

<span data-ttu-id="37421-127">**AddressBook** -Element ist in einer Antwort, die ein [Protokoll (POX)](protocol-pox.md) -Element mit dem **Type** -Attributwert "MapiHttp" ist vorhanden.</span><span class="sxs-lookup"><span data-stu-id="37421-127">The **AddressBook** element is present in a response that has a [Protocol (POX)](protocol-pox.md) element with a **Type** attribute value of "mapiHttp".</span></span> 
  
<span data-ttu-id="37421-128">**AddressBook** -Element wird von Clients, mit die die MAPI/HTTP-Protokoll und das Ziel Exchange Online, Exchange Online als Teil von Office 365, implementiert und lokale Versionen von Exchange, beginnend mit erstellen 15.00.0847.032 (Exchange Server 2013 SP1) .</span><span class="sxs-lookup"><span data-stu-id="37421-128">The **AddressBook** element is available to clients that implement the MAPI/HTTP protocol and target Exchange Online, Exchange Online as part of Office 365, and on-premises versions of Exchange starting with build 15.00.0847.032 (Exchange Server 2013 SP1).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="37421-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="37421-129">See also</span></span>

- [<span data-ttu-id="37421-130">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="37421-130">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

