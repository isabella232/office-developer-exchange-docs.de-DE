---
title: UniqueUnreadSenders
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UniqueUnreadSenders
api_type:
- schema
ms.assetid: eb7d1274-ce2e-4ef8-b47f-e911174aab0c
description: Das UniqueUnreadSenders-Element enthält eine Liste der Personen, die Nachrichten gesendet wurden, die derzeit in dieser Unterhaltung im aktuellen Ordner ungelesen sind. Dieses Element ist schreibgeschützt.
ms.openlocfilehash: d1f5593f6b86745aa27d86e9d25487f5855cb0cc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839311"
---
# <a name="uniqueunreadsenders"></a><span data-ttu-id="c761c-104">UniqueUnreadSenders</span><span class="sxs-lookup"><span data-stu-id="c761c-104">UniqueUnreadSenders</span></span>

<span data-ttu-id="c761c-105">Das **UniqueUnreadSenders** -Element enthält eine Liste der Personen, die Nachrichten gesendet wurden, die derzeit in dieser Unterhaltung im aktuellen Ordner ungelesen sind.</span><span class="sxs-lookup"><span data-stu-id="c761c-105">The **UniqueUnreadSenders** element contains a list of all the people who have sent messages that are currently unread in this conversation in the current folder.</span></span> <span data-ttu-id="c761c-106">Dieses Element ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="c761c-106">This element is read-only.</span></span> 
  
[<span data-ttu-id="c761c-107">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="c761c-107">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="c761c-108">Conversations</span><span class="sxs-lookup"><span data-stu-id="c761c-108">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="c761c-109">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="c761c-109">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="c761c-110">UniqueUnreadSenders</span><span class="sxs-lookup"><span data-stu-id="c761c-110">UniqueUnreadSenders</span></span>](uniqueunreadsenders.md)
  
```XML
<UniqueUnreadSenders>
   <String/>
</UniqueUnreadSenders>
```

 <span data-ttu-id="c761c-111">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="c761c-111">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c761c-112">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c761c-112">Attributes and elements</span></span>

<span data-ttu-id="c761c-113">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c761c-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c761c-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="c761c-114">Attributes</span></span>

<span data-ttu-id="c761c-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="c761c-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c761c-116">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c761c-116">Child elements</span></span>

|<span data-ttu-id="c761c-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="c761c-117">**Element**</span></span>|<span data-ttu-id="c761c-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c761c-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c761c-119">String</span><span class="sxs-lookup"><span data-stu-id="c761c-119">String</span></span>](string.md) <br/> |<span data-ttu-id="c761c-120">Enthält einen einzelnen Gespräch Absender.</span><span class="sxs-lookup"><span data-stu-id="c761c-120">Contains a single conversation sender.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c761c-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c761c-121">Parent elements</span></span>

|<span data-ttu-id="c761c-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="c761c-122">**Element**</span></span>|<span data-ttu-id="c761c-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c761c-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c761c-124">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="c761c-124">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="c761c-125">Stellt eine einfache Unterhaltung dar.</span><span class="sxs-lookup"><span data-stu-id="c761c-125">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c761c-126">Textwert</span><span class="sxs-lookup"><span data-stu-id="c761c-126">Text value</span></span>

<span data-ttu-id="c761c-127">Keine.</span><span class="sxs-lookup"><span data-stu-id="c761c-127">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c761c-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c761c-128">Remarks</span></span>

<span data-ttu-id="c761c-129">Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt. Das Schema, das dieses Element beschreibt befindet sich in dem virtuellen IIS-Verzeichnis, die Exchange-Webdienste gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="c761c-129">This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c761c-130">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="c761c-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c761c-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="c761c-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c761c-132">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c761c-132">Schema name</span></span>  <br/> |<span data-ttu-id="c761c-133">Schematypen</span><span class="sxs-lookup"><span data-stu-id="c761c-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="c761c-134">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c761c-134">Validation file</span></span>  <br/> |<span data-ttu-id="c761c-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c761c-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c761c-136">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="c761c-136">Can be empty</span></span>  <br/> |<span data-ttu-id="c761c-137">False</span><span class="sxs-lookup"><span data-stu-id="c761c-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c761c-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c761c-138">See also</span></span>



[<span data-ttu-id="c761c-139">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="c761c-139">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="c761c-140">ApplyConversationAction-Vorgang</span><span class="sxs-lookup"><span data-stu-id="c761c-140">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="c761c-141">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="c761c-141">Conversations in EWS</span></span>](http://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

