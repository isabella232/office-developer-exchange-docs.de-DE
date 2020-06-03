---
title: Isorganizer
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a31ac268-5061-4272-a433-ffaea2fbcfa9
description: Das isorganizer-Element gibt einen booleschen Wert an, der angibt, ob diese Person der Organisator der Besprechung ist.
ms.openlocfilehash: 45b7a66068dc00f6e60b7380240bea6836282fd4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466563"
---
# <a name="isorganizer"></a><span data-ttu-id="fa733-103">Isorganizer</span><span class="sxs-lookup"><span data-stu-id="fa733-103">IsOrganizer</span></span>

<span data-ttu-id="fa733-104">Das **isorganizer** -Element gibt einen booleschen Wert an, der angibt, ob diese Person der Organisator der Besprechung ist.</span><span class="sxs-lookup"><span data-stu-id="fa733-104">The **IsOrganizer** element specifies a Boolean value that indicates whether this person is the organizer of the meeting.</span></span> 
  
```XML
<IsOrganizer>true | false</IsOrganizer>
```

 <span data-ttu-id="fa733-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="fa733-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fa733-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="fa733-106">Attributes and elements</span></span>

<span data-ttu-id="fa733-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="fa733-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fa733-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="fa733-108">Attributes</span></span>

<span data-ttu-id="fa733-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="fa733-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fa733-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fa733-110">Child elements</span></span>

<span data-ttu-id="fa733-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="fa733-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="fa733-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fa733-112">Parent elements</span></span>

|<span data-ttu-id="fa733-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="fa733-113">**Element**</span></span>|<span data-ttu-id="fa733-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fa733-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fa733-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="fa733-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="fa733-116">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="fa733-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="fa733-117">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="fa733-117">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="fa733-118">Stellt eine Besprechungsnachricht dar.</span><span class="sxs-lookup"><span data-stu-id="fa733-118">Represents a meeting message.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="fa733-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="fa733-119">Text value</span></span>

<span data-ttu-id="fa733-120">Der Textwert **true** für das **isorganizer** -Element gibt an, dass das Kalenderelement oder die Besprechungsnachricht vom Benutzer erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="fa733-120">A text value of **true** for the **IsOrganizer** element indicates that the calendar item or meeting message was created by the user.</span></span> <span data-ttu-id="fa733-121">Der Wert **false** gibt an, dass das Kalenderelement oder die Besprechungsnachricht nicht vom Benutzer BV erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="fa733-121">A value of **false** indicates that the calendar item or meeting message was not created bv the user.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="fa733-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fa733-122">Remarks</span></span>

<span data-ttu-id="fa733-123">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="fa733-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="fa733-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="fa733-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fa733-125">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="fa733-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fa733-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="fa733-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fa733-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="fa733-127">Schema Name</span></span>  <br/> |<span data-ttu-id="fa733-128">Typschema</span><span class="sxs-lookup"><span data-stu-id="fa733-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="fa733-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="fa733-129">Validation File</span></span>  <br/> |<span data-ttu-id="fa733-130">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="fa733-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="fa733-131">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="fa733-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="fa733-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fa733-132">See also</span></span>



- [<span data-ttu-id="fa733-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="fa733-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

