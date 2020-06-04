---
title: Tofolder-Datei
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
description: Das tofolder-Element stellt den Zielordner für ein kopiertes oder verschobenes Element oder einen verschobenen Ordner dar.
ms.openlocfilehash: c9cceb17fd55b7357d54b37bf4c8da1137d39b6a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468775"
---
# <a name="tofolderid"></a><span data-ttu-id="24904-103">Tofolder-Datei</span><span class="sxs-lookup"><span data-stu-id="24904-103">ToFolderId</span></span>

<span data-ttu-id="24904-104">Das **tofolder** -Element stellt den Zielordner für ein kopiertes oder verschobenes Element oder einen verschobenen Ordner dar.</span><span class="sxs-lookup"><span data-stu-id="24904-104">The **ToFolderId** element represents the destination folder for a copied or moved item or folder.</span></span> 
  
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

<span data-ttu-id="24904-105">**TargetFolderIdType**</span><span class="sxs-lookup"><span data-stu-id="24904-105">**TargetFolderIdType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="24904-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="24904-106">Attributes and elements</span></span>

<span data-ttu-id="24904-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="24904-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="24904-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="24904-108">Attributes</span></span>

<span data-ttu-id="24904-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="24904-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="24904-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="24904-110">Child elements</span></span>

|<span data-ttu-id="24904-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="24904-111">**Element**</span></span>|<span data-ttu-id="24904-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="24904-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="24904-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="24904-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="24904-114">Enthält den Bezeichner eines Zielordners für ein kopiertes oder verschobenes Element oder einen verschobenen Ordner.</span><span class="sxs-lookup"><span data-stu-id="24904-114">Contains the identifier of a destination folder for a copied or moved item or folder.</span></span>  <br/> |
|[<span data-ttu-id="24904-115">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="24904-115">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="24904-116">Gibt einen benannten Zielordner für ein kopiertes oder verschobenes Element oder einen Ordner an.</span><span class="sxs-lookup"><span data-stu-id="24904-116">Identifies a named destination folder for a copied or moved item or folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="24904-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="24904-117">Parent elements</span></span>

|<span data-ttu-id="24904-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="24904-118">**Element**</span></span>|<span data-ttu-id="24904-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="24904-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="24904-120">MoveFolder</span><span class="sxs-lookup"><span data-stu-id="24904-120">MoveFolder</span></span>](movefolder.md) <br/> |<span data-ttu-id="24904-121">Definiert eine Anforderung zum Migrieren eines Ordners in der Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="24904-121">Defines a request to move a folder in the Exchange store.</span></span>  <br/> <span data-ttu-id="24904-122">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="24904-122">The following is the XPath expression to this element:</span></span>  <br/>  `/MoveFolder` <br/> |
|[<span data-ttu-id="24904-123">CopyFolder</span><span class="sxs-lookup"><span data-stu-id="24904-123">CopyFolder</span></span>](copyfolder.md) <br/> |<span data-ttu-id="24904-124">Definiert eine Anforderung zum Kopieren eines Ordners in der Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="24904-124">Defines a request to copy a folder in the Exchange store.</span></span>  <br/> <span data-ttu-id="24904-125">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="24904-125">The following is the XPath expression to this element:</span></span>  <br/>  `/CopyFolder` <br/> |
|[<span data-ttu-id="24904-126">MoveItem</span><span class="sxs-lookup"><span data-stu-id="24904-126">MoveItem</span></span>](moveitem.md) <br/> |<span data-ttu-id="24904-127">Definiert eine Anforderung zum verlagern eines Elements in der Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="24904-127">Defines a request to move an item in the Exchange store.</span></span>  <br/> <span data-ttu-id="24904-128">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="24904-128">The following is the XPath expression to this element:</span></span>  <br/>  `/MoveItem` <br/> |
|[<span data-ttu-id="24904-129">CopyItem</span><span class="sxs-lookup"><span data-stu-id="24904-129">CopyItem</span></span>](copyitem.md) <br/> |<span data-ttu-id="24904-130">Definiert eine Anforderung zum Kopieren eines Elements in der Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="24904-130">Defines a request to copy an item in the Exchange store.</span></span>  <br/> <span data-ttu-id="24904-131">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="24904-131">The following is the XPath expression to this element:</span></span>  <br/>  `/CopyItem` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="24904-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="24904-132">Remarks</span></span>

<span data-ttu-id="24904-133">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="24904-133">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="24904-134">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="24904-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="24904-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="24904-135">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="24904-136">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="24904-136">Schema Name</span></span>  <br/> |<span data-ttu-id="24904-137">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="24904-137">Messages schema</span></span>  <br/> |
|<span data-ttu-id="24904-138">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="24904-138">Validation File</span></span>  <br/> |<span data-ttu-id="24904-139">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="24904-139">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="24904-140">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="24904-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="24904-141">False</span><span class="sxs-lookup"><span data-stu-id="24904-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="24904-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="24904-142">See also</span></span>

- [<span data-ttu-id="24904-143">MoveFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="24904-143">MoveFolder operation</span></span>](movefolder-operation.md)  
- [<span data-ttu-id="24904-144">CopyFolder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="24904-144">CopyFolder operation</span></span>](copyfolder-operation.md) 
- [<span data-ttu-id="24904-145">MoveItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="24904-145">MoveItem operation</span></span>](moveitem-operation.md) 
- [<span data-ttu-id="24904-146">CopyItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="24904-146">CopyItem operation</span></span>](copyitem-operation.md)

