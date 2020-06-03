---
title: AddBlankTargetToLinks
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 30180298-2501-4369-9b8f-2f7663f02336
description: Das AddBlankTargetToLinks-Element gibt an, dass das target-Attribut in HTML-Links so festgelegt ist, dass ein neues Fenster geöffnet wird.
ms.openlocfilehash: 1d4d36c1f4b98ebee96baea683c40527d2a9ec27
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465043"
---
# <a name="addblanktargettolinks"></a><span data-ttu-id="3ad3a-103">AddBlankTargetToLinks</span><span class="sxs-lookup"><span data-stu-id="3ad3a-103">AddBlankTargetToLinks</span></span>

<span data-ttu-id="3ad3a-104">Das **AddBlankTargetToLinks** -Element gibt an, dass das target-Attribut in HTML-Links so festgelegt ist, dass ein neues Fenster geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="3ad3a-104">The **AddBlankTargetToLinks** element specifies that the target attribute in HTML links are set to open a new window.</span></span> 
  
```XML
<AddBlankTargetToLinks> true | false </AddBlankTargetToLinks>
```

<span data-ttu-id="3ad3a-105">**xs: Boolean**</span><span class="sxs-lookup"><span data-stu-id="3ad3a-105">**xs:Boolean**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="3ad3a-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3ad3a-106">Attributes and elements</span></span>

<span data-ttu-id="3ad3a-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="3ad3a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3ad3a-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="3ad3a-108">Attributes</span></span>

<span data-ttu-id="3ad3a-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="3ad3a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3ad3a-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3ad3a-110">Child elements</span></span>

<span data-ttu-id="3ad3a-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="3ad3a-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3ad3a-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3ad3a-112">Parent elements</span></span>

|<span data-ttu-id="3ad3a-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="3ad3a-113">**Element**</span></span>|<span data-ttu-id="3ad3a-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3ad3a-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3ad3a-115">ItemShape</span><span class="sxs-lookup"><span data-stu-id="3ad3a-115">ItemShape</span></span>](itemshape.md) <br/> | <span data-ttu-id="3ad3a-116">Identifiziert die Elementeigenschaften und Inhalte, die in einer **GetItem**-, **FindItem**-, **GetConversationItems** -oder **SyncFolderItems** -Antwort enthalten sein sollen.</span><span class="sxs-lookup"><span data-stu-id="3ad3a-116">Identifies the item properties and content to include in a **GetItem**, **FindItem**, **GetConversationItems** or **SyncFolderItems** response.</span></span><br/><br/>  <span data-ttu-id="3ad3a-117">Folgende XPath-Ausdrücke werden für dieses Element verwendet:</span><span class="sxs-lookup"><span data-stu-id="3ad3a-117">The following are the XPath expressions to this element:</span></span><br/><br/>  `/GetItem/ItemShape` <br/>  `/FindItem/ItemShape` <br/>  `/SyncFolderItems/ItemShape` <br/>  `/GetConversationItems/ItemShape` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3ad3a-118">Textwert</span><span class="sxs-lookup"><span data-stu-id="3ad3a-118">Text value</span></span>

<span data-ttu-id="3ad3a-119">Der Textwert **true** für das **AddBlankTargetToLinks** -Element gibt an, dass alle HTML-Links festgelegt werden, um ein neues Fenster zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="3ad3a-119">A text value of **true** for the **AddBlankTargetToLinks** element indicates that all HTML links will be set to open a new window.</span></span> <span data-ttu-id="3ad3a-120">Der Wert **false** gibt an, dass HTML-Links im aktuellen Fenster geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="3ad3a-120">A value of **false** indicates that HTML links will open in the current window.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3ad3a-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3ad3a-121">Remarks</span></span>

<span data-ttu-id="3ad3a-122">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="3ad3a-122">This element is optional.</span></span>
  
<span data-ttu-id="3ad3a-123">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="3ad3a-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="3ad3a-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="3ad3a-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3ad3a-125">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="3ad3a-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3ad3a-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="3ad3a-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3ad3a-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="3ad3a-127">Schema Name</span></span>  <br/> |<span data-ttu-id="3ad3a-128">Typschema</span><span class="sxs-lookup"><span data-stu-id="3ad3a-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="3ad3a-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="3ad3a-129">Validation File</span></span>  <br/> |<span data-ttu-id="3ad3a-130">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="3ad3a-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="3ad3a-131">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="3ad3a-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="3ad3a-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3ad3a-132">See also</span></span>

- [<span data-ttu-id="3ad3a-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="3ad3a-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

