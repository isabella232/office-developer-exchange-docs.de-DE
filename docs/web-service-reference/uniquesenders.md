---
title: UniqueSenders
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UniqueSenders
api_type:
- schema
ms.assetid: 1f55f2fe-b2f2-4169-83c1-fa5c752bd695
description: Das UniqueSenders-Element enthält eine Liste von allen Absendern von Unterhaltungselementen im aktuellen Ordner. Dieses Element ist schreibgeschützt.
ms.openlocfilehash: b75846534141e23e6d8158bc36f0ef60bcb1d7ad
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839313"
---
# <a name="uniquesenders"></a><span data-ttu-id="8d721-104">UniqueSenders</span><span class="sxs-lookup"><span data-stu-id="8d721-104">UniqueSenders</span></span>

<span data-ttu-id="8d721-105">Das **UniqueSenders** -Element enthält eine Liste von allen Absendern von Unterhaltungselementen im aktuellen Ordner.</span><span class="sxs-lookup"><span data-stu-id="8d721-105">The **UniqueSenders** element contains a list of all the senders of conversation items in the current folder.</span></span> <span data-ttu-id="8d721-106">Dieses Element ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="8d721-106">This element is read-only.</span></span> 
  
[<span data-ttu-id="8d721-107">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="8d721-107">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="8d721-108">Conversations</span><span class="sxs-lookup"><span data-stu-id="8d721-108">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="8d721-109">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="8d721-109">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="8d721-110">UniqueSenders</span><span class="sxs-lookup"><span data-stu-id="8d721-110">UniqueSenders</span></span>](uniquesenders.md)
  
```XML
<UniqueSenders>
   <String/>
</UniqueSenders>
```

 <span data-ttu-id="8d721-111">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="8d721-111">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8d721-112">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="8d721-112">Attributes and elements</span></span>

<span data-ttu-id="8d721-113">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="8d721-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8d721-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="8d721-114">Attributes</span></span>

<span data-ttu-id="8d721-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="8d721-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8d721-116">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8d721-116">Child elements</span></span>

|<span data-ttu-id="8d721-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="8d721-117">**Element**</span></span>|<span data-ttu-id="8d721-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8d721-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8d721-119">String</span><span class="sxs-lookup"><span data-stu-id="8d721-119">String</span></span>](string.md) <br/> |<span data-ttu-id="8d721-120">Enthält einen einzelnen Gespräch Absender.</span><span class="sxs-lookup"><span data-stu-id="8d721-120">Contains a single conversation sender.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8d721-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8d721-121">Parent elements</span></span>

|<span data-ttu-id="8d721-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="8d721-122">**Element**</span></span>|<span data-ttu-id="8d721-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8d721-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8d721-124">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="8d721-124">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="8d721-125">Stellt eine einfache Unterhaltung dar.</span><span class="sxs-lookup"><span data-stu-id="8d721-125">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="8d721-126">Textwert</span><span class="sxs-lookup"><span data-stu-id="8d721-126">Text value</span></span>

<span data-ttu-id="8d721-127">Keine.</span><span class="sxs-lookup"><span data-stu-id="8d721-127">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8d721-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8d721-128">Remarks</span></span>

<span data-ttu-id="8d721-129">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="8d721-129">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8d721-130">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="8d721-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8d721-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="8d721-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8d721-132">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="8d721-132">Schema name</span></span>  <br/> |<span data-ttu-id="8d721-133">Schematypen</span><span class="sxs-lookup"><span data-stu-id="8d721-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="8d721-134">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="8d721-134">Validation file</span></span>  <br/> |<span data-ttu-id="8d721-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="8d721-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8d721-136">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="8d721-136">Can be empty</span></span>  <br/> |<span data-ttu-id="8d721-137">False</span><span class="sxs-lookup"><span data-stu-id="8d721-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8d721-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8d721-138">See also</span></span>



[<span data-ttu-id="8d721-139">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="8d721-139">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="8d721-140">ApplyConversationAction-Vorgang</span><span class="sxs-lookup"><span data-stu-id="8d721-140">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="8d721-141">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="8d721-141">Conversations in EWS</span></span>](http://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

