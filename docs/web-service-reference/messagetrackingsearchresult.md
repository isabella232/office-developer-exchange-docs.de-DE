---
title: MessageTrackingSearchResult
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MessageTrackingSearchResult
api_type:
- schema
ms.assetid: 8ea77aa8-b93f-4287-be36-0a9da06e0946
description: Das MessageTrackingSearchResult-Element enthält ein einzelnes Nachrichten Ergebnis für ein FindMessageTrackingReportResponse-Element.
ms.openlocfilehash: 27e70cd9e11b480ab6bbb9b28275f142da7c76ac
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466682"
---
# <a name="messagetrackingsearchresult"></a><span data-ttu-id="989f3-103">MessageTrackingSearchResult</span><span class="sxs-lookup"><span data-stu-id="989f3-103">MessageTrackingSearchResult</span></span>

<span data-ttu-id="989f3-104">Das **MessageTrackingSearchResult** -Element enthält ein einzelnes Nachrichten Ergebnis für ein [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="989f3-104">The **MessageTrackingSearchResult** element contains a single message result for a [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) element.</span></span> 
  
```xml
<MessageTrackingSearchResult>
   <Subject/>
   <Sender/>
   <PurportedSender/>
   <Recipients/>
   <SubmittedTime/>
   <MessageTrackingReportId/>
   <PreviousHopServer/>
   <FirstHopServer/>
   <Properties/>
</MessageTrackingSearchResult>
```

 <span data-ttu-id="989f3-105">**FindMessageTrackingSearchResultType**</span><span class="sxs-lookup"><span data-stu-id="989f3-105">**FindMessageTrackingSearchResultType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="989f3-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="989f3-106">Attributes and elements</span></span>

<span data-ttu-id="989f3-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="989f3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="989f3-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="989f3-108">Attributes</span></span>

<span data-ttu-id="989f3-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="989f3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="989f3-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="989f3-110">Child elements</span></span>

|<span data-ttu-id="989f3-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="989f3-111">**Element**</span></span>|<span data-ttu-id="989f3-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="989f3-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="989f3-113">Betreff</span><span class="sxs-lookup"><span data-stu-id="989f3-113">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="989f3-114">Enthält den Betreff der e-Mail-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="989f3-114">Contains the e-mail message subject.</span></span>  <br/> |
|[<span data-ttu-id="989f3-115">Absender (e-mailemailtype)</span><span class="sxs-lookup"><span data-stu-id="989f3-115">Sender (EmailAddressType)</span></span>](sender-emailaddresstype.md) <br/> |<span data-ttu-id="989f3-116">Enthält die Adresse des Absenders des e-Mail-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="989f3-116">Contains the e-mail message sender's address.</span></span>  <br/> |
|[<span data-ttu-id="989f3-117">PurportedSender</span><span class="sxs-lookup"><span data-stu-id="989f3-117">PurportedSender</span></span>](purportedsender.md) <br/> |<span data-ttu-id="989f3-118">Enthält Kontaktinformationen für den mutmaßlichen Absender einer e-Mail-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="989f3-118">Contains contact information for the alleged sender of an e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="989f3-119">Recipients (ArrayOfRecipientsType)</span><span class="sxs-lookup"><span data-stu-id="989f3-119">Recipients (ArrayOfRecipientsType)</span></span>](recipients-arrayofrecipientstype.md) <br/> |<span data-ttu-id="989f3-120">Enthält eine Liste der e-Mail-Adressen, die diese Nachricht erhalten haben.</span><span class="sxs-lookup"><span data-stu-id="989f3-120">Contains a list of e-mail addresses that received this message.</span></span>  <br/> |
|[<span data-ttu-id="989f3-121">Übermittelt</span><span class="sxs-lookup"><span data-stu-id="989f3-121">SubmittedTime</span></span>](submittedtime.md) <br/> |<span data-ttu-id="989f3-122">Enthält die Zeit, zu der die Nachricht übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="989f3-122">Contains the time that the message was submitted.</span></span>  <br/> |
|[<span data-ttu-id="989f3-123">MessageTrackingReportId</span><span class="sxs-lookup"><span data-stu-id="989f3-123">MessageTrackingReportId</span></span>](messagetrackingreportid.md) <br/> |<span data-ttu-id="989f3-124">Enthält eine interne ID, die die Nachricht in der Transportdatenbank identifiziert.</span><span class="sxs-lookup"><span data-stu-id="989f3-124">Contains an internal ID that identifies the message in the transport database.</span></span>  <br/> |
|[<span data-ttu-id="989f3-125">PreviousHopServer</span><span class="sxs-lookup"><span data-stu-id="989f3-125">PreviousHopServer</span></span>](previoushopserver.md) <br/> |<span data-ttu-id="989f3-126">Enthält den Namen des Servers in der Gesamtstruktur, der die Nachricht zuvor akzeptiert hat.</span><span class="sxs-lookup"><span data-stu-id="989f3-126">Contains the name of the server in the forest that previously accepted the message.</span></span>  <br/> |
|[<span data-ttu-id="989f3-127">FirstHopServer</span><span class="sxs-lookup"><span data-stu-id="989f3-127">FirstHopServer</span></span>](firsthopserver.md) <br/> |<span data-ttu-id="989f3-128">Enthält den Namen des Servers in der Gesamtstruktur, der die Nachricht zuerst akzeptiert hat.</span><span class="sxs-lookup"><span data-stu-id="989f3-128">Contains the name of the server in the forest that first accepted the message.</span></span>  <br/> |
|[<span data-ttu-id="989f3-129">Eigenschaften (ArrayOfTrackingPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="989f3-129">Properties (ArrayOfTrackingPropertiesType)</span></span>](properties-arrayoftrackingpropertiestype.md) <br/> |<span data-ttu-id="989f3-130">Enthält eine Liste mit einer oder mehreren Überwachungseigenschaften.</span><span class="sxs-lookup"><span data-stu-id="989f3-130">Contains a list of one or more tracking properties.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="989f3-131">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="989f3-131">Parent elements</span></span>

|<span data-ttu-id="989f3-132">**Element**</span><span class="sxs-lookup"><span data-stu-id="989f3-132">**Element**</span></span>|<span data-ttu-id="989f3-133">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="989f3-133">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="989f3-134">MessageTrackingSearchResults</span><span class="sxs-lookup"><span data-stu-id="989f3-134">MessageTrackingSearchResults</span></span>](messagetrackingsearchresults.md) <br/> |<span data-ttu-id="989f3-135">Enthält eine Liste der Nachrichten, die den Suchkriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="989f3-135">Contains a list of messages that match the search criteria.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="989f3-136">Textwert</span><span class="sxs-lookup"><span data-stu-id="989f3-136">Text value</span></span>

<span data-ttu-id="989f3-137">Keine.</span><span class="sxs-lookup"><span data-stu-id="989f3-137">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="989f3-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="989f3-138">Remarks</span></span>

<span data-ttu-id="989f3-139">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="989f3-139">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="989f3-140">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="989f3-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="989f3-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="989f3-141">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="989f3-142">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="989f3-142">Schema Name</span></span>  <br/> |<span data-ttu-id="989f3-143">Schematypen</span><span class="sxs-lookup"><span data-stu-id="989f3-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="989f3-144">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="989f3-144">Validation File</span></span>  <br/> |<span data-ttu-id="989f3-145">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="989f3-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="989f3-146">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="989f3-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="989f3-147">False</span><span class="sxs-lookup"><span data-stu-id="989f3-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="989f3-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="989f3-148">See also</span></span>



[<span data-ttu-id="989f3-149">FindMessageTrackingReport-Vorgang</span><span class="sxs-lookup"><span data-stu-id="989f3-149">FindMessageTrackingReport operation</span></span>](findmessagetrackingreport-operation.md)


- [<span data-ttu-id="989f3-150">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="989f3-150">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

