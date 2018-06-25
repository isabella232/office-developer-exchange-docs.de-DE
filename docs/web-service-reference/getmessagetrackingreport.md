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
description: Das GetMessageTrackingReport-Element enthält die Anforderung für den Vorgang GetMessageTrackingReport zum Abrufen der vollständigen Nachricht Nachverfolgen der Bericht für den angegebenen ID.
ms.openlocfilehash: cb16f6e9d322cefb0d59c962af8e2f60ebae0e90
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758738"
---
# <a name="getmessagetrackingreport"></a><span data-ttu-id="0c467-103">GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="0c467-103">GetMessageTrackingReport</span></span>

<span data-ttu-id="0c467-104">Das **GetMessageTrackingReport** -Element enthält die Anforderung für den [GetMessageTrackingReport Vorgang](getmessagetrackingreport-operation.md) zum Abrufen der vollständigen Nachricht Nachverfolgen der Bericht für den angegebenen ID.</span><span class="sxs-lookup"><span data-stu-id="0c467-104">The **GetMessageTrackingReport** element contains the request for the [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md) to retrieve the full message tracking report for the specified ID.</span></span> 
  
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

 <span data-ttu-id="0c467-105">**GetMessageTrackingReportRequestType**</span><span class="sxs-lookup"><span data-stu-id="0c467-105">**GetMessageTrackingReportRequestType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0c467-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="0c467-106">Attributes and elements</span></span>

<span data-ttu-id="0c467-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="0c467-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0c467-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="0c467-108">Attributes</span></span>

<span data-ttu-id="0c467-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="0c467-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0c467-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0c467-110">Child elements</span></span>

|<span data-ttu-id="0c467-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="0c467-111">**Element**</span></span>|<span data-ttu-id="0c467-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0c467-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0c467-113">Bereich (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="0c467-113">Scope (NonEmptyStringType)</span></span>](scope-nonemptystringtype.md) <br/> |<span data-ttu-id="0c467-114">Gibt an, wo die Suche durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="0c467-114">Specifies where to perform the search.</span></span> <span data-ttu-id="0c467-115">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0c467-115">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="0c467-116">Berichtsvorlage</span><span class="sxs-lookup"><span data-stu-id="0c467-116">ReportTemplate</span></span>](reporttemplate.md) <br/> |<span data-ttu-id="0c467-117">Gibt den Typ der laufenden Bericht abgerufen.</span><span class="sxs-lookup"><span data-stu-id="0c467-117">Specifies the type of tracking report to retrieve.</span></span> <span data-ttu-id="0c467-118">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0c467-118">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="0c467-119">RecipientFilter</span><span class="sxs-lookup"><span data-stu-id="0c467-119">RecipientFilter</span></span>](recipientfilter.md) <br/> |<span data-ttu-id="0c467-120">Gibt eine Empfängeradresse mit den angegebenen Nachrichtenverfolgungsbericht verwenden.</span><span class="sxs-lookup"><span data-stu-id="0c467-120">Specifies a recipient address to use with the specified tracking report.</span></span> <span data-ttu-id="0c467-121">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="0c467-121">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="0c467-122">MessageTrackingReportId</span><span class="sxs-lookup"><span data-stu-id="0c467-122">MessageTrackingReportId</span></span>](messagetrackingreportid.md) <br/> |<span data-ttu-id="0c467-123">Gibt eine Identitätszeichenfolge, die aus der **FindMessageTrackingReport** -Operation abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="0c467-123">Specifies an identity string that was obtained from the **FindMessageTrackingReport** operation.</span></span> <span data-ttu-id="0c467-124">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0c467-124">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="0c467-125">ReturnQueueEvents</span><span class="sxs-lookup"><span data-stu-id="0c467-125">ReturnQueueEvents</span></span>](returnqueueevents.md) <br/> |<span data-ttu-id="0c467-126">Gibt an, dass die Person, die die Aufgabe ausgeführt wird, eine privilegierte Rolle wurde.</span><span class="sxs-lookup"><span data-stu-id="0c467-126">Specifies that the person who is running the task has a privileged role.</span></span> <span data-ttu-id="0c467-127">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="0c467-127">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="0c467-128">DiagnosticsLevel</span><span class="sxs-lookup"><span data-stu-id="0c467-128">DiagnosticsLevel</span></span>](diagnosticslevel.md) <br/> |<span data-ttu-id="0c467-129">Gibt die Timing und Leistungsinformationen, die verwendet wird, um den Nachrichtenverfolgungsbericht abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="0c467-129">Specifies timing and performance information that will be used to derive the tracking report.</span></span> <span data-ttu-id="0c467-130">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="0c467-130">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="0c467-131">Eigenschaften (ArrayOfTrackingPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="0c467-131">Properties (ArrayOfTrackingPropertiesType)</span></span>](properties-arrayoftrackingpropertiestype.md) <br/> |<span data-ttu-id="0c467-132">Gibt eine Liste der Eigenschaften für eine oder mehrere Tracking an.</span><span class="sxs-lookup"><span data-stu-id="0c467-132">Specifies a list of one or more tracking properties.</span></span> <span data-ttu-id="0c467-133">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="0c467-133">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0c467-134">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0c467-134">Parent elements</span></span>

<span data-ttu-id="0c467-135">Keine.</span><span class="sxs-lookup"><span data-stu-id="0c467-135">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0c467-136">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0c467-136">Remarks</span></span>

<span data-ttu-id="0c467-137">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="0c467-137">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0c467-138">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="0c467-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0c467-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="0c467-139">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0c467-140">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="0c467-140">Schema Name</span></span>  <br/> |<span data-ttu-id="0c467-141">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="0c467-141">Messages schema</span></span>  <br/> |
|<span data-ttu-id="0c467-142">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="0c467-142">Validation File</span></span>  <br/> |<span data-ttu-id="0c467-143">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="0c467-143">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0c467-144">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="0c467-144">Can be Empty</span></span>  <br/> |<span data-ttu-id="0c467-145">False</span><span class="sxs-lookup"><span data-stu-id="0c467-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0c467-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0c467-146">See also</span></span>



[<span data-ttu-id="0c467-147">GetMessageTrackingReport-Vorgang</span><span class="sxs-lookup"><span data-stu-id="0c467-147">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="0c467-148">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="0c467-148">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

