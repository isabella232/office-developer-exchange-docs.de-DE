---
title: BlockExternalImages
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5c754dfc-a9e9-4272-9b5f-5fe3db537e62
description: Das BlockExternalImages-Element gibt an, ob externe Bilder in HTML-Textkörpern blockiert werden.
ms.openlocfilehash: 73342316024ebe476a0e35f14157befc80edcf83
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527404"
---
# <a name="blockexternalimages"></a><span data-ttu-id="0cccb-103">BlockExternalImages</span><span class="sxs-lookup"><span data-stu-id="0cccb-103">BlockExternalImages</span></span>

<span data-ttu-id="0cccb-104">Das **BlockExternalImages** -Element gibt an, ob externe Bilder in HTML-Textkörpern blockiert werden.</span><span class="sxs-lookup"><span data-stu-id="0cccb-104">The **BlockExternalImages** element specifies whether external images are blocked in HTML text bodies.</span></span> 
  
```XML
<BlockExternalImages> true | false </BlockExternalImages>
```

 <span data-ttu-id="0cccb-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="0cccb-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0cccb-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="0cccb-106">Attributes and elements</span></span>

<span data-ttu-id="0cccb-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="0cccb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0cccb-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="0cccb-108">Attributes</span></span>

<span data-ttu-id="0cccb-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="0cccb-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0cccb-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0cccb-110">Child elements</span></span>

<span data-ttu-id="0cccb-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="0cccb-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0cccb-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0cccb-112">Parent elements</span></span>

|<span data-ttu-id="0cccb-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="0cccb-113">**Element**</span></span>|<span data-ttu-id="0cccb-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0cccb-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0cccb-115">FolderShape</span><span class="sxs-lookup"><span data-stu-id="0cccb-115">FolderShape</span></span>](foldershape.md) <br/> |<span data-ttu-id="0cccb-116">Identifiziert die Ordner Eigenschaften, die in die GetFolder-, FindFolder-oder SyncFolderHierarchy-Antwort eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0cccb-116">Identifies the folder properties to include in the GetFolder, FindFolder, or SyncFolderHierarchy response.</span></span>  <br/> |
|[<span data-ttu-id="0cccb-117">ItemShape</span><span class="sxs-lookup"><span data-stu-id="0cccb-117">ItemShape</span></span>](itemshape.md) <br/> |<span data-ttu-id="0cccb-118">Identifiziert die Elementeigenschaften und Inhalte, die in einer GetItem-, FindItem-oder SyncFolderItems-Antwort enthalten sein sollen.</span><span class="sxs-lookup"><span data-stu-id="0cccb-118">Identifies the item properties and content to include in a GetItem, FindItem, or SyncFolderItems response.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0cccb-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="0cccb-119">Text value</span></span>

<span data-ttu-id="0cccb-120">Der Textwert **true** für **BlockExternalImages** -Element gibt an, dass externe Bilder in HTML-Textkörpern blockiert werden.</span><span class="sxs-lookup"><span data-stu-id="0cccb-120">A text value of **true** for **BlockExternalImages** element indicates that external images are blocked in HTML bodies.</span></span> <span data-ttu-id="0cccb-121">Der Wert **false** gibt an, dass externe Bilder zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="0cccb-121">A value of **false** indicates that external images are allowed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="0cccb-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0cccb-122">Remarks</span></span>

<span data-ttu-id="0cccb-123">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0cccb-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="0cccb-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="0cccb-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0cccb-125">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="0cccb-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0cccb-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="0cccb-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0cccb-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="0cccb-127">Schema Name</span></span>  <br/> |<span data-ttu-id="0cccb-128">Typschema</span><span class="sxs-lookup"><span data-stu-id="0cccb-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="0cccb-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="0cccb-129">Validation File</span></span>  <br/> |<span data-ttu-id="0cccb-130">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="0cccb-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="0cccb-131">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="0cccb-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="0cccb-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0cccb-132">See also</span></span>



- [<span data-ttu-id="0cccb-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="0cccb-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

