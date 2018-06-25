---
title: IsOrganizer
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a31ac268-5061-4272-a433-ffaea2fbcfa9
description: Das IsOrganizer-Element gibt einen Boolean-Wert, der angibt, ob diese Person der Organisator der Besprechung ist.
ms.openlocfilehash: 5fd775cfc0a296c08d19d0468d96aa36ba67ddd0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830063"
---
# <a name="isorganizer"></a><span data-ttu-id="176ad-103">IsOrganizer</span><span class="sxs-lookup"><span data-stu-id="176ad-103">IsOrganizer</span></span>

<span data-ttu-id="176ad-104">Das **IsOrganizer** -Element gibt einen Boolean-Wert, der angibt, ob diese Person der Organisator der Besprechung ist.</span><span class="sxs-lookup"><span data-stu-id="176ad-104">The **IsOrganizer** element specifies a Boolean value that indicates whether this person is the organizer of the meeting.</span></span> 
  
```XML
<IsOrganizer>true | false</IsOrganizer>
```

 <span data-ttu-id="176ad-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="176ad-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="176ad-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="176ad-106">Attributes and elements</span></span>

<span data-ttu-id="176ad-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="176ad-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="176ad-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="176ad-108">Attributes</span></span>

<span data-ttu-id="176ad-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="176ad-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="176ad-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="176ad-110">Child elements</span></span>

<span data-ttu-id="176ad-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="176ad-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="176ad-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="176ad-112">Parent elements</span></span>

|<span data-ttu-id="176ad-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="176ad-113">**Element**</span></span>|<span data-ttu-id="176ad-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="176ad-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="176ad-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="176ad-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="176ad-116">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="176ad-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="176ad-117">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="176ad-117">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="176ad-118">Stellt eine Besprechungsnachricht dar.</span><span class="sxs-lookup"><span data-stu-id="176ad-118">Represents a meeting message.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="176ad-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="176ad-119">Text value</span></span>

<span data-ttu-id="176ad-120">Der Textwert **true** für das **IsOrganizer** -Element gibt an, dass die Kalendernachricht, Element oder eine Besprechung durch den Benutzer erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="176ad-120">A text value of **true** for the **IsOrganizer** element indicates that the calendar item or meeting message was created by the user.</span></span> <span data-ttu-id="176ad-121">Der Wert **false** gibt an, dass die Kalendernachricht, Element oder eine Besprechung nicht BW der Benutzer erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="176ad-121">A value of **false** indicates that the calendar item or meeting message was not created bv the user.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="176ad-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="176ad-122">Remarks</span></span>

<span data-ttu-id="176ad-123">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="176ad-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="176ad-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="176ad-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="176ad-125">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="176ad-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="176ad-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="176ad-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="176ad-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="176ad-127">Schema Name</span></span>  <br/> |<span data-ttu-id="176ad-128">Typschema</span><span class="sxs-lookup"><span data-stu-id="176ad-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="176ad-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="176ad-129">Validation File</span></span>  <br/> |<span data-ttu-id="176ad-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="176ad-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="176ad-131">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="176ad-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="176ad-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="176ad-132">See also</span></span>



- [<span data-ttu-id="176ad-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="176ad-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

