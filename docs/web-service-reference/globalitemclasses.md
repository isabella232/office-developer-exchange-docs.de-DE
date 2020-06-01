---
title: GlobalItemClasses
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GlobalItemClasses
api_type:
- schema
ms.assetid: 72634700-6d75-44c0-80b7-8c31743c04d6
description: Das GlobalItemClasses-Element enthält eine Liste von Elementklassen, die alle Elementklassen der Unterhaltungselemente in einem Postfach darstellt.
ms.openlocfilehash: e4cb8a8886f8262e8cb4a550b054e81ea18a5e11
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459433"
---
# <a name="globalitemclasses"></a><span data-ttu-id="af444-103">GlobalItemClasses</span><span class="sxs-lookup"><span data-stu-id="af444-103">GlobalItemClasses</span></span>

<span data-ttu-id="af444-104">Das **GlobalItemClasses** -Element enthält eine Liste von Elementklassen, die alle Elementklassen der Unterhaltungselemente in einem Postfach darstellt.</span><span class="sxs-lookup"><span data-stu-id="af444-104">The **GlobalItemClasses** element contains a list of item classes that represents all the item classes of the conversation items in a mailbox.</span></span> 
  
[<span data-ttu-id="af444-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="af444-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="af444-106">Conversations</span><span class="sxs-lookup"><span data-stu-id="af444-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="af444-107">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="af444-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="af444-108">GlobalItemClasses</span><span class="sxs-lookup"><span data-stu-id="af444-108">GlobalItemClasses</span></span>](globalitemclasses.md)
  
```XML
<GlobalItemClasses>
    <String/>
</GlobalItemClasses>
```

 <span data-ttu-id="af444-109">**ArrayOfItemClassType**</span><span class="sxs-lookup"><span data-stu-id="af444-109">**ArrayOfItemClassType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="af444-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="af444-110">Attributes and elements</span></span>

<span data-ttu-id="af444-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="af444-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="af444-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="af444-112">Attributes</span></span>

<span data-ttu-id="af444-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="af444-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="af444-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="af444-114">Child elements</span></span>

|<span data-ttu-id="af444-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="af444-115">**Element**</span></span>|<span data-ttu-id="af444-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="af444-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="af444-117">ItemClass</span><span class="sxs-lookup"><span data-stu-id="af444-117">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="af444-118">Stellt die Nachrichtenklasse eines Elements dar.</span><span class="sxs-lookup"><span data-stu-id="af444-118">Represents the message class of an item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="af444-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="af444-119">Parent elements</span></span>

|<span data-ttu-id="af444-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="af444-120">**Element**</span></span>|<span data-ttu-id="af444-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="af444-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="af444-122">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="af444-122">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="af444-123">Stellt eine einfache Unterhaltung dar.</span><span class="sxs-lookup"><span data-stu-id="af444-123">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="af444-124">Textwert</span><span class="sxs-lookup"><span data-stu-id="af444-124">Text value</span></span>

<span data-ttu-id="af444-125">Keine.</span><span class="sxs-lookup"><span data-stu-id="af444-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="af444-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="af444-126">Remarks</span></span>

<span data-ttu-id="af444-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="af444-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="af444-128">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="af444-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="af444-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="af444-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="af444-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="af444-130">Schema name</span></span>  <br/> |<span data-ttu-id="af444-131">Schematypen</span><span class="sxs-lookup"><span data-stu-id="af444-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="af444-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="af444-132">Validation file</span></span>  <br/> |<span data-ttu-id="af444-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="af444-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="af444-134">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="af444-134">Can be empty</span></span>  <br/> |<span data-ttu-id="af444-135">False</span><span class="sxs-lookup"><span data-stu-id="af444-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="af444-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="af444-136">See also</span></span>



[<span data-ttu-id="af444-137">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="af444-137">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="af444-138">ApplyConversationAction-Vorgang</span><span class="sxs-lookup"><span data-stu-id="af444-138">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="af444-139">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="af444-139">Conversations in EWS</span></span>](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

