---
title: MoreEvents
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MoreEvents
api_type:
- schema
ms.assetid: 76a7ea58-a44f-49b8-baba-d21302d742ad
description: Das MoreEvents-Element gibt an, ob es sind mehr Ereignisse in der Warteschlange an den Client übermittelt werden.
ms.openlocfilehash: cc3f7ed3b4b5f5ce27a9d45d508506bfa62e5086
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830489"
---
# <a name="moreevents"></a><span data-ttu-id="5732e-103">MoreEvents</span><span class="sxs-lookup"><span data-stu-id="5732e-103">MoreEvents</span></span>

<span data-ttu-id="5732e-104">Das **MoreEvents** -Element gibt an, ob es sind mehr Ereignisse in der Warteschlange an den Client übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="5732e-104">The **MoreEvents** element indicates whether there are more events in the queue to be delivered to the client.</span></span> 
  
```xml
<MoreEvents/>
```

 <span data-ttu-id="5732e-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="5732e-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5732e-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="5732e-106">Attributes and elements</span></span>

<span data-ttu-id="5732e-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="5732e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5732e-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="5732e-108">Attributes</span></span>

<span data-ttu-id="5732e-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="5732e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5732e-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5732e-110">Child elements</span></span>

<span data-ttu-id="5732e-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="5732e-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5732e-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5732e-112">Parent elements</span></span>

|<span data-ttu-id="5732e-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="5732e-113">**Element**</span></span>|<span data-ttu-id="5732e-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5732e-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5732e-115">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="5732e-115">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="5732e-116">Enthält Informationen über das Abonnement und die Ereignisse, die seit der letzten Benachrichtigung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="5732e-116">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5732e-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="5732e-117">Text value</span></span>

<span data-ttu-id="5732e-118">Der Textwert stellt einen Boolean-Wert.</span><span class="sxs-lookup"><span data-stu-id="5732e-118">The text value represents a Boolean value.</span></span> <span data-ttu-id="5732e-119">Der Wert **true** gibt an, dass mehr Ereignisse in der Warteschlange befinden.</span><span class="sxs-lookup"><span data-stu-id="5732e-119">A value of **true** indicates that more events are in the queue.</span></span> <span data-ttu-id="5732e-120">Der Wert **false** gibt an, dass keine weiteren Ereignisse in der Warteschlange befinden.</span><span class="sxs-lookup"><span data-stu-id="5732e-120">A value of **false** indicates that no more events are in the queue.</span></span> <span data-ttu-id="5732e-121">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="5732e-121">This property is read-only.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5732e-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5732e-122">Remarks</span></span>

<span data-ttu-id="5732e-123">Im Fall von Pull-Benachrichtigungen gibt ein **true** -Wert in diesem Element an den Client, dass eine andere GetEvents Anforderung ausgegeben werden soll, wenn Sie die verbleibenden Ereignisse erhalten möchten.</span><span class="sxs-lookup"><span data-stu-id="5732e-123">In the case of Pull notifications, a **true** value in this element indicates to the client that another GetEvents request should be issued to get the remaining events.</span></span> <span data-ttu-id="5732e-124">Unter der Annahme, dass die Client-Spezifikationen minimale Wartezeit für ereignisbenachrichtigungen benötigen, sollten GetEvents Anforderungen einer continuous nacheinander fortgesetzt, bis ein **false** **MoreEvents** Wert zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5732e-124">Assuming that the client specifications require minimum latency for event notifications, GetEvents requests should continue in a continuous succession until a **false** **MoreEvents** value is returned.</span></span> 
  
<span data-ttu-id="5732e-125">Im Fall von Pushbenachrichtigungen gibt der Wert **true** für **MoreEvents** an den Client, dass eine weitere Benachrichtigung-Anforderung an den Client gesendet wird die verbleibenden Ereignisse zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="5732e-125">In the case of Push notifications, a **true** value for **MoreEvents** indicates to the client that another notification request will be sent to the client to deliver the remaining events.</span></span> <span data-ttu-id="5732e-126">Ähnlich wie bei Pull Benachrichtigungen, werden diese weiteren Anforderungen kontinuierliche nacheinander fortgesetzt, bis die Ereigniswarteschlange auf dem Clientzugriffsserver leer ist.</span><span class="sxs-lookup"><span data-stu-id="5732e-126">Similar to Pull notifications, these follow-up requests will continue in continuous succession until the event queue on the Client Access server is empty.</span></span> 
  
<span data-ttu-id="5732e-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="5732e-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5732e-128">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="5732e-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5732e-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="5732e-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5732e-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="5732e-130">Schema Name</span></span>  <br/> |<span data-ttu-id="5732e-131">Schematypen</span><span class="sxs-lookup"><span data-stu-id="5732e-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="5732e-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="5732e-132">Validation File</span></span>  <br/> |<span data-ttu-id="5732e-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5732e-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5732e-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="5732e-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="5732e-135">False</span><span class="sxs-lookup"><span data-stu-id="5732e-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5732e-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5732e-136">See also</span></span>



[<span data-ttu-id="5732e-137">Vorgang abonnieren</span><span class="sxs-lookup"><span data-stu-id="5732e-137">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="5732e-138">GetEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="5732e-138">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="5732e-139">Vorgang des Kündigens von Abonnements</span><span class="sxs-lookup"><span data-stu-id="5732e-139">Unsubscribe operation</span></span>](unsubscribe-operation.md)

