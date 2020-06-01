---
title: SetItemField
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SetItemField
api_type:
- schema
ms.assetid: 85284fcb-bd1e-4fda-9dab-cb4cd637cd5b
description: Das setitemfield-Element stellt eine Aktualisierung auf eine einzelne Eigenschaft eines Elements in einer UpdateItem-Operation dar.
ms.openlocfilehash: b4606eb7d94b9d0c4c5bcd5a2b56d73a4d4270cb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467424"
---
# <a name="setitemfield"></a><span data-ttu-id="3fe03-103">SetItemField</span><span class="sxs-lookup"><span data-stu-id="3fe03-103">SetItemField</span></span>

<span data-ttu-id="3fe03-104">Das **setitemfield** -Element stellt eine Aktualisierung auf eine einzelne Eigenschaft eines Elements in einer [UpdateItem-Operation](updateitem-operation.md)dar.</span><span class="sxs-lookup"><span data-stu-id="3fe03-104">The **SetItemField** element represents an update to a single property of an item in an [UpdateItem operation](updateitem-operation.md).</span></span>
  
```xml
<SetItemField>
   <FieldURI/>
   <Item/>
</SetItemField>
```

```xml
<SetItemField>
   <ExtendedFieldURI/> 
   <Item/>
</SetItemField>
```

```xml
<SetItemField>
   <ExtendedFieldURI/> 
   <MeetingRequest/>
</SetItemField>
```

```xml
<SetItemField>
   <ExtendedFieldURI/> 
   <MeetingResponse/>
</SetItemField>
```

```xml
<SetItemField>
   <IndexedFieldURI/> 
   <Contact/>
</SetItemField>
```

```xml
<SetItemField>
   <IndexedFieldURI/> 
   <DistributionList/>
</SetItemField>
```

```xml
<SetItemField>
   <IndexedFieldURI/> 
   <MeetingResponse/>
</SetItemField>
```

```xml
<SetItemField>
   <FieldURI/> 
   <MeetingResponse/> 
</SetItemField>
```

```xml
<SetItemField>
   <FieldURI/> 
   <MeetingRequest/> 
</SetItemField>
```

```xml
<SetItemField>
   <FieldURI/> 
   <Contact/>
</SetItemField>
```

```xml
<SetItemField>
   <IndexedFieldURI/> 
   <Message/>
</SetItemField>
```

```xml
<SetItemField>
   <ExtendedFieldURI/> 
   <CalendarItem/>
</SetItemField>
```

```xml
<SetItemField>
   <ExtendedFieldURI/> 
   <Task/>
</SetItemField>
```

```xml
<SetItemField>
   <ExtendedFieldURI/> 
   <Message/> 
</SetItemField>
```

```xml
<SetItemField>
   <FieldURI/> 
   <MeetingCancellation/> 
</SetItemField>
```

```xml
<SetItemField>
   <FieldURI/> 
   <Task/> 
</SetItemField>
```

```xml
<SetItemField>
   <IndexedFieldURI/> 
   <MeetingRequest/>  
</SetItemField>
```

```xml
<SetItemField>
    <FieldURI/> 
    <CalendarItem/>
</SetItemField>
```

```xml
<SetItemField>
    <IndexedFieldURI/> 
    <Item/>
</SetItemField>
```

```xml
<SetItemField>
   <ExtendedFieldURI/> 
   <MeetingCancellation/>
</SetItemField>
```

```xml
<SetItemField>
   <FieldURI/> 
   <DistributionList/> 
</SetItemField>
```

```xml
<SetItemField>
   <IndexedFieldURI/> 
   <MeetingCancellation/>
</SetItemField>
```

```xml
<SetItemField>
   <ExtendedFieldURI/> 
   <MeetingMessage/>
</SetItemField>
```

```xml
<SetItemField>
   <IndexedFieldURI/> 
   <Task/> 
</SetItemField>
```

```xml
<SetItemField>
   <IndexedFieldURI/> 
   <CalendarItem/>
</SetItemField>
```

```xml
<SetItemField>
   <FieldURI/> 
   <MeetingMessage/>
</SetItemField>
```

```xml
<SetItemField>
   <IndexedFieldURI/> 
   <MeetingMessage/>
</SetItemField>
```

```xml
<SetItemField>
   <FieldURI/> 
   <Message/>
</SetItemField>
```

```xml
<SetItemField>
   <ExtendedFieldURI/> 
   <DistributionList/>
</SetItemField>
```

```xml
<SetItemField>
   <ExtendedFieldURI/> 
   <Contact/> 
</SetItemField>
```


<span data-ttu-id="3fe03-105">**SetItemFieldType**</span><span class="sxs-lookup"><span data-stu-id="3fe03-105">**SetItemFieldType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="3fe03-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3fe03-106">Attributes and elements</span></span>

<span data-ttu-id="3fe03-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="3fe03-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3fe03-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="3fe03-108">Attributes</span></span>

<span data-ttu-id="3fe03-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="3fe03-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3fe03-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3fe03-110">Child elements</span></span>

