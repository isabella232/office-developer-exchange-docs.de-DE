---
title: ExceptionFieldURI
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ExceptionFieldURI
api_type:
- schema
ms.assetid: 7afda93a-0f8c-4c9e-8e09-f1b0bfc928bf
description: Das ExceptionFieldURI -Element identifiziert bestimmte Fehlern in einer Anforderung. Dieses Element ist nur im Rahmen einer Fehlerantwort im Knoten MessageXml verwendet.
ms.openlocfilehash: 79909405179cec0d0b86ad12bf52031e1daeb790
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758292"
---
# <a name="exceptionfielduri"></a><span data-ttu-id="eb281-104">ExceptionFieldURI</span><span class="sxs-lookup"><span data-stu-id="eb281-104">ExceptionFieldURI</span></span>

<span data-ttu-id="eb281-p102">Das **ExceptionFieldURI** -Element identifiziert bestimmte Fehlern in einer Anforderung. Dieses Element ist nur im Rahmen einer Fehlerantwort im Knoten [MessageXml](messagexml.md) verwendet.</span><span class="sxs-lookup"><span data-stu-id="eb281-p102">The **ExceptionFieldURI** element identifies particular errors in a request. This element is only used as part of an error response in the [MessageXml](messagexml.md) node.</span></span> 
  
```xml
<ExceptionFieldURI FieldURI="" />
```

 <span data-ttu-id="eb281-107">**ExceptionPropertyURIType**</span><span class="sxs-lookup"><span data-stu-id="eb281-107">**ExceptionPropertyURIType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="eb281-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="eb281-108">Attributes and elements</span></span>

<span data-ttu-id="eb281-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="eb281-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="eb281-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="eb281-110">Attributes</span></span>

|<span data-ttu-id="eb281-111">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="eb281-111">**Attribute**</span></span>|<span data-ttu-id="eb281-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="eb281-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="eb281-113">**FieldURI**</span><span class="sxs-lookup"><span data-stu-id="eb281-113">**FieldURI**</span></span> <br/> |<span data-ttu-id="eb281-p103">Identifiziert eine Eigenschaft für das Vorkommen einer Terminserie. Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="eb281-p103">Identifies a property of an occurrence of a recurring item. This attribute is required.</span></span>  <br/> |
   
#### <a name="fielduri-attribute"></a><span data-ttu-id="eb281-116">FieldURI-Attribut</span><span class="sxs-lookup"><span data-stu-id="eb281-116">FieldURI Attribute</span></span>

|<span data-ttu-id="eb281-117">**Wert**</span><span class="sxs-lookup"><span data-stu-id="eb281-117">**Value**</span></span>|<span data-ttu-id="eb281-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="eb281-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="eb281-119">Name der Anlage:</span><span class="sxs-lookup"><span data-stu-id="eb281-119">attachment:Name</span></span>  <br/> |<span data-ttu-id="eb281-120">Gibt den Anlagennamen enthält einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="eb281-120">Identifies the attachment name as containing an error.</span></span>  <br/> |
|<span data-ttu-id="eb281-121">Anhang: ContentType</span><span class="sxs-lookup"><span data-stu-id="eb281-121">attachment:ContentType</span></span>  <br/> |<span data-ttu-id="eb281-122">Identifiziert den Inhaltstyp enthält einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="eb281-122">Identifies the content type as containing an error.</span></span>  <br/> |
|<span data-ttu-id="eb281-123">Anlageninhalt:</span><span class="sxs-lookup"><span data-stu-id="eb281-123">attachment:Content</span></span>  <br/> |<span data-ttu-id="eb281-124">Identifiziert den Inhalt, der einen Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="eb281-124">Identifies the content as containing an error.</span></span>  <br/> |
|<span data-ttu-id="eb281-125">Serie Monat:</span><span class="sxs-lookup"><span data-stu-id="eb281-125">recurrence:Month</span></span>  <br/> |<span data-ttu-id="eb281-126">Gibt das Feld Monat enthält einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="eb281-126">Identifies the month field as containing an error.</span></span>  <br/> |
|<span data-ttu-id="eb281-127">Serie: DayOfWeekIndex</span><span class="sxs-lookup"><span data-stu-id="eb281-127">recurrence:DayOfWeekIndex</span></span>  <br/> |<span data-ttu-id="eb281-128">Identifiziert den Tag der Wochentagindex enthält einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="eb281-128">Identifies the day of week index as containing an error.</span></span>  <br/> |
|<span data-ttu-id="eb281-129">Serie: DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="eb281-129">recurrence:DaysOfWeek</span></span>  <br/> |<span data-ttu-id="eb281-130">Bezeichnet die DaysOfWeek-Eigenschaft enthält einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="eb281-130">Identifies the DaysOfWeek property as containing an error.</span></span>  <br/> |
|<span data-ttu-id="eb281-131">Serie: DayOfMonth</span><span class="sxs-lookup"><span data-stu-id="eb281-131">recurrence:DayOfMonth</span></span>  <br/> |<span data-ttu-id="eb281-132">Identifiziert die DayOfMonth enthält einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="eb281-132">Identifies the DayOfMonth as containing an error.</span></span>  <br/> |
|<span data-ttu-id="eb281-133">Wiederholungsintervall:</span><span class="sxs-lookup"><span data-stu-id="eb281-133">recurrence:Interval</span></span>  <br/> |<span data-ttu-id="eb281-134">Gibt das Intervall enthält einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="eb281-134">Identifies the interval as containing an error.</span></span>  <br/> |
|<span data-ttu-id="eb281-135">Serie: NumberOfOccurrences</span><span class="sxs-lookup"><span data-stu-id="eb281-135">recurrence:NumberOfOccurrences</span></span>  <br/> |<span data-ttu-id="eb281-136">Feststellen der Anzahl von vorkommen, dass Sie einen Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="eb281-136">Identifies the number of occurrences as containing an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="eb281-137">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="eb281-137">Child elements</span></span>

<span data-ttu-id="eb281-138">Keine.</span><span class="sxs-lookup"><span data-stu-id="eb281-138">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="eb281-139">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="eb281-139">Parent elements</span></span>

|<span data-ttu-id="eb281-140">**Element**</span><span class="sxs-lookup"><span data-stu-id="eb281-140">**Element**</span></span>|<span data-ttu-id="eb281-141">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="eb281-141">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="eb281-142">MessageXml</span><span class="sxs-lookup"><span data-stu-id="eb281-142">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="eb281-143">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="eb281-143">Provides additional error response information.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eb281-144">Hinweise</span><span class="sxs-lookup"><span data-stu-id="eb281-144">Remarks</span></span>

<span data-ttu-id="eb281-145">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="eb281-145">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="eb281-146">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="eb281-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="eb281-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="eb281-147">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="eb281-148">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="eb281-148">Schema Name</span></span>  <br/> |<span data-ttu-id="eb281-149">Schematypen</span><span class="sxs-lookup"><span data-stu-id="eb281-149">Types schema</span></span>  <br/> |
|<span data-ttu-id="eb281-150">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="eb281-150">Validation File</span></span>  <br/> |<span data-ttu-id="eb281-151">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="eb281-151">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="eb281-152">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="eb281-152">Can be Empty</span></span>  <br/> |<span data-ttu-id="eb281-153">False</span><span class="sxs-lookup"><span data-stu-id="eb281-153">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="eb281-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eb281-154">See also</span></span>



- [<span data-ttu-id="eb281-155">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="eb281-155">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

