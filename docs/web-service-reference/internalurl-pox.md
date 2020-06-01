---
title: InternalURL (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4649baa9-eec9-426d-952b-361818c25fe0
description: Das InternalURL-Element enthält die URL für das Verbinden eines Clients mit dem Adressbuchserver oder dem Postfach eines Benutzers in der Organisation des Benutzers mithilfe des MAPI/http-Protokolls.
ms.openlocfilehash: 9c6ba621a681ec54d88089de6b7ae1eefdebc679
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465576"
---
# <a name="internalurl-pox"></a><span data-ttu-id="4889d-103">InternalURL (POX)</span><span class="sxs-lookup"><span data-stu-id="4889d-103">InternalUrl (POX)</span></span>

<span data-ttu-id="4889d-104">Das **InternalURL** -Element enthält die URL für das Verbinden eines Clients mit dem Adressbuchserver oder dem Postfach eines Benutzers in der Organisation des Benutzers mithilfe des MAPI/http-Protokolls.</span><span class="sxs-lookup"><span data-stu-id="4889d-104">The **InternalUrl** element contains the URL for connecting a client to the address book server or a user's mailbox from inside the user's organization by using the MAPI/HTTP protocol.</span></span> 
  
```XML
<InternalUrl/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="4889d-105">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="4889d-105">Attributes and elements</span></span>

<span data-ttu-id="4889d-106">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="4889d-106">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4889d-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="4889d-107">Attributes</span></span>

<span data-ttu-id="4889d-108">Keine.</span><span class="sxs-lookup"><span data-stu-id="4889d-108">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4889d-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4889d-109">Child elements</span></span>

<span data-ttu-id="4889d-110">Keine.</span><span class="sxs-lookup"><span data-stu-id="4889d-110">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4889d-111">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4889d-111">Parent elements</span></span>

|<span data-ttu-id="4889d-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="4889d-112">**Element**</span></span>|<span data-ttu-id="4889d-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4889d-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4889d-114">Adressbuch (POX)</span><span class="sxs-lookup"><span data-stu-id="4889d-114">AddressBook (POX)</span></span>](addressbook-pox.md) <br/> |<span data-ttu-id="4889d-115">Enthält die Spezifikationen für die Verbindung eines Clients mit dem Adressbuchserver mithilfe des MAPI/http-Protokolls.</span><span class="sxs-lookup"><span data-stu-id="4889d-115">Contains the specifications for connecting a client to the address book server by using the MAPI/HTTP protocol.</span></span>  <br/> |
|[<span data-ttu-id="4889d-116">MailStore (POX)</span><span class="sxs-lookup"><span data-stu-id="4889d-116">MailStore (POX)</span></span>](mailstore-pox.md) <br/> |<span data-ttu-id="4889d-117">Enthält die Spezifikationen für die Verbindung eines Clients mit dem Postfach des Benutzers mithilfe des MAPI/http-Protokolls.</span><span class="sxs-lookup"><span data-stu-id="4889d-117">Contains the specifications for connecting a client to the user's mailbox by using the MAPI/HTTP protocol.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4889d-118">Textwert</span><span class="sxs-lookup"><span data-stu-id="4889d-118">Text value</span></span>

<span data-ttu-id="4889d-119">Der Textwert stellt eine URL dar, die für den Zugriff auf einen Adressbuchserver oder ein Benutzerpostfach in der Organisation des Benutzers verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="4889d-119">The text value represents a URL that can be used to access an address book server or user's mailbox from inside the user's organization.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4889d-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4889d-120">Remarks</span></span>

<span data-ttu-id="4889d-121">Das **InternalURL** -Element kann in einer Antwort vorhanden sein, die ein [Protocol (POX)-](protocol-pox.md) Element mit dem **Type** -Attributwert "mapiHttp" aufweist.</span><span class="sxs-lookup"><span data-stu-id="4889d-121">The **InternalUrl** element can be present in a response that has a [Protocol (POX)](protocol-pox.md) element with a **Type** attribute value of "mapiHttp".</span></span> 
  
<span data-ttu-id="4889d-122">Das **InternalURL** -Element steht für Clients zur Verfügung, die das MAPI/http-Protokoll und die Ziel Exchange Online implementieren, Exchange Online im Rahmen von Office 365 und lokalen Versionen von Exchange, beginnend mit Build 15.00.0847.032 (Exchange Server 2013 SP1).</span><span class="sxs-lookup"><span data-stu-id="4889d-122">The **InternalUrl** element is available to clients that implement the MAPI/HTTP protocol and target Exchange Online, Exchange Online as part of Office 365, and on-premises versions of Exchange starting with build 15.00.0847.032 (Exchange Server 2013 SP1).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4889d-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4889d-123">See also</span></span>



[<span data-ttu-id="4889d-124">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="4889d-124">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

