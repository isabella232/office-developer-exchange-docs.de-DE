---
title: EndDate (Serie)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- EndDate
api_type:
- schema
ms.assetid: 16026595-26f8-4770-8a6d-0d3e4157effd
description: Das EndDate-Element darstellt, das Enddatum des einen sich wiederholenden Vorgang oder ein Kalenderelement, das den Mustertyp EndDateRecurrence verfügt.
ms.openlocfilehash: b8570a069fc0a2d05044a9c85ab2d5c39d70ccdf
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758221"
---
# <a name="enddate-recurrence"></a><span data-ttu-id="4d075-103">EndDate (Serie)</span><span class="sxs-lookup"><span data-stu-id="4d075-103">EndDate (Recurrence)</span></span>

<span data-ttu-id="4d075-104">Das **EndDate** -Element darstellt, das Enddatum des einen sich wiederholenden Vorgang oder ein Kalenderelement, das den Mustertyp EndDateRecurrence verfügt.</span><span class="sxs-lookup"><span data-stu-id="4d075-104">The **EndDate** element represents the end date of a recurring task or a calendar item that has the EndDateRecurrence pattern type.</span></span> 
  
```xml
<EndDate/>
```

 <span data-ttu-id="4d075-105">**date**</span><span class="sxs-lookup"><span data-stu-id="4d075-105">**date**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4d075-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="4d075-106">Attributes and elements</span></span>

<span data-ttu-id="4d075-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="4d075-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4d075-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="4d075-108">Attributes</span></span>

<span data-ttu-id="4d075-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="4d075-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4d075-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4d075-110">Child elements</span></span>

<span data-ttu-id="4d075-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="4d075-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4d075-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4d075-112">Parent elements</span></span>

|<span data-ttu-id="4d075-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="4d075-113">**Element**</span></span>|<span data-ttu-id="4d075-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4d075-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4d075-115">EndDateRecurrence</span><span class="sxs-lookup"><span data-stu-id="4d075-115">EndDateRecurrence</span></span>](enddaterecurrence.md) <br/> |<span data-ttu-id="4d075-116">Beschreibt das Startdatum und das Enddatum des ein Element Serienmuster.</span><span class="sxs-lookup"><span data-stu-id="4d075-116">Describes the start date and the end date of an item recurrence pattern.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4d075-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="4d075-117">Text value</span></span>

<span data-ttu-id="4d075-118">Ein Textwert, der ein Datum darstellt ist erforderlich, wenn dieses Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4d075-118">A text value that represents a date is required if this element is used.</span></span> <span data-ttu-id="4d075-119">Der Wert darf nicht größer als 1 September 4500 00:00:00.</span><span class="sxs-lookup"><span data-stu-id="4d075-119">The value cannot be larger than September 1, 4500 00:00:00.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4d075-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4d075-120">Remarks</span></span>

<span data-ttu-id="4d075-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="4d075-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4d075-122">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="4d075-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4d075-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="4d075-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4d075-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="4d075-124">Schema name</span></span>  <br/> |<span data-ttu-id="4d075-125">Schematypen</span><span class="sxs-lookup"><span data-stu-id="4d075-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="4d075-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="4d075-126">Validation file</span></span>  <br/> |<span data-ttu-id="4d075-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4d075-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4d075-128">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="4d075-128">Can be empty</span></span>  <br/> |<span data-ttu-id="4d075-129">False</span><span class="sxs-lookup"><span data-stu-id="4d075-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4d075-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4d075-130">See also</span></span>



- [<span data-ttu-id="4d075-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="4d075-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

