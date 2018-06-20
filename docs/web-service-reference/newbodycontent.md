---
title: NewBodyContent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- NewBodyContent
api_type:
- schema
ms.assetid: 0303600d-16d8-4685-88f2-980c5ca7e9a6
description: Das NewBodyContent-Element darstellt, den neuen Body-Inhalt einer Nachricht.
ms.openlocfilehash: b87393e460b1eee1c13efebf38e898d17915bd71
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830516"
---
# <a name="newbodycontent"></a><span data-ttu-id="1248a-103">NewBodyContent</span><span class="sxs-lookup"><span data-stu-id="1248a-103">NewBodyContent</span></span>

<span data-ttu-id="1248a-104">Das **NewBodyContent** -Element darstellt, den neuen Body-Inhalt einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="1248a-104">The **NewBodyContent** element represents the new body content of a message.</span></span> 
  
```xml
<NewBodyContent BodyType=""/>
```

 <span data-ttu-id="1248a-105">**BodyType**</span><span class="sxs-lookup"><span data-stu-id="1248a-105">**BodyType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1248a-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1248a-106">Attributes and elements</span></span>

<span data-ttu-id="1248a-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1248a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1248a-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="1248a-108">Attributes</span></span>

|<span data-ttu-id="1248a-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="1248a-109">**Attribute**</span></span>|<span data-ttu-id="1248a-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1248a-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1248a-111">**BodyType**</span><span class="sxs-lookup"><span data-stu-id="1248a-111">**BodyType**</span></span> <br/> |<span data-ttu-id="1248a-112">Stellt den tatsächlichen Textkörperinhalt einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="1248a-112">Represents the actual body content of a message.</span></span>  <br/> |
   
#### <a name="bodytype-attribute"></a><span data-ttu-id="1248a-113">BodyType-Attribut</span><span class="sxs-lookup"><span data-stu-id="1248a-113">BodyType Attribute</span></span>

|<span data-ttu-id="1248a-114">**Wert**</span><span class="sxs-lookup"><span data-stu-id="1248a-114">**Value**</span></span>|<span data-ttu-id="1248a-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1248a-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1248a-116">**HTML**</span><span class="sxs-lookup"><span data-stu-id="1248a-116">**HTML**</span></span> <br/> |<span data-ttu-id="1248a-117">Konvertiert alle Texte in HTML.</span><span class="sxs-lookup"><span data-stu-id="1248a-117">Converts all bodies to HTML.</span></span>  <br/> |
|<span data-ttu-id="1248a-118">**Text**</span><span class="sxs-lookup"><span data-stu-id="1248a-118">**Text**</span></span> <br/> |<span data-ttu-id="1248a-119">Alle Texte konvertiert in nur-Text.</span><span class="sxs-lookup"><span data-stu-id="1248a-119">Converts all bodies to plain text.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1248a-120">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1248a-120">Child elements</span></span>

<span data-ttu-id="1248a-121">Keine.</span><span class="sxs-lookup"><span data-stu-id="1248a-121">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1248a-122">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1248a-122">Parent elements</span></span>

|<span data-ttu-id="1248a-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="1248a-123">**Element**</span></span>|<span data-ttu-id="1248a-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1248a-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1248a-125">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="1248a-125">ReplyToItem</span></span>](replytoitem.md) <br/> |<span data-ttu-id="1248a-126">Enthält eine Antwort an den Absender eines Elements in der Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="1248a-126">Contains a reply to the sender of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="1248a-127">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="1248a-127">ReplyAllToItem</span></span>](replyalltoitem.md) <br/> |<span data-ttu-id="1248a-128">Enthält eine Antwort an den Absender und alle gefundenen Empfänger eines Elements in der Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="1248a-128">Contains a reply to the sender and all identified recipients of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="1248a-129">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="1248a-129">ForwardItem</span></span>](forwarditem.md) <br/> |<span data-ttu-id="1248a-130">Enthält ein Exchange-Speicher-Element an Empfänger weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="1248a-130">Contains an Exchange store item to forward to recipients.</span></span>  <br/> |
|[<span data-ttu-id="1248a-131">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="1248a-131">CancelCalendarItem</span></span>](cancelcalendaritem.md) <br/> |<span data-ttu-id="1248a-132">Stellt das Antwortobjekt, das Sie eine Besprechung absagen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1248a-132">Represents the response object that is used to cancel a meeting.</span></span>  <br/> |
|[<span data-ttu-id="1248a-133">PostReplyItem</span><span class="sxs-lookup"><span data-stu-id="1248a-133">PostReplyItem</span></span>](postreplyitem.md) <br/> |<span data-ttu-id="1248a-134">Eine Antwort auf eine Post-Element enthält.</span><span class="sxs-lookup"><span data-stu-id="1248a-134">Contains a reply to a post item.</span></span> <span data-ttu-id="1248a-135">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="1248a-135">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1248a-136">Textwert</span><span class="sxs-lookup"><span data-stu-id="1248a-136">Text value</span></span>

<span data-ttu-id="1248a-137">Der Textwert stellt den neuen Textkörperinhalt einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="1248a-137">The text value represents the new body content of a message.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1248a-138">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1248a-138">Remarks</span></span>

<span data-ttu-id="1248a-139">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Exchange-Servers, der die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="1248a-139">The schema that describes this element is located in the EWS virtual directory of the Exchange server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1248a-140">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="1248a-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1248a-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="1248a-141">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1248a-142">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="1248a-142">Schema Name</span></span>  <br/> |<span data-ttu-id="1248a-143">Schematypen</span><span class="sxs-lookup"><span data-stu-id="1248a-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="1248a-144">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="1248a-144">Validation File</span></span>  <br/> |<span data-ttu-id="1248a-145">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1248a-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1248a-146">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="1248a-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="1248a-147">False</span><span class="sxs-lookup"><span data-stu-id="1248a-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1248a-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1248a-148">See also</span></span>



- [<span data-ttu-id="1248a-149">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="1248a-149">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

