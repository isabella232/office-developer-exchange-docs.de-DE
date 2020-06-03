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
description: Das ConversationActions-Element enthält eine Sammlung von Unterhaltungen und die Aktionen, die auf diese angewendet werden sollen.
ms.openlocfilehash: 2db84f78b4b8c92e0a6ef7d69fba7c778fb5f96d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527103"
---
# <a name="conversationactions"></a><span data-ttu-id="93fa8-103">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="93fa8-103">ConversationActions</span></span>

<span data-ttu-id="93fa8-104">Das **ConversationActions** -Element enthält eine Sammlung von Unterhaltungen und die Aktionen, die auf diese angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="93fa8-104">The **ConversationActions** element contains a collection of conversations and the actions to apply to them.</span></span> 
  
[<span data-ttu-id="93fa8-105">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="93fa8-105">ApplyConversationAction</span></span>](applyconversationaction.md)
  
[<span data-ttu-id="93fa8-106">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="93fa8-106">ConversationActions</span></span>](conversationactions.md)
  
```XML
<ConversationActions>
   <ConversationAction/>
</ConversationActions>
```

 <span data-ttu-id="93fa8-107">**NonEmptyArrayOfApplyConversationActionType**</span><span class="sxs-lookup"><span data-stu-id="93fa8-107">**NonEmptyArrayOfApplyConversationActionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="93fa8-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="93fa8-108">Attributes and elements</span></span>

<span data-ttu-id="93fa8-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="93fa8-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="93fa8-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="93fa8-110">Attributes</span></span>

<span data-ttu-id="93fa8-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="93fa8-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="93fa8-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="93fa8-112">Child elements</span></span>

|<span data-ttu-id="93fa8-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="93fa8-113">**Element**</span></span>|<span data-ttu-id="93fa8-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="93fa8-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="93fa8-115">Unterhaltung</span><span class="sxs-lookup"><span data-stu-id="93fa8-115">ConversationAction</span></span>](conversationaction.md) <br/> |<span data-ttu-id="93fa8-116">Enthält eine einzelne Aktion, die auf eine einzelne Unterhaltung angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="93fa8-116">Contains a single action to be applied to a single conversation.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="93fa8-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="93fa8-117">Parent elements</span></span>

|<span data-ttu-id="93fa8-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="93fa8-118">**Element**</span></span>|<span data-ttu-id="93fa8-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="93fa8-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="93fa8-120">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="93fa8-120">ApplyConversationAction</span></span>](applyconversationaction.md) <br/> |<span data-ttu-id="93fa8-121">Definiert eine Anforderung zum Anwenden von Aktionen auf Elemente in einer Unterhaltung.</span><span class="sxs-lookup"><span data-stu-id="93fa8-121">Defines a request to apply actions to items in a conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="93fa8-122">Textwert</span><span class="sxs-lookup"><span data-stu-id="93fa8-122">Text value</span></span>

<span data-ttu-id="93fa8-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="93fa8-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="93fa8-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="93fa8-124">Remarks</span></span>

<span data-ttu-id="93fa8-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="93fa8-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="93fa8-126">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="93fa8-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="93fa8-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="93fa8-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="93fa8-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="93fa8-128">Schema Name</span></span>  <br/> |<span data-ttu-id="93fa8-129">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="93fa8-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="93fa8-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="93fa8-130">Validation File</span></span>  <br/> |<span data-ttu-id="93fa8-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="93fa8-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="93fa8-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="93fa8-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="93fa8-133">False</span><span class="sxs-lookup"><span data-stu-id="93fa8-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="93fa8-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="93fa8-134">See also</span></span>



[<span data-ttu-id="93fa8-135">ApplyConversationAction-Vorgang</span><span class="sxs-lookup"><span data-stu-id="93fa8-135">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)

