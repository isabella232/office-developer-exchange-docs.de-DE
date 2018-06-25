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
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830946"
---
# <a name="range"></a><span data-ttu-id="34734-103">Range</span><span class="sxs-lookup"><span data-stu-id="34734-103">Range</span></span>

<span data-ttu-id="34734-104">**Range** -Element gibt einen Bereich von Kalender Element Vorkommen eines Serienelements Kalender.</span><span class="sxs-lookup"><span data-stu-id="34734-104">The **Range** element specifies a range of calendar item occurrences for a repeating calendar item.</span></span> 
  
```XML
<Range Start="" End="" Count="" CompareOriginalStartTime=""/>
```

 <span data-ttu-id="34734-105">**OccurrencesRangeType**</span><span class="sxs-lookup"><span data-stu-id="34734-105">**OccurrencesRangeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="34734-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="34734-106">Attributes and elements</span></span>

<span data-ttu-id="34734-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="34734-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="34734-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="34734-108">Attributes</span></span>

|<span data-ttu-id="34734-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="34734-109">**Attribute**</span></span>|<span data-ttu-id="34734-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="34734-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="34734-111">**Start**</span><span class="sxs-lookup"><span data-stu-id="34734-111">**Start**</span></span> <br/> |<span data-ttu-id="34734-112">Der Textwert der **Start** -Attribut ist das Startdatum des sich wiederholenden Bereich.</span><span class="sxs-lookup"><span data-stu-id="34734-112">The text value of the **Start** attribute is the start date of the recurring item range.</span></span> <span data-ttu-id="34734-113">Dies ist ein **DateTime** -Wert.</span><span class="sxs-lookup"><span data-stu-id="34734-113">This is a **dateTime** value.</span></span>  <br/> |
|<span data-ttu-id="34734-114">**End**</span><span class="sxs-lookup"><span data-stu-id="34734-114">**End**</span></span> <br/> |<span data-ttu-id="34734-115">Der Textwert der **End** -Attribut wird das Enddatum des Bereichs sich wiederholenden Element.</span><span class="sxs-lookup"><span data-stu-id="34734-115">The text value of the **End** attribute is the end date of the recurring item range.</span></span> <span data-ttu-id="34734-116">Dies ist ein **DateTime** -Wert.</span><span class="sxs-lookup"><span data-stu-id="34734-116">This is a **dateTime** value.</span></span>  <br/> |
|<span data-ttu-id="34734-117">**Count**</span><span class="sxs-lookup"><span data-stu-id="34734-117">**Count**</span></span> <br/> |<span data-ttu-id="34734-118">Der Textwert der **Count** -Attribut ist die Anzahl der Vorkommen eines wiederkehrenden Objekts.</span><span class="sxs-lookup"><span data-stu-id="34734-118">The text value of the **Count** attribute is the number of occurrences of the recurring item.</span></span> <span data-ttu-id="34734-119">Dies ist eine **ganze** Zahl.</span><span class="sxs-lookup"><span data-stu-id="34734-119">This is an **integer** value.</span></span>  <br/> |
|<span data-ttu-id="34734-120">**CompareOriginalStartTime**</span><span class="sxs-lookup"><span data-stu-id="34734-120">**CompareOriginalStartTime**</span></span> <br/> |<span data-ttu-id="34734-121">Der Textwert der **"true"** für das **CompareOriginalStartTime** -Attribut gibt an, dass der Client die ursprüngliche Startzeit mit den neuen Startzeit verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="34734-121">The text value of **true** for the **CompareOriginalStartTime** attribute indicates that the client should compare the original start time with the new start time.</span></span> <span data-ttu-id="34734-122">Der Wert **false** gibt an, dass der Client nicht notwendigerweise die ursprünglichen Startzeit mit den neuen Startzeit verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="34734-122">A value of **false** indicates that the client does not need to compare the original start time with the new start time.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="34734-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="34734-123">Child elements</span></span>

<span data-ttu-id="34734-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="34734-124">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="34734-125">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="34734-125">Parent elements</span></span>

[<span data-ttu-id="34734-126">Ranges</span><span class="sxs-lookup"><span data-stu-id="34734-126">Ranges</span></span>](ranges.md)
  
## <a name="remarks"></a><span data-ttu-id="34734-127">Hinweise</span><span class="sxs-lookup"><span data-stu-id="34734-127">Remarks</span></span>

<span data-ttu-id="34734-128">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="34734-128">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="34734-129">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="34734-129">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="34734-130">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="34734-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="34734-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="34734-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="34734-132">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="34734-132">Schema name</span></span>  <br/> |<span data-ttu-id="34734-133">Schematypen</span><span class="sxs-lookup"><span data-stu-id="34734-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="34734-134">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="34734-134">Validation file</span></span>  <br/> |<span data-ttu-id="34734-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="34734-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="34734-136">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="34734-136">Can be empty</span></span>  <br/> ||
   

