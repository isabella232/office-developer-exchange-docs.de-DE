---
title: ProposedEnd (MeetingRegistrationResponseObjectType)
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3e5d2567-a5a2-4791-b209-c29082894a9e
description: Das ProposedEnd (MeetingRegistrationResponseObjectType)-Element gibt einen Teilnehmer vorgeschlagene neue Endzeit für eine Besprechung.
ms.openlocfilehash: deceacd54767bf9b5ae5b3e452709d397ef95402
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830902"
---
# <a name="proposedend-meetingregistrationresponseobjecttype"></a><span data-ttu-id="60418-103">ProposedEnd (MeetingRegistrationResponseObjectType)</span><span class="sxs-lookup"><span data-stu-id="60418-103">ProposedEnd (MeetingRegistrationResponseObjectType)</span></span>

<span data-ttu-id="60418-104">Das **ProposedEnd (MeetingRegistrationResponseObjectType)** -Element gibt einen Teilnehmer vorgeschlagene neue Endzeit für eine Besprechung.</span><span class="sxs-lookup"><span data-stu-id="60418-104">The **ProposedEnd (MeetingRegistrationResponseObjectType)** element specifies an attendee's proposed new end time for a meeting.</span></span> 
  
```XML
<ProposedEnd />
```

 <span data-ttu-id="60418-105">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="60418-105">**dateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="60418-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="60418-106">Attributes and elements</span></span>

<span data-ttu-id="60418-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="60418-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="60418-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="60418-108">Attributes</span></span>

<span data-ttu-id="60418-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="60418-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="60418-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="60418-110">Child elements</span></span>

<span data-ttu-id="60418-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="60418-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="60418-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="60418-112">Parent elements</span></span>

<span data-ttu-id="60418-113">[AcceptItem](acceptitem.md) | [TentativelyAcceptItem](tentativelyacceptitem.md) | [DeclineItem](declineitem.md)</span><span class="sxs-lookup"><span data-stu-id="60418-113">[AcceptItem](acceptitem.md) | [TentativelyAcceptItem](tentativelyacceptitem.md) | [DeclineItem](declineitem.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="60418-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="60418-114">Text value</span></span>

<span data-ttu-id="60418-115">Der Textwert des **ProposedEnd (MeetingRegistrationResponseObjectType)** -Elements ist das vorgeschlagene Enddatum und die Uhrzeit der Besprechung.</span><span class="sxs-lookup"><span data-stu-id="60418-115">The text value of the **ProposedEnd (MeetingRegistrationResponseObjectType)** element is the proposed end date and time of the meeting.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="60418-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="60418-116">Remarks</span></span>

<span data-ttu-id="60418-117">Dieses Element wurde in Exchange Server 2013 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="60418-117">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="60418-118">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="60418-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="60418-119">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="60418-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="60418-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="60418-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="60418-121">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="60418-121">Schema Name</span></span>  <br/> |<span data-ttu-id="60418-122">Schematypen</span><span class="sxs-lookup"><span data-stu-id="60418-122">Types schema</span></span>  <br/> |
|<span data-ttu-id="60418-123">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="60418-123">Validation File</span></span>  <br/> |<span data-ttu-id="60418-124">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="60418-124">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="60418-125">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="60418-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="60418-126">True</span><span class="sxs-lookup"><span data-stu-id="60418-126">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="60418-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="60418-127">See also</span></span>



[<span data-ttu-id="60418-128">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="60418-128">AcceptItem</span></span>](acceptitem.md)
  
[<span data-ttu-id="60418-129">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="60418-129">DeclineItem</span></span>](declineitem.md)
  
[<span data-ttu-id="60418-130">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="60418-130">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md)


- [<span data-ttu-id="60418-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="60418-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

