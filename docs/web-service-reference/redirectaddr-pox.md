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
description: Das RedirectAddr-Element gibt die e-Mail-Adresse an, die für eine nachfolgende Auto Ermittlungsanforderung verwendet werden soll.
ms.openlocfilehash: 6bff28001851f421b4c7429770185401f2f0a743
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529875"
---
# <a name="redirectaddr-pox"></a><span data-ttu-id="9a6b0-103">RedirectAddr (POX)</span><span class="sxs-lookup"><span data-stu-id="9a6b0-103">RedirectAddr (POX)</span></span>

<span data-ttu-id="9a6b0-104">Das **RedirectAddr** -Element gibt die e-Mail-Adresse an, die für eine nachfolgende Auto Ermittlungsanforderung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9a6b0-104">The **RedirectAddr** element specifies the e-mail address that should be used for a subsequent Autodiscover request.</span></span> 
  
[<span data-ttu-id="9a6b0-105">AutoErmittlung (POX)</span><span class="sxs-lookup"><span data-stu-id="9a6b0-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="9a6b0-106">Response (POX)</span><span class="sxs-lookup"><span data-stu-id="9a6b0-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="9a6b0-107">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="9a6b0-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="9a6b0-108">RedirectAddr (POX)</span><span class="sxs-lookup"><span data-stu-id="9a6b0-108">RedirectAddr (POX)</span></span>](redirectaddr-pox.md)
  
```xml
<RedirectAddr/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="9a6b0-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="9a6b0-109">Attributes and elements</span></span>

<span data-ttu-id="9a6b0-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="9a6b0-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9a6b0-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="9a6b0-111">Attributes</span></span>

<span data-ttu-id="9a6b0-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="9a6b0-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9a6b0-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9a6b0-113">Child elements</span></span>

<span data-ttu-id="9a6b0-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="9a6b0-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9a6b0-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9a6b0-115">Parent elements</span></span>

|<span data-ttu-id="9a6b0-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="9a6b0-116">**Element**</span></span>|<span data-ttu-id="9a6b0-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9a6b0-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9a6b0-118">Konto (POX)</span><span class="sxs-lookup"><span data-stu-id="9a6b0-118">Account (POX)</span></span>](account-pox.md) <br/> |<span data-ttu-id="9a6b0-119">Gibt Kontoeinstellungen für den Benutzer an.</span><span class="sxs-lookup"><span data-stu-id="9a6b0-119">Specifies account settings for the user.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="9a6b0-120">Textwert</span><span class="sxs-lookup"><span data-stu-id="9a6b0-120">Text value</span></span>

<span data-ttu-id="9a6b0-121">Der Wert Text stellt die e-Mail-Adresse dar, die für eine nachfolgende Auto Ermittlungsanforderung verwendet werden sollte.</span><span class="sxs-lookup"><span data-stu-id="9a6b0-121">The text value represents the e-mail address that should be used for a subsequent Autodiscover request.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9a6b0-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9a6b0-122">Remarks</span></span>

<span data-ttu-id="9a6b0-123">Wenn dieses Element in der Auto Ermittlungs Antwort vorhanden ist, stellen Sie eine weitere Anforderung mithilfe des Textwerts des **RedirectAddr** -Elements.</span><span class="sxs-lookup"><span data-stu-id="9a6b0-123">If this element is present in the Autodiscover response, make another request by using the text value of the **RedirectAddr** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9a6b0-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9a6b0-124">See also</span></span>



[<span data-ttu-id="9a6b0-125">POX Autodiscover XML-Elemente für Exchange</span><span class="sxs-lookup"><span data-stu-id="9a6b0-125">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

