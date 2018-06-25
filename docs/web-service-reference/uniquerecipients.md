---
title: UniqueRecipients
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UniqueRecipients
api_type:
- schema
ms.assetid: 9f46ed05-5370-46ee-80f5-83f97224c76e
description: Das UniqueRecipients -Element enthält die Empfängerliste einer Unterhaltung in einem bestimmten Ordner. Dieses Element ist schreibgeschützt.
ms.openlocfilehash: 710559e599c6cec1db371165f01187f8960024f6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839318"
---
# <a name="uniquerecipients"></a><span data-ttu-id="15a27-104">UniqueRecipients</span><span class="sxs-lookup"><span data-stu-id="15a27-104">UniqueRecipients</span></span>

<span data-ttu-id="15a27-p102">Das **UniqueRecipients** -Element enthält die Empfängerliste einer Unterhaltung in einem bestimmten Ordner. Dieses Element ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="15a27-p102">The **UniqueRecipients** element contains the recipient list of a conversation in a particular folder. This element is read-only.</span></span> 
  
[<span data-ttu-id="15a27-107">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="15a27-107">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="15a27-108">Conversations</span><span class="sxs-lookup"><span data-stu-id="15a27-108">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="15a27-109">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="15a27-109">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="15a27-110">UniqueRecipients</span><span class="sxs-lookup"><span data-stu-id="15a27-110">UniqueRecipients</span></span>](uniquerecipients.md)
  
```XML
<UniqueRecpients>
   <String/>
</UniqueRecpients>
```

 <span data-ttu-id="15a27-111">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="15a27-111">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="15a27-112">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="15a27-112">Attributes and elements</span></span>

<span data-ttu-id="15a27-113">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="15a27-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="15a27-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="15a27-114">Attributes</span></span>

<span data-ttu-id="15a27-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="15a27-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="15a27-116">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="15a27-116">Child elements</span></span>

|<span data-ttu-id="15a27-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="15a27-117">**Element**</span></span>|<span data-ttu-id="15a27-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="15a27-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="15a27-119">String</span><span class="sxs-lookup"><span data-stu-id="15a27-119">String</span></span>](string.md) <br/> |<span data-ttu-id="15a27-p103">Stellt einen eindeutigen Empfänger einer Unterhaltung. Dieses Element ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="15a27-p103">Represents a unique recipient of a conversation. This element is read-only.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="15a27-122">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="15a27-122">Parent elements</span></span>

|<span data-ttu-id="15a27-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="15a27-123">**Element**</span></span>|<span data-ttu-id="15a27-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="15a27-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="15a27-125">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="15a27-125">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="15a27-126">Stellt eine einfache Unterhaltung dar.</span><span class="sxs-lookup"><span data-stu-id="15a27-126">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="15a27-127">Textwert</span><span class="sxs-lookup"><span data-stu-id="15a27-127">Text value</span></span>

<span data-ttu-id="15a27-128">Keine.</span><span class="sxs-lookup"><span data-stu-id="15a27-128">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="15a27-129">Hinweise</span><span class="sxs-lookup"><span data-stu-id="15a27-129">Remarks</span></span>

<span data-ttu-id="15a27-130">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="15a27-130">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="15a27-131">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="15a27-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="15a27-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="15a27-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="15a27-133">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="15a27-133">Schema name</span></span>  <br/> |<span data-ttu-id="15a27-134">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="15a27-134">Messages schema</span></span>  <br/> |
|<span data-ttu-id="15a27-135">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="15a27-135">Validation file</span></span>  <br/> |<span data-ttu-id="15a27-136">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="15a27-136">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="15a27-137">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="15a27-137">Can be empty</span></span>  <br/> |<span data-ttu-id="15a27-138">False</span><span class="sxs-lookup"><span data-stu-id="15a27-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="15a27-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="15a27-139">See also</span></span>



[<span data-ttu-id="15a27-140">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="15a27-140">FindConversation operation</span></span>](findconversation-operation.md)


[<span data-ttu-id="15a27-141">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="15a27-141">Conversations in EWS</span></span>](http://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

