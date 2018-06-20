---
title: RedirectAddr (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 0e9fa6b6-7991-4dc1-a59a-48e5f8e041e4
description: Das RedirectAddr-Element gibt die E-mail-Adresse, die für eine nachfolgende autoermittlungsanforderung verwendet werden soll.
ms.openlocfilehash: fe15054b9962fc2decf52ac3c42536e36358948a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831020"
---
# <a name="redirectaddr-pox"></a><span data-ttu-id="d170a-103">RedirectAddr (POX)</span><span class="sxs-lookup"><span data-stu-id="d170a-103">RedirectAddr (POX)</span></span>

<span data-ttu-id="d170a-104">Das **RedirectAddr** -Element gibt die E-mail-Adresse, die für eine nachfolgende autoermittlungsanforderung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d170a-104">The **RedirectAddr** element specifies the e-mail address that should be used for a subsequent Autodiscover request.</span></span> 
  
[<span data-ttu-id="d170a-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="d170a-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="d170a-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="d170a-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="d170a-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="d170a-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="d170a-108">RedirectAddr (POX)</span><span class="sxs-lookup"><span data-stu-id="d170a-108">RedirectAddr (POX)</span></span>](redirectaddr-pox.md)
  
```xml
<RedirectAddr/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="d170a-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d170a-109">Attributes and elements</span></span>

<span data-ttu-id="d170a-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d170a-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d170a-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="d170a-111">Attributes</span></span>

<span data-ttu-id="d170a-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="d170a-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d170a-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d170a-113">Child elements</span></span>

<span data-ttu-id="d170a-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="d170a-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d170a-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d170a-115">Parent elements</span></span>

|<span data-ttu-id="d170a-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="d170a-116">**Element**</span></span>|<span data-ttu-id="d170a-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d170a-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d170a-118">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="d170a-118">Account (POX)</span></span>](account-pox.md) <br/> |<span data-ttu-id="d170a-119">Gibt die kontoeinstellungen für den Benutzer an.</span><span class="sxs-lookup"><span data-stu-id="d170a-119">Specifies account settings for the user.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d170a-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="d170a-120">Text value</span></span>

<span data-ttu-id="d170a-121">Der Textwert stellt die E-mail-Adresse, die für eine nachfolgende autoermittlungsanforderung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d170a-121">The text value represents the e-mail address that should be used for a subsequent Autodiscover request.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d170a-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d170a-122">Remarks</span></span>

<span data-ttu-id="d170a-123">Wenn dieses Element in der Antwort der AutoErmittlung vorhanden ist, stellen Sie eine weitere Anforderung mithilfe des Textwerts des **RedirectAddr** -Elements.</span><span class="sxs-lookup"><span data-stu-id="d170a-123">If this element is present in the Autodiscover response, make another request by using the text value of the **RedirectAddr** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d170a-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d170a-124">See also</span></span>



[<span data-ttu-id="d170a-125">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="d170a-125">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

