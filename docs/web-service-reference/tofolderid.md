---
title: ToFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ToFolderId
api_type:
- schema
ms.assetid: bd6a4265-ad40-43f6-bcc4-0bf5df4e984c
description: Das ToFolderId-Element darstellt, den Zielordner für eine kopierte oder verschobene Element oder einen Ordner.
ms.openlocfilehash: a48309f0b7f5c9bf667fc2eb653a0502832bc996
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839222"
---
# <a name="tofolderid"></a><span data-ttu-id="9d2de-103">ToFolderId</span><span class="sxs-lookup"><span data-stu-id="9d2de-103">ToFolderId</span></span>

<span data-ttu-id="9d2de-104">Das **ToFolderId** -Element darstellt, den Zielordner für eine kopierte oder verschobene Element oder einen Ordner.</span><span class="sxs-lookup"><span data-stu-id="9d2de-104">The **ToFolderId** element represents the destination folder for a copied or moved item or folder.</span></span> 
  
```xml
<ToFolderId>
   <FolderId/>
</ToFolderId>
```

 <span data-ttu-id="9d2de-105">**TargetFolderIdType**</span><span class="sxs-lookup"><span data-stu-id="9d2de-105">**TargetFolderIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9d2de-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="9d2de-106">Attributes and elements</span></span>

<span data-ttu-id="9d2de-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="9d2de-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9d2de-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="9d2de-108">Attributes</span></span>

<span data-ttu-id="9d2de-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="9d2de-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9d2de-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9d2de-110">Child elements</span></span>

|<span data-ttu-id="9d2de-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="9d2de-111">**Element**</span></span>|<span data-ttu-id="9d2de-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9d2de-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9d2de-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="9d2de-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="9d2de-114">Enthält den Bezeichner des Zielordners für eine kopierte oder verschobene Element oder einen Ordner.</span><span class="sxs-lookup"><span data-stu-id="9d2de-114">Contains the identifier of a destination folder for a copied or moved item or folder.</span></span>  <br/> |
|[<span data-ttu-id="9d2de-115">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="9d2de-115">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="9d2de-116">Gibt einen benannten Zielordner für eine kopierte oder verschobene Element oder einen Ordner.</span><span class="sxs-lookup"><span data-stu-id="9d2de-116">Identifies a named destination folder for a copied or moved item or folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9d2de-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9d2de-117">Parent elements</span></span>

|<span data-ttu-id="9d2de-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="9d2de-118">**Element**</span></span>|<span data-ttu-id="9d2de-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9d2de-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9d2de-120">MoveFolder</span><span class="sxs-lookup"><span data-stu-id="9d2de-120">MoveFolder</span></span>](movefolder.md) <br/> |<span data-ttu-id="9d2de-121">Definiert eine Anforderung an einen Ordner im Exchange-Speicher zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="9d2de-121">Defines a request to move a folder in the Exchange store.</span></span>  <br/> <span data-ttu-id="9d2de-122">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="9d2de-122">The following is the XPath expression to this element:</span></span>  <br/>  `/MoveFolder` <br/> |
|[<span data-ttu-id="9d2de-123">CopyFolder</span><span class="sxs-lookup"><span data-stu-id="9d2de-123">CopyFolder</span></span>](copyfolder.md) <br/> |<span data-ttu-id="9d2de-124">Definiert eine Anforderung an einen Ordner im Exchange-Speicher zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="9d2de-124">Defines a request to copy a folder in the Exchange store.</span></span>  <br/> <span data-ttu-id="9d2de-125">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="9d2de-125">The following is the XPath expression to this element:</span></span>  <br/>  `/CopyFolder` <br/> |
|[<span data-ttu-id="9d2de-126">MoveItem</span><span class="sxs-lookup"><span data-stu-id="9d2de-126">MoveItem</span></span>](moveitem.md) <br/> |<span data-ttu-id="9d2de-127">Definiert eine Anforderung an ein Element im Exchange-Speicher zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="9d2de-127">Defines a request to move an item in the Exchange store.</span></span>  <br/> <span data-ttu-id="9d2de-128">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="9d2de-128">The following is the XPath expression to this element:</span></span>  <br/>  `/MoveItem` <br/> |
|[<span data-ttu-id="9d2de-129">CopyItem</span><span class="sxs-lookup"><span data-stu-id="9d2de-129">CopyItem</span></span>](copyitem.md) <br/> |<span data-ttu-id="9d2de-130">Definiert eine Anforderung an ein Element im Exchange-Speicher zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="9d2de-130">Defines a request to copy an item in the Exchange store.</span></span>  <br/> <span data-ttu-id="9d2de-131">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="9d2de-131">The following is the XPath expression to this element:</span></span>  <br/>  `/CopyItem` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9d2de-132">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9d2de-132">Remarks</span></span>

<span data-ttu-id="9d2de-133">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="9d2de-133">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9d2de-134">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="9d2de-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9d2de-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="9d2de-135">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="9d2de-136">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="9d2de-136">Schema Name</span></span>  <br/> |<span data-ttu-id="9d2de-137">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="9d2de-137">Messages schema</span></span>  <br/> |
|<span data-ttu-id="9d2de-138">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="9d2de-138">Validation File</span></span>  <br/> |<span data-ttu-id="9d2de-139">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="9d2de-139">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9d2de-140">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="9d2de-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="9d2de-141">False</span><span class="sxs-lookup"><span data-stu-id="9d2de-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9d2de-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9d2de-142">See also</span></span>



[<span data-ttu-id="9d2de-143">MoveFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="9d2de-143">MoveFolder operation</span></span>](movefolder-operation.md)
  
[<span data-ttu-id="9d2de-144">CopyFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="9d2de-144">CopyFolder operation</span></span>](copyfolder-operation.md)
  
[<span data-ttu-id="9d2de-145">MoveItem Operation</span><span class="sxs-lookup"><span data-stu-id="9d2de-145">MoveItem operation</span></span>](moveitem-operation.md)
  
[<span data-ttu-id="9d2de-146">CopyItem Operation</span><span class="sxs-lookup"><span data-stu-id="9d2de-146">CopyItem operation</span></span>](copyitem-operation.md)

