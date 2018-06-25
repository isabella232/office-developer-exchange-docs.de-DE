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
ms.openlocfilehash: 5eb6e60d3ece8d8369f4603e36ffaaf72a3e459d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19829742"
---
# <a name="globaluniquerecipients"></a><span data-ttu-id="61dcc-103">GlobalUniqueRecipients</span><span class="sxs-lookup"><span data-stu-id="61dcc-103">GlobalUniqueRecipients</span></span>

<span data-ttu-id="61dcc-104">Das **GlobalUniqueRecipients** -Element enthält die Empfängerliste einer Unterhaltung über ein Postfach aggregiert.</span><span class="sxs-lookup"><span data-stu-id="61dcc-104">The **GlobalUniqueRecipients** element contains the recipient list of a conversation aggregated across a mailbox.</span></span> 
  
[<span data-ttu-id="61dcc-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="61dcc-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="61dcc-106">Conversations</span><span class="sxs-lookup"><span data-stu-id="61dcc-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="61dcc-107">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="61dcc-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="61dcc-108">GlobalUniqueRecipients</span><span class="sxs-lookup"><span data-stu-id="61dcc-108">GlobalUniqueRecipients</span></span>](globaluniquerecipients.md)
  
```XML
<GlobalUniqueRecipients>
   <String/>
</GlobalUniqueRecipients>
```

 <span data-ttu-id="61dcc-109">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="61dcc-109">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="61dcc-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="61dcc-110">Attributes and elements</span></span>

<span data-ttu-id="61dcc-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="61dcc-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="61dcc-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="61dcc-112">Attributes</span></span>

<span data-ttu-id="61dcc-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="61dcc-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="61dcc-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="61dcc-114">Child elements</span></span>

|<span data-ttu-id="61dcc-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="61dcc-115">**Element**</span></span>|<span data-ttu-id="61dcc-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="61dcc-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="61dcc-117">String</span><span class="sxs-lookup"><span data-stu-id="61dcc-117">String</span></span>](string.md) <br/> |<span data-ttu-id="61dcc-118">Einen einzelnen Gespräch Empfänger enthält.</span><span class="sxs-lookup"><span data-stu-id="61dcc-118">Contains a single conversation recipient.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="61dcc-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="61dcc-119">Parent elements</span></span>

|<span data-ttu-id="61dcc-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="61dcc-120">**Element**</span></span>|<span data-ttu-id="61dcc-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="61dcc-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="61dcc-122">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="61dcc-122">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="61dcc-123">Stellt eine einfache Unterhaltung dar.</span><span class="sxs-lookup"><span data-stu-id="61dcc-123">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="61dcc-124">Textwert</span><span class="sxs-lookup"><span data-stu-id="61dcc-124">Text value</span></span>

<span data-ttu-id="61dcc-125">Keine.</span><span class="sxs-lookup"><span data-stu-id="61dcc-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="61dcc-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="61dcc-126">Remarks</span></span>

<span data-ttu-id="61dcc-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="61dcc-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="61dcc-128">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="61dcc-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="61dcc-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="61dcc-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="61dcc-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="61dcc-130">Schema name</span></span>  <br/> |<span data-ttu-id="61dcc-131">Schematypen</span><span class="sxs-lookup"><span data-stu-id="61dcc-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="61dcc-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="61dcc-132">Validation file</span></span>  <br/> |<span data-ttu-id="61dcc-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="61dcc-133">types.xsd</span></span>  <br/> |
|<span data-ttu-id="61dcc-134">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="61dcc-134">Can be empty</span></span>  <br/> |<span data-ttu-id="61dcc-135">False</span><span class="sxs-lookup"><span data-stu-id="61dcc-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="61dcc-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="61dcc-136">See also</span></span>



[<span data-ttu-id="61dcc-137">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="61dcc-137">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="61dcc-138">ApplyConversationAction-Vorgang</span><span class="sxs-lookup"><span data-stu-id="61dcc-138">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="61dcc-139">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="61dcc-139">Conversations in EWS</span></span>](http://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

