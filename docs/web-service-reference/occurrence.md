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
description: Das Vorkommen-Element stellt ein einzelnes geändertes Vorkommen eines wiederkehrenden Kalenderelements dar.
ms.openlocfilehash: c3a6bcce23f0bb1125dbd2a5bb86e9b20039a4e1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466318"
---
# <a name="occurrence"></a><span data-ttu-id="a5d12-103">Vorkommen</span><span class="sxs-lookup"><span data-stu-id="a5d12-103">Occurrence</span></span>

<span data-ttu-id="a5d12-104">Das **vorkommen** -Element stellt ein einzelnes geändertes Vorkommen eines wiederkehrenden Kalenderelements dar.</span><span class="sxs-lookup"><span data-stu-id="a5d12-104">The **Occurrence** element represents a single modified occurrence of a recurring calendar item.</span></span> 
  
```xml
<Occurrence>
   <ItemId/>
   <Start/>
   <End/>
   <OriginalStart/>
</Occurrence>
```

<span data-ttu-id="a5d12-105">**OccurrenceInfoType**</span><span class="sxs-lookup"><span data-stu-id="a5d12-105">**OccurrenceInfoType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="a5d12-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a5d12-106">Attributes and elements</span></span>

<span data-ttu-id="a5d12-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a5d12-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a5d12-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="a5d12-108">Attributes</span></span>

<span data-ttu-id="a5d12-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="a5d12-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a5d12-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a5d12-110">Child elements</span></span>

|<span data-ttu-id="a5d12-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="a5d12-111">**Element**</span></span>|<span data-ttu-id="a5d12-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a5d12-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a5d12-113">ItemId</span><span class="sxs-lookup"><span data-stu-id="a5d12-113">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="a5d12-114">Enthält den eindeutigen Bezeichner und den Änderungsschlüssel eines geänderten Vorkommens eines wiederkehrenden Kalenderelements.</span><span class="sxs-lookup"><span data-stu-id="a5d12-114">Contains the unique identifier and change key of a modified occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="a5d12-115">Start</span><span class="sxs-lookup"><span data-stu-id="a5d12-115">Start</span></span>](start.md) <br/> |<span data-ttu-id="a5d12-116">Stellt die Startzeit eines geänderten Vorkommens eines wiederkehrenden Kalenderelements dar.</span><span class="sxs-lookup"><span data-stu-id="a5d12-116">Represents the start time of a modified occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="a5d12-117">End</span><span class="sxs-lookup"><span data-stu-id="a5d12-117">End </span></span>](end-ex15websvcsotherref.md) <br/> |<span data-ttu-id="a5d12-118">Stellt die Endzeit eines geänderten Vorkommens eines wiederkehrenden Kalenderelements dar.</span><span class="sxs-lookup"><span data-stu-id="a5d12-118">Represents the end time of a modified occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="a5d12-119">OriginalStart</span><span class="sxs-lookup"><span data-stu-id="a5d12-119">OriginalStart</span></span>](originalstart.md) <br/> |<span data-ttu-id="a5d12-120">Stellt die ursprüngliche Startzeit eines geänderten Vorkommens eines wiederkehrenden Kalenderelements dar.</span><span class="sxs-lookup"><span data-stu-id="a5d12-120">Represents the original start time of a modified occurrence of a recurring calendar item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a5d12-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a5d12-121">Parent elements</span></span>

|<span data-ttu-id="a5d12-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="a5d12-122">**Element**</span></span>|<span data-ttu-id="a5d12-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a5d12-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a5d12-124">ModifiedOccurrences</span><span class="sxs-lookup"><span data-stu-id="a5d12-124">ModifiedOccurrences</span></span>](modifiedoccurrences.md) <br/> |<span data-ttu-id="a5d12-125">Enthält eine Auflistung von wiederkehrenden Kalenderelement vorkommen, die geändert wurden, sodass Sie sich vom Serienmasterelement unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="a5d12-125">Contains a collection of recurring calendar item occurrences that have been modified so that they are different than the recurrence master item.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a5d12-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a5d12-126">Remarks</span></span>

<span data-ttu-id="a5d12-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="a5d12-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a5d12-128">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="a5d12-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a5d12-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="a5d12-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a5d12-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a5d12-130">Schema name</span></span>  <br/> |<span data-ttu-id="a5d12-131">Schematypen</span><span class="sxs-lookup"><span data-stu-id="a5d12-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="a5d12-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a5d12-132">Validation file</span></span>  <br/> |<span data-ttu-id="a5d12-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a5d12-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a5d12-134">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="a5d12-134">Can be empty</span></span>  <br/> |<span data-ttu-id="a5d12-135">False</span><span class="sxs-lookup"><span data-stu-id="a5d12-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a5d12-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a5d12-136">See also</span></span>

- [<span data-ttu-id="a5d12-137">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="a5d12-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

