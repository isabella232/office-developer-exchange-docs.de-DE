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
description: Das RemoveItem-Element stellt ein Response-Objekt dar, das zum Entfernen eines Besprechungselements verwendet wird, wenn eine MeetingCancellation-Nachricht empfangen wird.
ms.openlocfilehash: c0cd5c1f9894287ee78c2f7a65b8f4d3b943414e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467690"
---
# <a name="removeitem"></a><span data-ttu-id="8cd72-103">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="8cd72-103">RemoveItem</span></span>

<span data-ttu-id="8cd72-104">Das **RemoveItem** -Element stellt ein Response-Objekt dar, das zum Entfernen eines Besprechungselements verwendet wird, wenn eine MeetingCancellation-Nachricht empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="8cd72-104">The **RemoveItem** element represents a response object that is used to remove a meeting item when a MeetingCancellation message is received.</span></span> 
  
```xml
<RemoveItem ObjectName="">
   <ReferenceItemId/>
</RemoveItem>
```

 <span data-ttu-id="8cd72-105">**RemoveItemType**</span><span class="sxs-lookup"><span data-stu-id="8cd72-105">**RemoveItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8cd72-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="8cd72-106">Attributes and elements</span></span>

<span data-ttu-id="8cd72-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="8cd72-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8cd72-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="8cd72-108">Attributes</span></span>

|<span data-ttu-id="8cd72-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="8cd72-109">**Attribute**</span></span>|<span data-ttu-id="8cd72-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8cd72-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8cd72-111">**ObjectName**</span><span class="sxs-lookup"><span data-stu-id="8cd72-111">**ObjectName**</span></span> <br/> |<span data-ttu-id="8cd72-112">Stellt den Namen der RemoveItem-Antwortobjekt Klasse als englische Zeichenfolge dar.</span><span class="sxs-lookup"><span data-stu-id="8cd72-112">Represents the name of the RemoveItem reply object class as an English string.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8cd72-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8cd72-113">Child elements</span></span>

|<span data-ttu-id="8cd72-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="8cd72-114">**Element**</span></span>|<span data-ttu-id="8cd72-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8cd72-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8cd72-116">ReferenceItemId</span><span class="sxs-lookup"><span data-stu-id="8cd72-116">ReferenceItemId</span></span>](referenceitemid.md) <br/> |<span data-ttu-id="8cd72-117">Gibt das Element an, auf das das RemoveItem-Antwortobjekt verweist.</span><span class="sxs-lookup"><span data-stu-id="8cd72-117">Identifies the item to which the RemoveItem response object refers.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8cd72-118">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8cd72-118">Parent elements</span></span>

|<span data-ttu-id="8cd72-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="8cd72-119">**Element**</span></span>|<span data-ttu-id="8cd72-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8cd72-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8cd72-121">Elemente (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="8cd72-121">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="8cd72-122">Enthält ein Array von Elementen, die in dem Ordner erstellt werden sollen, der durch das [parentfolderid (TargetFolderIdType)-](parentfolderid-targetfolderidtype.md) Element identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="8cd72-122">Contains an array of items to create in the folder that is identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
|[<span data-ttu-id="8cd72-123">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="8cd72-123">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="8cd72-124">Enthält eine Auflistung aller Response-Objekte, die einem Element in der Exchange-Informationsspeicher zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="8cd72-124">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8cd72-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8cd72-125">Remarks</span></span>

 <span data-ttu-id="8cd72-126">**RemoveItem** ist nur für eine [MeetingCancellation](meetingcancellation.md)gültig.</span><span class="sxs-lookup"><span data-stu-id="8cd72-126">**RemoveItem** is valid only for a [MeetingCancellation](meetingcancellation.md).</span></span> <span data-ttu-id="8cd72-127">Andernfalls wird ein Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="8cd72-127">Otherwise, an error is thrown.</span></span>
  
> [!NOTE]
> <span data-ttu-id="8cd72-128">Das [ItemClass](itemclass.md) für eine Besprechungsabsage ist IPM. Schedule. Meeting. Canceled.</span><span class="sxs-lookup"><span data-stu-id="8cd72-128">The [ItemClass](itemclass.md) for a meeting cancellation is IPM.Schedule.Meeting.Canceled.</span></span> 
  
<span data-ttu-id="8cd72-129">Verwenden Sie zum Entfernen einer [MeetingRequest](meetingrequest.md) und der zugeordneten [CalendarItem](calendaritem.md)das [DeclineItem](declineitem.md) -Antwortobjekt anstelle von **RemoveItem**.</span><span class="sxs-lookup"><span data-stu-id="8cd72-129">To remove a [MeetingRequest](meetingrequest.md) and the associated [CalendarItem](calendaritem.md), use the [DeclineItem](declineitem.md) response object instead of **RemoveItem**.</span></span>
  
 <span data-ttu-id="8cd72-130">**RemoveItem** wird für den Stellvertretungszugriff nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8cd72-130">**RemoveItem** is not supported for delegate access.</span></span> 
  
<span data-ttu-id="8cd72-131">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="8cd72-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8cd72-132">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="8cd72-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8cd72-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="8cd72-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8cd72-134">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="8cd72-134">Schema Name</span></span>  <br/> |<span data-ttu-id="8cd72-135">Schematypen</span><span class="sxs-lookup"><span data-stu-id="8cd72-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="8cd72-136">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="8cd72-136">Validation File</span></span>  <br/> |<span data-ttu-id="8cd72-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="8cd72-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8cd72-138">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="8cd72-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="8cd72-139">False</span><span class="sxs-lookup"><span data-stu-id="8cd72-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8cd72-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8cd72-140">See also</span></span>



- [<span data-ttu-id="8cd72-141">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="8cd72-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

