---
title: Interne (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 69c22546-ebd6-4a03-b0b4-bbac72ec5551
description: Das internal-Element enthält die Auflistung von URLs, die ein Client für die Verbindung mit Exchange aus dem Netzwerk der Organisation verwenden kann.
ms.openlocfilehash: 8164a018a11f9bae9c3abcbfebf6cf0694ca4183
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465597"
---
# <a name="internal-pox"></a><span data-ttu-id="61d1d-103">Interne (POX)</span><span class="sxs-lookup"><span data-stu-id="61d1d-103">Internal (POX)</span></span>

<span data-ttu-id="61d1d-104">Das **internal** -Element enthält die Auflistung von URLs, die ein Client für die Verbindung mit Exchange aus dem Netzwerk der Organisation verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="61d1d-104">The **Internal** element contains the collection of URLs that a client can use to connect to Exchange from inside the organization's network.</span></span> 
  
[<span data-ttu-id="61d1d-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="61d1d-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="61d1d-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="61d1d-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="61d1d-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="61d1d-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="61d1d-108">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="61d1d-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="61d1d-109">Interne (POX)</span><span class="sxs-lookup"><span data-stu-id="61d1d-109">Internal (POX)</span></span>](internal-pox.md)
  
```xml
<Internal>
   <OWAUrl/>
   <Protocol>
      <Type/>
      <ASUrl/>
   </Protocol>
</Internal>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="61d1d-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="61d1d-110">Attributes and elements</span></span>

<span data-ttu-id="61d1d-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="61d1d-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="61d1d-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="61d1d-112">Attributes</span></span>

<span data-ttu-id="61d1d-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="61d1d-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="61d1d-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="61d1d-114">Child elements</span></span>

|<span data-ttu-id="61d1d-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="61d1d-115">**Element**</span></span>|<span data-ttu-id="61d1d-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="61d1d-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="61d1d-117">OWAUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="61d1d-117">OWAUrl (POX)</span></span>](owaurl-pox.md) <br/> |<span data-ttu-id="61d1d-118">Beschreibt die URL und das Authentifizierungsschema, das für den Zugriff auf einen bestimmten Computer verwendet wird, auf dem Exchange Server ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist, die Outlook Web Access hostet.</span><span class="sxs-lookup"><span data-stu-id="61d1d-118">Describes the URL and authentication schema that is used to access a particular computer that is running Microsoft Exchange Server that has the Client Access server role installed that hosts Outlook Web Access.</span></span>  <br/> |
|[<span data-ttu-id="61d1d-119">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="61d1d-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="61d1d-120">Enthält die Spezifikationen für das Verbinden eines Clients mit dem Computer, auf dem Exchange Server ausgeführt wird, auf dem die Clientzugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="61d1d-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span> <span data-ttu-id="61d1d-121">Dieses **Protokoll** Element hat nur zwei untergeordnete Elemente: ein [Type (POX)](type-pox.md) -Element, das das Verbindungsprotokoll angibt, und ein [vom asurl (POX)](asurl-pox.md) -Element, das den EWS-Endpunkt für den Verfügbarkeits-Webdienst angibt.</span><span class="sxs-lookup"><span data-stu-id="61d1d-121">This **Protocol** element has only two child elements: a [Type (POX)](type-pox.md) element specifying the connection protocol, and an [ASUrl (POX)](asurl-pox.md) element, specifying the EWS endpoint for the Availability web service.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="61d1d-122">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="61d1d-122">Parent elements</span></span>

|<span data-ttu-id="61d1d-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="61d1d-123">**Element**</span></span>|<span data-ttu-id="61d1d-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="61d1d-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="61d1d-125">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="61d1d-125">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="61d1d-126">Enthält die Spezifikationen für das Verbinden eines Clients mit dem Computer, auf dem Exchange Server ausgeführt wird, auf dem die Clientzugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="61d1d-126">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="61d1d-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="61d1d-127">Remarks</span></span>

<span data-ttu-id="61d1d-128">Das **internal** -Element ist ein optionales untergeordnetes Element des **Protocol** -Elements.</span><span class="sxs-lookup"><span data-stu-id="61d1d-128">The **Internal** element is an optional child element of the **Protocol** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="61d1d-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="61d1d-129">See also</span></span>



[<span data-ttu-id="61d1d-130">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="61d1d-130">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

