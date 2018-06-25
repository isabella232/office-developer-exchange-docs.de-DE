---
title: ReturnNewItemIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: aeef79e4-31e1-4213-b627-9bac676be018
description: Das ReturnNewItemIds-Element gibt an, ob die Element-IDs der neuen Elemente in der Antwort zurückgegeben werden.
ms.openlocfilehash: 6d3bc83c05a82d6e448041167676f41c2620dcd4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831232"
---
# <a name="returnnewitemids"></a><span data-ttu-id="8d762-103">ReturnNewItemIds</span><span class="sxs-lookup"><span data-stu-id="8d762-103">ReturnNewItemIds</span></span>

<span data-ttu-id="8d762-104">Das **ReturnNewItemIds** -Element gibt an, ob die Element-IDs der neuen Elemente in der Antwort zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8d762-104">The **ReturnNewItemIds** element indicates whether the item identifiers of new items are returned in the response.</span></span> 
  
```XML
<ReturnNewItemIds/>
```

 <span data-ttu-id="8d762-105">**xs: Boolean**</span><span class="sxs-lookup"><span data-stu-id="8d762-105">**xs:boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8d762-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="8d762-106">Attributes and elements</span></span>

<span data-ttu-id="8d762-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="8d762-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8d762-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="8d762-108">Attributes</span></span>

<span data-ttu-id="8d762-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="8d762-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8d762-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8d762-110">Child elements</span></span>

<span data-ttu-id="8d762-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="8d762-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8d762-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8d762-112">Parent elements</span></span>

|<span data-ttu-id="8d762-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="8d762-113">**Element**</span></span>|<span data-ttu-id="8d762-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8d762-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8d762-115">CopyItem</span><span class="sxs-lookup"><span data-stu-id="8d762-115">CopyItem</span></span>](copyitem.md) <br/> |<span data-ttu-id="8d762-116">Definiert eine Anforderung an ein Element in einem Postfach im Exchange-Speicher zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="8d762-116">Defines a request to copy an item in a mailbox in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="8d762-117">MoveItem</span><span class="sxs-lookup"><span data-stu-id="8d762-117">MoveItem</span></span>](moveitem.md) <br/> |<span data-ttu-id="8d762-118">Definiert eine Anforderung an ein Element im Exchange-Speicher zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="8d762-118">Defines a request to move an item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="8d762-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="8d762-119">Text value</span></span>

<span data-ttu-id="8d762-120">Der Textwert **true** für das **ReturnNewItemIds** -Element gibt an, dass das neue Element-IDs in der Antwort zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8d762-120">A text value of **true** for the **ReturnNewItemIds** element indicates that the new item identifiers are returned in the response.</span></span> <span data-ttu-id="8d762-121">Der Wert **false** gibt an, dass das neue Element-IDs nicht in der Antwort zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8d762-121">A value of **false** indicates that the new item identifiers are not returned in the response.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="8d762-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8d762-122">Remarks</span></span>

<span data-ttu-id="8d762-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="8d762-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8d762-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="8d762-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8d762-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="8d762-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="8d762-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="8d762-126">Schema Name</span></span>  <br/> |<span data-ttu-id="8d762-127">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="8d762-127">Message schema</span></span>  <br/> |
|<span data-ttu-id="8d762-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="8d762-128">Validation File</span></span>  <br/> |<span data-ttu-id="8d762-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="8d762-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="8d762-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="8d762-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="8d762-131">False</span><span class="sxs-lookup"><span data-stu-id="8d762-131">False</span></span>  <br/> |
   

