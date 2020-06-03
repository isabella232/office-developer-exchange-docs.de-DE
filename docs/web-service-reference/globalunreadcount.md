---
title: GlobalUnreadCount
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GlobalUnreadCount
api_type:
- schema
ms.assetid: 5e5ccf3e-2f95-4bf9-b915-8b7e59e807a5
description: Das GlobalUnreadCount-Element enthält die Anzahl aller ungelesenen Unterhaltungselemente im Postfach.
ms.openlocfilehash: 976067078908523936769b2856712e3e6908f0c4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530113"
---
# <a name="globalunreadcount"></a><span data-ttu-id="e6851-103">GlobalUnreadCount</span><span class="sxs-lookup"><span data-stu-id="e6851-103">GlobalUnreadCount</span></span>

<span data-ttu-id="e6851-104">Das **GlobalUnreadCount** -Element enthält die Anzahl aller ungelesenen Unterhaltungselemente im Postfach.</span><span class="sxs-lookup"><span data-stu-id="e6851-104">The **GlobalUnreadCount** element contains a count of all the unread conversation items in the mailbox.</span></span> 
  
[<span data-ttu-id="e6851-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="e6851-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="e6851-106">Conversations</span><span class="sxs-lookup"><span data-stu-id="e6851-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="e6851-107">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="e6851-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="e6851-108">GlobalUnreadCount</span><span class="sxs-lookup"><span data-stu-id="e6851-108">GlobalUnreadCount</span></span>](globalunreadcount.md)
  
```XML
<GlobalUnreadCount/>
```

 <span data-ttu-id="e6851-109">**xs: int**</span><span class="sxs-lookup"><span data-stu-id="e6851-109">**xs:int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e6851-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e6851-110">Attributes and elements</span></span>

<span data-ttu-id="e6851-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e6851-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e6851-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="e6851-112">Attributes</span></span>

<span data-ttu-id="e6851-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="e6851-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e6851-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e6851-114">Child elements</span></span>

<span data-ttu-id="e6851-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="e6851-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e6851-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e6851-116">Parent elements</span></span>

|<span data-ttu-id="e6851-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="e6851-117">**Element**</span></span>|<span data-ttu-id="e6851-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e6851-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e6851-119">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="e6851-119">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="e6851-120">Stellt eine einfache Unterhaltung dar.</span><span class="sxs-lookup"><span data-stu-id="e6851-120">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e6851-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="e6851-121">Text value</span></span>

<span data-ttu-id="e6851-122">Der Textwert des **GlobalUnreadCount** -Elements ist ein ganzzahliger Wert, der die Anzahl aller ungelesenen Unterhaltungselemente im Postfach darstellt.</span><span class="sxs-lookup"><span data-stu-id="e6851-122">The text value of the **GlobalUnreadCount** element is an integer value that represents a count of all the unread conversation items in the mailbox.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e6851-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e6851-123">Remarks</span></span>

<span data-ttu-id="e6851-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="e6851-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e6851-125">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="e6851-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e6851-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="e6851-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e6851-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e6851-127">Schema name</span></span>  <br/> |<span data-ttu-id="e6851-128">Schematypen</span><span class="sxs-lookup"><span data-stu-id="e6851-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="e6851-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e6851-129">Validation file</span></span>  <br/> |<span data-ttu-id="e6851-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e6851-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e6851-131">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="e6851-131">Can be empty</span></span>  <br/> |<span data-ttu-id="e6851-132">False</span><span class="sxs-lookup"><span data-stu-id="e6851-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e6851-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e6851-133">See also</span></span>



[<span data-ttu-id="e6851-134">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="e6851-134">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="e6851-135">ApplyConversationAction-Vorgang</span><span class="sxs-lookup"><span data-stu-id="e6851-135">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="e6851-136">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="e6851-136">Conversations in EWS</span></span>](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

