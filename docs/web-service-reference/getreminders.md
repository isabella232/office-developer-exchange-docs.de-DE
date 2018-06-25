---
title: GetReminders
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 943c3d5d-7d29-4d70-932c-8a4fe44a0037
description: Das GetReminders-Element gibt eine Anforderung an eine Erinnerung erhalten möchten.
ms.openlocfilehash: f4ecc858af2150bb3f88ebdf9ed541892f2fead1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758782"
---
# <a name="getreminders"></a><span data-ttu-id="101bc-103">GetReminders</span><span class="sxs-lookup"><span data-stu-id="101bc-103">GetReminders</span></span>

<span data-ttu-id="101bc-104">Das **GetReminders** -Element gibt eine Anforderung an eine Erinnerung erhalten möchten.</span><span class="sxs-lookup"><span data-stu-id="101bc-104">The **GetReminders** element specifies a request to get reminders.</span></span> 
  
```XML
<GetReminders>
   <BeginTime/>
   <EndTime/>
   <MaxItems/>
   <ReminderType/>
</GetReminders>

```

 <span data-ttu-id="101bc-105">**GetRemindersType**</span><span class="sxs-lookup"><span data-stu-id="101bc-105">**GetRemindersType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="101bc-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="101bc-106">Attributes and elements</span></span>

<span data-ttu-id="101bc-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="101bc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="101bc-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="101bc-108">Attributes</span></span>

<span data-ttu-id="101bc-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="101bc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="101bc-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="101bc-110">Child elements</span></span>

<span data-ttu-id="101bc-111">[BeginTime](begintime.md) | [EndTime (ReminderMessageDataType)](endtime-remindermessagedatatype.md) | [MaxItems wird](maxitems.md) | [ReminderType](remindertype.md)</span><span class="sxs-lookup"><span data-stu-id="101bc-111">[BeginTime](begintime.md) | [EndTime (ReminderMessageDataType)](endtime-remindermessagedatatype.md) | [MaxItems](maxitems.md) | [ReminderType](remindertype.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="101bc-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="101bc-112">Parent elements</span></span>

<span data-ttu-id="101bc-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="101bc-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="101bc-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="101bc-114">Remarks</span></span>

<span data-ttu-id="101bc-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="101bc-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="101bc-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="101bc-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="101bc-117">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="101bc-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="101bc-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="101bc-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="101bc-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="101bc-119">Schema Name</span></span>  <br/> |<span data-ttu-id="101bc-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="101bc-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="101bc-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="101bc-121">Validation File</span></span>  <br/> |<span data-ttu-id="101bc-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="101bc-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="101bc-123">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="101bc-123">Can be Empty</span></span>  <br/> |<span data-ttu-id="101bc-124">True</span><span class="sxs-lookup"><span data-stu-id="101bc-124">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="101bc-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="101bc-125">See also</span></span>



- [<span data-ttu-id="101bc-126">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="101bc-126">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

