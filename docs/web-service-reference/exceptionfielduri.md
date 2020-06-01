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
ms.openlocfilehash: a47d44098f85d8bacb1e7a2c48a33e478e56c7ac
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44454344"
---
# <a name="exceptionfielduri"></a><span data-ttu-id="66735-104">ExceptionFieldURI</span><span class="sxs-lookup"><span data-stu-id="66735-104">ExceptionFieldURI</span></span>

<span data-ttu-id="66735-p102">Das **ExceptionFieldURI** -Element identifiziert bestimmte Fehlern in einer Anforderung. Dieses Element ist nur im Rahmen einer Fehlerantwort im Knoten [MessageXml](messagexml.md) verwendet.</span><span class="sxs-lookup"><span data-stu-id="66735-p102">The **ExceptionFieldURI** element identifies particular errors in a request. This element is only used as part of an error response in the [MessageXml](messagexml.md) node.</span></span> 
  
```xml
<ExceptionFieldURI FieldURI="" />
```

 <span data-ttu-id="66735-107">**ExceptionPropertyURIType**</span><span class="sxs-lookup"><span data-stu-id="66735-107">**ExceptionPropertyURIType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="66735-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="66735-108">Attributes and elements</span></span>

<span data-ttu-id="66735-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="66735-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="66735-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="66735-110">Attributes</span></span>

|<span data-ttu-id="66735-111">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="66735-111">**Attribute**</span></span>|<span data-ttu-id="66735-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="66735-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="66735-113">**FieldURI**</span><span class="sxs-lookup"><span data-stu-id="66735-113">**FieldURI**</span></span> <br/> |<span data-ttu-id="66735-p103">Identifiziert eine Eigenschaft für das Vorkommen einer Terminserie. Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="66735-p103">Identifies a property of an occurrence of a recurring item. This attribute is required.</span></span>  <br/> |
   
#### <a name="fielduri-attribute"></a><span data-ttu-id="66735-116">FieldURI Attribute</span><span class="sxs-lookup"><span data-stu-id="66735-116">FieldURI Attribute</span></span>

|<span data-ttu-id="66735-117">**Wert**</span><span class="sxs-lookup"><span data-stu-id="66735-117">**Value**</span></span>|<span data-ttu-id="66735-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="66735-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="66735-119">Name der Anlage:</span><span class="sxs-lookup"><span data-stu-id="66735-119">attachment:Name</span></span>  <br/> |<span data-ttu-id="66735-120">Gibt den Anlagennamen enthält einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="66735-120">Identifies the attachment name as containing an error.</span></span>  <br/> |
|<span data-ttu-id="66735-121">Anlage: ContentType</span><span class="sxs-lookup"><span data-stu-id="66735-121">attachment:ContentType</span></span>  <br/> |<span data-ttu-id="66735-122">Identifiziert den Inhaltstyp enthält einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="66735-122">Identifies the content type as containing an error.</span></span>  <br/> |
|<span data-ttu-id="66735-123">Anlageninhalt:</span><span class="sxs-lookup"><span data-stu-id="66735-123">attachment:Content</span></span>  <br/> |<span data-ttu-id="66735-124">Identifiziert den Inhalt, der einen Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="66735-124">Identifies the content as containing an error.</span></span>  <br/> |
|<span data-ttu-id="66735-125">Serie Monat:</span><span class="sxs-lookup"><span data-stu-id="66735-125">recurrence:Month</span></span>  <br/> |<span data-ttu-id="66735-126">Gibt das Feld Monat enthält einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="66735-126">Identifies the month field as containing an error.</span></span>  <br/> |
|<span data-ttu-id="66735-127">Serie: DayOfWeekIndex</span><span class="sxs-lookup"><span data-stu-id="66735-127">recurrence:DayOfWeekIndex</span></span>  <br/> |<span data-ttu-id="66735-128">Identifiziert den Tag der Wochentagindex enthält einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="66735-128">Identifies the day of week index as containing an error.</span></span>  <br/> |
|<span data-ttu-id="66735-129">Serie: DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="66735-129">recurrence:DaysOfWeek</span></span>  <br/> |<span data-ttu-id="66735-130">Bezeichnet die DaysOfWeek-Eigenschaft enthält einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="66735-130">Identifies the DaysOfWeek property as containing an error.</span></span>  <br/> |
|<span data-ttu-id="66735-131">Serie: DAYOFMONTH</span><span class="sxs-lookup"><span data-stu-id="66735-131">recurrence:DayOfMonth</span></span>  <br/> |<span data-ttu-id="66735-132">Identifiziert die DayOfMonth enthält einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="66735-132">Identifies the DayOfMonth as containing an error.</span></span>  <br/> |
|<span data-ttu-id="66735-133">Wiederholungsintervall:</span><span class="sxs-lookup"><span data-stu-id="66735-133">recurrence:Interval</span></span>  <br/> |<span data-ttu-id="66735-134">Gibt das Intervall enthält einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="66735-134">Identifies the interval as containing an error.</span></span>  <br/> |
|<span data-ttu-id="66735-135">Serie: NumberOfOccurrences</span><span class="sxs-lookup"><span data-stu-id="66735-135">recurrence:NumberOfOccurrences</span></span>  <br/> |<span data-ttu-id="66735-136">Feststellen der Anzahl von vorkommen, dass Sie einen Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="66735-136">Identifies the number of occurrences as containing an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="66735-137">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="66735-137">Child elements</span></span>

<span data-ttu-id="66735-138">Keine.</span><span class="sxs-lookup"><span data-stu-id="66735-138">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="66735-139">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="66735-139">Parent elements</span></span>

|<span data-ttu-id="66735-140">**Element**</span><span class="sxs-lookup"><span data-stu-id="66735-140">**Element**</span></span>|<span data-ttu-id="66735-141">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="66735-141">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="66735-142">Messagexml verwendet</span><span class="sxs-lookup"><span data-stu-id="66735-142">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="66735-143">Bietet zusätzliche Fehlerantwortinformationen.</span><span class="sxs-lookup"><span data-stu-id="66735-143">Provides additional error response information.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="66735-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="66735-144">Remarks</span></span>

<span data-ttu-id="66735-145">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="66735-145">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="66735-146">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="66735-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="66735-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="66735-147">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="66735-148">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="66735-148">Schema Name</span></span>  <br/> |<span data-ttu-id="66735-149">Schematypen</span><span class="sxs-lookup"><span data-stu-id="66735-149">Types schema</span></span>  <br/> |
|<span data-ttu-id="66735-150">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="66735-150">Validation File</span></span>  <br/> |<span data-ttu-id="66735-151">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="66735-151">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="66735-152">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="66735-152">Can be Empty</span></span>  <br/> |<span data-ttu-id="66735-153">False</span><span class="sxs-lookup"><span data-stu-id="66735-153">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="66735-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="66735-154">See also</span></span>



- [<span data-ttu-id="66735-155">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="66735-155">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

