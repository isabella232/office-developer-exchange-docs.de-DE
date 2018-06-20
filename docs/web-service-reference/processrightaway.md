---
title: ProcessRightAway
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ProcessRightAway
api_type:
- schema
ms.assetid: f6bba68b-ae4f-41c1-b3e7-c8a31cdb1b0c
description: Das ProcessRightAway-Element gibt an, ob die Antwort gesendet wird, sobald die Aktion startet die Verarbeitung auf dem Server oder gibt an, ob die Antwort gesendet wird, nachdem der Vorgang abgeschlossen wurde. Dieses Element muss vorhanden sein, damit die Antwort für die angeforderte Aktion asynchronen gesendet werden.
ms.openlocfilehash: 940f8e8fa0a53801ce1c3a45c3aecf1bdb6f519d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830898"
---
# <a name="processrightaway"></a><span data-ttu-id="485a0-104">ProcessRightAway</span><span class="sxs-lookup"><span data-stu-id="485a0-104">ProcessRightAway</span></span>

<span data-ttu-id="485a0-105">Das **ProcessRightAway** -Element gibt an, ob die Antwort gesendet wird, sobald die Aktion startet die Verarbeitung auf dem Server oder gibt an, ob die Antwort gesendet wird, nachdem der Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="485a0-105">The **ProcessRightAway** element indicates whether the response is sent as soon as the action starts processing on the server or whether the response is sent after the action has completed.</span></span> <span data-ttu-id="485a0-106">Dieses Element muss vorhanden sein, damit die Antwort für die angeforderte Aktion asynchronen gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="485a0-106">This element must be present for the response to be sent asynchronous to the requested action.</span></span> 
  
[<span data-ttu-id="485a0-107">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="485a0-107">ApplyConversationAction</span></span>](applyconversationaction.md)
  
[<span data-ttu-id="485a0-108">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="485a0-108">ConversationActions</span></span>](conversationactions.md)
  
[<span data-ttu-id="485a0-109">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="485a0-109">ConversationAction</span></span>](conversationaction.md)
  
[<span data-ttu-id="485a0-110">ProcessRightAway</span><span class="sxs-lookup"><span data-stu-id="485a0-110">ProcessRightAway</span></span>](processrightaway.md)
  
```XML
<ProcessRightAway/>
```

 <span data-ttu-id="485a0-111">**xs: Boolean**</span><span class="sxs-lookup"><span data-stu-id="485a0-111">**xs:boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="485a0-112">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="485a0-112">Attributes and elements</span></span>

<span data-ttu-id="485a0-113">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="485a0-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="485a0-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="485a0-114">Attributes</span></span>

<span data-ttu-id="485a0-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="485a0-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="485a0-116">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="485a0-116">Child elements</span></span>

<span data-ttu-id="485a0-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="485a0-117">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="485a0-118">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="485a0-118">Parent elements</span></span>

|<span data-ttu-id="485a0-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="485a0-119">**Element**</span></span>|<span data-ttu-id="485a0-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="485a0-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="485a0-121">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="485a0-121">ConversationAction</span></span>](conversationaction.md) <br/> |<span data-ttu-id="485a0-122">Enthält eine einzelne Aktion auf einem einzelnen Gespräch angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="485a0-122">Contains a single action to be applied to a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="485a0-123">Textwert</span><span class="sxs-lookup"><span data-stu-id="485a0-123">Text value</span></span>

<span data-ttu-id="485a0-124">Der Textwert **true** gibt an, dass die Antwort gesendet wird, sobald die Aktion Verarbeitung auf dem Server gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="485a0-124">A text value of **true** indicates that the response is sent as soon as the action starts processing on the server.</span></span> <span data-ttu-id="485a0-125">Der Textwert **false** gibt an, dass die Antwort gesendet wird, nachdem der Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="485a0-125">A text value of **false** indicates that the response is sent after the action has completed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="485a0-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="485a0-126">Remarks</span></span>

<span data-ttu-id="485a0-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="485a0-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="485a0-128">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="485a0-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="485a0-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="485a0-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="485a0-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="485a0-130">Schema Name</span></span>  <br/> |<span data-ttu-id="485a0-131">Schematypen</span><span class="sxs-lookup"><span data-stu-id="485a0-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="485a0-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="485a0-132">Validation File</span></span>  <br/> |<span data-ttu-id="485a0-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="485a0-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="485a0-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="485a0-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="485a0-135">False</span><span class="sxs-lookup"><span data-stu-id="485a0-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="485a0-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="485a0-136">See also</span></span>



[<span data-ttu-id="485a0-137">ApplyConversationAction-Vorgang</span><span class="sxs-lookup"><span data-stu-id="485a0-137">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


- [<span data-ttu-id="485a0-138">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="485a0-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

