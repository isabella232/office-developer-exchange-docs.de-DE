---
title: GlobalUniqueSenders
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GlobalUniqueSenders
api_type:
- schema
ms.assetid: 6bd9e9cb-19c8-45af-b211-dfb8a6003b1b
description: Das GlobalUniqueSender-Element enthält eine Liste von allen Absendern der Unterhaltungselemente im Postfach.
ms.openlocfilehash: 72dec056880c41ac9e79235dddb3c82102580a31
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19829751"
---
# <a name="globaluniquesenders"></a><span data-ttu-id="21676-103">GlobalUniqueSenders</span><span class="sxs-lookup"><span data-stu-id="21676-103">GlobalUniqueSenders</span></span>

<span data-ttu-id="21676-104">Das **GlobalUniqueSender** -Element enthält eine Liste von allen Absendern der Unterhaltungselemente im Postfach.</span><span class="sxs-lookup"><span data-stu-id="21676-104">The **GlobalUniqueSender** element contains a list of all the senders of conversation items in the mailbox.</span></span> 
  
[<span data-ttu-id="21676-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="21676-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="21676-106">Conversations</span><span class="sxs-lookup"><span data-stu-id="21676-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="21676-107">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="21676-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="21676-108">GlobalUniqueSenders</span><span class="sxs-lookup"><span data-stu-id="21676-108">GlobalUniqueSenders</span></span>](globaluniquesenders.md)
  
```XML
<GlobalUniqueSender>
   <String/>
</GlobalUniqueSender>
```

 <span data-ttu-id="21676-109">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="21676-109">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="21676-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="21676-110">Attributes and elements</span></span>

<span data-ttu-id="21676-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="21676-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="21676-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="21676-112">Attributes</span></span>

<span data-ttu-id="21676-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="21676-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="21676-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="21676-114">Child elements</span></span>

|<span data-ttu-id="21676-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="21676-115">**Element**</span></span>|<span data-ttu-id="21676-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="21676-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="21676-117">String</span><span class="sxs-lookup"><span data-stu-id="21676-117">String</span></span>](string.md) <br/> |<span data-ttu-id="21676-118">Enthält einen einzelnen Gespräch Absender.</span><span class="sxs-lookup"><span data-stu-id="21676-118">Contains a single conversation sender.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="21676-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="21676-119">Parent elements</span></span>

|<span data-ttu-id="21676-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="21676-120">**Element**</span></span>|<span data-ttu-id="21676-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="21676-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="21676-122">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="21676-122">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="21676-123">Stellt eine einfache Unterhaltung dar.</span><span class="sxs-lookup"><span data-stu-id="21676-123">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="21676-124">Textwert</span><span class="sxs-lookup"><span data-stu-id="21676-124">Text value</span></span>

<span data-ttu-id="21676-125">Keine.</span><span class="sxs-lookup"><span data-stu-id="21676-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="21676-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="21676-126">Remarks</span></span>

<span data-ttu-id="21676-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="21676-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="21676-128">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="21676-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="21676-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="21676-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="21676-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="21676-130">Schema name</span></span>  <br/> |<span data-ttu-id="21676-131">Schematypen</span><span class="sxs-lookup"><span data-stu-id="21676-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="21676-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="21676-132">Validation file</span></span>  <br/> |<span data-ttu-id="21676-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="21676-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="21676-134">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="21676-134">Can be empty</span></span>  <br/> |<span data-ttu-id="21676-135">False</span><span class="sxs-lookup"><span data-stu-id="21676-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="21676-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="21676-136">See also</span></span>



[<span data-ttu-id="21676-137">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="21676-137">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="21676-138">ApplyConversationAction-Vorgang</span><span class="sxs-lookup"><span data-stu-id="21676-138">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="21676-139">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="21676-139">Conversations in EWS</span></span>](http://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

