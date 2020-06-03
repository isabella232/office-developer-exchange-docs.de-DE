---
title: Action Type (ReminderActionType)
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0ffcdcf4-8ea3-483c-bb7f-0cd84126120c
description: Das Action Type-Element gibt die Aktion an, die für die Erinnerung erfolgen soll.
ms.openlocfilehash: 5c62b2dd945b23a5ff2bb824385c45dbc617a5a5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465058"
---
# <a name="actiontype-reminderactiontype"></a><span data-ttu-id="e1c78-103">Action Type (ReminderActionType)</span><span class="sxs-lookup"><span data-stu-id="e1c78-103">ActionType (ReminderActionType)</span></span>

<span data-ttu-id="e1c78-104">Das **Action** Type-Element gibt die Aktion an, die für die Erinnerung erfolgen soll.</span><span class="sxs-lookup"><span data-stu-id="e1c78-104">The **ActionType** element specifies the action to take on the reminder.</span></span> 
  
```XML
<ActionType> Dismiss | Snooze </ActionType>
```

 <span data-ttu-id="e1c78-105">**ReminderActionType**</span><span class="sxs-lookup"><span data-stu-id="e1c78-105">**ReminderActionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e1c78-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e1c78-106">Attributes and elements</span></span>

<span data-ttu-id="e1c78-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e1c78-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e1c78-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="e1c78-108">Attributes</span></span>

<span data-ttu-id="e1c78-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="e1c78-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e1c78-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e1c78-110">Child elements</span></span>

<span data-ttu-id="e1c78-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="e1c78-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e1c78-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e1c78-112">Parent elements</span></span>

[<span data-ttu-id="e1c78-113">ReminderItemAction</span><span class="sxs-lookup"><span data-stu-id="e1c78-113">ReminderItemAction</span></span>](reminderitemaction.md)
  
## <a name="text-value"></a><span data-ttu-id="e1c78-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="e1c78-114">Text value</span></span>

<span data-ttu-id="e1c78-115">Der Textwert des **Action** Type-Elements gibt die Aktion an, die für die Erinnerung erfolgen soll.</span><span class="sxs-lookup"><span data-stu-id="e1c78-115">The text value of the **ActionType** element specifies the action to take on the reminder.</span></span> <span data-ttu-id="e1c78-116">Der Textwert von **entlassen** gibt an, dass die Erinnerung geschlossen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e1c78-116">The text value of **Dismiss** indicates the reminder should be dismissed.</span></span> <span data-ttu-id="e1c78-117">Der Textwert von **Snooze** gibt an, dass die Erinnerung bis zu der durch das Element [Reminder](newremindertime.md) angegebenen zeitverzögert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e1c78-117">The text value of **Snooze** indicates that the reminder should be delayed until the time specified by the [NewReminderTime](newremindertime.md) element.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e1c78-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e1c78-118">Remarks</span></span>

<span data-ttu-id="e1c78-119">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="e1c78-119">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="e1c78-120">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="e1c78-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e1c78-121">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="e1c78-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e1c78-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="e1c78-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e1c78-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e1c78-123">Schema Name</span></span>  <br/> |<span data-ttu-id="e1c78-124">Schematypen</span><span class="sxs-lookup"><span data-stu-id="e1c78-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="e1c78-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e1c78-125">Validation File</span></span>  <br/> |<span data-ttu-id="e1c78-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e1c78-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e1c78-127">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="e1c78-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="e1c78-128">False</span><span class="sxs-lookup"><span data-stu-id="e1c78-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e1c78-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e1c78-129">See also</span></span>

- [<span data-ttu-id="e1c78-130">ReminderItemAction</span><span class="sxs-lookup"><span data-stu-id="e1c78-130">ReminderItemAction</span></span>](reminderitemaction.md)
- [<span data-ttu-id="e1c78-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="e1c78-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

