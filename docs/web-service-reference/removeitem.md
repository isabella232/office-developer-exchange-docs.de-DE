---
title: RemoveItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RemoveItem
api_type:
- schema
ms.assetid: 766878e3-9007-454f-8501-45139bc5c0e2
description: Das RemoveItem-Element stellt ein Response-Objekt, das verwendet wird, um ein Besprechungselement zu entfernen, wenn eine Nachricht MeetingCancellation empfangen wird.
ms.openlocfilehash: 6897363eba602e6a135ad255822197f9296dd44a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831108"
---
# <a name="removeitem"></a><span data-ttu-id="3c13f-103">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="3c13f-103">RemoveItem</span></span>

<span data-ttu-id="3c13f-104">Das **RemoveItem** -Element stellt ein Response-Objekt, das verwendet wird, um ein Besprechungselement zu entfernen, wenn eine Nachricht MeetingCancellation empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="3c13f-104">The **RemoveItem** element represents a response object that is used to remove a meeting item when a MeetingCancellation message is received.</span></span> 
  
```xml
<RemoveItem ObjectName="">
   <ReferenceItemId/>
</RemoveItem>
```

 <span data-ttu-id="3c13f-105">**RemoveItemType**</span><span class="sxs-lookup"><span data-stu-id="3c13f-105">**RemoveItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3c13f-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3c13f-106">Attributes and elements</span></span>

<span data-ttu-id="3c13f-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="3c13f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3c13f-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="3c13f-108">Attributes</span></span>

|<span data-ttu-id="3c13f-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="3c13f-109">**Attribute**</span></span>|<span data-ttu-id="3c13f-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3c13f-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3c13f-111">**ObjectName**</span><span class="sxs-lookup"><span data-stu-id="3c13f-111">**ObjectName**</span></span> <br/> |<span data-ttu-id="3c13f-112">Stellt den Namen der RemoveItem Antwort Object-Klasse als eine englische Zeichenfolge dar.</span><span class="sxs-lookup"><span data-stu-id="3c13f-112">Represents the name of the RemoveItem reply object class as an English string.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="3c13f-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3c13f-113">Child elements</span></span>

|<span data-ttu-id="3c13f-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="3c13f-114">**Element**</span></span>|<span data-ttu-id="3c13f-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3c13f-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3c13f-116">ReferenceItemId</span><span class="sxs-lookup"><span data-stu-id="3c13f-116">ReferenceItemId</span></span>](referenceitemid.md) <br/> |<span data-ttu-id="3c13f-117">Identifiziert das Element auf dem RemoveItem-Response-Objekt verweist.</span><span class="sxs-lookup"><span data-stu-id="3c13f-117">Identifies the item to which the RemoveItem response object refers.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3c13f-118">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3c13f-118">Parent elements</span></span>

|<span data-ttu-id="3c13f-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="3c13f-119">**Element**</span></span>|<span data-ttu-id="3c13f-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3c13f-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3c13f-121">Elemente (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="3c13f-121">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="3c13f-122">Enthält ein Array von Elementen im Ordner zu erstellen, die durch das Element [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="3c13f-122">Contains an array of items to create in the folder that is identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
|[<span data-ttu-id="3c13f-123">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="3c13f-123">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="3c13f-124">Enthält eine Auflistung aller Antwort-Objekte, die ein Element in der Exchange-Informationsspeicher zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="3c13f-124">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3c13f-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3c13f-125">Remarks</span></span>

 <span data-ttu-id="3c13f-126">**RemoveItem** ist nur für eine [MeetingCancellation](meetingcancellation.md)gültig.</span><span class="sxs-lookup"><span data-stu-id="3c13f-126">**RemoveItem** is valid only for a [MeetingCancellation](meetingcancellation.md).</span></span> <span data-ttu-id="3c13f-127">Andernfalls wird ein Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="3c13f-127">Otherwise, an error is thrown.</span></span>
  
> [!NOTE]
> <span data-ttu-id="3c13f-128">Die [ItemClass](itemclass.md) für einen Besprechungsabsage lautet IPM. Schedule.Meeting.Canceled.</span><span class="sxs-lookup"><span data-stu-id="3c13f-128">The [ItemClass](itemclass.md) for a meeting cancellation is IPM.Schedule.Meeting.Canceled.</span></span> 
  
<span data-ttu-id="3c13f-129">Verwenden Sie zum Entfernen einer [MeetingRequest](meetingrequest.md) und die zugehörigen [CalendarItem](calendaritem.md) [DeclineItem](declineitem.md) -Response-Objekt anstelle von **RemoveItem**.</span><span class="sxs-lookup"><span data-stu-id="3c13f-129">To remove a [MeetingRequest](meetingrequest.md) and the associated [CalendarItem](calendaritem.md), use the [DeclineItem](declineitem.md) response object instead of **RemoveItem**.</span></span>
  
 <span data-ttu-id="3c13f-130">**RemoveItem** wird für Stellvertretungszugriff nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3c13f-130">**RemoveItem** is not supported for delegate access.</span></span> 
  
<span data-ttu-id="3c13f-131">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="3c13f-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3c13f-132">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="3c13f-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3c13f-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="3c13f-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3c13f-134">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="3c13f-134">Schema Name</span></span>  <br/> |<span data-ttu-id="3c13f-135">Schematypen</span><span class="sxs-lookup"><span data-stu-id="3c13f-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="3c13f-136">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="3c13f-136">Validation File</span></span>  <br/> |<span data-ttu-id="3c13f-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3c13f-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3c13f-138">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="3c13f-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="3c13f-139">False</span><span class="sxs-lookup"><span data-stu-id="3c13f-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3c13f-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3c13f-140">See also</span></span>



- [<span data-ttu-id="3c13f-141">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="3c13f-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

