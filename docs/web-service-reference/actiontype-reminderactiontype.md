---
title: ActionType (ReminderActionType)
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0ffcdcf4-8ea3-483c-bb7f-0cd84126120c
description: ActionType-Element gibt die durchzuführende Aktion auf die Erinnerung an.
ms.openlocfilehash: 361259f733756995fae2c2c2390013a728e475a4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757211"
---
# <a name="actiontype-reminderactiontype"></a><span data-ttu-id="289aa-103">ActionType (ReminderActionType)</span><span class="sxs-lookup"><span data-stu-id="289aa-103">ActionType (ReminderActionType)</span></span>

<span data-ttu-id="289aa-104">**ActionType** -Element gibt die durchzuführende Aktion auf die Erinnerung an.</span><span class="sxs-lookup"><span data-stu-id="289aa-104">The **ActionType** element specifies the action to take on the reminder.</span></span> 
  
```XML
<ActionType> Dismiss | Snooze </ActionType>
```

 <span data-ttu-id="289aa-105">**ReminderActionType**</span><span class="sxs-lookup"><span data-stu-id="289aa-105">**ReminderActionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="289aa-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="289aa-106">Attributes and elements</span></span>

<span data-ttu-id="289aa-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="289aa-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="289aa-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="289aa-108">Attributes</span></span>

<span data-ttu-id="289aa-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="289aa-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="289aa-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="289aa-110">Child elements</span></span>

<span data-ttu-id="289aa-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="289aa-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="289aa-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="289aa-112">Parent elements</span></span>

[<span data-ttu-id="289aa-113">ReminderItemAction</span><span class="sxs-lookup"><span data-stu-id="289aa-113">ReminderItemAction</span></span>](reminderitemaction.md)
  
## <a name="text-value"></a><span data-ttu-id="289aa-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="289aa-114">Text value</span></span>

<span data-ttu-id="289aa-115">Der Textwert der **ActionType** -Element gibt die durchzuführende Aktion auf die Erinnerung an.</span><span class="sxs-lookup"><span data-stu-id="289aa-115">The text value of the **ActionType** element specifies the action to take on the reminder.</span></span> <span data-ttu-id="289aa-116">Der Textwert der **Dismiss** gibt an, dass die Erinnerung geschlossen werden soll.</span><span class="sxs-lookup"><span data-stu-id="289aa-116">The text value of **Dismiss** indicates the reminder should be dismissed.</span></span> <span data-ttu-id="289aa-117">Der Textwert der **erneut erinnern** gibt an, dass die Erinnerung soll, bis die Zeit, die durch das [NewReminderTime](newremindertime.md) -Element angegeben verzögert werden.</span><span class="sxs-lookup"><span data-stu-id="289aa-117">The text value of **Snooze** indicates that the reminder should be delayed until the time specified by the [NewReminderTime](newremindertime.md) element.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="289aa-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="289aa-118">Remarks</span></span>

<span data-ttu-id="289aa-119">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="289aa-119">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="289aa-120">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="289aa-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="289aa-121">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="289aa-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="289aa-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="289aa-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="289aa-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="289aa-123">Schema Name</span></span>  <br/> |<span data-ttu-id="289aa-124">Schematypen</span><span class="sxs-lookup"><span data-stu-id="289aa-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="289aa-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="289aa-125">Validation File</span></span>  <br/> |<span data-ttu-id="289aa-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="289aa-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="289aa-127">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="289aa-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="289aa-128">False</span><span class="sxs-lookup"><span data-stu-id="289aa-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="289aa-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="289aa-129">See also</span></span>

- [<span data-ttu-id="289aa-130">ReminderItemAction</span><span class="sxs-lookup"><span data-stu-id="289aa-130">ReminderItemAction</span></span>](reminderitemaction.md)
- [<span data-ttu-id="289aa-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="289aa-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

