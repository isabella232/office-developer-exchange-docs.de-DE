---
title: CopyItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CopyItem
api_type:
- schema
ms.assetid: ffb4c13e-e7ea-4e6b-87a0-509ce5371100
description: Das CopyItem-Element definiert eine Anforderung an ein Element in einem Postfach im Exchange-Speicher zu kopieren.
ms.openlocfilehash: 08cc1b67f7c7d369263acfc4b3d13e8aa70d2d5f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757726"
---
# <a name="copyitem"></a><span data-ttu-id="43957-103">CopyItem</span><span class="sxs-lookup"><span data-stu-id="43957-103">CopyItem</span></span>

<span data-ttu-id="43957-104">Das **CopyItem** -Element definiert eine Anforderung an ein Element in einem Postfach im Exchange-Speicher zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="43957-104">The **CopyItem** element defines a request to copy an item in a mailbox in the Exchange store.</span></span> 
  
```XML
<CopyItem>
   <ToFolderId/>
   <ItemIds/>
   <ReturnNewItemIds/>
</CopyItem>
```

 <span data-ttu-id="43957-105">**CopyItemType**</span><span class="sxs-lookup"><span data-stu-id="43957-105">**CopyItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="43957-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="43957-106">Attributes and elements</span></span>

<span data-ttu-id="43957-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="43957-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="43957-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="43957-108">Attributes</span></span>

<span data-ttu-id="43957-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="43957-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="43957-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="43957-110">Child elements</span></span>

|<span data-ttu-id="43957-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="43957-111">**Element**</span></span>|<span data-ttu-id="43957-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="43957-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="43957-113">ToFolderId</span><span class="sxs-lookup"><span data-stu-id="43957-113">ToFolderId</span></span>](tofolderid.md) <br/> |<span data-ttu-id="43957-114">Stellt den Zielordner für ein Element kopiert.</span><span class="sxs-lookup"><span data-stu-id="43957-114">Represents the destination folder for a copied item.</span></span>  <br/> |
|[<span data-ttu-id="43957-115">Artikelnummern ein.</span><span class="sxs-lookup"><span data-stu-id="43957-115">ItemIds</span></span>](itemids.md) <br/> |<span data-ttu-id="43957-116">Enthält ein Array von identifizierten Elementen, die in den Ordner, dargestellt durch das Element [ToFolderId](tofolderid.md) kopieren.</span><span class="sxs-lookup"><span data-stu-id="43957-116">Contains an array of identified items to copy to the folder represented by the [ToFolderId](tofolderid.md) element.</span></span>  <br/> |
|[<span data-ttu-id="43957-117">ReturnNewItemIds</span><span class="sxs-lookup"><span data-stu-id="43957-117">ReturnNewItemIds</span></span>](returnnewitemids.md) <br/> |<span data-ttu-id="43957-118">Gibt an, ob die Element-IDs der neuen Elemente in der Antwort zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="43957-118">Indicates whether the item identifiers of new items are returned in the response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="43957-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="43957-119">Parent elements</span></span>

<span data-ttu-id="43957-120">Keine.</span><span class="sxs-lookup"><span data-stu-id="43957-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="43957-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="43957-121">Remarks</span></span>

<span data-ttu-id="43957-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="43957-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="43957-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="43957-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="43957-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="43957-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="43957-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="43957-125">Schema Name</span></span>  <br/> |<span data-ttu-id="43957-126">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="43957-126">Messages schema</span></span>  <br/> |
|<span data-ttu-id="43957-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="43957-127">Validation File</span></span>  <br/> |<span data-ttu-id="43957-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="43957-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="43957-129">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="43957-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="43957-130">False</span><span class="sxs-lookup"><span data-stu-id="43957-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="43957-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="43957-131">See also</span></span>



[<span data-ttu-id="43957-132">CopyItem Operation</span><span class="sxs-lookup"><span data-stu-id="43957-132">CopyItem operation</span></span>](copyitem-operation.md)


- [<span data-ttu-id="43957-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="43957-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

