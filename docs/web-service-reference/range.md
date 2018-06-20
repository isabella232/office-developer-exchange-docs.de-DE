---
title: Range
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ee2891e4-3aa6-4258-9727-1f2ee9622508
description: Range-Element gibt einen Bereich von Kalender Element Vorkommen eines Serienelements Kalender.
ms.openlocfilehash: 0264c541604808b46a50e292b8ff75f205796295
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830946"
---
# <a name="range"></a><span data-ttu-id="d9d51-103">Range</span><span class="sxs-lookup"><span data-stu-id="d9d51-103">Range</span></span>

<span data-ttu-id="d9d51-104">**Range** -Element gibt einen Bereich von Kalender Element Vorkommen eines Serienelements Kalender.</span><span class="sxs-lookup"><span data-stu-id="d9d51-104">The **Range** element specifies a range of calendar item occurrences for a repeating calendar item.</span></span> 
  
```XML
<Range Start="" End="" Count="" CompareOriginalStartTime=""/>
```

 <span data-ttu-id="d9d51-105">**OccurrencesRangeType**</span><span class="sxs-lookup"><span data-stu-id="d9d51-105">**OccurrencesRangeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d9d51-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d9d51-106">Attributes and elements</span></span>

<span data-ttu-id="d9d51-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d9d51-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d9d51-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d9d51-108">Attributes</span></span>

|<span data-ttu-id="d9d51-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="d9d51-109">**Attribute**</span></span>|<span data-ttu-id="d9d51-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d9d51-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d9d51-111">**Start**</span><span class="sxs-lookup"><span data-stu-id="d9d51-111">**Start**</span></span> <br/> |<span data-ttu-id="d9d51-112">Der Textwert der **Start** -Attribut ist das Startdatum des sich wiederholenden Bereich.</span><span class="sxs-lookup"><span data-stu-id="d9d51-112">The text value of the **Start** attribute is the start date of the recurring item range.</span></span> <span data-ttu-id="d9d51-113">Dies ist ein **DateTime** -Wert.</span><span class="sxs-lookup"><span data-stu-id="d9d51-113">This is a **dateTime** value.</span></span>  <br/> |
|<span data-ttu-id="d9d51-114">**End**</span><span class="sxs-lookup"><span data-stu-id="d9d51-114">**End**</span></span> <br/> |<span data-ttu-id="d9d51-115">Der Textwert der **End** -Attribut wird das Enddatum des Bereichs sich wiederholenden Element.</span><span class="sxs-lookup"><span data-stu-id="d9d51-115">The text value of the **End** attribute is the end date of the recurring item range.</span></span> <span data-ttu-id="d9d51-116">Dies ist ein **DateTime** -Wert.</span><span class="sxs-lookup"><span data-stu-id="d9d51-116">This is a **dateTime** value.</span></span>  <br/> |
|<span data-ttu-id="d9d51-117">**Count**</span><span class="sxs-lookup"><span data-stu-id="d9d51-117">**Count**</span></span> <br/> |<span data-ttu-id="d9d51-118">Der Textwert der **Count** -Attribut ist die Anzahl der Vorkommen eines wiederkehrenden Objekts.</span><span class="sxs-lookup"><span data-stu-id="d9d51-118">The text value of the **Count** attribute is the number of occurrences of the recurring item.</span></span> <span data-ttu-id="d9d51-119">Dies ist eine **ganze** Zahl.</span><span class="sxs-lookup"><span data-stu-id="d9d51-119">This is an **integer** value.</span></span>  <br/> |
|<span data-ttu-id="d9d51-120">**CompareOriginalStartTime**</span><span class="sxs-lookup"><span data-stu-id="d9d51-120">**CompareOriginalStartTime**</span></span> <br/> |<span data-ttu-id="d9d51-121">Der Textwert der **"true"** für das **CompareOriginalStartTime** -Attribut gibt an, dass der Client die ursprüngliche Startzeit mit den neuen Startzeit verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="d9d51-121">The text value of **true** for the **CompareOriginalStartTime** attribute indicates that the client should compare the original start time with the new start time.</span></span> <span data-ttu-id="d9d51-122">Der Wert **false** gibt an, dass der Client nicht notwendigerweise die ursprünglichen Startzeit mit den neuen Startzeit verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="d9d51-122">A value of **false** indicates that the client does not need to compare the original start time with the new start time.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d9d51-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d9d51-123">Child elements</span></span>

<span data-ttu-id="d9d51-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="d9d51-124">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d9d51-125">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d9d51-125">Parent elements</span></span>

[<span data-ttu-id="d9d51-126">Ranges</span><span class="sxs-lookup"><span data-stu-id="d9d51-126">Ranges</span></span>](ranges.md)
  
## <a name="remarks"></a><span data-ttu-id="d9d51-127">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d9d51-127">Remarks</span></span>

<span data-ttu-id="d9d51-128">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d9d51-128">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="d9d51-129">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="d9d51-129">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d9d51-130">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="d9d51-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d9d51-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="d9d51-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d9d51-132">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d9d51-132">Schema name</span></span>  <br/> |<span data-ttu-id="d9d51-133">Schematypen</span><span class="sxs-lookup"><span data-stu-id="d9d51-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="d9d51-134">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d9d51-134">Validation file</span></span>  <br/> |<span data-ttu-id="d9d51-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d9d51-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d9d51-136">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="d9d51-136">Can be empty</span></span>  <br/> ||
   

