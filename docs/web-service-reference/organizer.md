---
title: Organisator
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Organizer
api_type:
- schema
ms.assetid: 63892b57-3805-4d60-b9f7-20552a69c241
description: Das Organisator-Element darstellt, den Organisator einer Besprechung.
ms.openlocfilehash: b723578a1b52cd5f6e9bd869a15430453adfa291
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830662"
---
# <a name="organizer"></a><span data-ttu-id="27186-103">Organisator</span><span class="sxs-lookup"><span data-stu-id="27186-103">Organizer</span></span>

<span data-ttu-id="27186-104">Das **Organisator** -Element darstellt, den Organisator einer Besprechung.</span><span class="sxs-lookup"><span data-stu-id="27186-104">The **Organizer** element represents the organizer of a meeting.</span></span> 
  
```xml
<Organizer>
   <Mailbox/>
</Organizer>
```

<span data-ttu-id="27186-105">**SingleRecipientType**</span><span class="sxs-lookup"><span data-stu-id="27186-105">**SingleRecipientType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="27186-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="27186-106">Attributes and elements</span></span>

<span data-ttu-id="27186-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="27186-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="27186-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="27186-108">Attributes</span></span>

<span data-ttu-id="27186-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="27186-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="27186-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="27186-110">Child elements</span></span>

|<span data-ttu-id="27186-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="27186-111">**Element**</span></span>|<span data-ttu-id="27186-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="27186-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="27186-113">Postfach</span><span class="sxs-lookup"><span data-stu-id="27186-113">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="27186-114">Ein e-Mail-aktivierten Active Directory Directory Service-Objekt identifiziert.</span><span class="sxs-lookup"><span data-stu-id="27186-114">Identifies a mail-enabled Active Directory directory service object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="27186-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="27186-115">Parent elements</span></span>

|<span data-ttu-id="27186-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="27186-116">**Element**</span></span>|<span data-ttu-id="27186-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="27186-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="27186-118">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="27186-118">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="27186-119">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="27186-119">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="27186-120">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="27186-120">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="27186-121">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="27186-121">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="27186-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="27186-122">Remarks</span></span>

<span data-ttu-id="27186-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="27186-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="27186-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="27186-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="27186-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="27186-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="27186-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="27186-126">Schema name</span></span>  <br/> |<span data-ttu-id="27186-127">Schematypen</span><span class="sxs-lookup"><span data-stu-id="27186-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="27186-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="27186-128">Validation file</span></span>  <br/> |<span data-ttu-id="27186-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="27186-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="27186-130">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="27186-130">Can be empty</span></span>  <br/> |<span data-ttu-id="27186-131">False</span><span class="sxs-lookup"><span data-stu-id="27186-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="27186-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="27186-132">See also</span></span>

- [<span data-ttu-id="27186-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="27186-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

