---
title: Globals
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GlobalSize
api_type:
- schema
ms.assetid: 23c24437-8dab-4c86-888d-471d23af675a
description: Das Globals-Element enthält die Größe der Unterhaltung, die von der Größe aller Unterhaltungselemente im Postfach berechnet wird.
ms.openlocfilehash: d23ab080dadb006cd5eff9d712d081fe7d94a2a8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462451"
---
# <a name="globalsize"></a><span data-ttu-id="48b82-103">Globals</span><span class="sxs-lookup"><span data-stu-id="48b82-103">GlobalSize</span></span>

<span data-ttu-id="48b82-104">Das **Globals** -Element enthält die Größe der Unterhaltung, die von der Größe aller Unterhaltungselemente im Postfach berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="48b82-104">The **GlobalSize** element contains the size of the conversation calculated from the size of all conversation items in the mailbox.</span></span> 
  
[<span data-ttu-id="48b82-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="48b82-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="48b82-106">Conversations</span><span class="sxs-lookup"><span data-stu-id="48b82-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="48b82-107">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="48b82-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="48b82-108">Globals</span><span class="sxs-lookup"><span data-stu-id="48b82-108">GlobalSize</span></span>](globalsize.md)
  
```XML
<GlobalSize/>
```

 <span data-ttu-id="48b82-109">**xs: int**</span><span class="sxs-lookup"><span data-stu-id="48b82-109">**xs:int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="48b82-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="48b82-110">Attributes and elements</span></span>

<span data-ttu-id="48b82-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="48b82-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="48b82-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="48b82-112">Attributes</span></span>

<span data-ttu-id="48b82-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="48b82-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="48b82-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="48b82-114">Child elements</span></span>

<span data-ttu-id="48b82-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="48b82-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="48b82-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="48b82-116">Parent elements</span></span>

|<span data-ttu-id="48b82-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="48b82-117">**Element**</span></span>|<span data-ttu-id="48b82-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="48b82-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="48b82-119">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="48b82-119">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="48b82-120">Stellt eine einfache Unterhaltung dar.</span><span class="sxs-lookup"><span data-stu-id="48b82-120">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="48b82-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="48b82-121">Text value</span></span>

<span data-ttu-id="48b82-122">Der Textwert des **Globals** -Elements ist die Größe der Unterhaltung, die von der Größe aller Unterhaltungselemente im Postfach berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="48b82-122">The text value of the **GlobalSize** element is the size of the conversation calculated from the size of all conversation items in the mailbox.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="48b82-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="48b82-123">Remarks</span></span>

<span data-ttu-id="48b82-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="48b82-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="48b82-125">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="48b82-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="48b82-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="48b82-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="48b82-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="48b82-127">Schema name</span></span>  <br/> |<span data-ttu-id="48b82-128">Schematypen</span><span class="sxs-lookup"><span data-stu-id="48b82-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="48b82-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="48b82-129">Validation file</span></span>  <br/> |<span data-ttu-id="48b82-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="48b82-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="48b82-131">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="48b82-131">Can be empty</span></span>  <br/> |<span data-ttu-id="48b82-132">False</span><span class="sxs-lookup"><span data-stu-id="48b82-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="48b82-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="48b82-133">See also</span></span>



[<span data-ttu-id="48b82-134">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="48b82-134">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="48b82-135">ApplyConversationAction-Vorgang</span><span class="sxs-lookup"><span data-stu-id="48b82-135">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="48b82-136">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="48b82-136">Conversations in EWS</span></span>](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

