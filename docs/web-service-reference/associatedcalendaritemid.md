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
description: Das AssociatedCalendarItemId-Element darstellt, das Kalenderelement, das eine MeetingMessage, MeetingRequest, MeetingResponse, MeetingCancellation oder ReminderMessageData zugeordnet ist.
ms.openlocfilehash: 4445da88d6fec42c1e02cd8de4d2e423485a4472
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757390"
---
# <a name="associatedcalendaritemid"></a><span data-ttu-id="f7f1c-103">AssociatedCalendarItemId</span><span class="sxs-lookup"><span data-stu-id="f7f1c-103">AssociatedCalendarItemId</span></span>

<span data-ttu-id="f7f1c-104">Das **AssociatedCalendarItemId** -Element darstellt, das Kalenderelement, das eine [MeetingMessage](meetingmessage.md), [MeetingRequest](meetingrequest.md), [MeetingResponse](meetingresponse.md), [MeetingCancellation](meetingcancellation.md)oder [ReminderMessageData](remindermessagedata.md)zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f7f1c-104">The **AssociatedCalendarItemId** element represents the calendar item that is associated with a [MeetingMessage](meetingmessage.md), [MeetingRequest](meetingrequest.md), [MeetingResponse](meetingresponse.md), [MeetingCancellation](meetingcancellation.md), or [ReminderMessageData](remindermessagedata.md).</span></span>
  
```XML
<AssociatedCalendarItemId Id="" ChangeKey=""/>
```

 <span data-ttu-id="f7f1c-105">**ItemIdType**</span><span class="sxs-lookup"><span data-stu-id="f7f1c-105">**ItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f7f1c-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f7f1c-106">Attributes and elements</span></span>

<span data-ttu-id="f7f1c-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f7f1c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f7f1c-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="f7f1c-108">Attributes</span></span>

|<span data-ttu-id="f7f1c-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="f7f1c-109">**Attribute**</span></span>|<span data-ttu-id="f7f1c-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f7f1c-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f7f1c-111">**Id**</span><span class="sxs-lookup"><span data-stu-id="f7f1c-111">**Id**</span></span> <br/> |<span data-ttu-id="f7f1c-112">Identifiziert das Kalenderelement, das Besprechung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f7f1c-112">Identifies the calendar item that is associated with meeting.</span></span>  <br/> |
|<span data-ttu-id="f7f1c-113">**ChangeKey**</span><span class="sxs-lookup"><span data-stu-id="f7f1c-113">**ChangeKey**</span></span> <br/> |<span data-ttu-id="f7f1c-114">Identifiziert eine bestimmte Version des Kalenderelements an, die mit einer Besprechung verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="f7f1c-114">Identifies a specific version of the calendar item that is associated with a meeting.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f7f1c-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f7f1c-115">Child elements</span></span>

<span data-ttu-id="f7f1c-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="f7f1c-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f7f1c-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f7f1c-117">Parent elements</span></span>

<span data-ttu-id="f7f1c-118">[MeetingMessage](meetingmessage.md) | [MeetingRequest](meetingrequest.md) | [MeetingResponse](meetingresponse.md) | [MeetingCancellation](meetingcancellation.md) | [ReminderMessageData](remindermessagedata.md)</span><span class="sxs-lookup"><span data-stu-id="f7f1c-118">[MeetingMessage](meetingmessage.md) | [MeetingRequest](meetingrequest.md) | [MeetingResponse](meetingresponse.md) | [MeetingCancellation](meetingcancellation.md) | [ReminderMessageData](remindermessagedata.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f7f1c-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f7f1c-119">Remarks</span></span>

<span data-ttu-id="f7f1c-120">Versionen von Exchange, beginnend mit Buildnummer 15.00.0913.09 können das **AssociatedCalendarItemId** -Element als untergeordnetes Element des **ReminderMessageData** -Elements enthalten.</span><span class="sxs-lookup"><span data-stu-id="f7f1c-120">Versions of Exchange starting with build number 15.00.0913.09 can include the **AssociatedCalendarItemId** element as a child element of the **ReminderMessageData** element.</span></span> 
  
<span data-ttu-id="f7f1c-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="f7f1c-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f7f1c-122">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="f7f1c-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f7f1c-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="f7f1c-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f7f1c-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f7f1c-124">Schema Name</span></span>  <br/> |<span data-ttu-id="f7f1c-125">Schematypen</span><span class="sxs-lookup"><span data-stu-id="f7f1c-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="f7f1c-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f7f1c-126">Validation File</span></span>  <br/> |<span data-ttu-id="f7f1c-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f7f1c-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f7f1c-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="f7f1c-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="f7f1c-129">False</span><span class="sxs-lookup"><span data-stu-id="f7f1c-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f7f1c-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f7f1c-130">See also</span></span>

- [<span data-ttu-id="f7f1c-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="f7f1c-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

