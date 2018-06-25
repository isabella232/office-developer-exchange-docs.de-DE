---
title: MoveItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MoveItem
api_type:
- schema
ms.assetid: a4593377-22dd-415f-b01d-387389ef650f
description: Das MoveItem-Element definiert eine Anforderung an ein Element im Exchange-Speicher zu verschieben.
ms.openlocfilehash: cd7f35bdabe8a596f4c186df1c8cd54e0ea1c540
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830486"
---
# <a name="moveitem"></a><span data-ttu-id="d9d1a-103">MoveItem</span><span class="sxs-lookup"><span data-stu-id="d9d1a-103">MoveItem</span></span>

<span data-ttu-id="d9d1a-104">Das **MoveItem** -Element definiert eine Anforderung an ein Element im Exchange-Speicher zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="d9d1a-104">The **MoveItem** element defines a request to move an item in the Exchange store.</span></span> 
  
```XML
<MoveItem>
   <ToFolderId/>
   <ItemIds/>
   <ReturnNewItemIds/>
</MoveItem>
```

 <span data-ttu-id="d9d1a-105">**MoveItemType**</span><span class="sxs-lookup"><span data-stu-id="d9d1a-105">**MoveItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d9d1a-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d9d1a-106">Attributes and elements</span></span>

<span data-ttu-id="d9d1a-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d9d1a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d9d1a-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d9d1a-108">Attributes</span></span>

<span data-ttu-id="d9d1a-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="d9d1a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d9d1a-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d9d1a-110">Child elements</span></span>

|<span data-ttu-id="d9d1a-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="d9d1a-111">**Element**</span></span>|<span data-ttu-id="d9d1a-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d9d1a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d9d1a-113">ToFolderId</span><span class="sxs-lookup"><span data-stu-id="d9d1a-113">ToFolderId</span></span>](tofolderid.md) <br/> |<span data-ttu-id="d9d1a-114">Stellt den Zielordner für ein verschobene Element an.</span><span class="sxs-lookup"><span data-stu-id="d9d1a-114">Represents the destination folder for a moved item.</span></span>  <br/> |
|[<span data-ttu-id="d9d1a-115">Artikelnummern ein.</span><span class="sxs-lookup"><span data-stu-id="d9d1a-115">ItemIds</span></span>](itemids.md) <br/> |<span data-ttu-id="d9d1a-116">Enthält ein Array von identifizierten Elementen, die in den Ordner, dargestellt durch das [ToFolderId](tofolderid.md) -Element verschieben.</span><span class="sxs-lookup"><span data-stu-id="d9d1a-116">Contains an array of identified items to move to the folder represented by the [ToFolderId](tofolderid.md) element.</span></span>  <br/> |
|[<span data-ttu-id="d9d1a-117">ReturnNewItemIds</span><span class="sxs-lookup"><span data-stu-id="d9d1a-117">ReturnNewItemIds</span></span>](returnnewitemids.md) <br/> |<span data-ttu-id="d9d1a-118">Gibt an, ob die Element-IDs der neuen Elemente in der Antwort zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d9d1a-118">Indicates whether the item identifiers of new items are returned in the response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d9d1a-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d9d1a-119">Parent elements</span></span>

<span data-ttu-id="d9d1a-120">Keine.</span><span class="sxs-lookup"><span data-stu-id="d9d1a-120">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="d9d1a-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="d9d1a-121">Text value</span></span>

<span data-ttu-id="d9d1a-122">Keine.</span><span class="sxs-lookup"><span data-stu-id="d9d1a-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d9d1a-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d9d1a-123">Remarks</span></span>

<span data-ttu-id="d9d1a-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="d9d1a-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d9d1a-125">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="d9d1a-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d9d1a-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="d9d1a-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d9d1a-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d9d1a-127">Schema Name</span></span>  <br/> |<span data-ttu-id="d9d1a-128">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="d9d1a-128">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d9d1a-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d9d1a-129">Validation File</span></span>  <br/> |<span data-ttu-id="d9d1a-130">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="d9d1a-130">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d9d1a-131">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d9d1a-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="d9d1a-132">False</span><span class="sxs-lookup"><span data-stu-id="d9d1a-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d9d1a-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d9d1a-133">See also</span></span>



[<span data-ttu-id="d9d1a-134">MoveItem Operation</span><span class="sxs-lookup"><span data-stu-id="d9d1a-134">MoveItem operation</span></span>](moveitem-operation.md)


- [<span data-ttu-id="d9d1a-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="d9d1a-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

