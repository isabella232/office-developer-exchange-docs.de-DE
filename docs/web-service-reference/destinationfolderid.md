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
description: Das DestinationFolderId-Element gibt den Zielordner für die Aktionen kopieren und verlegen an.
ms.openlocfilehash: dbfd25084dbd4ea9d5f4ddf98b256d02e71139d3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526914"
---
# <a name="destinationfolderid"></a><span data-ttu-id="c0fd0-103">DestinationFolderId</span><span class="sxs-lookup"><span data-stu-id="c0fd0-103">DestinationFolderId</span></span>

<span data-ttu-id="c0fd0-104">Das **DestinationFolderId** -Element gibt den Zielordner für die Aktionen kopieren und verlegen an.</span><span class="sxs-lookup"><span data-stu-id="c0fd0-104">The **DestinationFolderId** element indicates the destination folder for copy and move actions.</span></span> 
  
- [<span data-ttu-id="c0fd0-105">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="c0fd0-105">ApplyConversationAction</span></span>](applyconversationaction.md)  
- [<span data-ttu-id="c0fd0-106">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="c0fd0-106">ConversationActions</span></span>](conversationactions.md) 
- [<span data-ttu-id="c0fd0-107">Unterhaltung</span><span class="sxs-lookup"><span data-stu-id="c0fd0-107">ConversationAction</span></span>](conversationaction.md)  
- [<span data-ttu-id="c0fd0-108">DestinationFolderId</span><span class="sxs-lookup"><span data-stu-id="c0fd0-108">DestinationFolderId</span></span>](destinationfolderid.md)
  
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

<span data-ttu-id="c0fd0-109">**TargetFolderIdType**</span><span class="sxs-lookup"><span data-stu-id="c0fd0-109">**TargetFolderIdType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="c0fd0-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c0fd0-110">Attributes and elements</span></span>

<span data-ttu-id="c0fd0-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c0fd0-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c0fd0-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="c0fd0-112">Attributes</span></span>

<span data-ttu-id="c0fd0-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="c0fd0-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c0fd0-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c0fd0-114">Child elements</span></span>

|<span data-ttu-id="c0fd0-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="c0fd0-115">**Element**</span></span>|<span data-ttu-id="c0fd0-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c0fd0-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c0fd0-117">FolderId</span><span class="sxs-lookup"><span data-stu-id="c0fd0-117">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="c0fd0-118">Enthält den Bezeichner und den Änderungsschlüssel des Zielordners.</span><span class="sxs-lookup"><span data-stu-id="c0fd0-118">Contains the identifier and change key of the destination folder.</span></span>  <br/> |
|[<span data-ttu-id="c0fd0-119">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="c0fd0-119">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="c0fd0-120">Identifiziert Ordner, auf die über den Namen verwiesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="c0fd0-120">Identifies folders that can be referenced by name.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c0fd0-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c0fd0-121">Parent elements</span></span>

|<span data-ttu-id="c0fd0-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="c0fd0-122">**Element**</span></span>|<span data-ttu-id="c0fd0-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c0fd0-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c0fd0-124">Unterhaltung</span><span class="sxs-lookup"><span data-stu-id="c0fd0-124">ConversationAction</span></span>](conversationaction.md) <br/> |<span data-ttu-id="c0fd0-125">Enthält eine einzelne Aktion, die auf eine einzelne Unterhaltung angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c0fd0-125">Contains a single action to be applied to a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c0fd0-126">Textwert</span><span class="sxs-lookup"><span data-stu-id="c0fd0-126">Text value</span></span>

<span data-ttu-id="c0fd0-127">Keine.</span><span class="sxs-lookup"><span data-stu-id="c0fd0-127">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c0fd0-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c0fd0-128">Remarks</span></span>

<span data-ttu-id="c0fd0-129">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="c0fd0-129">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c0fd0-130">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="c0fd0-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c0fd0-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="c0fd0-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c0fd0-132">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c0fd0-132">Schema Name</span></span>  <br/> |<span data-ttu-id="c0fd0-133">Schematypen</span><span class="sxs-lookup"><span data-stu-id="c0fd0-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="c0fd0-134">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c0fd0-134">Validation File</span></span>  <br/> |<span data-ttu-id="c0fd0-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c0fd0-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c0fd0-136">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="c0fd0-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="c0fd0-137">False</span><span class="sxs-lookup"><span data-stu-id="c0fd0-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c0fd0-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c0fd0-138">See also</span></span>

- [<span data-ttu-id="c0fd0-139">ApplyConversationAction-Vorgang</span><span class="sxs-lookup"><span data-stu-id="c0fd0-139">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)

