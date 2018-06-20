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
description: Das Update-Element identifiziert ein einzelnes Element in den Speicher des lokalen Client aktualisieren.
ms.openlocfilehash: ef1bd46906152affbe54372472766afc2a6ae8c1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839339"
---
# <a name="update-itemsync"></a><span data-ttu-id="28d28-103">Update (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="28d28-103">Update (ItemSync)</span></span>

<span data-ttu-id="28d28-104">**Update** -Elements gibt ein einzelnes Element in den Speicher des lokalen Client aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="28d28-104">The **Update** element identifies a single item to update in the local client store.</span></span> 
  
[<span data-ttu-id="28d28-105">SyncFolderItemsResponse</span><span class="sxs-lookup"><span data-stu-id="28d28-105">SyncFolderItemsResponse</span></span>](syncfolderitemsresponse.md)
  
[<span data-ttu-id="28d28-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="28d28-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="28d28-107">SyncFolderItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="28d28-107">SyncFolderItemsResponseMessage</span></span>](syncfolderitemsresponsemessage.md)
  
[<span data-ttu-id="28d28-108">Änderungen (Elemente)</span><span class="sxs-lookup"><span data-stu-id="28d28-108">Changes (Items)</span></span>](changes-items.md)
  
[<span data-ttu-id="28d28-109">Update (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="28d28-109">Update (ItemSync)</span></span>](update-itemsync.md)
  
```xml
<Update>
   <Item/>
</Update>
```

 <span data-ttu-id="28d28-110">**SyncFolderItemsCreateOrUpdateType**</span><span class="sxs-lookup"><span data-stu-id="28d28-110">**SyncFolderItemsCreateOrUpdateType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="28d28-111">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="28d28-111">Attributes and elements</span></span>

<span data-ttu-id="28d28-112">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="28d28-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="28d28-113">Attribute</span><span class="sxs-lookup"><span data-stu-id="28d28-113">Attributes</span></span>

<span data-ttu-id="28d28-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="28d28-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="28d28-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="28d28-115">Child elements</span></span>

|<span data-ttu-id="28d28-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="28d28-116">**Element**</span></span>|<span data-ttu-id="28d28-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="28d28-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="28d28-118">Item</span><span class="sxs-lookup"><span data-stu-id="28d28-118">Item</span></span>](item.md) <br/> |<span data-ttu-id="28d28-119">Stellt ein generisches Exchange-Element zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="28d28-119">Represents a generic Exchange item to update.</span></span>  <br/> |
|[<span data-ttu-id="28d28-120">Message</span><span class="sxs-lookup"><span data-stu-id="28d28-120">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="28d28-121">Stellt eine E-mail-Nachricht Exchange zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="28d28-121">Represents an Exchange e-mail message to update.</span></span>  <br/> |
|[<span data-ttu-id="28d28-122">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="28d28-122">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="28d28-123">Stellt ein Element des Exchange-Kalender zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="28d28-123">Represents an Exchange calendar item to update.</span></span>  <br/> |
|[<span data-ttu-id="28d28-124">Contact</span><span class="sxs-lookup"><span data-stu-id="28d28-124">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="28d28-125">Stellt ein Exchange-Kontaktelement zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="28d28-125">Represents an Exchange contact item to update.</span></span>  <br/> |
|[<span data-ttu-id="28d28-126">DistributionList</span><span class="sxs-lookup"><span data-stu-id="28d28-126">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="28d28-127">Stellt eine Verteilerliste aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="28d28-127">Represents a distribution list to update.</span></span>  <br/> |
|[<span data-ttu-id="28d28-128">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="28d28-128">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="28d28-129">Stellt eine Besprechungsnachricht zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="28d28-129">Represents a meeting message to update.</span></span>  <br/> |
|[<span data-ttu-id="28d28-130">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="28d28-130">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="28d28-131">So aktualisieren Sie eine Besprechungsanfrage darstellt.</span><span class="sxs-lookup"><span data-stu-id="28d28-131">Represents a meeting request to update.</span></span>  <br/> |
|[<span data-ttu-id="28d28-132">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="28d28-132">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="28d28-133">Stellt eine Antwort auf Besprechungsanfrage aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="28d28-133">Represents a meeting response to update.</span></span>  <br/> |
|[<span data-ttu-id="28d28-134">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="28d28-134">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="28d28-135">Aktualisieren einen Besprechungsabsage darstellt.</span><span class="sxs-lookup"><span data-stu-id="28d28-135">Represents a meeting cancellation to update.</span></span>  <br/> |
|[<span data-ttu-id="28d28-136">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="28d28-136">Task</span></span>](task.md) <br/> |<span data-ttu-id="28d28-137">Stellt eine Aufgabe zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="28d28-137">Represents a task to update.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="28d28-138">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="28d28-138">Parent elements</span></span>

|<span data-ttu-id="28d28-139">**Element**</span><span class="sxs-lookup"><span data-stu-id="28d28-139">**Element**</span></span>|<span data-ttu-id="28d28-140">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="28d28-140">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="28d28-141">Änderungen (Elemente)</span><span class="sxs-lookup"><span data-stu-id="28d28-141">Changes (Items)</span></span>](changes-items.md) <br/> |<span data-ttu-id="28d28-142">Enthält ein Array Sequenz von Dateitypen ändern, die den Typ der Unterschiede zwischen den Elementen auf dem Client und der Elemente auf dem Exchange-Server darstellen.</span><span class="sxs-lookup"><span data-stu-id="28d28-142">Contains a sequence array of change types that represent the type of differences between the items on the client and the items on the Exchange server.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="28d28-143">Hinweise</span><span class="sxs-lookup"><span data-stu-id="28d28-143">Remarks</span></span>

<span data-ttu-id="28d28-144">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="28d28-144">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="28d28-145">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="28d28-145">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="28d28-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="28d28-146">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="28d28-147">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="28d28-147">Schema name</span></span>  <br/> |<span data-ttu-id="28d28-148">Schematypen</span><span class="sxs-lookup"><span data-stu-id="28d28-148">Types schema</span></span>  <br/> |
|<span data-ttu-id="28d28-149">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="28d28-149">Validation file</span></span>  <br/> |<span data-ttu-id="28d28-150">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="28d28-150">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="28d28-151">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="28d28-151">Can be empty</span></span>  <br/> |<span data-ttu-id="28d28-152">False</span><span class="sxs-lookup"><span data-stu-id="28d28-152">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="28d28-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="28d28-153">See also</span></span>



[<span data-ttu-id="28d28-154">SyncFolderItems-Vorgang</span><span class="sxs-lookup"><span data-stu-id="28d28-154">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)


- [<span data-ttu-id="28d28-155">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="28d28-155">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

