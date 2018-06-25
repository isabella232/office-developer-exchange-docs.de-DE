---
title: MonthlyRegeneration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MonthlyRegeneration
api_type:
- schema
ms.assetid: 9a52ca97-a663-41fe-b61a-61d8c53833ca
description: Das MonthlyRegeneration-Element beschreibt die Häufigkeit in Monaten, von denen Aufgabe neu erstellt wird.
ms.openlocfilehash: 3de8ab5a6a2134ad5c596bf2bcb073d881c89746
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830488"
---
# <a name="monthlyregeneration"></a><span data-ttu-id="b67db-103">MonthlyRegeneration</span><span class="sxs-lookup"><span data-stu-id="b67db-103">MonthlyRegeneration</span></span>

<span data-ttu-id="b67db-104">Das **MonthlyRegeneration** -Element beschreibt die Häufigkeit in Monaten, von denen Aufgabe neu erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="b67db-104">The **MonthlyRegeneration** element describes the frequency, in months, of which task is regenerated.</span></span> 
  
```xml
<MonthlyRegeneration>
   <Interval/>
</MonthlyRegeneration>
```

 <span data-ttu-id="b67db-105">**MonthlyRegeneratingPatternType**</span><span class="sxs-lookup"><span data-stu-id="b67db-105">**MonthlyRegeneratingPatternType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b67db-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b67db-106">Attributes and elements</span></span>

<span data-ttu-id="b67db-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b67db-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b67db-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="b67db-108">Attributes</span></span>

<span data-ttu-id="b67db-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="b67db-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b67db-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b67db-110">Child elements</span></span>

|<span data-ttu-id="b67db-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="b67db-111">**Element**</span></span>|<span data-ttu-id="b67db-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b67db-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b67db-113">Intervall</span><span class="sxs-lookup"><span data-stu-id="b67db-113">Interval</span></span>](interval.md) <br/> |<span data-ttu-id="b67db-114">Definiert das Intervall in Monaten zwischen zwei aufeinander folgenden Terminserien.</span><span class="sxs-lookup"><span data-stu-id="b67db-114">Defines the interval, in months, between two consecutive recurring items.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b67db-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b67db-115">Parent elements</span></span>

|<span data-ttu-id="b67db-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="b67db-116">**Element**</span></span>|<span data-ttu-id="b67db-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b67db-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b67db-118">Serie (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="b67db-118">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="b67db-119">Serieninformationen für wiederkehrende Aufgaben enthält.</span><span class="sxs-lookup"><span data-stu-id="b67db-119">Contains recurrence information for recurring tasks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b67db-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b67db-120">Remarks</span></span>

<span data-ttu-id="b67db-121">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="b67db-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b67db-122">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="b67db-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b67db-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="b67db-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b67db-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b67db-124">Schema name</span></span>  <br/> |<span data-ttu-id="b67db-125">Schematypen</span><span class="sxs-lookup"><span data-stu-id="b67db-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="b67db-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b67db-126">Validation file</span></span>  <br/> |<span data-ttu-id="b67db-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b67db-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b67db-128">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="b67db-128">Can be empty</span></span>  <br/> |<span data-ttu-id="b67db-129">False</span><span class="sxs-lookup"><span data-stu-id="b67db-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b67db-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b67db-130">See also</span></span>



- [<span data-ttu-id="b67db-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="b67db-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

