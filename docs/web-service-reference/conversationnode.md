---
title: ConversationNode
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b7f7acd3-ed65-441e-9976-8b4ed5f12c0b
description: Das ConversationNode-Element gibt einen Knoten in einer Unterhaltung.
ms.openlocfilehash: c8289e5f30bfd25eb12d54e3be0c561786308dc6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757705"
---
# <a name="conversationnode"></a><span data-ttu-id="19efd-103">ConversationNode</span><span class="sxs-lookup"><span data-stu-id="19efd-103">ConversationNode</span></span>

<span data-ttu-id="19efd-104">Das **ConversationNode** -Element gibt einen Knoten in einer Unterhaltung.</span><span class="sxs-lookup"><span data-stu-id="19efd-104">The **ConversationNode** element specifies a node in a conversation.</span></span> 
  
```XML
<ConversationNode>
    <InternetMessageId></InternetMessageId>
    <ParentInternetMessageId></ParentInternetMessageId>
    <Items></Items>
</ConversationNode>
```

 <span data-ttu-id="19efd-105">**ConversationNodeType**</span><span class="sxs-lookup"><span data-stu-id="19efd-105">**ConversationNodeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="19efd-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="19efd-106">Attributes and elements</span></span>

<span data-ttu-id="19efd-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="19efd-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="19efd-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="19efd-108">Attributes</span></span>

<span data-ttu-id="19efd-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="19efd-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="19efd-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="19efd-110">Child elements</span></span>

|<span data-ttu-id="19efd-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="19efd-111">**Element**</span></span>|<span data-ttu-id="19efd-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="19efd-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="19efd-113">InternetMessageId</span><span class="sxs-lookup"><span data-stu-id="19efd-113">InternetMessageId</span></span>](internetmessageid.md) <br/> |<span data-ttu-id="19efd-114">Die Internetnachricht-ID eines Elements darstellt.</span><span class="sxs-lookup"><span data-stu-id="19efd-114">Represents the Internet message identifier of an item.</span></span>  <br/> |
|[<span data-ttu-id="19efd-115">ParentInternetMessageId</span><span class="sxs-lookup"><span data-stu-id="19efd-115">ParentInternetMessageId</span></span>](parentinternetmessageid.md) <br/> |<span data-ttu-id="19efd-116">Gibt den Bezeichner der übergeordneten Internet-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="19efd-116">Specifies the identifier of the parent Internet message.</span></span>  <br/> |
|[<span data-ttu-id="19efd-117">Artikelnummern ein (NonEmptyArrayOfItemIdsType).</span><span class="sxs-lookup"><span data-stu-id="19efd-117">ItemIds (NonEmptyArrayOfItemIdsType)</span></span>](itemids-nonemptyarrayofitemidstype.md) <br/> |<span data-ttu-id="19efd-118">Gibt alle Elemente im unterhaltungsknoten an.</span><span class="sxs-lookup"><span data-stu-id="19efd-118">Specifies all the items in the conversation node.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="19efd-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="19efd-119">Parent elements</span></span>

|<span data-ttu-id="19efd-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="19efd-120">**Element**</span></span>|<span data-ttu-id="19efd-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="19efd-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="19efd-122">ConversationNodes</span><span class="sxs-lookup"><span data-stu-id="19efd-122">ConversationNodes</span></span>](conversationnodes.md) <br/> |<span data-ttu-id="19efd-123">Gibt eine Auflistung von Knoten Unterhaltung an.</span><span class="sxs-lookup"><span data-stu-id="19efd-123">Specifies a collection of conversation nodes.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="19efd-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="19efd-124">Remarks</span></span>

<span data-ttu-id="19efd-125">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="19efd-125">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="19efd-126">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="19efd-126">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="19efd-127">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="19efd-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="19efd-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="19efd-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="19efd-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="19efd-129">Schema Name</span></span>  <br/> |<span data-ttu-id="19efd-130">Typschema</span><span class="sxs-lookup"><span data-stu-id="19efd-130">Type schema</span></span>  <br/> |
|<span data-ttu-id="19efd-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="19efd-131">Validation File</span></span>  <br/> |<span data-ttu-id="19efd-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="19efd-132">types.xsd</span></span>  <br/> |
|<span data-ttu-id="19efd-133">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="19efd-133">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="19efd-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="19efd-134">See also</span></span>



- [<span data-ttu-id="19efd-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="19efd-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

