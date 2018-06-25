---
title: Unterhaltungen
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Conversations
api_type:
- schema
ms.assetid: 1d18f98c-6457-45e9-a934-32da20885ac6
description: Das Element Unterhaltungen enthält ein Array von Unterhaltungen, die in der Antwort FindConversation zurückgegeben werden.
ms.openlocfilehash: cd36364bd975d1464af9a1114c64c29543b4ec47
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757711"
---
# <a name="conversations"></a><span data-ttu-id="ad40b-103">Unterhaltungen</span><span class="sxs-lookup"><span data-stu-id="ad40b-103">Conversations</span></span>

<span data-ttu-id="ad40b-104">Das Element **Unterhaltungen** enthält ein Array von Unterhaltungen, die in der Antwort **FindConversation** zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ad40b-104">The **Conversations** element contains an array of conversations that are returned in the **FindConversation** response.</span></span> 
  
[<span data-ttu-id="ad40b-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="ad40b-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="ad40b-106">Conversations</span><span class="sxs-lookup"><span data-stu-id="ad40b-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
```xml
<Conversations>
   <Conversation/>
</Conversations>
```

 <span data-ttu-id="ad40b-107">**ArrayOfConversationsType**</span><span class="sxs-lookup"><span data-stu-id="ad40b-107">**ArrayOfConversationsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ad40b-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ad40b-108">Attributes and elements</span></span>

<span data-ttu-id="ad40b-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ad40b-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ad40b-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="ad40b-110">Attributes</span></span>

<span data-ttu-id="ad40b-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="ad40b-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ad40b-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ad40b-112">Child elements</span></span>

|<span data-ttu-id="ad40b-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="ad40b-113">**Element**</span></span>|<span data-ttu-id="ad40b-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ad40b-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ad40b-115">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="ad40b-115">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="ad40b-116">Stellt eine einfache Unterhaltung dar.</span><span class="sxs-lookup"><span data-stu-id="ad40b-116">Represents a single conversation.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ad40b-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ad40b-117">Parent elements</span></span>

|<span data-ttu-id="ad40b-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="ad40b-118">**Element**</span></span>|<span data-ttu-id="ad40b-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ad40b-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ad40b-120">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="ad40b-120">FindConversationResponse</span></span>](findconversationresponse.md) <br/> |<span data-ttu-id="ad40b-121">Definiert eine Antwort auf eine **FindConversation** an.</span><span class="sxs-lookup"><span data-stu-id="ad40b-121">Defines a response to a **FindConversation** request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ad40b-122">Textwert</span><span class="sxs-lookup"><span data-stu-id="ad40b-122">Text value</span></span>

<span data-ttu-id="ad40b-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="ad40b-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ad40b-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ad40b-124">Remarks</span></span>

<span data-ttu-id="ad40b-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="ad40b-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ad40b-126">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="ad40b-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ad40b-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="ad40b-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ad40b-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ad40b-128">Schema name</span></span>  <br/> |<span data-ttu-id="ad40b-129">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="ad40b-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ad40b-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ad40b-130">Validation file</span></span>  <br/> |<span data-ttu-id="ad40b-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ad40b-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ad40b-132">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="ad40b-132">Can be empty</span></span>  <br/> |<span data-ttu-id="ad40b-133">False</span><span class="sxs-lookup"><span data-stu-id="ad40b-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ad40b-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ad40b-134">See also</span></span>



[<span data-ttu-id="ad40b-135">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="ad40b-135">FindConversation operation</span></span>](findconversation-operation.md)


[<span data-ttu-id="ad40b-136">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="ad40b-136">Conversations in EWS</span></span>](http://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

