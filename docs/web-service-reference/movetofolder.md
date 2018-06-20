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
description: MoveToFolder-Element gibt den Bezeichner des Ordners in den e-Mail-Elemente verschoben werden können.
ms.openlocfilehash: 058f008b348d49c932bf334dd3379f02d06154e9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830494"
---
# <a name="movetofolder"></a><span data-ttu-id="b38fc-103">MoveToFolder</span><span class="sxs-lookup"><span data-stu-id="b38fc-103">MoveToFolder</span></span>

<span data-ttu-id="b38fc-104">**MoveToFolder** -Element gibt den Bezeichner des Ordners in den e-Mail-Elemente verschoben werden können.</span><span class="sxs-lookup"><span data-stu-id="b38fc-104">The **MoveToFolder** element specifies the identifier of the folder to which email items can be moved.</span></span> 
  
```XML
<MoveToFolder>
    <FolderId></FolderId>
    <DistinguishedFolderId></DistinguisedFolderId>
</MoveToFolder>
```

 <span data-ttu-id="b38fc-105">**TargetFolderIdType**</span><span class="sxs-lookup"><span data-stu-id="b38fc-105">**TargetFolderIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b38fc-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b38fc-106">Attributes and elements</span></span>

<span data-ttu-id="b38fc-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b38fc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b38fc-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="b38fc-108">Attributes</span></span>

<span data-ttu-id="b38fc-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="b38fc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b38fc-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b38fc-110">Child elements</span></span>

|<span data-ttu-id="b38fc-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="b38fc-111">**Element**</span></span>|<span data-ttu-id="b38fc-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b38fc-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b38fc-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="b38fc-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="b38fc-114">Enthält den Bezeichner des Zielordners für eine kopierte oder verschobene Element oder einen Ordner.</span><span class="sxs-lookup"><span data-stu-id="b38fc-114">Contains the identifier of a destination folder for a copied or moved item or folder.</span></span>  <br/> |
|[<span data-ttu-id="b38fc-115">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="b38fc-115">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="b38fc-116">Gibt einen benannten Zielordner für eine kopierte oder verschobene Element oder einen Ordner.</span><span class="sxs-lookup"><span data-stu-id="b38fc-116">Identifies a named destination folder for a copied or moved item or folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b38fc-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b38fc-117">Parent elements</span></span>

|<span data-ttu-id="b38fc-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="b38fc-118">**Element**</span></span>|<span data-ttu-id="b38fc-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b38fc-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b38fc-120">Aktionen</span><span class="sxs-lookup"><span data-stu-id="b38fc-120">Actions</span></span>](actions.md) <br/> |<span data-ttu-id="b38fc-121">Repräsentiert den Satz von Aktionen, die sind verfügbar, die auf eine Nachricht durchgeführt werden, wenn die Bedingungen erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="b38fc-121">Represents the set of actions that are available to be taken on a message when the conditions are fulfilled..</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b38fc-122">Textwert</span><span class="sxs-lookup"><span data-stu-id="b38fc-122">Text value</span></span>

<span data-ttu-id="b38fc-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="b38fc-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b38fc-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b38fc-124">Remarks</span></span>

<span data-ttu-id="b38fc-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="b38fc-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b38fc-126">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="b38fc-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b38fc-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="b38fc-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b38fc-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b38fc-128">Schema Name</span></span>  <br/> |<span data-ttu-id="b38fc-129">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="b38fc-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b38fc-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b38fc-130">Validation File</span></span>  <br/> |<span data-ttu-id="b38fc-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="b38fc-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b38fc-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="b38fc-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="b38fc-133">True</span><span class="sxs-lookup"><span data-stu-id="b38fc-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b38fc-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b38fc-134">See also</span></span>



[<span data-ttu-id="b38fc-135">CopyToFolder</span><span class="sxs-lookup"><span data-stu-id="b38fc-135">CopyToFolder</span></span>](copytofolder.md)


- [<span data-ttu-id="b38fc-136">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="b38fc-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

