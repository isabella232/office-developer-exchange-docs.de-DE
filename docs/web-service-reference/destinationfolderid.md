---
title: DestinationFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DestinationFolderId
api_type:
- schema
ms.assetid: 77d2d222-320b-4aab-88e4-934ef177f55c
description: Das DestinationFolderId-Element gibt den Zielordner für die Kopie an und Aktionen zu verschieben.
ms.openlocfilehash: bfbacb9c82a681c7963ab5164c43cbb648e726cd
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353378"
---
# <a name="destinationfolderid"></a><span data-ttu-id="77acf-103">DestinationFolderId</span><span class="sxs-lookup"><span data-stu-id="77acf-103">DestinationFolderId</span></span>

<span data-ttu-id="77acf-104">Das **DestinationFolderId** -Element gibt den Zielordner für die Kopie an und Aktionen zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="77acf-104">The **DestinationFolderId** element indicates the destination folder for copy and move actions.</span></span> 
  
- [<span data-ttu-id="77acf-105">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="77acf-105">ApplyConversationAction</span></span>](applyconversationaction.md)  
- [<span data-ttu-id="77acf-106">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="77acf-106">ConversationActions</span></span>](conversationactions.md) 
- [<span data-ttu-id="77acf-107">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="77acf-107">ConversationAction</span></span>](conversationaction.md)  
- [<span data-ttu-id="77acf-108">DestinationFolderId</span><span class="sxs-lookup"><span data-stu-id="77acf-108">DestinationFolderId</span></span>](destinationfolderid.md)
  
```XML
<DestinationFolderId>
   <FolderId/>
</DestinationFolderId>
```

```XML
<DestinationFolderId>
   <DistinguishedFolderId/>
</DestinationFolderId>
```

<span data-ttu-id="77acf-109">**TargetFolderIdType**</span><span class="sxs-lookup"><span data-stu-id="77acf-109">**TargetFolderIdType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="77acf-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="77acf-110">Attributes and elements</span></span>

<span data-ttu-id="77acf-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="77acf-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="77acf-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="77acf-112">Attributes</span></span>

<span data-ttu-id="77acf-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="77acf-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="77acf-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="77acf-114">Child elements</span></span>

|<span data-ttu-id="77acf-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="77acf-115">**Element**</span></span>|<span data-ttu-id="77acf-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="77acf-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="77acf-117">FolderId</span><span class="sxs-lookup"><span data-stu-id="77acf-117">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="77acf-118">Enthält den Schlüssel-ID und Ändern des Zielordners.</span><span class="sxs-lookup"><span data-stu-id="77acf-118">Contains the identifier and change key of the destination folder.</span></span>  <br/> |
|[<span data-ttu-id="77acf-119">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="77acf-119">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="77acf-120">Bezeichnet die Ordner, die nach Namen verwiesen werden können.</span><span class="sxs-lookup"><span data-stu-id="77acf-120">Identifies folders that can be referenced by name.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="77acf-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="77acf-121">Parent elements</span></span>

|<span data-ttu-id="77acf-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="77acf-122">**Element**</span></span>|<span data-ttu-id="77acf-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="77acf-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="77acf-124">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="77acf-124">ConversationAction</span></span>](conversationaction.md) <br/> |<span data-ttu-id="77acf-125">Enthält eine einzelne Aktion auf einem einzelnen Gespräch angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="77acf-125">Contains a single action to be applied to a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="77acf-126">Textwert</span><span class="sxs-lookup"><span data-stu-id="77acf-126">Text value</span></span>

<span data-ttu-id="77acf-127">Keine.</span><span class="sxs-lookup"><span data-stu-id="77acf-127">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="77acf-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="77acf-128">Remarks</span></span>

<span data-ttu-id="77acf-129">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="77acf-129">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="77acf-130">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="77acf-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="77acf-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="77acf-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="77acf-132">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="77acf-132">Schema Name</span></span>  <br/> |<span data-ttu-id="77acf-133">Schematypen</span><span class="sxs-lookup"><span data-stu-id="77acf-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="77acf-134">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="77acf-134">Validation File</span></span>  <br/> |<span data-ttu-id="77acf-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="77acf-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="77acf-136">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="77acf-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="77acf-137">False</span><span class="sxs-lookup"><span data-stu-id="77acf-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="77acf-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="77acf-138">See also</span></span>

- [<span data-ttu-id="77acf-139">ApplyConversationAction-Vorgang</span><span class="sxs-lookup"><span data-stu-id="77acf-139">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)

