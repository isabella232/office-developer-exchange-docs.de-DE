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
description: Das MessageTrackingSearchResult-Element enthält eine einzelne Nachricht Ergebnis für ein FindMessageTrackingReportResponse-Element.
ms.openlocfilehash: ad4fb9d9e2266222303bd2015a7afba0bb46721b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830460"
---
# <a name="messagetrackingsearchresult"></a><span data-ttu-id="1e1d8-103">MessageTrackingSearchResult</span><span class="sxs-lookup"><span data-stu-id="1e1d8-103">MessageTrackingSearchResult</span></span>

<span data-ttu-id="1e1d8-104">Das **MessageTrackingSearchResult** -Element enthält eine einzelne Nachricht Ergebnis für ein [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="1e1d8-104">The **MessageTrackingSearchResult** element contains a single message result for a [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) element.</span></span> 
  
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

 <span data-ttu-id="1e1d8-105">**FindMessageTrackingSearchResultType**</span><span class="sxs-lookup"><span data-stu-id="1e1d8-105">**FindMessageTrackingSearchResultType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1e1d8-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1e1d8-106">Attributes and elements</span></span>

<span data-ttu-id="1e1d8-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1e1d8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1e1d8-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="1e1d8-108">Attributes</span></span>

<span data-ttu-id="1e1d8-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="1e1d8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1e1d8-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1e1d8-110">Child elements</span></span>

|<span data-ttu-id="1e1d8-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="1e1d8-111">**Element**</span></span>|<span data-ttu-id="1e1d8-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1e1d8-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1e1d8-113">Betreff</span><span class="sxs-lookup"><span data-stu-id="1e1d8-113">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="1e1d8-114">Der Betreff der e-Mail-Nachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="1e1d8-114">Contains the e-mail message subject.</span></span>  <br/> |
|[<span data-ttu-id="1e1d8-115">Absender (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="1e1d8-115">Sender (EmailAddressType)</span></span>](sender-emailaddresstype.md) <br/> |<span data-ttu-id="1e1d8-116">Enthält die e-Mail-Nachricht Adresse des Absenders.</span><span class="sxs-lookup"><span data-stu-id="1e1d8-116">Contains the e-mail message sender's address.</span></span>  <br/> |
|[<span data-ttu-id="1e1d8-117">PurportedSender</span><span class="sxs-lookup"><span data-stu-id="1e1d8-117">PurportedSender</span></span>](purportedsender.md) <br/> |<span data-ttu-id="1e1d8-118">Kontaktinformationen für den Absender einer e-Mail-Nachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="1e1d8-118">Contains contact information for the alleged sender of an e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="1e1d8-119">Empfänger (ArrayOfRecipientsType)</span><span class="sxs-lookup"><span data-stu-id="1e1d8-119">Recipients (ArrayOfRecipientsType)</span></span>](recipients-arrayofrecipientstype.md) <br/> |<span data-ttu-id="1e1d8-120">Enthält eine Liste von E-mail-Adressen, die diese Meldung erhalten.</span><span class="sxs-lookup"><span data-stu-id="1e1d8-120">Contains a list of e-mail addresses that received this message.</span></span>  <br/> |
|[<span data-ttu-id="1e1d8-121">SubmittedTime</span><span class="sxs-lookup"><span data-stu-id="1e1d8-121">SubmittedTime</span></span>](submittedtime.md) <br/> |<span data-ttu-id="1e1d8-122">Enthält die Zeit, die die Nachricht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="1e1d8-122">Contains the time that the message was submitted.</span></span>  <br/> |
|[<span data-ttu-id="1e1d8-123">MessageTrackingReportId</span><span class="sxs-lookup"><span data-stu-id="1e1d8-123">MessageTrackingReportId</span></span>](messagetrackingreportid.md) <br/> |<span data-ttu-id="1e1d8-124">Enthält eine interne ID, die Nachricht in der Datenbank Transport identifiziert.</span><span class="sxs-lookup"><span data-stu-id="1e1d8-124">Contains an internal ID that identifies the message in the transport database.</span></span>  <br/> |
|[<span data-ttu-id="1e1d8-125">PreviousHopServer</span><span class="sxs-lookup"><span data-stu-id="1e1d8-125">PreviousHopServer</span></span>](previoushopserver.md) <br/> |<span data-ttu-id="1e1d8-126">Enthält den Namen des Servers in der Gesamtstruktur, die zuvor die Nachricht akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="1e1d8-126">Contains the name of the server in the forest that previously accepted the message.</span></span>  <br/> |
|[<span data-ttu-id="1e1d8-127">FirstHopServer</span><span class="sxs-lookup"><span data-stu-id="1e1d8-127">FirstHopServer</span></span>](firsthopserver.md) <br/> |<span data-ttu-id="1e1d8-128">Enthält den Namen des Servers in der Gesamtstruktur, die zuerst die Nachricht akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="1e1d8-128">Contains the name of the server in the forest that first accepted the message.</span></span>  <br/> |
|[<span data-ttu-id="1e1d8-129">Eigenschaften (ArrayOfTrackingPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="1e1d8-129">Properties (ArrayOfTrackingPropertiesType)</span></span>](properties-arrayoftrackingpropertiestype.md) <br/> |<span data-ttu-id="1e1d8-130">Enthält eine Liste der Eigenschaften für eine oder mehrere Tracking an.</span><span class="sxs-lookup"><span data-stu-id="1e1d8-130">Contains a list of one or more tracking properties.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1e1d8-131">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1e1d8-131">Parent elements</span></span>

|<span data-ttu-id="1e1d8-132">**Element**</span><span class="sxs-lookup"><span data-stu-id="1e1d8-132">**Element**</span></span>|<span data-ttu-id="1e1d8-133">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1e1d8-133">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1e1d8-134">MessageTrackingSearchResults</span><span class="sxs-lookup"><span data-stu-id="1e1d8-134">MessageTrackingSearchResults</span></span>](messagetrackingsearchresults.md) <br/> |<span data-ttu-id="1e1d8-135">Enthält eine Liste von Nachrichten, die den Suchkriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="1e1d8-135">Contains a list of messages that match the search criteria.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1e1d8-136">Textwert</span><span class="sxs-lookup"><span data-stu-id="1e1d8-136">Text value</span></span>

<span data-ttu-id="1e1d8-137">Keine.</span><span class="sxs-lookup"><span data-stu-id="1e1d8-137">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1e1d8-138">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1e1d8-138">Remarks</span></span>

<span data-ttu-id="1e1d8-139">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="1e1d8-139">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1e1d8-140">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="1e1d8-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1e1d8-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="1e1d8-141">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1e1d8-142">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="1e1d8-142">Schema Name</span></span>  <br/> |<span data-ttu-id="1e1d8-143">Schematypen</span><span class="sxs-lookup"><span data-stu-id="1e1d8-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="1e1d8-144">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="1e1d8-144">Validation File</span></span>  <br/> |<span data-ttu-id="1e1d8-145">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1e1d8-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1e1d8-146">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="1e1d8-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="1e1d8-147">False</span><span class="sxs-lookup"><span data-stu-id="1e1d8-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1e1d8-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1e1d8-148">See also</span></span>



[<span data-ttu-id="1e1d8-149">FindMessageTrackingReport-Vorgang</span><span class="sxs-lookup"><span data-stu-id="1e1d8-149">FindMessageTrackingReport operation</span></span>](findmessagetrackingreport-operation.md)


- [<span data-ttu-id="1e1d8-150">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="1e1d8-150">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

