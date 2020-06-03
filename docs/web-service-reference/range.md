---
title: Bereich
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ee2891e4-3aa6-4258-9727-1f2ee9622508
description: Das Range-Element gibt einen Bereich von Kalenderelement Vorkommen für ein wiederholtes Kalenderelement an.
ms.openlocfilehash: b5fb41709905290326b47e2662383031c34fd9c9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465310"
---
# <a name="range"></a><span data-ttu-id="c1cb9-103">Bereich</span><span class="sxs-lookup"><span data-stu-id="c1cb9-103">Range</span></span>

<span data-ttu-id="c1cb9-104">Das **Range** -Element gibt einen Bereich von Kalenderelement Vorkommen für ein wiederholtes Kalenderelement an.</span><span class="sxs-lookup"><span data-stu-id="c1cb9-104">The **Range** element specifies a range of calendar item occurrences for a repeating calendar item.</span></span> 
  
```XML
<Range Start="" End="" Count="" CompareOriginalStartTime=""/>
```

 <span data-ttu-id="c1cb9-105">**OccurrencesRangeType**</span><span class="sxs-lookup"><span data-stu-id="c1cb9-105">**OccurrencesRangeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c1cb9-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c1cb9-106">Attributes and elements</span></span>

<span data-ttu-id="c1cb9-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c1cb9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c1cb9-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="c1cb9-108">Attributes</span></span>

|<span data-ttu-id="c1cb9-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="c1cb9-109">**Attribute**</span></span>|<span data-ttu-id="c1cb9-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c1cb9-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c1cb9-111">**Start**</span><span class="sxs-lookup"><span data-stu-id="c1cb9-111">**Start**</span></span> <br/> |<span data-ttu-id="c1cb9-112">Der Textwert des **Start** -Attributs entspricht dem Startdatum des Bereichs für wiederkehrende Elemente.</span><span class="sxs-lookup"><span data-stu-id="c1cb9-112">The text value of the **Start** attribute is the start date of the recurring item range.</span></span> <span data-ttu-id="c1cb9-113">Dies ist ein **DateTime** -Wert.</span><span class="sxs-lookup"><span data-stu-id="c1cb9-113">This is a **dateTime** value.</span></span>  <br/> |
|<span data-ttu-id="c1cb9-114">**End**</span><span class="sxs-lookup"><span data-stu-id="c1cb9-114">**End**</span></span> <br/> |<span data-ttu-id="c1cb9-115">Der Textwert des **End** -Attributs entspricht dem Enddatum des Bereichs für wiederkehrende Elemente.</span><span class="sxs-lookup"><span data-stu-id="c1cb9-115">The text value of the **End** attribute is the end date of the recurring item range.</span></span> <span data-ttu-id="c1cb9-116">Dies ist ein **DateTime** -Wert.</span><span class="sxs-lookup"><span data-stu-id="c1cb9-116">This is a **dateTime** value.</span></span>  <br/> |
|<span data-ttu-id="c1cb9-117">**Count**</span><span class="sxs-lookup"><span data-stu-id="c1cb9-117">**Count**</span></span> <br/> |<span data-ttu-id="c1cb9-118">Der Textwert des **count** -Attributs ist die Anzahl der Vorkommen des wiederkehrenden Elements.</span><span class="sxs-lookup"><span data-stu-id="c1cb9-118">The text value of the **Count** attribute is the number of occurrences of the recurring item.</span></span> <span data-ttu-id="c1cb9-119">Dies ist ein **ganzzahliger** Wert.</span><span class="sxs-lookup"><span data-stu-id="c1cb9-119">This is an **integer** value.</span></span>  <br/> |
|<span data-ttu-id="c1cb9-120">**CompareOriginalStartTime**</span><span class="sxs-lookup"><span data-stu-id="c1cb9-120">**CompareOriginalStartTime**</span></span> <br/> |<span data-ttu-id="c1cb9-121">Der Textwert **true** für das **CompareOriginalStartTime** -Attribut gibt an, dass der Client die ursprüngliche Startzeit mit der neuen Startzeit vergleichen sollte.</span><span class="sxs-lookup"><span data-stu-id="c1cb9-121">The text value of **true** for the **CompareOriginalStartTime** attribute indicates that the client should compare the original start time with the new start time.</span></span> <span data-ttu-id="c1cb9-122">Der Wert **false** gibt an, dass der Client die ursprüngliche Anfangszeit nicht mit der neuen Startzeit vergleichen muss.</span><span class="sxs-lookup"><span data-stu-id="c1cb9-122">A value of **false** indicates that the client does not need to compare the original start time with the new start time.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c1cb9-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c1cb9-123">Child elements</span></span>

<span data-ttu-id="c1cb9-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="c1cb9-124">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c1cb9-125">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c1cb9-125">Parent elements</span></span>

[<span data-ttu-id="c1cb9-126">Ranges</span><span class="sxs-lookup"><span data-stu-id="c1cb9-126">Ranges</span></span>](ranges.md)
  
## <a name="remarks"></a><span data-ttu-id="c1cb9-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c1cb9-127">Remarks</span></span>

<span data-ttu-id="c1cb9-128">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="c1cb9-128">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="c1cb9-129">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="c1cb9-129">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c1cb9-130">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="c1cb9-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c1cb9-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="c1cb9-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c1cb9-132">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c1cb9-132">Schema name</span></span>  <br/> |<span data-ttu-id="c1cb9-133">Schematypen</span><span class="sxs-lookup"><span data-stu-id="c1cb9-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="c1cb9-134">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c1cb9-134">Validation file</span></span>  <br/> |<span data-ttu-id="c1cb9-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c1cb9-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c1cb9-136">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="c1cb9-136">Can be empty</span></span>  <br/> ||
   

