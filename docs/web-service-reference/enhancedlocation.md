---
title: EnhancedLocation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4fdfb74f-f33c-46ae-a7c7-451a5b0c6a59
description: Das EnhancedLocation-Element gibt Speicherortinformationen wie den Namen, die Adresse und optionale Notizen zu einem Speicherort an.
ms.openlocfilehash: 06ec800b763ef61af51da03ca8a340f6ac4d2a8e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462957"
---
# <a name="enhancedlocation"></a><span data-ttu-id="b43e0-103">EnhancedLocation</span><span class="sxs-lookup"><span data-stu-id="b43e0-103">EnhancedLocation</span></span>

<span data-ttu-id="b43e0-104">Das **EnhancedLocation** -Element gibt Speicherortinformationen wie den Namen, die Adresse und optionale Notizen zu einem Speicherort an.</span><span class="sxs-lookup"><span data-stu-id="b43e0-104">The **EnhancedLocation** element specifies location information such as the name, address, and optional notes about a location.</span></span> 
  
```XML
<EnhancedLocation>
    <DisplayName/>
    <Annotation/>
    <PostalAddress/>
</EnhancedLocation>
```

 <span data-ttu-id="b43e0-105">**EnhancedLocationType**</span><span class="sxs-lookup"><span data-stu-id="b43e0-105">**EnhancedLocationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b43e0-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b43e0-106">Attributes and elements</span></span>

<span data-ttu-id="b43e0-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b43e0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b43e0-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="b43e0-108">Attributes</span></span>

<span data-ttu-id="b43e0-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="b43e0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b43e0-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b43e0-110">Child elements</span></span>

|<span data-ttu-id="b43e0-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="b43e0-111">**Element**</span></span>|<span data-ttu-id="b43e0-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b43e0-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b43e0-113">DisplayName (Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="b43e0-113">DisplayName (string)</span></span>](displayname-string.md) <br/> |<span data-ttu-id="b43e0-114">Definiert den Anzeigenamen eines Ordners, Kontakts, einer Verteilerliste, eines Stellvertreters, eines Orts oder einer Regel.</span><span class="sxs-lookup"><span data-stu-id="b43e0-114">Defines the display name of a folder, contact, distribution list, delegate user, location, or rule.</span></span>  <br/> |
|[<span data-ttu-id="b43e0-115">Anmerkung</span><span class="sxs-lookup"><span data-stu-id="b43e0-115">Annotation</span></span>](annotation.md) <br/> |<span data-ttu-id="b43e0-116">Enthält optionale Notizen, die von einem Benutzer hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="b43e0-116">Contains optional notes added by a user.</span></span>  <br/> |
|[<span data-ttu-id="b43e0-117">PostalAddress (PersonaPostalAddressType)</span><span class="sxs-lookup"><span data-stu-id="b43e0-117">PostalAddress (PersonaPostalAddressType)</span></span>](postaladdress-personapostaladdresstype.md) <br/> |<span data-ttu-id="b43e0-118">Gibt die Postanschrift für eine Person an.</span><span class="sxs-lookup"><span data-stu-id="b43e0-118">Specifies the postal address for a persona.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b43e0-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b43e0-119">Parent elements</span></span>

|<span data-ttu-id="b43e0-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="b43e0-120">**Element**</span></span>|<span data-ttu-id="b43e0-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b43e0-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b43e0-122">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="b43e0-122">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="b43e0-123">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="b43e0-123">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="b43e0-124">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="b43e0-124">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="b43e0-125">Stellt eine Besprechungsabsage im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="b43e0-125">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="b43e0-126">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="b43e0-126">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="b43e0-127">Stellt eine Besprechungsantwort im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="b43e0-127">Represents a meeting response in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b43e0-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b43e0-128">Remarks</span></span>

<span data-ttu-id="b43e0-129">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b43e0-129">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="b43e0-130">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="b43e0-130">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b43e0-131">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="b43e0-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b43e0-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="b43e0-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b43e0-133">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b43e0-133">Schema Name</span></span>  <br/> |<span data-ttu-id="b43e0-134">Typschema</span><span class="sxs-lookup"><span data-stu-id="b43e0-134">Type schema</span></span>  <br/> |
|<span data-ttu-id="b43e0-135">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b43e0-135">Validation File</span></span>  <br/> |<span data-ttu-id="b43e0-136">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="b43e0-136">types.xsd</span></span>  <br/> |
|<span data-ttu-id="b43e0-137">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="b43e0-137">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="b43e0-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b43e0-138">See also</span></span>



- [<span data-ttu-id="b43e0-139">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="b43e0-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

