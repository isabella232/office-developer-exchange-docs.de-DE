---
title: RecurringMasterItemIdRanges
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5c9c89b5-4ce8-437b-a332-fa7ed35c8388
description: Das RecurringMasterItemIdRanges-Element gibt ein Array von Bereichen vorkommen.
ms.openlocfilehash: 60d987f475bed5d630a1238550e4d14578ebd0d5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831016"
---
# <a name="recurringmasteritemidranges"></a><span data-ttu-id="47573-103">RecurringMasterItemIdRanges</span><span class="sxs-lookup"><span data-stu-id="47573-103">RecurringMasterItemIdRanges</span></span>

<span data-ttu-id="47573-104">Das **RecurringMasterItemIdRanges** -Element gibt ein Array von Bereichen vorkommen.</span><span class="sxs-lookup"><span data-stu-id="47573-104">The **RecurringMasterItemIdRanges** element specifies an array of occurrence ranges.</span></span> 
  
```XML
<RecurringMasterItemIdRanges Id="" ChangeKey="">
   <Ranges/>
</RecurringMasterItemIdRanges>
```

 <span data-ttu-id="47573-105">**RecurringMasterItemIdRangesType**</span><span class="sxs-lookup"><span data-stu-id="47573-105">**RecurringMasterItemIdRangesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="47573-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="47573-106">Attributes and elements</span></span>

<span data-ttu-id="47573-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="47573-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="47573-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="47573-108">Attributes</span></span>

|<span data-ttu-id="47573-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="47573-109">**Attribute**</span></span>|<span data-ttu-id="47573-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="47573-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="47573-111">**Id**</span><span class="sxs-lookup"><span data-stu-id="47573-111">**Id**</span></span> <br/> |<span data-ttu-id="47573-112">Der Textwert des **Id** -Attributs ist Eindeutiger Bezeichner für ein wiederkehrendes master-Objekt.</span><span class="sxs-lookup"><span data-stu-id="47573-112">The text value of the **Id** attribute is a recurring master item's unique identifier.</span></span> <span data-ttu-id="47573-113">Dies ist ein **String** -Wert.</span><span class="sxs-lookup"><span data-stu-id="47573-113">This is a **string** value.</span></span>  <br/> |
|<span data-ttu-id="47573-114">**ChangeKey**</span><span class="sxs-lookup"><span data-stu-id="47573-114">**ChangeKey**</span></span> <br/> |<span data-ttu-id="47573-115">Der Textwert des Attributs **ChangeKey** ist der wiederkehrenden master Schlüssel des Elements ändern.</span><span class="sxs-lookup"><span data-stu-id="47573-115">The text value of the **ChangeKey** attribute is the recurring master item's change key.</span></span> <span data-ttu-id="47573-116">Dies ist ein **String** -Wert.</span><span class="sxs-lookup"><span data-stu-id="47573-116">This is a **string** value.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="47573-117">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="47573-117">Child elements</span></span>

[<span data-ttu-id="47573-118">Ranges</span><span class="sxs-lookup"><span data-stu-id="47573-118">Ranges</span></span>](ranges.md)
  
### <a name="parent-elements"></a><span data-ttu-id="47573-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="47573-119">Parent elements</span></span>

<span data-ttu-id="47573-120">[Artikelnummern ein.](itemids.md) | [GlobalItemIds](globalitemids.md) | [DraftItemIds](draftitemids.md) | [ContactIds](contactids.md) | [GroupIds](groupids.md)</span><span class="sxs-lookup"><span data-stu-id="47573-120">[ItemIds](itemids.md) | [GlobalItemIds](globalitemids.md) | [DraftItemIds](draftitemids.md) | [ContactIds](contactids.md) | [GroupIds](groupids.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="47573-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="47573-121">Remarks</span></span>

<span data-ttu-id="47573-122">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="47573-122">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="47573-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="47573-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="47573-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="47573-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="47573-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="47573-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="47573-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="47573-126">Schema name</span></span>  <br/> |<span data-ttu-id="47573-127">Schematypen</span><span class="sxs-lookup"><span data-stu-id="47573-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="47573-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="47573-128">Validation file</span></span>  <br/> |<span data-ttu-id="47573-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="47573-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="47573-130">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="47573-130">Can be empty</span></span>  <br/> ||
   

