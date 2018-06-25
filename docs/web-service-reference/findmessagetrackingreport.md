---
title: FindMessageTrackingReport
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FindMessageTrackingReport
api_type:
- schema
ms.assetid: 7ca6e2f7-aae1-4920-b839-73513ba8d4d8
description: Das FindMessageTrackingReport-Element gibt die Kriterien für die Typen von Nachrichten suchen.
ms.openlocfilehash: 77545121aa056992248c045af3f3d36566678b94
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758468"
---
# <a name="findmessagetrackingreport"></a><span data-ttu-id="fee89-103">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="fee89-103">FindMessageTrackingReport</span></span>

<span data-ttu-id="fee89-104">Das **FindMessageTrackingReport** -Element gibt die Kriterien für die Typen von Nachrichten suchen.</span><span class="sxs-lookup"><span data-stu-id="fee89-104">The **FindMessageTrackingReport** element specifies criteria for the types of messages to find.</span></span> 
  
```xml
<FindMessageTrackingReport>
   <Scope/>
   <Domain/>
   <Sender/>
   <PurportedSender/>
   <Recipient/>
   <Subject/>
   <StartDateTime/>
   <EndDateTime/>
   <MessageId/>
   <FederatedDeliveryMailbox/>
   <DiagnosticsLevel/>
   <ServerHint/>
   <Properties/>
</FindMessageTrackingReport>
```

 <span data-ttu-id="fee89-105">**FindMessageTrackingReportRequestType**</span><span class="sxs-lookup"><span data-stu-id="fee89-105">**FindMessageTrackingReportRequestType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fee89-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="fee89-106">Attributes and elements</span></span>

<span data-ttu-id="fee89-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="fee89-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fee89-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="fee89-108">Attributes</span></span>

<span data-ttu-id="fee89-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="fee89-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fee89-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fee89-110">Child elements</span></span>

