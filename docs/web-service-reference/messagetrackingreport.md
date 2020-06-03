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
description: Das MessageTrackingReport-Element enthält eine einzelne Nachricht, die in einer GetMessageTrackingReport-Operation zurückgegeben wird.
ms.openlocfilehash: fc3e56fbb1bee411fa31751f558f520874133076
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463216"
---
# <a name="messagetrackingreport"></a><span data-ttu-id="2ff11-103">MessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="2ff11-103">MessageTrackingReport</span></span>

<span data-ttu-id="2ff11-104">Das **MessageTrackingReport** -Element enthält eine einzelne Nachricht, die in einer [GetMessageTrackingReport-Operation](getmessagetrackingreport-operation.md)zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2ff11-104">The **MessageTrackingReport** element contains a single message that is returned in a [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md).</span></span>
  
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

 <span data-ttu-id="2ff11-105">**MessageTrackingReportType**</span><span class="sxs-lookup"><span data-stu-id="2ff11-105">**MessageTrackingReportType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2ff11-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="2ff11-106">Attributes and elements</span></span>

<span data-ttu-id="2ff11-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="2ff11-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2ff11-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="2ff11-108">Attributes</span></span>

<span data-ttu-id="2ff11-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="2ff11-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2ff11-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2ff11-110">Child elements</span></span>

|<span data-ttu-id="2ff11-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="2ff11-111">**Element**</span></span>|<span data-ttu-id="2ff11-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2ff11-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2ff11-113">Absender (e-mailemailtype)</span><span class="sxs-lookup"><span data-stu-id="2ff11-113">Sender (EmailAddressType)</span></span>](sender-emailaddresstype.md) <br/> |<span data-ttu-id="2ff11-114">Enthält Kontaktinformationen für den Absender der e-Mail-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="2ff11-114">Contains contact information for the sender of the e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="2ff11-115">PurportedSender</span><span class="sxs-lookup"><span data-stu-id="2ff11-115">PurportedSender</span></span>](purportedsender.md) <br/> |<span data-ttu-id="2ff11-116">Enthält Kontaktinformationen für den mutmaßlichen Absender einer e-Mail-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="2ff11-116">Contains contact information for the alleged sender of an e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="2ff11-117">Betreff</span><span class="sxs-lookup"><span data-stu-id="2ff11-117">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="2ff11-118">Enthält den Betreff der e-Mail-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="2ff11-118">Contains the subject of the e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="2ff11-119">Übermittlungs Zeitangabe</span><span class="sxs-lookup"><span data-stu-id="2ff11-119">SubmitTime</span></span>](submittime.md) <br/> |<span data-ttu-id="2ff11-120">Enthält die Tageszeit, zu der die e-Mail-Nachricht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="2ff11-120">Contains the time of day that the e-mail message was submitted.</span></span>  <br/> |
|[<span data-ttu-id="2ff11-121">Element originalrecipients</span><span class="sxs-lookup"><span data-stu-id="2ff11-121">OriginalRecipients</span></span>](originalrecipients.md) <br/> |<span data-ttu-id="2ff11-122">Enthält eine Liste der Empfänger der e-Mail-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="2ff11-122">Contains a list of the recipients of the e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="2ff11-123">RecipientTrackingEvents</span><span class="sxs-lookup"><span data-stu-id="2ff11-123">RecipientTrackingEvents</span></span>](recipienttrackingevents.md) <br/> |<span data-ttu-id="2ff11-124">Enthält eine Liste mit einem oder mehreren Überwachungsereignissen für die Empfänger.</span><span class="sxs-lookup"><span data-stu-id="2ff11-124">Contains a list of one or more tracking events for the recipients.</span></span>  <br/> |
|[<span data-ttu-id="2ff11-125">Eigenschaften (ArrayOfTrackingPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="2ff11-125">Properties (ArrayOfTrackingPropertiesType)</span></span>](properties-arrayoftrackingpropertiestype.md) <br/> |<span data-ttu-id="2ff11-126">Enthält eine Liste mit einer oder mehreren Überwachungseigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2ff11-126">Contains a list of one or more tracking properties.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2ff11-127">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2ff11-127">Parent elements</span></span>

|<span data-ttu-id="2ff11-128">**Element**</span><span class="sxs-lookup"><span data-stu-id="2ff11-128">**Element**</span></span>|<span data-ttu-id="2ff11-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2ff11-129">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2ff11-130">GetMessageTrackingReportResponse</span><span class="sxs-lookup"><span data-stu-id="2ff11-130">GetMessageTrackingReportResponse</span></span>](getmessagetrackingreportresponse.md) <br/> |<span data-ttu-id="2ff11-131">Enthält das Ergebnis einer einzelnen [GetMessageTrackingReport-Vorgangs](getmessagetrackingreport-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="2ff11-131">Contains the result of a single [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2ff11-132">Textwert</span><span class="sxs-lookup"><span data-stu-id="2ff11-132">Text value</span></span>

<span data-ttu-id="2ff11-133">Keine.</span><span class="sxs-lookup"><span data-stu-id="2ff11-133">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2ff11-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2ff11-134">Remarks</span></span>

<span data-ttu-id="2ff11-135">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="2ff11-135">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2ff11-136">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="2ff11-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2ff11-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="2ff11-137">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2ff11-138">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="2ff11-138">Schema Name</span></span>  <br/> |<span data-ttu-id="2ff11-139">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="2ff11-139">Messages schema</span></span>  <br/> |
|<span data-ttu-id="2ff11-140">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="2ff11-140">Validation File</span></span>  <br/> |<span data-ttu-id="2ff11-141">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="2ff11-141">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2ff11-142">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="2ff11-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="2ff11-143">False</span><span class="sxs-lookup"><span data-stu-id="2ff11-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2ff11-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2ff11-144">See also</span></span>



[<span data-ttu-id="2ff11-145">FindMessageTrackingReport-Vorgang</span><span class="sxs-lookup"><span data-stu-id="2ff11-145">FindMessageTrackingReport operation</span></span>](findmessagetrackingreport-operation.md)
  
[<span data-ttu-id="2ff11-146">GetMessageTrackingReport-Vorgang</span><span class="sxs-lookup"><span data-stu-id="2ff11-146">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="2ff11-147">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="2ff11-147">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
  
- [<span data-ttu-id="2ff11-148">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="2ff11-148">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

