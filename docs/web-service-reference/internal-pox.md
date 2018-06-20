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
description: Das interne Element enthält die Auflistung von URLs, die ein Client zum Verbinden mit Exchange von innerhalb des Netzwerks der Organisation verwenden können.
ms.openlocfilehash: 0dc5b679af98b52f15ef3b40181c2d97f102f373
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19829946"
---
# <a name="internal-pox"></a><span data-ttu-id="d7925-103">Interne (POX)</span><span class="sxs-lookup"><span data-stu-id="d7925-103">Internal (POX)</span></span>

<span data-ttu-id="d7925-104">Das **Internal** -Element enthält die Auflistung von URLs, die ein Client zum Verbinden mit Exchange von innerhalb des Netzwerks der Organisation verwenden können.</span><span class="sxs-lookup"><span data-stu-id="d7925-104">The **Internal** element contains the collection of URLs that a client can use to connect to Exchange from inside the organization's network.</span></span> 
  
[<span data-ttu-id="d7925-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="d7925-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="d7925-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="d7925-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="d7925-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="d7925-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="d7925-108">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="d7925-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="d7925-109">Interne (POX)</span><span class="sxs-lookup"><span data-stu-id="d7925-109">Internal (POX)</span></span>](internal-pox.md)
  
```xml
<Internal>
   <OWAUrl/>
   <Protocol>
      <Type/>
      <ASUrl/>
   </Protocol>
</Internal>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="d7925-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d7925-110">Attributes and elements</span></span>

<span data-ttu-id="d7925-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d7925-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d7925-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="d7925-112">Attributes</span></span>

<span data-ttu-id="d7925-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="d7925-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d7925-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d7925-114">Child elements</span></span>

|<span data-ttu-id="d7925-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="d7925-115">**Element**</span></span>|<span data-ttu-id="d7925-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d7925-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d7925-117">OWAUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="d7925-117">OWAUrl (POX)</span></span>](owaurl-pox.md) <br/> |<span data-ttu-id="d7925-118">Beschreibt die URL und Authentifizierung Schema, das verwendet wird, auf einen bestimmten Computer zugreifen, der Microsoft Exchange Server ausgeführt wird, hat die Clientzugriffs-Serverrolle installiert, die Outlook Web Access gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="d7925-118">Describes the URL and authentication schema that is used to access a particular computer that is running Microsoft Exchange Server that has the Client Access server role installed that hosts Outlook Web Access.</span></span>  <br/> |
|[<span data-ttu-id="d7925-119">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="d7925-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="d7925-120">Enthält die Spezifikationen für die Verbindung eines Clients mit dem Computer, auf der Microsoft Exchange Server ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="d7925-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span> <span data-ttu-id="d7925-121">Dieses **Protokoll** -Element hat nur zwei untergeordnete Elemente: ein Element einer [Typ (POX)](type-pox.md) , das Verbindungsprotokoll und ein [ASUrl (POX)](asurl-pox.md) -Element, EWS-Endpunkts für den Webdienst Verfügbarkeit angeben.</span><span class="sxs-lookup"><span data-stu-id="d7925-121">This **Protocol** element has only two child elements: a [Type (POX)](type-pox.md) element specifying the connection protocol, and an [ASUrl (POX)](asurl-pox.md) element, specifying the EWS endpoint for the Availability web service.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d7925-122">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d7925-122">Parent elements</span></span>

|<span data-ttu-id="d7925-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="d7925-123">**Element**</span></span>|<span data-ttu-id="d7925-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d7925-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d7925-125">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="d7925-125">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="d7925-126">Enthält die Spezifikationen für die Verbindung eines Clients mit dem Computer, auf der Microsoft Exchange Server ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="d7925-126">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d7925-127">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d7925-127">Remarks</span></span>

<span data-ttu-id="d7925-128">Das **Internal** -Element ist ein optionales untergeordnetes Element des **Protokoll** -Elements.</span><span class="sxs-lookup"><span data-stu-id="d7925-128">The **Internal** element is an optional child element of the **Protocol** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d7925-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d7925-129">See also</span></span>



[<span data-ttu-id="d7925-130">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="d7925-130">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

