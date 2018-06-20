---
title: GlobalLastDeliveryTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GlobalLastDeliveryTime
api_type:
- schema
ms.assetid: a88dada9-c527-43a7-b2d3-31aad330def9
description: Das GlobalLastDeliveryTime-Element enthält die Zeit der Zustellung der Nachricht, die zuletzt in dieser Unterhaltung in allen Ordnern im Postfach empfangen wurde.
ms.openlocfilehash: fded5cd1891a406f0979cf4bec7321779d70ab3a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19829733"
---
# <a name="globallastdeliverytime"></a><span data-ttu-id="81abf-103">GlobalLastDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="81abf-103">GlobalLastDeliveryTime</span></span>

<span data-ttu-id="81abf-104">Das **GlobalLastDeliveryTime** -Element enthält die Zeit der Zustellung der Nachricht, die zuletzt in dieser Unterhaltung in allen Ordnern im Postfach empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="81abf-104">The **GlobalLastDeliveryTime** element contains the delivery time of the message that was last received in this conversation across all folders in the mailbox.</span></span> 
  
[<span data-ttu-id="81abf-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="81abf-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="81abf-106">Conversations</span><span class="sxs-lookup"><span data-stu-id="81abf-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="81abf-107">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="81abf-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="81abf-108">GlobalLastDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="81abf-108">GlobalLastDeliveryTime</span></span>](globallastdeliverytime.md)
  
```XML
<GlobalLastDeliveryTime/>
```

 <span data-ttu-id="81abf-109">**xs: DateTime**</span><span class="sxs-lookup"><span data-stu-id="81abf-109">**xs:dateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="81abf-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="81abf-110">Attributes and elements</span></span>

<span data-ttu-id="81abf-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="81abf-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="81abf-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="81abf-112">Attributes</span></span>

<span data-ttu-id="81abf-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="81abf-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="81abf-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="81abf-114">Child elements</span></span>

<span data-ttu-id="81abf-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="81abf-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="81abf-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="81abf-116">Parent elements</span></span>

|<span data-ttu-id="81abf-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="81abf-117">**Element**</span></span>|<span data-ttu-id="81abf-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="81abf-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="81abf-119">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="81abf-119">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="81abf-120">Stellt eine einfache Unterhaltung dar.</span><span class="sxs-lookup"><span data-stu-id="81abf-120">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="81abf-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="81abf-121">Text value</span></span>

<span data-ttu-id="81abf-122">Der Textwert des **GlobalLastDeliveryTime** -Elements ist das Datum und die Uhrzeit der Nachricht, die zuletzt in dieser Unterhaltung in allen Ordnern im Postfach empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="81abf-122">The text value of the **GlobalLastDeliveryTime** element is the date and time of the message that was last received in this conversation across all folders in the mailbox.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="81abf-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="81abf-123">Remarks</span></span>

<span data-ttu-id="81abf-124">Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt. Das Schema, das dieses Element beschreibt befindet sich in dem virtuellen IIS-Verzeichnis, die Exchange-Webdienste gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="81abf-124">This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="81abf-125">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="81abf-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="81abf-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="81abf-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="81abf-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="81abf-127">Schema name</span></span>  <br/> |<span data-ttu-id="81abf-128">Schematypen</span><span class="sxs-lookup"><span data-stu-id="81abf-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="81abf-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="81abf-129">Validation file</span></span>  <br/> |<span data-ttu-id="81abf-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="81abf-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="81abf-131">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="81abf-131">Can be empty</span></span>  <br/> |<span data-ttu-id="81abf-132">False</span><span class="sxs-lookup"><span data-stu-id="81abf-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="81abf-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="81abf-133">See also</span></span>



[<span data-ttu-id="81abf-134">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="81abf-134">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="81abf-135">ApplyConversationAction-Vorgang</span><span class="sxs-lookup"><span data-stu-id="81abf-135">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="81abf-136">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="81abf-136">Conversations in EWS</span></span>](http://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

