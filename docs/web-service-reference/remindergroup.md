---
title: ReminderGroup
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3e23c2a1-05d8-4fec-897c-f684a5b97e4c
description: Das ReminderGroup-Element gibt an, ob die Erinnerung für ein Kalenderelement oder einer Aufgabe ist.
ms.openlocfilehash: d9d31cdab482d04149428021ad44cc742108053a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831060"
---
# <a name="remindergroup"></a><span data-ttu-id="df6cc-103">ReminderGroup</span><span class="sxs-lookup"><span data-stu-id="df6cc-103">ReminderGroup</span></span>

<span data-ttu-id="df6cc-104">Das **ReminderGroup** -Element gibt an, ob die Erinnerung für ein Kalenderelement oder einer Aufgabe ist.</span><span class="sxs-lookup"><span data-stu-id="df6cc-104">The **ReminderGroup** element specifies whether the reminder is for a calendar item or a task.</span></span> 
  
```XML
<ReminderGroup> Calendar | Task </ReminderGroup>
```

 <span data-ttu-id="df6cc-105">**ReminderGroupType**</span><span class="sxs-lookup"><span data-stu-id="df6cc-105">**ReminderGroupType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="df6cc-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="df6cc-106">Attributes and elements</span></span>

<span data-ttu-id="df6cc-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="df6cc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="df6cc-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="df6cc-108">Attributes</span></span>

<span data-ttu-id="df6cc-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="df6cc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="df6cc-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="df6cc-110">Child elements</span></span>

<span data-ttu-id="df6cc-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="df6cc-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="df6cc-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="df6cc-112">Parent elements</span></span>

[<span data-ttu-id="df6cc-113">Reminder</span><span class="sxs-lookup"><span data-stu-id="df6cc-113">Reminder</span></span>](reminder.md)
  
## <a name="text-value"></a><span data-ttu-id="df6cc-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="df6cc-114">Text value</span></span>

<span data-ttu-id="df6cc-115">Der Textwert des **ReminderGroup** -Elements ist die Gruppentyp der Erinnerung.</span><span class="sxs-lookup"><span data-stu-id="df6cc-115">The text value of the **ReminderGroup** element is the group type of the reminder.</span></span> <span data-ttu-id="df6cc-116">Der Textwert der **Kalender** gibt an, dass die Erinnerung für ein Kalenderelement ist.</span><span class="sxs-lookup"><span data-stu-id="df6cc-116">The text value of **Calendar** specifies that the reminder is for a calendar item.</span></span> <span data-ttu-id="df6cc-117">Der Textwert der **Aufgabe** gibt an, dass die Erinnerung für ein Aufgabenelement ist.</span><span class="sxs-lookup"><span data-stu-id="df6cc-117">The text value of **Task** specifies that the reminder is for a task item.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="df6cc-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="df6cc-118">Remarks</span></span>

<span data-ttu-id="df6cc-119">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="df6cc-119">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="df6cc-120">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="df6cc-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="df6cc-121">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="df6cc-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="df6cc-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="df6cc-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="df6cc-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="df6cc-123">Schema Name</span></span>  <br/> |<span data-ttu-id="df6cc-124">Schematypen</span><span class="sxs-lookup"><span data-stu-id="df6cc-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="df6cc-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="df6cc-125">Validation File</span></span>  <br/> |<span data-ttu-id="df6cc-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="df6cc-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="df6cc-127">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="df6cc-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="df6cc-128">False</span><span class="sxs-lookup"><span data-stu-id="df6cc-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="df6cc-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="df6cc-129">See also</span></span>



[<span data-ttu-id="df6cc-130">Reminder</span><span class="sxs-lookup"><span data-stu-id="df6cc-130">Reminder</span></span>](reminder.md)


- [<span data-ttu-id="df6cc-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="df6cc-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

