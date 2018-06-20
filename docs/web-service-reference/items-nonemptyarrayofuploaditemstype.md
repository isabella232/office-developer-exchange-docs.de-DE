---
title: Elemente (NonEmptyArrayOfUploadItemsType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Items
api_type:
- schema
ms.assetid: 402bfa6d-11d7-4547-b8bd-197e9922ab49
description: Das Items-Element enthält ein Array von Elementen in einem Postfach hochladen.
ms.openlocfilehash: ac508b2026c3e0ec730154efeeff0a9669e6eff8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830156"
---
# <a name="items-nonemptyarrayofuploaditemstype"></a><span data-ttu-id="fecc4-103">Elemente (NonEmptyArrayOfUploadItemsType)</span><span class="sxs-lookup"><span data-stu-id="fecc4-103">Items (NonEmptyArrayOfUploadItemsType)</span></span>

<span data-ttu-id="fecc4-104">Das **Items** -Element enthält ein Array von Elementen in einem Postfach hochladen.</span><span class="sxs-lookup"><span data-stu-id="fecc4-104">The **Items** element contains an array of items to upload into a mailbox.</span></span> 
  
[<span data-ttu-id="fecc4-105">UploadItems</span><span class="sxs-lookup"><span data-stu-id="fecc4-105">UploadItems</span></span>](uploaditems.md)
  
[<span data-ttu-id="fecc4-106">Elemente (NonEmptyArrayOfUploadItemsType)</span><span class="sxs-lookup"><span data-stu-id="fecc4-106">Items (NonEmptyArrayOfUploadItemsType)</span></span>](items-nonemptyarrayofuploaditemstype.md)
  
```XML
<Items>
   <Item/>
</Items>
```

 <span data-ttu-id="fecc4-107">**NonEmptyArrayOfUploadItemsType**</span><span class="sxs-lookup"><span data-stu-id="fecc4-107">**NonEmptyArrayOfUploadItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fecc4-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="fecc4-108">Attributes and elements</span></span>

<span data-ttu-id="fecc4-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="fecc4-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fecc4-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="fecc4-110">Attributes</span></span>

<span data-ttu-id="fecc4-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="fecc4-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fecc4-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fecc4-112">Child elements</span></span>

|<span data-ttu-id="fecc4-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="fecc4-113">**Element**</span></span>|<span data-ttu-id="fecc4-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fecc4-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fecc4-115">Item (UploadItemType)</span><span class="sxs-lookup"><span data-stu-id="fecc4-115">Item (UploadItemType)</span></span>](item-uploaditemtype.md) <br/> |<span data-ttu-id="fecc4-116">Stellt ein einzelnes Element in einem Postfach hochladen.</span><span class="sxs-lookup"><span data-stu-id="fecc4-116">Represents a single item to upload into a mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="fecc4-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fecc4-117">Parent elements</span></span>

|<span data-ttu-id="fecc4-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="fecc4-118">**Element**</span></span>|<span data-ttu-id="fecc4-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fecc4-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fecc4-120">UploadItems</span><span class="sxs-lookup"><span data-stu-id="fecc4-120">UploadItems</span></span>](uploaditems.md) <br/> |<span data-ttu-id="fecc4-121">Stellt eine Anforderung zum Hochladen von Elementen in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="fecc4-121">Represents a request to upload items into a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="fecc4-122">Textwert</span><span class="sxs-lookup"><span data-stu-id="fecc4-122">Text value</span></span>

<span data-ttu-id="fecc4-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="fecc4-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fecc4-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fecc4-124">Remarks</span></span>

<span data-ttu-id="fecc4-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="fecc4-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fecc4-126">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="fecc4-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fecc4-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="fecc4-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="fecc4-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="fecc4-128">Schema Name</span></span>  <br/> |<span data-ttu-id="fecc4-129">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="fecc4-129">Message schema</span></span>  <br/> |
|<span data-ttu-id="fecc4-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="fecc4-130">Validation File</span></span>  <br/> |<span data-ttu-id="fecc4-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="fecc4-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="fecc4-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="fecc4-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="fecc4-133">False</span><span class="sxs-lookup"><span data-stu-id="fecc4-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fecc4-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fecc4-134">See also</span></span>



[<span data-ttu-id="fecc4-135">ExportItems-Vorgang</span><span class="sxs-lookup"><span data-stu-id="fecc4-135">ExportItems operation</span></span>](exportitems-operation.md)
  
[<span data-ttu-id="fecc4-136">UploadItems-Vorgang</span><span class="sxs-lookup"><span data-stu-id="fecc4-136">UploadItems operation</span></span>](uploaditems-operation.md)

