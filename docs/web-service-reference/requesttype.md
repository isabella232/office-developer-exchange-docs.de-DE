---
title: RequestType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RequestType
api_type:
- schema
ms.assetid: 4e657e57-528f-4250-a99c-f9850bbbcec5
description: Das RequestType-Element angibt, ob eine Proxyanforderung einer Cross-Site oder einer gesamtstrukturübergreifenden Anforderung ist.
ms.openlocfilehash: 96a4d57432b15aa54fff2618df458fc75cb227f3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831139"
---
# <a name="requesttype"></a><span data-ttu-id="9ddce-103">RequestType</span><span class="sxs-lookup"><span data-stu-id="9ddce-103">RequestType</span></span>

<span data-ttu-id="9ddce-104">Das **RequestType** -Element angibt, ob eine Proxyanforderung einer Cross-Site oder einer gesamtstrukturübergreifenden Anforderung ist.</span><span class="sxs-lookup"><span data-stu-id="9ddce-104">The **RequestType** element identifies whether a proxy request is a cross-site or a cross-forest request.</span></span> 
  
```xml
<RequestType>CrossSite or CrossForest</RequestType>
```

 <span data-ttu-id="9ddce-105">**AvailabilityProxyRequestType**</span><span class="sxs-lookup"><span data-stu-id="9ddce-105">**AvailabilityProxyRequestType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9ddce-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="9ddce-106">Attributes and elements</span></span>

<span data-ttu-id="9ddce-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="9ddce-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9ddce-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="9ddce-108">Attributes</span></span>

<span data-ttu-id="9ddce-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="9ddce-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9ddce-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9ddce-110">Child elements</span></span>

<span data-ttu-id="9ddce-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="9ddce-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9ddce-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9ddce-112">Parent elements</span></span>

<span data-ttu-id="9ddce-113">Dieses Element muss ein übergeordnetes Element nicht im Schema.</span><span class="sxs-lookup"><span data-stu-id="9ddce-113">This element does not have a parent in the schema.</span></span> <span data-ttu-id="9ddce-114">Dieses Element wird in den SOAP-Header verwendet.</span><span class="sxs-lookup"><span data-stu-id="9ddce-114">This element is used in the SOAP header.</span></span> <span data-ttu-id="9ddce-115">Weitere Informationen zur Verwendung dieses Elements finden Sie unter der WSDL-Datei.</span><span class="sxs-lookup"><span data-stu-id="9ddce-115">For more information about how this element is used, see the WSDL file.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="9ddce-116">Textwert</span><span class="sxs-lookup"><span data-stu-id="9ddce-116">Text value</span></span>

<span data-ttu-id="9ddce-117">Es wird ein Textwert für dieses Element erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9ddce-117">A text value is required for this element.</span></span> <span data-ttu-id="9ddce-118">Im Folgenden sind die möglichen Werte aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="9ddce-118">The following are the possible values:</span></span>
  
- <span data-ttu-id="9ddce-119">CrossSite</span><span class="sxs-lookup"><span data-stu-id="9ddce-119">CrossSite</span></span>
    
- <span data-ttu-id="9ddce-120">CrossForest</span><span class="sxs-lookup"><span data-stu-id="9ddce-120">CrossForest</span></span>
    
## <a name="element-information"></a><span data-ttu-id="9ddce-121">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="9ddce-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9ddce-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="9ddce-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9ddce-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="9ddce-123">Schema name</span></span>  <br/> |<span data-ttu-id="9ddce-124">Schematypen</span><span class="sxs-lookup"><span data-stu-id="9ddce-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="9ddce-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="9ddce-125">Validation file</span></span>  <br/> |<span data-ttu-id="9ddce-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9ddce-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9ddce-127">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="9ddce-127">Can be empty</span></span>  <br/> |<span data-ttu-id="9ddce-128">False</span><span class="sxs-lookup"><span data-stu-id="9ddce-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9ddce-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9ddce-129">See also</span></span>



- [<span data-ttu-id="9ddce-130">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="9ddce-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

