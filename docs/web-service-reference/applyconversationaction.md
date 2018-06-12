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
description: Das ApplyConversationAction-Element definiert eine Anforderung an die Aktionen auf Elemente in einer Unterhaltung anwenden.
ms.openlocfilehash: 1b672c6e6d2f60e50215417be7100e9cd77e2a58
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757355"
---
# <a name="applyconversationaction"></a><span data-ttu-id="08c36-103">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="08c36-103">ApplyConversationAction</span></span>

<span data-ttu-id="08c36-104">Das **ApplyConversationAction** -Element definiert eine Anforderung an die Aktionen auf Elemente in einer Unterhaltung anwenden.</span><span class="sxs-lookup"><span data-stu-id="08c36-104">The **ApplyConversationAction** element defines a request to apply actions to items in a conversation.</span></span> 
  
[<span data-ttu-id="08c36-105">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="08c36-105">ApplyConversationAction</span></span>](applyconversationaction.md)
  
```XML
<ApplyConversationAction>
   <ConversationActions/>
</ApplyConversationAction>
```

 <span data-ttu-id="08c36-106">**ApplyConversationActionType**</span><span class="sxs-lookup"><span data-stu-id="08c36-106">**ApplyConversationActionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="08c36-107">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="08c36-107">Attributes and elements</span></span>

<span data-ttu-id="08c36-108">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="08c36-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="08c36-109">Attribute</span><span class="sxs-lookup"><span data-stu-id="08c36-109">Attributes</span></span>

<span data-ttu-id="08c36-110">Keine.</span><span class="sxs-lookup"><span data-stu-id="08c36-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="08c36-111">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="08c36-111">Child elements</span></span>

|<span data-ttu-id="08c36-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="08c36-112">**Element**</span></span>|<span data-ttu-id="08c36-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="08c36-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="08c36-114">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="08c36-114">ConversationActions</span></span>](conversationactions.md) <br/> |<span data-ttu-id="08c36-115">Enthält eine Auflistung von Unterhaltungen und die Aktionen darauf anwenden.</span><span class="sxs-lookup"><span data-stu-id="08c36-115">Contains a collection of conversations and the actions to apply to them.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="08c36-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="08c36-116">Parent elements</span></span>

<span data-ttu-id="08c36-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="08c36-117">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="08c36-118">Textwert</span><span class="sxs-lookup"><span data-stu-id="08c36-118">Text value</span></span>

<span data-ttu-id="08c36-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="08c36-119">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="08c36-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="08c36-120">Remarks</span></span>

<span data-ttu-id="08c36-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="08c36-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="08c36-122">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="08c36-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="08c36-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="08c36-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="08c36-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="08c36-124">Schema Name</span></span>  <br/> |<span data-ttu-id="08c36-125">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="08c36-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="08c36-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="08c36-126">Validation File</span></span>  <br/> |<span data-ttu-id="08c36-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="08c36-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="08c36-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="08c36-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="08c36-129">False</span><span class="sxs-lookup"><span data-stu-id="08c36-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="08c36-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="08c36-130">See also</span></span>

- [<span data-ttu-id="08c36-131">ApplyConversationAction-Vorgang</span><span class="sxs-lookup"><span data-stu-id="08c36-131">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)
- [<span data-ttu-id="08c36-132">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="08c36-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

