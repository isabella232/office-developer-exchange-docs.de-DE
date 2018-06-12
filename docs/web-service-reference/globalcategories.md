---
title: GlobalCategories
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GlobalCategories
api_type:
- schema
ms.assetid: 7a1d3f04-4ada-4a31-845e-f1f1ff6e136f
description: Das GlobalCategories-Element enthält die Kategorieliste für alle Unterhaltungselemente in einem Postfach.
ms.openlocfilehash: 5cedea821b14264f15026c2d297c3017534ca354
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19829711"
---
# <a name="globalcategories"></a><span data-ttu-id="b8d50-103">GlobalCategories</span><span class="sxs-lookup"><span data-stu-id="b8d50-103">GlobalCategories</span></span>

<span data-ttu-id="b8d50-104">Das **GlobalCategories** -Element enthält die Kategorieliste für alle Unterhaltungselemente in einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="b8d50-104">The **GlobalCategories** element contains the category list for all conversation items in a mailbox.</span></span> 
  
[<span data-ttu-id="b8d50-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="b8d50-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="b8d50-106">Conversations</span><span class="sxs-lookup"><span data-stu-id="b8d50-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="b8d50-107">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="b8d50-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="b8d50-108">GlobalCategories</span><span class="sxs-lookup"><span data-stu-id="b8d50-108">GlobalCategories</span></span>](globalcategories.md)
  
```XML
<GlobalCategories>
   <String/>
</GlobalCategories>
```

 <span data-ttu-id="b8d50-109">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="b8d50-109">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b8d50-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b8d50-110">Attributes and elements</span></span>

<span data-ttu-id="b8d50-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b8d50-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b8d50-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="b8d50-112">Attributes</span></span>

<span data-ttu-id="b8d50-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="b8d50-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b8d50-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b8d50-114">Child elements</span></span>

|<span data-ttu-id="b8d50-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="b8d50-115">**Element**</span></span>|<span data-ttu-id="b8d50-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b8d50-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b8d50-117">String</span><span class="sxs-lookup"><span data-stu-id="b8d50-117">String</span></span>](string.md) <br/> |<span data-ttu-id="b8d50-118">Enthält eine einzelne Kategorie.</span><span class="sxs-lookup"><span data-stu-id="b8d50-118">Contains a single category.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b8d50-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b8d50-119">Parent elements</span></span>

|<span data-ttu-id="b8d50-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="b8d50-120">**Element**</span></span>|<span data-ttu-id="b8d50-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b8d50-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b8d50-122">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="b8d50-122">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="b8d50-123">Stellt eine einfache Unterhaltung dar.</span><span class="sxs-lookup"><span data-stu-id="b8d50-123">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b8d50-124">Textwert</span><span class="sxs-lookup"><span data-stu-id="b8d50-124">Text value</span></span>

<span data-ttu-id="b8d50-125">Keine.</span><span class="sxs-lookup"><span data-stu-id="b8d50-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b8d50-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b8d50-126">Remarks</span></span>

<span data-ttu-id="b8d50-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b8d50-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b8d50-128">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="b8d50-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b8d50-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="b8d50-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b8d50-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b8d50-130">Schema name</span></span>  <br/> |<span data-ttu-id="b8d50-131">Schematypen</span><span class="sxs-lookup"><span data-stu-id="b8d50-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="b8d50-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b8d50-132">Validation file</span></span>  <br/> |<span data-ttu-id="b8d50-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b8d50-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b8d50-134">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="b8d50-134">Can be empty</span></span>  <br/> |<span data-ttu-id="b8d50-135">False</span><span class="sxs-lookup"><span data-stu-id="b8d50-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b8d50-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b8d50-136">See also</span></span>



[<span data-ttu-id="b8d50-137">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="b8d50-137">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="b8d50-138">ApplyConversationAction-Vorgang</span><span class="sxs-lookup"><span data-stu-id="b8d50-138">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="b8d50-139">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="b8d50-139">Conversations in EWS</span></span>](http://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)
