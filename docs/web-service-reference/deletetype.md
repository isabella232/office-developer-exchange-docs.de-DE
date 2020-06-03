---
title: Deletetypeharddelete
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteType
api_type:
- schema
ms.assetid: 6e3136cd-9cb4-493a-aa85-9678f719002d
description: Das deleteType-Element gibt an, wie Elemente in einer Unterhaltung gelöscht werden.
ms.openlocfilehash: 199f7afc29fe866865509d2fb90d24944113d5c0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44442633"
---
# <a name="deletetype"></a><span data-ttu-id="bd9b2-103">Deletetypeharddelete</span><span class="sxs-lookup"><span data-stu-id="bd9b2-103">DeleteType</span></span>

<span data-ttu-id="bd9b2-104">Das **deleteType** -Element gibt an, wie Elemente in einer Unterhaltung gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="bd9b2-104">The **DeleteType** element indicates how items in a conversation are deleted.</span></span> 
  
- [<span data-ttu-id="bd9b2-105">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="bd9b2-105">ApplyConversationAction</span></span>](applyconversationaction.md)  
- [<span data-ttu-id="bd9b2-106">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="bd9b2-106">ConversationActions</span></span>](conversationactions.md)  
- [<span data-ttu-id="bd9b2-107">Unterhaltung</span><span class="sxs-lookup"><span data-stu-id="bd9b2-107">ConversationAction</span></span>](conversationaction.md)  
- [<span data-ttu-id="bd9b2-108">Deletetypeharddelete</span><span class="sxs-lookup"><span data-stu-id="bd9b2-108">DeleteType</span></span>](deletetype.md)
  
```XML
<DeleteType> HardDelete | MoveToDeletedItems | SoftDelete </DeleteType>
```

 <span data-ttu-id="bd9b2-109">**DisposalType**</span><span class="sxs-lookup"><span data-stu-id="bd9b2-109">**DisposalType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bd9b2-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="bd9b2-110">Attributes and elements</span></span>

<span data-ttu-id="bd9b2-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="bd9b2-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bd9b2-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="bd9b2-112">Attributes</span></span>

<span data-ttu-id="bd9b2-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="bd9b2-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bd9b2-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bd9b2-114">Child elements</span></span>

<span data-ttu-id="bd9b2-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="bd9b2-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="bd9b2-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bd9b2-116">Parent elements</span></span>

|<span data-ttu-id="bd9b2-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="bd9b2-117">**Element**</span></span>|<span data-ttu-id="bd9b2-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bd9b2-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bd9b2-119">Unterhaltung</span><span class="sxs-lookup"><span data-stu-id="bd9b2-119">ConversationAction</span></span>](conversationaction.md) <br/> |<span data-ttu-id="bd9b2-120">Enthält eine einzelne Aktion, die auf eine einzelne Unterhaltung angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="bd9b2-120">Contains a single action to be applied to a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="bd9b2-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="bd9b2-121">Text value</span></span>

<span data-ttu-id="bd9b2-122">Der Textwert des **deleteType** -Elements gibt an, wie Elemente in einer Unterhaltung gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="bd9b2-122">The text value of the **DeleteType** element indicates how items in a conversation are deleted.</span></span> <span data-ttu-id="bd9b2-123">Im folgenden sind die möglichen Text Werte zu finden:</span><span class="sxs-lookup"><span data-stu-id="bd9b2-123">The following are the possible text values:</span></span> 
  
- <span data-ttu-id="bd9b2-124">HardDelete – gibt an, dass Elemente in einer Unterhaltung dauerhaft aus der Postfachdatenbank entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="bd9b2-124">HardDelete - Indicates that items in a conversation are permanently removed from the mailbox database.</span></span>
    
- <span data-ttu-id="bd9b2-125">MoveToDeleteItems – gibt an, dass Elemente in einer Unterhaltung in den Ordner "Gelöschte Elemente" verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="bd9b2-125">MoveToDeleteItems - Indicates that items in a conversation are moved to the Deleted Items folder.</span></span>
    
- <span data-ttu-id="bd9b2-126">SoftDelete – gibt an, dass Elemente in einer Unterhaltung in den Papierkorb verschoben werden, wenn der Papierkorb aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="bd9b2-126">SoftDelete - Indicates that items in a conversation are moved to the dumpster if the dumpster is enabled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bd9b2-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bd9b2-127">Remarks</span></span>

<span data-ttu-id="bd9b2-128">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="bd9b2-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bd9b2-129">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="bd9b2-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bd9b2-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="bd9b2-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="bd9b2-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="bd9b2-131">Schema Name</span></span>  <br/> |<span data-ttu-id="bd9b2-132">Schematypen</span><span class="sxs-lookup"><span data-stu-id="bd9b2-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="bd9b2-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="bd9b2-133">Validation File</span></span>  <br/> |<span data-ttu-id="bd9b2-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="bd9b2-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="bd9b2-135">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="bd9b2-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="bd9b2-136">False</span><span class="sxs-lookup"><span data-stu-id="bd9b2-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bd9b2-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bd9b2-137">See also</span></span>

- [<span data-ttu-id="bd9b2-138">ApplyConversationAction-Vorgang</span><span class="sxs-lookup"><span data-stu-id="bd9b2-138">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)
- [<span data-ttu-id="bd9b2-139">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="bd9b2-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