|<span data-ttu-id="3fe03-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="3fe03-111">**Element**</span></span>|<span data-ttu-id="3fe03-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3fe03-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3fe03-113">FieldURI</span><span class="sxs-lookup"><span data-stu-id="3fe03-113">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="3fe03-114">Identifiziert häufig referenzierte Eigenschaften nach URI.</span><span class="sxs-lookup"><span data-stu-id="3fe03-114">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="3fe03-115">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="3fe03-115">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="3fe03-116">Identifiziert einzelne Member eines Wörterbuchs.</span><span class="sxs-lookup"><span data-stu-id="3fe03-116">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="3fe03-117">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="3fe03-117">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="3fe03-118">Identifiziert erweiterte MAPI-Eigenschaften, die festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3fe03-118">Identifies extended MAPI properties to set.</span></span>  <br/> |
|[<span data-ttu-id="3fe03-119">Element</span><span class="sxs-lookup"><span data-stu-id="3fe03-119">Item</span></span>](item.md) <br/> |<span data-ttu-id="3fe03-120">Stellt ein Element im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="3fe03-120">Represents an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="3fe03-121">Nachricht</span><span class="sxs-lookup"><span data-stu-id="3fe03-121">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="3fe03-122">Stellt eine zu aktualisierenden Exchange-e-Mail-Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="3fe03-122">Represents an Exchange e-mail message to update.</span></span>  <br/> |
|[<span data-ttu-id="3fe03-123">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="3fe03-123">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="3fe03-124">Stellt ein zu aktualisieres Exchange-Kalenderelement dar.</span><span class="sxs-lookup"><span data-stu-id="3fe03-124">Represents an Exchange calendar item to update.</span></span>  <br/> |
|[<span data-ttu-id="3fe03-125">Kontakt</span><span class="sxs-lookup"><span data-stu-id="3fe03-125">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="3fe03-126">Stellt ein zu aktualisieres Exchange-Kontaktelement dar.</span><span class="sxs-lookup"><span data-stu-id="3fe03-126">Represents an Exchange contact item to update.</span></span>  <br/> |
|[<span data-ttu-id="3fe03-127">DistributionList</span><span class="sxs-lookup"><span data-stu-id="3fe03-127">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="3fe03-128">Stellt eine zu aktualisierende Verteilerliste dar.</span><span class="sxs-lookup"><span data-stu-id="3fe03-128">Represents a distribution list to update.</span></span>  <br/> |
|[<span data-ttu-id="3fe03-129">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="3fe03-129">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="3fe03-130">Stellt eine zu aktualisierende Besprechungs Meldung dar.</span><span class="sxs-lookup"><span data-stu-id="3fe03-130">Represents a meeting message to update.</span></span>  <br/> |
|[<span data-ttu-id="3fe03-131">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="3fe03-131">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="3fe03-132">Stellt eine Besprechungsanfrage zum Aktualisieren dar.</span><span class="sxs-lookup"><span data-stu-id="3fe03-132">Represents a meeting request to update.</span></span>  <br/> |
|[<span data-ttu-id="3fe03-133">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="3fe03-133">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="3fe03-134">Stellt eine Besprechungsantwort dar, die aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="3fe03-134">Represents a meeting response to update.</span></span>  <br/> |
|[<span data-ttu-id="3fe03-135">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="3fe03-135">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="3fe03-136">Stellt einen Besprechungs Abbruch dar, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="3fe03-136">Represents a meeting cancellation to update.</span></span>  <br/> |
|[<span data-ttu-id="3fe03-137">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="3fe03-137">Task</span></span>](task.md) <br/> |<span data-ttu-id="3fe03-138">Stellt eine Aufgabe dar, die aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="3fe03-138">Represents a task to update.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3fe03-139">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3fe03-139">Parent elements</span></span>

|<span data-ttu-id="3fe03-140">**Element**</span><span class="sxs-lookup"><span data-stu-id="3fe03-140">**Element**</span></span>|<span data-ttu-id="3fe03-141">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3fe03-141">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3fe03-142">Updates (Element)</span><span class="sxs-lookup"><span data-stu-id="3fe03-142">Updates (Item)</span></span>](updates-item.md) <br/> |<span data-ttu-id="3fe03-143">Enthält eine Gruppe von Elementen, die Append-, festlegen-und DELETE-Änderungen an Elementeigenschaften definieren.</span><span class="sxs-lookup"><span data-stu-id="3fe03-143">Contains a set of elements that define append, set, and delete changes to item properties.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3fe03-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3fe03-144">Remarks</span></span>

<span data-ttu-id="3fe03-145">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="3fe03-145">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3fe03-146">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="3fe03-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3fe03-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="3fe03-147">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3fe03-148">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="3fe03-148">Schema Name</span></span>  <br/> |<span data-ttu-id="3fe03-149">Schematypen</span><span class="sxs-lookup"><span data-stu-id="3fe03-149">Types schema</span></span>  <br/> |
|<span data-ttu-id="3fe03-150">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="3fe03-150">Validation File</span></span>  <br/> |<span data-ttu-id="3fe03-151">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3fe03-151">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3fe03-152">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="3fe03-152">Can be Empty</span></span>  <br/> |<span data-ttu-id="3fe03-153">False</span><span class="sxs-lookup"><span data-stu-id="3fe03-153">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3fe03-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3fe03-154">See also</span></span>

- [<span data-ttu-id="3fe03-155">UpdateItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="3fe03-155">UpdateItem operation</span></span>](updateitem-operation.md)

