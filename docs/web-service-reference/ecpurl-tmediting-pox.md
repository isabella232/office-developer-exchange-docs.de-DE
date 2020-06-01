---
title: EcpUrl-tmEditing (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1fbc2ea9-3f94-441b-ab42-647326bf0021
description: Das EcpUrl-tmEditing-Element gibt eine partielle URL an, die mit dem Wert des EcpUrl (POX)-Elements kombiniert werden kann, um eine URL zu generieren, die zum Bearbeiten eines vorhandenen websitepostfachs verwendet werden kann.
ms.openlocfilehash: 5d6c6b8e8f73d113cfde3570065435927ffbae05
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463538"
---
# <a name="ecpurl-tmediting-pox"></a><span data-ttu-id="0d4ce-103">EcpUrl-tmEditing (POX)</span><span class="sxs-lookup"><span data-stu-id="0d4ce-103">EcpUrl-tmEditing (POX)</span></span>

<span data-ttu-id="0d4ce-104">Das **EcpUrl-tmEditing-** Element gibt eine partielle URL an, die mit dem Wert des [EcpUrl (POX)](ecpurl-pox.md) -Elements kombiniert werden kann, um eine URL zu generieren, die zum Bearbeiten eines vorhandenen websitepostfachs verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="0d4ce-104">The **EcpUrl-tmEditing** element specifies a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to edit an existing site mailbox.</span></span> 
  
[<span data-ttu-id="0d4ce-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="0d4ce-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="0d4ce-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="0d4ce-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="0d4ce-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="0d4ce-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="0d4ce-108">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="0d4ce-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="0d4ce-109">EcpUrl-tmEditing (POX)</span><span class="sxs-lookup"><span data-stu-id="0d4ce-109">EcpUrl-tmEditing (POX)</span></span>](ecpurl-tmediting-pox.md)
  
```XML
<EcpUrl-tmEditing/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="0d4ce-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="0d4ce-110">Attributes and elements</span></span>

<span data-ttu-id="0d4ce-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="0d4ce-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0d4ce-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="0d4ce-112">Attributes</span></span>

<span data-ttu-id="0d4ce-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="0d4ce-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0d4ce-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0d4ce-114">Child elements</span></span>

<span data-ttu-id="0d4ce-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="0d4ce-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0d4ce-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0d4ce-116">Parent elements</span></span>

|<span data-ttu-id="0d4ce-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="0d4ce-117">**Element**</span></span>|<span data-ttu-id="0d4ce-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0d4ce-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0d4ce-119">Protokoll (POX)</span><span class="sxs-lookup"><span data-stu-id="0d4ce-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="0d4ce-120">Enthält die Spezifikationen für das Verbinden eines Clients mit dem Computer, auf dem Exchange Server ausgeführt wird, auf dem die Clientzugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="0d4ce-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0d4ce-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="0d4ce-121">Text value</span></span>

<span data-ttu-id="0d4ce-122">Der Textwert stellt eine partielle URL dar, die mit dem [EcpUrl (POX)](ecpurl-pox.md) -Elementwert kombiniert werden kann, um eine URL zu generieren, die zum Bearbeiten eines vorhandenen websitepostfachs verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="0d4ce-122">The text value represents a partial URL that can be combined with the [EcpUrl (POX)](ecpurl-pox.md) element's value to generate a URL that can be used to edit an existing site mailbox.</span></span> <span data-ttu-id="0d4ce-123">Der Wert des **EcpUrl-tmEditing-** Elements enthält Parameter, die in "<"-und ">"-Zeichen enthalten sind, die durch den Client ersetzt werden, wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="0d4ce-123">The value of the **EcpUrl-tmEditing** element contains parameters contained within '<' and '>' characters that are substituted by the client as shown in the following table.</span></span> 
  
|<span data-ttu-id="0d4ce-124">**Parameter**</span><span class="sxs-lookup"><span data-stu-id="0d4ce-124">**Parameter**</span></span>|<span data-ttu-id="0d4ce-125">**Ersetzen durch**</span><span class="sxs-lookup"><span data-stu-id="0d4ce-125">**Substitute with**</span></span>|
|:-----|:-----|
| <span data-ttu-id="0d4ce-126">_Id_</span><span class="sxs-lookup"><span data-stu-id="0d4ce-126">_Id_</span></span> <br/> |<span data-ttu-id="0d4ce-127">Die SMTP-e-Mail-Adresse oder der Distinguished Name x500 des websitepostfachs.</span><span class="sxs-lookup"><span data-stu-id="0d4ce-127">The SMTP email address or the X500 distinguished name of the site mailbox.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0d4ce-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0d4ce-128">Remarks</span></span>

<span data-ttu-id="0d4ce-129">Das **EcpUrl-tmEditing-** Element ist ein optionales untergeordnetes Element des **Protocol** -Elements.</span><span class="sxs-lookup"><span data-stu-id="0d4ce-129">The **EcpUrl-tmEditing** element is an optional child element of the **Protocol** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0d4ce-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0d4ce-130">See also</span></span>



[<span data-ttu-id="0d4ce-131">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="0d4ce-131">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

