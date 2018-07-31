---
title: Create (ItemSync)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Create
api_type:
- schema
ms.assetid: cb5e64a2-66a5-4447-921e-7c13efb8f6bf
description: Das Create-Element identifiziert ein einzelnes Element in der lokalen Client-Speicher zu erstellen.
ms.openlocfilehash: d49e54c64f7bd53dcb296d998a856c20570d81be
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353945"
---
# <a name="create-itemsync"></a><span data-ttu-id="6540a-103">Create (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="6540a-103">Create (ItemSync)</span></span>

<span data-ttu-id="6540a-104">Das **Create** -Element identifiziert ein einzelnes Element in der lokalen Client-Speicher zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6540a-104">The **Create** element identifies a single item to create in the local client store.</span></span> 
  
- [<span data-ttu-id="6540a-105">SyncFolderItemsResponse</span><span class="sxs-lookup"><span data-stu-id="6540a-105">SyncFolderItemsResponse</span></span>](syncfolderitemsresponse.md) 
- [<span data-ttu-id="6540a-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="6540a-106">ResponseMessages</span></span>](responsemessages.md) 
- [<span data-ttu-id="6540a-107">SyncFolderItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="6540a-107">SyncFolderItemsResponseMessage</span></span>](syncfolderitemsresponsemessage.md) 
- [<span data-ttu-id="6540a-108">Änderungen (Elemente)</span><span class="sxs-lookup"><span data-stu-id="6540a-108">Changes (Items)</span></span>](changes-items.md) 
- [<span data-ttu-id="6540a-109">Create (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="6540a-109">Create (ItemSync)</span></span>](create-itemsync.md)
  
```xml
<Create>
   <Item/>
</Create>
```

```xml
<Create>
   <Task/> 
</Create>
```

```xml
<Create>
   <MeetingResponse/>
</Create>
```

```xml
<Create>
   <CalendarItem/>
</Create>
```

```xml
<Create>
   <MeetingMessage/>
</Create>
```

```xml
<Create>
   <DistributionList/>
</Create>
```

```xml
<Create>
   <MeetingCancellation/>
</Create>
```

```xml
<Create>
   <MeetingRequest/> 
</Create>
```

```xml
<Create>
   <Message/> 
</Create>
```

```xml
<Create>
   <Contact/> 
</Create>
```

<span data-ttu-id="6540a-110">**SyncFolderItemsCreateOrUpdateType**</span><span class="sxs-lookup"><span data-stu-id="6540a-110">**SyncFolderItemsCreateOrUpdateType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="6540a-111">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="6540a-111">Attributes and elements</span></span>

<span data-ttu-id="6540a-112">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="6540a-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6540a-113">Attribute</span><span class="sxs-lookup"><span data-stu-id="6540a-113">Attributes</span></span>

<span data-ttu-id="6540a-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="6540a-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6540a-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6540a-115">Child elements</span></span>

|<span data-ttu-id="6540a-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="6540a-116">**Element**</span></span>|<span data-ttu-id="6540a-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6540a-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6540a-118">Item</span><span class="sxs-lookup"><span data-stu-id="6540a-118">Item</span></span>](item.md) <br/> |<span data-ttu-id="6540a-119">So erstellen Sie ein generisches Exchange-Element darstellt.</span><span class="sxs-lookup"><span data-stu-id="6540a-119">Represents a generic Exchange item to create.</span></span>  <br/> |
|[<span data-ttu-id="6540a-120">Meldung</span><span class="sxs-lookup"><span data-stu-id="6540a-120">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="6540a-121">So erstellen Sie eine Exchange E-mail-Nachricht darstellt.</span><span class="sxs-lookup"><span data-stu-id="6540a-121">Represents an Exchange e-mail message to create.</span></span>  <br/> |
|[<span data-ttu-id="6540a-122">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="6540a-122">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="6540a-123">So erstellen Sie ein Exchange-Kalender-Element darstellt.</span><span class="sxs-lookup"><span data-stu-id="6540a-123">Represents an Exchange calendar item to create.</span></span>  <br/> |
|[<span data-ttu-id="6540a-124">Contact</span><span class="sxs-lookup"><span data-stu-id="6540a-124">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="6540a-125">So erstellen Sie ein Exchange-Kontaktelement darstellt.</span><span class="sxs-lookup"><span data-stu-id="6540a-125">Represents an Exchange contact item to create.</span></span>  <br/> |
|[<span data-ttu-id="6540a-126">DistributionList</span><span class="sxs-lookup"><span data-stu-id="6540a-126">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="6540a-127">So erstellen Sie eine Verteilerliste darstellt.</span><span class="sxs-lookup"><span data-stu-id="6540a-127">Represents a distribution list to create.</span></span>  <br/> |
|[<span data-ttu-id="6540a-128">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="6540a-128">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="6540a-129">Stellt eine Besprechungsnachricht zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6540a-129">Represents a meeting message to create.</span></span>  <br/> |
|[<span data-ttu-id="6540a-130">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="6540a-130">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="6540a-131">So erstellen Sie eine Besprechungsanfrage darstellt.</span><span class="sxs-lookup"><span data-stu-id="6540a-131">Represents a meeting request to create.</span></span>  <br/> |
|[<span data-ttu-id="6540a-132">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="6540a-132">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="6540a-133">So erstellen Sie eine Antwort auf Besprechungsanfrage darstellt.</span><span class="sxs-lookup"><span data-stu-id="6540a-133">Represents a meeting response to create.</span></span>  <br/> |
|[<span data-ttu-id="6540a-134">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="6540a-134">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="6540a-135">So erstellen Sie einen Besprechungsabsage darstellt.</span><span class="sxs-lookup"><span data-stu-id="6540a-135">Represents a meeting cancellation to create.</span></span>  <br/> |
|[<span data-ttu-id="6540a-136">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="6540a-136">Task</span></span>](task.md) <br/> |<span data-ttu-id="6540a-137">So erstellen Sie eine Aufgabe darstellt.</span><span class="sxs-lookup"><span data-stu-id="6540a-137">Represents a task to create.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6540a-138">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6540a-138">Parent elements</span></span>

|<span data-ttu-id="6540a-139">**Element**</span><span class="sxs-lookup"><span data-stu-id="6540a-139">**Element**</span></span>|<span data-ttu-id="6540a-140">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6540a-140">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6540a-141">Änderungen (Elemente)</span><span class="sxs-lookup"><span data-stu-id="6540a-141">Changes (Items)</span></span>](changes-items.md) <br/> |<span data-ttu-id="6540a-142">Enthält ein Array Sequenz von Dateitypen ändern, die die Typen der Unterschiede zwischen den Elementen auf dem Client und der Elemente auf dem Exchange-Server darstellen.</span><span class="sxs-lookup"><span data-stu-id="6540a-142">Contains a sequence array of change types that represent the types of differences between the items on the client and the items on the Exchange server.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6540a-143">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6540a-143">Remarks</span></span>

<span data-ttu-id="6540a-144">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="6540a-144">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6540a-145">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="6540a-145">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6540a-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="6540a-146">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6540a-147">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="6540a-147">Schema name</span></span>  <br/> |<span data-ttu-id="6540a-148">Schematypen</span><span class="sxs-lookup"><span data-stu-id="6540a-148">Types schema</span></span>  <br/> |
|<span data-ttu-id="6540a-149">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="6540a-149">Validation file</span></span>  <br/> |<span data-ttu-id="6540a-150">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6540a-150">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6540a-151">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="6540a-151">Can be empty</span></span>  <br/> |<span data-ttu-id="6540a-152">False</span><span class="sxs-lookup"><span data-stu-id="6540a-152">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6540a-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6540a-153">See also</span></span>

- [<span data-ttu-id="6540a-154">SyncFolderItems-Vorgang</span><span class="sxs-lookup"><span data-stu-id="6540a-154">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)
- [<span data-ttu-id="6540a-155">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="6540a-155">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

