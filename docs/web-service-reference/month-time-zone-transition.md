---
title: Monat (Übergang Zeitzone)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Month
api_type:
- schema
ms.assetid: 5e6aac75-366d-43d0-8ccb-956285474662
description: Month-Element darstellt, den Monat, in dem der Übergang zur Zeitzone erfolgt.
ms.openlocfilehash: 887bd750b9cad1e28e6f7603c7b3289da8f8dc07
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830483"
---
# <a name="month-time-zone-transition"></a><span data-ttu-id="bfd8e-103">Monat (Übergang Zeitzone)</span><span class="sxs-lookup"><span data-stu-id="bfd8e-103">Month (Time Zone Transition)</span></span>

<span data-ttu-id="bfd8e-104">**Month** -Element darstellt, den Monat, in dem der Übergang zur Zeitzone erfolgt.</span><span class="sxs-lookup"><span data-stu-id="bfd8e-104">The **Month** element represents the month in which the time zone transition occurs.</span></span> 
  
```xml
<Month/>
```

 <span data-ttu-id="bfd8e-105">**int**</span><span class="sxs-lookup"><span data-stu-id="bfd8e-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bfd8e-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="bfd8e-106">Attributes and elements</span></span>

<span data-ttu-id="bfd8e-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="bfd8e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bfd8e-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="bfd8e-108">Attributes</span></span>

<span data-ttu-id="bfd8e-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="bfd8e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bfd8e-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bfd8e-110">Child elements</span></span>

<span data-ttu-id="bfd8e-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="bfd8e-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="bfd8e-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bfd8e-112">Parent elements</span></span>

|<span data-ttu-id="bfd8e-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="bfd8e-113">**Element**</span></span>|<span data-ttu-id="bfd8e-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bfd8e-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bfd8e-115">RecurringDateTransition</span><span class="sxs-lookup"><span data-stu-id="bfd8e-115">RecurringDateTransition</span></span>](recurringdatetransition.md) <br/> |<span data-ttu-id="bfd8e-116">Stellt einen Zeitzone Übergang dar, der einem bestimmten Datum pro Jahr auftritt.</span><span class="sxs-lookup"><span data-stu-id="bfd8e-116">Represents a time zone transition that occurs on a specific date each year.</span></span>  <br/> |
|[<span data-ttu-id="bfd8e-117">RecurringDayTransition</span><span class="sxs-lookup"><span data-stu-id="bfd8e-117">RecurringDayTransition</span></span>](recurringdaytransition.md) <br/> |<span data-ttu-id="bfd8e-118">Stellt einen Zeitzone Übergang dar, bei dem gleichen Tag pro Jahr auftritt.</span><span class="sxs-lookup"><span data-stu-id="bfd8e-118">Represents a time zone transition that occurs on the same day each year.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="bfd8e-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="bfd8e-119">Text value</span></span>

<span data-ttu-id="bfd8e-120">Der Textwert ist eine ganze Zahl, die den Monat darstellt, in dem der Übergang zur Zeitzone auftritt.</span><span class="sxs-lookup"><span data-stu-id="bfd8e-120">The text value is an integer that represents the month in which the time zone transition occurs.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bfd8e-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bfd8e-121">Remarks</span></span>

<span data-ttu-id="bfd8e-122">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="bfd8e-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bfd8e-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="bfd8e-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bfd8e-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="bfd8e-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="bfd8e-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="bfd8e-125">Schema Name</span></span>  <br/> |<span data-ttu-id="bfd8e-126">Schematypen</span><span class="sxs-lookup"><span data-stu-id="bfd8e-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="bfd8e-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="bfd8e-127">Validation File</span></span>  <br/> |<span data-ttu-id="bfd8e-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="bfd8e-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="bfd8e-129">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="bfd8e-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="bfd8e-130">False</span><span class="sxs-lookup"><span data-stu-id="bfd8e-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bfd8e-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bfd8e-131">See also</span></span>



- [<span data-ttu-id="bfd8e-132">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="bfd8e-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

