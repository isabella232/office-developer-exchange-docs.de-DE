---
title: ConversationNode
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b7f7acd3-ed65-441e-9976-8b4ed5f12c0b
description: Das ConversationNode-Element gibt einen Knoten in einer Unterhaltung an.
ms.openlocfilehash: 074209c1b5669db8dd1ea4ba7f9dea064628afbd
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462703"
---
# <a name="conversationnode"></a><span data-ttu-id="dd716-103">ConversationNode</span><span class="sxs-lookup"><span data-stu-id="dd716-103">ConversationNode</span></span>

<span data-ttu-id="dd716-104">Das **ConversationNode** -Element gibt einen Knoten in einer Unterhaltung an.</span><span class="sxs-lookup"><span data-stu-id="dd716-104">The **ConversationNode** element specifies a node in a conversation.</span></span> 
  
```XML
<ConversationNode>
    <InternetMessageId></InternetMessageId>
    <ParentInternetMessageId></ParentInternetMessageId>
    <Items></Items>
</ConversationNode>
```

 <span data-ttu-id="dd716-105">**ConversationNodeType**</span><span class="sxs-lookup"><span data-stu-id="dd716-105">**ConversationNodeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="dd716-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="dd716-106">Attributes and elements</span></span>

<span data-ttu-id="dd716-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="dd716-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dd716-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="dd716-108">Attributes</span></span>

<span data-ttu-id="dd716-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="dd716-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dd716-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dd716-110">Child elements</span></span>

|<span data-ttu-id="dd716-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="dd716-111">**Element**</span></span>|<span data-ttu-id="dd716-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dd716-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dd716-113">InternetMessageId</span><span class="sxs-lookup"><span data-stu-id="dd716-113">InternetMessageId</span></span>](internetmessageid.md) <br/> |<span data-ttu-id="dd716-114">Stellt die Internet Nachrichten-ID eines Elements dar.</span><span class="sxs-lookup"><span data-stu-id="dd716-114">Represents the Internet message identifier of an item.</span></span>  <br/> |
|[<span data-ttu-id="dd716-115">ParentInternetMessageId</span><span class="sxs-lookup"><span data-stu-id="dd716-115">ParentInternetMessageId</span></span>](parentinternetmessageid.md) <br/> |<span data-ttu-id="dd716-116">Gibt den Bezeichner der übergeordneten Internet Nachricht an.</span><span class="sxs-lookup"><span data-stu-id="dd716-116">Specifies the identifier of the parent Internet message.</span></span>  <br/> |
|[<span data-ttu-id="dd716-117">Itemids (NonEmptyArrayOfItemIdsType)</span><span class="sxs-lookup"><span data-stu-id="dd716-117">ItemIds (NonEmptyArrayOfItemIdsType)</span></span>](itemids-nonemptyarrayofitemidstype.md) <br/> |<span data-ttu-id="dd716-118">Gibt alle Elemente im Unterhaltungs Knoten an.</span><span class="sxs-lookup"><span data-stu-id="dd716-118">Specifies all the items in the conversation node.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="dd716-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dd716-119">Parent elements</span></span>

|<span data-ttu-id="dd716-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="dd716-120">**Element**</span></span>|<span data-ttu-id="dd716-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dd716-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dd716-122">ConversationNodes</span><span class="sxs-lookup"><span data-stu-id="dd716-122">ConversationNodes</span></span>](conversationnodes.md) <br/> |<span data-ttu-id="dd716-123">Gibt eine Auflistung von Unterhaltungs Knoten an.</span><span class="sxs-lookup"><span data-stu-id="dd716-123">Specifies a collection of conversation nodes.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dd716-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dd716-124">Remarks</span></span>

<span data-ttu-id="dd716-125">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="dd716-125">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="dd716-126">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="dd716-126">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dd716-127">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="dd716-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dd716-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="dd716-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="dd716-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="dd716-129">Schema Name</span></span>  <br/> |<span data-ttu-id="dd716-130">Typschema</span><span class="sxs-lookup"><span data-stu-id="dd716-130">Type schema</span></span>  <br/> |
|<span data-ttu-id="dd716-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="dd716-131">Validation File</span></span>  <br/> |<span data-ttu-id="dd716-132">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="dd716-132">types.xsd</span></span>  <br/> |
|<span data-ttu-id="dd716-133">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="dd716-133">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="dd716-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dd716-134">See also</span></span>



- [<span data-ttu-id="dd716-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="dd716-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

