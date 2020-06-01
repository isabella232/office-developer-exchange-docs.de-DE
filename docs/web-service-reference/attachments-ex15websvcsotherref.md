---
title: Anlagen
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Attachments
api_type:
- schema
ms.assetid: b470e614-34bb-44f0-8790-7ddbdcbbd29d
description: Das Attachments-Element enthält die Elemente oder Dateien, die an ein Element im Exchange-Informationsspeicher angefügt sind.
ms.openlocfilehash: a9f79cd79f19e6226703c99c53c91efed600f495
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461534"
---
# <a name="attachments"></a><span data-ttu-id="0079f-103">Anlagen</span><span class="sxs-lookup"><span data-stu-id="0079f-103">Attachments</span></span>

<span data-ttu-id="0079f-104">Das **Attachments** -Element enthält die Elemente oder Dateien, die an ein Element im Exchange-Informationsspeicher angefügt sind.</span><span class="sxs-lookup"><span data-stu-id="0079f-104">The **Attachments** element contains the items or files that are attached to an item in the Exchange store.</span></span> 
  
```xml
<Attachments>
   <ItemAttachment/>
   <FileAttachment/>
</Attachments>
```

 <span data-ttu-id="0079f-105">**ArrayOfAttachmentsType** und **NonEmptyArrayOfAttachmentsType**</span><span class="sxs-lookup"><span data-stu-id="0079f-105">**ArrayOfAttachmentsType** and **NonEmptyArrayOfAttachmentsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0079f-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="0079f-106">Attributes and elements</span></span>

<span data-ttu-id="0079f-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="0079f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0079f-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="0079f-108">Attributes</span></span>

<span data-ttu-id="0079f-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="0079f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0079f-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0079f-110">Child elements</span></span>

|<span data-ttu-id="0079f-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="0079f-111">**Element**</span></span>|<span data-ttu-id="0079f-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0079f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0079f-113">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="0079f-113">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="0079f-114">Stellt ein Exchange-Element dar, das an ein anderes Exchange-Element angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="0079f-114">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="0079f-115">FileAttachment</span><span class="sxs-lookup"><span data-stu-id="0079f-115">FileAttachment</span></span>](fileattachment.md) <br/> |<span data-ttu-id="0079f-116">Stellt eine Datei dar, die an ein Element im Exchange-Informationsspeicher angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="0079f-116">Represents a file that is attached to an item in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0079f-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0079f-117">Parent elements</span></span>

