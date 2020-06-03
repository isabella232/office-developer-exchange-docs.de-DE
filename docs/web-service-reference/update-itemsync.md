---
title: Update (ItemSync)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Update
api_type:
- schema
ms.assetid: 4e204446-1c80-44f9-b93b-77ce630a01a5
description: Das Update-Element identifiziert ein einzelnes Element, das im lokalen Clientspeicher aktualisiert werden soll.
ms.openlocfilehash: 12248cbbd5d47a19e36d49fcebe6d4753a2e162f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468887"
---
# <a name="update-itemsync"></a><span data-ttu-id="65d22-103">Update (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="65d22-103">Update (ItemSync)</span></span>

<span data-ttu-id="65d22-104">Das **Update** -Element identifiziert ein einzelnes Element, das im lokalen Clientspeicher aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="65d22-104">The **Update** element identifies a single item to update in the local client store.</span></span> 
  
- [<span data-ttu-id="65d22-105">SyncFolderItemsResponse</span><span class="sxs-lookup"><span data-stu-id="65d22-105">SyncFolderItemsResponse</span></span>](syncfolderitemsresponse.md) 
- [<span data-ttu-id="65d22-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="65d22-106">ResponseMessages</span></span>](responsemessages.md)  
- [<span data-ttu-id="65d22-107">SyncFolderItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="65d22-107">SyncFolderItemsResponseMessage</span></span>](syncfolderitemsresponsemessage.md)  
- [<span data-ttu-id="65d22-108">Änderungen (Elemente)</span><span class="sxs-lookup"><span data-stu-id="65d22-108">Changes (Items)</span></span>](changes-items.md)  
- [<span data-ttu-id="65d22-109">Update (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="65d22-109">Update (ItemSync)</span></span>](update-itemsync.md)
  
```xml
<Update>
   <Item/>
</Update>
```

```xml
<Update>
   <MeetingRequest/>
</Update>
```

```xml
<Update>
   <MeetingCancellation/>
</Update>
```

```xml
<Update>
   <Task/>
</Update>
```

```xml
<Update>
   <CalendarItem/>
</Update>
```

```xml
<Update>
   <MeetingResponse/>
</Update>
```

```xml
<Update>
   <Message/>
</Update>
```

```xml
<Update>
   <DistributionList/>
</Update>
```

```xml
<Update>
   <MeetingMessage/>
</Update>
```

```xml
<Update>
   <Contact/> 
</Update>
```

<span data-ttu-id="65d22-110">**SyncFolderItemsCreateOrUpdateType**</span><span class="sxs-lookup"><span data-stu-id="65d22-110">**SyncFolderItemsCreateOrUpdateType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="65d22-111">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="65d22-111">Attributes and elements</span></span>

<span data-ttu-id="65d22-112">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="65d22-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="65d22-113">Attribute</span><span class="sxs-lookup"><span data-stu-id="65d22-113">Attributes</span></span>

<span data-ttu-id="65d22-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="65d22-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="65d22-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="65d22-115">Child elements</span></span>

|<span data-ttu-id="65d22-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="65d22-116">**Element**</span></span>|<span data-ttu-id="65d22-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="65d22-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="65d22-118">Item</span><span class="sxs-lookup"><span data-stu-id="65d22-118">Item</span></span>](item.md) <br/> |<span data-ttu-id="65d22-119">Stellt ein generisches Exchange-Element dar, das aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="65d22-119">Represents a generic Exchange item to update.</span></span>  <br/> |
|[<span data-ttu-id="65d22-120">Meldung</span><span class="sxs-lookup"><span data-stu-id="65d22-120">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="65d22-121">Stellt eine zu aktualisierenden Exchange-e-Mail-Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="65d22-121">Represents an Exchange e-mail message to update.</span></span>  <br/> |
|[<span data-ttu-id="65d22-122">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="65d22-122">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="65d22-123">Stellt ein zu aktualisieres Exchange-Kalenderelement dar.</span><span class="sxs-lookup"><span data-stu-id="65d22-123">Represents an Exchange calendar item to update.</span></span>  <br/> |
|[<span data-ttu-id="65d22-124">Contact</span><span class="sxs-lookup"><span data-stu-id="65d22-124">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="65d22-125">Stellt ein zu aktualisieres Exchange-Kontaktelement dar.</span><span class="sxs-lookup"><span data-stu-id="65d22-125">Represents an Exchange contact item to update.</span></span>  <br/> |
|[<span data-ttu-id="65d22-126">DistributionList</span><span class="sxs-lookup"><span data-stu-id="65d22-126">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="65d22-127">Stellt eine zu aktualisierende Verteilerliste dar.</span><span class="sxs-lookup"><span data-stu-id="65d22-127">Represents a distribution list to update.</span></span>  <br/> |
|[<span data-ttu-id="65d22-128">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="65d22-128">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="65d22-129">Stellt eine zu aktualisierende Besprechungs Meldung dar.</span><span class="sxs-lookup"><span data-stu-id="65d22-129">Represents a meeting message to update.</span></span>  <br/> |
|[<span data-ttu-id="65d22-130">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="65d22-130">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="65d22-131">Stellt eine Besprechungsanfrage zum Aktualisieren dar.</span><span class="sxs-lookup"><span data-stu-id="65d22-131">Represents a meeting request to update.</span></span>  <br/> |
|[<span data-ttu-id="65d22-132">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="65d22-132">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="65d22-133">Stellt eine Besprechungsantwort dar, die aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="65d22-133">Represents a meeting response to update.</span></span>  <br/> |
|[<span data-ttu-id="65d22-134">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="65d22-134">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="65d22-135">Stellt einen Besprechungs Abbruch dar, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="65d22-135">Represents a meeting cancellation to update.</span></span>  <br/> |
|[<span data-ttu-id="65d22-136">Task</span><span class="sxs-lookup"><span data-stu-id="65d22-136">Task</span></span>](task.md) <br/> |<span data-ttu-id="65d22-137">Stellt eine Aufgabe dar, die aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="65d22-137">Represents a task to update.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="65d22-138">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="65d22-138">Parent elements</span></span>

|<span data-ttu-id="65d22-139">**Element**</span><span class="sxs-lookup"><span data-stu-id="65d22-139">**Element**</span></span>|<span data-ttu-id="65d22-140">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="65d22-140">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="65d22-141">Änderungen (Elemente)</span><span class="sxs-lookup"><span data-stu-id="65d22-141">Changes (Items)</span></span>](changes-items.md) <br/> |<span data-ttu-id="65d22-142">Enthält ein Sequenz Array von Änderungstypen, die die Art der Unterschiede zwischen den Elementen auf dem Client und den Elementen auf dem Exchange-Server darstellen.</span><span class="sxs-lookup"><span data-stu-id="65d22-142">Contains a sequence array of change types that represent the type of differences between the items on the client and the items on the Exchange server.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="65d22-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="65d22-143">Remarks</span></span>

<span data-ttu-id="65d22-144">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="65d22-144">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="65d22-145">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="65d22-145">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="65d22-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="65d22-146">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="65d22-147">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="65d22-147">Schema name</span></span>  <br/> |<span data-ttu-id="65d22-148">Schematypen</span><span class="sxs-lookup"><span data-stu-id="65d22-148">Types schema</span></span>  <br/> |
|<span data-ttu-id="65d22-149">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="65d22-149">Validation file</span></span>  <br/> |<span data-ttu-id="65d22-150">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="65d22-150">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="65d22-151">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="65d22-151">Can be empty</span></span>  <br/> |<span data-ttu-id="65d22-152">False</span><span class="sxs-lookup"><span data-stu-id="65d22-152">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="65d22-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="65d22-153">See also</span></span>

- [<span data-ttu-id="65d22-154">SyncFolderItems-Vorgang</span><span class="sxs-lookup"><span data-stu-id="65d22-154">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)
- [<span data-ttu-id="65d22-155">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="65d22-155">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

