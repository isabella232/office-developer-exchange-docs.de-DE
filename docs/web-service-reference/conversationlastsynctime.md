---
title: ConversationLastSyncTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConversationLastSyncTime
api_type:
- schema
ms.assetid: 90f8f9e3-5fc6-4a6a-bdfb-fc91fa51f8a2
description: Das ConversationLastSyncTime-Element enthält das Datum und die Uhrzeit, zu der der letzten eine Unterhaltung Synchronisierung. Dieses Element muss vorhanden sein, wenn Sie versuchen, um alle Elemente in einer Unterhaltung zu löschen, die bis zu der angegebenen Zeit empfangen wurden.
ms.openlocfilehash: 3b086d69ac0ef307059df4902e65f796c63733d1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757703"
---
# <a name="conversationlastsynctime"></a><span data-ttu-id="70b4b-104">ConversationLastSyncTime</span><span class="sxs-lookup"><span data-stu-id="70b4b-104">ConversationLastSyncTime</span></span>

<span data-ttu-id="70b4b-105">Das **ConversationLastSyncTime** -Element enthält das Datum und die Uhrzeit, zu der der letzten eine Unterhaltung Synchronisierung.</span><span class="sxs-lookup"><span data-stu-id="70b4b-105">The **ConversationLastSyncTime** element contains the date and time that a conversation was last synchronized.</span></span> <span data-ttu-id="70b4b-106">Dieses Element muss vorhanden sein, wenn Sie versuchen, um alle Elemente in einer Unterhaltung zu löschen, die bis zu der angegebenen Zeit empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="70b4b-106">This element must be present when trying to delete all items in a conversation that were received up to the specified time.</span></span> 
  
[<span data-ttu-id="70b4b-107">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="70b4b-107">ApplyConversationAction</span></span>](applyconversationaction.md)
  
[<span data-ttu-id="70b4b-108">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="70b4b-108">ConversationActions</span></span>](conversationactions.md)
  
[<span data-ttu-id="70b4b-109">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="70b4b-109">ConversationAction</span></span>](conversationaction.md)
  
[<span data-ttu-id="70b4b-110">ConversationLastSyncTime</span><span class="sxs-lookup"><span data-stu-id="70b4b-110">ConversationLastSyncTime</span></span>](conversationlastsynctime.md)
  
```XML
<ConversationLastSyncTime/>
```

 <span data-ttu-id="70b4b-111">**xs: DateTime**</span><span class="sxs-lookup"><span data-stu-id="70b4b-111">**xs:dateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="70b4b-112">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="70b4b-112">Attributes and elements</span></span>

<span data-ttu-id="70b4b-113">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="70b4b-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="70b4b-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="70b4b-114">Attributes</span></span>

<span data-ttu-id="70b4b-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="70b4b-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="70b4b-116">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="70b4b-116">Child elements</span></span>

<span data-ttu-id="70b4b-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="70b4b-117">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="70b4b-118">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="70b4b-118">Parent elements</span></span>

|<span data-ttu-id="70b4b-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="70b4b-119">**Element**</span></span>|<span data-ttu-id="70b4b-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="70b4b-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="70b4b-121">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="70b4b-121">ConversationAction</span></span>](conversationaction.md) <br/> |<span data-ttu-id="70b4b-122">Enthält eine einzelne Aktion auf einem einzelnen Gespräch angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="70b4b-122">Contains a single action to be applied to a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="70b4b-123">Textwert</span><span class="sxs-lookup"><span data-stu-id="70b4b-123">Text value</span></span>

<span data-ttu-id="70b4b-124">Der Textwert der der **ConversationLastSyncTime** gibt den letzten Zeitpunkt die Unterhaltung synchronisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="70b4b-124">The text value of the **ConversationLastSyncTime** indicates the last time the conversation was synchronized.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="70b4b-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="70b4b-125">Remarks</span></span>

<span data-ttu-id="70b4b-126">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="70b4b-126">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="70b4b-127">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="70b4b-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="70b4b-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="70b4b-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="70b4b-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="70b4b-129">Schema Name</span></span>  <br/> |<span data-ttu-id="70b4b-130">Schematypen</span><span class="sxs-lookup"><span data-stu-id="70b4b-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="70b4b-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="70b4b-131">Validation File</span></span>  <br/> |<span data-ttu-id="70b4b-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="70b4b-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="70b4b-133">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="70b4b-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="70b4b-134">False</span><span class="sxs-lookup"><span data-stu-id="70b4b-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="70b4b-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="70b4b-135">See also</span></span>



[<span data-ttu-id="70b4b-136">ApplyConversationAction-Vorgang</span><span class="sxs-lookup"><span data-stu-id="70b4b-136">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


- [<span data-ttu-id="70b4b-137">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="70b4b-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

