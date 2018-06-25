---
title: ReminderMessageData
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 04dd4987-baaf-4ebe-ae58-ad962c2f8fa1
description: Das ReminderMessageData-Element gibt an, dass die Daten in eine Erinnerung.
ms.openlocfilehash: a1d01dd24030b047bd8ad025f3e1cebed0da8e29
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831067"
---
# <a name="remindermessagedata"></a><span data-ttu-id="9b820-103">ReminderMessageData</span><span class="sxs-lookup"><span data-stu-id="9b820-103">ReminderMessageData</span></span>

<span data-ttu-id="9b820-104">Das **ReminderMessageData** -Element gibt an, dass die Daten in eine Erinnerung.</span><span class="sxs-lookup"><span data-stu-id="9b820-104">The **ReminderMessageData** element specifies the data in a reminder message.</span></span> 
  
```XML
<ReminderMessageData>
   <ReminderText></ReminderText>
   <Location></Location>
   <StartTime></StartTime>
   <EndTime></EndTime>
   <AssociatedCalendarItemId></AssociatedCalendarItemId>
</ReminderMessageData>

```

 <span data-ttu-id="9b820-105">**ReminderMessageDataType**</span><span class="sxs-lookup"><span data-stu-id="9b820-105">**ReminderMessageDataType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9b820-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="9b820-106">Attributes and elements</span></span>

<span data-ttu-id="9b820-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="9b820-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9b820-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="9b820-108">Attributes</span></span>

<span data-ttu-id="9b820-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="9b820-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9b820-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9b820-110">Child elements</span></span>

<span data-ttu-id="9b820-111">[ReminderText](remindertext.md) | [Speicherort](location.md) | [StartTime (ReminderMessageDataType)](starttime-remindermessagedatatype.md) | [EndTime (ReminderMessageDataType)](endtime-remindermessagedatatype.md) | [AssociatedCalendarItemId](associatedcalendaritemid.md)</span><span class="sxs-lookup"><span data-stu-id="9b820-111">[ReminderText](remindertext.md) | [Location](location.md) | [StartTime (ReminderMessageDataType)](starttime-remindermessagedatatype.md) | [EndTime (ReminderMessageDataType)](endtime-remindermessagedatatype.md) | [AssociatedCalendarItemId](associatedcalendaritemid.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9b820-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9b820-112">Parent elements</span></span>

[<span data-ttu-id="9b820-113">Message</span><span class="sxs-lookup"><span data-stu-id="9b820-113">Message</span></span>](message-ex15websvcsotherref.md)
  
## <a name="remarks"></a><span data-ttu-id="9b820-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9b820-114">Remarks</span></span>

<span data-ttu-id="9b820-115">Dieses Element wurde in Exchange Server 2013 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="9b820-115">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="9b820-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="9b820-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
<span data-ttu-id="9b820-117">Versionen von Exchange, beginnend mit Buildnummer 15.00.0913.09 können das **AssociatedCalendarItemId** -Element als untergeordnetes Element des **ReminderMessageData** -Elements enthalten.</span><span class="sxs-lookup"><span data-stu-id="9b820-117">Versions of Exchange starting with build number 15.00.0913.09 can include the **AssociatedCalendarItemId** element as a child element of the **ReminderMessageData** element.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="9b820-118">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="9b820-118">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9b820-119">Namespace</span><span class="sxs-lookup"><span data-stu-id="9b820-119">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9b820-120">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="9b820-120">Schema Name</span></span>  <br/> |<span data-ttu-id="9b820-121">Schematypen</span><span class="sxs-lookup"><span data-stu-id="9b820-121">Types schema</span></span>  <br/> |
|<span data-ttu-id="9b820-122">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="9b820-122">Validation File</span></span>  <br/> |<span data-ttu-id="9b820-123">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9b820-123">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9b820-124">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="9b820-124">Can be Empty</span></span>  <br/> |<span data-ttu-id="9b820-125">True</span><span class="sxs-lookup"><span data-stu-id="9b820-125">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9b820-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9b820-126">See also</span></span>



[<span data-ttu-id="9b820-127">Message</span><span class="sxs-lookup"><span data-stu-id="9b820-127">Message</span></span>](message-ex15websvcsotherref.md)


- [<span data-ttu-id="9b820-128">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="9b820-128">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

