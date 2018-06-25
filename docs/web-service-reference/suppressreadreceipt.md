---
title: SuppressReadReceipt
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SuppressReadReceipt
api_type:
- schema
ms.assetid: fc09bcc2-c003-4322-8315-d929bd0a9e2e
description: Das Element SuppressReadReceipt wird verwendet, um lesebestätigungen zu unterdrücken.
ms.openlocfilehash: de2eef68abd25c8208530ba5e98ab3278c8702d1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839140"
---
# <a name="suppressreadreceipt"></a><span data-ttu-id="d3ee9-103">SuppressReadReceipt</span><span class="sxs-lookup"><span data-stu-id="d3ee9-103">SuppressReadReceipt</span></span>

<span data-ttu-id="d3ee9-104">Das Element **SuppressReadReceipt** wird verwendet, um lesebestätigungen zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="d3ee9-104">The **SuppressReadReceipt** element is used to suppress read receipts.</span></span> 
  
```xml
<SuppressReadReceipt>
   <ReferenceItemId/>
</SuppressReadReceipt>
```

 <span data-ttu-id="d3ee9-105">**SuppressReadReceiptType**</span><span class="sxs-lookup"><span data-stu-id="d3ee9-105">**SuppressReadReceiptType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d3ee9-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d3ee9-106">Attributes and elements</span></span>

<span data-ttu-id="d3ee9-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d3ee9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d3ee9-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d3ee9-108">Attributes</span></span>

<span data-ttu-id="d3ee9-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="d3ee9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d3ee9-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d3ee9-110">Child elements</span></span>

|<span data-ttu-id="d3ee9-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="d3ee9-111">**Element**</span></span>|<span data-ttu-id="d3ee9-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d3ee9-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d3ee9-113">ReferenceItemId</span><span class="sxs-lookup"><span data-stu-id="d3ee9-113">ReferenceItemId</span></span>](referenceitemid.md) <br/> |<span data-ttu-id="d3ee9-114">Identifiziert das Element auf dem im Response-Objekt verweist.</span><span class="sxs-lookup"><span data-stu-id="d3ee9-114">Identifies the item to which the response object refers.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d3ee9-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d3ee9-115">Parent elements</span></span>

|<span data-ttu-id="d3ee9-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="d3ee9-116">**Element**</span></span>|<span data-ttu-id="d3ee9-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d3ee9-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d3ee9-118">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="d3ee9-118">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> | <span data-ttu-id="d3ee9-119">Werden alle Elemente, die an eine Besprechungszeit angrenzen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d3ee9-119">Describes all items that are adjacent to a meeting time.</span></span>  <br/><br/>  <span data-ttu-id="d3ee9-120">Im folgenden sind einige der XPath-Ausdrücke auf dieses Element:</span><span class="sxs-lookup"><span data-stu-id="d3ee9-120">The following are some of the XPath expressions to this element:</span></span><br/>  <br/>  `/CalendarItem/AdjacentMeetings` <br/>  `/MeetingRequest/AdjacentMeetings` <br/>  `/SetItemField/CalendarItem/AdjacentMeetings` <br/>  `/AppendToItemField/CalendarItem/AdjacentMeetings` <br/>  `/AcceptItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/DeclineItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/TentativelyAcceptItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/SetItemField/CalendarItem/AdjacentMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/AppendToItemField/CalendarItem/AdjacentMeetings` <br/>  `/CreateAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/GetAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/> |
|[<span data-ttu-id="d3ee9-121">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="d3ee9-121">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> | <span data-ttu-id="d3ee9-122">Beschreibt alle Elemente, die mit einem bestimmten Zeitpunkt treffen in Konflikt stehen.</span><span class="sxs-lookup"><span data-stu-id="d3ee9-122">Describes all items that conflict with a meeting time.</span></span> <br/> <br/>  <span data-ttu-id="d3ee9-123">Im folgenden sind einige der XPath-Ausdrücke auf dieses Element:</span><span class="sxs-lookup"><span data-stu-id="d3ee9-123">The following are some of the XPath expressions to this element:</span></span> <br/> <br/>  `/CalendarItem/ConflictingMeetings` <br/>  `/MeetingRequest/ConflictingMeetings` <br/>  `/SetItemField/CalendarItem/ConflictingMeetings` <br/>  `/AppendToItemField/CalendarItem/ConflictingMeetings` <br/>  `/AcceptItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/DeclineItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/TentativelyAcceptItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/SetItemField/CalendarItem/ConflictingMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/AppendToItemField/CalendarItem/ConflictingMeetings` <br/>  `/CreateAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/GetAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/> |
|[<span data-ttu-id="d3ee9-124">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="d3ee9-124">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="d3ee9-125">Enthält eine Auflistung aller Antwort-Objekte, die ein Element in der Exchange-Informationsspeicher zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d3ee9-125">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="d3ee9-126">Elemente (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="d3ee9-126">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="d3ee9-127">Enthält ein Array von Elementen im Ordner zu erstellen, die durch das Element [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="d3ee9-127">Contains an array of items to create in the folder that is identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d3ee9-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d3ee9-128">Remarks</span></span>

<span data-ttu-id="d3ee9-129">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="d3ee9-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d3ee9-130">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="d3ee9-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d3ee9-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="d3ee9-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d3ee9-132">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d3ee9-132">Schema Name</span></span>  <br/> |<span data-ttu-id="d3ee9-133">Schematypen</span><span class="sxs-lookup"><span data-stu-id="d3ee9-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="d3ee9-134">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d3ee9-134">Validation File</span></span>  <br/> |<span data-ttu-id="d3ee9-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d3ee9-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d3ee9-136">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d3ee9-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="d3ee9-137">False</span><span class="sxs-lookup"><span data-stu-id="d3ee9-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d3ee9-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d3ee9-138">See also</span></span>

- [<span data-ttu-id="d3ee9-139">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="d3ee9-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

