---
title: Erinnerung
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 54dd748a-23a5-4ea2-88f2-b74c68a3c48f
description: Das Reminder-Element gibt eine Erinnerung für eine Aufgabe oder ein Kalenderelement an.
ms.openlocfilehash: 71e54d920a169b8060d22bb7d7d294208c344c2e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457487"
---
# <a name="reminder"></a><span data-ttu-id="d077c-103">Erinnerung</span><span class="sxs-lookup"><span data-stu-id="d077c-103">Reminder</span></span>

<span data-ttu-id="d077c-104">Das **Reminder** -Element gibt eine Erinnerung für eine Aufgabe oder ein Kalenderelement an.</span><span class="sxs-lookup"><span data-stu-id="d077c-104">The **Reminder** element specifies a reminder for a task or a calendar item.</span></span> 
  
```XML
<Reminder>
   <Subject></Subject>
   <Location></Location>
   <ReminderTime></ReminderTime>
   <StartDate></StartDate>
   <EndDate></EndDate>
   <ItemId></ItemId>
   <RecurringMasterItemId></RecurringMasterItemId>
   <ReminderGroup></ReminderGroup>
   <UID></UID>
</Reminder>

```

 <span data-ttu-id="d077c-105">**Reminder**</span><span class="sxs-lookup"><span data-stu-id="d077c-105">**ReminderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d077c-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d077c-106">Attributes and elements</span></span>

<span data-ttu-id="d077c-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d077c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d077c-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d077c-108">Attributes</span></span>

<span data-ttu-id="d077c-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="d077c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d077c-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d077c-110">Child elements</span></span>

<span data-ttu-id="d077c-111">[Betreff](subject.md)  |  [Speicherort](location.md)  |  [Erinnerungsfunktion](remindertime.md)  |  [StartDate](startdate.md)  |  [EndDate (Reminder)](enddate-remindertype.md)  |  [ItemID](itemid.md)  |  [RecurringMasterItemId (itemidtype)](recurringmasteritemid-itemidtype.md)  |  [Reminder](remindergroup.md)  |  [UID](uid.md)</span><span class="sxs-lookup"><span data-stu-id="d077c-111">[Subject](subject.md) | [Location](location.md) | [ReminderTime](remindertime.md) | [StartDate](startdate.md) | [EndDate (ReminderType)](enddate-remindertype.md) | [ItemId](itemid.md) | [RecurringMasterItemId (ItemIdType)](recurringmasteritemid-itemidtype.md) | [ReminderGroup](remindergroup.md) | [UID](uid.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d077c-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d077c-112">Parent elements</span></span>

[<span data-ttu-id="d077c-113">Reminders</span><span class="sxs-lookup"><span data-stu-id="d077c-113">Reminders</span></span>](reminders.md)
  
## <a name="remarks"></a><span data-ttu-id="d077c-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d077c-114">Remarks</span></span>

<span data-ttu-id="d077c-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d077c-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="d077c-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="d077c-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d077c-117">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="d077c-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d077c-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="d077c-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d077c-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d077c-119">Schema Name</span></span>  <br/> |<span data-ttu-id="d077c-120">Schematypen</span><span class="sxs-lookup"><span data-stu-id="d077c-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="d077c-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d077c-121">Validation File</span></span>  <br/> |<span data-ttu-id="d077c-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d077c-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d077c-123">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d077c-123">Can be Empty</span></span>  <br/> |<span data-ttu-id="d077c-124">False</span><span class="sxs-lookup"><span data-stu-id="d077c-124">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d077c-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d077c-125">See also</span></span>



[<span data-ttu-id="d077c-126">Reminders</span><span class="sxs-lookup"><span data-stu-id="d077c-126">Reminders</span></span>](reminders.md)


- [<span data-ttu-id="d077c-127">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="d077c-127">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

