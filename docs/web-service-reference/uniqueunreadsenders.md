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
description: Das UniqueUnreadSenders-Element enthält eine Liste aller Personen, die Nachrichten gesendet haben, die derzeit in dieser Unterhaltung in dem aktuellen Ordner nicht gelesen wurden. Dieses Element ist schreibgeschützt.
ms.openlocfilehash: 0e45362e88be4930b8bc2f641c1fb00cc63c0605
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458852"
---
# <a name="uniqueunreadsenders"></a><span data-ttu-id="cdcc8-104">UniqueUnreadSenders</span><span class="sxs-lookup"><span data-stu-id="cdcc8-104">UniqueUnreadSenders</span></span>

<span data-ttu-id="cdcc8-105">Das **UniqueUnreadSenders** -Element enthält eine Liste aller Personen, die Nachrichten gesendet haben, die derzeit in dieser Unterhaltung in dem aktuellen Ordner nicht gelesen wurden.</span><span class="sxs-lookup"><span data-stu-id="cdcc8-105">The **UniqueUnreadSenders** element contains a list of all the people who have sent messages that are currently unread in this conversation in the current folder.</span></span> <span data-ttu-id="cdcc8-106">Dieses Element ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="cdcc8-106">This element is read-only.</span></span> 
  
[<span data-ttu-id="cdcc8-107">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="cdcc8-107">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="cdcc8-108">Conversations</span><span class="sxs-lookup"><span data-stu-id="cdcc8-108">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="cdcc8-109">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="cdcc8-109">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="cdcc8-110">UniqueUnreadSenders</span><span class="sxs-lookup"><span data-stu-id="cdcc8-110">UniqueUnreadSenders</span></span>](uniqueunreadsenders.md)
  
```XML
<UniqueUnreadSenders>
   <String/>
</UniqueUnreadSenders>
```

 <span data-ttu-id="cdcc8-111">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="cdcc8-111">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cdcc8-112">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="cdcc8-112">Attributes and elements</span></span>

<span data-ttu-id="cdcc8-113">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="cdcc8-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cdcc8-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="cdcc8-114">Attributes</span></span>

<span data-ttu-id="cdcc8-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="cdcc8-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cdcc8-116">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cdcc8-116">Child elements</span></span>

|<span data-ttu-id="cdcc8-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="cdcc8-117">**Element**</span></span>|<span data-ttu-id="cdcc8-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cdcc8-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cdcc8-119">String</span><span class="sxs-lookup"><span data-stu-id="cdcc8-119">String</span></span>](string.md) <br/> |<span data-ttu-id="cdcc8-120">Enthält einen einzelnen Unterhaltungs Absender.</span><span class="sxs-lookup"><span data-stu-id="cdcc8-120">Contains a single conversation sender.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="cdcc8-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cdcc8-121">Parent elements</span></span>

|<span data-ttu-id="cdcc8-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="cdcc8-122">**Element**</span></span>|<span data-ttu-id="cdcc8-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cdcc8-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cdcc8-124">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="cdcc8-124">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="cdcc8-125">Stellt eine einfache Unterhaltung dar.</span><span class="sxs-lookup"><span data-stu-id="cdcc8-125">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="cdcc8-126">Textwert</span><span class="sxs-lookup"><span data-stu-id="cdcc8-126">Text value</span></span>

<span data-ttu-id="cdcc8-127">Keine.</span><span class="sxs-lookup"><span data-stu-id="cdcc8-127">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cdcc8-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cdcc8-128">Remarks</span></span>

<span data-ttu-id="cdcc8-129">Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt. Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, in dem Exchange Webdienste gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="cdcc8-129">This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cdcc8-130">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="cdcc8-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cdcc8-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="cdcc8-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="cdcc8-132">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="cdcc8-132">Schema name</span></span>  <br/> |<span data-ttu-id="cdcc8-133">Schematypen</span><span class="sxs-lookup"><span data-stu-id="cdcc8-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="cdcc8-134">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="cdcc8-134">Validation file</span></span>  <br/> |<span data-ttu-id="cdcc8-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="cdcc8-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="cdcc8-136">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="cdcc8-136">Can be empty</span></span>  <br/> |<span data-ttu-id="cdcc8-137">False</span><span class="sxs-lookup"><span data-stu-id="cdcc8-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cdcc8-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cdcc8-138">See also</span></span>



[<span data-ttu-id="cdcc8-139">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="cdcc8-139">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="cdcc8-140">ApplyConversationAction-Vorgang</span><span class="sxs-lookup"><span data-stu-id="cdcc8-140">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="cdcc8-141">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="cdcc8-141">Conversations in EWS</span></span>](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

