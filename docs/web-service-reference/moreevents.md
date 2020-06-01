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
description: Das MoreEvents-Element gibt an, ob weitere Ereignisse in der Warteschlange vorhanden sind, die an den Client übermittelt werden sollen.
ms.openlocfilehash: fd12dd2e2e64ce1711e553ba5eb29bd0eb64c892
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462731"
---
# <a name="moreevents"></a><span data-ttu-id="b689d-103">MoreEvents</span><span class="sxs-lookup"><span data-stu-id="b689d-103">MoreEvents</span></span>

<span data-ttu-id="b689d-104">Das **MoreEvents** -Element gibt an, ob weitere Ereignisse in der Warteschlange vorhanden sind, die an den Client übermittelt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b689d-104">The **MoreEvents** element indicates whether there are more events in the queue to be delivered to the client.</span></span> 
  
```xml
<MoreEvents/>
```

 <span data-ttu-id="b689d-105">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="b689d-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b689d-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b689d-106">Attributes and elements</span></span>

<span data-ttu-id="b689d-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b689d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b689d-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="b689d-108">Attributes</span></span>

<span data-ttu-id="b689d-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="b689d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b689d-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b689d-110">Child elements</span></span>

<span data-ttu-id="b689d-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="b689d-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b689d-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b689d-112">Parent elements</span></span>

|<span data-ttu-id="b689d-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="b689d-113">**Element**</span></span>|<span data-ttu-id="b689d-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b689d-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b689d-115">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="b689d-115">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="b689d-116">Enthält Informationen über das Abonnement und die Ereignisse, die seit der letzten Benachrichtigung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="b689d-116">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b689d-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="b689d-117">Text value</span></span>

<span data-ttu-id="b689d-118">Der Wert Text stellt einen booleschen Wert dar.</span><span class="sxs-lookup"><span data-stu-id="b689d-118">The text value represents a Boolean value.</span></span> <span data-ttu-id="b689d-119">Der Wert **true** gibt an, dass sich weitere Ereignisse in der Warteschlange befinden.</span><span class="sxs-lookup"><span data-stu-id="b689d-119">A value of **true** indicates that more events are in the queue.</span></span> <span data-ttu-id="b689d-120">Der Wert **false** gibt an, dass sich keine weiteren Ereignisse in der Warteschlange befinden.</span><span class="sxs-lookup"><span data-stu-id="b689d-120">A value of **false** indicates that no more events are in the queue.</span></span> <span data-ttu-id="b689d-121">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="b689d-121">This property is read-only.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b689d-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b689d-122">Remarks</span></span>

<span data-ttu-id="b689d-123">Im Fall von Pull-Benachrichtigungen gibt ein Wert **true** in diesem Element an den Client an, dass eine andere GetEvents-Anforderung ausgegeben werden soll, um die restlichen Ereignisse abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b689d-123">In the case of Pull notifications, a **true** value in this element indicates to the client that another GetEvents request should be issued to get the remaining events.</span></span> <span data-ttu-id="b689d-124">Unter der Voraussetzung, dass die Client Spezifikationen eine minimale Wartezeit für Ereignisbenachrichtigungen erfordern, sollten GetEvents-Anforderungen in einer kontinuierlichen Reihenfolge fortgesetzt werden, bis ein **falscher** **MoreEvents** -Wert zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b689d-124">Assuming that the client specifications require minimum latency for event notifications, GetEvents requests should continue in a continuous succession until a **false** **MoreEvents** value is returned.</span></span> 
  
<span data-ttu-id="b689d-125">Im Fall von Push-Benachrichtigungen gibt ein **echter** Wert für **MoreEvents** dem Client an, dass eine andere Benachrichtigungsanforderung an den Client gesendet wird, um die verbleibenden Ereignisse zuzustellen.</span><span class="sxs-lookup"><span data-stu-id="b689d-125">In the case of Push notifications, a **true** value for **MoreEvents** indicates to the client that another notification request will be sent to the client to deliver the remaining events.</span></span> <span data-ttu-id="b689d-126">Ähnlich wie Pull-Benachrichtigungen werden diese nachverfolgungsanforderungen in Folge fortgesetzt, bis die Ereigniswarteschlange auf dem Client Zugriffsserver leer ist.</span><span class="sxs-lookup"><span data-stu-id="b689d-126">Similar to Pull notifications, these follow-up requests will continue in continuous succession until the event queue on the Client Access server is empty.</span></span> 
  
<span data-ttu-id="b689d-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="b689d-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b689d-128">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="b689d-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b689d-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="b689d-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b689d-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b689d-130">Schema Name</span></span>  <br/> |<span data-ttu-id="b689d-131">Schematypen</span><span class="sxs-lookup"><span data-stu-id="b689d-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="b689d-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b689d-132">Validation File</span></span>  <br/> |<span data-ttu-id="b689d-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b689d-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b689d-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="b689d-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="b689d-135">False</span><span class="sxs-lookup"><span data-stu-id="b689d-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b689d-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b689d-136">See also</span></span>



[<span data-ttu-id="b689d-137">Vorgang abonnieren</span><span class="sxs-lookup"><span data-stu-id="b689d-137">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="b689d-138">GetEvents-Vorgang</span><span class="sxs-lookup"><span data-stu-id="b689d-138">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="b689d-139">Vorgang des Kündigens von Abonnements</span><span class="sxs-lookup"><span data-stu-id="b689d-139">Unsubscribe operation</span></span>](unsubscribe-operation.md)

