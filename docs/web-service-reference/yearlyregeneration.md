---
title: YearlyRegeneration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- YearlyRegeneration
api_type:
- schema
ms.assetid: 23538bca-738e-4319-944e-f459ff8a7eba
description: Das YearlyRegeneration-Element beschreibt die Häufigkeit in Jahren, in der eine Aufgabe neu generiert wird.
ms.openlocfilehash: 7a6796c433bc54d145d5a769e01f9bba46897735
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457879"
---
# <a name="yearlyregeneration"></a><span data-ttu-id="7a4c5-103">YearlyRegeneration</span><span class="sxs-lookup"><span data-stu-id="7a4c5-103">YearlyRegeneration</span></span>

<span data-ttu-id="7a4c5-104">Das **YearlyRegeneration** -Element beschreibt die Häufigkeit in Jahren, in der eine Aufgabe neu generiert wird.</span><span class="sxs-lookup"><span data-stu-id="7a4c5-104">The **YearlyRegeneration** element describes the frequency, in years, in which a task is regenerated.</span></span> 
  
```xml
<YearlyRegeneratingPatternType>
   <Interval/>
</YearlyRegeneratingPatternType>
```

<span data-ttu-id="7a4c5-105">**YearlyRegeneratingPatternType**</span><span class="sxs-lookup"><span data-stu-id="7a4c5-105">**YearlyRegeneratingPatternType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="7a4c5-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="7a4c5-106">Attributes and elements</span></span>

<span data-ttu-id="7a4c5-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="7a4c5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7a4c5-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="7a4c5-108">Attributes</span></span>

<span data-ttu-id="7a4c5-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="7a4c5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7a4c5-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7a4c5-110">Child elements</span></span>

|<span data-ttu-id="7a4c5-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="7a4c5-111">**Element**</span></span>|<span data-ttu-id="7a4c5-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7a4c5-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7a4c5-113">Intervall</span><span class="sxs-lookup"><span data-stu-id="7a4c5-113">Interval</span></span>](interval.md) <br/> |<span data-ttu-id="7a4c5-114">Definiert das Intervall in Jahren, in dem eine neue Aufgabe nach Abschluss der Aufgabe neu generiert wird.</span><span class="sxs-lookup"><span data-stu-id="7a4c5-114">Defines the interval, in years, during which a new task is regenerated after the completion of the task.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7a4c5-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7a4c5-115">Parent elements</span></span>

|<span data-ttu-id="7a4c5-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="7a4c5-116">**Element**</span></span>|<span data-ttu-id="7a4c5-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7a4c5-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7a4c5-118">Serie (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="7a4c5-118">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="7a4c5-119">Enthält Serieninformationen für wiederkehrende Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="7a4c5-119">Contains recurrence information for recurring tasks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7a4c5-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7a4c5-120">Remarks</span></span>

<span data-ttu-id="7a4c5-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="7a4c5-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="7a4c5-122">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="7a4c5-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7a4c5-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="7a4c5-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7a4c5-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="7a4c5-124">Schema Name</span></span>  <br/> |<span data-ttu-id="7a4c5-125">Schematypen</span><span class="sxs-lookup"><span data-stu-id="7a4c5-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="7a4c5-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="7a4c5-126">Validation File</span></span>  <br/> |<span data-ttu-id="7a4c5-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7a4c5-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7a4c5-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="7a4c5-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="7a4c5-129">False</span><span class="sxs-lookup"><span data-stu-id="7a4c5-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7a4c5-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a4c5-130">See also</span></span>

- [<span data-ttu-id="7a4c5-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="7a4c5-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

