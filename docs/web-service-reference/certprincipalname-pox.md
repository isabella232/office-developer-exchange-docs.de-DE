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
description: Das CertPrincipalName-Element gibt den Secure Sockets Layer (SSL) zertifikatprinzipalnamen an, der zum Herstellen einer Verbindung mit der Microsoft Exchange Server 2007 Organisation mithilfe von SSL erforderlich ist.
ms.openlocfilehash: fb2a1c8577bce41945b669be56f2a94a2c4dca26
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463342"
---
# <a name="certprincipalname-pox"></a><span data-ttu-id="af7f5-103">CertPrincipalName (POX)</span><span class="sxs-lookup"><span data-stu-id="af7f5-103">CertPrincipalName (POX)</span></span>

<span data-ttu-id="af7f5-104">Das **CertPrincipalName** -Element gibt den Secure Sockets Layer (SSL) zertifikatprinzipalnamen an, der zum Herstellen einer Verbindung mit der Microsoft Exchange Server 2007 Organisation mithilfe von SSL erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="af7f5-104">The **CertPrincipalName** element specifies the Secure Sockets Layer (SSL) certificate principal name that is required to connect to the Microsoft Exchange Server 2007 organization by using SSL.</span></span> 
  
[<span data-ttu-id="af7f5-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="af7f5-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="af7f5-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="af7f5-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="af7f5-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="af7f5-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="af7f5-108">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="af7f5-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="af7f5-109">CertPrincipalName (POX)</span><span class="sxs-lookup"><span data-stu-id="af7f5-109">CertPrincipalName (POX)</span></span>](certprincipalname-pox.md)
  
```xml
<CertPrincipalName>none or servername</CertPrinicpalName>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="af7f5-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="af7f5-110">Attributes and elements</span></span>

<span data-ttu-id="af7f5-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="af7f5-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="af7f5-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="af7f5-112">Attributes</span></span>

<span data-ttu-id="af7f5-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="af7f5-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="af7f5-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="af7f5-114">Child elements</span></span>

<span data-ttu-id="af7f5-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="af7f5-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="af7f5-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="af7f5-116">Parent elements</span></span>

|<span data-ttu-id="af7f5-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="af7f5-117">**Element**</span></span>|<span data-ttu-id="af7f5-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="af7f5-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="af7f5-119">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="af7f5-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="af7f5-120">Enthält die Spezifikationen für das Verbinden eines Clients mit dem Computer, auf dem Exchange 2007 ausgeführt wird, auf dem die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="af7f5-120">Contains the specifications for connecting a client to the computer that is running Exchange 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="af7f5-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="af7f5-121">Text value</span></span>

<span data-ttu-id="af7f5-122">Der Text-Wert gibt den Namen des SSL-Zertifikat Prinzipals an, der zum Herstellen einer Verbindung mit der Microsoft Exchange Organisation mithilfe von SSL erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="af7f5-122">The text value specifies the SSL certificate principal name that is required to connect to the Microsoft Exchange organization by using SSL.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="af7f5-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="af7f5-123">Remarks</span></span>

<span data-ttu-id="af7f5-124">Wenn das **CertPrincipalName** -Element nicht angegeben ist, wird standardmäßig auf msstd: Server festgelegt, wobei Server der Wert ist, der im [Server (POX)-](server-pox.md) Element angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="af7f5-124">If the **CertPrincipalName** element is not specified, the default is set to msstd:SERVER, where SERVER is the value that is specified in the [Server (POX)](server-pox.md) element.</span></span> <span data-ttu-id="af7f5-125">Wenn beispielsweise Server als example.com angegeben ist und **CertPrincipalName** mit aktiviertem [SSL (POX)](ssl-pox.md) leer gelassen wird, lautet der Standardwert von **CertPrincipalName** msstd:example. com.</span><span class="sxs-lookup"><span data-stu-id="af7f5-125">For example, if SERVER is specified as example.com and **CertPrincipalName** is left blank with [SSL (POX)](ssl-pox.md) turned on, the default value of **CertPrincipalName** would be msstd:example.com.</span></span> 
  
<span data-ttu-id="af7f5-126">Wenn **None** angegeben ist, überprüft Windows den zertifikatprinzipalnamen gemäß den Informationen, die im Thema [Principal Names](https://go.microsoft.com/fwlink/?LinkId=93417) auf MSDN gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="af7f5-126">If **none** is specified, Windows will validate the certificate principal name according to information found in the [Principal Names](https://go.microsoft.com/fwlink/?LinkId=93417) topic on MSDN.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="af7f5-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="af7f5-127">See also</span></span>



[<span data-ttu-id="af7f5-128">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="af7f5-128">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

