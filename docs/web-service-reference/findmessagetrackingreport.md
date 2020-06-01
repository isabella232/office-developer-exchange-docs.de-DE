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
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462936"
---
# <a name="findmessagetrackingreport"></a><span data-ttu-id="e95be-103">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="e95be-103">FindMessageTrackingReport</span></span>

<span data-ttu-id="e95be-104">Das **FindMessageTrackingReport** -Element gibt Kriterien für die Typen von Nachrichten an, die gesucht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e95be-104">The **FindMessageTrackingReport** element specifies criteria for the types of messages to find.</span></span> 
  
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

 <span data-ttu-id="e95be-105">**FindMessageTrackingReportRequestType**</span><span class="sxs-lookup"><span data-stu-id="e95be-105">**FindMessageTrackingReportRequestType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e95be-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e95be-106">Attributes and elements</span></span>

<span data-ttu-id="e95be-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e95be-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e95be-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="e95be-108">Attributes</span></span>

<span data-ttu-id="e95be-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="e95be-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e95be-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e95be-110">Child elements</span></span>

|<span data-ttu-id="e95be-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="e95be-111">**Element**</span></span>|<span data-ttu-id="e95be-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e95be-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e95be-113">Bereich (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="e95be-113">Scope (NonEmptyStringType)</span></span>](scope-nonemptystringtype.md) <br/> |<span data-ttu-id="e95be-114">Stellt dar, wie umfangreich der Nachrichtenverfolgungsbericht sein soll.</span><span class="sxs-lookup"><span data-stu-id="e95be-114">Represents how extensive the message tracking report should be.</span></span>  <br/> |
|[<span data-ttu-id="e95be-115">Domäne (Nachrichtenverfolgung)</span><span class="sxs-lookup"><span data-stu-id="e95be-115">Domain (Message Tracking)</span></span>](domain-message-tracking.md) <br/> |<span data-ttu-id="e95be-116">Enthält den Namen der Domäne, in der die Nachrichtenverfolgung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e95be-116">Contains the name of the domain where the message tracking is executed.</span></span>  <br/> |
|[<span data-ttu-id="e95be-117">Absender (e-mailemailtype)</span><span class="sxs-lookup"><span data-stu-id="e95be-117">Sender (EmailAddressType)</span></span>](sender-emailaddresstype.md) <br/> |<span data-ttu-id="e95be-118">Enthält Kontaktinformationen für den Absender der e-Mail-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="e95be-118">Contains contact information for the sender of the e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="e95be-119">PurportedSender</span><span class="sxs-lookup"><span data-stu-id="e95be-119">PurportedSender</span></span>](purportedsender.md) <br/> |<span data-ttu-id="e95be-120">Enthält Kontaktinformationen für den mutmaßlichen Absender einer e-Mail-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="e95be-120">Contains contact information for the alleged sender of an e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="e95be-121">Empfänger</span><span class="sxs-lookup"><span data-stu-id="e95be-121">Recipient</span></span>](recipient.md) <br/> |<span data-ttu-id="e95be-122">Enthält die e-Mail-Adresse des Empfängers der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="e95be-122">Contains the e-mail address for the recipient of the message.</span></span>  <br/> |
|[<span data-ttu-id="e95be-123">Betreff</span><span class="sxs-lookup"><span data-stu-id="e95be-123">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="e95be-124">Enthält den Betreff der e-Mail-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="e95be-124">Contains the subject of the e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="e95be-125">StartDateTime</span><span class="sxs-lookup"><span data-stu-id="e95be-125">StartDateTime</span></span>](startdatetime.md) <br/> |<span data-ttu-id="e95be-126">Enthält das Startdatum und die Startzeit für die Suche.</span><span class="sxs-lookup"><span data-stu-id="e95be-126">Contains the starting date and time for the search.</span></span>  <br/> |
|[<span data-ttu-id="e95be-127">EndDateTime</span><span class="sxs-lookup"><span data-stu-id="e95be-127">EndDateTime</span></span>](enddatetime.md) <br/> |<span data-ttu-id="e95be-128">Enthält das Enddatum und die Endzeit für die Suche.</span><span class="sxs-lookup"><span data-stu-id="e95be-128">Contains the ending date and time for the search.</span></span>  <br/> |
|[<span data-ttu-id="e95be-129">MessageId</span><span class="sxs-lookup"><span data-stu-id="e95be-129">MessageId</span></span>](messageid.md) <br/> |<span data-ttu-id="e95be-130">Enthält den Nachrichtenbezeichner für die Suche.</span><span class="sxs-lookup"><span data-stu-id="e95be-130">Contains the message identifier for the search.</span></span>  <br/> |
|[<span data-ttu-id="e95be-131">FederatedDeliveryMailbox</span><span class="sxs-lookup"><span data-stu-id="e95be-131">FederatedDeliveryMailbox</span></span>](federateddeliverymailbox.md) <br/> |<span data-ttu-id="e95be-132">Enthält den Namen des Postfachs, in dem die standortübergreifende Nachricht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="e95be-132">Contains the name of the mailbox where the cross-premise message was sent.</span></span>  <br/> |
|[<span data-ttu-id="e95be-133">DiagnosticsLevel</span><span class="sxs-lookup"><span data-stu-id="e95be-133">DiagnosticsLevel</span></span>](diagnosticslevel.md) <br/> |<span data-ttu-id="e95be-134">Stellt die Detailebene für Diagnoseberichte dar.</span><span class="sxs-lookup"><span data-stu-id="e95be-134">Represents the level of detail for diagnostic reports.</span></span>  <br/> |
|[<span data-ttu-id="e95be-135">ServerHint</span><span class="sxs-lookup"><span data-stu-id="e95be-135">ServerHint</span></span>](serverhint.md) <br/> |<span data-ttu-id="e95be-136">Stellt den Ausgangspunkt zum Nachverfolgen einer Nachricht an einem Remotestandort oder einer Remotegesamtstruktur dar.</span><span class="sxs-lookup"><span data-stu-id="e95be-136">Represents the starting point for tracking a message in a remote site or forest.</span></span>  <br/> |
|[<span data-ttu-id="e95be-137">Eigenschaften (ArrayOfTrackingPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="e95be-137">Properties (ArrayOfTrackingPropertiesType)</span></span>](properties-arrayoftrackingpropertiestype.md) <br/> |<span data-ttu-id="e95be-138">Enthält eine Liste mit einer oder mehreren Überwachungseigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e95be-138">Contains a list of one or more tracking properties.</span></span> <span data-ttu-id="e95be-139">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="e95be-139">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e95be-140">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e95be-140">Parent elements</span></span>

<span data-ttu-id="e95be-141">Keine.</span><span class="sxs-lookup"><span data-stu-id="e95be-141">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="e95be-142">Textwert</span><span class="sxs-lookup"><span data-stu-id="e95be-142">Text value</span></span>

<span data-ttu-id="e95be-143">Keine.</span><span class="sxs-lookup"><span data-stu-id="e95be-143">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e95be-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e95be-144">Remarks</span></span>

<span data-ttu-id="e95be-145">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="e95be-145">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e95be-146">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="e95be-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e95be-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="e95be-147">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e95be-148">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e95be-148">Schema Name</span></span>  <br/> |<span data-ttu-id="e95be-149">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="e95be-149">Messages schema</span></span>  <br/> |
|<span data-ttu-id="e95be-150">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e95be-150">Validation File</span></span>  <br/> |<span data-ttu-id="e95be-151">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="e95be-151">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e95be-152">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="e95be-152">Can be Empty</span></span>  <br/> |<span data-ttu-id="e95be-153">False</span><span class="sxs-lookup"><span data-stu-id="e95be-153">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e95be-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e95be-154">See also</span></span>



[<span data-ttu-id="e95be-155">FindMessageTrackingReport-Vorgang</span><span class="sxs-lookup"><span data-stu-id="e95be-155">FindMessageTrackingReport operation</span></span>](findmessagetrackingreport-operation.md)


- [<span data-ttu-id="e95be-156">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="e95be-156">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

