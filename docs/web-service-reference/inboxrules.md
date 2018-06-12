---
title: InboxRules
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- InboxRules
api_type:
- schema
ms.assetid: 7bb9896c-bd12-49ae-842a-a10b5f9a2ef6
description: Das InboxRules -Element stellt ein Array von Regeln in das Postfach des Benutzers.
ms.openlocfilehash: 47fcad5dde06f3af9fbae7e70adbfd8b225081c2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19829899"
---
# <a name="inboxrules"></a><span data-ttu-id="ec46f-103">InboxRules</span><span class="sxs-lookup"><span data-stu-id="ec46f-103">InboxRules</span></span>

<span data-ttu-id="ec46f-104">Das **InboxRules** -Element stellt ein Array von Regeln in das Postfach des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="ec46f-104">The **InboxRules** element represents an array of rules in the user's mailbox.</span></span> 
  
[<span data-ttu-id="ec46f-105">GetInboxRulesResponse</span><span class="sxs-lookup"><span data-stu-id="ec46f-105">GetInboxRulesResponse</span></span>](getinboxrulesresponse.md)
  
[<span data-ttu-id="ec46f-106">InboxRules</span><span class="sxs-lookup"><span data-stu-id="ec46f-106">InboxRules</span></span>](inboxrules.md)
  
```XML
<InboxRules>
   <Rule/>
</InboxRules>
```

 <span data-ttu-id="ec46f-107">**ArrayOfRulesType**</span><span class="sxs-lookup"><span data-stu-id="ec46f-107">**ArrayOfRulesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ec46f-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ec46f-108">Attributes and elements</span></span>

<span data-ttu-id="ec46f-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ec46f-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ec46f-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="ec46f-110">Attributes</span></span>

<span data-ttu-id="ec46f-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="ec46f-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ec46f-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ec46f-112">Child elements</span></span>

|<span data-ttu-id="ec46f-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="ec46f-113">**Element**</span></span>|<span data-ttu-id="ec46f-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ec46f-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ec46f-115">Regel (RuleType)</span><span class="sxs-lookup"><span data-stu-id="ec46f-115">Rule (RuleType)</span></span>](rule-ruletype.md) <br/> |<span data-ttu-id="ec46f-116">Enthält eine einzelne Regel und stellt eine Regel in das Postfach des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="ec46f-116">Contains a single rule and represents a rule in the user's mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ec46f-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ec46f-117">Parent elements</span></span>

|<span data-ttu-id="ec46f-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="ec46f-118">**Element**</span></span>|<span data-ttu-id="ec46f-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ec46f-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ec46f-120">GetInboxRulesResponse</span><span class="sxs-lookup"><span data-stu-id="ec46f-120">GetInboxRulesResponse</span></span>](getinboxrulesresponse.md) <br/> |<span data-ttu-id="ec46f-121">Definiert eine Antwort auf eine [GetInboxRules-Vorgang](getinboxrules-operation.md) an.</span><span class="sxs-lookup"><span data-stu-id="ec46f-121">Defines a response to a [GetInboxRules operation](getinboxrules-operation.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ec46f-122">Textwert</span><span class="sxs-lookup"><span data-stu-id="ec46f-122">Text value</span></span>

<span data-ttu-id="ec46f-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="ec46f-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ec46f-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ec46f-124">Remarks</span></span>

<span data-ttu-id="ec46f-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="ec46f-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ec46f-126">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="ec46f-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ec46f-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="ec46f-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ec46f-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ec46f-128">Schema Name</span></span>  <br/> |<span data-ttu-id="ec46f-129">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="ec46f-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ec46f-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ec46f-130">Validation File</span></span>  <br/> |<span data-ttu-id="ec46f-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ec46f-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ec46f-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="ec46f-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="ec46f-133">True</span><span class="sxs-lookup"><span data-stu-id="ec46f-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ec46f-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ec46f-134">See also</span></span>



[<span data-ttu-id="ec46f-135">GetInboxRules</span><span class="sxs-lookup"><span data-stu-id="ec46f-135">GetInboxRules</span></span>](getinboxrules.md)
  
[<span data-ttu-id="ec46f-136">GetInboxRules-Vorgang</span><span class="sxs-lookup"><span data-stu-id="ec46f-136">GetInboxRules operation</span></span>](getinboxrules-operation.md)


- [<span data-ttu-id="ec46f-137">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="ec46f-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

