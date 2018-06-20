---
title: Vorkommen
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Occurrence
api_type:
- schema
ms.assetid: d292b99c-b896-40b7-be5d-2cb314c9481f
description: Das Vorkommen-Element repräsentiert ein geändertes Auftreten eines sich wiederholenden Kalenderelements.
ms.openlocfilehash: 5a40faa9b885a235d30e7f41830d1eefe2ed23c3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830653"
---
# <a name="occurrence"></a><span data-ttu-id="7c9cc-103">Vorkommen</span><span class="sxs-lookup"><span data-stu-id="7c9cc-103">Occurrence</span></span>

<span data-ttu-id="7c9cc-104">Das **Vorkommen** -Element repräsentiert ein geändertes Auftreten eines sich wiederholenden Kalenderelements.</span><span class="sxs-lookup"><span data-stu-id="7c9cc-104">The **Occurrence** element represents a single modified occurrence of a recurring calendar item.</span></span> 
  
```xml
<Occurrence>
   <ItemId/>
   <Start/>
   <End/>
   <OriginalStart/>
</Occurrence>
```

<span data-ttu-id="7c9cc-105">**OccurrenceInfoType**</span><span class="sxs-lookup"><span data-stu-id="7c9cc-105">**OccurrenceInfoType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="7c9cc-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="7c9cc-106">Attributes and elements</span></span>

<span data-ttu-id="7c9cc-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="7c9cc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7c9cc-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="7c9cc-108">Attributes</span></span>

<span data-ttu-id="7c9cc-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="7c9cc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7c9cc-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7c9cc-110">Child elements</span></span>

|<span data-ttu-id="7c9cc-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="7c9cc-111">**Element**</span></span>|<span data-ttu-id="7c9cc-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7c9cc-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7c9cc-113">ItemId</span><span class="sxs-lookup"><span data-stu-id="7c9cc-113">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="7c9cc-114">Enthält den eindeutigen Schlüssel-ID und ein Änderungsprotokoll für ein geänderte Auftreten eines sich wiederholenden Kalenderelements an.</span><span class="sxs-lookup"><span data-stu-id="7c9cc-114">Contains the unique identifier and change key of a modified occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="7c9cc-115">Start</span><span class="sxs-lookup"><span data-stu-id="7c9cc-115">Start</span></span>](start.md) <br/> |<span data-ttu-id="7c9cc-116">Die Anfangszeit der eine geänderte Vorkommen eines sich wiederholenden Kalenderelements darstellt.</span><span class="sxs-lookup"><span data-stu-id="7c9cc-116">Represents the start time of a modified occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="7c9cc-117">Ende</span><span class="sxs-lookup"><span data-stu-id="7c9cc-117">End </span></span>](end-ex15websvcsotherref.md) <br/> |<span data-ttu-id="7c9cc-118">Die Endzeit der eine geänderte Vorkommen eines sich wiederholenden Kalenderelements darstellt.</span><span class="sxs-lookup"><span data-stu-id="7c9cc-118">Represents the end time of a modified occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="7c9cc-119">OriginalStart</span><span class="sxs-lookup"><span data-stu-id="7c9cc-119">OriginalStart</span></span>](originalstart.md) <br/> |<span data-ttu-id="7c9cc-120">Stellt die ursprünglichen Anfangszeit der eine geänderte Vorkommen eines sich wiederholenden Kalenderelements an.</span><span class="sxs-lookup"><span data-stu-id="7c9cc-120">Represents the original start time of a modified occurrence of a recurring calendar item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7c9cc-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7c9cc-121">Parent elements</span></span>

|<span data-ttu-id="7c9cc-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="7c9cc-122">**Element**</span></span>|<span data-ttu-id="7c9cc-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7c9cc-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7c9cc-124">ModifiedOccurrences</span><span class="sxs-lookup"><span data-stu-id="7c9cc-124">ModifiedOccurrences</span></span>](modifiedoccurrences.md) <br/> |<span data-ttu-id="7c9cc-125">Enthält eine Auflistung von sich wiederholenden Kalender Element vorkommen, die geändert wurden, damit diese als das Master-Shape Recurrence-Element unterschiedlich sind.</span><span class="sxs-lookup"><span data-stu-id="7c9cc-125">Contains a collection of recurring calendar item occurrences that have been modified so that they are different than the recurrence master item.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7c9cc-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7c9cc-126">Remarks</span></span>

<span data-ttu-id="7c9cc-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="7c9cc-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7c9cc-128">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="7c9cc-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7c9cc-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="7c9cc-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7c9cc-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="7c9cc-130">Schema name</span></span>  <br/> |<span data-ttu-id="7c9cc-131">Schematypen</span><span class="sxs-lookup"><span data-stu-id="7c9cc-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="7c9cc-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="7c9cc-132">Validation file</span></span>  <br/> |<span data-ttu-id="7c9cc-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7c9cc-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7c9cc-134">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="7c9cc-134">Can be empty</span></span>  <br/> |<span data-ttu-id="7c9cc-135">False</span><span class="sxs-lookup"><span data-stu-id="7c9cc-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7c9cc-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7c9cc-136">See also</span></span>

- [<span data-ttu-id="7c9cc-137">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="7c9cc-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

