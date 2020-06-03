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
description: Das RequestType-Element gibt an, ob es sich bei einer Proxyanforderung um eine Cross-Site-oder eine gesamtstrukturübergreifende Anforderung handelt.
ms.openlocfilehash: 278a65a1f2ce4cb433ae8099703d70d0a2cafa3b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455968"
---
# <a name="requesttype"></a><span data-ttu-id="18d69-103">RequestType</span><span class="sxs-lookup"><span data-stu-id="18d69-103">RequestType</span></span>

<span data-ttu-id="18d69-104">Das **RequestType** -Element gibt an, ob es sich bei einer Proxyanforderung um eine Cross-Site-oder eine gesamtstrukturübergreifende Anforderung handelt.</span><span class="sxs-lookup"><span data-stu-id="18d69-104">The **RequestType** element identifies whether a proxy request is a cross-site or a cross-forest request.</span></span> 
  
```xml
<RequestType>CrossSite or CrossForest</RequestType>
```

 <span data-ttu-id="18d69-105">**AvailabilityProxyRequestType**</span><span class="sxs-lookup"><span data-stu-id="18d69-105">**AvailabilityProxyRequestType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="18d69-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="18d69-106">Attributes and elements</span></span>

<span data-ttu-id="18d69-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="18d69-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="18d69-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="18d69-108">Attributes</span></span>

<span data-ttu-id="18d69-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="18d69-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="18d69-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="18d69-110">Child elements</span></span>

<span data-ttu-id="18d69-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="18d69-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="18d69-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="18d69-112">Parent elements</span></span>

<span data-ttu-id="18d69-113">Dieses Element verfügt nicht über ein übergeordnetes Objekt im Schema.</span><span class="sxs-lookup"><span data-stu-id="18d69-113">This element does not have a parent in the schema.</span></span> <span data-ttu-id="18d69-114">Dieses Element wird im SOAP-Header verwendet.</span><span class="sxs-lookup"><span data-stu-id="18d69-114">This element is used in the SOAP header.</span></span> <span data-ttu-id="18d69-115">Weitere Informationen zur Verwendung dieses Elements finden Sie in der WSDL-Datei.</span><span class="sxs-lookup"><span data-stu-id="18d69-115">For more information about how this element is used, see the WSDL file.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="18d69-116">Textwert</span><span class="sxs-lookup"><span data-stu-id="18d69-116">Text value</span></span>

<span data-ttu-id="18d69-117">Für dieses Element ist ein Textwert erforderlich.</span><span class="sxs-lookup"><span data-stu-id="18d69-117">A text value is required for this element.</span></span> <span data-ttu-id="18d69-118">Im Folgenden sind die möglichen Werte aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="18d69-118">The following are the possible values:</span></span>
  
- <span data-ttu-id="18d69-119">CrossSite</span><span class="sxs-lookup"><span data-stu-id="18d69-119">CrossSite</span></span>
    
- <span data-ttu-id="18d69-120">CrossForest</span><span class="sxs-lookup"><span data-stu-id="18d69-120">CrossForest</span></span>
    
## <a name="element-information"></a><span data-ttu-id="18d69-121">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="18d69-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="18d69-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="18d69-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="18d69-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="18d69-123">Schema name</span></span>  <br/> |<span data-ttu-id="18d69-124">Schematypen</span><span class="sxs-lookup"><span data-stu-id="18d69-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="18d69-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="18d69-125">Validation file</span></span>  <br/> |<span data-ttu-id="18d69-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="18d69-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="18d69-127">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="18d69-127">Can be empty</span></span>  <br/> |<span data-ttu-id="18d69-128">False</span><span class="sxs-lookup"><span data-stu-id="18d69-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="18d69-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="18d69-129">See also</span></span>



- [<span data-ttu-id="18d69-130">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="18d69-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

