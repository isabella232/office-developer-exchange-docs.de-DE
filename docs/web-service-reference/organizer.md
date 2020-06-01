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
description: Das Organizer-Element stellt den Organisator einer Besprechung dar.
ms.openlocfilehash: c1188c9b3a894e86a08b8869045c3647e394f506
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462416"
---
# <a name="organizer"></a><span data-ttu-id="f9682-103">Organisator</span><span class="sxs-lookup"><span data-stu-id="f9682-103">Organizer</span></span>

<span data-ttu-id="f9682-104">Das **Organizer** -Element stellt den Organisator einer Besprechung dar.</span><span class="sxs-lookup"><span data-stu-id="f9682-104">The **Organizer** element represents the organizer of a meeting.</span></span> 
  
```xml
<Organizer>
   <Mailbox/>
</Organizer>
```

<span data-ttu-id="f9682-105">**SingleRecipientType**</span><span class="sxs-lookup"><span data-stu-id="f9682-105">**SingleRecipientType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="f9682-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f9682-106">Attributes and elements</span></span>

<span data-ttu-id="f9682-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f9682-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f9682-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="f9682-108">Attributes</span></span>

<span data-ttu-id="f9682-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="f9682-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f9682-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f9682-110">Child elements</span></span>

|<span data-ttu-id="f9682-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="f9682-111">**Element**</span></span>|<span data-ttu-id="f9682-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f9682-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f9682-113">Postfach</span><span class="sxs-lookup"><span data-stu-id="f9682-113">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="f9682-114">Ein e-Mail-aktivierten Active Directory Directory Service-Objekt identifiziert.</span><span class="sxs-lookup"><span data-stu-id="f9682-114">Identifies a mail-enabled Active Directory directory service object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f9682-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f9682-115">Parent elements</span></span>

|<span data-ttu-id="f9682-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="f9682-116">**Element**</span></span>|<span data-ttu-id="f9682-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f9682-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f9682-118">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="f9682-118">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="f9682-119">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="f9682-119">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="f9682-120">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="f9682-120">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="f9682-121">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="f9682-121">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f9682-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f9682-122">Remarks</span></span>

<span data-ttu-id="f9682-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="f9682-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f9682-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="f9682-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f9682-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="f9682-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f9682-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f9682-126">Schema name</span></span>  <br/> |<span data-ttu-id="f9682-127">Schematypen</span><span class="sxs-lookup"><span data-stu-id="f9682-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="f9682-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f9682-128">Validation file</span></span>  <br/> |<span data-ttu-id="f9682-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f9682-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f9682-130">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="f9682-130">Can be empty</span></span>  <br/> |<span data-ttu-id="f9682-131">False</span><span class="sxs-lookup"><span data-stu-id="f9682-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f9682-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f9682-132">See also</span></span>

- [<span data-ttu-id="f9682-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="f9682-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

