---
title: ConversationActions
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConversationActions
api_type:
- schema
ms.assetid: 3d6c663d-4bd9-4eec-b95a-cd683f592672
description: Das ConversationActions-Element enthält eine Auflistung von Unterhaltungen und die Aktionen darauf anwenden.
ms.openlocfilehash: 3dff7ff66f758f1cd2eb3cd7b8126294d2799fc0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757699"
---
# <a name="conversationactions"></a><span data-ttu-id="509ba-103">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="509ba-103">ConversationActions</span></span>

<span data-ttu-id="509ba-104">Das **ConversationActions** -Element enthält eine Auflistung von Unterhaltungen und die Aktionen darauf anwenden.</span><span class="sxs-lookup"><span data-stu-id="509ba-104">The **ConversationActions** element contains a collection of conversations and the actions to apply to them.</span></span> 
  
[<span data-ttu-id="509ba-105">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="509ba-105">ApplyConversationAction</span></span>](applyconversationaction.md)
  
[<span data-ttu-id="509ba-106">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="509ba-106">ConversationActions</span></span>](conversationactions.md)
  
```XML
<ConversationActions>
   <ConversationAction/>
</ConversationActions>
```

 <span data-ttu-id="509ba-107">**NonEmptyArrayOfApplyConversationActionType**</span><span class="sxs-lookup"><span data-stu-id="509ba-107">**NonEmptyArrayOfApplyConversationActionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="509ba-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="509ba-108">Attributes and elements</span></span>

<span data-ttu-id="509ba-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="509ba-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="509ba-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="509ba-110">Attributes</span></span>

<span data-ttu-id="509ba-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="509ba-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="509ba-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="509ba-112">Child elements</span></span>

|<span data-ttu-id="509ba-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="509ba-113">**Element**</span></span>|<span data-ttu-id="509ba-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="509ba-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="509ba-115">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="509ba-115">ConversationAction</span></span>](conversationaction.md) <br/> |<span data-ttu-id="509ba-116">Enthält eine einzelne Aktion auf einem einzelnen Gespräch angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="509ba-116">Contains a single action to be applied to a single conversation.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="509ba-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="509ba-117">Parent elements</span></span>

|<span data-ttu-id="509ba-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="509ba-118">**Element**</span></span>|<span data-ttu-id="509ba-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="509ba-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="509ba-120">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="509ba-120">ApplyConversationAction</span></span>](applyconversationaction.md) <br/> |<span data-ttu-id="509ba-121">Definiert eine Anforderung an die Aktionen auf Elemente in einer Unterhaltung anwenden.</span><span class="sxs-lookup"><span data-stu-id="509ba-121">Defines a request to apply actions to items in a conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="509ba-122">Textwert</span><span class="sxs-lookup"><span data-stu-id="509ba-122">Text value</span></span>

<span data-ttu-id="509ba-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="509ba-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="509ba-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="509ba-124">Remarks</span></span>

<span data-ttu-id="509ba-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="509ba-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="509ba-126">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="509ba-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="509ba-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="509ba-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="509ba-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="509ba-128">Schema Name</span></span>  <br/> |<span data-ttu-id="509ba-129">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="509ba-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="509ba-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="509ba-130">Validation File</span></span>  <br/> |<span data-ttu-id="509ba-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="509ba-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="509ba-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="509ba-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="509ba-133">False</span><span class="sxs-lookup"><span data-stu-id="509ba-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="509ba-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="509ba-134">See also</span></span>



[<span data-ttu-id="509ba-135">ApplyConversationAction-Vorgang</span><span class="sxs-lookup"><span data-stu-id="509ba-135">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)

