---
title: ExternalURL (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3b647d88-6feb-40d7-9299-b2ca47b707db
description: Das ExternalURL-Element enthält die URL für das Verbinden eines Clients mit dem Adressbuchserver oder einem Benutzerpostfach von außerhalb der Organisation des Benutzers mithilfe des MAPI/http-Protokolls.
ms.openlocfilehash: 94265051be68ed06d1dab8d46dd4ce29d8694c93
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457956"
---
# <a name="externalurl-pox"></a><span data-ttu-id="8f032-103">ExternalURL (POX)</span><span class="sxs-lookup"><span data-stu-id="8f032-103">ExternalUrl (POX)</span></span>

<span data-ttu-id="8f032-104">Das **ExternalURL** -Element enthält die URL für das Verbinden eines Clients mit dem Adressbuchserver oder einem Benutzerpostfach von außerhalb der Organisation des Benutzers mithilfe des MAPI/http-Protokolls.</span><span class="sxs-lookup"><span data-stu-id="8f032-104">The **ExternalUrl** element contains the URL for connecting a client to the address book server or a user's mailbox from outside the user's organization by using the MAPI/HTTP protocol.</span></span> 
  
```XML
<ExternalUrl/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="8f032-105">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="8f032-105">Attributes and elements</span></span>

<span data-ttu-id="8f032-106">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="8f032-106">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8f032-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="8f032-107">Attributes</span></span>

<span data-ttu-id="8f032-108">Keine.</span><span class="sxs-lookup"><span data-stu-id="8f032-108">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8f032-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8f032-109">Child elements</span></span>

<span data-ttu-id="8f032-110">Keine.</span><span class="sxs-lookup"><span data-stu-id="8f032-110">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8f032-111">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8f032-111">Parent elements</span></span>

|<span data-ttu-id="8f032-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="8f032-112">**Element**</span></span>|<span data-ttu-id="8f032-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8f032-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8f032-114">Adressbuch (POX)</span><span class="sxs-lookup"><span data-stu-id="8f032-114">AddressBook (POX)</span></span>](addressbook-pox.md) <br/> |<span data-ttu-id="8f032-115">Enthält die Spezifikationen für die Verbindung eines Clients mit dem Adressbuchserver mithilfe des MAPI/http-Protokolls.</span><span class="sxs-lookup"><span data-stu-id="8f032-115">Contains the specifications for connecting a client to the address book server by using the MAPI/HTTP protocol.</span></span>  <br/> |
|[<span data-ttu-id="8f032-116">MailStore (POX)</span><span class="sxs-lookup"><span data-stu-id="8f032-116">MailStore (POX)</span></span>](mailstore-pox.md) <br/> |<span data-ttu-id="8f032-117">Enthält die Spezifikationen für die Verbindung eines Clients mit dem Postfach des Benutzers mithilfe des MAPI/http-Protokolls.</span><span class="sxs-lookup"><span data-stu-id="8f032-117">Contains the specifications for connecting a client to the user's mailbox by using the MAPI/HTTP protocol.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="8f032-118">Textwert</span><span class="sxs-lookup"><span data-stu-id="8f032-118">Text value</span></span>

<span data-ttu-id="8f032-119">Der Wert Text stellt eine URL dar, die für den Zugriff auf einen Adressbuchserver oder ein Benutzerpostfach von außerhalb der Organisation des Benutzers verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="8f032-119">The text value represents a URL that can be used to access an address book server or user's mailbox from outside the user's organization.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8f032-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8f032-120">Remarks</span></span>

<span data-ttu-id="8f032-121">Das **ExternalURL** -Element kann in einer Antwort vorhanden sein, die ein [Protocol (POX)-](protocol-pox.md) Element mit dem **Type** -Attributwert "mapiHttp" aufweist.</span><span class="sxs-lookup"><span data-stu-id="8f032-121">The **ExternalUrl** element can be present in a response that has a [Protocol (POX)](protocol-pox.md) element with a **Type** attribute value of "mapiHttp".</span></span> 
  
<span data-ttu-id="8f032-122">Das **ExternalURL** -Element steht für Clients zur Verfügung, die das MAPI/http-Protokoll und die Ziel Exchange Online implementieren, Exchange Online im Rahmen von Office 365 und lokalen Versionen von Exchange, beginnend mit Build 15.00.0847.032 (Exchange Server 2013 SP1).</span><span class="sxs-lookup"><span data-stu-id="8f032-122">The **ExternalUrl** element is available to clients that implement the MAPI/HTTP protocol and target Exchange Online, Exchange Online as part of Office 365, and on-premises versions of Exchange starting with build 15.00.0847.032 (Exchange Server 2013 SP1).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8f032-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8f032-123">See also</span></span>



[<span data-ttu-id="8f032-124">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="8f032-124">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

