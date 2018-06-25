---
title: DailyRegeneration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DailyRegeneration
api_type:
- schema
ms.assetid: cafb57e4-c518-45e0-b565-2babd0dab1df
description: Das DailyRegeneration-Element beschreibt die Häufigkeit in Tagen, in denen eine Aufgabe neu erstellt wird.
ms.openlocfilehash: 356f7fd2672b2ad87d17e597c52e9f12273ce3c6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757846"
---
# <a name="dailyregeneration"></a><span data-ttu-id="99db1-103">DailyRegeneration</span><span class="sxs-lookup"><span data-stu-id="99db1-103">DailyRegeneration</span></span>

<span data-ttu-id="99db1-104">Das **DailyRegeneration** -Element beschreibt die Häufigkeit in Tagen, in denen eine Aufgabe neu erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="99db1-104">The **DailyRegeneration** element describes the frequency, in days, in which a task is regenerated.</span></span> 
  
```xml
<DailyRegeneration>
   <Interval/>
</DailyRegeneration>
```

<span data-ttu-id="99db1-105">**DailyRegeneratingPatternType**</span><span class="sxs-lookup"><span data-stu-id="99db1-105">**DailyRegeneratingPatternType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="99db1-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="99db1-106">Attributes and elements</span></span>

<span data-ttu-id="99db1-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="99db1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="99db1-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="99db1-108">Attributes</span></span>

<span data-ttu-id="99db1-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="99db1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="99db1-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="99db1-110">Child elements</span></span>

|<span data-ttu-id="99db1-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="99db1-111">**Element**</span></span>|<span data-ttu-id="99db1-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="99db1-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="99db1-113">Intervall</span><span class="sxs-lookup"><span data-stu-id="99db1-113">Interval</span></span>](interval.md) <br/> |<span data-ttu-id="99db1-114">Definiert das Intervall in Tagen zwischen zwei aufeinander folgenden Terminserien.</span><span class="sxs-lookup"><span data-stu-id="99db1-114">Defines the interval, in days, between two consecutive recurring items.</span></span> <span data-ttu-id="99db1-115">Der Wert muss im Bereich von 1 bis 999.</span><span class="sxs-lookup"><span data-stu-id="99db1-115">The value must be in the range of 1 to 999.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="99db1-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="99db1-116">Parent elements</span></span>

|<span data-ttu-id="99db1-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="99db1-117">**Element**</span></span>|<span data-ttu-id="99db1-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="99db1-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="99db1-119">Serie (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="99db1-119">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="99db1-120">Serieninformationen für wiederkehrende Aufgaben enthält.</span><span class="sxs-lookup"><span data-stu-id="99db1-120">Contains recurrence information for recurring tasks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="99db1-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="99db1-121">Remarks</span></span>

<span data-ttu-id="99db1-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="99db1-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="99db1-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="99db1-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="99db1-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="99db1-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="99db1-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="99db1-125">Schema name</span></span>  <br/> |<span data-ttu-id="99db1-126">Schematypen</span><span class="sxs-lookup"><span data-stu-id="99db1-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="99db1-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="99db1-127">Validation file</span></span>  <br/> |<span data-ttu-id="99db1-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="99db1-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="99db1-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="99db1-129">Can be empty</span></span>  <br/> |<span data-ttu-id="99db1-130">False</span><span class="sxs-lookup"><span data-stu-id="99db1-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="99db1-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="99db1-131">See also</span></span>

- [<span data-ttu-id="99db1-132">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="99db1-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

