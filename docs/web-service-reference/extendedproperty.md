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
description: Das Extended-Element identifiziert erweiterte MAPI-Eigenschaften für Ordner und Elemente.
ms.openlocfilehash: 99ede097d803d6fbf534cde0e77c08cec054bfa3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530607"
---
# <a name="extendedproperty"></a><span data-ttu-id="548af-103">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="548af-103">ExtendedProperty</span></span>

<span data-ttu-id="548af-104">Das **Extended** -Element identifiziert erweiterte MAPI-Eigenschaften für Ordner und Elemente.</span><span class="sxs-lookup"><span data-stu-id="548af-104">The **ExtendedProperty** element identifies extended MAPI properties on folders and items.</span></span> 
  
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

<span data-ttu-id="548af-105">**Extendedpropertytype Schematyp**</span><span class="sxs-lookup"><span data-stu-id="548af-105">**ExtendedPropertyType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="548af-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="548af-106">Attributes and elements</span></span>

<span data-ttu-id="548af-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="548af-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="548af-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="548af-108">Attributes</span></span>

<span data-ttu-id="548af-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="548af-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="548af-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="548af-110">Child elements</span></span>

|<span data-ttu-id="548af-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="548af-111">**Element**</span></span>|<span data-ttu-id="548af-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="548af-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="548af-113">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="548af-113">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="548af-114">Bezeichnet eine erweiterte MAPI-Eigenschaft, die abgerufen, festgelegt oder erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="548af-114">Identifies an extended MAPI property to get, set, or create.</span></span>  <br/> |
|[<span data-ttu-id="548af-115">Values</span><span class="sxs-lookup"><span data-stu-id="548af-115">Values</span></span>](values.md) <br/> |<span data-ttu-id="548af-116">Enthält eine Auflistung von Werten für eine mehrwertige erweiterte MAPI-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="548af-116">Contains a collection of values for a multivalued extended MAPI property.</span></span>  <br/> |
|[<span data-ttu-id="548af-117">Wert</span><span class="sxs-lookup"><span data-stu-id="548af-117">Value</span></span>](value.md) <br/> |<span data-ttu-id="548af-118">Enthält den Wert der erweiterten einwertigen MAPI-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="548af-118">Contains the value of single-valued MAPI extended property.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="548af-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="548af-119">Parent elements</span></span>

|<span data-ttu-id="548af-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="548af-120">**Element**</span></span>|<span data-ttu-id="548af-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="548af-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="548af-122">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="548af-122">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="548af-123">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="548af-123">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="548af-124">Kontaktperson</span><span class="sxs-lookup"><span data-stu-id="548af-124">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="548af-125">Stellt ein Exchange-Kontaktelement dar.</span><span class="sxs-lookup"><span data-stu-id="548af-125">Represents an Exchange contact item.</span></span>  <br/> |
|[<span data-ttu-id="548af-126">DistributionList</span><span class="sxs-lookup"><span data-stu-id="548af-126">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="548af-127">Stellt eine Verteilerliste dar.</span><span class="sxs-lookup"><span data-stu-id="548af-127">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="548af-128">Element</span><span class="sxs-lookup"><span data-stu-id="548af-128">Item</span></span>](item.md) <br/> |<span data-ttu-id="548af-129">Stellt ein Element im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="548af-129">Represents an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="548af-130">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="548af-130">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="548af-131">Stellt eine Besprechungsabsage im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="548af-131">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="548af-132">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="548af-132">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="548af-133">Stellt eine Besprechung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="548af-133">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="548af-134">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="548af-134">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="548af-135">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="548af-135">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="548af-136">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="548af-136">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="548af-137">Stellt eine Besprechungsantwort im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="548af-137">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="548af-138">Message</span><span class="sxs-lookup"><span data-stu-id="548af-138">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="548af-139">Stellt eine Exchange-E-Mail-Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="548af-139">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="548af-140">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="548af-140">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="548af-141">Entfernt ein Element aus dem Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="548af-141">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="548af-142">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="548af-142">Task</span></span>](task.md) <br/> |<span data-ttu-id="548af-143">Stellt eine Aufgabe im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="548af-143">Represents a task in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="548af-144">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="548af-144">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="548af-145">Stellt einen Ordner dar, der in erster Linie Kalenderelemente enthält.</span><span class="sxs-lookup"><span data-stu-id="548af-145">Represents a folder that primarily contains calendar items.</span></span>  <br/> |
|[<span data-ttu-id="548af-146">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="548af-146">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="548af-147">Stellt einen Ordner Kontakte in einem Postfach dar.</span><span class="sxs-lookup"><span data-stu-id="548af-147">Represents a contacts folder in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="548af-148">Ordner</span><span class="sxs-lookup"><span data-stu-id="548af-148">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="548af-149">Stellt einen Ordner zum Erstellen, abrufen, suchen, synchronisieren oder aktualisieren dar.</span><span class="sxs-lookup"><span data-stu-id="548af-149">Represents a folder to create, get, find, synchronize, or update.</span></span>  <br/> |
|[<span data-ttu-id="548af-150">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="548af-150">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="548af-151">Stellt einen Suchordner dar, der in einem Postfach enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="548af-151">Represents a search folder that is contained in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="548af-152">TasksFolder</span><span class="sxs-lookup"><span data-stu-id="548af-152">TasksFolder</span></span>](tasksfolder.md) <br/> |<span data-ttu-id="548af-153">Stellt einen Aufgabenordner dar, der in einem Postfach enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="548af-153">Represents a tasks folder that is contained in a mailbox.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="548af-154">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="548af-154">Remarks</span></span>

<span data-ttu-id="548af-155">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="548af-155">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="548af-156">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="548af-156">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="548af-157">Namespace</span><span class="sxs-lookup"><span data-stu-id="548af-157">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="548af-158">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="548af-158">Schema Name</span></span>  <br/> |<span data-ttu-id="548af-159">Schematypen</span><span class="sxs-lookup"><span data-stu-id="548af-159">Types schema</span></span>  <br/> |
|<span data-ttu-id="548af-160">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="548af-160">Validation File</span></span>  <br/> |<span data-ttu-id="548af-161">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="548af-161">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="548af-162">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="548af-162">Can be Empty</span></span>  <br/> |<span data-ttu-id="548af-163">False</span><span class="sxs-lookup"><span data-stu-id="548af-163">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="548af-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="548af-164">See also</span></span>

- [<span data-ttu-id="548af-165">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="548af-165">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

