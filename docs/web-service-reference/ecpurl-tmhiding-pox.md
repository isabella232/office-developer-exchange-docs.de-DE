---
title: EcpUrl-TmHiding (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b9ae15b-3ac1-45ac-85ba-38c7231fe508
description: Das EcpUrl TmHiding-Element gibt eine partielle URL, die kombiniert werden kann, mit dem EcpUrl (POX) Elementwert generiert eine URL, die die Benutzer von einem websitepostfach Kündigen des Abonnements verwendet werden können.
ms.openlocfilehash: 461e9780dbd657ba0ba8b9ce9ea4fe902cba9698
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758132"
---
# <a name="ecpurl-tmhiding-pox"></a><span data-ttu-id="d805d-103">EcpUrl-TmHiding (POX)</span><span class="sxs-lookup"><span data-stu-id="d805d-103">EcpUrl-tmHiding (POX)</span></span>

<span data-ttu-id="d805d-104">Das **EcpUrl TmHiding** -Element gibt eine partielle URL, die kombiniert werden kann, mit dem [EcpUrl (POX)](ecpurl-pox.md) Elementwert generiert eine URL, die die Benutzer von einem websitepostfach Kündigen des Abonnements verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="d805d-104">The **EcpUrl-tmHiding** element specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to unsubscribe the user from a site mailbox.</span></span> 
  
[<span data-ttu-id="d805d-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="d805d-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="d805d-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="d805d-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="d805d-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="d805d-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="d805d-108">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="d805d-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="d805d-109">EcpUrl-TmHiding (POX)</span><span class="sxs-lookup"><span data-stu-id="d805d-109">EcpUrl-tmHiding (POX)</span></span>](ecpurl-tmhiding-pox.md)
  
```XML
<EcpUrl-tmHiding/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="d805d-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d805d-110">Attributes and elements</span></span>

<span data-ttu-id="d805d-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d805d-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d805d-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="d805d-112">Attributes</span></span>

<span data-ttu-id="d805d-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="d805d-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d805d-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d805d-114">Child elements</span></span>

<span data-ttu-id="d805d-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="d805d-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d805d-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d805d-116">Parent elements</span></span>

|<span data-ttu-id="d805d-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="d805d-117">**Element**</span></span>|<span data-ttu-id="d805d-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d805d-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d805d-119">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="d805d-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="d805d-120">Enthält die Spezifikationen für die Verbindung eines Clients mit dem Computer, auf der Microsoft Exchange Server ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="d805d-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d805d-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="d805d-121">Text value</span></span>

<span data-ttu-id="d805d-122">Der Textwert stellt eine partielle URL, die kombiniert werden kann, mit dem [EcpUrl (POX)](ecpurl-pox.md) Elementwert generiert eine URL, die die Benutzer von einem websitepostfach Kündigen des Abonnements verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="d805d-122">The text value represents a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to unsubscribe the user from a site mailbox.</span></span> <span data-ttu-id="d805d-123">Der Wert des **EcpUrl TmHiding** -Elements enthält Parameter enthaltenen ' <' und ' >' Zeichen, die vom Client ersetzt werden, wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="d805d-123">The value of the **EcpUrl-tmHiding** element contains parameters contained within '<' and '>' characters that are substituted by the client as shown in the following table.</span></span> 
  
|<span data-ttu-id="d805d-124">**Parameter**</span><span class="sxs-lookup"><span data-stu-id="d805d-124">**Parameter**</span></span>|<span data-ttu-id="d805d-125">**Ersetzen durch**</span><span class="sxs-lookup"><span data-stu-id="d805d-125">**Substitute with**</span></span>|
|:-----|:-----|
| <span data-ttu-id="d805d-126">
  _ID_</span><span class="sxs-lookup"><span data-stu-id="d805d-126">_Id_</span></span> <br/> |<span data-ttu-id="d805d-127">Die SMTP-e-Mail-Adresse oder die X500 distinguished Name des websitepostfachs.</span><span class="sxs-lookup"><span data-stu-id="d805d-127">The SMTP email address or the X500 distinguished name of the site mailbox.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d805d-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d805d-128">Remarks</span></span>

<span data-ttu-id="d805d-129">Das **EcpUrl TmHiding** -Element ist ein optionales untergeordnetes Element des **Protokoll** -Elements.</span><span class="sxs-lookup"><span data-stu-id="d805d-129">The **EcpUrl-tmHiding** element is an optional child element of the **Protocol** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d805d-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d805d-130">See also</span></span>



[<span data-ttu-id="d805d-131">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="d805d-131">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

