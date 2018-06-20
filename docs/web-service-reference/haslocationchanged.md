---
title: HasLocationChanged
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5fd465b4-6070-4cd0-9ac3-ed9d2bfd5951
description: Das HasLocationChanged-Element gibt an, ob die Location-Eigenschaft einer Besprechung geändert wurde.
ms.openlocfilehash: dbb811b93149be0bb43fbb2f579a5086a396e401
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19829804"
---
# <a name="haslocationchanged"></a><span data-ttu-id="0890c-103">HasLocationChanged</span><span class="sxs-lookup"><span data-stu-id="0890c-103">HasLocationChanged</span></span>

<span data-ttu-id="0890c-104">Das **HasLocationChanged** -Element gibt an, ob die Location-Eigenschaft einer Besprechung geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="0890c-104">The **HasLocationChanged** element specifies whether the location property of a meeting has changed.</span></span> 
  
```XML
<HasLocationChanged> true | false </HasLocationChanged>
```

 <span data-ttu-id="0890c-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="0890c-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0890c-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="0890c-106">Attributes and elements</span></span>

<span data-ttu-id="0890c-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="0890c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0890c-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="0890c-108">Attributes</span></span>

<span data-ttu-id="0890c-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="0890c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0890c-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0890c-110">Child elements</span></span>

<span data-ttu-id="0890c-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="0890c-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0890c-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0890c-112">Parent elements</span></span>

|<span data-ttu-id="0890c-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="0890c-113">**Element**</span></span>|<span data-ttu-id="0890c-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0890c-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0890c-115">ChangeHighlights</span><span class="sxs-lookup"><span data-stu-id="0890c-115">ChangeHighlights</span></span>](changehighlights.md) <br/> |<span data-ttu-id="0890c-116">Gibt an, was sich zwischen zwei Versionen einer Besprechung geändert hat Request-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="0890c-116">Specifies what has changed between two versions of a meeting request message.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0890c-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="0890c-117">Text value</span></span>

<span data-ttu-id="0890c-118">Der Textwert **true** für das **HasLocationChanged** -Element gibt an, dass die Location-Eigenschaft einer Besprechung geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="0890c-118">A text value of **true** for the **HasLocationChanged** element indicates that the location property of a meeting has changed.</span></span> <span data-ttu-id="0890c-119">Ein Wert **false** gibt an, dass die Location-Eigenschaft einer Besprechung nicht geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="0890c-119">A value **false** indicates that the location property of a meeting has not changed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="0890c-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0890c-120">Remarks</span></span>

<span data-ttu-id="0890c-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0890c-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="0890c-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="0890c-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0890c-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="0890c-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0890c-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="0890c-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0890c-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="0890c-125">Schema Name</span></span>  <br/> |<span data-ttu-id="0890c-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="0890c-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="0890c-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="0890c-127">Validation File</span></span>  <br/> |<span data-ttu-id="0890c-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0890c-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="0890c-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="0890c-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="0890c-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0890c-130">See also</span></span>



- [<span data-ttu-id="0890c-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="0890c-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

