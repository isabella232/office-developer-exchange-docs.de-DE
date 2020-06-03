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
ms.openlocfilehash: d7f6b0aa01aceb6a251fb0c46d89b34cad260acd
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530726"
---
# <a name="uniquerecipients"></a><span data-ttu-id="ebaf8-104">UniqueRecipients</span><span class="sxs-lookup"><span data-stu-id="ebaf8-104">UniqueRecipients</span></span>

<span data-ttu-id="ebaf8-p102">Das **UniqueRecipients** -Element enthält die Empfängerliste einer Unterhaltung in einem bestimmten Ordner. Dieses Element ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="ebaf8-p102">The **UniqueRecipients** element contains the recipient list of a conversation in a particular folder. This element is read-only.</span></span> 
  
[<span data-ttu-id="ebaf8-107">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="ebaf8-107">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="ebaf8-108">Conversations</span><span class="sxs-lookup"><span data-stu-id="ebaf8-108">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="ebaf8-109">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="ebaf8-109">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="ebaf8-110">UniqueRecipients</span><span class="sxs-lookup"><span data-stu-id="ebaf8-110">UniqueRecipients</span></span>](uniquerecipients.md)
  
```XML
<UniqueRecpients>
   <String/>
</UniqueRecpients>
```

 <span data-ttu-id="ebaf8-111">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="ebaf8-111">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ebaf8-112">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ebaf8-112">Attributes and elements</span></span>

<span data-ttu-id="ebaf8-113">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ebaf8-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ebaf8-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="ebaf8-114">Attributes</span></span>

<span data-ttu-id="ebaf8-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="ebaf8-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ebaf8-116">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ebaf8-116">Child elements</span></span>

|<span data-ttu-id="ebaf8-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="ebaf8-117">**Element**</span></span>|<span data-ttu-id="ebaf8-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ebaf8-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ebaf8-119">String</span><span class="sxs-lookup"><span data-stu-id="ebaf8-119">String</span></span>](string.md) <br/> |<span data-ttu-id="ebaf8-p103">Stellt einen eindeutigen Empfänger einer Unterhaltung. Dieses Element ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="ebaf8-p103">Represents a unique recipient of a conversation. This element is read-only.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ebaf8-122">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ebaf8-122">Parent elements</span></span>

|<span data-ttu-id="ebaf8-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="ebaf8-123">**Element**</span></span>|<span data-ttu-id="ebaf8-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ebaf8-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ebaf8-125">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="ebaf8-125">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="ebaf8-126">Stellt eine einfache Unterhaltung dar.</span><span class="sxs-lookup"><span data-stu-id="ebaf8-126">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ebaf8-127">Textwert</span><span class="sxs-lookup"><span data-stu-id="ebaf8-127">Text value</span></span>

<span data-ttu-id="ebaf8-128">Keine.</span><span class="sxs-lookup"><span data-stu-id="ebaf8-128">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ebaf8-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ebaf8-129">Remarks</span></span>

<span data-ttu-id="ebaf8-130">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="ebaf8-130">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ebaf8-131">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="ebaf8-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ebaf8-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="ebaf8-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ebaf8-133">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ebaf8-133">Schema name</span></span>  <br/> |<span data-ttu-id="ebaf8-134">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="ebaf8-134">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ebaf8-135">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ebaf8-135">Validation file</span></span>  <br/> |<span data-ttu-id="ebaf8-136">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="ebaf8-136">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ebaf8-137">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="ebaf8-137">Can be empty</span></span>  <br/> |<span data-ttu-id="ebaf8-138">False</span><span class="sxs-lookup"><span data-stu-id="ebaf8-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ebaf8-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ebaf8-139">See also</span></span>



[<span data-ttu-id="ebaf8-140">FindConversation-Vorgang</span><span class="sxs-lookup"><span data-stu-id="ebaf8-140">FindConversation operation</span></span>](findconversation-operation.md)


[<span data-ttu-id="ebaf8-141">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="ebaf8-141">Conversations in EWS</span></span>](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

