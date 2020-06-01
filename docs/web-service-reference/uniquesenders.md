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
description: Das UniqueSenders-Element enthält eine Liste aller Absender von Unterhaltungselementen im aktuellen Ordner. Dieses Element ist schreibgeschützt.
ms.openlocfilehash: 5c9a98a3083d02f3900cc263e0b99a570203b544
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459875"
---
# <a name="uniquesenders"></a><span data-ttu-id="5f49e-104">UniqueSenders</span><span class="sxs-lookup"><span data-stu-id="5f49e-104">UniqueSenders</span></span>

<span data-ttu-id="5f49e-105">Das **UniqueSenders** -Element enthält eine Liste aller Absender von Unterhaltungselementen im aktuellen Ordner.</span><span class="sxs-lookup"><span data-stu-id="5f49e-105">The **UniqueSenders** element contains a list of all the senders of conversation items in the current folder.</span></span> <span data-ttu-id="5f49e-106">Dieses Element ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="5f49e-106">This element is read-only.</span></span> 
  
[<span data-ttu-id="5f49e-107">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="5f49e-107">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="5f49e-108">Conversations</span><span class="sxs-lookup"><span data-stu-id="5f49e-108">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="5f49e-109">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="5f49e-109">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="5f49e-110">UniqueSenders</span><span class="sxs-lookup"><span data-stu-id="5f49e-110">UniqueSenders</span></span>](uniquesenders.md)
  
```XML
<UniqueSenders>
   <String/>
</UniqueSenders>
```

 <span data-ttu-id="5f49e-111">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="5f49e-111">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5f49e-112">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="5f49e-112">Attributes and elements</span></span>

<span data-ttu-id="5f49e-113">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="5f49e-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5f49e-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="5f49e-114">Attributes</span></span>

<span data-ttu-id="5f49e-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="5f49e-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5f49e-116">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5f49e-116">Child elements</span></span>

|<span data-ttu-id="5f49e-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="5f49e-117">**Element**</span></span>|<span data-ttu-id="5f49e-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5f49e-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5f49e-119">String</span><span class="sxs-lookup"><span data-stu-id="5f49e-119">String</span></span>](string.md) <br/> |<span data-ttu-id="5f49e-120">Enthält einen einzelnen Unterhaltungs Absender.</span><span class="sxs-lookup"><span data-stu-id="5f49e-120">Contains a single conversation sender.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5f49e-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5f49e-121">Parent elements</span></span>

|<span data-ttu-id="5f49e-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="5f49e-122">**Element**</span></span>|<span data-ttu-id="5f49e-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5f49e-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5f49e-124">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="5f49e-124">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="5f49e-125">Stellt eine einfache Unterhaltung dar.</span><span class="sxs-lookup"><span data-stu-id="5f49e-125">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5f49e-126">Textwert</span><span class="sxs-lookup"><span data-stu-id="5f49e-126">Text value</span></span>

<span data-ttu-id="5f49e-127">Keine.</span><span class="sxs-lookup"><span data-stu-id="5f49e-127">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5f49e-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5f49e-128">Remarks</span></span>

<span data-ttu-id="5f49e-129">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="5f49e-129">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5f49e-130">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="5f49e-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5f49e-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="5f49e-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5f49e-132">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="5f49e-132">Schema name</span></span>  <br/> |<span data-ttu-id="5f49e-133">Schematypen</span><span class="sxs-lookup"><span data-stu-id="5f49e-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="5f49e-134">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="5f49e-134">Validation file</span></span>  <br/> |<span data-ttu-id="5f49e-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5f49e-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5f49e-136">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="5f49e-136">Can be empty</span></span>  <br/> |<span data-ttu-id="5f49e-137">False</span><span class="sxs-lookup"><span data-stu-id="5f49e-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5f49e-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5f49e-138">See also</span></span>



[<span data-ttu-id="5f49e-139">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="5f49e-139">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="5f49e-140">ApplyConversationAction-Vorgang</span><span class="sxs-lookup"><span data-stu-id="5f49e-140">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="5f49e-141">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="5f49e-141">Conversations in EWS</span></span>](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

