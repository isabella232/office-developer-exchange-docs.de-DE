---
title: Neuerinnerung
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ff1b6b1c-3557-41d4-8aa6-9528fdb3a21a
description: Das Element Reminder gibt eine neue Zeit für eine Erinnerung an.
ms.openlocfilehash: a10f7e481b474501f33dba4c09060766568952b0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465954"
---
# <a name="newremindertime"></a><span data-ttu-id="881df-103">Neuerinnerung</span><span class="sxs-lookup"><span data-stu-id="881df-103">NewReminderTime</span></span>

<span data-ttu-id="881df-104">Das Element **Reminder** gibt eine neue Zeit für eine Erinnerung an.</span><span class="sxs-lookup"><span data-stu-id="881df-104">The **NewReminderTime** element specifies a new time for a reminder.</span></span> 
  
```XML
<NewReminderTime/>
```

 <span data-ttu-id="881df-105">**Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="881df-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="881df-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="881df-106">Attributes and elements</span></span>

<span data-ttu-id="881df-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="881df-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="881df-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="881df-108">Attributes</span></span>

<span data-ttu-id="881df-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="881df-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="881df-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="881df-110">Child elements</span></span>

<span data-ttu-id="881df-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="881df-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="881df-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="881df-112">Parent elements</span></span>

[<span data-ttu-id="881df-113">ReminderItemAction</span><span class="sxs-lookup"><span data-stu-id="881df-113">ReminderItemAction</span></span>](reminderitemaction.md)
  
## <a name="text-value"></a><span data-ttu-id="881df-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="881df-114">Text value</span></span>

<span data-ttu-id="881df-115">Der Textwert des Elements **Reminder** ist eine neue Zeit für die Erinnerung.</span><span class="sxs-lookup"><span data-stu-id="881df-115">The text value of the **NewReminderTime** element is a new time for the reminder.</span></span> <span data-ttu-id="881df-116">Das Element **Reminder** wird verwendet, wenn das [Action](actiontype-reminderactiontype.md) Type-Element auf **Snooze**festgelegt ist, um die Erinnerung zu verzögern.</span><span class="sxs-lookup"><span data-stu-id="881df-116">The **NewReminderTime** element is used when the [ActionType](actiontype-reminderactiontype.md) element is set to **Snooze**, in order to delay the reminder.</span></span> <span data-ttu-id="881df-117">Der Wert der **Reminder** -Uhrzeit muss größer sein als die von der [geterinnerungs-Operation](getreminders-operation.md)zurückgegebene [Erinnerungszeit](remindertime.md) .</span><span class="sxs-lookup"><span data-stu-id="881df-117">The value of the **NewReminderTime** must be greater than the [ReminderTime](remindertime.md) returned by the [GetReminders operation](getreminders-operation.md).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="881df-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="881df-118">Remarks</span></span>

<span data-ttu-id="881df-119">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="881df-119">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="881df-120">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="881df-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="881df-121">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="881df-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="881df-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="881df-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="881df-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="881df-123">Schema Name</span></span>  <br/> |<span data-ttu-id="881df-124">Schematypen</span><span class="sxs-lookup"><span data-stu-id="881df-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="881df-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="881df-125">Validation File</span></span>  <br/> |<span data-ttu-id="881df-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="881df-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="881df-127">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="881df-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="881df-128">False</span><span class="sxs-lookup"><span data-stu-id="881df-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="881df-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="881df-129">See also</span></span>



[<span data-ttu-id="881df-130">ReminderItemAction</span><span class="sxs-lookup"><span data-stu-id="881df-130">ReminderItemAction</span></span>](reminderitemaction.md)


- [<span data-ttu-id="881df-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="881df-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

