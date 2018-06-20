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
description: Das GlobalUnreadCount-Element enthält die Anzahl der ungelesenen Unterhaltungselemente im Postfach.
ms.openlocfilehash: fe001b70633198c0c1351e3c11c9542ed556a938
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19829743"
---
# <a name="globalunreadcount"></a><span data-ttu-id="cfc84-103">GlobalUnreadCount</span><span class="sxs-lookup"><span data-stu-id="cfc84-103">GlobalUnreadCount</span></span>

<span data-ttu-id="cfc84-104">Das **GlobalUnreadCount** -Element enthält die Anzahl der ungelesenen Unterhaltungselemente im Postfach.</span><span class="sxs-lookup"><span data-stu-id="cfc84-104">The **GlobalUnreadCount** element contains a count of all the unread conversation items in the mailbox.</span></span> 
  
[<span data-ttu-id="cfc84-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="cfc84-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="cfc84-106">Conversations</span><span class="sxs-lookup"><span data-stu-id="cfc84-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="cfc84-107">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="cfc84-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="cfc84-108">GlobalUnreadCount</span><span class="sxs-lookup"><span data-stu-id="cfc84-108">GlobalUnreadCount</span></span>](globalunreadcount.md)
  
```XML
<GlobalUnreadCount/>
```

 <span data-ttu-id="cfc84-109">**xs: int**</span><span class="sxs-lookup"><span data-stu-id="cfc84-109">**xs:int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cfc84-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="cfc84-110">Attributes and elements</span></span>

<span data-ttu-id="cfc84-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="cfc84-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cfc84-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="cfc84-112">Attributes</span></span>

<span data-ttu-id="cfc84-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="cfc84-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cfc84-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cfc84-114">Child elements</span></span>

<span data-ttu-id="cfc84-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="cfc84-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="cfc84-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cfc84-116">Parent elements</span></span>

|<span data-ttu-id="cfc84-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="cfc84-117">**Element**</span></span>|<span data-ttu-id="cfc84-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cfc84-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cfc84-119">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="cfc84-119">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="cfc84-120">Stellt eine einfache Unterhaltung dar.</span><span class="sxs-lookup"><span data-stu-id="cfc84-120">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="cfc84-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="cfc84-121">Text value</span></span>

<span data-ttu-id="cfc84-122">Der Textwert der **GlobalUnreadCount** -Element ist ein Integer-Wert, der Anzahl der ungelesenen Unterhaltungselemente im Postfach darstellt.</span><span class="sxs-lookup"><span data-stu-id="cfc84-122">The text value of the **GlobalUnreadCount** element is an integer value that represents a count of all the unread conversation items in the mailbox.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="cfc84-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="cfc84-123">Remarks</span></span>

<span data-ttu-id="cfc84-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="cfc84-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cfc84-125">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="cfc84-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cfc84-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="cfc84-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="cfc84-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="cfc84-127">Schema name</span></span>  <br/> |<span data-ttu-id="cfc84-128">Schematypen</span><span class="sxs-lookup"><span data-stu-id="cfc84-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="cfc84-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="cfc84-129">Validation file</span></span>  <br/> |<span data-ttu-id="cfc84-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="cfc84-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="cfc84-131">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="cfc84-131">Can be empty</span></span>  <br/> |<span data-ttu-id="cfc84-132">False</span><span class="sxs-lookup"><span data-stu-id="cfc84-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cfc84-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cfc84-133">See also</span></span>



[<span data-ttu-id="cfc84-134">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="cfc84-134">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="cfc84-135">ApplyConversationAction-Vorgang</span><span class="sxs-lookup"><span data-stu-id="cfc84-135">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="cfc84-136">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="cfc84-136">Conversations in EWS</span></span>](http://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

