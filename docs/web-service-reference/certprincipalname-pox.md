---
title: CertPrincipalName (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: a24092c9-58be-4008-92c4-68ec5c6c0fa6
description: Das Element CertPrincipalName gibt den Prinzipal Secure Sockets Layer (SSL) Zertifikat-Namen, der von der Microsoft Exchange Server 2007-Organisation Herstellen einer Verbindung mit SSL erforderlich ist.
ms.openlocfilehash: d2766b16a3e8a1bcd013de332d9c07f709fcf949
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757560"
---
# <a name="certprincipalname-pox"></a><span data-ttu-id="606c1-103">CertPrincipalName (POX)</span><span class="sxs-lookup"><span data-stu-id="606c1-103">CertPrincipalName (POX)</span></span>

<span data-ttu-id="606c1-104">Das Element **CertPrincipalName** gibt den Prinzipal Secure Sockets Layer (SSL) Zertifikat-Namen, der von der Microsoft Exchange Server 2007-Organisation Herstellen einer Verbindung mit SSL erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="606c1-104">The **CertPrincipalName** element specifies the Secure Sockets Layer (SSL) certificate principal name that is required to connect to the Microsoft Exchange Server 2007 organization by using SSL.</span></span> 
  
[<span data-ttu-id="606c1-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="606c1-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="606c1-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="606c1-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="606c1-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="606c1-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="606c1-108">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="606c1-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="606c1-109">CertPrincipalName (POX)</span><span class="sxs-lookup"><span data-stu-id="606c1-109">CertPrincipalName (POX)</span></span>](certprincipalname-pox.md)
  
```xml
<CertPrincipalName>none or servername</CertPrinicpalName>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="606c1-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="606c1-110">Attributes and elements</span></span>

<span data-ttu-id="606c1-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="606c1-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="606c1-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="606c1-112">Attributes</span></span>

<span data-ttu-id="606c1-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="606c1-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="606c1-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="606c1-114">Child elements</span></span>

<span data-ttu-id="606c1-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="606c1-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="606c1-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="606c1-116">Parent elements</span></span>

|<span data-ttu-id="606c1-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="606c1-117">**Element**</span></span>|<span data-ttu-id="606c1-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="606c1-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="606c1-119">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="606c1-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="606c1-120">Enthält die Spezifikationen für die Verbindung eines Clients mit dem Computer mit Exchange 2007, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="606c1-120">Contains the specifications for connecting a client to the computer that is running Exchange 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="606c1-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="606c1-121">Text value</span></span>

<span data-ttu-id="606c1-122">Der Textwert gibt den SSL-Zertifikat principal Name, der von der Microsoft Exchange-Organisation Herstellen einer Verbindung mit SSL erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="606c1-122">The text value specifies the SSL certificate principal name that is required to connect to the Microsoft Exchange organization by using SSL.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="606c1-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="606c1-123">Remarks</span></span>

<span data-ttu-id="606c1-124">Wenn das Element **CertPrincipalName** nicht angegeben wird, ist die Standardeinstellung auf Msstd:SERVER, festlegen SERVER ist, auf dem der Wert, der im [Server (POX)](server-pox.md) -Element angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="606c1-124">If the **CertPrincipalName** element is not specified, the default is set to msstd:SERVER, where SERVER is the value that is specified in the [Server (POX)](server-pox.md) element.</span></span> <span data-ttu-id="606c1-125">Angenommen, wenn der SERVER als example.com angegeben ist, und **CertPrincipalName** mit [SSL (POX)](ssl-pox.md) eingeschaltet ist leer, wäre der Standardwert der **CertPrincipalName** msstd:example.com.</span><span class="sxs-lookup"><span data-stu-id="606c1-125">For example, if SERVER is specified as example.com and **CertPrincipalName** is left blank with [SSL (POX)](ssl-pox.md) turned on, the default value of **CertPrincipalName** would be msstd:example.com.</span></span> 
  
<span data-ttu-id="606c1-126">Wenn **keines** angegeben ist, wird Windows den Prinzipal Zertifikatnamen entsprechend den Informationen im Thema [Dienstprinzipalnamen](http://go.microsoft.com/fwlink/?LinkId=93417) auf MSDN überprüfen.</span><span class="sxs-lookup"><span data-stu-id="606c1-126">If **none** is specified, Windows will validate the certificate principal name according to information found in the [Principal Names](http://go.microsoft.com/fwlink/?LinkId=93417) topic on MSDN.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="606c1-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="606c1-127">See also</span></span>



[<span data-ttu-id="606c1-128">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="606c1-128">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

