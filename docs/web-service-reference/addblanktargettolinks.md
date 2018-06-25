---
title: AddBlankTargetToLinks
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 30180298-2501-4369-9b8f-2f7663f02336
description: Das AddBlankTargetToLinks-Element gibt an, dass das Zielattribut in HTML-Links werden festgelegt, um ein neues Fenster zu öffnen.
ms.openlocfilehash: 8a47e44d89bcc84bc0e8b61d45f18ff3182f7870
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757216"
---
# <a name="addblanktargettolinks"></a><span data-ttu-id="559ee-103">AddBlankTargetToLinks</span><span class="sxs-lookup"><span data-stu-id="559ee-103">AddBlankTargetToLinks</span></span>

<span data-ttu-id="559ee-104">Das **AddBlankTargetToLinks** -Element gibt an, dass das Zielattribut in HTML-Links werden festgelegt, um ein neues Fenster zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="559ee-104">The **AddBlankTargetToLinks** element specifies that the target attribute in HTML links are set to open a new window.</span></span> 
  
```XML
<AddBlankTargetToLinks> true | false </AddBlankTargetToLinks>
```

<span data-ttu-id="559ee-105">**xs: Boolean**</span><span class="sxs-lookup"><span data-stu-id="559ee-105">**xs:Boolean**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="559ee-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="559ee-106">Attributes and elements</span></span>

<span data-ttu-id="559ee-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="559ee-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="559ee-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="559ee-108">Attributes</span></span>

<span data-ttu-id="559ee-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="559ee-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="559ee-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="559ee-110">Child elements</span></span>

<span data-ttu-id="559ee-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="559ee-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="559ee-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="559ee-112">Parent elements</span></span>

|<span data-ttu-id="559ee-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="559ee-113">**Element**</span></span>|<span data-ttu-id="559ee-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="559ee-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="559ee-115">ItemShape</span><span class="sxs-lookup"><span data-stu-id="559ee-115">ItemShape</span></span>](itemshape.md) <br/> | <span data-ttu-id="559ee-116">Identifiziert die Elementeigenschaften und Inhalte in **GetItem**, **FindItem**, **GetConversationItems** oder **SyncFolderItems** Antwort enthalten.</span><span class="sxs-lookup"><span data-stu-id="559ee-116">Identifies the item properties and content to include in a **GetItem**, **FindItem**, **GetConversationItems** or **SyncFolderItems** response.</span></span><br/><br/>  <span data-ttu-id="559ee-117">Folgende XPath-Ausdrücke werden für dieses Element verwendet:</span><span class="sxs-lookup"><span data-stu-id="559ee-117">The following are the XPath expressions to this element:</span></span><br/><br/>  `/GetItem/ItemShape` <br/>  `/FindItem/ItemShape` <br/>  `/SyncFolderItems/ItemShape` <br/>  `/GetConversationItems/ItemShape` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="559ee-118">Textwert</span><span class="sxs-lookup"><span data-stu-id="559ee-118">Text value</span></span>

<span data-ttu-id="559ee-119">Der Textwert **true** für das **AddBlankTargetToLinks** -Element gibt an, dass alle HTML-Links festgelegt wird, um ein neues Fenster zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="559ee-119">A text value of **true** for the **AddBlankTargetToLinks** element indicates that all HTML links will be set to open a new window.</span></span> <span data-ttu-id="559ee-120">Der Wert **false** gibt an, dass HTML-Links im aktuellen Fenster geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="559ee-120">A value of **false** indicates that HTML links will open in the current window.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="559ee-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="559ee-121">Remarks</span></span>

<span data-ttu-id="559ee-122">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="559ee-122">This element is optional.</span></span>
  
<span data-ttu-id="559ee-123">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="559ee-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="559ee-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="559ee-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="559ee-125">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="559ee-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="559ee-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="559ee-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="559ee-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="559ee-127">Schema Name</span></span>  <br/> |<span data-ttu-id="559ee-128">Typschema</span><span class="sxs-lookup"><span data-stu-id="559ee-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="559ee-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="559ee-129">Validation File</span></span>  <br/> |<span data-ttu-id="559ee-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="559ee-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="559ee-131">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="559ee-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="559ee-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="559ee-132">See also</span></span>

- [<span data-ttu-id="559ee-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="559ee-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

