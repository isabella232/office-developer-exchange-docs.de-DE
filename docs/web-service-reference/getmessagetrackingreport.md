---
title: GetMessageTrackingReport
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetMessageTrackingReport
api_type:
- schema
ms.assetid: b6ffa8ef-90f6-402d-afac-c3f5ee55cf49
description: Das GetMessageTrackingReport-Element enthält die Anforderung für den GetMessageTrackingReport-Vorgang zum Abrufen des vollständigen Nachrichtenverfolgungsberichts für die angegebene ID.
ms.openlocfilehash: 30596acd209580147e0f03e12a7868502159b29c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/02/2020
ms.locfileid: "44466577"
---
# <a name="getmessagetrackingreport"></a><span data-ttu-id="32466-103">GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="32466-103">GetMessageTrackingReport</span></span>

<span data-ttu-id="32466-104">Das **GetMessageTrackingReport** -Element enthält die Anforderung für den [GetMessageTrackingReport-Vorgang](getmessagetrackingreport-operation.md) zum Abrufen des vollständigen Nachrichtenverfolgungsberichts für die angegebene ID.</span><span class="sxs-lookup"><span data-stu-id="32466-104">The **GetMessageTrackingReport** element contains the request for the [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md) to retrieve the full message tracking report for the specified ID.</span></span> 
  
```XML
<GetMessageTrackingReport>
   <Scope/>
   <ReportTemplate/>
   <RecipientFilter/>
   <MessageTrackingReportId/>
   <ReturnQueueEvents/>
   <DiagnosticsLevel/>
   <Properties/>
</GetMessageTrackingReport>
```

 <span data-ttu-id="32466-105">**GetMessageTrackingReportRequestType**</span><span class="sxs-lookup"><span data-stu-id="32466-105">**GetMessageTrackingReportRequestType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="32466-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="32466-106">Attributes and elements</span></span>

<span data-ttu-id="32466-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="32466-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="32466-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="32466-108">Attributes</span></span>

<span data-ttu-id="32466-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="32466-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="32466-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="32466-110">Child elements</span></span>

|<span data-ttu-id="32466-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="32466-111">**Element**</span></span>|<span data-ttu-id="32466-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="32466-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="32466-113">Bereich (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="32466-113">Scope (NonEmptyStringType)</span></span>](scope-nonemptystringtype.md) <br/> |<span data-ttu-id="32466-114">Gibt an, wo die Suche durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="32466-114">Specifies where to perform the search.</span></span> <span data-ttu-id="32466-115">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="32466-115">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="32466-116">Report Template</span><span class="sxs-lookup"><span data-stu-id="32466-116">ReportTemplate</span></span>](reporttemplate.md) <br/> |<span data-ttu-id="32466-117">Gibt den Typ des abzurufenden Überwachungsberichts an.</span><span class="sxs-lookup"><span data-stu-id="32466-117">Specifies the type of tracking report to retrieve.</span></span> <span data-ttu-id="32466-118">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="32466-118">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="32466-119">RecipientFilter</span><span class="sxs-lookup"><span data-stu-id="32466-119">RecipientFilter</span></span>](recipientfilter.md) <br/> |<span data-ttu-id="32466-120">Gibt eine Empfängeradresse an, die mit dem angegebenen Überwachungsbericht verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="32466-120">Specifies a recipient address to use with the specified tracking report.</span></span> <span data-ttu-id="32466-121">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="32466-121">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="32466-122">MessageTrackingReportId</span><span class="sxs-lookup"><span data-stu-id="32466-122">MessageTrackingReportId</span></span>](messagetrackingreportid.md) <br/> |<span data-ttu-id="32466-123">Gibt eine Identitätszeichenfolge an, die aus dem **FindMessageTrackingReport** -Vorgang abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="32466-123">Specifies an identity string that was obtained from the **FindMessageTrackingReport** operation.</span></span> <span data-ttu-id="32466-124">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="32466-124">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="32466-125">ReturnQueueEvents</span><span class="sxs-lookup"><span data-stu-id="32466-125">ReturnQueueEvents</span></span>](returnqueueevents.md) <br/> |<span data-ttu-id="32466-126">Gibt an, dass die Person, die den Vorgang ausführt, eine privilegierte Rolle besitzt.</span><span class="sxs-lookup"><span data-stu-id="32466-126">Specifies that the person who is running the task has a privileged role.</span></span> <span data-ttu-id="32466-127">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="32466-127">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="32466-128">DiagnosticsLevel</span><span class="sxs-lookup"><span data-stu-id="32466-128">DiagnosticsLevel</span></span>](diagnosticslevel.md) <br/> |<span data-ttu-id="32466-129">Gibt Timing-und Leistungsinformationen an, die zum Ableiten des Überwachungsberichts verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="32466-129">Specifies timing and performance information that will be used to derive the tracking report.</span></span> <span data-ttu-id="32466-130">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="32466-130">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="32466-131">Eigenschaften (ArrayOfTrackingPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="32466-131">Properties (ArrayOfTrackingPropertiesType)</span></span>](properties-arrayoftrackingpropertiestype.md) <br/> |<span data-ttu-id="32466-132">Gibt eine Liste mit einer oder mehreren Überwachungseigenschaften an.</span><span class="sxs-lookup"><span data-stu-id="32466-132">Specifies a list of one or more tracking properties.</span></span> <span data-ttu-id="32466-133">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="32466-133">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="32466-134">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="32466-134">Parent elements</span></span>

<span data-ttu-id="32466-135">Keine.</span><span class="sxs-lookup"><span data-stu-id="32466-135">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="32466-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="32466-136">Remarks</span></span>

<span data-ttu-id="32466-137">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="32466-137">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="32466-138">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="32466-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="32466-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="32466-139">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="32466-140">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="32466-140">Schema Name</span></span>  <br/> |<span data-ttu-id="32466-141">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="32466-141">Messages schema</span></span>  <br/> |
|<span data-ttu-id="32466-142">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="32466-142">Validation File</span></span>  <br/> |<span data-ttu-id="32466-143">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="32466-143">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="32466-144">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="32466-144">Can be Empty</span></span>  <br/> |<span data-ttu-id="32466-145">False</span><span class="sxs-lookup"><span data-stu-id="32466-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="32466-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="32466-146">See also</span></span>



[<span data-ttu-id="32466-147">GetMessageTrackingReport-Vorgang</span><span class="sxs-lookup"><span data-stu-id="32466-147">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="32466-148">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="32466-148">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

