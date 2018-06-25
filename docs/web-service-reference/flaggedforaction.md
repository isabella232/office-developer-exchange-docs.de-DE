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
description: Das FlaggedForAction-Element gibt die Kennzeichen für den Aktionswert, die angezeigt werden, muss auf eingehende Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme anwenden.
ms.openlocfilehash: 5b6e714512edcf12ded2c04f414d047b8622d305
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758497"
---
# <a name="flaggedforaction"></a><span data-ttu-id="2c679-103">FlaggedForAction</span><span class="sxs-lookup"><span data-stu-id="2c679-103">FlaggedForAction</span></span>

<span data-ttu-id="2c679-104">Das **FlaggedForAction** -Element gibt die Kennzeichen für den Aktionswert, die angezeigt werden, muss auf eingehende Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme anwenden.</span><span class="sxs-lookup"><span data-stu-id="2c679-104">The **FlaggedForAction** element specifies the flag for action value that must appear on incoming messages in order for the condition or exception to apply.</span></span> 
  
```XML
<FlaggedForAction/>
```

 <span data-ttu-id="2c679-105">**FlaggedForActionType**</span><span class="sxs-lookup"><span data-stu-id="2c679-105">**FlaggedForActionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2c679-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="2c679-106">Attributes and elements</span></span>

<span data-ttu-id="2c679-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="2c679-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2c679-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="2c679-108">Attributes</span></span>

<span data-ttu-id="2c679-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="2c679-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2c679-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2c679-110">Child elements</span></span>

<span data-ttu-id="2c679-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="2c679-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2c679-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2c679-112">Parent elements</span></span>

|<span data-ttu-id="2c679-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="2c679-113">**Element**</span></span>|<span data-ttu-id="2c679-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2c679-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2c679-115">Bedingungen</span><span class="sxs-lookup"><span data-stu-id="2c679-115">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="2c679-116">Stellt die Bedingungen dar, bei deren Erfüllung die Regelaktionen für eine Regel ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="2c679-116">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="2c679-117">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="2c679-117">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="2c679-118">Stellt die Ausnahmen, die alle verfügbaren Regel Ausnahmebedingungen für eine Posteingangsregel darstellen.</span><span class="sxs-lookup"><span data-stu-id="2c679-118">Represents the exceptions that represent all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2c679-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="2c679-119">Text value</span></span>

<span data-ttu-id="2c679-120">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2c679-120">A text value is required.</span></span> <span data-ttu-id="2c679-121">Es folgen die möglichen Textwerte für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="2c679-121">The following are the possible text values for this element:</span></span>
  
- <span data-ttu-id="2c679-122">Jede</span><span class="sxs-lookup"><span data-stu-id="2c679-122">Any</span></span>
    
- <span data-ttu-id="2c679-123">Aufruf</span><span class="sxs-lookup"><span data-stu-id="2c679-123">Call</span></span>
    
- <span data-ttu-id="2c679-124">DoNotForward</span><span class="sxs-lookup"><span data-stu-id="2c679-124">DoNotForward</span></span>
    
- <span data-ttu-id="2c679-125">Nachverfolgung</span><span class="sxs-lookup"><span data-stu-id="2c679-125">FollowUp</span></span>
    
- <span data-ttu-id="2c679-126">FYI</span><span class="sxs-lookup"><span data-stu-id="2c679-126">FYI</span></span>
    
- <span data-ttu-id="2c679-127">Forward</span><span class="sxs-lookup"><span data-stu-id="2c679-127">Forward</span></span>
    
- <span data-ttu-id="2c679-128">NoResponseNecessary</span><span class="sxs-lookup"><span data-stu-id="2c679-128">NoResponseNecessary</span></span>
    
- <span data-ttu-id="2c679-129">Lesen</span><span class="sxs-lookup"><span data-stu-id="2c679-129">Read</span></span>
    
- <span data-ttu-id="2c679-130">Antworten</span><span class="sxs-lookup"><span data-stu-id="2c679-130">Reply</span></span>
    
- <span data-ttu-id="2c679-131">ReplyToAll</span><span class="sxs-lookup"><span data-stu-id="2c679-131">ReplyToAll</span></span>
    
- <span data-ttu-id="2c679-132">Überprüfung</span><span class="sxs-lookup"><span data-stu-id="2c679-132">Review</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2c679-133">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2c679-133">Remarks</span></span>

<span data-ttu-id="2c679-134">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="2c679-134">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2c679-135">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="2c679-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2c679-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="2c679-136">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2c679-137">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="2c679-137">Schema Name</span></span>  <br/> |<span data-ttu-id="2c679-138">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="2c679-138">Messages schema</span></span>  <br/> |
|<span data-ttu-id="2c679-139">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="2c679-139">Validation File</span></span>  <br/> |<span data-ttu-id="2c679-140">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="2c679-140">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2c679-141">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="2c679-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="2c679-142">True</span><span class="sxs-lookup"><span data-stu-id="2c679-142">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2c679-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2c679-143">See also</span></span>



- [<span data-ttu-id="2c679-144">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="2c679-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

