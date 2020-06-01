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
description: Das NewBodyContent-Element stellt den neuen Textkörper Inhalt einer Nachricht dar.
ms.openlocfilehash: dcfa927bb284ff00e510d8c7b4b31910a70b3cbb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466857"
---
# <a name="newbodycontent"></a><span data-ttu-id="b6222-103">NewBodyContent</span><span class="sxs-lookup"><span data-stu-id="b6222-103">NewBodyContent</span></span>

<span data-ttu-id="b6222-104">Das **NewBodyContent** -Element stellt den neuen Textkörper Inhalt einer Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="b6222-104">The **NewBodyContent** element represents the new body content of a message.</span></span> 
  
```xml
<NewBodyContent BodyType=""/>
```

 <span data-ttu-id="b6222-105">**BodyType**</span><span class="sxs-lookup"><span data-stu-id="b6222-105">**BodyType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b6222-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b6222-106">Attributes and elements</span></span>

<span data-ttu-id="b6222-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b6222-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b6222-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="b6222-108">Attributes</span></span>

|<span data-ttu-id="b6222-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="b6222-109">**Attribute**</span></span>|<span data-ttu-id="b6222-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b6222-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b6222-111">**BodyType**</span><span class="sxs-lookup"><span data-stu-id="b6222-111">**BodyType**</span></span> <br/> |<span data-ttu-id="b6222-112">Stellt den tatsächlichen Textinhalt einer Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="b6222-112">Represents the actual body content of a message.</span></span>  <br/> |
   
#### <a name="bodytype-attribute"></a><span data-ttu-id="b6222-113">BodyType-Attribut</span><span class="sxs-lookup"><span data-stu-id="b6222-113">BodyType Attribute</span></span>

|<span data-ttu-id="b6222-114">**Wert**</span><span class="sxs-lookup"><span data-stu-id="b6222-114">**Value**</span></span>|<span data-ttu-id="b6222-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b6222-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b6222-116">**HTML**</span><span class="sxs-lookup"><span data-stu-id="b6222-116">**HTML**</span></span> <br/> |<span data-ttu-id="b6222-117">Wandelt alle Textkörper in HTML um.</span><span class="sxs-lookup"><span data-stu-id="b6222-117">Converts all bodies to HTML.</span></span>  <br/> |
|<span data-ttu-id="b6222-118">**Text**</span><span class="sxs-lookup"><span data-stu-id="b6222-118">**Text**</span></span> <br/> |<span data-ttu-id="b6222-119">Wandelt alle Textkörper in nur-Text um.</span><span class="sxs-lookup"><span data-stu-id="b6222-119">Converts all bodies to plain text.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b6222-120">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b6222-120">Child elements</span></span>

<span data-ttu-id="b6222-121">Keine.</span><span class="sxs-lookup"><span data-stu-id="b6222-121">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b6222-122">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b6222-122">Parent elements</span></span>

|<span data-ttu-id="b6222-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="b6222-123">**Element**</span></span>|<span data-ttu-id="b6222-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b6222-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b6222-125">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="b6222-125">ReplyToItem</span></span>](replytoitem.md) <br/> |<span data-ttu-id="b6222-126">Enthält eine Antwort an den Absender eines Elements in der Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="b6222-126">Contains a reply to the sender of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="b6222-127">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="b6222-127">ReplyAllToItem</span></span>](replyalltoitem.md) <br/> |<span data-ttu-id="b6222-128">Enthält eine Antwort an den Absender und alle identifizierten Empfänger eines Elements in der Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="b6222-128">Contains a reply to the sender and all identified recipients of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="b6222-129">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="b6222-129">ForwardItem</span></span>](forwarditem.md) <br/> |<span data-ttu-id="b6222-130">Enthält ein Exchange-Speicher-Element an Empfänger weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="b6222-130">Contains an Exchange store item to forward to recipients.</span></span>  <br/> |
|[<span data-ttu-id="b6222-131">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="b6222-131">CancelCalendarItem</span></span>](cancelcalendaritem.md) <br/> |<span data-ttu-id="b6222-132">Stellt das Antwortobjekt, das Sie eine Besprechung absagen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b6222-132">Represents the response object that is used to cancel a meeting.</span></span>  <br/> |
|[<span data-ttu-id="b6222-133">PostReplyItem</span><span class="sxs-lookup"><span data-stu-id="b6222-133">PostReplyItem</span></span>](postreplyitem.md) <br/> |<span data-ttu-id="b6222-134">Enthält eine Antwort auf ein Post-Element.</span><span class="sxs-lookup"><span data-stu-id="b6222-134">Contains a reply to a post item.</span></span> <span data-ttu-id="b6222-135">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b6222-135">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b6222-136">Textwert</span><span class="sxs-lookup"><span data-stu-id="b6222-136">Text value</span></span>

<span data-ttu-id="b6222-137">Der Textwert stellt den neuen Textkörper Inhalt einer Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="b6222-137">The text value represents the new body content of a message.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b6222-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b6222-138">Remarks</span></span>

<span data-ttu-id="b6222-139">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Exchange-Servers, auf dem die Client Zugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="b6222-139">The schema that describes this element is located in the EWS virtual directory of the Exchange server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b6222-140">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="b6222-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b6222-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="b6222-141">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b6222-142">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b6222-142">Schema Name</span></span>  <br/> |<span data-ttu-id="b6222-143">Schematypen</span><span class="sxs-lookup"><span data-stu-id="b6222-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="b6222-144">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b6222-144">Validation File</span></span>  <br/> |<span data-ttu-id="b6222-145">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b6222-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b6222-146">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="b6222-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="b6222-147">False</span><span class="sxs-lookup"><span data-stu-id="b6222-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b6222-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b6222-148">See also</span></span>



- [<span data-ttu-id="b6222-149">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="b6222-149">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

