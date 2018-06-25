---
title: GlobalParentFolderIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8f5fcbcb-05ed-462a-99cf-a6b112a4aef6
description: Das GlobalParentFolderIds-Element gibt den Bezeichner der globalen übergeordneten Ordner.
ms.openlocfilehash: b0ff9ab00f3e46351b5a2db9bc4b6282fa4385cd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19829747"
---
# <a name="globalparentfolderids"></a><span data-ttu-id="eea4c-103">GlobalParentFolderIds</span><span class="sxs-lookup"><span data-stu-id="eea4c-103">GlobalParentFolderIds</span></span>

<span data-ttu-id="eea4c-104">Das **GlobalParentFolderIds** -Element gibt den Bezeichner der globalen übergeordneten Ordner.</span><span class="sxs-lookup"><span data-stu-id="eea4c-104">The **GlobalParentFolderIds** element specifies the identifiers of the global parent folders.</span></span> 
  
```XML
<GlobalParentFolderIds>
    <FolderId/>
    <DistinguishedFolderId/>
</GlobalParentFolderIds>
```

 <span data-ttu-id="eea4c-105">**NonEmptyArrayOfBaseFolderIdsType**</span><span class="sxs-lookup"><span data-stu-id="eea4c-105">**NonEmptyArrayOfBaseFolderIdsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="eea4c-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="eea4c-106">Attributes and elements</span></span>

<span data-ttu-id="eea4c-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="eea4c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="eea4c-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="eea4c-108">Attributes</span></span>

<span data-ttu-id="eea4c-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="eea4c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="eea4c-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="eea4c-110">Child elements</span></span>

|<span data-ttu-id="eea4c-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="eea4c-111">**Element**</span></span>|<span data-ttu-id="eea4c-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="eea4c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="eea4c-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="eea4c-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="eea4c-114">Enthält den Schlüssel-ID und Ändern eines Ordners.</span><span class="sxs-lookup"><span data-stu-id="eea4c-114">Contains the identifier and change key of a folder.</span></span>  <br/> |
|[<span data-ttu-id="eea4c-115">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="eea4c-115">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="eea4c-116">Bezeichnet die Ordner, die nach Namen verwiesen werden können.</span><span class="sxs-lookup"><span data-stu-id="eea4c-116">Identifies folders that can be referenced by name.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="eea4c-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="eea4c-117">Parent elements</span></span>

|<span data-ttu-id="eea4c-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="eea4c-118">**Element**</span></span>|<span data-ttu-id="eea4c-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="eea4c-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="eea4c-120">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="eea4c-120">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="eea4c-121">Stellt eine einfache Unterhaltung dar.</span><span class="sxs-lookup"><span data-stu-id="eea4c-121">Represents a single conversation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eea4c-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="eea4c-122">Remarks</span></span>

<span data-ttu-id="eea4c-123">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="eea4c-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="eea4c-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="eea4c-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="eea4c-125">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="eea4c-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="eea4c-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="eea4c-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="eea4c-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="eea4c-127">Schema Name</span></span>  <br/> |<span data-ttu-id="eea4c-128">Typschema</span><span class="sxs-lookup"><span data-stu-id="eea4c-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="eea4c-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="eea4c-129">Validation File</span></span>  <br/> |<span data-ttu-id="eea4c-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="eea4c-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="eea4c-131">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="eea4c-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="eea4c-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eea4c-132">See also</span></span>



- [<span data-ttu-id="eea4c-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="eea4c-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

