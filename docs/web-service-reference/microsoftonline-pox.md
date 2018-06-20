---
title: MicrosoftOnline (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0b88f02a-9c50-44b3-841b-560b24e37af5
description: Das MicrosoftOnline-Element enthält einen Wert, der angibt, ob das Postfach des Benutzers im Exchange Online gehostet wird oder Exchange Online als Teil von Office 365.
ms.openlocfilehash: b952bfda17b30dcf29812697d225db32718d9781
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830458"
---
# <a name="microsoftonline-pox"></a><span data-ttu-id="cbca5-103">MicrosoftOnline (POX)</span><span class="sxs-lookup"><span data-stu-id="cbca5-103">MicrosoftOnline (POX)</span></span>

<span data-ttu-id="cbca5-104">Das **MicrosoftOnline** -Element enthält einen Wert, der angibt, ob das Postfach des Benutzers im Exchange Online gehostet wird oder Exchange Online als Teil von Office 365.</span><span class="sxs-lookup"><span data-stu-id="cbca5-104">The **MicrosoftOnline** element contains a value that indicates whether the user's mailbox is hosted in Exchange Online or Exchange Online as part of Office 365.</span></span> 
  
[<span data-ttu-id="cbca5-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="cbca5-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="cbca5-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="cbca5-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="cbca5-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="cbca5-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="cbca5-108">MicrosoftOnline (POX)</span><span class="sxs-lookup"><span data-stu-id="cbca5-108">MicrosoftOnline (POX)</span></span>](microsoftonline-pox.md)
  
```XML
<MicrosoftOnline/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="cbca5-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="cbca5-109">Attributes and elements</span></span>

<span data-ttu-id="cbca5-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="cbca5-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cbca5-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="cbca5-111">Attributes</span></span>

<span data-ttu-id="cbca5-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="cbca5-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cbca5-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cbca5-113">Child elements</span></span>

<span data-ttu-id="cbca5-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="cbca5-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="cbca5-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cbca5-115">Parent elements</span></span>

|<span data-ttu-id="cbca5-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="cbca5-116">**Element**</span></span>|<span data-ttu-id="cbca5-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cbca5-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cbca5-118">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="cbca5-118">Account (POX)</span></span>](account-pox.md) <br/> |<span data-ttu-id="cbca5-119">Gibt die kontoeinstellungen für den Benutzer oder Fehlerantworten enthält.</span><span class="sxs-lookup"><span data-stu-id="cbca5-119">Specifies account settings for the user or contains error responses.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cbca5-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="cbca5-120">Remarks</span></span>

<span data-ttu-id="cbca5-121">Der Textwert gibt an, ob das Postfach des Benutzers in Exchange Online gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="cbca5-121">The text value indicates whether the user's mailbox is hosted in Exchange Online.</span></span> <span data-ttu-id="cbca5-122">Der Wert ist **true,** Wenn das Postfach des Benutzers ist im Exchange Online gehostet. anderenfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="cbca5-122">The value is **true** if the user's mailbox is hosted in Exchange Online; otherwise, **false**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cbca5-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cbca5-123">See also</span></span>



[<span data-ttu-id="cbca5-124">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="cbca5-124">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

