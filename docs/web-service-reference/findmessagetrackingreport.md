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
description: Das FindMessageTrackingReport-Element gibt Kriterien für die Typen von Nachrichten an, die gesucht werden sollen.
ms.openlocfilehash: d30e5391bb4305cae0004a9788df971a57297cae
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462936"
---
# <a name="findmessagetrackingreport"></a><span data-ttu-id="3533b-103">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="3533b-103">FindMessageTrackingReport</span></span>

<span data-ttu-id="3533b-104">Das **FindMessageTrackingReport** -Element gibt Kriterien für die Typen von Nachrichten an, die gesucht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3533b-104">The **FindMessageTrackingReport** element specifies criteria for the types of messages to find.</span></span> 
  
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

 <span data-ttu-id="3533b-105">**FindMessageTrackingReportRequestType**</span><span class="sxs-lookup"><span data-stu-id="3533b-105">**FindMessageTrackingReportRequestType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3533b-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3533b-106">Attributes and elements</span></span>

<span data-ttu-id="3533b-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="3533b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3533b-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="3533b-108">Attributes</span></span>

<span data-ttu-id="3533b-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="3533b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3533b-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3533b-110">Child elements</span></span>

|<span data-ttu-id="3533b-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="3533b-111">**Element**</span></span>|<span data-ttu-id="3533b-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3533b-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3533b-113">Bereich (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="3533b-113">Scope (NonEmptyStringType)</span></span>](scope-nonemptystringtype.md) <br/> |<span data-ttu-id="3533b-114">Stellt dar, wie umfangreich der Nachrichtenverfolgungsbericht sein soll.</span><span class="sxs-lookup"><span data-stu-id="3533b-114">Represents how extensive the message tracking report should be.</span></span>  <br/> |
|[<span data-ttu-id="3533b-115">Domäne (Nachrichtenverfolgung)</span><span class="sxs-lookup"><span data-stu-id="3533b-115">Domain (Message Tracking)</span></span>](domain-message-tracking.md) <br/> |<span data-ttu-id="3533b-116">Enthält den Namen der Domäne, in der die Nachrichtenverfolgung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3533b-116">Contains the name of the domain where the message tracking is executed.</span></span>  <br/> |
|[<span data-ttu-id="3533b-117">Absender (e-mailemailtype)</span><span class="sxs-lookup"><span data-stu-id="3533b-117">Sender (EmailAddressType)</span></span>](sender-emailaddresstype.md) <br/> |<span data-ttu-id="3533b-118">Enthält Kontaktinformationen für den Absender der e-Mail-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="3533b-118">Contains contact information for the sender of the e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="3533b-119">PurportedSender</span><span class="sxs-lookup"><span data-stu-id="3533b-119">PurportedSender</span></span>](purportedsender.md) <br/> |<span data-ttu-id="3533b-120">Enthält Kontaktinformationen für den mutmaßlichen Absender einer e-Mail-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="3533b-120">Contains contact information for the alleged sender of an e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="3533b-121">Empfänger</span><span class="sxs-lookup"><span data-stu-id="3533b-121">Recipient</span></span>](recipient.md) <br/> |<span data-ttu-id="3533b-122">Enthält die e-Mail-Adresse des Empfängers der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="3533b-122">Contains the e-mail address for the recipient of the message.</span></span>  <br/> |
|[<span data-ttu-id="3533b-123">Betreff</span><span class="sxs-lookup"><span data-stu-id="3533b-123">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="3533b-124">Enthält den Betreff der e-Mail-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="3533b-124">Contains the subject of the e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="3533b-125">StartDateTime</span><span class="sxs-lookup"><span data-stu-id="3533b-125">StartDateTime</span></span>](startdatetime.md) <br/> |<span data-ttu-id="3533b-126">Enthält das Startdatum und die Startzeit für die Suche.</span><span class="sxs-lookup"><span data-stu-id="3533b-126">Contains the starting date and time for the search.</span></span>  <br/> |
|[<span data-ttu-id="3533b-127">EndDateTime</span><span class="sxs-lookup"><span data-stu-id="3533b-127">EndDateTime</span></span>](enddatetime.md) <br/> |<span data-ttu-id="3533b-128">Enthält das Enddatum und die Endzeit für die Suche.</span><span class="sxs-lookup"><span data-stu-id="3533b-128">Contains the ending date and time for the search.</span></span>  <br/> |
|[<span data-ttu-id="3533b-129">MessageId</span><span class="sxs-lookup"><span data-stu-id="3533b-129">MessageId</span></span>](messageid.md) <br/> |<span data-ttu-id="3533b-130">Enthält den Nachrichtenbezeichner für die Suche.</span><span class="sxs-lookup"><span data-stu-id="3533b-130">Contains the message identifier for the search.</span></span>  <br/> |
|[<span data-ttu-id="3533b-131">FederatedDeliveryMailbox</span><span class="sxs-lookup"><span data-stu-id="3533b-131">FederatedDeliveryMailbox</span></span>](federateddeliverymailbox.md) <br/> |<span data-ttu-id="3533b-132">Enthält den Namen des Postfachs, in dem die standortübergreifende Nachricht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="3533b-132">Contains the name of the mailbox where the cross-premise message was sent.</span></span>  <br/> |
|[<span data-ttu-id="3533b-133">DiagnosticsLevel</span><span class="sxs-lookup"><span data-stu-id="3533b-133">DiagnosticsLevel</span></span>](diagnosticslevel.md) <br/> |<span data-ttu-id="3533b-134">Stellt die Detailebene für Diagnoseberichte dar.</span><span class="sxs-lookup"><span data-stu-id="3533b-134">Represents the level of detail for diagnostic reports.</span></span>  <br/> |
|[<span data-ttu-id="3533b-135">ServerHint</span><span class="sxs-lookup"><span data-stu-id="3533b-135">ServerHint</span></span>](serverhint.md) <br/> |<span data-ttu-id="3533b-136">Stellt den Ausgangspunkt zum Nachverfolgen einer Nachricht an einem Remotestandort oder einer Remotegesamtstruktur dar.</span><span class="sxs-lookup"><span data-stu-id="3533b-136">Represents the starting point for tracking a message in a remote site or forest.</span></span>  <br/> |
|[<span data-ttu-id="3533b-137">Eigenschaften (ArrayOfTrackingPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="3533b-137">Properties (ArrayOfTrackingPropertiesType)</span></span>](properties-arrayoftrackingpropertiestype.md) <br/> |<span data-ttu-id="3533b-138">Enthält eine Liste mit einer oder mehreren Überwachungseigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3533b-138">Contains a list of one or more tracking properties.</span></span> <span data-ttu-id="3533b-139">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="3533b-139">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3533b-140">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3533b-140">Parent elements</span></span>

<span data-ttu-id="3533b-141">Keine.</span><span class="sxs-lookup"><span data-stu-id="3533b-141">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="3533b-142">Textwert</span><span class="sxs-lookup"><span data-stu-id="3533b-142">Text value</span></span>

<span data-ttu-id="3533b-143">Keine.</span><span class="sxs-lookup"><span data-stu-id="3533b-143">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3533b-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3533b-144">Remarks</span></span>

<span data-ttu-id="3533b-145">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="3533b-145">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3533b-146">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="3533b-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3533b-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="3533b-147">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="3533b-148">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="3533b-148">Schema Name</span></span>  <br/> |<span data-ttu-id="3533b-149">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="3533b-149">Messages schema</span></span>  <br/> |
|<span data-ttu-id="3533b-150">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="3533b-150">Validation File</span></span>  <br/> |<span data-ttu-id="3533b-151">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="3533b-151">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3533b-152">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="3533b-152">Can be Empty</span></span>  <br/> |<span data-ttu-id="3533b-153">False</span><span class="sxs-lookup"><span data-stu-id="3533b-153">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3533b-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3533b-154">See also</span></span>



[<span data-ttu-id="3533b-155">FindMessageTrackingReport-Vorgang</span><span class="sxs-lookup"><span data-stu-id="3533b-155">FindMessageTrackingReport operation</span></span>](findmessagetrackingreport-operation.md)


- [<span data-ttu-id="3533b-156">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="3533b-156">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

