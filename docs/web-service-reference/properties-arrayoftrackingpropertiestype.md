---
title: Eigenschaften (ArrayOfTrackingPropertiesType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Properties
api_type:
- schema
ms.assetid: 175566d2-fd62-45a2-8518-2827912cec88
description: Das Properties-Element enthält eine Liste der Eigenschaften für eine oder mehrere Tracking.
ms.openlocfilehash: 079d2d2c101fdeb7f26d65798048c3c6c59f3e94
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830897"
---
# <a name="properties-arrayoftrackingpropertiestype"></a><span data-ttu-id="a26dd-103">Eigenschaften (ArrayOfTrackingPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="a26dd-103">Properties (ArrayOfTrackingPropertiesType)</span></span>

<span data-ttu-id="a26dd-104">Das **Properties** -Element enthält eine Liste der Eigenschaften für eine oder mehrere Tracking.</span><span class="sxs-lookup"><span data-stu-id="a26dd-104">The **Properties** element contains a list of one or more tracking properties.</span></span> 
  
- [<span data-ttu-id="a26dd-105">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="a26dd-105">FindMessageTrackingReport</span></span>](findmessagetrackingreport.md)
  
- [<span data-ttu-id="a26dd-106">Eigenschaften (ArrayOfTrackingPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="a26dd-106">Properties (ArrayOfTrackingPropertiesType)</span></span>](properties-arrayoftrackingpropertiestype.md)
  
```xml
<Properties>
   <TrackingPropertyType/>
</Properties>
```

<span data-ttu-id="a26dd-107">**ArrayOfTrackingPropertiesType**</span><span class="sxs-lookup"><span data-stu-id="a26dd-107">**ArrayOfTrackingPropertiesType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="a26dd-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a26dd-108">Attributes and elements</span></span>

<span data-ttu-id="a26dd-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a26dd-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a26dd-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="a26dd-110">Attributes</span></span>

<span data-ttu-id="a26dd-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="a26dd-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a26dd-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a26dd-112">Child elements</span></span>

|<span data-ttu-id="a26dd-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="a26dd-113">**Element**</span></span>|<span data-ttu-id="a26dd-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a26dd-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a26dd-115">TrackingPropertyType</span><span class="sxs-lookup"><span data-stu-id="a26dd-115">TrackingPropertyType</span></span>](trackingpropertytype.md) <br/> |<span data-ttu-id="a26dd-116">Stellt ein Name-Wert-Paar von Zeichenfolgen, die zum Erstellen von Eigenschaften für nachrichtenverfolgungsberichte verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a26dd-116">Represents a name and value pair of strings that is used to create properties for message tracking reports.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a26dd-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a26dd-117">Parent elements</span></span>

|<span data-ttu-id="a26dd-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="a26dd-118">**Element**</span></span>|<span data-ttu-id="a26dd-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a26dd-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a26dd-120">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="a26dd-120">FindMessageTrackingReport</span></span>](findmessagetrackingreport.md) <br/> |<span data-ttu-id="a26dd-121">Gibt Kriterien für die Typen von Nachrichten suchen.</span><span class="sxs-lookup"><span data-stu-id="a26dd-121">Specifies criteria for the types of messages to find.</span></span>  <br/> |
|[<span data-ttu-id="a26dd-122">FindMessageTrackingReportResponse</span><span class="sxs-lookup"><span data-stu-id="a26dd-122">FindMessageTrackingReportResponse</span></span>](findmessagetrackingreportresponse.md) <br/> |<span data-ttu-id="a26dd-123">Enthält den Status und das Ergebnis einer einzelnen Anforderung [FindMessageTrackingReport Vorgang](findmessagetrackingreport-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="a26dd-123">Contains the status and result of a single [FindMessageTrackingReport operation](findmessagetrackingreport-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="a26dd-124">GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="a26dd-124">GetMessageTrackingReport</span></span>](getmessagetrackingreport.md) <br/> |<span data-ttu-id="a26dd-125">Enthält die Anforderung für den [GetMessageTrackingReport Vorgang](getmessagetrackingreport-operation.md) zum Abrufen der vollständigen Nachricht Nachverfolgen der Bericht für den angegebenen ID.</span><span class="sxs-lookup"><span data-stu-id="a26dd-125">Contains the request for the [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md) to retrieve the full message tracking report for the specified ID.</span></span>  <br/> |
|[<span data-ttu-id="a26dd-126">GetMessageTrackingReportResponse</span><span class="sxs-lookup"><span data-stu-id="a26dd-126">GetMessageTrackingReportResponse</span></span>](getmessagetrackingreportresponse.md) <br/> |<span data-ttu-id="a26dd-127">Enthält das Ergebnis einer einzelnen Anforderung [GetMessageTrackingReport Vorgang](getmessagetrackingreport-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="a26dd-127">Contains the result of a single [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="a26dd-128">RecipientTrackingEvent</span><span class="sxs-lookup"><span data-stu-id="a26dd-128">RecipientTrackingEvent</span></span>](recipienttrackingevent.md) <br/> |<span data-ttu-id="a26dd-129">Enthält Informationen für ein einzelnes Ereignis für einen Empfänger.</span><span class="sxs-lookup"><span data-stu-id="a26dd-129">Contains information for a single event for a recipient.</span></span>  <br/> |
|[<span data-ttu-id="a26dd-130">MessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="a26dd-130">MessageTrackingReport</span></span>](messagetrackingreport.md) <br/> |<span data-ttu-id="a26dd-131">Enthält eine Nachricht, die in einem [GetMessageTrackingReport-Vorgang](getmessagetrackingreport-operation.md)zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a26dd-131">Contains a single message that is returned in a [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="a26dd-132">MessageTrackingSearchResult</span><span class="sxs-lookup"><span data-stu-id="a26dd-132">MessageTrackingSearchResult</span></span>](messagetrackingsearchresult.md) <br/> |<span data-ttu-id="a26dd-133">Ein einzelnes Nachricht Ergebnis für ein [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) -Element enthält.</span><span class="sxs-lookup"><span data-stu-id="a26dd-133">Contains a single message result for a [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) element.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a26dd-134">Textwert</span><span class="sxs-lookup"><span data-stu-id="a26dd-134">Text value</span></span>

<span data-ttu-id="a26dd-135">Keine.</span><span class="sxs-lookup"><span data-stu-id="a26dd-135">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a26dd-136">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a26dd-136">Remarks</span></span>

<span data-ttu-id="a26dd-137">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="a26dd-137">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a26dd-138">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="a26dd-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a26dd-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="a26dd-139">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a26dd-140">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a26dd-140">Schema Name</span></span>  <br/> |<span data-ttu-id="a26dd-141">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="a26dd-141">Messages schema</span></span>  <br/> |
|<span data-ttu-id="a26dd-142">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a26dd-142">Validation File</span></span>  <br/> |<span data-ttu-id="a26dd-143">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="a26dd-143">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a26dd-144">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="a26dd-144">Can be Empty</span></span>  <br/> |<span data-ttu-id="a26dd-145">False</span><span class="sxs-lookup"><span data-stu-id="a26dd-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a26dd-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a26dd-146">See also</span></span>

- [<span data-ttu-id="a26dd-147">FindMessageTrackingReport-Vorgang</span><span class="sxs-lookup"><span data-stu-id="a26dd-147">FindMessageTrackingReport operation</span></span>](findmessagetrackingreport-operation.md)
- [<span data-ttu-id="a26dd-148">GetMessageTrackingReport-Vorgang</span><span class="sxs-lookup"><span data-stu-id="a26dd-148">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)
- [<span data-ttu-id="a26dd-149">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="a26dd-149">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

