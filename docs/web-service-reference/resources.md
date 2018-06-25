---
title: Ressourcen
manager: sethgros
ms.date: 09/17/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Resources
api_type:
- schema
ms.assetid: a2133cf2-7c62-4f1c-b3aa-75f14d30dd74
description: Resources-Element stellt eine geplante Ressource für eine Besprechung.
ms.openlocfilehash: 31f358414e53f55b983f7633fc9c67b0ce3ab645
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831166"
---
# <a name="resources"></a><span data-ttu-id="af560-103">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="af560-103">Resources</span></span>

<span data-ttu-id="af560-104">**Resources** -Element stellt eine geplante Ressource für eine Besprechung.</span><span class="sxs-lookup"><span data-stu-id="af560-104">The **Resources** element represents a scheduled resource for a meeting.</span></span> 
  
```xml
<Resources>
   <Attendee/>
</Resources>
```

 <span data-ttu-id="af560-105">**NonEmptyArrayOfAttendeesType**</span><span class="sxs-lookup"><span data-stu-id="af560-105">**NonEmptyArrayOfAttendeesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="af560-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="af560-106">Attributes and elements</span></span>

<span data-ttu-id="af560-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="af560-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="af560-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="af560-108">Attributes</span></span>

<span data-ttu-id="af560-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="af560-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="af560-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="af560-110">Child elements</span></span>

|<span data-ttu-id="af560-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="af560-111">**Element**</span></span>|<span data-ttu-id="af560-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="af560-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="af560-113">Attendee</span><span class="sxs-lookup"><span data-stu-id="af560-113">Attendee</span></span>](attendee.md) <br/> |<span data-ttu-id="af560-114">Stellt Teilnehmer und Ressourcen für eine Besprechung.</span><span class="sxs-lookup"><span data-stu-id="af560-114">Represents attendees and resources for a meeting.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="af560-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="af560-115">Parent elements</span></span>

|<span data-ttu-id="af560-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="af560-116">**Element**</span></span>|<span data-ttu-id="af560-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="af560-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="af560-118">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="af560-118">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="af560-119">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="af560-119">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="af560-120">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="af560-120">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="af560-121">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="af560-121">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="af560-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="af560-122">Remarks</span></span>

<span data-ttu-id="af560-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="af560-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="af560-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="af560-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="af560-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="af560-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="af560-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="af560-126">Schema name</span></span>  <br/> |<span data-ttu-id="af560-127">Schematypen</span><span class="sxs-lookup"><span data-stu-id="af560-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="af560-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="af560-128">Validation file</span></span>  <br/> |<span data-ttu-id="af560-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="af560-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="af560-130">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="af560-130">Can be empty</span></span>  <br/> |<span data-ttu-id="af560-131">False</span><span class="sxs-lookup"><span data-stu-id="af560-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="af560-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="af560-132">See also</span></span>



- [<span data-ttu-id="af560-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="af560-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

