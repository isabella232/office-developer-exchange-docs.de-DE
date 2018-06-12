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
ms.openlocfilehash: 5733738d733578c47b849b9d7c62c9b66cd8922e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757457"
---
# <a name="blockstatus"></a><span data-ttu-id="4a16c-103">BlockStatus</span><span class="sxs-lookup"><span data-stu-id="4a16c-103">BlockStatus</span></span>

<span data-ttu-id="4a16c-104">Das **BlockStatus** -Element gibt den Block Status eines Elements an.</span><span class="sxs-lookup"><span data-stu-id="4a16c-104">The **BlockStatus** element specifies the block status of an item.</span></span> 
  
```XML
<BlockStatus> true | false </BlockStatus
```

 <span data-ttu-id="4a16c-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="4a16c-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4a16c-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="4a16c-106">Attributes and elements</span></span>

<span data-ttu-id="4a16c-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="4a16c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4a16c-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="4a16c-108">Attributes</span></span>

<span data-ttu-id="4a16c-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="4a16c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4a16c-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4a16c-110">Child elements</span></span>

<span data-ttu-id="4a16c-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="4a16c-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4a16c-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4a16c-112">Parent elements</span></span>

|<span data-ttu-id="4a16c-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="4a16c-113">**Element**</span></span>|<span data-ttu-id="4a16c-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4a16c-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4a16c-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="4a16c-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="4a16c-116">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="4a16c-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="4a16c-117">Kontaktperson</span><span class="sxs-lookup"><span data-stu-id="4a16c-117">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="4a16c-118">Stellt ein Kontaktelement im Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="4a16c-118">Represents a contact item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="4a16c-119">DistributionList</span><span class="sxs-lookup"><span data-stu-id="4a16c-119">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="4a16c-120">Stellt eine Verteilerliste dar.</span><span class="sxs-lookup"><span data-stu-id="4a16c-120">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="4a16c-121">Element</span><span class="sxs-lookup"><span data-stu-id="4a16c-121">Item</span></span>](item.md) <br/> |<span data-ttu-id="4a16c-122">Stellt ein generisches Element im Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="4a16c-122">Represents a generic item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4a16c-123">Textwert</span><span class="sxs-lookup"><span data-stu-id="4a16c-123">Text value</span></span>

<span data-ttu-id="4a16c-124">Der Textwert **true** für das **BlockStatus** -Element gibt an, dass ein Element ausgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="4a16c-124">A text value of **true** for the **BlockStatus** element indicates that an item is blocked.</span></span> <span data-ttu-id="4a16c-125">Der Wert **false** gibt an, dass ein Element nicht gesperrt ist.</span><span class="sxs-lookup"><span data-stu-id="4a16c-125">A value of **false** indicates that an item is not blocked.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="4a16c-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4a16c-126">Remarks</span></span>

<span data-ttu-id="4a16c-127">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="4a16c-127">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="4a16c-128">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="4a16c-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4a16c-129">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="4a16c-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4a16c-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="4a16c-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4a16c-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="4a16c-131">Schema Name</span></span>  <br/> |<span data-ttu-id="4a16c-132">Typschema</span><span class="sxs-lookup"><span data-stu-id="4a16c-132">Type schema</span></span>  <br/> |
|<span data-ttu-id="4a16c-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="4a16c-133">Validation File</span></span>  <br/> |<span data-ttu-id="4a16c-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4a16c-134">types.xsd</span></span>  <br/> |
|<span data-ttu-id="4a16c-135">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="4a16c-135">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="4a16c-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4a16c-136">See also</span></span>



- [<span data-ttu-id="4a16c-137">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="4a16c-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

