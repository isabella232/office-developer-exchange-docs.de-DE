---
title: EnhancedLocation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4fdfb74f-f33c-46ae-a7c7-451a5b0c6a59
description: Das EnhancedLocation-Element gibt Speicherort Informationen wie Name, Adresse und optionalen Hinweise, die über einen Ort.
ms.openlocfilehash: 90397cfc622fed40c561d30c13d6617eb979a68a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758245"
---
# <a name="enhancedlocation"></a><span data-ttu-id="dc571-103">EnhancedLocation</span><span class="sxs-lookup"><span data-stu-id="dc571-103">EnhancedLocation</span></span>

<span data-ttu-id="dc571-104">Das **EnhancedLocation** -Element gibt Speicherort Informationen wie Name, Adresse und optionalen Hinweise, die über einen Ort.</span><span class="sxs-lookup"><span data-stu-id="dc571-104">The **EnhancedLocation** element specifies location information such as the name, address, and optional notes about a location.</span></span> 
  
```XML
<EnhancedLocation>
    <DisplayName/>
    <Annotation/>
    <PostalAddress/>
</EnhancedLocation>
```

 <span data-ttu-id="dc571-105">**EnhancedLocationType**</span><span class="sxs-lookup"><span data-stu-id="dc571-105">**EnhancedLocationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="dc571-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="dc571-106">Attributes and elements</span></span>

<span data-ttu-id="dc571-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="dc571-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dc571-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="dc571-108">Attributes</span></span>

<span data-ttu-id="dc571-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="dc571-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dc571-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dc571-110">Child elements</span></span>

|<span data-ttu-id="dc571-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="dc571-111">**Element**</span></span>|<span data-ttu-id="dc571-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dc571-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dc571-113">DisplayName (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="dc571-113">DisplayName (string)</span></span>](displayname-string.md) <br/> |<span data-ttu-id="dc571-114">Der Anzeigename eines Ordners, Kontakt, Verteilerliste, Stellvertretungsbenutzers, Standort oder Regel definiert.</span><span class="sxs-lookup"><span data-stu-id="dc571-114">Defines the display name of a folder, contact, distribution list, delegate user, location, or rule.</span></span>  <br/> |
|[<span data-ttu-id="dc571-115">Anmerkung</span><span class="sxs-lookup"><span data-stu-id="dc571-115">Annotation</span></span>](annotation.md) <br/> |<span data-ttu-id="dc571-116">Enthält die optionalen Hinweise, die von einem Benutzer hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="dc571-116">Contains optional notes added by a user.</span></span>  <br/> |
|[<span data-ttu-id="dc571-117">PostalAddress (PersonaPostalAddressType)</span><span class="sxs-lookup"><span data-stu-id="dc571-117">PostalAddress (PersonaPostalAddressType)</span></span>](postaladdress-personapostaladdresstype.md) <br/> |<span data-ttu-id="dc571-118">Gibt die Adresse für eine Rolle an.</span><span class="sxs-lookup"><span data-stu-id="dc571-118">Specifies the postal address for a persona.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="dc571-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dc571-119">Parent elements</span></span>

|<span data-ttu-id="dc571-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="dc571-120">**Element**</span></span>|<span data-ttu-id="dc571-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dc571-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dc571-122">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="dc571-122">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="dc571-123">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="dc571-123">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="dc571-124">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="dc571-124">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="dc571-125">Stellt eine Besprechungsabsage im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="dc571-125">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="dc571-126">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="dc571-126">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="dc571-127">Stellt eine Besprechungsantwort im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="dc571-127">Represents a meeting response in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dc571-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="dc571-128">Remarks</span></span>

<span data-ttu-id="dc571-129">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="dc571-129">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="dc571-130">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="dc571-130">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dc571-131">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="dc571-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dc571-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="dc571-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="dc571-133">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="dc571-133">Schema Name</span></span>  <br/> |<span data-ttu-id="dc571-134">Typschema</span><span class="sxs-lookup"><span data-stu-id="dc571-134">Type schema</span></span>  <br/> |
|<span data-ttu-id="dc571-135">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="dc571-135">Validation File</span></span>  <br/> |<span data-ttu-id="dc571-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="dc571-136">types.xsd</span></span>  <br/> |
|<span data-ttu-id="dc571-137">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="dc571-137">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="dc571-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dc571-138">See also</span></span>



- [<span data-ttu-id="dc571-139">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="dc571-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

