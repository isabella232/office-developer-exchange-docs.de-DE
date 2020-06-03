---
title: NetShowUrl
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- NetShowUrl
api_type:
- schema
ms.assetid: a5d48fc1-b141-422c-bcb0-05d0f9ba90dd
description: Das NetShowUrl-Element gibt die URL für eine Microsoft NetShow Online-Besprechung an.
ms.openlocfilehash: 66e288a5e66eecf404698135cc3257085b852034
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466332"
---
# <a name="netshowurl"></a><span data-ttu-id="1477c-103">NetShowUrl</span><span class="sxs-lookup"><span data-stu-id="1477c-103">NetShowUrl</span></span>

<span data-ttu-id="1477c-104">Das **NetShowUrl** -Element gibt die URL für eine Microsoft NetShow Online-Besprechung an.</span><span class="sxs-lookup"><span data-stu-id="1477c-104">The **NetShowUrl** element specifies the URL for a Microsoft NetShow online meeting.</span></span> 
  
```xml
<NetShowUrl/>
```

 <span data-ttu-id="1477c-105">**Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1477c-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1477c-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1477c-106">Attributes and elements</span></span>

<span data-ttu-id="1477c-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1477c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1477c-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="1477c-108">Attributes</span></span>

<span data-ttu-id="1477c-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="1477c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1477c-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1477c-110">Child elements</span></span>

<span data-ttu-id="1477c-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="1477c-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1477c-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1477c-112">Parent elements</span></span>

|<span data-ttu-id="1477c-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="1477c-113">**Element**</span></span>|<span data-ttu-id="1477c-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1477c-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1477c-115">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="1477c-115">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="1477c-116">Stellt eine Besprechung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="1477c-116">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="1477c-117">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="1477c-117">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="1477c-118">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="1477c-118">Represents an Exchange calendar item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1477c-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="1477c-119">Text value</span></span>

<span data-ttu-id="1477c-120">Ein Text Wert, der eine URL darstellt, ist erforderlich, wenn dieses Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1477c-120">A text value that represents a URL is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1477c-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1477c-121">Remarks</span></span>

<span data-ttu-id="1477c-122">Diese NetShowUrl-Eigenschaft ist schreibgeschützt für das Kalenderelement des Organisators.</span><span class="sxs-lookup"><span data-stu-id="1477c-122">This NetShowUrl property is read-writable for the organizer's calendar item.</span></span> <span data-ttu-id="1477c-123">Er ist schreibgeschützt für Besprechungsanfragen und für Teilnehmer.</span><span class="sxs-lookup"><span data-stu-id="1477c-123">It is read-only for meeting requests and for attendees.</span></span>
  
<span data-ttu-id="1477c-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="1477c-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1477c-125">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="1477c-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1477c-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="1477c-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1477c-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="1477c-127">Schema name</span></span>  <br/> |<span data-ttu-id="1477c-128">Schematypen</span><span class="sxs-lookup"><span data-stu-id="1477c-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="1477c-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="1477c-129">Validation file</span></span>  <br/> |<span data-ttu-id="1477c-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1477c-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1477c-131">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="1477c-131">Can be empty</span></span>  <br/> |<span data-ttu-id="1477c-132">False</span><span class="sxs-lookup"><span data-stu-id="1477c-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1477c-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1477c-133">See also</span></span>



- [<span data-ttu-id="1477c-134">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="1477c-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

