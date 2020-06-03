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
ms.openlocfilehash: 4f774adcf4a7666f40524931504f1172e15ba24d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462444"
---
# <a name="haslocationchanged"></a><span data-ttu-id="1ef36-103">HasLocationChanged</span><span class="sxs-lookup"><span data-stu-id="1ef36-103">HasLocationChanged</span></span>

<span data-ttu-id="1ef36-104">Das **HasLocationChanged** -Element gibt an, ob die Location-Eigenschaft einer Besprechung geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="1ef36-104">The **HasLocationChanged** element specifies whether the location property of a meeting has changed.</span></span> 
  
```XML
<HasLocationChanged> true | false </HasLocationChanged>
```

 <span data-ttu-id="1ef36-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="1ef36-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1ef36-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1ef36-106">Attributes and elements</span></span>

<span data-ttu-id="1ef36-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1ef36-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1ef36-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="1ef36-108">Attributes</span></span>

<span data-ttu-id="1ef36-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="1ef36-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1ef36-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1ef36-110">Child elements</span></span>

<span data-ttu-id="1ef36-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="1ef36-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1ef36-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1ef36-112">Parent elements</span></span>

|<span data-ttu-id="1ef36-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="1ef36-113">**Element**</span></span>|<span data-ttu-id="1ef36-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1ef36-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1ef36-115">ChangeHighlights</span><span class="sxs-lookup"><span data-stu-id="1ef36-115">ChangeHighlights</span></span>](changehighlights.md) <br/> |<span data-ttu-id="1ef36-116">Gibt an, was zwischen zwei Versionen einer Besprechungsanfrage Nachricht geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="1ef36-116">Specifies what has changed between two versions of a meeting request message.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1ef36-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="1ef36-117">Text value</span></span>

<span data-ttu-id="1ef36-118">Der Textwert **true** für das **HasLocationChanged** -Element gibt an, dass die Location-Eigenschaft einer Besprechung geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="1ef36-118">A text value of **true** for the **HasLocationChanged** element indicates that the location property of a meeting has changed.</span></span> <span data-ttu-id="1ef36-119">Der Wert **false** gibt an, dass die Location-Eigenschaft einer Besprechung nicht geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="1ef36-119">A value **false** indicates that the location property of a meeting has not changed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="1ef36-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1ef36-120">Remarks</span></span>

<span data-ttu-id="1ef36-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="1ef36-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="1ef36-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="1ef36-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1ef36-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="1ef36-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1ef36-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="1ef36-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1ef36-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="1ef36-125">Schema Name</span></span>  <br/> |<span data-ttu-id="1ef36-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="1ef36-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="1ef36-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="1ef36-127">Validation File</span></span>  <br/> |<span data-ttu-id="1ef36-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="1ef36-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="1ef36-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="1ef36-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="1ef36-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1ef36-130">See also</span></span>



- [<span data-ttu-id="1ef36-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="1ef36-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

