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
description: Das DAYOFMONTH-Element beschreibt den Tag in einem Monat, an dem ein wiederkehrendes Element auftritt.
ms.openlocfilehash: dc333a46283d5e8eba3a79f62f8c22c22f56e190
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44442829"
---
# <a name="dayofmonth"></a><span data-ttu-id="5ce27-103">DayOfMonth</span><span class="sxs-lookup"><span data-stu-id="5ce27-103">DayOfMonth</span></span>

<span data-ttu-id="5ce27-104">Das **DAYOFMONTH** -Element beschreibt den Tag in einem Monat, an dem ein wiederkehrendes Element auftritt.</span><span class="sxs-lookup"><span data-stu-id="5ce27-104">The **DayOfMonth** element describes the day in a month that a recurring item occurs.</span></span> 
  
```xml
<DayOfMonth/>
```

<span data-ttu-id="5ce27-105">**int**</span><span class="sxs-lookup"><span data-stu-id="5ce27-105">**int**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="5ce27-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="5ce27-106">Attributes and elements</span></span>

<span data-ttu-id="5ce27-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="5ce27-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5ce27-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="5ce27-108">Attributes</span></span>

<span data-ttu-id="5ce27-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="5ce27-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5ce27-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5ce27-110">Child elements</span></span>

<span data-ttu-id="5ce27-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="5ce27-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5ce27-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5ce27-112">Parent elements</span></span>

|<span data-ttu-id="5ce27-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="5ce27-113">**Element**</span></span>|<span data-ttu-id="5ce27-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5ce27-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5ce27-115">AbsoluteYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="5ce27-115">AbsoluteYearlyRecurrence</span></span>](absoluteyearlyrecurrence.md) <br/> |<span data-ttu-id="5ce27-116">Stellt ein jährliches Serienmuster dar.</span><span class="sxs-lookup"><span data-stu-id="5ce27-116">Represents a yearly recurrence pattern.</span></span>  <br/> |
|[<span data-ttu-id="5ce27-117">AbsoluteMonthlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="5ce27-117">AbsoluteMonthlyRecurrence</span></span>](absolutemonthlyrecurrence.md) <br/> |<span data-ttu-id="5ce27-118">Stellt ein monatliches Serienmuster dar.</span><span class="sxs-lookup"><span data-stu-id="5ce27-118">Represents a monthly recurrence pattern.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5ce27-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="5ce27-119">Text value</span></span>

<span data-ttu-id="5ce27-120">Ein Textwert, der eine ganze Zahl im Bereich von 1 bis 31 darstellt, ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5ce27-120">A text value that represents an integer in the range of 1 to 31 is required.</span></span> <span data-ttu-id="5ce27-121">Wenn dieser Wert für einen bestimmten Monat größer ist als die Anzahl der Tage im Monat, wird der letzte Tag des Monats angenommen.</span><span class="sxs-lookup"><span data-stu-id="5ce27-121">If for a particular month this value is larger than the number of days in the month, the last day of the month is assumed.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5ce27-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5ce27-122">Remarks</span></span>

<span data-ttu-id="5ce27-123">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="5ce27-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5ce27-124">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="5ce27-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5ce27-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="5ce27-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5ce27-126">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="5ce27-126">Schema name</span></span>  <br/> |<span data-ttu-id="5ce27-127">Schematypen</span><span class="sxs-lookup"><span data-stu-id="5ce27-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="5ce27-128">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="5ce27-128">Validation file</span></span>  <br/> |<span data-ttu-id="5ce27-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5ce27-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5ce27-130">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="5ce27-130">Can be empty</span></span>  <br/> |<span data-ttu-id="5ce27-131">False</span><span class="sxs-lookup"><span data-stu-id="5ce27-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5ce27-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5ce27-132">See also</span></span>

- [<span data-ttu-id="5ce27-133">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="5ce27-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

