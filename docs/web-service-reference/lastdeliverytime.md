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
description: Das LastDeliveryTime-Element enthält die Zustellungszeit der Nachricht, die zuletzt in dieser Unterhaltung im aktuellen Ordner empfangen wurde.
ms.openlocfilehash: 77147693a9394e983575afa6fcfda242f8f76ae3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458110"
---
# <a name="lastdeliverytime"></a><span data-ttu-id="29719-103">LastDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="29719-103">LastDeliveryTime</span></span>

<span data-ttu-id="29719-104">Das **LastDeliveryTime** -Element enthält die Zustellungszeit der Nachricht, die zuletzt in dieser Unterhaltung im aktuellen Ordner empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="29719-104">The **LastDeliveryTime** element contains the delivery time of the message that was last received in this conversation in the current folder.</span></span> 
  
[<span data-ttu-id="29719-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="29719-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="29719-106">Conversations</span><span class="sxs-lookup"><span data-stu-id="29719-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="29719-107">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="29719-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="29719-108">LastDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="29719-108">LastDeliveryTime</span></span>](lastdeliverytime.md)
  
```XML
<LastDeliveryTime/>
```

 <span data-ttu-id="29719-109">**xs: DateTime**</span><span class="sxs-lookup"><span data-stu-id="29719-109">**xs:dateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="29719-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="29719-110">Attributes and elements</span></span>

<span data-ttu-id="29719-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="29719-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="29719-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="29719-112">Attributes</span></span>

<span data-ttu-id="29719-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="29719-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="29719-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="29719-114">Child elements</span></span>

<span data-ttu-id="29719-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="29719-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="29719-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="29719-116">Parent elements</span></span>

|<span data-ttu-id="29719-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="29719-117">**Element**</span></span>|<span data-ttu-id="29719-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="29719-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="29719-119">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="29719-119">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="29719-120">Stellt eine einfache Unterhaltung dar.</span><span class="sxs-lookup"><span data-stu-id="29719-120">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="29719-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="29719-121">Text value</span></span>

<span data-ttu-id="29719-122">Der Textwert des **LastDeliveryTime** -Elements ist das Datum und die Uhrzeit der Nachricht, die zuletzt in dieser Unterhaltung im aktuellen Ordner empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="29719-122">The text value of the **LastDeliveryTime** element is the date and time of the message that was last received in this conversation in the current folder.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="29719-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="29719-123">Remarks</span></span>

<span data-ttu-id="29719-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="29719-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="29719-125">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="29719-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="29719-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="29719-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="29719-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="29719-127">Schema name</span></span>  <br/> |<span data-ttu-id="29719-128">Schematypen</span><span class="sxs-lookup"><span data-stu-id="29719-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="29719-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="29719-129">Validation file</span></span>  <br/> |<span data-ttu-id="29719-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="29719-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="29719-131">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="29719-131">Can be empty</span></span>  <br/> |<span data-ttu-id="29719-132">False</span><span class="sxs-lookup"><span data-stu-id="29719-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="29719-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="29719-133">See also</span></span>



[<span data-ttu-id="29719-134">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="29719-134">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="29719-135">ApplyConversationAction-Vorgang</span><span class="sxs-lookup"><span data-stu-id="29719-135">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


- [<span data-ttu-id="29719-136">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="29719-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="29719-137">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="29719-137">Conversations in EWS</span></span>](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

