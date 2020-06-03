---
title: AssociatedCalendarItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AssociatedCalendarItemId
api_type:
- schema
ms.assetid: 5b29898c-ea59-4e6a-914c-c011ec754032
description: Das AssociatedCalendarItemId-Element stellt das Kalenderelement dar, das einem MeetingMessage, MeetingRequest, MeetingResponse, MeetingCancellation oder ReminderMessageData zugeordnet ist.
ms.openlocfilehash: 816372c38243ba0fe5a7606c264dd1c5107350f2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460883"
---
# <a name="associatedcalendaritemid"></a><span data-ttu-id="6930d-103">AssociatedCalendarItemId</span><span class="sxs-lookup"><span data-stu-id="6930d-103">AssociatedCalendarItemId</span></span>

<span data-ttu-id="6930d-104">Das **AssociatedCalendarItemId** -Element stellt das Kalenderelement dar, das einem [MeetingMessage](meetingmessage.md), [MeetingRequest](meetingrequest.md), [MeetingResponse](meetingresponse.md), [MeetingCancellation](meetingcancellation.md)oder [ReminderMessageData](remindermessagedata.md)zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="6930d-104">The **AssociatedCalendarItemId** element represents the calendar item that is associated with a [MeetingMessage](meetingmessage.md), [MeetingRequest](meetingrequest.md), [MeetingResponse](meetingresponse.md), [MeetingCancellation](meetingcancellation.md), or [ReminderMessageData](remindermessagedata.md).</span></span>
  
```XML
<AssociatedCalendarItemId Id="" ChangeKey=""/>
```

 <span data-ttu-id="6930d-105">**Itemidtype**</span><span class="sxs-lookup"><span data-stu-id="6930d-105">**ItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6930d-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="6930d-106">Attributes and elements</span></span>

<span data-ttu-id="6930d-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="6930d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6930d-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="6930d-108">Attributes</span></span>

|<span data-ttu-id="6930d-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="6930d-109">**Attribute**</span></span>|<span data-ttu-id="6930d-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6930d-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6930d-111">**Id**</span><span class="sxs-lookup"><span data-stu-id="6930d-111">**Id**</span></span> <br/> |<span data-ttu-id="6930d-112">Gibt das Kalenderelement an, das der Besprechung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="6930d-112">Identifies the calendar item that is associated with meeting.</span></span>  <br/> |
|<span data-ttu-id="6930d-113">**ChangeKey**</span><span class="sxs-lookup"><span data-stu-id="6930d-113">**ChangeKey**</span></span> <br/> |<span data-ttu-id="6930d-114">Gibt eine bestimmte Version des Kalenderelements an, das einer Besprechung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="6930d-114">Identifies a specific version of the calendar item that is associated with a meeting.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="6930d-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6930d-115">Child elements</span></span>

<span data-ttu-id="6930d-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="6930d-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6930d-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6930d-117">Parent elements</span></span>

<span data-ttu-id="6930d-118">[MeetingMessage](meetingmessage.md)  |  [MeetingRequest](meetingrequest.md)  |  [MeetingResponse](meetingresponse.md)  |  [MeetingCancellation](meetingcancellation.md)  |  [ReminderMessageData](remindermessagedata.md)</span><span class="sxs-lookup"><span data-stu-id="6930d-118">[MeetingMessage](meetingmessage.md) | [MeetingRequest](meetingrequest.md) | [MeetingResponse](meetingresponse.md) | [MeetingCancellation](meetingcancellation.md) | [ReminderMessageData](remindermessagedata.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6930d-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6930d-119">Remarks</span></span>

<span data-ttu-id="6930d-120">Versionen von Exchange, die mit Buildnummer 15.00.0913.09 beginnen, können das **AssociatedCalendarItemId** -Element als untergeordnetes Element des **ReminderMessageData** -Elements enthalten.</span><span class="sxs-lookup"><span data-stu-id="6930d-120">Versions of Exchange starting with build number 15.00.0913.09 can include the **AssociatedCalendarItemId** element as a child element of the **ReminderMessageData** element.</span></span> 
  
<span data-ttu-id="6930d-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="6930d-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6930d-122">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="6930d-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6930d-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="6930d-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6930d-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="6930d-124">Schema Name</span></span>  <br/> |<span data-ttu-id="6930d-125">Schematypen</span><span class="sxs-lookup"><span data-stu-id="6930d-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="6930d-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="6930d-126">Validation File</span></span>  <br/> |<span data-ttu-id="6930d-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6930d-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6930d-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="6930d-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="6930d-129">False</span><span class="sxs-lookup"><span data-stu-id="6930d-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6930d-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6930d-130">See also</span></span>

- [<span data-ttu-id="6930d-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="6930d-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

