---
title: MessageTrackingReport
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MessageTrackingReport
api_type:
- schema
ms.assetid: 2740bcf6-f86d-4756-a0f2-24ed6e9b75f7
description: Das MessageTrackingReport-Element enthält eine Nachricht, die in einem Vorgang GetMessageTrackingReport zurückgegeben wird.
ms.openlocfilehash: d01e0fbf099d096c7f255a8e94070e330577e6ca
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830457"
---
# <a name="messagetrackingreport"></a><span data-ttu-id="1f542-103">MessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="1f542-103">MessageTrackingReport</span></span>

<span data-ttu-id="1f542-104">Das **MessageTrackingReport** -Element enthält eine Nachricht, die in einem [Vorgang GetMessageTrackingReport](getmessagetrackingreport-operation.md)zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1f542-104">The **MessageTrackingReport** element contains a single message that is returned in a [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md).</span></span>
  
```XML
<MessageTrackingReport>
   <Sender/>
   <PurportedSender/>
   <Subject/>
   <SubmitTime/>
   <OriginalRecipients/>
   <RecipientTrackingEvents/>
   <Properties/>
</MessageTrackingReport>
```

 <span data-ttu-id="1f542-105">**MessageTrackingReportType**</span><span class="sxs-lookup"><span data-stu-id="1f542-105">**MessageTrackingReportType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1f542-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1f542-106">Attributes and elements</span></span>

<span data-ttu-id="1f542-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1f542-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1f542-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="1f542-108">Attributes</span></span>

<span data-ttu-id="1f542-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="1f542-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1f542-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1f542-110">Child elements</span></span>

|<span data-ttu-id="1f542-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="1f542-111">**Element**</span></span>|<span data-ttu-id="1f542-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1f542-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1f542-113">Absender (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="1f542-113">Sender (EmailAddressType)</span></span>](sender-emailaddresstype.md) <br/> |<span data-ttu-id="1f542-114">Kontaktinformationen für den Absender der E-mail-Nachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="1f542-114">Contains contact information for the sender of the e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="1f542-115">PurportedSender</span><span class="sxs-lookup"><span data-stu-id="1f542-115">PurportedSender</span></span>](purportedsender.md) <br/> |<span data-ttu-id="1f542-116">Kontaktinformationen für den Absender einer e-Mail-Nachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="1f542-116">Contains contact information for the alleged sender of an e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="1f542-117">Betreff</span><span class="sxs-lookup"><span data-stu-id="1f542-117">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="1f542-118">Enthält den Betreff der E-mail-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="1f542-118">Contains the subject of the e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="1f542-119">SubmitTime</span><span class="sxs-lookup"><span data-stu-id="1f542-119">SubmitTime</span></span>](submittime.md) <br/> |<span data-ttu-id="1f542-120">Enthält die Tageszeit, die die e-Mail-Nachricht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="1f542-120">Contains the time of day that the e-mail message was submitted.</span></span>  <br/> |
|[<span data-ttu-id="1f542-121">OriginalRecipients</span><span class="sxs-lookup"><span data-stu-id="1f542-121">OriginalRecipients</span></span>](originalrecipients.md) <br/> |<span data-ttu-id="1f542-122">Enthält eine Liste der Empfänger der E-mail-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="1f542-122">Contains a list of the recipients of the e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="1f542-123">RecipientTrackingEvents</span><span class="sxs-lookup"><span data-stu-id="1f542-123">RecipientTrackingEvents</span></span>](recipienttrackingevents.md) <br/> |<span data-ttu-id="1f542-124">Enthält eine Liste mit mindestens einen Tracking-Ereignissen für die Empfänger an.</span><span class="sxs-lookup"><span data-stu-id="1f542-124">Contains a list of one or more tracking events for the recipients.</span></span>  <br/> |
|[<span data-ttu-id="1f542-125">Eigenschaften (ArrayOfTrackingPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="1f542-125">Properties (ArrayOfTrackingPropertiesType)</span></span>](properties-arrayoftrackingpropertiestype.md) <br/> |<span data-ttu-id="1f542-126">Enthält eine Liste der Eigenschaften für eine oder mehrere Tracking an.</span><span class="sxs-lookup"><span data-stu-id="1f542-126">Contains a list of one or more tracking properties.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1f542-127">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1f542-127">Parent elements</span></span>

|<span data-ttu-id="1f542-128">**Element**</span><span class="sxs-lookup"><span data-stu-id="1f542-128">**Element**</span></span>|<span data-ttu-id="1f542-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1f542-129">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1f542-130">GetMessageTrackingReportResponse</span><span class="sxs-lookup"><span data-stu-id="1f542-130">GetMessageTrackingReportResponse</span></span>](getmessagetrackingreportresponse.md) <br/> |<span data-ttu-id="1f542-131">Enthält das Ergebnis einer einzelnen Anforderung [GetMessageTrackingReport Vorgang](getmessagetrackingreport-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="1f542-131">Contains the result of a single [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1f542-132">Textwert</span><span class="sxs-lookup"><span data-stu-id="1f542-132">Text value</span></span>

<span data-ttu-id="1f542-133">Keine.</span><span class="sxs-lookup"><span data-stu-id="1f542-133">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1f542-134">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1f542-134">Remarks</span></span>

<span data-ttu-id="1f542-135">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="1f542-135">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1f542-136">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="1f542-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1f542-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="1f542-137">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="1f542-138">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="1f542-138">Schema Name</span></span>  <br/> |<span data-ttu-id="1f542-139">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="1f542-139">Messages schema</span></span>  <br/> |
|<span data-ttu-id="1f542-140">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="1f542-140">Validation File</span></span>  <br/> |<span data-ttu-id="1f542-141">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="1f542-141">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1f542-142">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="1f542-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="1f542-143">False</span><span class="sxs-lookup"><span data-stu-id="1f542-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1f542-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1f542-144">See also</span></span>



[<span data-ttu-id="1f542-145">FindMessageTrackingReport-Vorgang</span><span class="sxs-lookup"><span data-stu-id="1f542-145">FindMessageTrackingReport operation</span></span>](findmessagetrackingreport-operation.md)
  
[<span data-ttu-id="1f542-146">GetMessageTrackingReport-Vorgang</span><span class="sxs-lookup"><span data-stu-id="1f542-146">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="1f542-147">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="1f542-147">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
  
- [<span data-ttu-id="1f542-148">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="1f542-148">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

