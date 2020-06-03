---
title: GlobalParentFolderIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8f5fcbcb-05ed-462a-99cf-a6b112a4aef6
description: Das GlobalParentFolderIds-Element gibt die Bezeichner der globalen übergeordneten Ordner an.
ms.openlocfilehash: 11c520fa0f4a1ed6d6c9d694b407e39cd036b9cd
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459097"
---
# <a name="globalparentfolderids"></a><span data-ttu-id="17459-103">GlobalParentFolderIds</span><span class="sxs-lookup"><span data-stu-id="17459-103">GlobalParentFolderIds</span></span>

<span data-ttu-id="17459-104">Das **GlobalParentFolderIds** -Element gibt die Bezeichner der globalen übergeordneten Ordner an.</span><span class="sxs-lookup"><span data-stu-id="17459-104">The **GlobalParentFolderIds** element specifies the identifiers of the global parent folders.</span></span> 
  
```XML
<GlobalParentFolderIds>
    <FolderId/>
    <DistinguishedFolderId/>
</GlobalParentFolderIds>
```

 <span data-ttu-id="17459-105">**NonEmptyArrayOfBaseFolderIdsType**</span><span class="sxs-lookup"><span data-stu-id="17459-105">**NonEmptyArrayOfBaseFolderIdsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="17459-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="17459-106">Attributes and elements</span></span>

<span data-ttu-id="17459-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="17459-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="17459-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="17459-108">Attributes</span></span>

<span data-ttu-id="17459-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="17459-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="17459-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="17459-110">Child elements</span></span>

|<span data-ttu-id="17459-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="17459-111">**Element**</span></span>|<span data-ttu-id="17459-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="17459-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="17459-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="17459-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="17459-114">Enthält den Bezeichner und den Änderungsschlüssel eines Ordners.</span><span class="sxs-lookup"><span data-stu-id="17459-114">Contains the identifier and change key of a folder.</span></span>  <br/> |
|[<span data-ttu-id="17459-115">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="17459-115">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="17459-116">Identifiziert Ordner, auf die über den Namen verwiesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="17459-116">Identifies folders that can be referenced by name.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="17459-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="17459-117">Parent elements</span></span>

|<span data-ttu-id="17459-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="17459-118">**Element**</span></span>|<span data-ttu-id="17459-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="17459-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="17459-120">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="17459-120">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="17459-121">Stellt eine einfache Unterhaltung dar.</span><span class="sxs-lookup"><span data-stu-id="17459-121">Represents a single conversation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="17459-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="17459-122">Remarks</span></span>

<span data-ttu-id="17459-123">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="17459-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="17459-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="17459-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="17459-125">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="17459-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="17459-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="17459-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="17459-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="17459-127">Schema Name</span></span>  <br/> |<span data-ttu-id="17459-128">Typschema</span><span class="sxs-lookup"><span data-stu-id="17459-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="17459-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="17459-129">Validation File</span></span>  <br/> |<span data-ttu-id="17459-130">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="17459-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="17459-131">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="17459-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="17459-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="17459-132">See also</span></span>



- [<span data-ttu-id="17459-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="17459-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

