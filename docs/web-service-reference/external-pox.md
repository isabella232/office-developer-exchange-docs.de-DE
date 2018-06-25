---
title: Externe (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8eed1f79-6eb3-4a88-80fb-d4edf9f34fda
description: Externe Element enthält eine Auflistung von URLs, die ein Client zum Verbinden mit Exchange von außerhalb des Netzwerks der Organisation verwenden können.
ms.openlocfilehash: 7f01fc29b5ce63b02de0a4a6e42887dcffbb4b82
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758358"
---
# <a name="external-pox"></a><span data-ttu-id="53e05-103">Externe (POX)</span><span class="sxs-lookup"><span data-stu-id="53e05-103">External (POX)</span></span>

<span data-ttu-id="53e05-104">**Externes** Element enthält eine Auflistung von URLs, die ein Client zum Verbinden mit Exchange von außerhalb des Netzwerks der Organisation verwenden können.</span><span class="sxs-lookup"><span data-stu-id="53e05-104">The **External** element contains a collection of URLs that a client can use to connect to Exchange from outside of the organization's network.</span></span> 
  
[<span data-ttu-id="53e05-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="53e05-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="53e05-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="53e05-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="53e05-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="53e05-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="53e05-108">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="53e05-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="53e05-109">Externe (POX)</span><span class="sxs-lookup"><span data-stu-id="53e05-109">External (POX)</span></span>](external-pox.md)
  
```XML
<External>
   <OWAUrl/>
   <Protocol>
      <Type/>
      <ASUrl/>
   </Protocol>
</External>

```

## <a name="attributes-and-elements"></a><span data-ttu-id="53e05-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="53e05-110">Attributes and elements</span></span>

<span data-ttu-id="53e05-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="53e05-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="53e05-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="53e05-112">Attributes</span></span>

<span data-ttu-id="53e05-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="53e05-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="53e05-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="53e05-114">Child elements</span></span>

|<span data-ttu-id="53e05-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="53e05-115">**Element**</span></span>|<span data-ttu-id="53e05-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="53e05-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="53e05-117">OWAUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="53e05-117">OWAUrl (POX)</span></span>](owaurl-pox.md) <br/> |<span data-ttu-id="53e05-118">Beschreibt die URL und Authentifizierung Schema, das verwendet wird, auf einen bestimmten Computer zugreifen, der Microsoft Exchange Server ausgeführt wird, hat die Clientzugriffs-Serverrolle installiert, die Outlook Web Access gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="53e05-118">Describes the URL and authentication schema that is used to access a particular computer that is running Microsoft Exchange Server that has the Client Access server role installed that hosts Outlook Web Access.</span></span>  <br/> |
|[<span data-ttu-id="53e05-119">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="53e05-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="53e05-120">Enthält die Spezifikationen für die Verbindung eines Clients mit dem Computer, auf der Microsoft Exchange Server ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="53e05-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span> <span data-ttu-id="53e05-121">Dieses **Protokoll** -Element hat nur zwei untergeordnete Elemente: ein Element einer [Typ (POX)](type-pox.md) , das Verbindungsprotokoll und ein [ASUrl (POX)](asurl-pox.md) -Element, EWS-Endpunkts für den Webdienst Verfügbarkeit angeben.</span><span class="sxs-lookup"><span data-stu-id="53e05-121">This **Protocol** element has only two child elements: a [Type (POX)](type-pox.md) element specifying the connection protocol, and an [ASUrl (POX)](asurl-pox.md) element, specifying the EWS endpoint for the Availability web service.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="53e05-122">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="53e05-122">Parent elements</span></span>

|<span data-ttu-id="53e05-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="53e05-123">**Element**</span></span>|<span data-ttu-id="53e05-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="53e05-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="53e05-125">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="53e05-125">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="53e05-126">Enthält die Spezifikationen für die Verbindung eines Clients mit dem Computer, auf der Microsoft Exchange Server ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="53e05-126">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="53e05-127">Hinweise</span><span class="sxs-lookup"><span data-stu-id="53e05-127">Remarks</span></span>

<span data-ttu-id="53e05-128">**Externes** Element ist ein optionales untergeordnetes Element des **Protokoll** -Elements.</span><span class="sxs-lookup"><span data-stu-id="53e05-128">The **External** element is an optional child element of the **Protocol** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="53e05-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="53e05-129">See also</span></span>



[<span data-ttu-id="53e05-130">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="53e05-130">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

