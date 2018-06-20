---
title: ReminderType
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bfaf84eb-271a-4728-84fc-a20205a100bd
description: Das ReminderType-Element gibt den Typ des zurückzugebenden Erinnerungen.
ms.openlocfilehash: 11739d2068a1009b2840b2169e86b113151cbfa9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831077"
---
# <a name="remindertype"></a><span data-ttu-id="3c758-103">ReminderType</span><span class="sxs-lookup"><span data-stu-id="3c758-103">ReminderType</span></span>

<span data-ttu-id="3c758-104">Das **ReminderType** -Element gibt den Typ des zurückzugebenden Erinnerungen.</span><span class="sxs-lookup"><span data-stu-id="3c758-104">The **ReminderType** element specifies the type of reminders to return.</span></span> 
  
```XML
<ReminderType> All | Current | Old </ReminderType>
```

 <span data-ttu-id="3c758-105">**string**</span><span class="sxs-lookup"><span data-stu-id="3c758-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3c758-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3c758-106">Attributes and elements</span></span>

<span data-ttu-id="3c758-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="3c758-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3c758-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="3c758-108">Attributes</span></span>

<span data-ttu-id="3c758-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="3c758-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3c758-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3c758-110">Child elements</span></span>

<span data-ttu-id="3c758-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="3c758-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3c758-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3c758-112">Parent elements</span></span>

[<span data-ttu-id="3c758-113">GetReminders</span><span class="sxs-lookup"><span data-stu-id="3c758-113">GetReminders</span></span>](getreminders.md)
  
## <a name="text-value"></a><span data-ttu-id="3c758-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="3c758-114">Text value</span></span>

<span data-ttu-id="3c758-115">Der Textwert des **ReminderType** -Elements ist der Typ der Erinnerungen um **Alle**, **aktuelle**oder **alte**zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="3c758-115">The text value of the **ReminderType** element is the type of reminders to return, either **All**, **Current**, or **Old**.</span></span> <span data-ttu-id="3c758-116">**Alle** ist der empfohlene Wert für dieses Element.</span><span class="sxs-lookup"><span data-stu-id="3c758-116">**All** is the recommended value for this element.</span></span> <span data-ttu-id="3c758-117">Weitere Informationen zur Beziehung zwischen dem **ReminderType** -Element und die Elemente [BeginTime](begintime.md) und [EndTime](endtime-remindermessagedatatype.md) finden Sie unter [GetReminders-Vorgang](getreminders-operation.md).</span><span class="sxs-lookup"><span data-stu-id="3c758-117">For more information about the relationship between the **ReminderType** element and the [BeginTime](begintime.md) and [EndTime](endtime-remindermessagedatatype.md) elements, see [GetReminders operation](getreminders-operation.md).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3c758-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3c758-118">Remarks</span></span>

<span data-ttu-id="3c758-119">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="3c758-119">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="3c758-120">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="3c758-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3c758-121">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="3c758-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3c758-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="3c758-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="3c758-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="3c758-123">Schema Name</span></span>  <br/> |<span data-ttu-id="3c758-124">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="3c758-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="3c758-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="3c758-125">Validation File</span></span>  <br/> |<span data-ttu-id="3c758-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="3c758-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3c758-127">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="3c758-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="3c758-128">False</span><span class="sxs-lookup"><span data-stu-id="3c758-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3c758-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3c758-129">See also</span></span>



[<span data-ttu-id="3c758-130">GetReminders</span><span class="sxs-lookup"><span data-stu-id="3c758-130">GetReminders</span></span>](getreminders.md)


- [<span data-ttu-id="3c758-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="3c758-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

