---
title: ExtendedProperty
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ExtendedProperty
api_type:
- schema
ms.assetid: f9701409-b620-4afe-b9ee-4c1e95507af7
description: Das ExtendedProperty-Element identifiziert extended MAPI-Eigenschaften für Ordner und Elemente.
ms.openlocfilehash: 9a6c44e953cab4900e4b75eb42bdf4d8633e58f9
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353728"
---
# <a name="extendedproperty"></a><span data-ttu-id="97b8b-103">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="97b8b-103">ExtendedProperty</span></span>

<span data-ttu-id="97b8b-104">Das **ExtendedProperty** -Element identifiziert extended MAPI-Eigenschaften für Ordner und Elemente.</span><span class="sxs-lookup"><span data-stu-id="97b8b-104">The **ExtendedProperty** element identifies extended MAPI properties on folders and items.</span></span> 
  
```xml
<ExtendedProperty>
   <ExtendedFieldURI/>
   <Values/>
</ExtendedProperty>
```

```xml
<ExtendedProperty>
   <ExtendedFieldURI/>
   <Value/>
</ExtendedProperty>
```

<span data-ttu-id="97b8b-105">**ExtendedPropertyType**</span><span class="sxs-lookup"><span data-stu-id="97b8b-105">**ExtendedPropertyType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="97b8b-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="97b8b-106">Attributes and elements</span></span>

<span data-ttu-id="97b8b-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="97b8b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="97b8b-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="97b8b-108">Attributes</span></span>

<span data-ttu-id="97b8b-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="97b8b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="97b8b-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="97b8b-110">Child elements</span></span>

|<span data-ttu-id="97b8b-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="97b8b-111">**Element**</span></span>|<span data-ttu-id="97b8b-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="97b8b-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="97b8b-113">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="97b8b-113">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="97b8b-114">Identifiziert eine erweiterte MAPI-Eigenschaft zum Abrufen oder festlegen, oder erstellen.</span><span class="sxs-lookup"><span data-stu-id="97b8b-114">Identifies an extended MAPI property to get, set, or create.</span></span>  <br/> |
|[<span data-ttu-id="97b8b-115">Values</span><span class="sxs-lookup"><span data-stu-id="97b8b-115">Values</span></span>](values.md) <br/> |<span data-ttu-id="97b8b-116">Enthält eine Auflistung von Werten für eine mehrwertige extended MAPI-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="97b8b-116">Contains a collection of values for a multivalued extended MAPI property.</span></span>  <br/> |
|[<span data-ttu-id="97b8b-117">Wert</span><span class="sxs-lookup"><span data-stu-id="97b8b-117">Value</span></span>](value.md) <br/> |<span data-ttu-id="97b8b-118">Enthält den Wert der erweiterten Eigenschaft einwertig MAPI.</span><span class="sxs-lookup"><span data-stu-id="97b8b-118">Contains the value of single-valued MAPI extended property.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="97b8b-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="97b8b-119">Parent elements</span></span>

|<span data-ttu-id="97b8b-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="97b8b-120">**Element**</span></span>|<span data-ttu-id="97b8b-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="97b8b-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="97b8b-122">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="97b8b-122">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="97b8b-123">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="97b8b-123">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="97b8b-124">Kontaktperson</span><span class="sxs-lookup"><span data-stu-id="97b8b-124">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="97b8b-125">Stellt ein Exchange-Kontaktelement dar.</span><span class="sxs-lookup"><span data-stu-id="97b8b-125">Represents an Exchange contact item.</span></span>  <br/> |
|[<span data-ttu-id="97b8b-126">DistributionList</span><span class="sxs-lookup"><span data-stu-id="97b8b-126">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="97b8b-127">Stellt eine Verteilerliste dar.</span><span class="sxs-lookup"><span data-stu-id="97b8b-127">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="97b8b-128">Element</span><span class="sxs-lookup"><span data-stu-id="97b8b-128">Item</span></span>](item.md) <br/> |<span data-ttu-id="97b8b-129">Stellt ein Element im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="97b8b-129">Represents an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="97b8b-130">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="97b8b-130">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="97b8b-131">Stellt eine Besprechungsabsage im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="97b8b-131">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="97b8b-132">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="97b8b-132">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="97b8b-133">Stellt eine Besprechung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="97b8b-133">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="97b8b-134">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="97b8b-134">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="97b8b-135">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="97b8b-135">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="97b8b-136">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="97b8b-136">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="97b8b-137">Stellt eine Besprechungsantwort im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="97b8b-137">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="97b8b-138">Message</span><span class="sxs-lookup"><span data-stu-id="97b8b-138">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="97b8b-139">Stellt eine Exchange-E-Mail-Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="97b8b-139">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="97b8b-140">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="97b8b-140">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="97b8b-141">Entfernt ein Element aus dem Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="97b8b-141">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="97b8b-142">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="97b8b-142">Task</span></span>](task.md) <br/> |<span data-ttu-id="97b8b-143">Stellt eine Aufgabe im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="97b8b-143">Represents a task in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="97b8b-144">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="97b8b-144">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="97b8b-145">Stellt einen Ordner, der in erster Linie Kalenderelemente enthält.</span><span class="sxs-lookup"><span data-stu-id="97b8b-145">Represents a folder that primarily contains calendar items.</span></span>  <br/> |
|[<span data-ttu-id="97b8b-146">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="97b8b-146">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="97b8b-147">Stellt einen Kontakteordner in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="97b8b-147">Represents a contacts folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="97b8b-148">Folder</span><span class="sxs-lookup"><span data-stu-id="97b8b-148">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="97b8b-149">Stellt einen Ordner zu erstellen, abrufen, suchen, synchronisieren oder zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="97b8b-149">Represents a folder to create, get, find, synchronize, or update.</span></span>  <br/> |
|[<span data-ttu-id="97b8b-150">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="97b8b-150">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="97b8b-151">Stellt einen Suchordner, der in einem Postfach enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="97b8b-151">Represents a search folder that is contained in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="97b8b-152">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="97b8b-152">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="97b8b-153">Stellt einen Aufgabenordner, der in einem Postfach enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="97b8b-153">Represents a tasks folder that is contained in a mailbox.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="97b8b-154">Hinweise</span><span class="sxs-lookup"><span data-stu-id="97b8b-154">Remarks</span></span>

<span data-ttu-id="97b8b-155">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="97b8b-155">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="97b8b-156">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="97b8b-156">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="97b8b-157">Namespace</span><span class="sxs-lookup"><span data-stu-id="97b8b-157">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="97b8b-158">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="97b8b-158">Schema Name</span></span>  <br/> |<span data-ttu-id="97b8b-159">Schematypen</span><span class="sxs-lookup"><span data-stu-id="97b8b-159">Types schema</span></span>  <br/> |
|<span data-ttu-id="97b8b-160">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="97b8b-160">Validation File</span></span>  <br/> |<span data-ttu-id="97b8b-161">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="97b8b-161">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="97b8b-162">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="97b8b-162">Can be Empty</span></span>  <br/> |<span data-ttu-id="97b8b-163">False</span><span class="sxs-lookup"><span data-stu-id="97b8b-163">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="97b8b-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="97b8b-164">See also</span></span>

- [<span data-ttu-id="97b8b-165">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="97b8b-165">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

