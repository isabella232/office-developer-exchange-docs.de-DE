---
title: Reminder
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bfaf84eb-271a-4728-84fc-a20205a100bd
description: Das Reminder-Element gibt den Typ der Erinnerungen an, die zurückgegeben werden sollen.
ms.openlocfilehash: 4ac20143bbfb29fb8f962515f2faba224b2f973f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465527"
---
# <a name="remindertype"></a><span data-ttu-id="79ec5-103">Reminder</span><span class="sxs-lookup"><span data-stu-id="79ec5-103">ReminderType</span></span>

<span data-ttu-id="79ec5-104">Das **Reminder** -Element gibt den Typ der Erinnerungen an, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="79ec5-104">The **ReminderType** element specifies the type of reminders to return.</span></span> 
  
```XML
<ReminderType> All | Current | Old </ReminderType>
```

 <span data-ttu-id="79ec5-105">**Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="79ec5-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="79ec5-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="79ec5-106">Attributes and elements</span></span>

<span data-ttu-id="79ec5-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="79ec5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="79ec5-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="79ec5-108">Attributes</span></span>

<span data-ttu-id="79ec5-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="79ec5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="79ec5-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="79ec5-110">Child elements</span></span>

<span data-ttu-id="79ec5-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="79ec5-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="79ec5-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="79ec5-112">Parent elements</span></span>

[<span data-ttu-id="79ec5-113">GetReminders</span><span class="sxs-lookup"><span data-stu-id="79ec5-113">GetReminders</span></span>](getreminders.md)
  
## <a name="text-value"></a><span data-ttu-id="79ec5-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="79ec5-114">Text value</span></span>

<span data-ttu-id="79ec5-115">Der Textwert des **Reminder** -Elements ist der Typ der Erinnerungen, die zurückgegeben werden sollen, entweder **all**, **Current**oder **Old**.</span><span class="sxs-lookup"><span data-stu-id="79ec5-115">The text value of the **ReminderType** element is the type of reminders to return, either **All**, **Current**, or **Old**.</span></span> <span data-ttu-id="79ec5-116">**All** ist der empfohlene Wert für dieses Element.</span><span class="sxs-lookup"><span data-stu-id="79ec5-116">**All** is the recommended value for this element.</span></span> <span data-ttu-id="79ec5-117">Weitere Informationen zur Beziehung zwischen dem **Reminder** -Element und den Elementen [BeginTime](begintime.md) und [EndTime](endtime-remindermessagedatatype.md) finden Sie unter [getmahnte-Vorgang](getreminders-operation.md).</span><span class="sxs-lookup"><span data-stu-id="79ec5-117">For more information about the relationship between the **ReminderType** element and the [BeginTime](begintime.md) and [EndTime](endtime-remindermessagedatatype.md) elements, see [GetReminders operation](getreminders-operation.md).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="79ec5-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="79ec5-118">Remarks</span></span>

<span data-ttu-id="79ec5-119">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="79ec5-119">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="79ec5-120">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="79ec5-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="79ec5-121">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="79ec5-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="79ec5-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="79ec5-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="79ec5-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="79ec5-123">Schema Name</span></span>  <br/> |<span data-ttu-id="79ec5-124">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="79ec5-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="79ec5-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="79ec5-125">Validation File</span></span>  <br/> |<span data-ttu-id="79ec5-126">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="79ec5-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="79ec5-127">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="79ec5-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="79ec5-128">False</span><span class="sxs-lookup"><span data-stu-id="79ec5-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="79ec5-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="79ec5-129">See also</span></span>



[<span data-ttu-id="79ec5-130">GetReminders</span><span class="sxs-lookup"><span data-stu-id="79ec5-130">GetReminders</span></span>](getreminders.md)


- [<span data-ttu-id="79ec5-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="79ec5-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

