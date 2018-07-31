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
ms.openlocfilehash: 9d2fd6c177711cfe3a5d3415320440259e2f5289
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353658"
---
# <a name="tofolderid"></a><span data-ttu-id="d2e3e-103">ToFolderId</span><span class="sxs-lookup"><span data-stu-id="d2e3e-103">ToFolderId</span></span>

<span data-ttu-id="d2e3e-104">Das **ToFolderId** -Element darstellt, den Zielordner für eine kopierte oder verschobene Element oder einen Ordner.</span><span class="sxs-lookup"><span data-stu-id="d2e3e-104">The **ToFolderId** element represents the destination folder for a copied or moved item or folder.</span></span> 
  
```xml
<ToFolderId>
   <FolderId/>
</ToFolderId>
```

```xml
<ToFolderId>
   <DistinguishedFolderId/>
</ToFolderId>
```

<span data-ttu-id="d2e3e-105">**TargetFolderIdType**</span><span class="sxs-lookup"><span data-stu-id="d2e3e-105">**TargetFolderIdType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="d2e3e-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d2e3e-106">Attributes and elements</span></span>

<span data-ttu-id="d2e3e-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d2e3e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d2e3e-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d2e3e-108">Attributes</span></span>

<span data-ttu-id="d2e3e-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="d2e3e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d2e3e-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d2e3e-110">Child elements</span></span>

|<span data-ttu-id="d2e3e-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="d2e3e-111">**Element**</span></span>|<span data-ttu-id="d2e3e-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d2e3e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d2e3e-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="d2e3e-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="d2e3e-114">Enthält den Bezeichner des Zielordners für eine kopierte oder verschobene Element oder einen Ordner.</span><span class="sxs-lookup"><span data-stu-id="d2e3e-114">Contains the identifier of a destination folder for a copied or moved item or folder.</span></span>  <br/> |
|[<span data-ttu-id="d2e3e-115">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="d2e3e-115">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="d2e3e-116">Gibt einen benannten Zielordner für eine kopierte oder verschobene Element oder einen Ordner.</span><span class="sxs-lookup"><span data-stu-id="d2e3e-116">Identifies a named destination folder for a copied or moved item or folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d2e3e-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d2e3e-117">Parent elements</span></span>

|<span data-ttu-id="d2e3e-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="d2e3e-118">**Element**</span></span>|<span data-ttu-id="d2e3e-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d2e3e-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d2e3e-120">MoveFolder</span><span class="sxs-lookup"><span data-stu-id="d2e3e-120">MoveFolder</span></span>](movefolder.md) <br/> |<span data-ttu-id="d2e3e-121">Definiert eine Anforderung an einen Ordner im Exchange-Speicher zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="d2e3e-121">Defines a request to move a folder in the Exchange store.</span></span>  <br/> <span data-ttu-id="d2e3e-122">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="d2e3e-122">The following is the XPath expression to this element:</span></span>  <br/>  `/MoveFolder` <br/> |
|[<span data-ttu-id="d2e3e-123">CopyFolder</span><span class="sxs-lookup"><span data-stu-id="d2e3e-123">CopyFolder</span></span>](copyfolder.md) <br/> |<span data-ttu-id="d2e3e-124">Definiert eine Anforderung an einen Ordner im Exchange-Speicher zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="d2e3e-124">Defines a request to copy a folder in the Exchange store.</span></span>  <br/> <span data-ttu-id="d2e3e-125">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="d2e3e-125">The following is the XPath expression to this element:</span></span>  <br/>  `/CopyFolder` <br/> |
|[<span data-ttu-id="d2e3e-126">MoveItem</span><span class="sxs-lookup"><span data-stu-id="d2e3e-126">MoveItem</span></span>](moveitem.md) <br/> |<span data-ttu-id="d2e3e-127">Definiert eine Anforderung an ein Element im Exchange-Speicher zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="d2e3e-127">Defines a request to move an item in the Exchange store.</span></span>  <br/> <span data-ttu-id="d2e3e-128">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="d2e3e-128">The following is the XPath expression to this element:</span></span>  <br/>  `/MoveItem` <br/> |
|[<span data-ttu-id="d2e3e-129">CopyItem</span><span class="sxs-lookup"><span data-stu-id="d2e3e-129">CopyItem</span></span>](copyitem.md) <br/> |<span data-ttu-id="d2e3e-130">Definiert eine Anforderung an ein Element im Exchange-Speicher zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="d2e3e-130">Defines a request to copy an item in the Exchange store.</span></span>  <br/> <span data-ttu-id="d2e3e-131">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="d2e3e-131">The following is the XPath expression to this element:</span></span>  <br/>  `/CopyItem` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d2e3e-132">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d2e3e-132">Remarks</span></span>

<span data-ttu-id="d2e3e-133">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="d2e3e-133">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d2e3e-134">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="d2e3e-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d2e3e-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="d2e3e-135">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d2e3e-136">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d2e3e-136">Schema Name</span></span>  <br/> |<span data-ttu-id="d2e3e-137">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="d2e3e-137">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d2e3e-138">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d2e3e-138">Validation File</span></span>  <br/> |<span data-ttu-id="d2e3e-139">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="d2e3e-139">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d2e3e-140">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d2e3e-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="d2e3e-141">False</span><span class="sxs-lookup"><span data-stu-id="d2e3e-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d2e3e-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d2e3e-142">See also</span></span>

- [<span data-ttu-id="d2e3e-143">MoveFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d2e3e-143">MoveFolder operation</span></span>](movefolder-operation.md)  
- [<span data-ttu-id="d2e3e-144">CopyFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d2e3e-144">CopyFolder operation</span></span>](copyfolder-operation.md) 
- [<span data-ttu-id="d2e3e-145">MoveItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d2e3e-145">MoveItem operation</span></span>](moveitem-operation.md) 
- [<span data-ttu-id="d2e3e-146">CopyItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d2e3e-146">CopyItem operation</span></span>](copyitem-operation.md)