|<span data-ttu-id="0079f-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="0079f-118">**Element**</span></span>|<span data-ttu-id="0079f-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0079f-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0079f-120">CreateAttachment</span><span class="sxs-lookup"><span data-stu-id="0079f-120">CreateAttachment</span></span>](createattachment.md) <br/> |<span data-ttu-id="0079f-121">Definiert eine Anforderung zum Erstellen einer Anlage für ein Element in der Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="0079f-121">Defines a request to create an attachment to an item in the Exchange store.</span></span><br/><br/> <span data-ttu-id="0079f-122">Im folgenden finden Sie den XPath-Ausdruck für dieses Element:`/CreateAttachment`</span><span class="sxs-lookup"><span data-stu-id="0079f-122">The following is the XPath expression to this element:  `/CreateAttachment`</span></span> <br/> |
|[<span data-ttu-id="0079f-123">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="0079f-123">AcceptItem</span></span>](acceptitem.md) <br/> | <span data-ttu-id="0079f-124">Stellt eine Accept-Antwort auf eine Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="0079f-124">Represents an Accept reply to a meeting request.</span></span><br/><br/><span data-ttu-id="0079f-125">Im folgenden finden Sie einige der XPath-Ausdrücke für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="0079f-125">The following are some of the XPath expressions to this element:</span></span><ul><li>`/CreateItem/Items`</li><li>`/MeetingRequest/ConflictingMeetings` </li><li>`/SetItemField/CalendarItem/ConflictingMeetings`</li><li>`/AppendToItemField/CalendarItem/ConflictingMeetings`</li><li>`/AcceptItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings`</li><li>`/DeclineItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings`</li><li>`/UpdateItem/ItemChanges/ItemChange/Updates/AppendToItemField/CalendarItem/AdjacentMeetings`</li><li>`/CreateAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings`</li><li>`/GetAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings`</li></ul> |
|[<span data-ttu-id="0079f-126">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="0079f-126">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="0079f-127">Stellt eine ablehnen Antwort auf eine Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="0079f-127">Represents a Decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="0079f-128">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="0079f-128">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="0079f-129">Stellt eine mit Vorbehalt Antworten auf eine Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="0079f-129">Represents a Tentative reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="0079f-130">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="0079f-130">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="0079f-131">Entfernt ein Element aus dem Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="0079f-131">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="0079f-132">Element</span><span class="sxs-lookup"><span data-stu-id="0079f-132">Item</span></span>](item.md) <br/> |<span data-ttu-id="0079f-133">Stellt ein generisches Exchange-Element dar.</span><span class="sxs-lookup"><span data-stu-id="0079f-133">Represents a generic Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="0079f-134">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="0079f-134">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="0079f-135">Stellt eine Besprechung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="0079f-135">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="0079f-136">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="0079f-136">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="0079f-137">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="0079f-137">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="0079f-138">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="0079f-138">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="0079f-139">Stellt eine Besprechungsantwort im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="0079f-139">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="0079f-140">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="0079f-140">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="0079f-141">Stellt eine Besprechungsabsage im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="0079f-141">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="0079f-142">Message</span><span class="sxs-lookup"><span data-stu-id="0079f-142">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="0079f-143">Stellt eine Exchange-E-Mail-Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="0079f-143">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="0079f-144">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="0079f-144">Task</span></span>](task.md) <br/> |<span data-ttu-id="0079f-145">Stellt eine Aufgabe im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="0079f-145">Represents a task in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="0079f-146">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="0079f-146">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="0079f-147">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="0079f-147">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="0079f-148">Kontaktperson</span><span class="sxs-lookup"><span data-stu-id="0079f-148">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="0079f-149">Stellt ein Exchange-Kontaktelement dar.</span><span class="sxs-lookup"><span data-stu-id="0079f-149">Represents an Exchange contact item.</span></span>  <br/> |
|[<span data-ttu-id="0079f-150">DistributionList</span><span class="sxs-lookup"><span data-stu-id="0079f-150">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="0079f-151">Stellt eine Verteilerliste dar.</span><span class="sxs-lookup"><span data-stu-id="0079f-151">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="0079f-152">CreateAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="0079f-152">CreateAttachmentResponseMessage</span></span>](createattachmentresponsemessage.md) <br/> |<span data-ttu-id="0079f-153">Enthält den Status und das Ergebnis einer einzelnen CreateAttachment-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="0079f-153">Contains the status and result of a single CreateAttachment request.</span></span>  <br/> |
|[<span data-ttu-id="0079f-154">GetAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="0079f-154">GetAttachmentResponseMessage</span></span>](getattachmentresponsemessage.md) <br/> |<span data-ttu-id="0079f-155">Enthält den Status und das Ergebnis einer GetAttachment-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="0079f-155">Contains the status and result of a GetAttachment request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0079f-156">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0079f-156">Remarks</span></span>

<span data-ttu-id="0079f-157">Die **Attachments** -Elemente weisen dieselben untergeordneten Elemente auf, basieren jedoch auf unterschiedlichen Typen: **ArrayOfAttachmentsType** und **NonEmptyArrayOfAttachmentsType**.</span><span class="sxs-lookup"><span data-stu-id="0079f-157">The **Attachments** elements have the same child elements but are based on different types: **ArrayOfAttachmentsType** and **NonEmptyArrayOfAttachmentsType**.</span></span> <span data-ttu-id="0079f-158">Die Typen definieren, ob ein untergeordnetes Element erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="0079f-158">The types define whether a child element is required.</span></span> <span data-ttu-id="0079f-159">Das **ArrayOfAttachmentsType** wird nur in der Antwortnachricht verwendet.</span><span class="sxs-lookup"><span data-stu-id="0079f-159">The **ArrayOfAttachmentsType** is only used in the response message.</span></span> <span data-ttu-id="0079f-160">Beachten Sie auch, dass diese Elemente sowohl im Messages-als auch im types-Namespace vorkommen.</span><span class="sxs-lookup"><span data-stu-id="0079f-160">It is also important to note that these elements occur in both the messages and types namespaces.</span></span> 
  
<span data-ttu-id="0079f-161">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="0079f-161">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0079f-162">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="0079f-162">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0079f-163">Namespace</span><span class="sxs-lookup"><span data-stu-id="0079f-163">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0079f-164">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="0079f-164">Schema Name</span></span>  <br/> |<span data-ttu-id="0079f-165">Schematypen</span><span class="sxs-lookup"><span data-stu-id="0079f-165">Types schema</span></span>  <br/> |
|<span data-ttu-id="0079f-166">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="0079f-166">Validation File</span></span>  <br/> |<span data-ttu-id="0079f-167">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0079f-167">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0079f-168">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="0079f-168">Can be Empty</span></span>  <br/> |<span data-ttu-id="0079f-169">False</span><span class="sxs-lookup"><span data-stu-id="0079f-169">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0079f-170">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0079f-170">See also</span></span>

- [<span data-ttu-id="0079f-171">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="0079f-171">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

