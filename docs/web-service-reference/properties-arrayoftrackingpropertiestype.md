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
description: Das properties-Element enthält eine Liste mit einer oder mehreren Überwachungseigenschaften.
ms.openlocfilehash: 007a4dc14c84c47ea7af8ccacc554c134d563e44
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/01/2020
ms.locfileid: "44465632"
---
# <a name="properties-arrayoftrackingpropertiestype"></a><span data-ttu-id="0d47d-103">Eigenschaften (ArrayOfTrackingPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="0d47d-103">Properties (ArrayOfTrackingPropertiesType)</span></span>

<span data-ttu-id="0d47d-104">Das **Properties** -Element enthält eine Liste mit einer oder mehreren Überwachungseigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0d47d-104">The **Properties** element contains a list of one or more tracking properties.</span></span> 
  
- [<span data-ttu-id="0d47d-105">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="0d47d-105">FindMessageTrackingReport</span></span>](findmessagetrackingreport.md)
  
- [<span data-ttu-id="0d47d-106">Eigenschaften (ArrayOfTrackingPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="0d47d-106">Properties (ArrayOfTrackingPropertiesType)</span></span>](properties-arrayoftrackingpropertiestype.md)
  
```xml
<Properties>
   <TrackingPropertyType/>
</Properties>
```

<span data-ttu-id="0d47d-107">**ArrayOfTrackingPropertiesType**</span><span class="sxs-lookup"><span data-stu-id="0d47d-107">**ArrayOfTrackingPropertiesType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="0d47d-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="0d47d-108">Attributes and elements</span></span>

<span data-ttu-id="0d47d-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="0d47d-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0d47d-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="0d47d-110">Attributes</span></span>

<span data-ttu-id="0d47d-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="0d47d-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0d47d-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0d47d-112">Child elements</span></span>

|<span data-ttu-id="0d47d-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="0d47d-113">**Element**</span></span>|<span data-ttu-id="0d47d-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0d47d-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0d47d-115">TrackingPropertyType</span><span class="sxs-lookup"><span data-stu-id="0d47d-115">TrackingPropertyType</span></span>](trackingpropertytype.md) <br/> |<span data-ttu-id="0d47d-116">Stellt ein Name-Wert-Paar von Zeichenfolgen dar, das zum Erstellen von Eigenschaften für Nachrichtenverfolgungsberichte verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0d47d-116">Represents a name and value pair of strings that is used to create properties for message tracking reports.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0d47d-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0d47d-117">Parent elements</span></span>

|<span data-ttu-id="0d47d-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="0d47d-118">**Element**</span></span>|<span data-ttu-id="0d47d-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0d47d-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0d47d-120">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="0d47d-120">FindMessageTrackingReport</span></span>](findmessagetrackingreport.md) <br/> |<span data-ttu-id="0d47d-121">Gibt Kriterien für die Typen von Nachrichten an, die gesucht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0d47d-121">Specifies criteria for the types of messages to find.</span></span>  <br/> |
|[<span data-ttu-id="0d47d-122">FindMessageTrackingReportResponse</span><span class="sxs-lookup"><span data-stu-id="0d47d-122">FindMessageTrackingReportResponse</span></span>](findmessagetrackingreportresponse.md) <br/> |<span data-ttu-id="0d47d-123">Enthält den Status und das Ergebnis einer einzelnen [FindMessageTrackingReport-Vorgangs](findmessagetrackingreport-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="0d47d-123">Contains the status and result of a single [FindMessageTrackingReport operation](findmessagetrackingreport-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="0d47d-124">GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="0d47d-124">GetMessageTrackingReport</span></span>](getmessagetrackingreport.md) <br/> |<span data-ttu-id="0d47d-125">Enthält die Anforderung für den [GetMessageTrackingReport-Vorgang](getmessagetrackingreport-operation.md) zum Abrufen des vollständigen Nachrichtenverfolgungsberichts für die angegebene ID.</span><span class="sxs-lookup"><span data-stu-id="0d47d-125">Contains the request for the [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md) to retrieve the full message tracking report for the specified ID.</span></span>  <br/> |
|[<span data-ttu-id="0d47d-126">GetMessageTrackingReportResponse</span><span class="sxs-lookup"><span data-stu-id="0d47d-126">GetMessageTrackingReportResponse</span></span>](getmessagetrackingreportresponse.md) <br/> |<span data-ttu-id="0d47d-127">Enthält das Ergebnis einer einzelnen [GetMessageTrackingReport-Vorgangs](getmessagetrackingreport-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="0d47d-127">Contains the result of a single [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="0d47d-128">RecipientTrackingEvent</span><span class="sxs-lookup"><span data-stu-id="0d47d-128">RecipientTrackingEvent</span></span>](recipienttrackingevent.md) <br/> |<span data-ttu-id="0d47d-129">Enthält Informationen zu einem einzelnen Ereignis für einen Empfänger.</span><span class="sxs-lookup"><span data-stu-id="0d47d-129">Contains information for a single event for a recipient.</span></span>  <br/> |
|[<span data-ttu-id="0d47d-130">MessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="0d47d-130">MessageTrackingReport</span></span>](messagetrackingreport.md) <br/> |<span data-ttu-id="0d47d-131">Enthält eine Nachricht, die in einem [GetMessageTrackingReport-Vorgang](getmessagetrackingreport-operation.md)zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0d47d-131">Contains a single message that is returned in a [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="0d47d-132">MessageTrackingSearchResult</span><span class="sxs-lookup"><span data-stu-id="0d47d-132">MessageTrackingSearchResult</span></span>](messagetrackingsearchresult.md) <br/> |<span data-ttu-id="0d47d-133">Enthält ein einzelnes Nachrichten Ergebnis für ein [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="0d47d-133">Contains a single message result for a [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) element.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0d47d-134">Textwert</span><span class="sxs-lookup"><span data-stu-id="0d47d-134">Text value</span></span>

<span data-ttu-id="0d47d-135">Keine.</span><span class="sxs-lookup"><span data-stu-id="0d47d-135">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0d47d-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0d47d-136">Remarks</span></span>

<span data-ttu-id="0d47d-137">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0d47d-137">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0d47d-138">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="0d47d-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0d47d-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="0d47d-139">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0d47d-140">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="0d47d-140">Schema Name</span></span>  <br/> |<span data-ttu-id="0d47d-141">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="0d47d-141">Messages schema</span></span>  <br/> |
|<span data-ttu-id="0d47d-142">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="0d47d-142">Validation File</span></span>  <br/> |<span data-ttu-id="0d47d-143">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="0d47d-143">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0d47d-144">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="0d47d-144">Can be Empty</span></span>  <br/> |<span data-ttu-id="0d47d-145">False</span><span class="sxs-lookup"><span data-stu-id="0d47d-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0d47d-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0d47d-146">See also</span></span>

- [<span data-ttu-id="0d47d-147">FindMessageTrackingReport-Vorgang</span><span class="sxs-lookup"><span data-stu-id="0d47d-147">FindMessageTrackingReport operation</span></span>](findmessagetrackingreport-operation.md)
- [<span data-ttu-id="0d47d-148">GetMessageTrackingReport-Vorgang</span><span class="sxs-lookup"><span data-stu-id="0d47d-148">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)
- [<span data-ttu-id="0d47d-149">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="0d47d-149">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

