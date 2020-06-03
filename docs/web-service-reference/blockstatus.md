---
title: BlockStatus
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 08556ee9-0923-437c-99a4-bb630f04e973
description: Das BlockStatus-Element gibt den Block Status eines Elements an.
ms.openlocfilehash: e88236274bfa70216e872025c2a94231f837df1f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462276"
---
# <a name="blockstatus"></a><span data-ttu-id="158c5-103">BlockStatus</span><span class="sxs-lookup"><span data-stu-id="158c5-103">BlockStatus</span></span>

<span data-ttu-id="158c5-104">Das **BlockStatus** -Element gibt den Block Status eines Elements an.</span><span class="sxs-lookup"><span data-stu-id="158c5-104">The **BlockStatus** element specifies the block status of an item.</span></span> 
  
```XML
<BlockStatus> true | false </BlockStatus
```

 <span data-ttu-id="158c5-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="158c5-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="158c5-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="158c5-106">Attributes and elements</span></span>

<span data-ttu-id="158c5-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="158c5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="158c5-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="158c5-108">Attributes</span></span>

<span data-ttu-id="158c5-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="158c5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="158c5-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="158c5-110">Child elements</span></span>

<span data-ttu-id="158c5-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="158c5-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="158c5-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="158c5-112">Parent elements</span></span>

|<span data-ttu-id="158c5-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="158c5-113">**Element**</span></span>|<span data-ttu-id="158c5-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="158c5-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="158c5-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="158c5-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="158c5-116">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="158c5-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="158c5-117">Kontaktperson</span><span class="sxs-lookup"><span data-stu-id="158c5-117">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="158c5-118">Stellt ein Kontaktelement im Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="158c5-118">Represents a contact item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="158c5-119">DistributionList</span><span class="sxs-lookup"><span data-stu-id="158c5-119">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="158c5-120">Stellt eine Verteilerliste dar.</span><span class="sxs-lookup"><span data-stu-id="158c5-120">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="158c5-121">Element</span><span class="sxs-lookup"><span data-stu-id="158c5-121">Item</span></span>](item.md) <br/> |<span data-ttu-id="158c5-122">Stellt ein generisches Element in der Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="158c5-122">Represents a generic item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="158c5-123">Textwert</span><span class="sxs-lookup"><span data-stu-id="158c5-123">Text value</span></span>

<span data-ttu-id="158c5-124">Der Textwert **true** für das **BlockStatus** -Element gibt an, dass ein Element blockiert wird.</span><span class="sxs-lookup"><span data-stu-id="158c5-124">A text value of **true** for the **BlockStatus** element indicates that an item is blocked.</span></span> <span data-ttu-id="158c5-125">Der Wert **false** gibt an, dass ein Element nicht blockiert wird.</span><span class="sxs-lookup"><span data-stu-id="158c5-125">A value of **false** indicates that an item is not blocked.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="158c5-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="158c5-126">Remarks</span></span>

<span data-ttu-id="158c5-127">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="158c5-127">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="158c5-128">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="158c5-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="158c5-129">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="158c5-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="158c5-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="158c5-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="158c5-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="158c5-131">Schema Name</span></span>  <br/> |<span data-ttu-id="158c5-132">Typschema</span><span class="sxs-lookup"><span data-stu-id="158c5-132">Type schema</span></span>  <br/> |
|<span data-ttu-id="158c5-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="158c5-133">Validation File</span></span>  <br/> |<span data-ttu-id="158c5-134">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="158c5-134">types.xsd</span></span>  <br/> |
|<span data-ttu-id="158c5-135">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="158c5-135">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="158c5-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="158c5-136">See also</span></span>



- [<span data-ttu-id="158c5-137">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="158c5-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

