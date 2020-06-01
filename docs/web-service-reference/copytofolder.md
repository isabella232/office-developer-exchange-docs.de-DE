---
title: CopyToFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CopyToFolder
api_type:
- schema
ms.assetid: 6fd8a6b8-d813-43ff-991b-0e9e782fe00e
description: Das CopyToFolder-Element gibt den Bezeichner des Ordners an, in den e-Mail-Elemente kopiert werden können.
ms.openlocfilehash: 7cdda0f9769f909255c9b76f78ac7094a8dfc8f8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463174"
---
# <a name="copytofolder"></a><span data-ttu-id="0edf7-103">CopyToFolder</span><span class="sxs-lookup"><span data-stu-id="0edf7-103">CopyToFolder</span></span>

<span data-ttu-id="0edf7-104">Das **CopyToFolder** -Element gibt den Bezeichner des Ordners an, in den e-Mail-Elemente kopiert werden können.</span><span class="sxs-lookup"><span data-stu-id="0edf7-104">The **CopyToFolder** element specifies the identifier of the folder that email items can be copied to.</span></span> 
  
```XML
<CopyToFolder>
    <FolderId></FolderId>
    <DistinguishedFolderId></DistinguisedFolderId>
</CopyToFolder>
```

 <span data-ttu-id="0edf7-105">**TargetFolderIdType**</span><span class="sxs-lookup"><span data-stu-id="0edf7-105">**TargetFolderIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0edf7-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="0edf7-106">Attributes and elements</span></span>

<span data-ttu-id="0edf7-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="0edf7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0edf7-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="0edf7-108">Attributes</span></span>

<span data-ttu-id="0edf7-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="0edf7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0edf7-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0edf7-110">Child elements</span></span>

|<span data-ttu-id="0edf7-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="0edf7-111">**Element**</span></span>|<span data-ttu-id="0edf7-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0edf7-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0edf7-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="0edf7-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="0edf7-114">Enthält den Bezeichner eines Zielordners für ein kopiertes oder verschobenes Element oder einen verschobenen Ordner.</span><span class="sxs-lookup"><span data-stu-id="0edf7-114">Contains the identifier of a destination folder for a copied or moved item or folder.</span></span>  <br/> |
|[<span data-ttu-id="0edf7-115">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="0edf7-115">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="0edf7-116">Gibt einen benannten Zielordner für ein kopiertes oder verschobenes Element oder einen Ordner an.</span><span class="sxs-lookup"><span data-stu-id="0edf7-116">Identifies a named destination folder for a copied or moved item or folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0edf7-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0edf7-117">Parent elements</span></span>

|<span data-ttu-id="0edf7-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="0edf7-118">**Element**</span></span>|<span data-ttu-id="0edf7-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0edf7-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0edf7-120">Aktionen</span><span class="sxs-lookup"><span data-stu-id="0edf7-120">Actions</span></span>](actions.md) <br/> |<span data-ttu-id="0edf7-121">Repräsentiert den Satz von Aktionen, die sind verfügbar, die auf eine Nachricht durchgeführt werden, wenn die Bedingungen erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="0edf7-121">Represents the set of actions that are available to be taken on a message when the conditions are fulfilled.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0edf7-122">Textwert</span><span class="sxs-lookup"><span data-stu-id="0edf7-122">Text value</span></span>

<span data-ttu-id="0edf7-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="0edf7-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0edf7-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0edf7-124">Remarks</span></span>

<span data-ttu-id="0edf7-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="0edf7-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0edf7-126">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="0edf7-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0edf7-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="0edf7-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0edf7-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="0edf7-128">Schema Name</span></span>  <br/> |<span data-ttu-id="0edf7-129">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="0edf7-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="0edf7-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="0edf7-130">Validation File</span></span>  <br/> |<span data-ttu-id="0edf7-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="0edf7-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0edf7-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="0edf7-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="0edf7-133">True</span><span class="sxs-lookup"><span data-stu-id="0edf7-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0edf7-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0edf7-134">See also</span></span>



[<span data-ttu-id="0edf7-135">MoveToFolder</span><span class="sxs-lookup"><span data-stu-id="0edf7-135">MoveToFolder</span></span>](movetofolder.md)


- [<span data-ttu-id="0edf7-136">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="0edf7-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

