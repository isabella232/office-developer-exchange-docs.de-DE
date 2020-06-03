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
description: Das MoveItem-Element definiert eine Anforderung zum verlagern eines Elements in der Exchange-Informationsspeicher.
ms.openlocfilehash: 61dbb91cc20a71f50999241b3daa21bf8ebfbcc8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530401"
---
# <a name="moveitem"></a><span data-ttu-id="ca053-103">MoveItem</span><span class="sxs-lookup"><span data-stu-id="ca053-103">MoveItem</span></span>

<span data-ttu-id="ca053-104">Das **MoveItem** -Element definiert eine Anforderung zum verlagern eines Elements in der Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="ca053-104">The **MoveItem** element defines a request to move an item in the Exchange store.</span></span> 
  
```XML
<MoveItem>
   <ToFolderId/>
   <ItemIds/>
   <ReturnNewItemIds/>
</MoveItem>
```

 <span data-ttu-id="ca053-105">**MoveItemType**</span><span class="sxs-lookup"><span data-stu-id="ca053-105">**MoveItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ca053-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ca053-106">Attributes and elements</span></span>

<span data-ttu-id="ca053-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ca053-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ca053-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="ca053-108">Attributes</span></span>

<span data-ttu-id="ca053-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="ca053-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ca053-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ca053-110">Child elements</span></span>

|<span data-ttu-id="ca053-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="ca053-111">**Element**</span></span>|<span data-ttu-id="ca053-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ca053-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ca053-113">Tofolder-Datei</span><span class="sxs-lookup"><span data-stu-id="ca053-113">ToFolderId</span></span>](tofolderid.md) <br/> |<span data-ttu-id="ca053-114">Stellt den Zielordner für ein verschobenes Element dar.</span><span class="sxs-lookup"><span data-stu-id="ca053-114">Represents the destination folder for a moved item.</span></span>  <br/> |
|[<span data-ttu-id="ca053-115">ItemIds</span><span class="sxs-lookup"><span data-stu-id="ca053-115">ItemIds</span></span>](itemids.md) <br/> |<span data-ttu-id="ca053-116">Enthält ein Array von identifizierten Elementen, das in den durch das [tofolder](tofolderid.md) -Element dargestellten Ordner zu navigieren ist.</span><span class="sxs-lookup"><span data-stu-id="ca053-116">Contains an array of identified items to move to the folder represented by the [ToFolderId](tofolderid.md) element.</span></span>  <br/> |
|[<span data-ttu-id="ca053-117">ReturnNewItemIds</span><span class="sxs-lookup"><span data-stu-id="ca053-117">ReturnNewItemIds</span></span>](returnnewitemids.md) <br/> |<span data-ttu-id="ca053-118">Gibt an, ob die Elementbezeichner neuer Elemente in der Antwort zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ca053-118">Indicates whether the item identifiers of new items are returned in the response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ca053-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ca053-119">Parent elements</span></span>

<span data-ttu-id="ca053-120">Keine.</span><span class="sxs-lookup"><span data-stu-id="ca053-120">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="ca053-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="ca053-121">Text value</span></span>

<span data-ttu-id="ca053-122">Keine.</span><span class="sxs-lookup"><span data-stu-id="ca053-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ca053-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ca053-123">Remarks</span></span>

<span data-ttu-id="ca053-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="ca053-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ca053-125">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="ca053-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ca053-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="ca053-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ca053-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ca053-127">Schema Name</span></span>  <br/> |<span data-ttu-id="ca053-128">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="ca053-128">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ca053-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ca053-129">Validation File</span></span>  <br/> |<span data-ttu-id="ca053-130">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="ca053-130">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ca053-131">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="ca053-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="ca053-132">False</span><span class="sxs-lookup"><span data-stu-id="ca053-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ca053-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ca053-133">See also</span></span>



[<span data-ttu-id="ca053-134">MoveItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="ca053-134">MoveItem operation</span></span>](moveitem-operation.md)


- [<span data-ttu-id="ca053-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="ca053-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

