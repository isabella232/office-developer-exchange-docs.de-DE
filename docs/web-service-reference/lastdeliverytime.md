---
title: LastDeliveryTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- LastDeliveryTime
api_type:
- schema
ms.assetid: 23d02ceb-f28e-40f2-8f63-673723a50e2a
description: Das LastDeliveryTime-Element enthält die Übermittlungszeit der Nachricht, die in dieser Unterhaltung im aktuellen Ordner zuletzt empfangen wurde.
ms.openlocfilehash: 240f6acaf3e5249686ab26501a26ee3e0f337b0f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830198"
---
# <a name="lastdeliverytime"></a><span data-ttu-id="8d043-103">LastDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="8d043-103">LastDeliveryTime</span></span>

<span data-ttu-id="8d043-104">Das **LastDeliveryTime** -Element enthält die Übermittlungszeit der Nachricht, die in dieser Unterhaltung im aktuellen Ordner zuletzt empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="8d043-104">The **LastDeliveryTime** element contains the delivery time of the message that was last received in this conversation in the current folder.</span></span> 
  
[<span data-ttu-id="8d043-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="8d043-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="8d043-106">Conversations</span><span class="sxs-lookup"><span data-stu-id="8d043-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="8d043-107">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="8d043-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="8d043-108">LastDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="8d043-108">LastDeliveryTime</span></span>](lastdeliverytime.md)
  
```XML
<LastDeliveryTime/>
```

 <span data-ttu-id="8d043-109">**xs: DateTime**</span><span class="sxs-lookup"><span data-stu-id="8d043-109">**xs:dateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8d043-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="8d043-110">Attributes and elements</span></span>

<span data-ttu-id="8d043-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="8d043-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8d043-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="8d043-112">Attributes</span></span>

<span data-ttu-id="8d043-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="8d043-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8d043-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8d043-114">Child elements</span></span>

<span data-ttu-id="8d043-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="8d043-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8d043-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8d043-116">Parent elements</span></span>

|<span data-ttu-id="8d043-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="8d043-117">**Element**</span></span>|<span data-ttu-id="8d043-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8d043-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8d043-119">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="8d043-119">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="8d043-120">Stellt eine einfache Unterhaltung dar.</span><span class="sxs-lookup"><span data-stu-id="8d043-120">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="8d043-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="8d043-121">Text value</span></span>

<span data-ttu-id="8d043-122">Der Textwert des **LastDeliveryTime** -Elements ist das Datum und die Uhrzeit der Nachricht, die in dieser Unterhaltung im aktuellen Ordner zuletzt empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="8d043-122">The text value of the **LastDeliveryTime** element is the date and time of the message that was last received in this conversation in the current folder.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="8d043-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8d043-123">Remarks</span></span>

<span data-ttu-id="8d043-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="8d043-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8d043-125">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="8d043-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8d043-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="8d043-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8d043-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="8d043-127">Schema name</span></span>  <br/> |<span data-ttu-id="8d043-128">Schematypen</span><span class="sxs-lookup"><span data-stu-id="8d043-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="8d043-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="8d043-129">Validation file</span></span>  <br/> |<span data-ttu-id="8d043-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="8d043-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8d043-131">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="8d043-131">Can be empty</span></span>  <br/> |<span data-ttu-id="8d043-132">False</span><span class="sxs-lookup"><span data-stu-id="8d043-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8d043-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8d043-133">See also</span></span>



[<span data-ttu-id="8d043-134">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="8d043-134">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="8d043-135">ApplyConversationAction-Vorgang</span><span class="sxs-lookup"><span data-stu-id="8d043-135">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


- [<span data-ttu-id="8d043-136">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="8d043-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="8d043-137">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="8d043-137">Conversations in EWS</span></span>](http://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

