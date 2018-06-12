---
title: Erinnerungen
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 19294300-ab84-4784-8aa7-3395a08de640
description: Das Reminders-Element gibt die Erinnerungen in der Antwort auf eine Anforderung GetReminders zurückgegeben.
ms.openlocfilehash: 955fc568dc919d591076271382a8c9bbd1d146ad
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831071"
---
# <a name="reminders"></a><span data-ttu-id="3f0a2-103">Erinnerungen</span><span class="sxs-lookup"><span data-stu-id="3f0a2-103">Reminders</span></span>

<span data-ttu-id="3f0a2-104">Das **Reminders** -Element gibt die Erinnerungen in der Antwort auf eine Anforderung **GetReminders** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3f0a2-104">The **Reminders** element specifies the reminders returned in the response to a **GetReminders** request.</span></span> 
  
```XML
<Reminders>
   <Reminder></Reminder>
</Reminders>
```

 <span data-ttu-id="3f0a2-105">**ArrayOfRemindersType**</span><span class="sxs-lookup"><span data-stu-id="3f0a2-105">**ArrayOfRemindersType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3f0a2-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3f0a2-106">Attributes and elements</span></span>

<span data-ttu-id="3f0a2-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="3f0a2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3f0a2-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="3f0a2-108">Attributes</span></span>

<span data-ttu-id="3f0a2-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="3f0a2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3f0a2-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3f0a2-110">Child elements</span></span>

[<span data-ttu-id="3f0a2-111">Reminder</span><span class="sxs-lookup"><span data-stu-id="3f0a2-111">Reminder</span></span>](reminder.md)
  
### <a name="parent-elements"></a><span data-ttu-id="3f0a2-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3f0a2-112">Parent elements</span></span>

[<span data-ttu-id="3f0a2-113">GetRemindersResponse</span><span class="sxs-lookup"><span data-stu-id="3f0a2-113">GetRemindersResponse</span></span>](getremindersresponse.md)
  
## <a name="remarks"></a><span data-ttu-id="3f0a2-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3f0a2-114">Remarks</span></span>

<span data-ttu-id="3f0a2-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="3f0a2-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="3f0a2-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="3f0a2-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3f0a2-117">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="3f0a2-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3f0a2-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="3f0a2-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="3f0a2-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="3f0a2-119">Schema Name</span></span>  <br/> |<span data-ttu-id="3f0a2-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="3f0a2-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="3f0a2-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="3f0a2-121">Validation File</span></span>  <br/> |<span data-ttu-id="3f0a2-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="3f0a2-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3f0a2-123">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="3f0a2-123">Can be Empty</span></span>  <br/> |<span data-ttu-id="3f0a2-124">False</span><span class="sxs-lookup"><span data-stu-id="3f0a2-124">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3f0a2-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3f0a2-125">See also</span></span>



[<span data-ttu-id="3f0a2-126">GetRemindersResponse</span><span class="sxs-lookup"><span data-stu-id="3f0a2-126">GetRemindersResponse</span></span>](getremindersresponse.md)


- [<span data-ttu-id="3f0a2-127">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="3f0a2-127">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

