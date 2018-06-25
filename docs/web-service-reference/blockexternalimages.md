---
title: BlockExternalImages
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5c754dfc-a9e9-4272-9b5f-5fe3db537e62
description: Das BlockExternalImages-Element gibt an, ob externe Bilder in HTML-Text Texte blockiert sind.
ms.openlocfilehash: 41ab2ec7ec1c24ccbbef037ef1e27431c1fe6811
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757446"
---
# <a name="blockexternalimages"></a><span data-ttu-id="c0ca1-103">BlockExternalImages</span><span class="sxs-lookup"><span data-stu-id="c0ca1-103">BlockExternalImages</span></span>

<span data-ttu-id="c0ca1-104">Das **BlockExternalImages** -Element gibt an, ob externe Bilder in HTML-Text Texte blockiert sind.</span><span class="sxs-lookup"><span data-stu-id="c0ca1-104">The **BlockExternalImages** element specifies whether external images are blocked in HTML text bodies.</span></span> 
  
```XML
<BlockExternalImages> true | false </BlockExternalImages>
```

 <span data-ttu-id="c0ca1-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="c0ca1-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c0ca1-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c0ca1-106">Attributes and elements</span></span>

<span data-ttu-id="c0ca1-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c0ca1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c0ca1-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="c0ca1-108">Attributes</span></span>

<span data-ttu-id="c0ca1-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="c0ca1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c0ca1-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c0ca1-110">Child elements</span></span>

<span data-ttu-id="c0ca1-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="c0ca1-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c0ca1-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c0ca1-112">Parent elements</span></span>

|<span data-ttu-id="c0ca1-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="c0ca1-113">**Element**</span></span>|<span data-ttu-id="c0ca1-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c0ca1-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c0ca1-115">FolderShape</span><span class="sxs-lookup"><span data-stu-id="c0ca1-115">FolderShape</span></span>](foldershape.md) <br/> |<span data-ttu-id="c0ca1-116">Identifiziert die Ordnereigenschaften in der Antwort GetFolder, FindFolder oder SyncFolderHierarchy aufzunehmen.</span><span class="sxs-lookup"><span data-stu-id="c0ca1-116">Identifies the folder properties to include in the GetFolder, FindFolder, or SyncFolderHierarchy response.</span></span>  <br/> |
|[<span data-ttu-id="c0ca1-117">ItemShape</span><span class="sxs-lookup"><span data-stu-id="c0ca1-117">ItemShape</span></span>](itemshape.md) <br/> |<span data-ttu-id="c0ca1-118">Identifiziert die Elementeigenschaften und den Inhalt in einer Antwort GetItem, FindItem oder SyncFolderItems aufzunehmen.</span><span class="sxs-lookup"><span data-stu-id="c0ca1-118">Identifies the item properties and content to include in a GetItem, FindItem, or SyncFolderItems response.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c0ca1-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="c0ca1-119">Text value</span></span>

<span data-ttu-id="c0ca1-120">Der Textwert **true** für **BlockExternalImages** -Element gibt an, dass externe Bilder in HTML-Textkörper blockiert sind.</span><span class="sxs-lookup"><span data-stu-id="c0ca1-120">A text value of **true** for **BlockExternalImages** element indicates that external images are blocked in HTML bodies.</span></span> <span data-ttu-id="c0ca1-121">Der Wert **false** gibt an, dass externe Bilder zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="c0ca1-121">A value of **false** indicates that external images are allowed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c0ca1-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c0ca1-122">Remarks</span></span>

<span data-ttu-id="c0ca1-123">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="c0ca1-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="c0ca1-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="c0ca1-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c0ca1-125">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="c0ca1-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c0ca1-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="c0ca1-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c0ca1-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c0ca1-127">Schema Name</span></span>  <br/> |<span data-ttu-id="c0ca1-128">Typschema</span><span class="sxs-lookup"><span data-stu-id="c0ca1-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="c0ca1-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c0ca1-129">Validation File</span></span>  <br/> |<span data-ttu-id="c0ca1-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c0ca1-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="c0ca1-131">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="c0ca1-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="c0ca1-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c0ca1-132">See also</span></span>



- [<span data-ttu-id="c0ca1-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="c0ca1-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

