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
description: Das GlobalUniqueSender-Element enthält eine Liste aller Absender von Unterhaltungselementen im Postfach.
ms.openlocfilehash: 0e85e201017e175a9ffc6b923976020d4157d5b7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459063"
---
# <a name="globaluniquesenders"></a><span data-ttu-id="c45fe-103">GlobalUniqueSenders</span><span class="sxs-lookup"><span data-stu-id="c45fe-103">GlobalUniqueSenders</span></span>

<span data-ttu-id="c45fe-104">Das **GlobalUniqueSender** -Element enthält eine Liste aller Absender von Unterhaltungselementen im Postfach.</span><span class="sxs-lookup"><span data-stu-id="c45fe-104">The **GlobalUniqueSender** element contains a list of all the senders of conversation items in the mailbox.</span></span> 
  
[<span data-ttu-id="c45fe-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="c45fe-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="c45fe-106">Conversations</span><span class="sxs-lookup"><span data-stu-id="c45fe-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="c45fe-107">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="c45fe-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="c45fe-108">GlobalUniqueSenders</span><span class="sxs-lookup"><span data-stu-id="c45fe-108">GlobalUniqueSenders</span></span>](globaluniquesenders.md)
  
```XML
<GlobalUniqueSender>
   <String/>
</GlobalUniqueSender>
```

 <span data-ttu-id="c45fe-109">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="c45fe-109">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c45fe-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c45fe-110">Attributes and elements</span></span>

<span data-ttu-id="c45fe-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c45fe-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c45fe-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="c45fe-112">Attributes</span></span>

<span data-ttu-id="c45fe-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="c45fe-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c45fe-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c45fe-114">Child elements</span></span>

|<span data-ttu-id="c45fe-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="c45fe-115">**Element**</span></span>|<span data-ttu-id="c45fe-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c45fe-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c45fe-117">String</span><span class="sxs-lookup"><span data-stu-id="c45fe-117">String</span></span>](string.md) <br/> |<span data-ttu-id="c45fe-118">Enthält einen einzelnen Unterhaltungs Absender.</span><span class="sxs-lookup"><span data-stu-id="c45fe-118">Contains a single conversation sender.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c45fe-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c45fe-119">Parent elements</span></span>

|<span data-ttu-id="c45fe-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="c45fe-120">**Element**</span></span>|<span data-ttu-id="c45fe-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c45fe-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c45fe-122">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="c45fe-122">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="c45fe-123">Stellt eine einfache Unterhaltung dar.</span><span class="sxs-lookup"><span data-stu-id="c45fe-123">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c45fe-124">Textwert</span><span class="sxs-lookup"><span data-stu-id="c45fe-124">Text value</span></span>

<span data-ttu-id="c45fe-125">Keine.</span><span class="sxs-lookup"><span data-stu-id="c45fe-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c45fe-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c45fe-126">Remarks</span></span>

<span data-ttu-id="c45fe-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="c45fe-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c45fe-128">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="c45fe-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c45fe-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="c45fe-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c45fe-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c45fe-130">Schema name</span></span>  <br/> |<span data-ttu-id="c45fe-131">Schematypen</span><span class="sxs-lookup"><span data-stu-id="c45fe-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="c45fe-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c45fe-132">Validation file</span></span>  <br/> |<span data-ttu-id="c45fe-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c45fe-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c45fe-134">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="c45fe-134">Can be empty</span></span>  <br/> |<span data-ttu-id="c45fe-135">False</span><span class="sxs-lookup"><span data-stu-id="c45fe-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c45fe-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c45fe-136">See also</span></span>



[<span data-ttu-id="c45fe-137">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="c45fe-137">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="c45fe-138">ApplyConversationAction-Vorgang</span><span class="sxs-lookup"><span data-stu-id="c45fe-138">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="c45fe-139">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="c45fe-139">Conversations in EWS</span></span>](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

