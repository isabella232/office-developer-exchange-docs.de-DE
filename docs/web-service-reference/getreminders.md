---
title: GetReminders
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 943c3d5d-7d29-4d70-932c-8a4fe44a0037
description: Das geterinnerungs-Element gibt eine Anforderung zum Abrufen von Erinnerungen an.
ms.openlocfilehash: 8b869730f39876b838fbcbef3c39661238ed203c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458299"
---
# <a name="getreminders"></a><span data-ttu-id="7a136-103">GetReminders</span><span class="sxs-lookup"><span data-stu-id="7a136-103">GetReminders</span></span>

<span data-ttu-id="7a136-104">Das **geterinnerungs** -Element gibt eine Anforderung zum Abrufen von Erinnerungen an.</span><span class="sxs-lookup"><span data-stu-id="7a136-104">The **GetReminders** element specifies a request to get reminders.</span></span> 
  
```XML
<GetReminders>
   <BeginTime/>
   <EndTime/>
   <MaxItems/>
   <ReminderType/>
</GetReminders>

```

 <span data-ttu-id="7a136-105">**GetRemindersType**</span><span class="sxs-lookup"><span data-stu-id="7a136-105">**GetRemindersType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7a136-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="7a136-106">Attributes and elements</span></span>

<span data-ttu-id="7a136-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="7a136-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7a136-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="7a136-108">Attributes</span></span>

<span data-ttu-id="7a136-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="7a136-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7a136-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7a136-110">Child elements</span></span>

<span data-ttu-id="7a136-111">[BeginTime](begintime.md)  |  [EndTime (ReminderMessageDataType)](endtime-remindermessagedatatype.md)  |  [MaxItems wird](maxitems.md)  |  [Reminder](remindertype.md)</span><span class="sxs-lookup"><span data-stu-id="7a136-111">[BeginTime](begintime.md) | [EndTime (ReminderMessageDataType)](endtime-remindermessagedatatype.md) | [MaxItems](maxitems.md) | [ReminderType](remindertype.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7a136-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7a136-112">Parent elements</span></span>

<span data-ttu-id="7a136-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="7a136-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7a136-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7a136-114">Remarks</span></span>

<span data-ttu-id="7a136-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="7a136-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="7a136-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="7a136-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7a136-117">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="7a136-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7a136-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="7a136-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="7a136-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="7a136-119">Schema Name</span></span>  <br/> |<span data-ttu-id="7a136-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="7a136-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="7a136-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="7a136-121">Validation File</span></span>  <br/> |<span data-ttu-id="7a136-122">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="7a136-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7a136-123">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="7a136-123">Can be Empty</span></span>  <br/> |<span data-ttu-id="7a136-124">True</span><span class="sxs-lookup"><span data-stu-id="7a136-124">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7a136-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a136-125">See also</span></span>



- [<span data-ttu-id="7a136-126">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="7a136-126">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

