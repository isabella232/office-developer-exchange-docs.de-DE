---
title: EnableAlwaysDelete
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- EnableAlwaysDelete
api_type:
- schema
ms.assetid: 7753aec5-3f93-4aeb-a28e-8b9b42ca7f9b
description: Das EnableAlwaysDelete-Element gibt ein Flag an, das das Löschen für alle neuen Elemente in einer Unterhaltung ermöglicht.
ms.openlocfilehash: 14784d3a6ba52c76b64b81e15c0522d66d125cbf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526207"
---
# <a name="enablealwaysdelete"></a><span data-ttu-id="34d38-103">EnableAlwaysDelete</span><span class="sxs-lookup"><span data-stu-id="34d38-103">EnableAlwaysDelete</span></span>

<span data-ttu-id="34d38-104">Das **EnableAlwaysDelete** -Element gibt ein Flag an, das das Löschen für alle neuen Elemente in einer Unterhaltung ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="34d38-104">The **EnableAlwaysDelete** element specifies a flag that enables deletion for all new items in a conversation.</span></span> 
  
[<span data-ttu-id="34d38-105">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="34d38-105">ApplyConversationAction</span></span>](applyconversationaction.md)
  
[<span data-ttu-id="34d38-106">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="34d38-106">ConversationActions</span></span>](conversationactions.md)
  
[<span data-ttu-id="34d38-107">Unterhaltung</span><span class="sxs-lookup"><span data-stu-id="34d38-107">ConversationAction</span></span>](conversationaction.md)
  
[<span data-ttu-id="34d38-108">EnableAlwaysDelete</span><span class="sxs-lookup"><span data-stu-id="34d38-108">EnableAlwaysDelete</span></span>](enablealwaysdelete.md)
  
```XML
<EnableAlwaysDelete/>
```

 <span data-ttu-id="34d38-109">**xs: Boolean**</span><span class="sxs-lookup"><span data-stu-id="34d38-109">**xs:boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="34d38-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="34d38-110">Attributes and elements</span></span>

<span data-ttu-id="34d38-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="34d38-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="34d38-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="34d38-112">Attributes</span></span>

<span data-ttu-id="34d38-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="34d38-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="34d38-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="34d38-114">Child elements</span></span>

<span data-ttu-id="34d38-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="34d38-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="34d38-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="34d38-116">Parent elements</span></span>

|<span data-ttu-id="34d38-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="34d38-117">**Element**</span></span>|<span data-ttu-id="34d38-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="34d38-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="34d38-119">Unterhaltung</span><span class="sxs-lookup"><span data-stu-id="34d38-119">ConversationAction</span></span>](conversationaction.md) <br/> |<span data-ttu-id="34d38-120">Enthält eine einzelne Aktion, die auf eine einzelne Unterhaltung angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="34d38-120">Contains a single action to be applied to a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="34d38-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="34d38-121">Text value</span></span>

<span data-ttu-id="34d38-122">Der Textwert des **EnableAlwaysDelete** -Elements ist **true** , um das Löschen aller Elemente in der Unterhaltung zu ermöglichen; andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="34d38-122">The text value of the **EnableAlwaysDelete** element is **true** to enable the deletion of all items in conversation; otherwise, **false**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="34d38-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="34d38-123">Remarks</span></span>

<span data-ttu-id="34d38-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="34d38-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="34d38-125">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="34d38-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="34d38-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="34d38-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="34d38-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="34d38-127">Schema Name</span></span>  <br/> |<span data-ttu-id="34d38-128">Schematypen</span><span class="sxs-lookup"><span data-stu-id="34d38-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="34d38-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="34d38-129">Validation File</span></span>  <br/> |<span data-ttu-id="34d38-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="34d38-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="34d38-131">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="34d38-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="34d38-132">False</span><span class="sxs-lookup"><span data-stu-id="34d38-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="34d38-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="34d38-133">See also</span></span>



[<span data-ttu-id="34d38-134">ApplyConversationAction-Vorgang</span><span class="sxs-lookup"><span data-stu-id="34d38-134">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)

