---
title: InternalUrl (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4649baa9-eec9-426d-952b-361818c25fe0
description: Das InternalUrl-Element enthält die URL für die Verbindung eines Clients mit der Adressbuchserver oder dem Postfach eines Benutzers von innerhalb der Organisation des Benutzers mithilfe des MAPI/HTTP-Protokolls.
ms.openlocfilehash: 3823236081961128b31bb2c0f563062897c55814
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19829950"
---
# <a name="internalurl-pox"></a><span data-ttu-id="9c7bd-103">InternalUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="9c7bd-103">InternalUrl (POX)</span></span>

<span data-ttu-id="9c7bd-104">Das **InternalUrl** -Element enthält die URL für die Verbindung eines Clients mit der Adressbuchserver oder dem Postfach eines Benutzers von innerhalb der Organisation des Benutzers mithilfe des MAPI/HTTP-Protokolls.</span><span class="sxs-lookup"><span data-stu-id="9c7bd-104">The **InternalUrl** element contains the URL for connecting a client to the address book server or a user's mailbox from inside the user's organization by using the MAPI/HTTP protocol.</span></span> 
  
```XML
<InternalUrl/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="9c7bd-105">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="9c7bd-105">Attributes and elements</span></span>

<span data-ttu-id="9c7bd-106">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="9c7bd-106">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9c7bd-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="9c7bd-107">Attributes</span></span>

<span data-ttu-id="9c7bd-108">Keine.</span><span class="sxs-lookup"><span data-stu-id="9c7bd-108">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9c7bd-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9c7bd-109">Child elements</span></span>

<span data-ttu-id="9c7bd-110">Keine.</span><span class="sxs-lookup"><span data-stu-id="9c7bd-110">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9c7bd-111">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9c7bd-111">Parent elements</span></span>

|<span data-ttu-id="9c7bd-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="9c7bd-112">**Element**</span></span>|<span data-ttu-id="9c7bd-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9c7bd-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9c7bd-114">AddressBook (POX)</span><span class="sxs-lookup"><span data-stu-id="9c7bd-114">AddressBook (POX)</span></span>](addressbook-pox.md) <br/> |<span data-ttu-id="9c7bd-115">Enthält die Spezifikationen für die Verbindung eines Clients mit der Adressbuchserver mithilfe des MAPI/HTTP-Protokolls.</span><span class="sxs-lookup"><span data-stu-id="9c7bd-115">Contains the specifications for connecting a client to the address book server by using the MAPI/HTTP protocol.</span></span>  <br/> |
|[<span data-ttu-id="9c7bd-116">Postspeicher weitergeleitet (POX)</span><span class="sxs-lookup"><span data-stu-id="9c7bd-116">MailStore (POX)</span></span>](mailstore-pox.md) <br/> |<span data-ttu-id="9c7bd-117">Enthält die Spezifikationen für die Verbindung eines Clients an das Postfach des Benutzers mithilfe des MAPI/HTTP-Protokolls.</span><span class="sxs-lookup"><span data-stu-id="9c7bd-117">Contains the specifications for connecting a client to the user's mailbox by using the MAPI/HTTP protocol.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="9c7bd-118">Textwert</span><span class="sxs-lookup"><span data-stu-id="9c7bd-118">Text value</span></span>

<span data-ttu-id="9c7bd-119">Der Textwert stellt eine URL, die Zugriff auf eine Adressbuchserver oder Postfach des Benutzers aus innerhalb der Organisation des Benutzers verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="9c7bd-119">The text value represents a URL that can be used to access an address book server or user's mailbox from inside the user's organization.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9c7bd-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9c7bd-120">Remarks</span></span>

<span data-ttu-id="9c7bd-121">Das Element **InternalUrl** kann in einer Antwort vorhanden sein, die ein [Protokoll (POX)](protocol-pox.md) -Element mit dem Wert **Type** -Attribut "MapiHttp" hat.</span><span class="sxs-lookup"><span data-stu-id="9c7bd-121">The **InternalUrl** element can be present in a response that has a [Protocol (POX)](protocol-pox.md) element with a **Type** attribute value of "mapiHttp".</span></span> 
  
<span data-ttu-id="9c7bd-122">Das **InternalUrl** -Element wird von Clients, mit die die MAPI/HTTP-Protokoll und das Ziel Exchange Online, Exchange Online als Teil von Office 365, implementiert und lokale Versionen von Exchange, beginnend mit erstellen 15.00.0847.032 (Exchange Server 2013 SP1) .</span><span class="sxs-lookup"><span data-stu-id="9c7bd-122">The **InternalUrl** element is available to clients that implement the MAPI/HTTP protocol and target Exchange Online, Exchange Online as part of Office 365, and on-premises versions of Exchange starting with build 15.00.0847.032 (Exchange Server 2013 SP1).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9c7bd-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9c7bd-123">See also</span></span>



[<span data-ttu-id="9c7bd-124">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="9c7bd-124">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

