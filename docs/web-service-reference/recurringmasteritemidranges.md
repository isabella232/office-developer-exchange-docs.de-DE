---
title: RecurringMasterItemIdRanges
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5c9c89b5-4ce8-437b-a332-fa7ed35c8388
description: Das RecurringMasterItemIdRanges-Element gibt ein Array von Ereignis Bereichen an.
ms.openlocfilehash: 784676844c5c58c65b8cc6177843bf26d351b7d9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528755"
---
# <a name="recurringmasteritemidranges"></a><span data-ttu-id="a97d0-103">RecurringMasterItemIdRanges</span><span class="sxs-lookup"><span data-stu-id="a97d0-103">RecurringMasterItemIdRanges</span></span>

<span data-ttu-id="a97d0-104">Das **RecurringMasterItemIdRanges** -Element gibt ein Array von Ereignis Bereichen an.</span><span class="sxs-lookup"><span data-stu-id="a97d0-104">The **RecurringMasterItemIdRanges** element specifies an array of occurrence ranges.</span></span> 
  
```XML
<RecurringMasterItemIdRanges Id="" ChangeKey="">
   <Ranges/>
</RecurringMasterItemIdRanges>
```

 <span data-ttu-id="a97d0-105">**RecurringMasterItemIdRangesType**</span><span class="sxs-lookup"><span data-stu-id="a97d0-105">**RecurringMasterItemIdRangesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a97d0-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a97d0-106">Attributes and elements</span></span>

<span data-ttu-id="a97d0-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a97d0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a97d0-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="a97d0-108">Attributes</span></span>

|<span data-ttu-id="a97d0-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="a97d0-109">**Attribute**</span></span>|<span data-ttu-id="a97d0-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a97d0-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a97d0-111">**Id**</span><span class="sxs-lookup"><span data-stu-id="a97d0-111">**Id**</span></span> <br/> |<span data-ttu-id="a97d0-112">Der Textwert des **ID-** Attributs ist die eindeutige ID eines wiederkehrenden Hauptelements.</span><span class="sxs-lookup"><span data-stu-id="a97d0-112">The text value of the **Id** attribute is a recurring master item's unique identifier.</span></span> <span data-ttu-id="a97d0-113">Dies ist ein **String** -Wert.</span><span class="sxs-lookup"><span data-stu-id="a97d0-113">This is a **string** value.</span></span>  <br/> |
|<span data-ttu-id="a97d0-114">**ChangeKey**</span><span class="sxs-lookup"><span data-stu-id="a97d0-114">**ChangeKey**</span></span> <br/> |<span data-ttu-id="a97d0-115">Der Textwert des **ChangeKey** -Attributs ist der Änderungsschlüssel des wiederkehrenden Hauptelements.</span><span class="sxs-lookup"><span data-stu-id="a97d0-115">The text value of the **ChangeKey** attribute is the recurring master item's change key.</span></span> <span data-ttu-id="a97d0-116">Dies ist ein **String** -Wert.</span><span class="sxs-lookup"><span data-stu-id="a97d0-116">This is a **string** value.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a97d0-117">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a97d0-117">Child elements</span></span>

[<span data-ttu-id="a97d0-118">Ranges</span><span class="sxs-lookup"><span data-stu-id="a97d0-118">Ranges</span></span>](ranges.md)
  
### <a name="parent-elements"></a><span data-ttu-id="a97d0-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a97d0-119">Parent elements</span></span>

<span data-ttu-id="a97d0-120">[Itemids](itemids.md)  |  [GlobalItemIds](globalitemids.md)  |  [DraftItemIds](draftitemids.md)  |  [ContactIds](contactids.md) Die  |  [GroupIds](groupids.md)</span><span class="sxs-lookup"><span data-stu-id="a97d0-120">[ItemIds](itemids.md) | [GlobalItemIds](globalitemids.md) | [DraftItemIds](draftitemids.md) | [ContactIds](contactids.md) | [GroupIds](groupids.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a97d0-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a97d0-121">Remarks</span></span>

<span data-ttu-id="a97d0-122">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="a97d0-122">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="a97d0-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="a97d0-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a97d0-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="a97d0-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a97d0-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="a97d0-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a97d0-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a97d0-126">Schema name</span></span>  <br/> |<span data-ttu-id="a97d0-127">Schematypen</span><span class="sxs-lookup"><span data-stu-id="a97d0-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="a97d0-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a97d0-128">Validation file</span></span>  <br/> |<span data-ttu-id="a97d0-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a97d0-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a97d0-130">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="a97d0-130">Can be empty</span></span>  <br/> ||
   

