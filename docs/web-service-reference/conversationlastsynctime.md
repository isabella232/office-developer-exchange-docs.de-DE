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
description: Das ConversationLastSyncTime-Element enthält das Datum und die Uhrzeit, zu der eine Unterhaltung zuletzt synchronisiert wurde. Dieses Element muss vorhanden sein, wenn Sie versuchen, alle Elemente in einer Unterhaltung zu löschen, die bis zur angegebenen Zeit empfangen wurden.
ms.openlocfilehash: f7cc6e205ab9936685d7b8c1f34129b799a53021
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461429"
---
# <a name="conversationlastsynctime"></a><span data-ttu-id="a8487-104">ConversationLastSyncTime</span><span class="sxs-lookup"><span data-stu-id="a8487-104">ConversationLastSyncTime</span></span>

<span data-ttu-id="a8487-105">Das **ConversationLastSyncTime** -Element enthält das Datum und die Uhrzeit, zu der eine Unterhaltung zuletzt synchronisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="a8487-105">The **ConversationLastSyncTime** element contains the date and time that a conversation was last synchronized.</span></span> <span data-ttu-id="a8487-106">Dieses Element muss vorhanden sein, wenn Sie versuchen, alle Elemente in einer Unterhaltung zu löschen, die bis zur angegebenen Zeit empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="a8487-106">This element must be present when trying to delete all items in a conversation that were received up to the specified time.</span></span> 
  
[<span data-ttu-id="a8487-107">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="a8487-107">ApplyConversationAction</span></span>](applyconversationaction.md)
  
[<span data-ttu-id="a8487-108">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="a8487-108">ConversationActions</span></span>](conversationactions.md)
  
[<span data-ttu-id="a8487-109">Unterhaltung</span><span class="sxs-lookup"><span data-stu-id="a8487-109">ConversationAction</span></span>](conversationaction.md)
  
[<span data-ttu-id="a8487-110">ConversationLastSyncTime</span><span class="sxs-lookup"><span data-stu-id="a8487-110">ConversationLastSyncTime</span></span>](conversationlastsynctime.md)
  
```XML
<ConversationLastSyncTime/>
```

 <span data-ttu-id="a8487-111">**xs: DateTime**</span><span class="sxs-lookup"><span data-stu-id="a8487-111">**xs:dateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a8487-112">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a8487-112">Attributes and elements</span></span>

<span data-ttu-id="a8487-113">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a8487-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a8487-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="a8487-114">Attributes</span></span>

<span data-ttu-id="a8487-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="a8487-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a8487-116">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a8487-116">Child elements</span></span>

<span data-ttu-id="a8487-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="a8487-117">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a8487-118">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a8487-118">Parent elements</span></span>

|<span data-ttu-id="a8487-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="a8487-119">**Element**</span></span>|<span data-ttu-id="a8487-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a8487-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a8487-121">Unterhaltung</span><span class="sxs-lookup"><span data-stu-id="a8487-121">ConversationAction</span></span>](conversationaction.md) <br/> |<span data-ttu-id="a8487-122">Enthält eine einzelne Aktion, die auf eine einzelne Unterhaltung angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a8487-122">Contains a single action to be applied to a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a8487-123">Textwert</span><span class="sxs-lookup"><span data-stu-id="a8487-123">Text value</span></span>

<span data-ttu-id="a8487-124">Der Textwert des **ConversationLastSyncTime** gibt an, wann die Unterhaltung zuletzt synchronisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="a8487-124">The text value of the **ConversationLastSyncTime** indicates the last time the conversation was synchronized.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a8487-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a8487-125">Remarks</span></span>

<span data-ttu-id="a8487-126">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="a8487-126">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a8487-127">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="a8487-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a8487-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="a8487-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a8487-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a8487-129">Schema Name</span></span>  <br/> |<span data-ttu-id="a8487-130">Schematypen</span><span class="sxs-lookup"><span data-stu-id="a8487-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="a8487-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a8487-131">Validation File</span></span>  <br/> |<span data-ttu-id="a8487-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a8487-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a8487-133">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="a8487-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="a8487-134">False</span><span class="sxs-lookup"><span data-stu-id="a8487-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a8487-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a8487-135">See also</span></span>



[<span data-ttu-id="a8487-136">ApplyConversationAction-Vorgang</span><span class="sxs-lookup"><span data-stu-id="a8487-136">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


- [<span data-ttu-id="a8487-137">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="a8487-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

