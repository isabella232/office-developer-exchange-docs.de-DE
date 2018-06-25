---
title: NewReminderTime
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ff1b6b1c-3557-41d4-8aa6-9528fdb3a21a
description: Das NewReminderTime-Element gibt eine neue Zeit für eine Erinnerung.
ms.openlocfilehash: 9f3f509942c673c916cc646cd9519240aef6ea06
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830531"
---
# <a name="newremindertime"></a><span data-ttu-id="f74aa-103">NewReminderTime</span><span class="sxs-lookup"><span data-stu-id="f74aa-103">NewReminderTime</span></span>

<span data-ttu-id="f74aa-104">Das **NewReminderTime** -Element gibt eine neue Zeit für eine Erinnerung.</span><span class="sxs-lookup"><span data-stu-id="f74aa-104">The **NewReminderTime** element specifies a new time for a reminder.</span></span> 
  
```XML
<NewReminderTime/>
```

 <span data-ttu-id="f74aa-105">**string**</span><span class="sxs-lookup"><span data-stu-id="f74aa-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f74aa-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f74aa-106">Attributes and elements</span></span>

<span data-ttu-id="f74aa-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f74aa-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f74aa-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="f74aa-108">Attributes</span></span>

<span data-ttu-id="f74aa-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="f74aa-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f74aa-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f74aa-110">Child elements</span></span>

<span data-ttu-id="f74aa-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="f74aa-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f74aa-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f74aa-112">Parent elements</span></span>

[<span data-ttu-id="f74aa-113">ReminderItemAction</span><span class="sxs-lookup"><span data-stu-id="f74aa-113">ReminderItemAction</span></span>](reminderitemaction.md)
  
## <a name="text-value"></a><span data-ttu-id="f74aa-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="f74aa-114">Text value</span></span>

<span data-ttu-id="f74aa-115">Der Textwert der **NewReminderTime** -Element ist ein neues Zeitintervall für die Erinnerung.</span><span class="sxs-lookup"><span data-stu-id="f74aa-115">The text value of the **NewReminderTime** element is a new time for the reminder.</span></span> <span data-ttu-id="f74aa-116">Das **NewReminderTime** -Element wird verwendet, wenn das [ActionType](actiontype-reminderactiontype.md) -Element, um die Erinnerung verzögert **erneut erinnern**, festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f74aa-116">The **NewReminderTime** element is used when the [ActionType](actiontype-reminderactiontype.md) element is set to **Snooze**, in order to delay the reminder.</span></span> <span data-ttu-id="f74aa-117">Der Wert der **NewReminderTime** muss größer als der durch die [GetReminders Vorgang](getreminders-operation.md)zurückgegebenen [ReminderTime](remindertime.md) sein.</span><span class="sxs-lookup"><span data-stu-id="f74aa-117">The value of the **NewReminderTime** must be greater than the [ReminderTime](remindertime.md) returned by the [GetReminders operation](getreminders-operation.md).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f74aa-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f74aa-118">Remarks</span></span>

<span data-ttu-id="f74aa-119">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="f74aa-119">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="f74aa-120">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="f74aa-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f74aa-121">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="f74aa-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f74aa-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="f74aa-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f74aa-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f74aa-123">Schema Name</span></span>  <br/> |<span data-ttu-id="f74aa-124">Schematypen</span><span class="sxs-lookup"><span data-stu-id="f74aa-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="f74aa-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f74aa-125">Validation File</span></span>  <br/> |<span data-ttu-id="f74aa-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f74aa-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f74aa-127">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="f74aa-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="f74aa-128">False</span><span class="sxs-lookup"><span data-stu-id="f74aa-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f74aa-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f74aa-129">See also</span></span>



[<span data-ttu-id="f74aa-130">ReminderItemAction</span><span class="sxs-lookup"><span data-stu-id="f74aa-130">ReminderItemAction</span></span>](reminderitemaction.md)


- [<span data-ttu-id="f74aa-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="f74aa-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

