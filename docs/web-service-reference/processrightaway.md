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
description: Das ProcessRightAway-Element gibt an, ob die Antwort gesendet wird, sobald die Aktion auf dem Server verarbeitet wird oder ob die Antwort gesendet wird, nachdem die Aktion abgeschlossen wurde. Dieses Element muss vorhanden sein, damit die Antwort asynchron an die angeforderte Aktion gesendet werden kann.
ms.openlocfilehash: 58d2b926c48db5e7395df64e1f8ee9d6a8f0e73c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44434071"
---
# <a name="processrightaway"></a><span data-ttu-id="3b921-104">ProcessRightAway</span><span class="sxs-lookup"><span data-stu-id="3b921-104">ProcessRightAway</span></span>

<span data-ttu-id="3b921-105">Das **ProcessRightAway** -Element gibt an, ob die Antwort gesendet wird, sobald die Aktion auf dem Server verarbeitet wird oder ob die Antwort gesendet wird, nachdem die Aktion abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="3b921-105">The **ProcessRightAway** element indicates whether the response is sent as soon as the action starts processing on the server or whether the response is sent after the action has completed.</span></span> <span data-ttu-id="3b921-106">Dieses Element muss vorhanden sein, damit die Antwort asynchron an die angeforderte Aktion gesendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="3b921-106">This element must be present for the response to be sent asynchronous to the requested action.</span></span> 
  
[<span data-ttu-id="3b921-107">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="3b921-107">ApplyConversationAction</span></span>](applyconversationaction.md)
  
[<span data-ttu-id="3b921-108">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="3b921-108">ConversationActions</span></span>](conversationactions.md)
  
[<span data-ttu-id="3b921-109">Unterhaltung</span><span class="sxs-lookup"><span data-stu-id="3b921-109">ConversationAction</span></span>](conversationaction.md)
  
[<span data-ttu-id="3b921-110">ProcessRightAway</span><span class="sxs-lookup"><span data-stu-id="3b921-110">ProcessRightAway</span></span>](processrightaway.md)
  
```XML
<ProcessRightAway/>
```

 <span data-ttu-id="3b921-111">**xs: Boolean**</span><span class="sxs-lookup"><span data-stu-id="3b921-111">**xs:boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3b921-112">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3b921-112">Attributes and elements</span></span>

<span data-ttu-id="3b921-113">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="3b921-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3b921-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="3b921-114">Attributes</span></span>

<span data-ttu-id="3b921-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="3b921-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3b921-116">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3b921-116">Child elements</span></span>

<span data-ttu-id="3b921-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="3b921-117">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3b921-118">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3b921-118">Parent elements</span></span>

|<span data-ttu-id="3b921-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="3b921-119">**Element**</span></span>|<span data-ttu-id="3b921-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3b921-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3b921-121">Unterhaltung</span><span class="sxs-lookup"><span data-stu-id="3b921-121">ConversationAction</span></span>](conversationaction.md) <br/> |<span data-ttu-id="3b921-122">Enthält eine einzelne Aktion, die auf eine einzelne Unterhaltung angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3b921-122">Contains a single action to be applied to a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3b921-123">Textwert</span><span class="sxs-lookup"><span data-stu-id="3b921-123">Text value</span></span>

<span data-ttu-id="3b921-124">Der Textwert **true** gibt an, dass die Antwort gesendet wird, sobald die Aktion auf dem Server verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="3b921-124">A text value of **true** indicates that the response is sent as soon as the action starts processing on the server.</span></span> <span data-ttu-id="3b921-125">Der Textwert **false** gibt an, dass die Antwort gesendet wird, nachdem die Aktion abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="3b921-125">A text value of **false** indicates that the response is sent after the action has completed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3b921-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3b921-126">Remarks</span></span>

<span data-ttu-id="3b921-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="3b921-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3b921-128">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="3b921-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3b921-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="3b921-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3b921-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="3b921-130">Schema Name</span></span>  <br/> |<span data-ttu-id="3b921-131">Schematypen</span><span class="sxs-lookup"><span data-stu-id="3b921-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="3b921-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="3b921-132">Validation File</span></span>  <br/> |<span data-ttu-id="3b921-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3b921-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3b921-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="3b921-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="3b921-135">False</span><span class="sxs-lookup"><span data-stu-id="3b921-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3b921-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3b921-136">See also</span></span>



[<span data-ttu-id="3b921-137">ApplyConversationAction-Vorgang</span><span class="sxs-lookup"><span data-stu-id="3b921-137">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


- [<span data-ttu-id="3b921-138">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="3b921-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

