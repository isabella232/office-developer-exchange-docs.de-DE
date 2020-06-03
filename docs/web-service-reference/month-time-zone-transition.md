---
title: Month (Zeitzonenübergang)
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
description: Das Month-Element stellt den Monat dar, in dem der Zeitzonenübergang erfolgt.
ms.openlocfilehash: 1fa32ea355cc3fe826f9c34b2fd147a0d8201673
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467739"
---
# <a name="month-time-zone-transition"></a><span data-ttu-id="c533a-103">Month (Zeitzonenübergang)</span><span class="sxs-lookup"><span data-stu-id="c533a-103">Month (Time Zone Transition)</span></span>

<span data-ttu-id="c533a-104">Das **Month** -Element stellt den Monat dar, in dem der Zeitzonenübergang erfolgt.</span><span class="sxs-lookup"><span data-stu-id="c533a-104">The **Month** element represents the month in which the time zone transition occurs.</span></span> 
  
```xml
<Month/>
```

 <span data-ttu-id="c533a-105">**int**</span><span class="sxs-lookup"><span data-stu-id="c533a-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c533a-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c533a-106">Attributes and elements</span></span>

<span data-ttu-id="c533a-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c533a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c533a-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="c533a-108">Attributes</span></span>

<span data-ttu-id="c533a-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="c533a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c533a-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c533a-110">Child elements</span></span>

<span data-ttu-id="c533a-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="c533a-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c533a-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c533a-112">Parent elements</span></span>

|<span data-ttu-id="c533a-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="c533a-113">**Element**</span></span>|<span data-ttu-id="c533a-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c533a-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c533a-115">RecurringDateTransition</span><span class="sxs-lookup"><span data-stu-id="c533a-115">RecurringDateTransition</span></span>](recurringdatetransition.md) <br/> |<span data-ttu-id="c533a-116">Stellt einen Zeitzonenübergang dar, der jedes Jahr an einem bestimmten Datum auftritt.</span><span class="sxs-lookup"><span data-stu-id="c533a-116">Represents a time zone transition that occurs on a specific date each year.</span></span>  <br/> |
|[<span data-ttu-id="c533a-117">RecurringDayTransition</span><span class="sxs-lookup"><span data-stu-id="c533a-117">RecurringDayTransition</span></span>](recurringdaytransition.md) <br/> |<span data-ttu-id="c533a-118">Stellt einen Zeitzonenübergang dar, der an demselben Tag jedes Jahr erfolgt.</span><span class="sxs-lookup"><span data-stu-id="c533a-118">Represents a time zone transition that occurs on the same day each year.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c533a-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="c533a-119">Text value</span></span>

<span data-ttu-id="c533a-120">Der Textwert ist ein Integer-Wert, der den Monat darstellt, in dem der Zeitzonenübergang erfolgt.</span><span class="sxs-lookup"><span data-stu-id="c533a-120">The text value is an integer that represents the month in which the time zone transition occurs.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c533a-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c533a-121">Remarks</span></span>

<span data-ttu-id="c533a-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Exchange Server ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="c533a-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c533a-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="c533a-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c533a-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="c533a-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c533a-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c533a-125">Schema Name</span></span>  <br/> |<span data-ttu-id="c533a-126">Schematypen</span><span class="sxs-lookup"><span data-stu-id="c533a-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="c533a-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c533a-127">Validation File</span></span>  <br/> |<span data-ttu-id="c533a-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c533a-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c533a-129">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="c533a-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="c533a-130">False</span><span class="sxs-lookup"><span data-stu-id="c533a-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c533a-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c533a-131">See also</span></span>



- [<span data-ttu-id="c533a-132">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="c533a-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

