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
description: Das CopyItem-Element definiert eine Anforderung zum Kopieren eines Elements in einem Postfach im Exchange-Informationsspeicher.
ms.openlocfilehash: b9af1670fd580107de08ad3b950191399436388d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458502"
---
# <a name="copyitem"></a><span data-ttu-id="4a807-103">CopyItem</span><span class="sxs-lookup"><span data-stu-id="4a807-103">CopyItem</span></span>

<span data-ttu-id="4a807-104">Das **CopyItem** -Element definiert eine Anforderung zum Kopieren eines Elements in einem Postfach im Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="4a807-104">The **CopyItem** element defines a request to copy an item in a mailbox in the Exchange store.</span></span> 
  
```XML
<CopyItem>
   <ToFolderId/>
   <ItemIds/>
   <ReturnNewItemIds/>
</CopyItem>
```

 <span data-ttu-id="4a807-105">**CopyItemType**</span><span class="sxs-lookup"><span data-stu-id="4a807-105">**CopyItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4a807-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="4a807-106">Attributes and elements</span></span>

<span data-ttu-id="4a807-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="4a807-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4a807-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="4a807-108">Attributes</span></span>

<span data-ttu-id="4a807-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="4a807-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4a807-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4a807-110">Child elements</span></span>

|<span data-ttu-id="4a807-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="4a807-111">**Element**</span></span>|<span data-ttu-id="4a807-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4a807-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4a807-113">Tofolder-Datei</span><span class="sxs-lookup"><span data-stu-id="4a807-113">ToFolderId</span></span>](tofolderid.md) <br/> |<span data-ttu-id="4a807-114">Stellt den Zielordner für ein kopiertes Element dar.</span><span class="sxs-lookup"><span data-stu-id="4a807-114">Represents the destination folder for a copied item.</span></span>  <br/> |
|[<span data-ttu-id="4a807-115">ItemIds</span><span class="sxs-lookup"><span data-stu-id="4a807-115">ItemIds</span></span>](itemids.md) <br/> |<span data-ttu-id="4a807-116">Enthält ein Array von identifizierten Elementen, das in den durch das [tofolder](tofolderid.md) -Element dargestellten Ordner kopiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="4a807-116">Contains an array of identified items to copy to the folder represented by the [ToFolderId](tofolderid.md) element.</span></span>  <br/> |
|[<span data-ttu-id="4a807-117">ReturnNewItemIds</span><span class="sxs-lookup"><span data-stu-id="4a807-117">ReturnNewItemIds</span></span>](returnnewitemids.md) <br/> |<span data-ttu-id="4a807-118">Gibt an, ob die Elementbezeichner neuer Elemente in der Antwort zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4a807-118">Indicates whether the item identifiers of new items are returned in the response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4a807-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4a807-119">Parent elements</span></span>

<span data-ttu-id="4a807-120">Keine.</span><span class="sxs-lookup"><span data-stu-id="4a807-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4a807-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4a807-121">Remarks</span></span>

<span data-ttu-id="4a807-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="4a807-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4a807-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="4a807-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4a807-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="4a807-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="4a807-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="4a807-125">Schema Name</span></span>  <br/> |<span data-ttu-id="4a807-126">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="4a807-126">Messages schema</span></span>  <br/> |
|<span data-ttu-id="4a807-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="4a807-127">Validation File</span></span>  <br/> |<span data-ttu-id="4a807-128">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="4a807-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="4a807-129">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="4a807-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="4a807-130">False</span><span class="sxs-lookup"><span data-stu-id="4a807-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4a807-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4a807-131">See also</span></span>



[<span data-ttu-id="4a807-132">CopyItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="4a807-132">CopyItem operation</span></span>](copyitem-operation.md)


- [<span data-ttu-id="4a807-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="4a807-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

