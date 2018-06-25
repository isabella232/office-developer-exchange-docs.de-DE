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
description: CopyToFolder-Element gibt den Bezeichner des Ordners die e-Mail, die auf Elemente kopiert werden können.
ms.openlocfilehash: b641c23b7aed11ae85157e2ed01cfa9d61d07e0a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757728"
---
# <a name="copytofolder"></a><span data-ttu-id="c2517-103">CopyToFolder</span><span class="sxs-lookup"><span data-stu-id="c2517-103">CopyToFolder</span></span>

<span data-ttu-id="c2517-104">**CopyToFolder** -Element gibt den Bezeichner des Ordners die e-Mail, die auf Elemente kopiert werden können.</span><span class="sxs-lookup"><span data-stu-id="c2517-104">The **CopyToFolder** element specifies the identifier of the folder that email items can be copied to.</span></span> 
  
```XML
<CopyToFolder>
    <FolderId></FolderId>
    <DistinguishedFolderId></DistinguisedFolderId>
</CopyToFolder>
```

 <span data-ttu-id="c2517-105">**TargetFolderIdType**</span><span class="sxs-lookup"><span data-stu-id="c2517-105">**TargetFolderIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c2517-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c2517-106">Attributes and elements</span></span>

<span data-ttu-id="c2517-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c2517-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c2517-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="c2517-108">Attributes</span></span>

<span data-ttu-id="c2517-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="c2517-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c2517-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c2517-110">Child elements</span></span>

|<span data-ttu-id="c2517-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="c2517-111">**Element**</span></span>|<span data-ttu-id="c2517-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c2517-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c2517-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="c2517-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="c2517-114">Enthält den Bezeichner des Zielordners für eine kopierte oder verschobene Element oder einen Ordner.</span><span class="sxs-lookup"><span data-stu-id="c2517-114">Contains the identifier of a destination folder for a copied or moved item or folder.</span></span>  <br/> |
|[<span data-ttu-id="c2517-115">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="c2517-115">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="c2517-116">Gibt einen benannten Zielordner für eine kopierte oder verschobene Element oder einen Ordner.</span><span class="sxs-lookup"><span data-stu-id="c2517-116">Identifies a named destination folder for a copied or moved item or folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c2517-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c2517-117">Parent elements</span></span>

|<span data-ttu-id="c2517-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="c2517-118">**Element**</span></span>|<span data-ttu-id="c2517-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c2517-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c2517-120">Aktionen</span><span class="sxs-lookup"><span data-stu-id="c2517-120">Actions</span></span>](actions.md) <br/> |<span data-ttu-id="c2517-121">Repräsentiert den Satz von Aktionen, die sind verfügbar, die auf eine Nachricht durchgeführt werden, wenn die Bedingungen erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="c2517-121">Represents the set of actions that are available to be taken on a message when the conditions are fulfilled.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c2517-122">Textwert</span><span class="sxs-lookup"><span data-stu-id="c2517-122">Text value</span></span>

<span data-ttu-id="c2517-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="c2517-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c2517-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c2517-124">Remarks</span></span>

<span data-ttu-id="c2517-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="c2517-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c2517-126">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="c2517-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c2517-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="c2517-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c2517-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c2517-128">Schema Name</span></span>  <br/> |<span data-ttu-id="c2517-129">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="c2517-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c2517-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c2517-130">Validation File</span></span>  <br/> |<span data-ttu-id="c2517-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="c2517-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c2517-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="c2517-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="c2517-133">True</span><span class="sxs-lookup"><span data-stu-id="c2517-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c2517-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c2517-134">See also</span></span>



[<span data-ttu-id="c2517-135">MoveToFolder</span><span class="sxs-lookup"><span data-stu-id="c2517-135">MoveToFolder</span></span>](movetofolder.md)


- [<span data-ttu-id="c2517-136">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="c2517-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

