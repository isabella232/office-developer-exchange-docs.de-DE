---
title: ConversationNodes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5c8a35b8-a940-4b3e-8768-9ba95766fd79
description: Das ConversationNodes-Element gibt eine Auflistung von Knoten Unterhaltung.
ms.openlocfilehash: 62ec061f6d03abb9db7e511722e5570e70d65772
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757714"
---
# <a name="conversationnodes"></a><span data-ttu-id="458e9-103">ConversationNodes</span><span class="sxs-lookup"><span data-stu-id="458e9-103">ConversationNodes</span></span>

<span data-ttu-id="458e9-104">Das **ConversationNodes** -Element gibt eine Auflistung von Knoten Unterhaltung.</span><span class="sxs-lookup"><span data-stu-id="458e9-104">The **ConversationNodes** element specifies a collection of conversation nodes.</span></span> 
  
```XML
<ConversationNodes>
    <ConversationNode></ConversationNode>
</ConversationNodes>
```

 <span data-ttu-id="458e9-105">**ArrayOfConversationNodesType**</span><span class="sxs-lookup"><span data-stu-id="458e9-105">**ArrayOfConversationNodesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="458e9-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="458e9-106">Attributes and elements</span></span>

<span data-ttu-id="458e9-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="458e9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="458e9-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="458e9-108">Attributes</span></span>

<span data-ttu-id="458e9-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="458e9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="458e9-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="458e9-110">Child elements</span></span>

|<span data-ttu-id="458e9-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="458e9-111">**Element**</span></span>|<span data-ttu-id="458e9-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="458e9-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="458e9-113">ConversationNode</span><span class="sxs-lookup"><span data-stu-id="458e9-113">ConversationNode</span></span>](conversationnode.md) <br/> |<span data-ttu-id="458e9-114">Gibt einen Knoten in einer Unterhaltung.</span><span class="sxs-lookup"><span data-stu-id="458e9-114">Specifies a node in a conversation.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="458e9-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="458e9-115">Parent elements</span></span>

|<span data-ttu-id="458e9-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="458e9-116">**Element**</span></span>|<span data-ttu-id="458e9-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="458e9-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="458e9-118">Unterhaltung (ConversationResponseType)</span><span class="sxs-lookup"><span data-stu-id="458e9-118">Conversation (ConversationResponseType)</span></span>](conversation-conversationresponsetype.md) <br/> |<span data-ttu-id="458e9-119">Stellt eine einzelne Unterhaltung in einer Antwort **GetConversationItems** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="458e9-119">Represents a single conversation returned in a **GetConversationItems** response.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="458e9-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="458e9-120">Remarks</span></span>

<span data-ttu-id="458e9-121">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="458e9-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="458e9-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="458e9-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="458e9-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="458e9-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="458e9-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="458e9-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="458e9-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="458e9-125">Schema Name</span></span>  <br/> |<span data-ttu-id="458e9-126">Typschema</span><span class="sxs-lookup"><span data-stu-id="458e9-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="458e9-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="458e9-127">Validation File</span></span>  <br/> |<span data-ttu-id="458e9-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="458e9-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="458e9-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="458e9-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="458e9-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="458e9-130">See also</span></span>



- [<span data-ttu-id="458e9-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="458e9-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

