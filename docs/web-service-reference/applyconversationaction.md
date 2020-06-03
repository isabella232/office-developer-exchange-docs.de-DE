---
title: ApplyConversationAction
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ApplyConversationAction
api_type:
- schema
ms.assetid: e0ee8f30-529b-4d87-8bc0-b6616e75fb6b
description: Das ApplyConversationAction-Element definiert eine Anforderung zum Anwenden von Aktionen auf Elemente in einer Unterhaltung.
ms.openlocfilehash: 659b3392778bb1a318c3942a0c8e314f12110c12
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461688"
---
# <a name="applyconversationaction"></a><span data-ttu-id="c59ed-103">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="c59ed-103">ApplyConversationAction</span></span>

<span data-ttu-id="c59ed-104">Das **ApplyConversationAction** -Element definiert eine Anforderung zum Anwenden von Aktionen auf Elemente in einer Unterhaltung.</span><span class="sxs-lookup"><span data-stu-id="c59ed-104">The **ApplyConversationAction** element defines a request to apply actions to items in a conversation.</span></span> 
  
[<span data-ttu-id="c59ed-105">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="c59ed-105">ApplyConversationAction</span></span>](applyconversationaction.md)
  
```XML
<ApplyConversationAction>
   <ConversationActions/>
</ApplyConversationAction>
```

 <span data-ttu-id="c59ed-106">**ApplyConversationActionType**</span><span class="sxs-lookup"><span data-stu-id="c59ed-106">**ApplyConversationActionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c59ed-107">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c59ed-107">Attributes and elements</span></span>

<span data-ttu-id="c59ed-108">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c59ed-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c59ed-109">Attribute</span><span class="sxs-lookup"><span data-stu-id="c59ed-109">Attributes</span></span>

<span data-ttu-id="c59ed-110">Keine.</span><span class="sxs-lookup"><span data-stu-id="c59ed-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c59ed-111">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c59ed-111">Child elements</span></span>

|<span data-ttu-id="c59ed-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="c59ed-112">**Element**</span></span>|<span data-ttu-id="c59ed-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c59ed-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c59ed-114">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="c59ed-114">ConversationActions</span></span>](conversationactions.md) <br/> |<span data-ttu-id="c59ed-115">Enthält eine Auflistung von Unterhaltungen und die Aktionen, die auf diese angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c59ed-115">Contains a collection of conversations and the actions to apply to them.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c59ed-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c59ed-116">Parent elements</span></span>

<span data-ttu-id="c59ed-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="c59ed-117">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="c59ed-118">Textwert</span><span class="sxs-lookup"><span data-stu-id="c59ed-118">Text value</span></span>

<span data-ttu-id="c59ed-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="c59ed-119">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c59ed-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c59ed-120">Remarks</span></span>

<span data-ttu-id="c59ed-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="c59ed-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c59ed-122">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="c59ed-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c59ed-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="c59ed-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c59ed-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c59ed-124">Schema Name</span></span>  <br/> |<span data-ttu-id="c59ed-125">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="c59ed-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c59ed-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c59ed-126">Validation File</span></span>  <br/> |<span data-ttu-id="c59ed-127">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="c59ed-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c59ed-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="c59ed-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="c59ed-129">False</span><span class="sxs-lookup"><span data-stu-id="c59ed-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c59ed-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c59ed-130">See also</span></span>

- [<span data-ttu-id="c59ed-131">ApplyConversationAction-Vorgang</span><span class="sxs-lookup"><span data-stu-id="c59ed-131">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)
- [<span data-ttu-id="c59ed-132">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="c59ed-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

