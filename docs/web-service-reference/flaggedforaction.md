---
title: FlaggedForAction
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FlaggedForAction
api_type:
- schema
ms.assetid: 6a08c48a-7b32-4754-8940-adbda55e8133
description: Das FlaggedForAction-Element gibt das Flag für Action-Wert an, das in eingehenden Nachrichten angezeigt werden muss, damit die Bedingung oder Ausnahme zutrifft.
ms.openlocfilehash: f996dc4bcf30db32e1d73fb302ab137f0a6ad4d4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466241"
---
# <a name="flaggedforaction"></a><span data-ttu-id="a785d-103">FlaggedForAction</span><span class="sxs-lookup"><span data-stu-id="a785d-103">FlaggedForAction</span></span>

<span data-ttu-id="a785d-104">Das **FlaggedForAction** -Element gibt das Flag für Action-Wert an, das in eingehenden Nachrichten angezeigt werden muss, damit die Bedingung oder Ausnahme zutrifft.</span><span class="sxs-lookup"><span data-stu-id="a785d-104">The **FlaggedForAction** element specifies the flag for action value that must appear on incoming messages in order for the condition or exception to apply.</span></span> 
  
```XML
<FlaggedForAction/>
```

 <span data-ttu-id="a785d-105">**FlaggedForActionType**</span><span class="sxs-lookup"><span data-stu-id="a785d-105">**FlaggedForActionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a785d-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a785d-106">Attributes and elements</span></span>

<span data-ttu-id="a785d-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a785d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a785d-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="a785d-108">Attributes</span></span>

<span data-ttu-id="a785d-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="a785d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a785d-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a785d-110">Child elements</span></span>

<span data-ttu-id="a785d-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="a785d-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a785d-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a785d-112">Parent elements</span></span>

|<span data-ttu-id="a785d-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="a785d-113">**Element**</span></span>|<span data-ttu-id="a785d-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a785d-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a785d-115">Bedingungen</span><span class="sxs-lookup"><span data-stu-id="a785d-115">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="a785d-116">Stellt die Bedingungen dar, bei deren Erfüllung die Regelaktionen für eine Regel ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="a785d-116">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="a785d-117">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="a785d-117">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="a785d-118">Stellt die Ausnahmen, die alle verfügbaren Regel Ausnahmebedingungen für eine Posteingangsregel darstellen.</span><span class="sxs-lookup"><span data-stu-id="a785d-118">Represents the exceptions that represent all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a785d-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="a785d-119">Text value</span></span>

<span data-ttu-id="a785d-120">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a785d-120">A text value is required.</span></span> <span data-ttu-id="a785d-121">Im folgenden sind die möglichen Text Werte für dieses Element angegeben:</span><span class="sxs-lookup"><span data-stu-id="a785d-121">The following are the possible text values for this element:</span></span>
  
- <span data-ttu-id="a785d-122">Any</span><span class="sxs-lookup"><span data-stu-id="a785d-122">Any</span></span>
    
- <span data-ttu-id="a785d-123">Anruf</span><span class="sxs-lookup"><span data-stu-id="a785d-123">Call</span></span>
    
- <span data-ttu-id="a785d-124">DoNotForward</span><span class="sxs-lookup"><span data-stu-id="a785d-124">DoNotForward</span></span>
    
- <span data-ttu-id="a785d-125">FollowUp</span><span class="sxs-lookup"><span data-stu-id="a785d-125">FollowUp</span></span>
    
- <span data-ttu-id="a785d-126">FYI</span><span class="sxs-lookup"><span data-stu-id="a785d-126">FYI</span></span>
    
- <span data-ttu-id="a785d-127">Weiterleiten</span><span class="sxs-lookup"><span data-stu-id="a785d-127">Forward</span></span>
    
- <span data-ttu-id="a785d-128">NoResponseNecessary</span><span class="sxs-lookup"><span data-stu-id="a785d-128">NoResponseNecessary</span></span>
    
- <span data-ttu-id="a785d-129">Read</span><span class="sxs-lookup"><span data-stu-id="a785d-129">Read</span></span>
    
- <span data-ttu-id="a785d-130">Antworten</span><span class="sxs-lookup"><span data-stu-id="a785d-130">Reply</span></span>
    
- <span data-ttu-id="a785d-131">ReplyToAll</span><span class="sxs-lookup"><span data-stu-id="a785d-131">ReplyToAll</span></span>
    
- <span data-ttu-id="a785d-132">Überprüfung</span><span class="sxs-lookup"><span data-stu-id="a785d-132">Review</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a785d-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a785d-133">Remarks</span></span>

<span data-ttu-id="a785d-134">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="a785d-134">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a785d-135">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="a785d-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a785d-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="a785d-136">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a785d-137">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a785d-137">Schema Name</span></span>  <br/> |<span data-ttu-id="a785d-138">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="a785d-138">Messages schema</span></span>  <br/> |
|<span data-ttu-id="a785d-139">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a785d-139">Validation File</span></span>  <br/> |<span data-ttu-id="a785d-140">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="a785d-140">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a785d-141">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="a785d-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="a785d-142">True</span><span class="sxs-lookup"><span data-stu-id="a785d-142">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a785d-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a785d-143">See also</span></span>



- [<span data-ttu-id="a785d-144">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="a785d-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

