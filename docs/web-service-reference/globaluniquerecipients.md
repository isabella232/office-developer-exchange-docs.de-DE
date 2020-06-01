---
title: GlobalUniqueRecipients
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GlobalUniqueRecipients
api_type:
- schema
ms.assetid: 67379c1c-85d9-4b11-8f17-ad9d24904788
description: Das GlobalUniqueRecipients -Element enthält die Empfängerliste einer Unterhaltung über ein Postfach aggregiert.
ms.openlocfilehash: 3481c43b99f75a05a8e7fbe5a288e04708290d83
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456038"
---
# <a name="globaluniquerecipients"></a><span data-ttu-id="afd7f-103">GlobalUniqueRecipients</span><span class="sxs-lookup"><span data-stu-id="afd7f-103">GlobalUniqueRecipients</span></span>

<span data-ttu-id="afd7f-104">Das **GlobalUniqueRecipients** -Element enthält die Empfängerliste einer Unterhaltung über ein Postfach aggregiert.</span><span class="sxs-lookup"><span data-stu-id="afd7f-104">The **GlobalUniqueRecipients** element contains the recipient list of a conversation aggregated across a mailbox.</span></span> 
  
[<span data-ttu-id="afd7f-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="afd7f-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="afd7f-106">Conversations</span><span class="sxs-lookup"><span data-stu-id="afd7f-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="afd7f-107">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="afd7f-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="afd7f-108">GlobalUniqueRecipients</span><span class="sxs-lookup"><span data-stu-id="afd7f-108">GlobalUniqueRecipients</span></span>](globaluniquerecipients.md)
  
```XML
<GlobalUniqueRecipients>
   <String/>
</GlobalUniqueRecipients>
```

 <span data-ttu-id="afd7f-109">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="afd7f-109">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="afd7f-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="afd7f-110">Attributes and elements</span></span>

<span data-ttu-id="afd7f-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="afd7f-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="afd7f-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="afd7f-112">Attributes</span></span>

<span data-ttu-id="afd7f-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="afd7f-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="afd7f-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="afd7f-114">Child elements</span></span>

|<span data-ttu-id="afd7f-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="afd7f-115">**Element**</span></span>|<span data-ttu-id="afd7f-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="afd7f-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="afd7f-117">String</span><span class="sxs-lookup"><span data-stu-id="afd7f-117">String</span></span>](string.md) <br/> |<span data-ttu-id="afd7f-118">Einen einzelnen Gespräch Empfänger enthält.</span><span class="sxs-lookup"><span data-stu-id="afd7f-118">Contains a single conversation recipient.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="afd7f-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="afd7f-119">Parent elements</span></span>

|<span data-ttu-id="afd7f-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="afd7f-120">**Element**</span></span>|<span data-ttu-id="afd7f-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="afd7f-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="afd7f-122">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="afd7f-122">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="afd7f-123">Stellt eine einfache Unterhaltung dar.</span><span class="sxs-lookup"><span data-stu-id="afd7f-123">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="afd7f-124">Textwert</span><span class="sxs-lookup"><span data-stu-id="afd7f-124">Text value</span></span>

<span data-ttu-id="afd7f-125">Keine.</span><span class="sxs-lookup"><span data-stu-id="afd7f-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="afd7f-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="afd7f-126">Remarks</span></span>

<span data-ttu-id="afd7f-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="afd7f-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="afd7f-128">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="afd7f-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="afd7f-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="afd7f-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="afd7f-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="afd7f-130">Schema name</span></span>  <br/> |<span data-ttu-id="afd7f-131">Schematypen</span><span class="sxs-lookup"><span data-stu-id="afd7f-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="afd7f-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="afd7f-132">Validation file</span></span>  <br/> |<span data-ttu-id="afd7f-133">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="afd7f-133">types.xsd</span></span>  <br/> |
|<span data-ttu-id="afd7f-134">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="afd7f-134">Can be empty</span></span>  <br/> |<span data-ttu-id="afd7f-135">False</span><span class="sxs-lookup"><span data-stu-id="afd7f-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="afd7f-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="afd7f-136">See also</span></span>



[<span data-ttu-id="afd7f-137">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="afd7f-137">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="afd7f-138">ApplyConversationAction-Vorgang</span><span class="sxs-lookup"><span data-stu-id="afd7f-138">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="afd7f-139">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="afd7f-139">Conversations in EWS</span></span>](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