|<span data-ttu-id="fee89-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="fee89-111">**Element**</span></span>|<span data-ttu-id="fee89-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fee89-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fee89-113">Bereich (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="fee89-113">Scope (NonEmptyStringType)</span></span>](scope-nonemptystringtype.md) <br/> |<span data-ttu-id="fee89-114">Stellt dar, wie umfangreich die nachrichtenverfolgung Bericht werden soll.</span><span class="sxs-lookup"><span data-stu-id="fee89-114">Represents how extensive the message tracking report should be.</span></span>  <br/> |
|[<span data-ttu-id="fee89-115">Domäne (Nachrichtenverfolgung)</span><span class="sxs-lookup"><span data-stu-id="fee89-115">Domain (Message Tracking)</span></span>](domain-message-tracking.md) <br/> |<span data-ttu-id="fee89-116">Enthält den Namen der Domäne, in der mit der Verfolgung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fee89-116">Contains the name of the domain where the message tracking is executed.</span></span>  <br/> |
|[<span data-ttu-id="fee89-117">Absender (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="fee89-117">Sender (EmailAddressType)</span></span>](sender-emailaddresstype.md) <br/> |<span data-ttu-id="fee89-118">Kontaktinformationen für den Absender der E-mail-Nachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="fee89-118">Contains contact information for the sender of the e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="fee89-119">PurportedSender</span><span class="sxs-lookup"><span data-stu-id="fee89-119">PurportedSender</span></span>](purportedsender.md) <br/> |<span data-ttu-id="fee89-120">Kontaktinformationen für den Absender einer e-Mail-Nachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="fee89-120">Contains contact information for the alleged sender of an e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="fee89-121">Recipient</span><span class="sxs-lookup"><span data-stu-id="fee89-121">Recipient</span></span>](recipient.md) <br/> |<span data-ttu-id="fee89-122">Enthält die E-mail-Adresse für den Empfänger der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="fee89-122">Contains the e-mail address for the recipient of the message.</span></span>  <br/> |
|[<span data-ttu-id="fee89-123">Betreff</span><span class="sxs-lookup"><span data-stu-id="fee89-123">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="fee89-124">Enthält den Betreff der E-mail-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="fee89-124">Contains the subject of the e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="fee89-125">StartDateTime</span><span class="sxs-lookup"><span data-stu-id="fee89-125">StartDateTime</span></span>](startdatetime.md) <br/> |<span data-ttu-id="fee89-126">Enthält das Datum und die Uhrzeit für die Suche.</span><span class="sxs-lookup"><span data-stu-id="fee89-126">Contains the starting date and time for the search.</span></span>  <br/> |
|[<span data-ttu-id="fee89-127">EndDateTime</span><span class="sxs-lookup"><span data-stu-id="fee89-127">EndDateTime</span></span>](enddatetime.md) <br/> |<span data-ttu-id="fee89-128">Enthält das Enddatum und die Uhrzeit für die Suche.</span><span class="sxs-lookup"><span data-stu-id="fee89-128">Contains the ending date and time for the search.</span></span>  <br/> |
|[<span data-ttu-id="fee89-129">MessageId</span><span class="sxs-lookup"><span data-stu-id="fee89-129">MessageId</span></span>](messageid.md) <br/> |<span data-ttu-id="fee89-130">Enthält die ID für die Suche an.</span><span class="sxs-lookup"><span data-stu-id="fee89-130">Contains the message identifier for the search.</span></span>  <br/> |
|[<span data-ttu-id="fee89-131">FederatedDeliveryMailbox</span><span class="sxs-lookup"><span data-stu-id="fee89-131">FederatedDeliveryMailbox</span></span>](federateddeliverymailbox.md) <br/> |<span data-ttu-id="fee89-132">Enthält den Namen des Postfachs, in dem die standortbasierte Cross-Nachricht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="fee89-132">Contains the name of the mailbox where the cross-premise message was sent.</span></span>  <br/> |
|[<span data-ttu-id="fee89-133">DiagnosticsLevel</span><span class="sxs-lookup"><span data-stu-id="fee89-133">DiagnosticsLevel</span></span>](diagnosticslevel.md) <br/> |<span data-ttu-id="fee89-134">Stellt die Detailebene für Diagnoseberichte.</span><span class="sxs-lookup"><span data-stu-id="fee89-134">Represents the level of detail for diagnostic reports.</span></span>  <br/> |
|[<span data-ttu-id="fee89-135">ServerHint</span><span class="sxs-lookup"><span data-stu-id="fee89-135">ServerHint</span></span>](serverhint.md) <br/> |<span data-ttu-id="fee89-136">Den Ausgangspunkt für Nachrichtenstatus wird in einer remote-Standort oder Gesamtstruktur darstellt.</span><span class="sxs-lookup"><span data-stu-id="fee89-136">Represents the starting point for tracking a message in a remote site or forest.</span></span>  <br/> |
|[<span data-ttu-id="fee89-137">Eigenschaften (ArrayOfTrackingPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="fee89-137">Properties (ArrayOfTrackingPropertiesType)</span></span>](properties-arrayoftrackingpropertiestype.md) <br/> |<span data-ttu-id="fee89-138">Enthält eine Liste der Eigenschaften für eine oder mehrere Tracking an.</span><span class="sxs-lookup"><span data-stu-id="fee89-138">Contains a list of one or more tracking properties.</span></span> <span data-ttu-id="fee89-139">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="fee89-139">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="fee89-140">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fee89-140">Parent elements</span></span>

<span data-ttu-id="fee89-141">Keine.</span><span class="sxs-lookup"><span data-stu-id="fee89-141">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="fee89-142">Textwert</span><span class="sxs-lookup"><span data-stu-id="fee89-142">Text value</span></span>

<span data-ttu-id="fee89-143">Keine.</span><span class="sxs-lookup"><span data-stu-id="fee89-143">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fee89-144">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fee89-144">Remarks</span></span>

<span data-ttu-id="fee89-145">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="fee89-145">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fee89-146">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="fee89-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fee89-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="fee89-147">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="fee89-148">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="fee89-148">Schema Name</span></span>  <br/> |<span data-ttu-id="fee89-149">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="fee89-149">Messages schema</span></span>  <br/> |
|<span data-ttu-id="fee89-150">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="fee89-150">Validation File</span></span>  <br/> |<span data-ttu-id="fee89-151">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="fee89-151">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="fee89-152">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="fee89-152">Can be Empty</span></span>  <br/> |<span data-ttu-id="fee89-153">False</span><span class="sxs-lookup"><span data-stu-id="fee89-153">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fee89-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fee89-154">See also</span></span>



[<span data-ttu-id="fee89-155">FindMessageTrackingReport-Vorgang</span><span class="sxs-lookup"><span data-stu-id="fee89-155">FindMessageTrackingReport operation</span></span>](findmessagetrackingreport-operation.md)


- [<span data-ttu-id="fee89-156">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="fee89-156">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

