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
description: Das YearlyRegeneration-Element beschreibt die Häufigkeit in Jahre, in denen eine Aufgabe neu erstellt wird.
ms.openlocfilehash: d034be1ff70e92fd5e96118b9fd1eb3033737f6c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839561"
---
# <a name="yearlyregeneration"></a><span data-ttu-id="1ca4c-103">YearlyRegeneration</span><span class="sxs-lookup"><span data-stu-id="1ca4c-103">YearlyRegeneration</span></span>

<span data-ttu-id="1ca4c-104">Das **YearlyRegeneration** -Element beschreibt die Häufigkeit in Jahre, in denen eine Aufgabe neu erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="1ca4c-104">The **YearlyRegeneration** element describes the frequency, in years, in which a task is regenerated.</span></span> 
  
```xml
<YearlyRegeneratingPatternType>
   <Interval/>
</YearlyRegeneratingPatternType>
```

<span data-ttu-id="1ca4c-105">**YearlyRegeneratingPatternType**</span><span class="sxs-lookup"><span data-stu-id="1ca4c-105">**YearlyRegeneratingPatternType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="1ca4c-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1ca4c-106">Attributes and elements</span></span>

<span data-ttu-id="1ca4c-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1ca4c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1ca4c-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="1ca4c-108">Attributes</span></span>

<span data-ttu-id="1ca4c-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="1ca4c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1ca4c-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1ca4c-110">Child elements</span></span>

|<span data-ttu-id="1ca4c-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="1ca4c-111">**Element**</span></span>|<span data-ttu-id="1ca4c-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1ca4c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1ca4c-113">Intervall</span><span class="sxs-lookup"><span data-stu-id="1ca4c-113">Interval</span></span>](interval.md) <br/> |<span data-ttu-id="1ca4c-114">Definiert das Intervall in Jahre, in denen eine neue Aufgabe nach dem Abschluss des Vorgangs erneut generiert wird.</span><span class="sxs-lookup"><span data-stu-id="1ca4c-114">Defines the interval, in years, during which a new task is regenerated after the completion of the task.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1ca4c-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1ca4c-115">Parent elements</span></span>

|<span data-ttu-id="1ca4c-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="1ca4c-116">**Element**</span></span>|<span data-ttu-id="1ca4c-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1ca4c-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1ca4c-118">Serie (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="1ca4c-118">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="1ca4c-119">Serieninformationen für wiederkehrende Aufgaben enthält.</span><span class="sxs-lookup"><span data-stu-id="1ca4c-119">Contains recurrence information for recurring tasks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1ca4c-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1ca4c-120">Remarks</span></span>

<span data-ttu-id="1ca4c-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="1ca4c-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="1ca4c-122">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="1ca4c-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1ca4c-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="1ca4c-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1ca4c-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="1ca4c-124">Schema Name</span></span>  <br/> |<span data-ttu-id="1ca4c-125">Schematypen</span><span class="sxs-lookup"><span data-stu-id="1ca4c-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="1ca4c-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="1ca4c-126">Validation File</span></span>  <br/> |<span data-ttu-id="1ca4c-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1ca4c-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1ca4c-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="1ca4c-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="1ca4c-129">False</span><span class="sxs-lookup"><span data-stu-id="1ca4c-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1ca4c-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1ca4c-130">See also</span></span>

- [<span data-ttu-id="1ca4c-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="1ca4c-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

