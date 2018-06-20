---
title: NoEndRecurrence
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- NoEndRecurrence
api_type:
- schema
ms.assetid: ab2ebd9c-388e-45f1-abf9-56e293ef123b
description: Das NoEndRecurrence-Element beschreibt das Startdatum des ein Element Serienmuster, die nicht über einen definierten Enddatum verfügt.
ms.openlocfilehash: fc3eae170f5c07e31d7a80b45836efd07d74e543
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830537"
---
# <a name="noendrecurrence"></a><span data-ttu-id="7a3ae-103">NoEndRecurrence</span><span class="sxs-lookup"><span data-stu-id="7a3ae-103">NoEndRecurrence</span></span>

<span data-ttu-id="7a3ae-104">Das **NoEndRecurrence** -Element beschreibt das Startdatum des ein Element Serienmuster, die nicht über einen definierten Enddatum verfügt.</span><span class="sxs-lookup"><span data-stu-id="7a3ae-104">The **NoEndRecurrence** element describes the start date of an item recurrence pattern that does not have a defined end date.</span></span> 
  
```xml
<NoEndRecurrence>
   <StartDate/>
</NoEndRecurrence>
```

 <span data-ttu-id="7a3ae-105">**NoEndRecurrenceRangeType**</span><span class="sxs-lookup"><span data-stu-id="7a3ae-105">**NoEndRecurrenceRangeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7a3ae-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="7a3ae-106">Attributes and elements</span></span>

<span data-ttu-id="7a3ae-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="7a3ae-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7a3ae-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="7a3ae-108">Attributes</span></span>

<span data-ttu-id="7a3ae-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="7a3ae-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7a3ae-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7a3ae-110">Child elements</span></span>

|<span data-ttu-id="7a3ae-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="7a3ae-111">**Element**</span></span>|<span data-ttu-id="7a3ae-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7a3ae-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7a3ae-113">StartDate (Serie)</span><span class="sxs-lookup"><span data-stu-id="7a3ae-113">StartDate (Recurrence)</span></span>](startdate-recurrence.md) <br/> |<span data-ttu-id="7a3ae-114">Stellt das Startdatum einer Aufgabenserie oder Kalenderelement.</span><span class="sxs-lookup"><span data-stu-id="7a3ae-114">Represents the start date of a recurring task or calendar item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7a3ae-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7a3ae-115">Parent elements</span></span>

|<span data-ttu-id="7a3ae-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="7a3ae-116">**Element**</span></span>|<span data-ttu-id="7a3ae-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7a3ae-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7a3ae-118">Serie (RecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="7a3ae-118">Recurrence (RecurrenceType)</span></span>](recurrence-recurrencetype.md) <br/> |<span data-ttu-id="7a3ae-119">Das Serienmuster für Kalenderelemente und Besprechungsanfragen enthält.</span><span class="sxs-lookup"><span data-stu-id="7a3ae-119">Contains the recurrence pattern for calendar items and meeting requests.</span></span>  <br/> |
|[<span data-ttu-id="7a3ae-120">Serie (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="7a3ae-120">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="7a3ae-121">Serieninformationen für wiederkehrende Aufgaben enthält.</span><span class="sxs-lookup"><span data-stu-id="7a3ae-121">Contains recurrence information for recurring tasks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7a3ae-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7a3ae-122">Remarks</span></span>

<span data-ttu-id="7a3ae-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="7a3ae-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7a3ae-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="7a3ae-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7a3ae-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="7a3ae-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7a3ae-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="7a3ae-126">Schema name</span></span>  <br/> |<span data-ttu-id="7a3ae-127">Schematypen</span><span class="sxs-lookup"><span data-stu-id="7a3ae-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="7a3ae-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="7a3ae-128">Validation file</span></span>  <br/> |<span data-ttu-id="7a3ae-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7a3ae-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7a3ae-130">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="7a3ae-130">Can be empty</span></span>  <br/> |<span data-ttu-id="7a3ae-131">False</span><span class="sxs-lookup"><span data-stu-id="7a3ae-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7a3ae-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a3ae-132">See also</span></span>



- [<span data-ttu-id="7a3ae-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="7a3ae-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

