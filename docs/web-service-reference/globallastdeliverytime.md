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
description: Das GlobalLastDeliveryTime-Element enthält die Zustellungszeit der Nachricht, die zuletzt in dieser Unterhaltung über alle Ordner im Postfach empfangen wurde.
ms.openlocfilehash: b6d4d7c1d51c206e44973a717d25df4066845ada
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459412"
---
# <a name="globallastdeliverytime"></a><span data-ttu-id="c330e-103">GlobalLastDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="c330e-103">GlobalLastDeliveryTime</span></span>

<span data-ttu-id="c330e-104">Das **GlobalLastDeliveryTime** -Element enthält die Zustellungszeit der Nachricht, die zuletzt in dieser Unterhaltung über alle Ordner im Postfach empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="c330e-104">The **GlobalLastDeliveryTime** element contains the delivery time of the message that was last received in this conversation across all folders in the mailbox.</span></span> 
  
[<span data-ttu-id="c330e-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="c330e-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="c330e-106">Conversations</span><span class="sxs-lookup"><span data-stu-id="c330e-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="c330e-107">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="c330e-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="c330e-108">GlobalLastDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="c330e-108">GlobalLastDeliveryTime</span></span>](globallastdeliverytime.md)
  
```XML
<GlobalLastDeliveryTime/>
```

 <span data-ttu-id="c330e-109">**xs: DateTime**</span><span class="sxs-lookup"><span data-stu-id="c330e-109">**xs:dateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c330e-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c330e-110">Attributes and elements</span></span>

<span data-ttu-id="c330e-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c330e-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c330e-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="c330e-112">Attributes</span></span>

<span data-ttu-id="c330e-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="c330e-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c330e-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c330e-114">Child elements</span></span>

<span data-ttu-id="c330e-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="c330e-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c330e-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c330e-116">Parent elements</span></span>

|<span data-ttu-id="c330e-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="c330e-117">**Element**</span></span>|<span data-ttu-id="c330e-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c330e-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c330e-119">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="c330e-119">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="c330e-120">Stellt eine einfache Unterhaltung dar.</span><span class="sxs-lookup"><span data-stu-id="c330e-120">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c330e-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="c330e-121">Text value</span></span>

<span data-ttu-id="c330e-122">Der Textwert des **GlobalLastDeliveryTime** -Elements ist das Datum und die Uhrzeit der Nachricht, die zuletzt in dieser Unterhaltung über alle Ordner im Postfach empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="c330e-122">The text value of the **GlobalLastDeliveryTime** element is the date and time of the message that was last received in this conversation across all folders in the mailbox.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c330e-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c330e-123">Remarks</span></span>

<span data-ttu-id="c330e-124">Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt. Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, in dem Exchange Webdienste gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="c330e-124">This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c330e-125">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="c330e-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c330e-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="c330e-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c330e-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c330e-127">Schema name</span></span>  <br/> |<span data-ttu-id="c330e-128">Schematypen</span><span class="sxs-lookup"><span data-stu-id="c330e-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="c330e-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c330e-129">Validation file</span></span>  <br/> |<span data-ttu-id="c330e-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c330e-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c330e-131">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="c330e-131">Can be empty</span></span>  <br/> |<span data-ttu-id="c330e-132">False</span><span class="sxs-lookup"><span data-stu-id="c330e-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c330e-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c330e-133">See also</span></span>



[<span data-ttu-id="c330e-134">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="c330e-134">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="c330e-135">ApplyConversationAction-Vorgang</span><span class="sxs-lookup"><span data-stu-id="c330e-135">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="c330e-136">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="c330e-136">Conversations in EWS</span></span>](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

