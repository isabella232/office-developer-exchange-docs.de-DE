---
title: MoveToFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MoveToFolder
api_type:
- schema
ms.assetid: 991673b9-b627-4848-bfba-59a187b8575f
description: Das MoveToFolder-Element gibt den Bezeichner des Ordners an, in den e-Mail-Elemente verschoben werden können.
ms.openlocfilehash: e323b2ac5390855b3db0b5495af667cdf2da5596
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530007"
---
# <a name="movetofolder"></a><span data-ttu-id="2dbf5-103">MoveToFolder</span><span class="sxs-lookup"><span data-stu-id="2dbf5-103">MoveToFolder</span></span>

<span data-ttu-id="2dbf5-104">Das **MoveToFolder** -Element gibt den Bezeichner des Ordners an, in den e-Mail-Elemente verschoben werden können.</span><span class="sxs-lookup"><span data-stu-id="2dbf5-104">The **MoveToFolder** element specifies the identifier of the folder to which email items can be moved.</span></span> 
  
```XML
<MoveToFolder>
    <FolderId></FolderId>
    <DistinguishedFolderId></DistinguisedFolderId>
</MoveToFolder>
```

 <span data-ttu-id="2dbf5-105">**TargetFolderIdType**</span><span class="sxs-lookup"><span data-stu-id="2dbf5-105">**TargetFolderIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2dbf5-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="2dbf5-106">Attributes and elements</span></span>

<span data-ttu-id="2dbf5-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="2dbf5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2dbf5-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="2dbf5-108">Attributes</span></span>

<span data-ttu-id="2dbf5-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="2dbf5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2dbf5-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2dbf5-110">Child elements</span></span>

|<span data-ttu-id="2dbf5-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="2dbf5-111">**Element**</span></span>|<span data-ttu-id="2dbf5-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2dbf5-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2dbf5-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="2dbf5-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="2dbf5-114">Enthält den Bezeichner eines Zielordners für ein kopiertes oder verschobenes Element oder einen verschobenen Ordner.</span><span class="sxs-lookup"><span data-stu-id="2dbf5-114">Contains the identifier of a destination folder for a copied or moved item or folder.</span></span>  <br/> |
|[<span data-ttu-id="2dbf5-115">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="2dbf5-115">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="2dbf5-116">Gibt einen benannten Zielordner für ein kopiertes oder verschobenes Element oder einen Ordner an.</span><span class="sxs-lookup"><span data-stu-id="2dbf5-116">Identifies a named destination folder for a copied or moved item or folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2dbf5-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2dbf5-117">Parent elements</span></span>

|<span data-ttu-id="2dbf5-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="2dbf5-118">**Element**</span></span>|<span data-ttu-id="2dbf5-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2dbf5-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2dbf5-120">Aktionen</span><span class="sxs-lookup"><span data-stu-id="2dbf5-120">Actions</span></span>](actions.md) <br/> |<span data-ttu-id="2dbf5-121">Stellt die Gruppe von Aktionen dar, die für eine Nachricht zur Verfügung stehen, wenn die Bedingungen erfüllt sind..</span><span class="sxs-lookup"><span data-stu-id="2dbf5-121">Represents the set of actions that are available to be taken on a message when the conditions are fulfilled..</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2dbf5-122">Textwert</span><span class="sxs-lookup"><span data-stu-id="2dbf5-122">Text value</span></span>

<span data-ttu-id="2dbf5-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="2dbf5-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2dbf5-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2dbf5-124">Remarks</span></span>

<span data-ttu-id="2dbf5-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="2dbf5-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2dbf5-126">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="2dbf5-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2dbf5-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="2dbf5-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2dbf5-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="2dbf5-128">Schema Name</span></span>  <br/> |<span data-ttu-id="2dbf5-129">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="2dbf5-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="2dbf5-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="2dbf5-130">Validation File</span></span>  <br/> |<span data-ttu-id="2dbf5-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="2dbf5-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2dbf5-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="2dbf5-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="2dbf5-133">True</span><span class="sxs-lookup"><span data-stu-id="2dbf5-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2dbf5-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2dbf5-134">See also</span></span>



[<span data-ttu-id="2dbf5-135">CopyToFolder</span><span class="sxs-lookup"><span data-stu-id="2dbf5-135">CopyToFolder</span></span>](copytofolder.md)


- [<span data-ttu-id="2dbf5-136">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="2dbf5-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

