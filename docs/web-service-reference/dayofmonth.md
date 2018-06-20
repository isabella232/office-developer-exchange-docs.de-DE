---
title: DayOfMonth
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DayOfMonth
api_type:
- schema
ms.assetid: 09b7504e-08d8-42f9-88cc-a2a37a2e2b8b
description: DayOfMonth-Element beschreibt den Tag im Monat, den eine Terminserie auftritt.
ms.openlocfilehash: 0d0d95849a2562e06b88872b2857cc5e6ca67af3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757874"
---
# <a name="dayofmonth"></a><span data-ttu-id="ca064-103">DayOfMonth</span><span class="sxs-lookup"><span data-stu-id="ca064-103">DayOfMonth</span></span>

<span data-ttu-id="ca064-104">**DayOfMonth** -Element beschreibt den Tag im Monat, den eine Terminserie auftritt.</span><span class="sxs-lookup"><span data-stu-id="ca064-104">The **DayOfMonth** element describes the day in a month that a recurring item occurs.</span></span> 
  
```xml
<DayOfMonth/>
```

<span data-ttu-id="ca064-105">**int**</span><span class="sxs-lookup"><span data-stu-id="ca064-105">**int**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="ca064-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ca064-106">Attributes and elements</span></span>

<span data-ttu-id="ca064-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ca064-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ca064-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="ca064-108">Attributes</span></span>

<span data-ttu-id="ca064-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="ca064-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ca064-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ca064-110">Child elements</span></span>

<span data-ttu-id="ca064-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="ca064-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ca064-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ca064-112">Parent elements</span></span>

|<span data-ttu-id="ca064-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="ca064-113">**Element**</span></span>|<span data-ttu-id="ca064-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ca064-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ca064-115">AbsoluteYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="ca064-115">AbsoluteYearlyRecurrence</span></span>](absoluteyearlyrecurrence.md) <br/> |<span data-ttu-id="ca064-116">Stellt ein jährliches Serienmuster dar.</span><span class="sxs-lookup"><span data-stu-id="ca064-116">Represents a yearly recurrence pattern.</span></span>  <br/> |
|[<span data-ttu-id="ca064-117">AbsoluteMonthlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="ca064-117">AbsoluteMonthlyRecurrence</span></span>](absolutemonthlyrecurrence.md) <br/> |<span data-ttu-id="ca064-118">Stellt ein monatliches Serienmuster dar.</span><span class="sxs-lookup"><span data-stu-id="ca064-118">Represents a monthly recurrence pattern.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ca064-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="ca064-119">Text value</span></span>

<span data-ttu-id="ca064-120">Ein Textwert, der eine ganze Zahl im Bereich von 1 bis 31 darstellt, ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ca064-120">A text value that represents an integer in the range of 1 to 31 is required.</span></span> <span data-ttu-id="ca064-121">Wenn dieser Wert für einen bestimmten Monat größer als die Anzahl der Tage des Monats ist, wird der letzte Tag des Monats angenommen.</span><span class="sxs-lookup"><span data-stu-id="ca064-121">If for a particular month this value is larger than the number of days in the month, the last day of the month is assumed.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ca064-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ca064-122">Remarks</span></span>

<span data-ttu-id="ca064-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="ca064-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ca064-124">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="ca064-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ca064-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="ca064-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ca064-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ca064-126">Schema name</span></span>  <br/> |<span data-ttu-id="ca064-127">Schematypen</span><span class="sxs-lookup"><span data-stu-id="ca064-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="ca064-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ca064-128">Validation file</span></span>  <br/> |<span data-ttu-id="ca064-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ca064-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ca064-130">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="ca064-130">Can be empty</span></span>  <br/> |<span data-ttu-id="ca064-131">False</span><span class="sxs-lookup"><span data-stu-id="ca064-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ca064-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ca064-132">See also</span></span>

- [<span data-ttu-id="ca064-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="ca064-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

