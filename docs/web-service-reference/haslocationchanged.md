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
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462444"
---
# <a name="haslocationchanged"></a><span data-ttu-id="f455a-103">HasLocationChanged</span><span class="sxs-lookup"><span data-stu-id="f455a-103">HasLocationChanged</span></span>

<span data-ttu-id="f455a-104">Das **HasLocationChanged** -Element gibt an, ob die Location-Eigenschaft einer Besprechung geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="f455a-104">The **HasLocationChanged** element specifies whether the location property of a meeting has changed.</span></span> 
  
```XML
<HasLocationChanged> true | false </HasLocationChanged>
```

 <span data-ttu-id="f455a-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="f455a-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f455a-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f455a-106">Attributes and elements</span></span>

<span data-ttu-id="f455a-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f455a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f455a-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="f455a-108">Attributes</span></span>

<span data-ttu-id="f455a-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="f455a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f455a-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f455a-110">Child elements</span></span>

<span data-ttu-id="f455a-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="f455a-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f455a-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f455a-112">Parent elements</span></span>

|<span data-ttu-id="f455a-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="f455a-113">**Element**</span></span>|<span data-ttu-id="f455a-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f455a-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f455a-115">ChangeHighlights</span><span class="sxs-lookup"><span data-stu-id="f455a-115">ChangeHighlights</span></span>](changehighlights.md) <br/> |<span data-ttu-id="f455a-116">Gibt an, was zwischen zwei Versionen einer Besprechungsanfrage Nachricht geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="f455a-116">Specifies what has changed between two versions of a meeting request message.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f455a-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="f455a-117">Text value</span></span>

<span data-ttu-id="f455a-118">Der Textwert **true** für das **HasLocationChanged** -Element gibt an, dass die Location-Eigenschaft einer Besprechung geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="f455a-118">A text value of **true** for the **HasLocationChanged** element indicates that the location property of a meeting has changed.</span></span> <span data-ttu-id="f455a-119">Der Wert **false** gibt an, dass die Location-Eigenschaft einer Besprechung nicht geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="f455a-119">A value **false** indicates that the location property of a meeting has not changed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f455a-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f455a-120">Remarks</span></span>

<span data-ttu-id="f455a-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="f455a-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="f455a-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="f455a-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f455a-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="f455a-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f455a-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="f455a-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f455a-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f455a-125">Schema Name</span></span>  <br/> |<span data-ttu-id="f455a-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="f455a-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="f455a-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f455a-127">Validation File</span></span>  <br/> |<span data-ttu-id="f455a-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="f455a-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="f455a-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="f455a-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="f455a-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f455a-130">See also</span></span>



- [<span data-ttu-id="f455a-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="f455a-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

