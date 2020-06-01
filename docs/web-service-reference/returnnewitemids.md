---
title: ReturnNewItemIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: aeef79e4-31e1-4213-b627-9bac676be018
description: Das ReturnNewItemIds-Element gibt an, ob die Elementbezeichner neuer Elemente in der Antwort zurückgegeben werden.
ms.openlocfilehash: 003676c4c034454aa551e42bf3af976183117b8c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465114"
---
# <a name="returnnewitemids"></a><span data-ttu-id="5030a-103">ReturnNewItemIds</span><span class="sxs-lookup"><span data-stu-id="5030a-103">ReturnNewItemIds</span></span>

<span data-ttu-id="5030a-104">Das **ReturnNewItemIds** -Element gibt an, ob die Elementbezeichner neuer Elemente in der Antwort zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5030a-104">The **ReturnNewItemIds** element indicates whether the item identifiers of new items are returned in the response.</span></span> 
  
```XML
<ReturnNewItemIds/>
```

 <span data-ttu-id="5030a-105">**xs: Boolean**</span><span class="sxs-lookup"><span data-stu-id="5030a-105">**xs:boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5030a-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="5030a-106">Attributes and elements</span></span>

<span data-ttu-id="5030a-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="5030a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5030a-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="5030a-108">Attributes</span></span>

<span data-ttu-id="5030a-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="5030a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5030a-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5030a-110">Child elements</span></span>

<span data-ttu-id="5030a-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="5030a-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5030a-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5030a-112">Parent elements</span></span>

|<span data-ttu-id="5030a-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="5030a-113">**Element**</span></span>|<span data-ttu-id="5030a-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5030a-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5030a-115">CopyItem</span><span class="sxs-lookup"><span data-stu-id="5030a-115">CopyItem</span></span>](copyitem.md) <br/> |<span data-ttu-id="5030a-116">Definiert eine Anforderung zum Kopieren eines Elements in einem Postfach im Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="5030a-116">Defines a request to copy an item in a mailbox in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="5030a-117">MoveItem</span><span class="sxs-lookup"><span data-stu-id="5030a-117">MoveItem</span></span>](moveitem.md) <br/> |<span data-ttu-id="5030a-118">Definiert eine Anforderung zum verlagern eines Elements in der Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="5030a-118">Defines a request to move an item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5030a-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="5030a-119">Text value</span></span>

<span data-ttu-id="5030a-120">Der Textwert **true** für das **ReturnNewItemIds** -Element gibt an, dass die neuen Elementbezeichner in der Antwort zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5030a-120">A text value of **true** for the **ReturnNewItemIds** element indicates that the new item identifiers are returned in the response.</span></span> <span data-ttu-id="5030a-121">Der Wert **false** gibt an, dass die neuen Elementbezeichner nicht in der Antwort zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5030a-121">A value of **false** indicates that the new item identifiers are not returned in the response.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5030a-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5030a-122">Remarks</span></span>

<span data-ttu-id="5030a-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="5030a-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5030a-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="5030a-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5030a-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="5030a-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="5030a-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="5030a-126">Schema Name</span></span>  <br/> |<span data-ttu-id="5030a-127">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="5030a-127">Message schema</span></span>  <br/> |
|<span data-ttu-id="5030a-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="5030a-128">Validation File</span></span>  <br/> |<span data-ttu-id="5030a-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="5030a-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="5030a-130">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="5030a-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="5030a-131">False</span><span class="sxs-lookup"><span data-stu-id="5030a-131">False</span></span>  <br/> |
   

