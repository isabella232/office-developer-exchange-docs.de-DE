---
title: GlobalImportance
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GlobalImportance
api_type:
- schema
ms.assetid: 8bcec699-e771-4f38-b7d9-61f324af1b4e
description: Das GlobalImportance-Element enthält die aggregierte Wichtigkeit für alle Unterhaltungselemente in einem Postfach.
ms.openlocfilehash: c760168afa3edac20ca0ae7bc677610d8456d178
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459447"
---
# <a name="globalimportance"></a><span data-ttu-id="ba902-103">GlobalImportance</span><span class="sxs-lookup"><span data-stu-id="ba902-103">GlobalImportance</span></span>

<span data-ttu-id="ba902-104">Das **GlobalImportance** -Element enthält die aggregierte Wichtigkeit für alle Unterhaltungselemente in einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="ba902-104">The **GlobalImportance** element contains the aggregated importance for all conversation items in a mailbox.</span></span> 
  
[<span data-ttu-id="ba902-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="ba902-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="ba902-106">Conversations</span><span class="sxs-lookup"><span data-stu-id="ba902-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="ba902-107">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="ba902-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="ba902-108">GlobalImportance</span><span class="sxs-lookup"><span data-stu-id="ba902-108">GlobalImportance</span></span>](globalimportance.md)
  
```XML
<GlobalImportance> Low | Normal | High </GlobalImportance>
```

 <span data-ttu-id="ba902-109">**ImportanceChoicesType**</span><span class="sxs-lookup"><span data-stu-id="ba902-109">**ImportanceChoicesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ba902-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ba902-110">Attributes and elements</span></span>

<span data-ttu-id="ba902-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ba902-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ba902-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="ba902-112">Attributes</span></span>

<span data-ttu-id="ba902-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="ba902-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ba902-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ba902-114">Child elements</span></span>

<span data-ttu-id="ba902-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="ba902-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ba902-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ba902-116">Parent elements</span></span>

|<span data-ttu-id="ba902-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="ba902-117">**Element**</span></span>|<span data-ttu-id="ba902-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ba902-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ba902-119">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="ba902-119">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="ba902-120">Stellt eine einfache Unterhaltung dar.</span><span class="sxs-lookup"><span data-stu-id="ba902-120">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ba902-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="ba902-121">Text value</span></span>

<span data-ttu-id="ba902-122">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ba902-122">A text value is required.</span></span> <span data-ttu-id="ba902-123">Im folgenden sind die möglichen Werte für dieses Element angegeben:</span><span class="sxs-lookup"><span data-stu-id="ba902-123">The following are the possible values for this element:</span></span>
  
- <span data-ttu-id="ba902-124">Niedrig</span><span class="sxs-lookup"><span data-stu-id="ba902-124">Low</span></span>
    
- <span data-ttu-id="ba902-125">Normal</span><span class="sxs-lookup"><span data-stu-id="ba902-125">Normal</span></span>
    
- <span data-ttu-id="ba902-126">Hoch</span><span class="sxs-lookup"><span data-stu-id="ba902-126">High</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ba902-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ba902-127">Remarks</span></span>

<span data-ttu-id="ba902-128">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="ba902-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ba902-129">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="ba902-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ba902-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="ba902-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ba902-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ba902-131">Schema name</span></span>  <br/> |<span data-ttu-id="ba902-132">Schematypen</span><span class="sxs-lookup"><span data-stu-id="ba902-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="ba902-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ba902-133">Validation file</span></span>  <br/> |<span data-ttu-id="ba902-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ba902-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ba902-135">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="ba902-135">Can be empty</span></span>  <br/> |<span data-ttu-id="ba902-136">False</span><span class="sxs-lookup"><span data-stu-id="ba902-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ba902-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ba902-137">See also</span></span>



[<span data-ttu-id="ba902-138">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="ba902-138">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="ba902-139">ApplyConversationAction-Vorgang</span><span class="sxs-lookup"><span data-stu-id="ba902-139">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="ba902-140">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="ba902-140">Conversations in EWS</span></span>](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

