---
title: HasBlockedImages
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ddeb11db-797d-4939-91d5-3e44be5f0778
description: Das HasBlockedImages-Element gibt einen Boolean-Wert, der angibt, ob das Element Bilder blockiert wurde.
ms.openlocfilehash: fbe9967c898016aeef27e3c86e8a1cf603bd87fc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19829795"
---
# <a name="hasblockedimages"></a><span data-ttu-id="c94bd-103">HasBlockedImages</span><span class="sxs-lookup"><span data-stu-id="c94bd-103">HasBlockedImages</span></span>

<span data-ttu-id="c94bd-104">Das **HasBlockedImages** -Element gibt einen Boolean-Wert, der angibt, ob das Element Bilder blockiert wurde.</span><span class="sxs-lookup"><span data-stu-id="c94bd-104">The **HasBlockedImages** element specifies a Boolean value that indicates whether the item has blocked images.</span></span> 
  
```XML
<HasBlockedImages> true | false </HasBlockedImages>
```

 <span data-ttu-id="c94bd-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="c94bd-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c94bd-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c94bd-106">Attributes and elements</span></span>

<span data-ttu-id="c94bd-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c94bd-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c94bd-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="c94bd-108">Attributes</span></span>

<span data-ttu-id="c94bd-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="c94bd-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c94bd-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c94bd-110">Child elements</span></span>

<span data-ttu-id="c94bd-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="c94bd-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c94bd-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c94bd-112">Parent elements</span></span>

|<span data-ttu-id="c94bd-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="c94bd-113">**Element**</span></span>|<span data-ttu-id="c94bd-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c94bd-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c94bd-115">Item</span><span class="sxs-lookup"><span data-stu-id="c94bd-115">Item</span></span>](item.md) <br/> |<span data-ttu-id="c94bd-116">Stellt ein generisches Element im Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="c94bd-116">Represents a generic item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c94bd-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="c94bd-117">Text value</span></span>

<span data-ttu-id="c94bd-118">Der Textwert **true** für das **HasBlockedImages** -Element gibt an, dass das Element Bilder blockiert wurde.</span><span class="sxs-lookup"><span data-stu-id="c94bd-118">A text value of **true** for the **HasBlockedImages** element indicates that the item has blocked images.</span></span> <span data-ttu-id="c94bd-119">Der Wert **false** gibt an, dass das Element blockierte Bilder, die nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c94bd-119">A value of **false** indicates that the item does not have any blocked images.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c94bd-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c94bd-120">Remarks</span></span>

<span data-ttu-id="c94bd-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="c94bd-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="c94bd-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="c94bd-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c94bd-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="c94bd-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c94bd-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="c94bd-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c94bd-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c94bd-125">Schema Name</span></span>  <br/> |<span data-ttu-id="c94bd-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="c94bd-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="c94bd-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c94bd-127">Validation File</span></span>  <br/> |<span data-ttu-id="c94bd-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c94bd-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="c94bd-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="c94bd-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="c94bd-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c94bd-130">See also</span></span>



- [<span data-ttu-id="c94bd-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="c94bd-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

