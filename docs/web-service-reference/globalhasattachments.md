---
title: GlobalHasAttachments
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GlobalHasAttachments
api_type:
- schema
ms.assetid: 3d075e93-14bc-479d-957f-9b7873d1db39
description: Das GlobalHasAttachments -Element enthält einen Wert, der angibt, ob mindestens eine unterhaltungselement in einem Postfach eine Anlage enthält.
ms.openlocfilehash: 85443c45f611a2f4bff392ffecb26029564d7558
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19829715"
---
# <a name="globalhasattachments"></a><span data-ttu-id="0b698-103">GlobalHasAttachments</span><span class="sxs-lookup"><span data-stu-id="0b698-103">GlobalHasAttachments</span></span>

<span data-ttu-id="0b698-104">Das **GlobalHasAttachments** -Element enthält einen Wert, der angibt, ob mindestens eine unterhaltungselement in einem Postfach eine Anlage enthält.</span><span class="sxs-lookup"><span data-stu-id="0b698-104">The **GlobalHasAttachments** element contains a value that indicates whether at least one conversation item in a mailbox has an attachment.</span></span> 
  
[<span data-ttu-id="0b698-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="0b698-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="0b698-106">Conversations</span><span class="sxs-lookup"><span data-stu-id="0b698-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="0b698-107">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="0b698-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="0b698-108">GlobalHasAttachments</span><span class="sxs-lookup"><span data-stu-id="0b698-108">GlobalHasAttachments</span></span>](globalhasattachments.md)
  
```XML
<GlobalHasAttachments/>
```

 <span data-ttu-id="0b698-109">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="0b698-109">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0b698-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="0b698-110">Attributes and elements</span></span>

<span data-ttu-id="0b698-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="0b698-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0b698-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="0b698-112">Attributes</span></span>

<span data-ttu-id="0b698-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="0b698-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0b698-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0b698-114">Child elements</span></span>

<span data-ttu-id="0b698-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="0b698-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0b698-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0b698-116">Parent elements</span></span>

|<span data-ttu-id="0b698-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="0b698-117">**Element**</span></span>|<span data-ttu-id="0b698-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0b698-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0b698-119">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="0b698-119">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="0b698-120">Stellt eine einfache Unterhaltung dar.</span><span class="sxs-lookup"><span data-stu-id="0b698-120">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0b698-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="0b698-121">Text value</span></span>

<span data-ttu-id="0b698-p101">Der Wert des **GlobalHasAttachments** -Elements gibt an, ob mindestens eine unterhaltungselement in einem Postfach eine Anlage enthält. Ein Textwert, der einen booleschen Wert darstellt, ist erforderlich. Der Wert **true** bedeutet, dass die Unterhaltung mindestens eine Anlage sichtbar ist. Der Wert **false** bedeutet, dass die Unterhaltung keine Anlagen enthält oder nur Anlagen ausgeblendet wurde.</span><span class="sxs-lookup"><span data-stu-id="0b698-p101">The value of the **GlobalHasAttachments** element indicates whether at least one conversation item in a mailbox has an attachment. A text value that represents a Boolean value is required. A value of **true** means that the conversation has at least one visible attachment. A value of **false** means that the conversation either has no attachments or has only hidden attachments.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="0b698-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0b698-126">Remarks</span></span>

<span data-ttu-id="0b698-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0b698-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0b698-128">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="0b698-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0b698-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="0b698-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0b698-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="0b698-130">Schema name</span></span>  <br/> |<span data-ttu-id="0b698-131">Schematypen</span><span class="sxs-lookup"><span data-stu-id="0b698-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="0b698-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="0b698-132">Validation file</span></span>  <br/> |<span data-ttu-id="0b698-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0b698-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0b698-134">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="0b698-134">Can be empty</span></span>  <br/> |<span data-ttu-id="0b698-135">False</span><span class="sxs-lookup"><span data-stu-id="0b698-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0b698-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b698-136">See also</span></span>



[<span data-ttu-id="0b698-137">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="0b698-137">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="0b698-138">ApplyConversationAction-Vorgang</span><span class="sxs-lookup"><span data-stu-id="0b698-138">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="0b698-139">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="0b698-139">Conversations in EWS</span></span>](http://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

